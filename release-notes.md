# Release Notes

## v0.1.3

# Release Notes for Version 0.1.3

## New Features
- **Release Automation**: Added automatic release note generation in the Maven publish workflow. ([5be36ca](https://github.com/microsphere-projects/commit/5be36ca))

## Other Changes
- **Dependencies**: Updated parent project and Spring Cloud BOM versions. ([2cbb4d0](https://github.com/microsphere-projects/commit/2cbb4d0))
- **Documentation**: Updated README with latest branch versions. ([0050c6d](https://github.com/microsphere-projects/commit/0050c6d))
- **Build Tools**: Updated Maven wrapper to version 3.9.15. ([cbc93c6](https://github.com/microsphere-projects/commit/cbc93c6))
- **Workflows**: Adjusted GitHub workflow permissions to read-only for contents. ([21abd7c](https://github.com/microsphere-projects/commit/21abd7c))  

## v0.1.4

# Release Notes - Version 0.1.4

## Dependency Updates
- Upgraded parent POM version to `0.1.11`. ([2004256](#))
- Bumped `microsphere-spring-cloud` to `0.1.11`. ([a5cf317](#))

## Documentation
- Updated README to reflect new branch version numbers. ([2fda6c4](#))
- Enhanced release notes and release creation process. ([cd6cebc](#))

## Build and Workflow Enhancements
- Merged `release-1.x` branch into `dev-1.x`. ([fe9a3cf](#))
- Bumped version to the next patch after publishing `0.1.3`. ([0c94a5d](#))

**Full Changelog**: https://github.com/microsphere-projects/microsphere-gateway/compare/0.1.3...0.1.4## v0.1.5

# Release Notes - Version 0.1.5

## Dependency Updates
- Bumped `microsphere-spring-cloud` to version 0.1.12.

## Documentations
- Updated branch names and version references in the `README`.

## Build and Workflow Enhancements
- Added Maven server credentials to the CI workflow.
- Improved Maven workflows by enabling caching and switching `mvnw` with `mvn`.

## Other Changes
- Prepared for the next patch release by bumping the version post 0.1.4.

**Full Changelog**: https://github.com/microsphere-projects/microsphere-gateway/compare/0.1.4...0.1.5## v0.1.6

# Release Notes: Version 0.1.6

## New Features
- Added prompt templates for developer tasks in `.github`. ([c2404ef])
- Set default values in the "explain-code" prompt. ([c81c8f0])

## Documentation
- Revamped `README`: reorganized content and improved usage documentation. ([4f26fb5])
- Added `CONTRIBUTING.md` guide and updated `README`. ([e287e69])
- Included instructions for GitHub Copilot usage. ([d252ae4])

## Dependency Updates
- Upgraded `microsphere-spring-cloud` dependency to `0.1.13`. ([bec3cda])

## Build and Workflow Enhancements
- Merged `release-1.x` into `dev-1.x` for consistency. ([f46a981])

---

*This release includes minor enhancements, documentation updates, and improved workflows to streamline development.* 

**Full Changelog**: https://github.com/microsphere-projects/microsphere-gateway/compare/0.1.5...0.1.6## v0.1.7

# Release Notes - Version 0.1.7

## Dependency Updates
- **Microsphere Spring Cloud**: Upgraded to version `0.1.14`. ([27de74e](#))

## Code Quality Improvements
- Removed duplicate blank lines and trailing whitespace in Java source code for improved readability and cleanliness. ([7520015](#))

## Other Changes
- Version bump to `0.1.7` post `0.1.6` release for continued development. ([8872c33](#)) 

---

**Note**: No new features, documentation updates, bug fixes, or test improvements in this release.

**Full Changelog**: https://github.com/microsphere-projects/microsphere-gateway/compare/0.1.6...0.1.7## v0.1.8

# Release Notes: Version 0.1.8

## Dependency Updates
- Upgraded `microsphere-spring-cloud` to version **0.1.15** for enhanced compatibility and bug fixes. ([4516982](#))

## Build and Workflow Enhancements
- Merged `release-1.x` changes into `dev-1.x` branch for alignment and maintenance. ([328129d](#))
- Updated version to prepare for the next patch after publishing **0.1.7**. ([657ad15](#))

---

**Full Changelog**: https://github.com/microsphere-projects/microsphere-gateway/compare/0.1.7...0.1.8## v0.1.9

# Release Notes - Version 0.1.9

## Other Changes
- **Chore:** Bump version to the next patch after publishing 0.1.8. (`3893088`)

**Full Changelog**: https://github.com/microsphere-projects/microsphere-gateway/compare/0.1.8...0.1.9## v0.1.10

# Release Notes for Version 0.1.10

## New Features
- **WebFlux Support**: Added WebFlux availability condition to enhance compatibility. ([3e91d80](#))

## Test Improvements
- Removed `EnableWebFluxExtension` from tests to streamline the codebase. ([3ec87cf](#))

## Dependency Updates
- Bumped parent and BOM versions to `0.1.19`. ([ebb1658](#))
- Updated `microsphere-spring-cloud` to version `0.1.18`. ([488a05b](#))

## Build and Workflow Enhancements
- Merged `release-1.x` into `dev-1.x` for codebase alignment. ([2c6a3a2](#), [f2127cb](#))
- Adjusted versioning to prepare for the next patch release. ([8631694](#))

**Full Changelog**: https://github.com/microsphere-projects/microsphere-gateway/compare/0.1.9...0.1.10## v0.1.12

# Release Notes - Version 0.1.12

## New Features
- Added support for metadata and condition tests. ([d3dfdf5](#))

## Improvements
### Refactoring
- Refactored web-endpoint bind advisor to use a listener approach. ([6436445](#))

## Dependency Updates
- Updated Spring Cloud parent to version 0.1.20. ([706560f](#))

## Build and Workflow Enhancements
- Merged `release-1.x` into `dev-1.x` for streamlined development. ([2b85cac](#))
- Bumped version to `0.1.12` post `0.1.10` release. ([44cca33](#))

---

**Full Changelog**: https://github.com/microsphere-projects/microsphere-gateway/compare/0.1.10...0.1.12## v0.1.13

# Release Notes for Version 0.1.13

## Dependency Updates
- Updated Microsphere Spring Cloud to `0.1.21`. ([98f81b7](https://github.com/mercyblitz/microsphere-gateway/commit/98f81b7))

## Build and Workflow Enhancements
- Merged `release-1.x` into `dev-1.x` to streamline development. ([78433b9](https://github.com/mercyblitz/microsphere-gateway/commit/78433b9))
- Prepared version bump to next patch after publishing `0.1.12`. ([15e8cde](https://github.com/mercyblitz/microsphere-gateway/commit/15e8cde))

## Other Changes
- Merged contributions from `dev-1.x` branch. ([5185c1e](https://github.com/mercyblitz/microsphere-gateway/commit/5185c1e), [518fcb8](https://github.com/mercyblitz/microsphere-gateway/commit/518fcb8))

**Full Changelog**: https://github.com/microsphere-projects/microsphere-gateway/compare/0.1.12...0.1.13## v0.1.14

```markdown
# Release Notes - Version 0.1.14

## New Features
- Added gateway starter as an optional dependency for enhanced modularity. ([e39daf2](#))

## Bug Fixes
- Fixed base class issues in gateway auto-configuration tests. ([ff15cae](#))

## Improvements
### Gateway Enhancements
- Refined gateway WebFlux conditional wiring for better configurability. ([26c75c6](#))
- Improved gateway availability conditions. ([4cae6e0](#))
- Aligned gateway enable property references for consistency. ([9d80238](#))
- Updated gateway modules to align with new dependencies. ([0616a89](#))

### Dependency Updates
- Upgraded Microsphere Spring Cloud dependency to `0.1.22`. ([e183b87](#))

### Build and Workflow Enhancements
- Merged `release-1.x` into `dev-1.x` to consolidate branches. ([62254e5](#))
- Bumped version to the next patch after publishing `0.1.13`. ([d3c06ca](#))

---
```

**Full Changelog**: https://github.com/microsphere-projects/microsphere-gateway/compare/0.1.13...0.1.14