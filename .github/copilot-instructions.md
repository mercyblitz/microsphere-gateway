# Copilot Instructions

## Build and test commands

- Build all modules: `./mvnw -DskipTests package`
- Run the full test suite: `./mvnw test`
- Run one test class from a leaf module: `./mvnw -pl microsphere-spring-cloud-gateway-server-webflux -am -Dtest=WebEndpointMappingGlobalFilterTest -Dsurefire.failIfNoSpecifiedTests=false test`
- CI also exercises compatibility profiles with commands like `./mvnw -Drevision=0.0.1-SNAPSHOT test -Ptest,coverage,spring-cloud-2021` and the same profile set for `spring-cloud-hoxton` and `spring-cloud-2020`

## High-level architecture

- The root `pom.xml` is a Maven reactor. `microsphere-gateway-parent` imports the Microsphere Spring Cloud BOM, and `microsphere-gateway-dependencies` publishes the BOM that downstream applications import.
- `microsphere-spring-cloud-gateway-commons` contains the shared gateway contract: property constants, conditional annotations, `WebEndpointConfig`, and `WebEndpointConfigurationPropertiesBindHandlerAdvisor`. That advisor injects typed `metadata.web-endpoint` config into bound `spring.cloud.gateway.routes[*]` definitions.
- `microsphere-spring-cloud-gateway-server-webflux` is the runtime module. It registers auto-configuration in both `META-INF/spring.factories` and `META-INF/spring/org.springframework.boot.autoconfigure.AutoConfiguration.imports`, and uses `WebEndpointApplicationContextInitializer` to install the bind-handler advisor before route properties are bound.
- The main runtime feature is web-endpoint routing. Gateway routes that use `uri: we://...` and usually `Path=/{application}/**` are intercepted by `WebEndpointMappingGlobalFilter`, which loads `WebEndpointMapping` metadata from discovered service instances, caches request-mapping candidates per route, rewrites the downstream path, adds the endpoint mapping ID header, and forwards to a load-balanced target instance.
- `GatewayAutoConfiguration` also replaces Spring Cloud Gateway's `FilteringWebHandler` with `CachingFilteringWebHandler`, and wires listeners/interceptors that refresh route state on successful route refreshes, environment changes, and service-instance changes while suppressing heartbeat-triggered refresh noise.

## Key conventions

- The custom route scheme is `we`. `we://all` subscribes to every discovered service; otherwise the URI host names the subscribed services.
- Per-route web-endpoint exclusions live under `spring.cloud.gateway.routes[*].metadata.web-endpoint.excludes` and use Spring request-mapping fields such as `patterns`, `methods`, `params`, `headers`, `consumes`, and `produces`.
- Gateway features are layered behind property-based conditional annotations and default to enabled: `spring.cloud.gateway.enabled`, `microsphere.spring.cloud.gateway.enabled`, and `microsphere.spring.cloud.web-endpoint-mapping.enabled`.
- When changing auto-configuration, keep both registration files in sync: `spring.factories` and `AutoConfiguration.imports`.
- Tests rely on shared YAML fixtures in `src/test/resources/META-INF/config/default/test.yaml`. WebFlux integration-style tests commonly activate the `simple-service-registry,gateway` profiles and use `@EnableWebFluxExtension`.
