<div align="center">

# DrakesCraft Labs

Official development lab for the DrakesCraft ecosystem.

Focused on Minecraft plugin engineering, Slimefun ecosystem work, Paper tooling, and long-term maintainable server systems.

<p>
  <a href="https://github.com/DrakesCraft-Labs"><img src="https://img.shields.io/badge/GitHub-DrakesCraft--Labs-181717?style=for-the-badge&logo=github" alt="GitHub" /></a>
  <img src="https://img.shields.io/badge/Java-21-F89820?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java 21" />
  <img src="https://img.shields.io/badge/Paper-1.21.11-00A651?style=for-the-badge&logo=minecraft&logoColor=white" alt="Paper 1.21.11" />
  <img src="https://img.shields.io/badge/Open%20Source-Active-2563eb?style=for-the-badge" alt="Open Source Active" />
</p>

</div>

## Overview

DrakesCraft Labs is the public engineering space behind several Minecraft server-side projects, plugin experiments, compatibility ports, and ecosystem maintenance efforts.

This organization currently has two strong public lines:

- active work around the `Drake Framework` and the Slimefun ecosystem on modern Paper builds
- the broader DrakesCraft plugin suite, including core server modules and gameplay systems

Not every repository here is in the same phase. Some are active engineering labs, some are support modules, and some are historical or compatibility-focused snapshots that are still useful as references.

## Current Public Focus

### 1. Slimefun / Drake migration work

The most actively updated public repository right now is:

- [`drakes-slimefun-labs`](https://github.com/DrakesCraft-Labs/drakes-slimefun-labs)

This repo is the migration lab for:

- `Paper 1.21.11`
- `Java 21`
- `Slimefun 6`
- `dev.drake.dough:dough-core:1.3.1-DRAKE`
- large-scale addon porting and validation

Related public repositories in this line:

- [`Slimefun4-1.20.6-Port`](https://github.com/DrakesCraft-Labs/Slimefun4-1.20.6-Port)
- [`Cultivation_Updated`](https://github.com/DrakesCraft-Labs/Cultivation_Updated)
- [`Networks---Better-Compatibility-Unofficial-`](https://github.com/DrakesCraft-Labs/Networks---Better-Compatibility-Unofficial-)
- [`Military-Arsenal-addon-for-Slimefun4`](https://github.com/DrakesCraft-Labs/Military-Arsenal-addon-for-Slimefun4)

### 2. DrakesCraft plugin ecosystem

These repositories represent the broader modular plugin line for the server:

- [`DrakesCore`](https://github.com/DrakesCraft-Labs/DrakesCore)
- [`DrakesWorlds`](https://github.com/DrakesCraft-Labs/DrakesWorlds)
- [`DrakesTech`](https://github.com/DrakesCraft-Labs/DrakesTech)
- [`DrakesCrates`](https://github.com/DrakesCraft-Labs/DrakesCrates)
- [`DrakesRanks`](https://github.com/DrakesCraft-Labs/DrakesRanks)
- [`DrakesTab`](https://github.com/DrakesCraft-Labs/DrakesTab)
- [`DrakesMotd`](https://github.com/DrakesCraft-Labs/DrakesMotd)
- [`MultiverseCreatures`](https://github.com/DrakesCraft-Labs/MultiverseCreatures)

## Active Public Repositories

| Repository | Role | Current relevance |
| :--- | :--- | :--- |
| [`drakes-slimefun-labs`](https://github.com/DrakesCraft-Labs/drakes-slimefun-labs) | Main migration lab | Current flagship public engineering repo. |
| [`Slimefun4-1.20.6-Port`](https://github.com/DrakesCraft-Labs/Slimefun4-1.20.6-Port) | Compatibility port | Useful historical/public release line for `1.20.6`. |
| [`DrakesCore`](https://github.com/DrakesCraft-Labs/DrakesCore) | Core server plugin | Important ecosystem base, but its public description is still tied to `1.20.6`. |
| [`DrakesWorlds`](https://github.com/DrakesCraft-Labs/DrakesWorlds) | World systems | Part of the broader modular server suite. |
| [`DrakesTech`](https://github.com/DrakesCraft-Labs/DrakesTech) | Technical gameplay systems | Part of the broader modular server suite. |
| [`Cultivation_Updated`](https://github.com/DrakesCraft-Labs/Cultivation_Updated) | Active compatibility variant | Public addon-side compatibility work. |
| [`Networks---Better-Compatibility-Unofficial-`](https://github.com/DrakesCraft-Labs/Networks---Better-Compatibility-Unofficial-) | Active compatibility variant | Public addon-side compatibility work. |

## How To Read This Organization

- If you want the most up-to-date public engineering work, start with [`drakes-slimefun-labs`](https://github.com/DrakesCraft-Labs/drakes-slimefun-labs).
- If you are looking for the older public Slimefun compatibility baseline, check [`Slimefun4-1.20.6-Port`](https://github.com/DrakesCraft-Labs/Slimefun4-1.20.6-Port).
- If you are exploring the wider DrakesCraft server plugin suite, start with [`DrakesCore`](https://github.com/DrakesCraft-Labs/DrakesCore) and the related modular repos.
- If a repo looks older, treat it as either a support module, a compatibility branch, or a historical reference unless the README says otherwise.

## Engineering Principles

- performance-conscious server development
- modular plugin architecture
- explicit configuration over hidden magic
- compatibility work that is documented, reproducible, and maintainable
- open repositories that remain useful to other server operators and developers

## Team

- [JackStar6677-1](https://github.com/JackStar6677-1): lead developer, architecture, automation, ecosystem direction
- [Chagui68](https://github.com/Chagui68): core plugin development, compatibility work, technical collaboration

## Language Note

Most public code and documentation here may mix Spanish and English depending on project history and intended audience. Newer public-facing documentation is being normalized progressively.

<div align="center">
  <b>DrakesCraft Labs · Build systems that scale.</b>
</div>
