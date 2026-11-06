# Changelog

All notable changes to stuxapis.github.io are documented here.

Each release's sections follow a fixed order: Added, Changed, Fixed, Removed, Security, Deprecated. This project adheres to [Date Versioning](https://datevers.ing) since v26.10.23 (`YY.MM.DD`, the UTC release date, with `-1`, `-2`… for later releases the same day); earlier releases used [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## v26.11.06-1

### Added

- `.github/workflows/ci.yml`, running `bash tests/version.sh` on pushes to `main` and `test` and on every pull request

### Changed

- `commit.sh` and `commit.bat` end by saying to push `test` and open a pull request into `main`
- README (Versioning) and CONTRIBUTING (a new Branches section) describe the `test` branch flow: work and releases happen on `test`, and reach `main` only through a reviewed pull request that needs CI to pass

## v26.11.06

### Changed

- The README header uses the light/dark StuxAPIs logo (`<picture>` with `logo-light.png` and `logo-dark.png`) instead of the plain `logo.png`
- The changelog intro gives the fixed section order (Added, Changed, Fixed, Removed, Security, Deprecated) instead of citing Keep a Changelog, whose order differs

## v26.10.23

### Added

- `tests/version.sh`, which checks that `VERSION.md` is a valid Date Version, a real calendar date not in the future, and the same as the newest entry in this changelog

### Changed

- Switched from Semantic Versioning to [Date Versioning](https://datevers.ing): releases are numbered by their UTC release date as `YY.MM.DD`, with `-1`, `-2`… for later releases the same day. This release follows v1.0.1
- `commit.sh` and `commit.bat` refuse a `VERSION.md` that isn't a valid Date Version or is dated in the future (UTC), and warn when it's dated before today
- `README.md` and `CONTRIBUTING.md` describe Date Versioning and the release steps

## v1.0.1

### Fixed
- GitHub Pages was using the legacy branch-deploy build system, which can silently stop auto-deploying with no error recorded anywhere (discovered on SeasonalOverlaysLibrary — its live site served stale content for over an hour with no visible failure). Switched to GitHub Actions-based Pages deployment (`.github/workflows/pages.yml`), making every deploy an ordinary, observable CI run instead.

## v1.0.0

### Added
- First version-tracked release of this GitHub Pages redirect repo — `VERSION.md`/`CHANGELOG.md`/`CONTRIBUTING.md`/`commit.sh`+`commit.bat` added, following the standard release-flow convention used across other StuxAPIs repos. `README.md`'s header logo already correctly pointed at `https://global.media.stuxapis.net/logo.png` — no content fix needed here, just bringing the repo under version tracking.
