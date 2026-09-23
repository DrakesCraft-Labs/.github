<div align="center">

<img src="https://raw.githubusercontent.com/DrakesCraft-Labs/.github/main/profile/assets/labs-hero.svg" alt="DrakesCraft Labs" width="100%" />

# ✦ DrakesCraft Labs ✦

### Software, mundos y herramientas que nacen de una comunidad

[![DrakesCraft](https://img.shields.io/badge/DrakesCraft-Producto_principal-7C4DFF?style=for-the-badge&logo=minecraft&logoColor=white)](https://web.drakescraft.cl)
[![Java](https://img.shields.io/badge/Java-21_LTS-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://openjdk.org/)
[![Rust](https://img.shields.io/badge/Rust-Workspace-DEA584?style=for-the-badge&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![Community](https://img.shields.io/badge/Discord-Comunidad-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/rv3vtXZTk7)

**DrakesCraft Labs es una organización de creación y mantenimiento de software.**
DrakesCraft es nuestro mundo principal y el lugar donde más probamos ideas, pero
el laboratorio también reúne herramientas, servicios, experimentos de IA,
multimedia e infraestructura que pueden vivir por sí mismos.

[🌐 DrakesCraft](https://web.drakescraft.cl) ·
[💬 Comunidad](https://discord.gg/rv3vtXZTk7) ·
[🧭 Explorar repositorios](https://github.com/orgs/DrakesCraft-Labs/repositories)

</div>

---

## Lo que hacemos

No todos los repositorios de esta organización son plugins de Minecraft, y no
tienen por qué serlo. Organizamos el trabajo alrededor de productos y problemas
reales, no de una sola tecnología.

| Línea | Qué reúne | Ejemplos |
|---|---|---|
| 🎮 **DrakesCraft** | Plugins, contenido, operaciones y herramientas para la red de Minecraft. | [Odysseia](https://github.com/DrakesCraft-Labs/Odysseia), [Slimefun4-Drake](https://github.com/DrakesCraft-Labs/Slimefun4-Drake), [DrakesBosses](https://github.com/DrakesCraft-Labs/DrakesBosses), [drakescraft-web](https://github.com/DrakesCraft-Labs/drakescraft-web) |
| 🧠 **IA y automatización** | Experimentos, componentes y utilidades para asistentes, chat, voz y flujos automáticos. | [javaai-core](https://github.com/DrakesCraft-Labs/javaai-core), [java-chat-ai](https://github.com/DrakesCraft-Labs/java-chat-ai), [voice-java-ai](https://github.com/DrakesCraft-Labs/voice-java-ai) |
| 🌐 **Infraestructura y red** | Herramientas para observar, administrar o proteger servicios y redes. | [IP-Detector](https://github.com/DrakesCraft-Labs/IP-Detector), [maven-repo](https://github.com/DrakesCraft-Labs/maven-repo) |
| 🎵 **Medios y creatividad** | Proyectos de música, contenido interactivo y prototipos audiovisuales. | [YoutubeMusicMachine](https://github.com/DrakesCraft-Labs/YoutubeMusicMachine), [MusicMP3-Downloader](https://github.com/DrakesCraft-Labs/MusicMP3-Downloader) |
| 🧪 **Investigación y prototipos** | Ideas en exploración; no todas son productos terminados ni están destinadas a producción. | Repositorios experimentales y forks de compatibilidad |

## DrakesCraft sigue siendo nuestro corazón

DrakesCraft Labs mantiene el ecosistema técnico que sostiene
[DrakesCraft](https://web.drakescraft.cl): gameplay, economía, automatización,
contenido, web y herramientas de operación. El trabajo de Minecraft se organiza
en repositorios independientes para que cada cambio pueda revisarse, probarse y
liberarse con claridad.

Algunos proyectos relevantes:

- **[Odysseia](https://github.com/DrakesCraft-Labs/Odysseia)** — núcleo operativo,
  eventos, entregas y lógica de comunidad.
- **[StarSuites](https://github.com/DrakesCraft-Labs/Drakes-Suites)** (`Drakes-Suites`) —
  arquitectura maestra que consolida más de 180 micro-addons en suites desacopladas
  con persistencia SQLite WAL, configs modulares y aceleración off-heap en Rust.
  > ℹ️ *Aclaración de Autoría:* Slimefun es una obra open-source creada por **TheBusyBiscuit**
  y su comunidad. DrakesCraft Labs / JackStar no es su creador original, sino el arquitecto de su
  modernización técnica, estabilidad en Paper 1.21.11 y erradicación de pausas de Garbage Collector.
- **Suite Multiverse (por Chagui68)** — autoría y diseño soberano de **Chagui68**
  consolidado en [MultiverseCreatures](https://github.com/DrakesCraft-Labs/MultiverseCreatures) y
  [MultiverseNets](https://github.com/DrakesCraft-Labs/MultiverseNets).
- **[DrakesBosses](https://github.com/DrakesCraft-Labs/DrakesBosses)** — encuentros,
  arenas y recompensas.
- **[Slimefun-Rust](https://github.com/DrakesCraft-Labs/Slimefun-Rust)** — motor nativo
  JNI/FFM para resolver grafos de redes y matrices energéticas off-heap sin GC pauses.
- **[DrakesCrates](https://github.com/DrakesCraft-Labs/DrakesCrates)** y
  **[DrakesRankup](https://github.com/DrakesCraft-Labs/DrakesRankup)** — sistemas de
  progresión y recompensas de la comunidad.
- **[DrakesTab](https://github.com/DrakesCraft-Labs/DrakesTab)** — presentación de
  información del servidor para jugadores.
- **[drakescraft-web](https://github.com/DrakesCraft-Labs/drakescraft-web)** — portal
  web y experiencia pública de la comunidad.

## Cómo leer este laboratorio

- **Producción**: proyectos usados activamente por DrakesCraft o por un servicio
  identificado. Sus cambios requieren revisión, pruebas y plan de reversión.
- **Mantenimiento / compatibilidad**: ports y forks que conservamos para que un
  ecosistema existente siga funcionando en versiones modernas.
- **Experimental**: pruebas, prototipos y aprendizaje. Que un repositorio sea
  público no significa que esté listo para instalarse ni que tenga soporte.

Cada repositorio debería declarar su estado, propósito, licencia y forma de
probarlo. Si falta esa información, se agradecen issues o contribuciones para
dejarlo más claro.

## Principios

1. **El producto manda.** Elegimos la tecnología que resuelve el problema; no
   forzamos todo a Minecraft, Java o un único tipo de proyecto.
2. **No romper datos.** Compras, inventarios, configuraciones y trabajo de la
   comunidad se tratan como información que hay que preservar.
3. **Aprender en público, operar con cuidado.** Los experimentos pueden ser
   abiertos; la producción necesita cambios trazables y reversibles.
4. **Crédito y colaboración.** Mantenemos forks y aportes con atribución,
   licencia y contexto técnico.

## Colaborar

Puedes abrir un issue, proponer una mejora o revisar un proyecto concreto. Para
cambios que afecten DrakesCraft, explica el impacto sobre jugadores, datos y
compatibilidad antes de enviar un pull request.

<div align="center">

**Construimos cosas para jugar, aprender y resolver problemas.**

[DrakesCraft](https://web.drakescraft.cl) · [Discord](https://discord.gg/rv3vtXZTk7) · [Repositorios](https://github.com/orgs/DrakesCraft-Labs/repositories)

</div>
