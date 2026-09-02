<div align="center">

<img src="https://raw.githubusercontent.com/DrakesCraft-Labs/.github/main/profile/assets/labs-hero.svg" alt="DrakesCraft Labs" width="100%" />

# ✦ DrakesCraft Labs ✦

### High-Performance Minecraft Engineering & Distributed Server Architecture for Purpur 1.21.11 & Java 21

[![Minecraft](https://img.shields.io/badge/Minecraft-1.21.11-7C4DFF?style=for-the-badge&logo=minecraft&logoColor=white)](https://papermc.io/)
[![Purpur](https://img.shields.io/badge/Purpur-1.21.11-FFA000?style=for-the-badge&logo=purpur)](https://purpurmc.org/)
[![Java](https://img.shields.io/badge/Java-21_LTS-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://openjdk.org/)
[![Rust](https://img.shields.io/badge/Rust-2021_Workspace-DEA584?style=for-the-badge&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![Server](https://img.shields.io/badge/Server-mc.drakescraft.cl-00E5FF?style=for-the-badge&logo=minecraft&logoColor=white)](https://web.drakescraft.cl)
[![Discord](https://img.shields.io/badge/Discord-Community-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/rv3vtXZTk7)

**DrakesCraft Labs is the engineering organization responsible for the core infrastructure, gameplay engines, native calculation layers, and 80+ maintained addons powering the [DrakesCraft Network](https://web.drakescraft.cl).**

[🌐 Official Portal](https://web.drakescraft.cl) ·
[📖 Player & Command Guide](https://web.drakescraft.cl/guia-comandos.html) ·
[🛒 Official Store](https://web.drakescraft.cl/store.html) ·
[🏛️ Ecosystem Architecture](#-canonical-architecture--ecosystem-pillars) ·
[💬 Join Discord](https://discord.gg/rv3vtXZTk7)

</div>

---

## 🏛️ About DrakesCraft Labs

**DrakesCraft** is a high-concurrency, long-running survival ecosystem supporting both **Java Edition** and **Bedrock Edition** (via Floodgate/Geyser) without ever resetting player progress or the main world. 

To achieve zero-lag scalability, technical stability, and rich cross-discipline gameplay, DrakesCraft Labs engineers and maintains **a fully modular, decoupled architecture**. Rather than running monolithic mega-plugins, every domain—from transactional commerce and mythological pantheons to technical logistics and instanced combat—runs as an independent, hardened system.

---

## 🗺️ Canonical Architecture & Ecosystem Pillars

```
                                  ┌──────────────────────────────────────────────────┐
                                  │               DRAKESCRAFT LABS                   │
                                  │      High-Performance Minecraft Systems          │
                                  └────────────────────────┬─────────────────────────┘
                                                           │
         ┌─────────────────────────┬───────────────────────┴───────────────────────┬─────────────────────────┐
         ▼                         ▼                                               ▼                         ▼
┌──────────────────┐      ┌──────────────────┐                           ┌──────────────────┐      ┌──────────────────┐
│     ODYSSEIA     │      │   DIOSESDRAKES   │                           │   DRAKESBOSSES   │      │   ARCANADRAKES   │
│ Sovereign Core,  │      │ Divine Pantheon, │                           │ Instanced Arenas,│      │ 6 Elemental Magic│
│ Store Gateway &  │      │ Favor Systems &  │                           │ Dragmas Economy &│      │ Paths, Shrines & │
│ Server Controls  │      │ Altars           │                           │ Mailbox Delivery │      │ Spells Codex     │
└────────┬─────────┘      └────────┬─────────┘                           └────────┬─────────┘      └────────┬─────────┘
         │                         │                                               │                         │
         └─────────────────────────┼───────────────────────────────────────────────┴─────────────────────────┘
                                   │
                                   ▼
         ┌───────────────────────────────────────────────────┐
         │             SLIMEFUN PLATFORM & LOGISTICS         │
         │  Slimefun4-Drake · NetworksV6-drake · 80+ Addons  │
         └─────────────────────────┬─────────────────────────┘
                                   │
                                   ▼
         ┌───────────────────────────────────────────────────┐
         │              RUST COMPUTATION LAYER               │
         │  Slimefun-Rust · Odysseia-Rust (FFM / Project     │
         │  Panama Native Off-JVM Calculations)              │
         └───────────────────────────────────────────────────┘
```

---

## 🌟 The 4 Core Autonomous Pillars

| Pillar Repository | Domain & Purpose | Key Highlights |
|---|---|---|
| **[`Odysseia`](https://github.com/DrakesCraft-Labs/Odysseia)** | **Central Execution Core & Store Gateway** | Idempotent Tebex state machine, SQLite WAL transaction logs, cross-modality inventory protection, 4-tier kit delivery, `/restart30` atomic saving, and horror night environmental events. |
| **[`DiosesDrakes`](https://github.com/DrakesCraft-Labs/DiosesDrakes)** | **Mythological Pantheons & Divine Favor** | 5 active pantheons (Greek, Norse, Celtic, Egyptian, Hindu), favor point accumulation, deity sacrifices, unique blessings, and community Convergence anchors. |
| **[`DrakesBosses`](https://github.com/DrakesCraft-Labs/DrakesBosses)** | **Instanced Arena Encounters & Boss Systems** | Multi-phase custom armor-stand bosses in `drakes_bosses`, Dragmas economy entry fees, anti-griefing arena barriers, and asynchronous mailbox reward dispatch (`/buzon`). |
| **[`ArcanaDrakes`](https://github.com/DrakesCraft-Labs/ArcanaDrakes)** | **Elemental Magic & Spiritual Progression** | 6 elemental affinities (Fire, Water, Earth, Air, Ice, Lightning), meditation shrines, spell grimoires, divine resonance, and custom PvE mechanics. |

---

## ⚙️ Technical Platform & Logistics Engine

The technical foundation of DrakesCraft relies on an enterprise-grade Slimefun4 fork and a hardened logistics network:

- **[`Slimefun4-Drake`](https://github.com/DrakesCraft-Labs/Slimefun4-Drake)** — High-performance Slimefun 4 core optimized for Java 21 and Paper 1.21.11. Features robust thread-safe block persistence, optimized ticker scheduling, and strict memory safety.
- **[`NetworksV6-drake`](https://github.com/DrakesCraft-Labs/NetworksV6-drake)** — The high-throughput item transport, quantum storage, auto-crafting, and energy distribution backbone. Features zero-lag cached inventory resolution, WorldGuard protection caching, and on-the-fly network reconciliation (`/networks doctor` & `/networks reload`).
- **[`Slimefun-Rust`](https://github.com/DrakesCraft-Labs/Slimefun-Rust)** & **[`Odysseia-Rust`](https://github.com/DrakesCraft-Labs/Odysseia-Rust)** — High-performance native Rust 2021 calculation workspaces interfacing with Java 21 via Project Panama (Foreign Function & Memory API) for heavy math, item indexing, and graph operations.

---

## 📦 Maintained Addons & Ecosystem Portfolio

DrakesCraft Labs actively maintains over **80+ curated, ported, and hardened plugins** ensuring 100% compatibility with Paper/Purpur 1.21.11, modern Java 21, and UTF-8 Spanish localization.

```
├── 🤖 Logistics & Automation
│   ├── NetworksV6-drake       # High-throughput transport, quantum vaults & autocrafters
│   ├── ChestTerminal-drake    # Remote centralized chest network access
│   ├── DynaTech-drake         # Advanced technical machinery, generators & materials
│   ├── SensibleToolbox-drake  # Mechanical item filters, pipes & fluid routing
│   ├── FoxyMachines-drake     # High-tier industrial processing & material synthetics
│   └── Automation             # Automated crafting & factory assembly lines
│
├── ⚔️ Bosses, Combat & Legends
│   ├── MultiverseCreatures    # Adaptive bosses (Mahoraga, Dio, Obsidian Sentinel) & relics
│   ├── DrakesBosses           # Instanced boss dimensions, Dragmas fees & loot mailbox
│   ├── Military-Arsenal       # Tactical firearms, turrets & ballistic defense systems
│   ├── MissileWarfare-drake   # Guided missile launchers, radar & defensive interceptors
│   ├── SFPortalGun            # Dual-portal quantum teleportation & gravity manipulation
│   └── RelicsOfCthonia-drake  # Nether abyssal artifacts, catalysts & dark enchantments
│
├── 🔮 Magic, Alchemy & Dimensions
│   ├── ArcanaDrakes           # 6 elemental magic trees, meditation shrines & codices
│   ├── Galactifun2-drake      # Space exploration, rockets, alien planets & oxygen nets
│   ├── Galaxyfun-drake        # Solar generators, stellar progression & celestial drills
│   ├── InfernalExpansion      # Nether thermal alchemy, runic altars & volcanic tech
│   ├── DemonicExpansion       # Soul extraction, demonic rituals & void catalysts
│   ├── MagicXpansion          # Magical wands, soul manipulation & ethereal synthesis
│   └── CrystamaeHistoria-drake# Magical lore books, crystal infusers & arcane research
│
├── 🌾 Agriculture, Cooking & Economy
│   ├── Gastronomicon-drake    # Gourmet culinary recipes, custom kitchenware & buffs
│   ├── Cultivation_Updated    # Enhanced farming, automated harvesters & sprinklers
│   ├── SlimyBees              # Genetic apiculture, resource bees & automated apiaries
│   ├── Drugfun                # Botanical alchemy, brewing distillation & status perks
│   ├── sbank                  # Comprehensive banking system, interest & player loans
│   └── DrakesSlimeMarket      # Dynamic fluctuating material exchange & market trading
│
└── 🛡️ Server Core, Utilities & Identity
    ├── Odysseia               # Sovereign operational core, Tebex gateway & kits
    ├── DrakesCore             # Community essentials, performance utilities & commands
    ├── DrakesCrates           # Animated loot crates with weighted probability
    ├── DrakesRanks            # Tiered visual prefix hierarchy & LP synchronization
    ├── DrakesTab              # Dynamic gradient tablist & scoreboard integration
    └── AxGraves-Drakes        # Secure death graves with Soulbound item protection
```

---

## 🛡️ Production Engineering Standards

All software produced and maintained by DrakesCraft Labs adheres to strict engineering rules:

1. **Player Data Integrity First**: Inventory state, machine locations, land claims, player vaults, and economy ledgers are sacred. Migrations and updates must be 100% backwards-compatible.
2. **Transactional Idempotency**: Commercial transactions utilize state machines with atomic SQLite WAL journaling. Duplicate events, network timeouts, or sudden restarts will never duplicate rewards or drop purchases.
3. **Zero Rogue Telemetry**: External analytics, background pings, and unverified webhooks are systematically stripped from all third-party ports. All telemetry is internal and auditable.
4. **Graceful Maintenance Protocol**: Server maintenance utilizes safe countdowns (`/restart30`) with global warnings and forced disk flushes, ensuring zero rollback on restarts.

---

## 👥 Engineering Leadership & Collaboration

DrakesCraft Labs is driven by a small, focused team combining dedicated solo backend engineering with valued collaborative development:

* **👑 Lead Architect & Systems Operator:** **Jack** ([@JackStar6677-1](https://github.com/JackStar6677-1)) — Leads and executes the server-side architecture, 100+ maintained plugin codebases, Java 21 LTS ports, custom forks, database integrity, Linux SRE infrastructure, and the **SAORI** autonomous operating fleet.
* **🤝 Core Engineering Collaboration:** **Shaggy** — Actively collaborates on core mechanics, gameplay enhancements, technical testing, and feature implementations.
* **🛡️ Community & Moderation Staff:** Supported by our dedicated in-game and Discord staff team who manage player support, community events, and day-to-day player relations.

---

## 🌐 Connect with DrakesCraft

<div align="center">

| Platform | Address / URL |
|---|---|
| **Java Edition** | `mc.drakescraft.cl` (Port: `25565`) |
| **Bedrock Edition** | `mc.drakescraft.cl` (Port: `25565` / Geyser) |
| **Official Web Portal** | [web.drakescraft.cl](https://web.drakescraft.cl) |
| **Command & Player Guide** | [web.drakescraft.cl/guia-comandos.html](https://web.drakescraft.cl/guia-comandos.html) |
| **Official Store** | [web.drakescraft.cl/store.html](https://web.drakescraft.cl/store.html) |
| **Discord Community** | [discord.gg/rv3vtXZTk7](https://discord.gg/rv3vtXZTk7) |
| **Instagram** | [@drakescraft.cl](https://www.instagram.com/drakescraft.cl/) |

<br>

```
  ____                 _                 ____                __ _     _               _             
 |  _ \  _ __   __ _  | | __  ___  ___  / ___|_ __  __ _   / _| |_  | |    __ _  ___| |_   ___  
 | | | || '__| / _` | | |/ / / _ \/ __|| |   | '__|/ _` | | |_| __| | |   / _` |/ __| __| / __| 
 | |_| || |   | (_| | |   < |  __/\__ \| |___| |  | (_| | |  _| |_  | |__| (_| |\__ \ |_ _\__ \ 
 |____/ |_|    \__,_| |_|\_\ \___||___/ \____|_|   \__,_| |_|  \__| |_____\__,_||___/\__(_)___/ 
```

**Engineered with ☕, 🦀, and architectural precision for the DrakesCraft community.**

</div>
