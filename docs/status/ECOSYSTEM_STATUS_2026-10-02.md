# Ecosystem status — measured 2026-10-02

> Every number in the organization README comes from this page. They were **measured on 2026-10-02**, not estimated. Re-run the commands to update them.
> 🇪🇸 Los números de esta página se midieron el 2026-10-02; los comandos permiten repetirlos.

## 1. Production network (Paper/Purpur 1.21.11)

**Method.** Parsed the live server log (`latest.log`) for `Loading server plugin <name> v<version>` lines.
**Result.** **169 plugins loaded**, 163 with an explicit *Enabling* line in the current boot, **no plugin failed to load** (one non-fatal warning about a Slimefun item
referenced by a custom surprise configuration).

Classification by the version string reported by each plugin (heuristic — a plugin counts as *ours/adapted* when its version carries our branding or an adaptation marker):

| Class | Count | Rule |
|---|---:|---|
| Own or Drake-branded forks/ports | **43** | version contains `Drake`, name starts with `Drakes`, or it is one of our own plugins |
| Adapted without our branding | **21** | version marked `UNOFFICIAL` / `MODIFIED` / `PRIVATE` / `DEV` |
| Third-party, unmodified | **105** | everything else |

<details><summary>Own or Drake-branded (43)</summary>

AxGraves, Bump, ChestTerminal, ColoredEnderChests, CrazyAuctions, DiosesDrakes, DrakesArcana, DrakesBosses, DrakesChatBridge, DrakesCrates, DrakesNanotech, DrakesRankup, DrakesSlimeMarket, DrakesTranslate, DrakesVIPPlusPlus, DyedBackpacks, DynaTech, EcoPower, ElectricSpawners, ExtraGear, FastMachines, FoxyMachines, Galaxyfun, HotbarPets, InfinityExpansion, LiteXpansion, MobCapturer, MultiverseCreatures, MultiverseNets, MultiverseProgramming, Odysseia, PlayerVaultZ, RelicsOfCthonia, SFCalc, SensibleToolbox, SlimeTinker, Slimefun, SlimefunLuckyBlocks, SlimefunWarfare, SlimyTreeTaps, SoulJars, Supreme, sBank
</details>

<details><summary>Adapted without our branding (21)</summary>

BentoBox, BetterChests, DankTech2, DyeBench, EquivalencyTech, GeneticChickengineering, HeadLimiter, IDreamOfEasy, MoreResearches, Netheopoiesis, NotEnoughAddons, ObsidianExpansion, PrivateStorage, SimpleUtils, SlimefunAdvancements, SlimefunOreChunks, SlimyBees, TranscEndence, VillagerTrade, VillagerUtil, WorldEditSlimefun
</details>

## 2. Repositories

| Metric | Value | Method |
|---|---:|---|
| Repositories in the organization | **189** | GitHub API |
| Maintained ports/forks (`*-drake` naming) | **90** | repository names |
| DrakesCraft family (`Drakes*`, `DiosesDrakes`, `ArcanaDrakes`) | **23** | repository names |
| Multiverse family | **5** | repository names |

## 3. Minecraft API targeted by each repository

**Method.** Scanned `pom.xml`, `build.gradle(.kts)` and `gradle.properties` of 179 local clones for the Paper/Spigot/Purpur API version or `minecraft.version`.
75 repositories expose a detectable target:

| Highest API version targeted | Repositories |
|---|---:|
| 26.2 | 1 |
| 26.1.2 | 1 |
| **1.21.11** | **61** |
| 1.21.8 | 1 |
| 1.21.4 | 2 |
| 1.21.1 | 3 |
| 1.20.6 | 2 |
| 1.20.4 | 2 |
| 1.20.1 | 2 |

Repositories already referencing 26.x: `EliteMobs` (fork) and `WorldwideChat-Drake`. The rest of the older-API repositories are the **next porting queue**.

## 4. StarSuites on Paper 26.2

**Method.** `Drakes-Suites`, branch `26.x`, built with the 26.2 API and JDK 25:

```bash
JAVA_HOME=/usr/lib/jvm/java-25-openjdk-amd64 mvn -B -fae -DskipTests \
  -Dpaper.version=26.2.build.129-stable -Djava.version=25 -Dmaven.compiler.release=25 compile
```

**Result.** `BUILD SUCCESS` for all 9 modules (Core, Tech, Bio, Magic, Generators, Utility, Combat, Server, Multiverse), about 90 seconds.

**Limits of this result.**
- It proves the code **compiles** against the 26.2 API. It does **not** prove the plugins **run** on a 26.x server: the staging server currently runs 1.21.11, and unit tests were not executed against 26.2.
- The suites' default `paper.version` is still `1.21.11-R0.1-SNAPSHOT` (production target); 26.2 was passed as an override.

**Modules inside the suites (Phase 2, in progress): 44**

| Suite | Modules |
|---|---|
| Core (1) | GenericSuite |
| Tech (6) | DynaTech, FoxyMachines, Supreme, Nanotech, FluffyMachines, InfinityExpansion |
| Bio (7) | Cultivation, GeneticChickens, FlowerPower, TreeTaps, MobCapturer, ExoticGarden, SlimyBees |
| Magic (4) | RelicsOfCthonia, Crystamae, AlchimiaVitae, SoulJars |
| Generators (6) | LiteXpansion, BetterReactors, SMG, EcoPower, OreChunks, UltimateGenerators |
| Utility (13) | Backpacks, SlimeHUD, SimpleUtils, EnderCarryOn, ChestTerminal, ExtraTools, SoundMuffler, ColoredEnderChests, PortalGun, SFCalc, Trash, VanillaPatPat, NotEnoughAddons |
| Combat (6) | Warfare, ObsidianExpansion, ExtraGear, MobDrops, SlimefunDisc, SlimeTinker |
| Server (1) | DrakesEconomy |

## 5. What is still unknown (and how we will find out)

| Open question | Next step |
|---|---|
| Do the suites **run** on a 26.x server? | Boot a staging server on Paper 26.2 with the 9 suites and run the per-module smoke tests |
| Which of the 90 `-drake` ports compile on 26.x? | Batch-build every port against the 26.2 API and publish the result table here |
| Exact count of "successfully ported" plugins | Define *ported* = builds on the target API **and** loads/enables on a real server of that version; fill this page per version |
