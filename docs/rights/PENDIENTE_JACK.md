# Repositorios con Licencia y Derechos Pendientes de Decisión de Jack

> Documento generado según la directiva de organización de octubre 2026 (`mision-org-2026-10.md`).
> **Regla dura:** NO añadir archivo `LICENSE` a repositorios clase A candidatos ni a los sin clasificar sin la confirmación explícita de Jack. Ante cualquier duda legal, el repositorio se lista aquí.

---

## 1. Repositorios Clase A Candidatos (Código Original de DrakesCraft)

Estos repositorios contienen código original desarrollado para DrakesCraft. Son candidatos a **All Rights Reserved (ARR)** bajo `templates/rights/LICENSE-ARR.txt`. 
**Estado**: Pendiente confirmación de Jack para agregar formalmente `LICENSE` con texto ARR.

| Repositorio | Paquete Dominante | Slimefun | Propuesta | Acción Requerida |
|---|---|---|---|---|
| **ArcanaDrakes** | `cl.drakescraft.arcana` | No | ARR (Clase A) | Jack confirma si aplica ARR o licencia abierta. |
| **DiosesDrakes** | `cl.drakescraft.diosesdrakes` | No | ARR (Clase A) | Jack confirma si aplica ARR o licencia abierta. |
| **DrakesRankup** | `com.drakescraft.rankup` | No | ARR (Clase A) | Jack confirma si aplica ARR o licencia abierta. |
| **DrakesTranslate** | `cl.drakescraft.translate` | No | ARR (Clase A) | Jack confirma si aplica ARR o licencia abierta. |
| **DrakesVIPPlusPlus** | `com.drakescraft.vip` | No | ARR (Clase A) | Jack confirma si aplica ARR o licencia abierta. |

---

## 2. Repositorios de Autoría Externa Alojados en la Organización (Chagui68)

Proyectos creados o liderados por **Chagui68**. Se mantiene su autoría íntegra y créditos.
**Estado**: Requiere confirmación con Chagui68 de la licencia deseada antes de crear cualquier archivo `LICENSE`.

| Repositorio | Paquete Dominante | Slimefun | Acción Requerida |
|---|---|---|---|
| **Drakes-Suites** | `com.chagui68.multiversenets` | Sí | Monorepo de suites. Varios submódulos son de Chagui68 y otros integran Slimefun (GPL-3.0). Confirmar licenciamiento conjunto. |
| **MultiverseTinker** | `com.chagui68.multiversetinker` | No | Confirmar con Chagui68 si desea GPL-3.0, MIT u otra. |

---

## 3. Derivados de Terceros sin Licencia en el Repo (Verificar Upstream)

Forks o modificaciones de proyectos de terceros que actualmente no tienen archivo `LICENSE` o su licencia upstream no está clara en el repositorio.
**Regla de seguridad**: NO publicar releases ni proyectos en Modrinth hasta confirmar la licencia upstream. Agregar `NOTICE-UPSTREAM.md` citando al autor original.

| Repositorio | Autor / Upstream Detectado | Slimefun | Acción Requerida |
|---|---|---|---|
| **Automation** | `io.github.seggan` | Sí | Verificar upstream de Seggan (habitualmente GPL-3.0). |
| **BentoBox-Drake** | `world.bentobox.bentobox` | Sí | BentoBox upstream es GPL-3.0. Añadir `LICENSE` GPL-3.0 oficial con upstream attribution. |
| **Better-Nuclear-Generator-drake** | `me.CAPS123987.Item` | Sí | Verificar upstream. Por estar ligado a Slimefun, el derivado es GPL-3.0. |
| **BreweryMenu** | `me.figgnus.slimefunaddon` | Sí | Addon de Slimefun: upstream GPL-3.0 por derivación. |
| **Drugfun** | `tsp.drugfun.implementation` | Sí | Upstream TheSilentPro: verificar licencia original. |
| **InvSwitcher-Drake** | `com.wasteofplastic.invswitcher` | No | Upstream BentoBox/tastybento: verificar licencia (habitualmente GPL-3.0). |
| **Inventory-Rollback-Plus** | `com.nuclyon.technicallycoded` | No | Upstream Nuclyon/TechnicallyCoded: verificar licencia original. |
| **Inventory-Rollback-Plus-Drake** | `com.nuclyon.technicallycoded` | No | Fork para DrakesCraft. Requiere verificación de upstream de IRP. |
| **ObsidianExpansion** | `me.lucasgithuber.obsidianexpansion` | Sí | Addon Slimefun: upstream GPL-3.0. |
| **Odysseia** | `org.metamechanists.odysseia` | No | Upstream MetaMechanists: verificar licencia original. |
| **Odysseia-Rust** | `org.metamechanists.odysseia` | No | Módulo Rust acoplado a Odysseia. Verificar licencia. |
| **PlayerVaultZ-Drake** | `com.rugzy.playervaultz` | No | Upstream Rugzy: verificar licencia original. |
| **Slimefun-Disc-drake** | `dev.drake.disc` | Sí | Addon Slimefun de audio: verificar licencia. |
| **VanillaPatPat** | `dev.synapseos.patpat` | No | Upstream SynapseOS: verificar licencia original. |
| **WorldEditSlimefun-drake** | `dev.j3fftw.worldeditslimefun` | Sí | Upstream j3fftw: verificar licencia (habitualmente MIT o GPL-3.0). |
| **WorldwideChat-Drake** | `com.dominicfeliton.worldwidechat` | No | Upstream Dominic Feliton: verificar licencia original. |
| **dough-core** | `dev.drake.dough` | Sí | Fork de `dough` (TheBusyBiscuit): licencia MIT original de dough. |
| **sbank** | `com.spearforge.sBank` | No | Upstream SpearForge: verificar licencia original. |

---

## 4. Paquetes con Nombre Propio pero con Posible Origen Externo (Verificar)

Repositorios que usan paquetes como `me.jackstar.*` o `com.github.jackstar.*` pero podrían ser adaptaciones o forks de plugins existentes.

| Repositorio | Paquete | Slimefun | Acción Requerida |
|---|---|---|---|
| **Coronalis-drake** | `com.github.jackstar` | Sí | Confirmar si es 100% propio o fork de addon de Slimefun. |
| **DrakesCrates** | `me.jackstar.drakescrates` | Sí | Confirmar si deriva de GoldenCrates / CrazyCrates o si es desarrollo desde cero. |
| **DrakesMotd** | `me.jackstar.drakesmotd` | No | Confirmar si es desarrollo original. |
| **DrakesRanks** | `me.jackstar.drakesranks` | No | Confirmar si es desarrollo original. |
| **DrakesTab** | `me.jackstar.drakestab` | No | Confirmar si es desarrollo original. |
| **DrakesTech** | `me.jackstar.drakestech` | Sí | Confirmar derivaciones. |
| **DrakesWorlds** | `me.jackstar.drakesworlds` | No | Confirmar si es desarrollo original. |

---

## 5. Repositorios Sin Código Java / Solo Documentación o Configuración (42 Repositorios)

Repositorios que no contienen archivos `.java` en el árbol actual (son repositorios de documentación, forks sin rama de código clonada, o plantillas):
- `.github` (documentación y perfiles de la org)
- `AlchimiaVitae-drake`, `AllSlimeCustomAddons`, `ColoredEnderChests-drake`, `CompressionCraft-drake`
- `DrakesLabPresence-drake`, `DyeBench-drake`, `EMCTech-drake`, `ElectricSpawners-drake`
- `ExtraGear-drake`, `ExtraHeads-drake`, `HeadLimiter-drake`, `HotbarPets-drake`
- `KinematicCore-drake`, `Magic-8-Ball-drake`, `MapJammers-drake`, `MiniBlocks-drake`
- `MoreResearches-drake`, `PotionExpansion-drake`, `Quaptics-drake`, `SfBetterChests-drake`
- `SfChunkInfo-drake`, `Simple-Storage-drake`, `SlimyRepair-drake`, `SlimyTreeTaps-drake`
- `SpiritsUnchained-drake`, `VillagerTrade-drake`, `VillagerUtil-drake`, `Wildernether-drake`
- `luckyblocks-sf-drake`, etc.

**Acción**: Si solo contienen documentación de DrakesCraft, aplicar atribución de la documentación de la organización sin crear licencias de código falsas. Si son submódulos absorbidos en Drakes-Suites, documentar el mapeo a su módulo suite correspondiente.
