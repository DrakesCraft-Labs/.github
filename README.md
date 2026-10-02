<div align="center">

<img src="https://raw.githubusercontent.com/DrakesCraft-Labs/.github/main/profile/assets/new-horizons-banner.svg" alt="Slimefun: New Horizons — Modernizing Slimefun for the next generation of Minecraft" width="100%" />

# Slimefun: New Horizons

### Modernizing Slimefun for the next generation of Minecraft

[![StarSuites](https://img.shields.io/badge/StarSuites-Monorepo-8B5CF6?style=for-the-badge&logo=github&logoColor=white)](https://github.com/DrakesCraft-Labs/Drakes-Suites)
[![Paper](https://img.shields.io/badge/Paper-1.21.11_→_26.x-38BDF8?style=for-the-badge&logo=minecraft&logoColor=white)](https://papermc.io/)
[![Java 21](https://img.shields.io/badge/Java-21_LTS-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://openjdk.org/)
[![Rust](https://img.shields.io/badge/Rust-Off--Heap_SIMD-DEA584?style=for-the-badge&logo=rust&logoColor=white)](https://github.com/DrakesCraft-Labs/Slimefun-Rust)
[![Discord](https://img.shields.io/badge/Discord-Community-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/rv3vtXZTk7)

[🌐 Website](https://web.drakescraft.cl) ·
[💬 Discord](https://discord.gg/rv3vtXZTk7) ·
[🌌 StarSuites](https://github.com/DrakesCraft-Labs/Drakes-Suites) ·
[🧭 All repositories](https://github.com/orgs/DrakesCraft-Labs/repositories) ·
[🇪🇸 Español](README_ES.md)

</div>

---

## What is this?

**Slimefun: New Horizons** is an independent, community-driven effort to carry [Slimefun](https://github.com/Slimefun/Slimefun4) and its addon
ecosystem into the next generation of Minecraft servers: current Paper releases, modern Java, predictable performance, and addons that keep working
instead of being abandoned.

Everything here is battle-tested on a live production network, **DrakesCraft** (`mc.drakescraft.cl`), before it is published.

> ℹ️ **Credit and independence.** Slimefun is an open-source project created by **TheBusyBiscuit** and its community.
> We are **not** its original authors and are **not affiliated with or endorsed by** the official Slimefun team. Our role is modernization and
> rescue: keeping Slimefun and its addons alive on current server software while preserving the original licenses and author credits.

## What we build

| Pillar | What it means | Where to look |
|---|---|---|
| 🧬 **Modern Slimefun core** | A maintained Slimefun port for current Paper (production on **1.21.11**, **26.x** in staging). | `Slimefun4-Drake`, [`Drakes-Suites`](https://github.com/DrakesCraft-Labs/Drakes-Suites) |
| 🌌 **StarSuites** | 180+ scattered addon repositories consolidated into **8 mega-suites** plus the Multiverse suite, with one ticker engine and one module system. | [`Drakes-Suites`](https://github.com/DrakesCraft-Labs/Drakes-Suites) |
| ⚡ **Native acceleration** | Graph, network and energy solving moved off-heap with SIMD, to remove Garbage Collector pauses. | [`Slimefun-Rust`](https://github.com/DrakesCraft-Labs/Slimefun-Rust) |
| 🔗 **Addon interoperability** | Bridges that let independent plugins cooperate while each still works standalone (Networks ↔ MultiverseNets, SlimeTinker ↔ MultiverseTinker). | `NetworksV6-drake`, `SlimeTinker-drake`, `MultiverseNets`, `MultiverseTinker` |
| 🛡️ **Player-data safety** | Item identifiers (PDC keys) are never renamed; migrations are additive and every fix is replicated into the next-generation suites. | Project policy |

## StarSuites at a glance

| Suite | Artifact | Focus |
|---|---|---|
| 0 · Core | `drakes-core.jar` | Kernel, shaded Dough, centralized `SuiteTickerEngine`, JNI bindings, SQLite WAL, audit logs |
| 1 · Tech | `drakes-tech.jar` | Digital logistics (Networks), quantum storage, InfinityExpansion, DynaTech, FastMachines |
| 2 · Bio | `drakes-bio.jar` | GeneticChickengineering, ExoticGarden, Cultivation, SlimyBees |
| 3 · Magic | `drakes-magic.jar` | AlchimiaVitae, Crystamae, RelicsOfCthonia, SoulJars, transmutation |
| 4 · Generators | `drakes-generators.jar` | LiteXpansion, SMG, solar and nuclear reactors, energy cells |
| 5 · Utility | `drakes-utility.jar` | DyedBackpacks, ColoredEnderChests, ChestTerminal, SFCalc, SlimeHUD |
| 6 · Combat | `drakes-combat.jar` | DrakesBosses, SlimeTinker, SlimefunWarfare, reactive armor |
| 7 · Server | `drakes-server.jar` | Star Engine (server kernel), Rust bridge, isolated game modes, dynamic economy |
| Multiverse | `drakes-multiverse.jar` | **Authored by [Chagui68](https://github.com/Chagui68):** MultiverseCreatures, MultiverseNets, MultiverseTinker |

## Roadmap (exploring)

- **Season 2 on Paper 26.x**: atomic rollout of the StarSuites jars after staging validation.
- **Display-based 3D**: pipes and cables drawn with `ItemDisplay`/`BlockDisplay` entities instead of fixed blocks (inspired by the approach used by
  [PylonMC/Rebar](https://github.com/pylonmc/rebar), LGPL-3.0, with attribution).
- **Unified configuration**: one modular YAML folder per suite, hot-reloadable per module.

## Using our artifacts

Maven repository (used by our addons): `https://drakescraft-labs.github.io/maven-repo`. Each repository documents its own coordinates and licence.

## Contributing

1. Active development of consolidated plugins happens in the [`Drakes-Suites`](https://github.com/DrakesCraft-Labs/Drakes-Suites) monorepo.
2. **Never break player data**: no item, inventory or purchase history may be put at risk; PDC keys are preserved.
3. Forks and consolidations **keep their original licenses** (GPL-3.0 / LGPL-3.0 / MIT / Apache-2.0) and credit the original authors.
4. Public READMEs are written in English; Spanish documentation lives alongside as `README_ES.md`.

<div align="center">

**Slimefun: New Horizons** · built with ♥ by the DrakesCraft Labs community<br/>
[Website](https://web.drakescraft.cl) · [Discord](https://discord.gg/rv3vtXZTk7) · [StarSuites](https://github.com/DrakesCraft-Labs/Drakes-Suites)

</div>
