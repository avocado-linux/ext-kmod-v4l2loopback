# Changelog

All notable changes to avocado-ext-kmod-v4l2loopback are documented in this file.
The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

The extension version tracks the upstream
[v4l2loopback](https://github.com/v4l2loopback/v4l2loopback) module release it builds.

## [0.15.3]

### Added
- Initial release: V4L2 loopback kernel module, built from upstream v4l2loopback v0.15.3
  (supports the 2026 kernel 6.18; the earlier v0.13.2 used the removed `setup_timer()` API).
- CI via the shared `avocado-linux/actions` reusable workflows: PR build check
  (`test.yml`) and tag-driven package + publish to the Avocado feed (`release.yml`).
