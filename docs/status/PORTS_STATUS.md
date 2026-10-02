# Ports status — 1.21.11 y 26.x (medición en el VPS)

> Generado por `~/ai-hub/scripts/gen_ports_status.sh` el 2026-10-02 desde `~/ai-hub/log/ports/ports_status_raw.csv`.
> **«compila» ≠ «corre».** *Compila* = `mvn -B -fae package` terminó en el VPS con el JDK indicado.
> *Corre* = el plugin arrancó y cargó en un servidor real de esa versión; **esta página no lo certifica**.
> Nada de aquí se llama «portado» hasta que exista prueba de ejecución (staging 26.x / producción 1.21.11).

## Metodología

```bash
# 1.21.11 (JDK 21) — compila + tests
~/ai-hub/scripts/build_seguro.sh 21 <repo> mvn -B -fae package
# 26.x (JDK 25) — compila sin tests
~/ai-hub/scripts/build_seguro.sh 25 <repo> mvn -B -fae -DskipTests \
    -Dpaper.version=26.2.build.129-stable -Djava.version=25 -Dmaven.compiler.release=25 package
```

* Siempre vía `build_seguro.sh` (un solo build a la vez en todo el VPS, `nice`/`ionice`, espera si la carga ≥ 5). Máximo ~450 s de presupuesto por pasada.
* `indeterminado` = el build falló sin llegar a compilar (p. ej. no resolvió dependencias): **no es un no-compila**, hay que repetirlo.
* Los cambios propios de 26.x van a la rama `port-26x` de cada repo, nunca directo a `main`.

## Resumen

| Alcance | Repos | Medidos |
|---|---:|---:|
| Maven (`*-drake`, `Drakes*`, `DiosesDrakes`, `ArcanaDrakes`) | 49 | 3 |
| Gradle | 9 | 9 |
| Sin código fuente en el repo | 28 | 28 |
| **Total** | **86** | **40** |

## Tabla

| repo | build | 1.21.11 compila | 26.x compila | tests | bloqueo / nota |
|---|---|---|---|---|---|
| AlchimiaVitae-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| ArcanaDrakes | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| BentoBox-Drake | gradle | n/a | ⏳ pendiente (gradle) | sin tests | gradle: medir con wrapper |
| BreweryX-Drake | gradle | n/a | ⏳ pendiente (gradle) | sin tests | gradle: medir con wrapper |
| ChestTerminal-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| ColoredEnderChests-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| CompressionCraft-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| CrystamaeHistoria-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| DankTech2-Drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| DiosesDrakes | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| Drakes-Suites | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| DrakesBosses | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| DrakesCore | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| DrakesCrates | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| DrakesLabPresence-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| DrakesMotd | maven | ✅ sí | ✅ sí | sin tests | sin bloqueo |
| DrakesNanotech | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| DrakesRanks | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| DrakesRankup | maven | ✅ sí | ✅ sí | ✅ ok | sin bloqueo |
| DrakesSlimeMarket | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| DrakesTab | maven | ✅ sí | ✅ sí | sin tests | sin bloqueo |
| DrakesTech | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| DrakesTranslate | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| DrakesWorlds | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| DyeBench-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| DynaTech-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| EMCTech-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| ElectricSpawners-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| EssentialsX-Drake | gradle | n/a | ⏳ pendiente (gradle) | sin tests | gradle: medir con wrapper |
| ExcellentEnchants-Drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| ExoticGarden-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| ExtraGear-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| ExtraHeads-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| FlowerPower-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| FluffyMachines-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| FoxyMachines-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| Galactifun2-drake | gradle | n/a | ⏳ pendiente (gradle) | sin tests | gradle: medir con wrapper |
| Galaxyfun-drake | gradle | n/a | ⏳ pendiente (gradle) | sin tests | gradle: medir con wrapper |
| Gastronomicon-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| GeneticChickengineering-Reborn-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| HeadLimiter-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| HotbarPets-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| InfinityExpansion-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| InfinityLib-Drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| Inventory-Rollback-Plus-Drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| KinematicCore-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| LevelledMobs-Drake | gradle | n/a | ⏳ pendiente (gradle) | sin tests | gradle: medir con wrapper |
| LiteXpansion-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| Magic-8-Ball-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| MapJammers-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| MiniBlocks-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| MissileWarfare-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| MobCapturer-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| MoreResearches-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| NetworksV6-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| PotionExpansion-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| ProtectionStones-Drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| Pylon-Drake | gradle | n/a | ⏳ pendiente (gradle) | sin tests | gradle: medir con wrapper |
| Quaptics-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| Rebar-Drake | gradle | n/a | ⏳ pendiente (gradle) | sin tests | gradle: medir con wrapper |
| RelicsOfCthonia-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| S-PlayerWarps-Drake | gradle | n/a | ⏳ pendiente (gradle) | sin tests | gradle: medir con wrapper |
| SaneCrafting-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| SensibleToolbox-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| SfBetterChests-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| SfChunkInfo-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| Simple-Storage-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| SimpleUtils-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| SlimeChem-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| SlimeFrame-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| SlimeTinker-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| Slimefun4-Drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| SlimefunWarfare-Drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| SlimyRepair-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| SlimyTreeTaps-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| SoulJars-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| SoundMuffler-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| SpiritsUnchained-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| Supreme-Drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| TranscEndence-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| VillagerTrade-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| VillagerUtil-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| Wildernether-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |
| WorldEditSlimefun-drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| WorldwideChat-Drake | maven | ⏳ pendiente | ⏳ pendiente | ⏳ pendiente |  |
| luckyblocks-sf-drake | sin-codigo | n/a (sin fuente) | n/a (sin fuente) | n/a | sin codigo fuente en el repo (solo README/docs) |

## Fuente de las mediciones

* CSV crudo: `~/ai-hub/log/ports/ports_status_raw.csv` (repo | jdk21 | tests | jdk26 | bloqueo | fecha UTC).
* Logs completos por repo: `~/ai-hub/log/ports/<repo>-jdk21.log` y `-jdk25.log`.
* Script: `~/ai-hub/scripts/check_ports.sh <repo>` o `--batch <raiz> <regex>`.

## Pendiente evidente

* Repos Gradle: medir con su `gradlew` (no hay Gradle global en el VPS).
* `Drakes-Suites`: reactor de 9 módulos, se mide aparte (ver `ECOSYSTEM_STATUS_2026-10-02.md` §4).
* Ningún resultado de esta tabla certifica *ejecución*; el staging 26.x sigue sin construirse.
