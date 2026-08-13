<div align="center">

<img src="https://raw.githubusercontent.com/DrakesCraft-Labs/.github/main/profile/assets/labs-hero.svg" alt="DrakesCraft Labs" width="920" />

# DrakesCraft Labs

**A production Minecraft engineering lab for Purpur 1.21.11 and Java 21.**

[![Server](https://img.shields.io/badge/Server-mc.drakescraft.cl-42c77a?style=for-the-badge&logo=minecraft&logoColor=white)](https://web.drakescraft.cl)
[![Guide](https://img.shields.io/badge/Player_Guide-Commands_%26_Systems-d9b657?style=for-the-badge)](https://web.drakescraft.cl/guia)
[![Discord](https://img.shields.io/badge/Discord-Community-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/rR7FbfCt9Y)
[![Instagram](https://img.shields.io/badge/Instagram-drakescraft.cl-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/drakescraft.cl/)

</div>

DrakesCraft Labs builds and maintains the software behind **DrakesCraft**: a long-running Java and Bedrock survival server where technology, mythology, magic, bosses, economy, and classic Minecraft coexist without resetting the main world.

This organization contains original products, production hardening, compatibility ports, migration tooling, and research. Repositories are kept independent so a gameplay system can evolve without turning the server core into a monolith.

## Production ecosystem

| Area | Projects | Responsibility |
| --- | --- | --- |
| Server orchestration | [Odysseia](https://github.com/DrakesCraft-Labs/Odysseia) | Store delivery, kits, modalities, cosmetics, moderation, protection policy, and general server workflows. |
| Mythology and magic | [DiosesDrakes](https://github.com/DrakesCraft-Labs/DiosesDrakes), [ArcanaDrakes](https://github.com/DrakesCraft-Labs/ArcanaDrakes) | Pantheons, divine progression, elemental affinities, codices, abilities, and PvE integrations. |
| Boss encounters | [DrakesBosses](https://github.com/DrakesCraft-Labs/DrakesBosses) | Isolated arenas, entry fees, refunds, spectators, boss lifecycle, and rewards. |
| Slimefun platform | [Slimefun4-Drake](https://github.com/DrakesCraft-Labs/Slimefun4-Drake), [NetworksV6-drake](https://github.com/DrakesCraft-Labs/NetworksV6-drake) | Java 21 compatibility core and the production logistics network used by the addon ecosystem. |
| Economy and safety | [sbank](https://github.com/DrakesCraft-Labs/sbank), [DrakesSlimeMarket](https://github.com/DrakesCraft-Labs/DrakesSlimeMarket), [AxGraves-Drakes](https://github.com/DrakesCraft-Labs/AxGraves-Drakes) | Banking, dynamic material markets, audit trails, graves, Soulbound handling, and inventory integrity. |
| Player experience | [drakescraft-web](https://github.com/DrakesCraft-Labs/drakescraft-web), [drakescraft-datapack](https://github.com/DrakesCraft-Labs/drakescraft-datapack), [DrakesTab](https://github.com/DrakesCraft-Labs/DrakesTab) | Storefront, player guide, native dialogs, navigation, and presentation. |

## Maintained addon program

Many Slimefun projects were written for older Minecraft APIs or different cores. We maintain targeted compatibility ports for **Paper/Purpur 1.21.11 and Java 21**, preserving existing item IDs and player data whenever possible.

Current work includes:

- Automation and logistics: Networks, DynaTech, FoxyMachines, SensibleToolbox, ChestTerminal, DankTech2.
- Progression and materials: Supreme, Bump, SlimeCustomizer, SlimeTinker, Cultivation, Gastronomicon.
- Exploration and combat: Galactifun, InfernalExpansion, DemonicExpansion, MagicXpansion, Relics of Cthonia.
- Shared compatibility: GuizhanLib, SefiLib, InfinityLib-Drake, the public [Maven repository](https://github.com/DrakesCraft-Labs/maven-repo), and [porting tools](https://github.com/DrakesCraft-Labs/slimefun-porting-tools).

Maintained ports retain upstream attribution and licensing. A repository being present here does not automatically mean it is enabled in production; releases are tested against the complete server stack before deployment.

## Engineering principles

- **Player data first.** Item IDs, inventories, machines, graves, and economy state are migration constraints, not implementation details.
- **Reversible operations.** Deployments use backups, checksums, staged artifacts, and explicit rollback paths.
- **No hidden updaters or telemetry.** Production artifacts are built, reviewed, and deployed by the server team.
- **Configuration before recompilation.** Balance and operations belong in validated configuration whenever practical.
- **Compatibility with evidence.** A successful build is only the start; full-stack startup logs and gameplay tests decide whether a port is ready.
- **Clear boundaries.** Bosses, divine progression, arcane progression, commerce, and Slimefun infrastructure communicate through narrow APIs.

## Runtime and research

The live platform is centered on **Purpur 1.21.11, Java 21, SQLite, Docker, and Cloudflare Tunnel**, with Geyser/Floodgate support for Bedrock players.

[Slimefun-Rust](https://github.com/DrakesCraft-Labs/Slimefun-Rust), [Odysseia-Rust](https://github.com/DrakesCraft-Labs/Odysseia-Rust), and the FFM/JNI workspaces are **experimental research**, not blanket replacements for the production Java plugins. Native components are promoted only after ABI, lifecycle, shadow-mode, and rollback validation.

## Connect

- Java: `mc.drakescraft.cl`
- Bedrock: `mc.drakescraft.cl:25565`
- Store and public guide: [web.drakescraft.cl](https://web.drakescraft.cl)
- Maintainer: [JackStar6677-1](https://github.com/JackStar6677-1)

<div align="center">

**Built in Chile. Maintained against a real server, real player data, and real production constraints.**

</div>
