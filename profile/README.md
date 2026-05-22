<div align="center">

<img
  src="https://raw.githubusercontent.com/DrakesCraft-Labs/.github/main/profile/assets/labs-hero.svg"
  alt="DrakesCraft Labs"
  width="920"
/>

# DrakesCraft Labs

Laboratorio publico de ingenieria alrededor de **Paper**, **Slimefun Drake** y sistemas de servidor mantenibles en produccion.

<p>
  <a href="https://github.com/DrakesCraft-Labs"><img src="https://img.shields.io/badge/GitHub-DrakesCraft--Labs-181717?style=for-the-badge&logo=github" alt="GitHub"/></a>
  <img src="https://img.shields.io/badge/Java-21-F89820?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java 21"/>
  <img src="https://img.shields.io/badge/Paper-1.21.x-00A651?style=for-the-badge&logo=minecraft&logoColor=white" alt="Paper 1.21"/>
  <img src="https://img.shields.io/badge/Rama-main-7c3aed?style=for-the-badge" alt="rama main"/>
</p>

<p>
  <a href="https://discord.gg/rR7FbfCt9Y"><img src="https://img.shields.io/badge/Discord-DrakesCraft-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Discord"/></a>
  <a href="https://drakescraft.cl"><img src="https://img.shields.io/badge/Web-drakescraft.cl-c9a227?style=for-the-badge" alt="Web"/></a>
  <a href="https://github.com/DrakesCraft-Labs/drakes-slimefun-labs"><img src="https://img.shields.io/badge/Monorepo-drakes--slimefun--labs-6d28d9?style=for-the-badge" alt="Monorepo"/></a>
</p>

**Build systems that scale.** · Validacion en servidor real [DrakesCraft](https://drakescraft.cl)

</div>

---

## Proyectos destacados

| Repo | Que es |
|------|--------|
| [**drakes-slimefun-labs**](https://github.com/DrakesCraft-Labs/drakes-slimefun-labs) | Monorepo principal: Slimefun 4 Drake, dough-core, ~80 addons, CI unificado |
| [**NetworksV6-drake**](https://github.com/DrakesCraft-Labs/NetworksV6-drake) | Networks estabilizado para Paper 1.21.11 (anti-dupe, sin autoupdate) |
| [**DrakesCore**](https://github.com/DrakesCraft-Labs/DrakesCore) | Plugin nucleo del servidor DrakesCraft |

Rama estable del lab: **`main`** (Paper 1.21.x, Java 21). Linea experimental 26.x en rama dedicada del monorepo.

---

## Comunidad y servidor (DrakesCraft)

- **Discord:** [discord.gg/rR7FbfCt9Y](https://discord.gg/rR7FbfCt9Y)
- **Web:** [drakescraft.cl](https://drakescraft.cl)

### Java Edition

- **Host:** `mc.drakescraft.cl` (tambien `play.drakescraft.cl`)

### Bedrock ([Geyser](https://github.com/GeyserMC/Geyser))

- **Host:** `mc.drakescraft.cl` · **UDP:** `25571`
- **Auth:** [Floodgate](https://wiki.geysermc.org/floodgate/)
- Wiki: [wiki.geysermc.org](https://wiki.geysermc.org/)

### Discord ↔ Minecraft ([DiscordSRV](https://github.com/DiscordSRV/DiscordSRV))

Chat global y presencia enlazados; en juego: **`/discord`**. Docs: [docs.discordsrv.com](https://docs.discordsrv.com/).

---

## Ecosistema Slimefun (mapa)

### Nucleo y portes

- [**drakes-slimefun-labs**](https://github.com/DrakesCraft-Labs/drakes-slimefun-labs) — reactor Maven + Gradle, foundry, releases
- [**NetworksV6-drake**](https://github.com/DrakesCraft-Labs/NetworksV6-drake/releases) — almacenamiento en red (fork Chagui / Netex / Sefiraat)
- [**Slimefun4-1.20.6-Port**](https://github.com/DrakesCraft-Labs/Slimefun4-1.20.6-Port) — linea historica 1.20.6

### Satelite / compatibilidad

- [Cultivation_Updated](https://github.com/DrakesCraft-Labs/Cultivation_Updated)
- [Networks---Better-Compatibility-Unofficial-](https://github.com/DrakesCraft-Labs/Networks---Better-Compatibility-Unofficial-) (legacy; ver NetworksV6-drake)
- [Military-Arsenal-addon-for-Slimefun4](https://github.com/DrakesCraft-Labs/Military-Arsenal-addon-for-Slimefun4)

### Suite modular servidor (`Drakes*`)

[DrakesCore](https://github.com/DrakesCraft-Labs/DrakesCore) · [DrakesWorlds](https://github.com/DrakesCraft-Labs/DrakesWorlds) · [DrakesTech](https://github.com/DrakesCraft-Labs/DrakesTech) · [DrakesCrates](https://github.com/DrakesCraft-Labs/DrakesCrates) · [DrakesRanks](https://github.com/DrakesCraft-Labs/DrakesRanks) · [DrakesTab](https://github.com/DrakesCraft-Labs/DrakesTab) · [DrakesMotd](https://github.com/DrakesCraft-Labs/DrakesMotd) · [MultiverseCreatures](https://github.com/DrakesCraft-Labs/MultiverseCreatures)

---

## Como leer esta organizacion

1. **Ingenieria activa:** empieza por [drakes-slimefun-labs](https://github.com/DrakesCraft-Labs/drakes-slimefun-labs).
2. **Networks en produccion:** [NetworksV6-drake](https://github.com/DrakesCraft-Labs/NetworksV6-drake) (rama `main`, releases con JAR).
3. **Plugins del servidor:** suite `Drakes*` — revisa README y version MC de cada repo.

## Principios

- Rendimiento medido en servidor real, no solo en compilacion.
- Arquitectura modular y configuracion explicita.
- Compatibilidad documentada y reproducible (CI + smoke cuando aplica).
- Codigo abierto util para operadores y desarrolladores.

## Equipo

- [**JackStar6677-1**](https://github.com/JackStar6677-1) — arquitectura, automatizacion, direccion del ecosistema.
- [**Chagui68**](https://github.com/Chagui68) — plugins, compatibilidad, validacion en produccion.

## Idioma

Documentacion y codigo mezclan **espanol e ingles** segun historial del proyecto; la documentacion nueva del monorepo se normaliza de forma incremental.

<div align="center">

**DrakesCraft Labs** · Chile · [drakescraft.cl](https://drakescraft.cl)

</div>
