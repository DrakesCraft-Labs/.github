<div align="center">

<img
  src="https://raw.githubusercontent.com/DrakesCraft-Labs/.github/main/profile/assets/labs-hero.svg"
  alt="DrakesCraft Labs"
  width="920"
/>

# DrakesCraft Labs

**Ingeniería de plataforma para Paper, Slimefun y DrakesCraft.**

Construimos, portamos y operamos software que necesita sobrevivir versiones de Minecraft,
cargas reales y mantenimiento continuo. El laboratorio reúne el núcleo de Slimefun Drake,
addons mantenidos y herramientas que respaldan la plataforma DrakesCraft.

<p>
  <a href="https://github.com/DrakesCraft-Labs"><img src="https://img.shields.io/badge/GitHub-DrakesCraft--Labs-181717?style=for-the-badge&logo=github" alt="GitHub"/></a>
  <a href="https://drakescraft.cl"><img src="https://img.shields.io/badge/Platform-DrakesCraft-c9a227?style=for-the-badge" alt="DrakesCraft"/></a>
  <img src="https://img.shields.io/badge/Java-21-F89820?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java 21"/>
  <img src="https://img.shields.io/badge/Paper-1.21.x-00A651?style=for-the-badge&logo=minecraft&logoColor=white" alt="Paper 1.21.x"/>
</p>

<p>
  <a href="https://drakescraft.cl"><strong>Portal</strong></a> ·
  <a href="https://discord.gg/rR7FbfCt9Y"><strong>Discord</strong></a> ·
  <a href="https://github.com/DrakesCraft-Labs/maven-repo"><strong>Maven repository</strong></a>
</p>

</div>

---

## Qué mantenemos

| Área | Proyecto | Responsabilidad |
|---|---|---|
| Núcleo | [**Slimefun4-Drake**](https://github.com/DrakesCraft-Labs/Slimefun4-Drake) | Adaptación y mantenimiento del core para el runtime Drake. |
| Integración | [**drakes-slimefun-labs**](https://github.com/DrakesCraft-Labs/drakes-slimefun-labs) | Laboratorio de migración, compatibilidad y construcción de addons. |
| Addons | [**SlimeTinker-drake**](https://github.com/DrakesCraft-Labs/SlimeTinker-drake) · [**FoxyMachines-drake**](https://github.com/DrakesCraft-Labs/FoxyMachines-drake) | Distribuciones independientes con compatibilidad legacy y builds reproducibles. |
| Redes | [**NetworksV6-drake**](https://github.com/DrakesCraft-Labs/NetworksV6-drake) | Almacenamiento y automatización de redes para Paper 1.21.x. |
| Contenido avanzado | [**Supreme-Drake**](https://github.com/DrakesCraft-Labs/Supreme-Drake) | Integración de contenido endgame dentro del ecosistema Drake. |
| Distribución | [**maven-repo**](https://github.com/DrakesCraft-Labs/maven-repo) | Artefactos Maven consumidos por los proyectos mantenidos. |

## Cómo trabajamos

- **Compatibilidad antes que reemplazos.** Un port no debe invalidar inventarios, recetas, claves PDC ni datos de mundo existentes.
- **Cambios trazables.** Cada build se compila, valida y conserva con una ruta de rollback antes de una ventana de reinicio.
- **Operación real.** Los proyectos se prueban contra una plataforma Paper/Slimefun en funcionamiento, no sólo contra una compilación local.
- **Complejidad con propósito.** Preferimos una integración mantenible a añadir capas que no mejoran la experiencia de jugadores u operadores.

## Stack

`Java 21` · `Paper 1.21.x` · `Slimefun Drake` · `Maven` · `GitHub Actions` ·
`SQLite` · `Docker` · `Linux` · `Cloudflare` · `Tailscale`

El código de esta organización se centra en el plano de ejecución de Minecraft. La infraestructura,
observabilidad, despliegues y automatizaciones de DrakesCraft se mantienen como parte del ecosistema
operativo, con acceso privado por diseño.

## DrakesCraft

DrakesCraft es la plataforma donde estos componentes se integran y validan.

- **Java Edition:** `mc.drakescraft.cl` o `play.drakescraft.cl`
- **Bedrock:** `mc.drakescraft.cl:25571` mediante [Geyser](https://github.com/GeyserMC/Geyser) y Floodgate
- **Comunidad:** [Discord DrakesCraft](https://discord.gg/rR7FbfCt9Y)
- **Portal:** [drakescraft.cl](https://drakescraft.cl)

## Estado de repositorios

Los repositorios con sufijo `-drake`, los proyectos destacados arriba y sus releases/documentación son
la referencia para trabajo activo. Los forks históricos siguen públicos para preservar procedencia y
contexto técnico, pero no deben asumirse como builds recomendados ni como compatibilidad actual.

## Contribuir

Los reportes útiles incluyen versión de Paper, Java, Slimefun Drake, addon afectado, pasos para
reproducir y el error completo. Para cambios de código, abre primero un issue cuando el alcance pueda
afectar datos de jugadores, recetas o compatibilidad entre versiones.

## Dirección

[**JackStar6677-1**](https://github.com/JackStar6677-1) dirige la arquitectura, desarrollo y operación
del ecosistema DrakesCraft.

<div align="center">

**DrakesCraft Labs** · Chile · software mantenible para comunidades y operadores

</div>
