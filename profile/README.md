# GoldSrc.rs Organization

<div align="center">

[![Rust: 2024 Edition](https://img.shields.io/badge/rust-2024_edition-orange.svg?logo=rust&logoColor=orange)](https://doc.rust-lang.org/edition-guide/rust-2024/)
[![License: MIT OR Apache-2.0](https://img.shields.io/badge/license-MIT%20OR%20Apache--2.0-blue.svg)](#license)
[![GitHub](https://img.shields.io/badge/github-goldsrc--rs-181717?logo=github)](https://github.com/goldsrc-rs)

**Next-generation, memory-safe Rust platform and WebAssembly plugin ecosystem for the GoldSrc engine.**  
*First-class specialization for Counter-Strike 1.6 (ReHLDS / ReGameDLL / Metamod / GoldClient).*

</div>

---

## Welcome to GoldSrc.rs

**GoldSrc.rs** is a modern, modular technology platform engineered to replace decades of legacy, unstable, and closed-source server modding tools (such as AMX Mod X / AMXX) with high-performance Rust, sandboxed WebAssembly (Wasmtime Component Model), and pure open-source engineering.

### Core Values & Philosophy

- **Zero-DRM & Zero-Snake-Oil**: Free as in freedom (MIT / Apache-2.0). No obfuscated binaries, no external billing check crashes, and no monopoly licensing lock-ins.
- **Microsecond Systems Craft**: Zero-allocation hot paths, cache-line alignment, and mechanical sympathy.
- **Memory Safety & Process Isolation**: Plugins run in isolated WebAssembly sandboxes. A plugin bug never crashes the dedicated server process.
- **Native UTF-8 Everywhere**: Seamless native internationalization without legacy CP1251 code page corruption.

---

## Ecosystem Repositories

| Repository | Status | Description | Audience |
| :--- | :---: | :--- | :--- |
| [**`goldsrc`**](https://github.com/goldsrc-rs/goldsrc) | ![Active](https://img.shields.io/badge/status-active-brightgreen) | Official facade meta-crate (`use goldsrc::prelude::*;`), Developer CLI (`grs`), and architectural standards hub. | Plugin Authors & Integrators |
| [**`goldsrc-runtime`**](https://github.com/goldsrc-rs/goldsrc-runtime) | ![Active](https://img.shields.io/badge/status-active-brightgreen) | High-performance host engine, Metamod & Standalone C-ABI backends, and Wasmtime Component Model runtime. | Server Administrators & DevOps |
| [**`goldsrc-sdk`**](https://github.com/goldsrc-rs/goldsrc-sdk) | ![Active](https://img.shields.io/badge/status-active-brightgreen) | Pure guest SDK, procedural macros (`#[plugin]`, `#[command]`), SPI contracts, and raw engine FFI bindings. | Plugin Developers |
| [**`goldsrc-plugins-standard`**](https://github.com/goldsrc-rs/goldsrc-plugins-standard) | ![Active](https://img.shields.io/badge/status-active-brightgreen) | Standard production suite of WASM plugins: `administration`, `chat_director`, `map_manager`, `menu_frontend`, `moderation`, `privileges`. | Server Administrators |
| [**`goldsrc-template-plugin-rust`**](https://github.com/goldsrc-rs/goldsrc-template-plugin-rust) | ![Active](https://img.shields.io/badge/status-active-brightgreen) | Canonical template repository for scaffolding new plugins with `cargo generate`. | Plugin Developers |
| [**`goldsrc-game-cstrike`**](https://github.com/goldsrc-rs/goldsrc-game-cstrike) | ![In Progress](https://img.shields.io/badge/status-in_progress-blue) | Counter-Strike 1.6 domain models: weapons, economy, round lifecycle, defuse/bomb typestates, and ReGameDLL hooks. | Game Mode Developers |

---

## Quickstart for Plugin Developers

Scaffold and compile your first GoldSrc WebAssembly plugin in seconds:

```bash
# 1. Install the GoldSrc Developer CLI
cargo install --git https://github.com/goldsrc-rs/goldsrc.git grs

# 2. Add the unified facade crate to your Cargo.toml
# [dependencies]
# goldsrc = { git = "https://github.com/goldsrc-rs/goldsrc.git", branch = "dev" }
```

```rust
use goldsrc::prelude::*;

#[plugin]
pub struct MyPlugin;

impl Plugin for MyPlugin {
    fn on_load(&mut self) -> Result<()> {
        log_info!("MyPlugin initialized on GoldSrc.rs!");
        Ok(())
    }
}
```

---

## Security & Execution Model

1. **WebAssembly Sandboxing (Tier-1)**: Plugins execute within memory-isolated WebAssembly components. Memory limits, CPU instructions, and capability permissions (`#[permissions]`) are strictly enforced by the host.
2. **Deterministic FFI & Crash Containment**: All C-ABI boundaries are wrapped with re-entrant panic barriers (`catch_unwind`), guaranteeing that engine callbacks never cause undefined behavior.
3. **Decoupled Architecture**: Plugins never touch raw server pointers directly; all interactions pass through typed WIT component interfaces.

---

## Getting Involved & Contributing

We welcome community contributions, suggestions, and benchmarks! Check out the [Contributing Guide](CONTRIBUTING.md) and join us in building the next generation of GoldSrc gaming.

---

## Trademark Notice

> [!NOTE]  
> Half-Life, GoldSrc, and Counter-Strike are trademarks and/or registered trademarks of Valve Corporation.  
> GoldSrc.rs is an independent, non-commercial open-source project and is not affiliated with, endorsed by, or sponsored by Valve Corporation or the Rust Foundation.

---

## License

All official GoldSrc.rs projects are dual-licensed under **MIT** OR **Apache-2.0**.
