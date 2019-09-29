# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.6.0] - 2019-09-29

## [0.5.1] - 2019-07-16

### Fixed

- Fixed a bug that prevented accessing the GraphiQL interface when subscriptions were not enabled.

## [0.5.0] - 2019-07-12

### Added

- WebSocket subscriptions, configurable with the new `subscriptions` option on `TartifletteApp`.
- Pass extra context to resolvers using the new `context` option on `TartifletteApp`.

## [0.4.0] - 2019-07-04

### Added

- Support for Tartiflette 0.12.x.
- Add a `mount` module with submounting helpers.
- Add `mount.starlette()`.

### Changed

- Due to the new [engine cooking API](https://tartiflette.io/docs/api/engine#cook-your-tartiflette) in Tartiflette 0.12, `TartifletteApp` now includes a startup event handler responsible for building the GraphQL engine. If submounting, it **must** be registered on the parent ASGI app. Helpers in the `mount` module take care of this for you.

### Removed

- Drop support for Tartiflette 0.11.x and below.

## [0.3.0] - 2019-07-03

### Added

- GraphiQL configuration via the `GraphiQL` helper. Options: `path`, `default_query`, `default_headers`, `default_variables`, `template`.

### Changed

- Internal refactoring that leverages more of Starlette's capabilities.
- Documentation improvements.

## [0.2.0] - 2019-06-10

### Added

- Support for `starlette>=0.12` (previously `>=0.12.0b3`).
- Tartiflette is now installed too when installing `tartiflette-starlette`.

### Changed

- The default `path` is now `""` (previously `"/"`).
- The request is now accessible in the GraphQL context via `context["req"]` (previously `context["request"]`).
- If no error occurred, the `errors` field is not present in the response anymore (previously was `None`).

### Fixed

- More robust URL matching on `TartifletteApp`.

## [0.1.1] - 2019-04-28

### Fixed

- Add missing `graphiql.html` package asset.

## [0.1.0] - 2019-04-26

### Added

Features:

- `TartifletteApp` ASGI application.
- Built-in GraphiQL client.

Project-related additions:

- Package setup.
- Changelog.
- Contributing guide.
- README and documentation.

[unreleased]: https://github.com/tartiflette/tartiflette-starlette/compare/0.6.0...HEAD
[0.6.0]: https://github.com/tartiflette/tartiflette-starlette/compare/0.5.1...0.6.0
[0.5.1]: https://github.com/tartiflette/tartiflette-starlette/compare/0.5.0...0.5.1
[0.5.0]: https://github.com/tartiflette/tartiflette-starlette/compare/0.4.0...0.5.0
[0.4.0]: https://github.com/tartiflette/tartiflette-starlette/compare/0.3.0...0.4.0
[0.3.0]: https://github.com/tartiflette/tartiflette-starlette/compare/0.2.0...0.3.0
[0.2.0]: https://github.com/tartiflette/tartiflette-starlette/compare/0.1.1...0.2.0
[0.1.1]: https://github.com/tartiflette/tartiflette-starlette/compare/0.1.0...0.1.1
[0.1.0]: https://github.com/tartiflette/tartiflette-starlette/compare/5a1ecf...0.1.0
