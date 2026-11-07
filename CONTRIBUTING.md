<p align="center">
  <img src="https://global.media.stuxapis.net/logo.png" height="80" alt="StuxAPIs Logo">
</p>

# Contributing to stuxapis.github.io

This is a minimal GitHub Pages redirect page (`index.html`) that forwards visitors from `stuxapis.github.io` to [github.com/StuxAPIs](https://github.com/StuxAPIs). This document is for anyone working on the redirect page itself.

## Local setup

There's no build step or dependencies — just open `index.html` in a browser, or serve the directory with any static file server, e.g.:

```bash
python3 -m http.server 8000
```

## Project conventions

- Single static `index.html` — no framework, no build step, no backend.
- Keep it minimal; this repo exists only to redirect GitHub Pages traffic.

## Branches

- Work on `test`, or on a branch off it. Never push to `main`
- Changes reach `main` only through a pull request from `test` into `main`, which needs CI to pass and is reviewed and merged by Leo
- Release commits and tags are made on `test` (`git push origin test --tags`) and take effect when the pull request is merged. Merging deploys the redirect to GitHub Pages.

## Versioning

This project uses [Date Versioning](https://datevers.ing). To release:

1. Add a `## vYY.MM.DD` entry at the top of `CHANGELOG.md`, with its sections in this order: Added, Changed, Fixed, Removed, Security, Deprecated.
2. Set `VERSION.md` to the same bare version (no `v`): today's **UTC** date as `YY.MM.DD`, or `YY.MM.DD-1`, `-2`… for later releases the same UTC day. Never a future date. Use UTC, not local time: just after midnight in the UK it is still the previous day in UTC.
3. Run `bash tests/version.sh`.
4. Run `./commit.sh` (or `commit.bat` on Windows). It checks the version, commits and tags `vYY.MM.DD`, and never pushes.

## Before committing

- Open `index.html` in a browser and confirm the redirect fires correctly
