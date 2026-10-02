# Estado del Servidor de Pruebas (Staging) - Temporada 2 (Paper 26.2 / 26.x)

## 1. Topología y Entorno de Ejecución
- **Host**: Star VPS (migración completada)
- **Ruta de Trabajo**: `/home/jack/workspace/season2-staging`
- **Motor**: Paper 26.2 (`26.2-129-9240f58`)
- **Runtime Java**: OpenJDK 25.0.4.1 LTS (`/usr/lib/jvm/java-25-openjdk-amd64`)
- **Configuración de Red**:
  - `server-ip=127.0.0.1` (Aislamiento total, solo accesible localmente / Tailscale)
  - `server-port=25566`
  - `online-mode=false` (Alineado con staging)
  - `white-list=true` / `enforce-whitelist=true`
- **Gestión Systemd**:
  - Unidad de usuario: `saori-staging-s2.service`
  - Slice: `Slice=saori-agentes.slice`
  - Cuotas: `CPUQuota=200%`, `MemoryMax=6G`
  - Parámetros JVM: `-Xms1G -Xmx4G -XX:+UseG1GC -jar paper-26.2-129.jar --nogui`
  - Política de ciclo de vida: Se levanta exclusivamente para pruebas y se apaga al finalizar (`1 servidor de pruebas a la vez`).

---

## 2. Monorepo Drakes-Suites (Rama `26.x`)
- **Repositorio**: `/home/jack/workspace/drakescraft/Drakes-Suites`
- **Compilador Seguro**: `~/ai-hub/scripts/build_seguro.sh 25` (control de carga y límites de memoria del VPS)
- **Maven Centralizado**: `https://maven.drakescraft.cl`
- **Pruebas Unitarias**: 25/25 en verde en `DrakesCore` (`CommandModalityGateTest`, `NativeEngineBridgeTest`, `SuiteDatabaseEngineTest`, `SuiteTickerEngineTest`, `CrossVersionAdapterTest`, `SuiteItemPdcBridgeTest`, `SlimefunWorldFilterTest`, `PurpurRuntimeProviderTest`).
- **Construcción Reactor**: 10/10 módulos compilados con éxito en 3m 23s.

---

## 3. Matriz de Plugins en Staging (Smoke Test en Ejecución)

| Plugin / Módulo | Origen | Versión | Carga OK | Diagnóstico / Notas |
| :--- | :--- | :--- | :---: | :--- |
| **DrakesCore** | Drakes-Suites (`26.x`) | 2.0.0-26.X-SNAPSHOT |  SÍ | Kernel, SQLite WAL, Telemetría y Ticker Centralizado activos |
| **DrakesCombat** | Drakes-Suites (`26.x`) | 2.0.0-26.X-SNAPSHOT |  SÍ | Módulos de combate cargados e inicializados |
| **DrakesTech** | Drakes-Suites (`26.x`) | 2.0.0-26.X-SNAPSHOT |  SÍ | Integraciones tecnológicas y addons absorbidos |
| **DrakesGenerators** | Drakes-Suites (`26.x`) | 2.0.0-26.X-SNAPSHOT |  SÍ | Generadores de materiales y energía |
| **DrakesUtility** | Drakes-Suites (`26.x`) | 2.0.0-26.X-SNAPSHOT |  SÍ | NotEnoughAddons & Terraria Tools activos |
| **DrakesMagic** | Drakes-Suites (`26.x`) | 2.0.0-26.X-SNAPSHOT |  SÍ | 12 submódulos mágicos (AlchimiaVitae, Crystamae, Relics, SoulJars, Netheopoiesis, TranscEndence, SpiritsUnchained, DemonicExpansion, ElementManipulation, MagicXpansion, SlimeChem, Coronalis, InfernalExpansion) |
| **DrakesMultiverse** | Drakes-Suites (`26.x`) | 2.0.0-26.X-SNAPSHOT |  SÍ | 30 recetas de crafteo Bukkit registradas |
| **DrakesBio** | Drakes-Suites (`26.x`) | 2.0.0-26.X-SNAPSHOT |  SÍ | Módulos biológicos y flora habilitados |
| **DrakesServer** | Drakes-Suites (`26.x`) | 2.0.0-26.X-SNAPSHOT |  SÍ | Gestión de bóvedas y utilidades de servidor |
| **Slimefun** | Dallas (`Slimefun4-Drake`) | 11.0-Drake-1.21.11-SNAPSHOT |  SÍ | 554 ítems, 257 investigaciones, 1615 recetas |
| **PlaceholderAPI** | PlaceholderAPI upstream | 2.12.3 | SÍ | Prueba real 2026-10-02 17:33 CLT: habilitado en Paper 26.2; la versión upstream declara soporte 26.2 experimental. SHA-256: `fde03259f5af6938f3c33eeb4d814000a1adabf1d2304ce14970be81f609a437`. |
| **DeluxeMenus** | Dallas (`BASE_PLUGINS_TO_SYNC`) | 1.14.1-Release | SÍ, con límite | Prueba real 2026-10-02 17:33 CLT: se enganchó correctamente a PlaceholderAPI y Vault; cargó 3 menús. Las opciones NBT heredadas (`nbt_int`, `nbt_ints`, `nbt_string`, `nbt_strings`) no tienen hook NMS en 26.2. |
| **LuckPerms** | Dallas (`BASE_PLUGINS_TO_SYNC`) | 5.5.17 |  SÍ | Almacenamiento H2, ganchos Vault registrados |
| **Vault** | Dallas (`BASE_PLUGINS_TO_SYNC`) | 1.7.3-b131 |  SÍ | Proveedor de economía y permisos enlazado |
| **BentoBox** | Dallas (`BASE_PLUGINS_TO_SYNC`) | 3.17.0-SNAPSHOT-LOCAL |  SÍ | Gancho con Vault y Slimefun activo, módulo de protección reflection OK |
| **Essentials** | Dallas (`BASE_PLUGINS_TO_SYNC`) | 2.22.0 |  SÍ | 46.312 ítems cargados, proveedores Paper 1.21+ activos |
| **EssentialsChat** | Dallas (`BASE_PLUGINS_TO_SYNC`) | 2.22.0 |  SÍ | Integración con chat |
| **EssentialsSpawn** | Dallas (`BASE_PLUGINS_TO_SYNC`) | 2.22.0 |  SÍ | Manejo de spawn |
| **ProtocolLib** | Dallas (`BASE_PLUGINS_TO_SYNC`) | 5.4.0 |  SÍ | Interceptor de paquetes activo |
| **packetevents** | Dallas (`BASE_PLUGINS_TO_SYNC`) | 2.13.0 |  SÍ | Inicializado para Paper 26.2 |
| **QuickShop-Hikari** | Dallas (`BASE_PLUGINS_TO_SYNC`) | 6.2.0.11 |  SÍ | Base de datos SQLite inicializada, gancho Vault OK |
| **DecentHolograms** | Dallas (`BASE_PLUGINS_TO_SYNC`) | 2.10.1 |  SÍ | Adaptador NMS v26_2 inicializado |
| **CMILib** | Dallas (`BASE_PLUGINS_TO_SYNC`) | 1.5.9.3 |  SÍ | Detección Mojang Mappings v26_2_0 OK |
| **spark** | Staging (`spark`) | 1.10.119 |  SÍ | Profiler de rendimiento en segundo plano |
| **DrakesWorlds** | Repo `DrakesWorlds` (`003529d`) | 1.0 |  SÍ | Prueba puntual 2026-10-02 15:15 CLT: carga y genera `drakes_wild` (perfil `wild_natural`) sin excepciones. Retirado tras la prueba: reescribe `level-name` y `bukkit.yml` al habilitarse |

---

## 4. Última verificación integrada

- El servicio `saori-staging-s2.service` inició con JDK 25 y alcanzó `Done` en 83.163 s el 2026-10-02 a las 17:33 CLT.
- PlaceholderAPI 2.12.3 eliminó el fallo anterior de dependencia: DeluxeMenus quedó habilitado, enlazado con PlaceholderAPI y Vault, y cargó sus tres menús. Esta es una prueba de ejecución en staging; no implica despliegue ni compatibilidad declarada para Dallas.
- Persisten incompatibilidades independientes para seguir triando: Slimefun-Rust usa el fallback Java por ausencia de su biblioteca nativa, EssentialsX emite aviso de versión no soportada y DeluxeMenus limita cuatro opciones NBT heredadas. No se presentan como resueltas.
- El servicio se detuvo limpiamente al terminar la prueba; su pico fue 2.0 GiB de memoria y 2 min 57 s de CPU. No hubo cambios en Dallas.

## 5. Próximos Pasos (Fase 2 de Temporada 2)
1. Absorción y verificación de addons secundarios de Slimefun pendientes en las StarSuites (manteniendo invariantes de IDs y claves PDC).
2. Sincronización de configuraciones de modalidades de juego (SkyBlock, OneBlock, Clásico, Survival) en solo-lectura desde producción.
3. Smoke test exhaustivo in-game y preparación del plan atómico de despliegue a Dallas con escalado a Jack.
