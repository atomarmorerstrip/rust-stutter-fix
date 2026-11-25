# Changelog

All notable changes to Rust Stutter Fix are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] вЂ” November 2026

### Added

- Frame pacing fix: render-queue tuning and frame-limit profiles that stabilize frame times.
- Stutter logging: per-session recording of frame drops and 1% lows for before/after comparison.
- Input lag reduction: buffering adjustments and CPU-affinity layout for the game process.
- Cache cleanup: one-click clearing of shader and asset cache that accumulates stutter over updates.
- Config backup: timestamped copies of current settings with one-click restore.
- Portable, offline design: single folder, no account, no telemetry, no background process.
- Plain-text activity log covering every applied change.

### Notes

- Native C++ build, 6 MB, no runtime dependencies.
- Windows 10 and Windows 11 (64-bit).
- No administrator rights required for standard operations.

[1.0.0]: https://atomarmorerstrip.github.io/rust-stutter-fix/
