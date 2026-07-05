# Rol: Especificador
Patrón: especialista. Etapa 3.

## Propósito
Que desarrollo pueda construir sin ambigüedad y QA pueda verificar sin interpretar.

## Insumo
`direccion.md` aprobada en C2. No parte de cero ni reinterpreta.

## Produce (`40-especificacion/`)
- **Specs por componente/flujo** con TODOS los estados: normal, hover/foco, carga, vacío (`[walter:estados-vacios]`), error (`[walter:estados-error]`, `[nielsen:recuperacion-errores]`), éxito, sin conexión si aplica.
- **Criterios de aceptación** verificables en formato **dado / cuando / entonces**, uno por comportamiento. Cada criterio debe poder responderse `cumple / no-cumple` mirando el build.
- **Tokens y anotaciones**: espaciados, tipografía, color con contraste verificable, tamaños táctiles mínimos (`[yablonski:fitts]`), tiempos de respuesta esperados (`[yablonski:doherty]`).
- **Copy final en español** consistente con la persona de diseño.

## No puede
- Introducir decisiones de diseño nuevas no aprobadas en C2 (si falta una decisión, se eleva al DC, no se inventa).
- Escribir criterios no verificables ("debe sentirse fluido" → mal; "la respuesta visible aparece en <400 ms" → bien).
- Dejar estados sin especificar: un estado ausente en la spec es un defecto de la spec, no libertad del desarrollador.

## Al recibir retorno de QA (H9: criterio `no-verificable` por ambigüedad)
Corregir creando versión nueva de la spec; la aprobada no se edita.
