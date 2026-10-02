<div align="center">

<img src="https://raw.githubusercontent.com/DrakesCraft-Labs/.github/main/profile/assets/new-horizons-banner.svg" alt="Slimefun: New Horizons — Modernizando Slimefun para la próxima generación de Minecraft" width="100%" />

# Slimefun: New Horizons

### Modernizando Slimefun para la próxima generación de Minecraft

[🌐 Web](https://web.drakescraft.cl) ·
[💬 Discord](https://discord.gg/rv3vtXZTk7) ·
[🌌 StarSuites](https://github.com/DrakesCraft-Labs/Drakes-Suites) ·
[🇬🇧 English](README.md)

</div>

---

## ¿Qué es esto?

**Slimefun: New Horizons** es un esfuerzo independiente y comunitario para llevar [Slimefun](https://github.com/Slimefun/Slimefun4) y su ecosistema de
addons a la próxima generación de servidores de Minecraft: versiones actuales de Paper, Java moderno, rendimiento predecible y addons que siguen
funcionando en lugar de quedar abandonados.

Todo lo que publicamos se prueba antes en una red de producción real, **DrakesCraft** (`mc.drakescraft.cl`).

> ℹ️ **Crédito e independencia.** Slimefun es un proyecto de código abierto creado por **TheBusyBiscuit** y su comunidad. **No somos sus autores
> originales** ni estamos **afiliados ni respaldados** por el equipo oficial de Slimefun. Nuestro rol es la modernización y el rescate: mantener
> Slimefun y sus addons vivos en software de servidor actual, preservando las licencias originales y el crédito de cada autor.

## Qué construimos

| Pilar | Qué significa | Dónde verlo |
|---|---|---|
| 🧬 **Núcleo Slimefun moderno** | Un port mantenido de Slimefun para Paper actual (producción en **1.21.11**, **26.x** en staging). | `Slimefun4-Drake`, [`Drakes-Suites`](https://github.com/DrakesCraft-Labs/Drakes-Suites) |
| 🌌 **StarSuites** | Más de 180 repositorios de addons dispersos consolidados en **8 mega-suites** más la suite Multiverse, con un solo motor de ticker y un solo sistema de módulos. | [`Drakes-Suites`](https://github.com/DrakesCraft-Labs/Drakes-Suites) |
| ⚡ **Aceleración nativa** | Resolución de grafos, redes y energía fuera del heap con SIMD, para eliminar las pausas del Garbage Collector. | [`Slimefun-Rust`](https://github.com/DrakesCraft-Labs/Slimefun-Rust) |
| 🔗 **Interoperabilidad entre addons** | Puentes que permiten que plugins independientes cooperen y que cada uno siga funcionando solo (Networks ↔ MultiverseNets, SlimeTinker ↔ MultiverseTinker). | `NetworksV6-drake`, `SlimeTinker-drake`, `MultiverseNets`, `MultiverseTinker` |
| 🛡️ **Seguridad de datos de jugadores** | Los identificadores de ítems (claves PDC) nunca se renombran; las migraciones son aditivas y cada arreglo se replica en las suites de nueva generación. | Política del proyecto |

## Hoja de ruta (en exploración)

- **Temporada 2 en Paper 26.x**: despliegue atómico de los jars de StarSuites tras validar en staging.
- **3D basado en displays**: tuberías y cables dibujados con entidades `ItemDisplay`/`BlockDisplay` en lugar de bloques fijos (inspirado en el enfoque de
  [PylonMC/Rebar](https://github.com/pylonmc/rebar), LGPL-3.0, con atribución).
- **Configuración unificada**: una carpeta YAML modular por suite, recargable en caliente por módulo.

## Cómo contribuir

1. El desarrollo activo de los plugins consolidados ocurre en el monorepo [`Drakes-Suites`](https://github.com/DrakesCraft-Labs/Drakes-Suites).
2. **Nunca romper datos de jugadores**: ningún ítem, inventario ni historial de compras puede ponerse en riesgo; se conservan las claves PDC.
3. Los forks y consolidaciones **conservan sus licencias originales** (GPL-3.0 / LGPL-3.0 / MIT / Apache-2.0) y acreditan a los autores originales.
4. Los README públicos se escriben en inglés; la documentación en español vive al lado como `README_ES.md`.

<div align="center">

**Slimefun: New Horizons** · hecho con ♥ por la comunidad de DrakesCraft Labs<br/>
[Web](https://web.drakescraft.cl) · [Discord](https://discord.gg/rv3vtXZTk7) · [StarSuites](https://github.com/DrakesCraft-Labs/Drakes-Suites)

</div>
