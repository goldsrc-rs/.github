# GoldSrc.rs Organization

[![Rust: 2024 Edition](https://img.shields.io/badge/rust-2024_edition-orange.svg?logo=rust&logoColor=orange)](https://doc.rust-lang.org/edition-guide/rust-2024/)
[![License: MIT OR Apache-2.0](https://img.shields.io/badge/license-MIT%20OR%20Apache--2.0-blue.svg)](#license)
[![GitHub](https://img.shields.io/badge/github-goldsrc--rs-181717?logo=github)](https://github.com/goldsrc-rs)

> Next-generation, memory-safe Rust framework and WebAssembly plugin ecosystem for GoldSrc engine modding, with first-class (Tier-1) specialization for **Counter-Strike 1.6 (ReHLDS / ReGameDLL / GoldClient)**.

Welcome to the **GoldSrc.rs** organization! We are building next-generation modding infrastructure for the GoldSrc engine (Half-Life 1, Counter-Strike 1.6, Team Fortress Classic, Day of Defeat, Sven Co-op).

## 🏛️ Ecosystem Overview & Project Matrix

| Project | Status | Description |
| :--- | :---: | :--- |
| [**goldsrc-rs**](https://github.com/goldsrc-rs/goldsrc-rs) | ![Active](https://img.shields.io/badge/status-active-brightgreen) | Core engine framework, FFI bindings, Dual backends (Metamod/Standalone), and WASM Host runtime. |
| [**goldsrc-game-cstrike**](https://github.com/goldsrc-rs/goldsrc-game-cstrike) | ![In Progress](https://img.shields.io/badge/status-in_progress-blue) | First-class Counter-Strike 1.6 domain models: weapons, money, round events, defuse/bomb, and player typestates. |
| [**cargo-goldsrc (grs)**](https://github.com/goldsrc-rs/cargo-goldsrc) | ![Planned](https://img.shields.io/badge/status-planned-lightgrey) | Dedicated dual CLI tool (cargo goldsrc / grs) for scaffolding, live watching, building, packaging (.gsp), and deployment. |
| [**goldsrc-plugins-standard**](https://github.com/goldsrc-rs/goldsrc-plugins-standard) | ![Planned](https://img.shields.io/badge/status-planned-lightgrey) | Official standard WASM plugin suite: modular Admin system, colored Chat & prefixes, player Stats (SQLite WAL), and Menus. |
| [**goldsrc-coreutils**](https://github.com/goldsrc-rs/goldsrc-coreutils) | ![Planned](https://img.shields.io/badge/status-planned-lightgrey) | POSIX shell diagnostic utilities (ls, cat, grep, 	ail, wc, sort) for ReHLDS console powered by uutils/coreutils. |
| [**goldsrc-host-csharp**](https://github.com/goldsrc-rs/goldsrc-host-csharp) | ![Planned](https://img.shields.io/badge/status-planned-lightgrey) | Dynamic Native AOT / .NET runtime host for high-performance C# GoldSrc plugins. |
| [**goldsrc-host-python**](https://github.com/goldsrc-rs/goldsrc-host-python) | ![Planned](https://img.shields.io/badge/status-planned-lightgrey) | Dynamic Python 3.x runtime host with @plugin, @command, and @event decorators. |
| [**docs**](https://github.com/goldsrc-rs/docs) | ![In Progress](https://img.shields.io/badge/status-in_progress-blue) | Official documentation, tutorials, API guides, and website for [docs.goldsrc.rs](https://docs.goldsrc.rs). |

## 🔒 Security & Execution Models

1. **WebAssembly Plugins (Safe & Sandboxed)**: Memory-safe execution in an isolated WASM sandbox with declarative granular permissions (#[permissions]), safe hot-reloading, and zero crash risk for the server process.
2. **Native Host Extensions (Trusted Native Execution)**: Full-speed native .dll / .so libraries executing with direct process privileges for specialized hardware/OS integrations.

## 🤝 Getting Involved & Contributing

All repositories welcome contributions! Check out the [Contributing Guide](https://github.com/goldsrc-rs/goldsrc-rs/blob/main/CONTRIBUTING.md) and [Roadmap](https://github.com/goldsrc-rs/goldsrc-rs/blob/main/ROADMAP.md) in the main repository.

## ⚖️ Trademark Notice

> [!NOTE]
> Half-Life, GoldSrc, and the Half-Life logo are trademarks and/or registered trademarks of Valve Corporation.  
> GoldSrc.rs is an independent, non-commercial open-source project and is not affiliated with, endorsed by, or sponsored by Valve Corporation or Rust Foundation.

## 📄 License

All official GoldSrc.rs projects are dual-licensed under **MIT** and **Apache-2.0**.
