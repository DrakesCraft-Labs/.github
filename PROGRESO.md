# PROGRESO

## Tarea 1 — Inventario (hecha, solo lectura)
- 182 repos no archivados clonados (--depth 1). Detalle: `docs/status/INVENTARIO_2026-10-02.csv`.
- Con `drakescraft-labs.github.io/maven-repo`: **81** (esperado ~86).
- Con `github.com/DrakesCraft-Labs`: **135**; con `raw.githubusercontent.com/DrakesCraft-Labs`: **115**; JitPack `com.github.DrakesCraft-Labs`: **2**.
- Sin archivo LICENSE: **86** repos.
- Diferencias con lo esperado (86 / 153): el conteo se hizo solo sobre archivos de texto rastreados <2 MB; el listado de la org visible para la sesión tiene 185 repos (3 archivados), no 189.

## Tareas 2–5 — NO iniciadas (bloqueos)
1. **Acceso de escritura**: la sesión solo tiene autorizado `DrakesCraft-Labs/.github`. Los demás repos se leen por el proxy pero el push da 403 hasta añadirlos con `add_repo`.
2. **`maven.drakescraft.cl` no verificable**: desde esta sesión el host responde 403 del proxy de salida, no del sitio. Según la regla, nada va a main; todo iría a rama `maven-dominio` + PR en borrador.
3. `gh` tiene un token inválido; no hay API de organización (solo endpoints por repo).
4. Tarea 5 requiere JDK 25 y descargar Paper 26.2 desde hosts que el proxy puede no permitir.
