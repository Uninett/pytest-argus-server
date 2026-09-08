# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.4.0] - 2026-09-08

### Removed

- Explicit support for Python 3.9 and 3.10 was dropped. The minimum supported version is now Python 3.11.

### Changed

- Relaxed the exact pin on `pytest-docker-compose-v2` to `>=0.2.0`. The old `==0.1.1` pin transitively capped pytest below 8 for every consumer of this plugin, since that release declares `pytest>=7.2.2,<8` (fixes #5). Consumers are now free to use pytest 8 and 9.
- Raised the stale `pytest>=6.2.0` lower bound to `>=7.2.2`, matching what `pytest-docker-compose-v2` itself requires. Verified against those exact minimums.

### Added

- Python 3.13 and 3.14 added to the test matrix, and declared via trove classifiers.
- A proper changelog was added.
