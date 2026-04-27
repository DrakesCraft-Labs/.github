<div align="center">

# DrakesCraft Labs

Laboratorio público de ingeniería alrededor de **Paper**, **Slimefun** y sistemas de servidor mantenibles.

<p>
  <a href="https://github.com/DrakesCraft-Labs"><img src="https://img.shields.io/badge/GitHub-DrakesCraft--Labs-181717?style=for-the-badge&logo=github" alt="GitHub" /></a>
  <img src="https://img.shields.io/badge/Java-21-F89820?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java 21" />
  <img src="https://img.shields.io/badge/Paper-1.21.x-00A651?style=for-the-badge&logo=minecraft&logoColor=white" alt="Paper 1.21" />
  <img src="https://img.shields.io/badge/Open%20Source-Active-2563eb?style=for-the-badge" alt="Open Source" />
</p>

<p>
  <a href="https://discord.gg/rR7FbfCt9Y"><img src="https://img.shields.io/badge/Discord-DrakesCraft-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Discord DrakesCraft" /></a>
  <a href="https://drakescraft.cl"><img src="https://img.shields.io/badge/Web-drakescraft.cl-7c3aed?style=for-the-badge" alt="Web" /></a>
</p>

</div>

## Comunidad y servidor (DrakesCraft)

- **Discord (oficial):** [discord.gg/rR7FbfCt9Y](https://discord.gg/rR7FbfCt9Y) — anuncios, normas y contacto con staff.
- **Web:** [drakescraft.cl](https://drakescraft.cl)

### Java (Minecraft: Java Edition)

- **Dirección:** `mc.drakescraft.cl` (también se usa `play.drakescraft.cl` según el cliente).

### Chat Minecraft ↔ Discord ([DiscordSRV](https://github.com/DiscordSRV/DiscordSRV))

En el servidor de referencia el chat global, entradas/salidas, estado y mensajes similares se enlazan con Discord mediante **DiscordSRV**; los jugadores suelen usar **`/discord`** para ver la invitación y enlazar cuenta. Documentación del plugin: [docs.discordsrv.com](https://docs.discordsrv.com/).

### Bedrock ([Geyser](https://github.com/GeyserMC/Geyser))

- **Dirección:** `mc.drakescraft.cl`
- **Puerto Bedrock (UDP):** `25571` (listener Geyser en el despliegue actual).
- **Autenticación Bedrock → Java:** [Floodgate](https://wiki.geysermc.org/floodgate/) (`auth-type: floodgate` en Geyser).
- Nombre visible en cliente Bedrock: **DrakesCraft** (MOTD secundario configurado junto a la odisea Java & Bedrock).

Guías oficiales: [wiki Geyser](https://wiki.geysermc.org/) · [Discord GeyserMC](https://discord.gg/geysermc).

---

## Proyecto principal

El **eje actual** de la organización es el monorepo **[`drakes-slimefun-labs`](https://github.com/DrakesCraft-Labs/drakes-slimefun-labs)**:

- **Slimefun 4 (fork Drake)**, **dough-core**, parches internos y **decenas de addons** en un solo reactor **Maven + Gradle**
- Baseline **Paper 1.21.x** y **Java 21**; rama estable **`1.21-latin`**; línea experimental **26.x** en rama dedicada (no mezclar bases sin acuerdo; ver README del monorepo)
- **CI**, smoke, documentación y matriz de módulos en el propio repo

Si quieres ver **qué está pasando ahora** en el laboratorio, empieza ahí.

## Otras líneas públicas

### Slimefun / compatibilidad (repos satélite)

Repos históricos o de compatibilidad que siguen siendo referencia:

- [`Slimefun4-1.20.6-Port`](https://github.com/DrakesCraft-Labs/Slimefun4-1.20.6-Port)
- [`Cultivation_Updated`](https://github.com/DrakesCraft-Labs/Cultivation_Updated)
- [`Networks---Better-Compatibility-Unofficial-`](https://github.com/DrakesCraft-Labs/Networks---Better-Compatibility-Unofficial-)
- [`Military-Arsenal-addon-for-Slimefun4`](https://github.com/DrakesCraft-Labs/Military-Arsenal-addon-for-Slimefun4)

### Suite modular DrakesCraft (servidor)

Módulos del ecosistema **DrakesCraft** en el servidor (core, mundos, gameplay, etc.); **no sustituyen** al monorepo como “proyecto central” de ingeniería abierta hoy, pero siguen siendo parte del mapa:

- [`DrakesCore`](https://github.com/DrakesCraft-Labs/DrakesCore), [`DrakesWorlds`](https://github.com/DrakesCraft-Labs/DrakesWorlds), [`DrakesTech`](https://github.com/DrakesCraft-Labs/DrakesTech), [`DrakesCrates`](https://github.com/DrakesCraft-Labs/DrakesCrates), [`DrakesRanks`](https://github.com/DrakesCraft-Labs/DrakesRanks), [`DrakesTab`](https://github.com/DrakesCraft-Labs/DrakesTab), [`DrakesMotd`](https://github.com/DrakesCraft-Labs/DrakesMotd), [`MultiverseCreatures`](https://github.com/DrakesCraft-Labs/MultiverseCreatures)

## Mapa rápido

| Repositorio | Rol |
| :--- | :--- |
| [`drakes-slimefun-labs`](https://github.com/DrakesCraft-Labs/drakes-slimefun-labs) | **Monorepo principal** (Slimefun Drake + addons + CI) |
| [`Slimefun4-1.20.6-Port`](https://github.com/DrakesCraft-Labs/Slimefun4-1.20.6-Port) | Línea pública / histórica 1.20.6 |
| [`DrakesCore`](https://github.com/DrakesCraft-Labs/DrakesCore) | Core del servidor (suite modular) |

## Cómo leer esta organización

1. **Ingeniería actual y porte masivo:** [`drakes-slimefun-labs`](https://github.com/DrakesCraft-Labs/drakes-slimefun-labs).
2. **Baseline antiguo Slimefun 1.20.6:** [`Slimefun4-1.20.6-Port`](https://github.com/DrakesCraft-Labs/Slimefun4-1.20.6-Port).
3. **Plugins del servidor DrakesCraft:** suite `Drakes*` enlazada arriba; revisa el README de cada repo para fase y versión de Minecraft.

## Principios

- Rendimiento y servidor real.
- Arquitectura modular y configuración explícita.
- Compatibilidad documentada y reproducible.
- Repos abiertos útiles para otros operadores y desarrolladores.

## Equipo

- [JackStar6677-1](https://github.com/JackStar6677-1): liderazgo técnico, arquitectura, automatización, dirección del ecosistema.
- [Chagui68](https://github.com/Chagui68): desarrollo de plugins, compatibilidad, colaboración técnica.

## Idioma

Parte del código y de la documentación mezcla **español e inglés** según historia del proyecto y audiencia. La documentación nueva del monorepo se va normalizando de forma incremental.

<div align="center">
  <b>DrakesCraft Labs · Build systems that scale.</b>
</div>
