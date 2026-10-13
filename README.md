<div align="center">

# DevSweep: node_modules Cleaner & Dev Cache Cleanup Tool

**Free up tens of GBs in seconds. Find and delete `node_modules`, `dist`, `build`, `.next`, `.cache`, `__pycache__`, `target` and other disposable folders across all your old projects, with one click.**

[![Release](https://img.shields.io/github/v/release/SupervisorExpiate86/devsweep-node-modules-cleaner?style=flat-square)](https://github.com/YOUR_USERNAME/devsweep-node-modules-cleaner/releases)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows-blue?style=flat-square)](#installation)
[![Stars](https://img.shields.io/github/stars/SupervisorExpiate86/devsweep-node-modules-cleaner?style=flat-square)](https://github.com/SupervisorExpiate86/devsweep-node-modules-cleaner/stargazers)

[Download](#installation) · [Features](#features) · [How it works](#how-it-works) · [FAQ](#faq) · [Contributing](#contributing)

![DevSweep screenshot](/DevSweep.png)

</div>

---

## Why DevSweep?

If you have been a developer for more than a year, your disk is full of forgotten `node_modules` folders, old build outputs and package caches. A single `node_modules` can weigh **hundreds of MB**; across dozens of old projects that is **tens of GB** of pure waste.

**DevSweep** is a portable, single-file desktop app that scans your drives, shows exactly what can be safely removed, and frees the space in one click. No installer, no dependencies, no command line.

## Features

- **One portable `.exe`**: download, run, done. No installation or runtime required.
- **Fast recursive scan** of any folder or whole drive.
- **Detects 20+ disposable folder types**: see the [full list](#supported-folders).
- **Sorted by size**: biggest space hogs first.
- **Last-modified age filter**: only show projects untouched for 30 / 90 / 180+ days.
- **Safe by design**: preview before delete, optional move to Recycle Bin, ignore list for projects you care about.
- **Smart detection**: only removes folders when a matching project file exists (e.g. `node_modules` next to `package.json`).
- **Dry-run mode**: see how much space you would free without deleting anything.
- **Drag & drop** folders to scan.
- **Dark / light theme.**
- **Open source (MIT)** and free forever.

## Supported folders

| Ecosystem | Folders cleaned |
|---|---|
| Node.js / JavaScript | `node_modules`, `.npm`, `.yarn/cache`, `.pnpm-store` |
| Frontend builds | `dist`, `build`, `out`, `.next`, `.nuxt`, `.svelte-kit`, `.parcel-cache`, `.turbo`, `.vite`, `.angular` |
| Python | `__pycache__`, `.venv`, `venv`, `.pytest_cache`, `.mypy_cache`, `.tox`, `*.egg-info` |
| Rust | `target` |
| Java / Kotlin | `.gradle`, `build`, `target` |
| .NET | `bin`, `obj` |
| PHP | `vendor` |
| Generic | `.cache`, `.tmp`, `coverage` |

> Missing something? [Open an issue](../../issues/new/choose) or send a pull request.

## Installation

1. Go to the [**Releases**](https://github.com/SupervisorExpiate86/devsweep-node-modules-cleaner/releases/latest) page.
2. Download `DevSweep.zip`.
3. Extract it.
4. Run the .exe file. That's it.

> **Windows SmartScreen / antivirus warning?** The app is not code-signed yet, so Windows may show a warning for unknown publishers. The full source code is in this repository and you can build the exe yourself (see [Building from source](#building-from-source)).

## How it works

1. **Choose a folder** (or drag & drop it): for example `C:\Projects`.
2. **Click Scan.** DevSweep finds all disposable folders and shows their size.
3. **Select** what you want to remove (or use *Select all older than 90 days*).
4. **Click Clean.** Space is freed instantly.

Tip: every `node_modules` can be restored at any time with `npm install`, `yarn` or `pnpm install`.

## Safety

DevSweep only targets **regenerable** folders: dependencies, build output and caches. It never touches your source code.

- Preview list before any deletion
- Dry-run mode
- Optional Recycle Bin instead of permanent delete
- Ignore list (`.devsweepignore`)
- Skips system folders and anything outside the selected path

## Building from source

```bash
git clone https://github.com/YOUR_USERNAME/devsweep-node-modules-cleaner.git
cd devsweep-node-modules-cleaner

# Add your build commands here, for example:
# dotnet publish -c Release -p:PublishSingleFile=true
# pyinstaller --onefile src/main.py
# cargo build --release
```

## FAQ

**Is it safe to delete `node_modules`?**
Yes. It is fully regenerated from `package.json` and your lockfile with `npm install`.

**How much space can I free?**
Most developers recover between 5 and 50+ GB.

**Does it work with pnpm, Yarn and Bun?**
Yes. It deletes folders, so it works regardless of the package manager.

**Will it delete my source code?**
No. Only the folders in the [supported list](#supported-folders), and only after you confirm.

**Does it send any data?**
No. DevSweep works fully offline and collects no telemetry.

**Windows only?**
The first release targets Windows. Linux and macOS builds are on the [roadmap](#roadmap).

## Roadmap

- [ ] Linux and macOS builds
- [ ] Command-line mode for scripts and CI
- [ ] Scheduled automatic cleanup
- [ ] Custom rules editor
- [ ] Code signing
- [ ] Multi-language UI

## Contributing

Contributions are welcome! Read [CONTRIBUTING.md](CONTRIBUTING.md), then open an issue or a pull request. If DevSweep saved you disk space, a star on the repo helps other developers find it.

## License

[MIT](LICENSE) © SupervisorExpiate86

---

<sub>Keywords: node_modules cleaner, delete node_modules, clean node_modules, free disk space, developer disk cleanup, build cache cleaner, dist folder cleaner, npm cache cleaner, pycache cleaner, portable exe, Windows developer tools.</sub>
