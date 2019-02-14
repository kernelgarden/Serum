# Serum Changelog

## Unreleased Changes

### Changed

- Serum now tries to compile the project codes (in `lib/`)
  when the user invokes `mix serum.build` or `mix serum.server` task.

## v0.8.1 &mdash; 2019-02-13

### Fixed

- Now `serum.gen.post` generates well-formed tags header.

### Added

- Added missing `mix serum` task.

## v0.8.0 &mdash; 2019-02-13

### Changed

- Installation method has changed.
  - escript is no longer used. Install `serum_new` archive from external
    source (e.g. Hex) and run `mix serum.new` to create a new Serum project.
  - A Serum project is also a Mix project, with `serum` added as a dependency.
    Run `mix do deps.get, deps.compile` to install Serum under that project.
  - Then existing Serum tasks will be available as Mix tasks.
    (e.g. `mix serum.build`, etc.)

- Due to the above change, every Serum project now requires its own
  `mix.exs` file.

## v0.7.0 &mdash; 2019-02-12

### Added

- An optional project property `server_root` is added in `serum.json`.
- A list of image URLs (relative to `@site.server_root`) are available through
  `@page.images` in `base`, `list`, `page`, `post` templates and includes.

### Changed

- Regex pattern requirement for `base_url` project property has changed.
  Now it must start and end with a slash (`/`).

## v0.6.1 &mdash; 2019-01-01

### Changed

- Changed the minimum Elixir version requirement from 1.4 to 1.6.

## v0.6.0 &mdash; 2019-01-01

### Changed

- Massive internal refactoring
- Minor performance optimization

## v0.5.0 &mdash; 2018-12-11

- Initial version; began changelog tracking.