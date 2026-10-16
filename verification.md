# Verificacion

Fecha: 2026-10-16

## Cambio verificado

El periodo del encabezado del dashboard se calcula a partir del primer y ultimo mes disponible en los movimientos; durante la carga muestra `Loading...` y, sin datos, `Period unavailable`.

## Comprobaciones

- `docker compose ps`: frontend y backend activos.
- `docker compose exec frontend npm test`: 7 pruebas aprobadas.
- `docker compose exec frontend npm run build`: compilacion y TypeScript aprobados.
- `docker compose exec backend pytest`: 15 pruebas aprobadas.
- `git diff --check`: sin errores de formato.

## Avisos no bloqueantes

- Vite advierte que el bundle JavaScript supera 500 kB.
- Starlette muestra una advertencia de obsolescencia relacionada con `httpx` en las pruebas.