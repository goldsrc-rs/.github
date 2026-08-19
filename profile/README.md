# GoldSrc.rs Organization

[![Rust: 2021 Edition](https://img.shields.io/badge/rust-2021_edition-orange.svg?logo=rust&logoColor=orange)](https://doc.rust-lang.org/edition-guide/rust-2021/)
[![License: MIT OR Apache-2.0](https://img.shields.io/badge/license-MIT%20OR%20Apache--2.0-blue.svg)](#license)
[![GitHub](https://img.shields.io/badge/github-goldsrc--rs-181717?logo=github)](https://github.com/goldsrc-rs)

> A modern, memory-safe Rust framework and WebAssembly plugin runtime for GoldSrc engine modding.

Welcome to the **GoldSrc.rs** organization! We are building next-generation modding infrastructure for the GoldSrc engine (Half-Life 1, Counter-Strike 1.6, Team Fortress Classic, Day of Defeat, Sven Co-op).

---

## Ecosystem & Repositories

| Repository | Status | Description |
| :--- | :--- | :--- |
| **[goldsrc-rs](https://github.com/goldsrc-rs/goldsrc-rs)** | 🟢 Active | Core workspace: safe API traits, Metamod & Standalone backends, Wasmtime JIT host, ECS framework, and unified tooling. |
| **[goldsrc-cstrike](https://github.com/goldsrc-rs)** | ⏳ Planned | Counter-Strike 1.6 game-specific extension crate (weapons, player state, bomb/hostage entities). |
| **[wasm-plugin-template](https://github.com/goldsrc-rs)** | ⏳ Planned | cargo generate starter template for authoring sandboxed WASM plugins. |
| **[docs](https://github.com/goldsrc-rs)** | ⏳ Planned | Comprehensive architecture guides, API reference, and plugin author tutorials. |

---

## Core Philosophy

1. **Memory Safety & Panic Isolation:** No server crashes from plugin segfaults. All plugin code is sandboxed in WebAssembly with catch_unwind FFI barriers.
2. **True Hot-Reloading:** Compile and reload .wasm plugins on live dedicated servers in milliseconds with zero map changes or player disconnects.
3. **Ergonomic Rust SDK:** Modern ECS (Entity Component System), typed entity handles, vector math, and event buses.
4. **Dual Backend Compatibility:** Operates seamlessly via Metamod-r or as a standalone direct GameDLL proxy.

---

## Getting Involved & Contributing

All repositories welcome contributions! Check out the [Contributing Guide](https://github.com/goldsrc-rs/goldsrc-rs/blob/dev/CONTRIBUTING.md) and [Roadmap](https://github.com/goldsrc-rs/goldsrc-rs/blob/dev/ROADMAP.md) in the main repository.

---

## License

All official GoldSrc.rs projects are dual-licensed under **MIT** and **Apache-2.0**.
