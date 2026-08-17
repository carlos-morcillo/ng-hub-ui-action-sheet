# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0/).

## [0.0.2] - 2026-08-17

### Fixed

- **The package shipped without its licence notice.** `package.json` declared MIT, but no `LICENSE` file travelled in the tarball — and MIT itself requires the copyright notice to be included in distributions. The notice ships now.

## [0.0.1] - 2026-06-17

### Added

- Initial pre-release scaffold of the `ng-hub-ui-action-sheet` package.
- Placeholder `ActionSheet` standalone component (selector `lib-action-sheet`) exported
  from the public API to bootstrap the package.
- Package metadata: MIT license, description, keywords, and repository information.
- English (`README.md`) and Spanish (`README.es.md`) documentation describing the current
  pre-release state and the planned action sheet API.
