# Changelog

All notable changes to avocado-ext-kmod-v4l2loopback are documented in this file.
The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

Up to 0.15.3 the extension version tracked the upstream
[v4l2loopback](https://github.com/v4l2loopback/v4l2loopback) release it builds. From
0.16.0 it is the extension's own version; each entry names the upstream release.

## [0.16.0]

### Changed
- Builds upstream v4l2loopback v0.15.4 (was v0.15.3).
- `supported_targets: '*'`: the module compiles against the target's own
  `kernel-devsrc` at build time, so it is no longer limited to a hand-kept list.
  The old list named the pre-rename Jetson `-devkit` targets, which the 2024 feed
  dropped. A target whose kernel does not provide `kernel-module-videodev` still
  fails at install.
- The version no longer mirrors upstream: republishing needs a new version, and
  upstream owns the next patch number.
- `test.yml` gains the 2026 leg, matching `release.yml`.

## [0.15.3]

### Added
- Initial release: V4L2 loopback kernel module, built from upstream v4l2loopback v0.15.3
  (supports the 2026 kernel 6.18; the earlier v0.13.2 used the removed `setup_timer()` API).
- CI via the shared `avocado-linux/actions` reusable workflows: PR build check
  (`test.yml`) and tag-driven package + publish to the Avocado feed (`release.yml`).
