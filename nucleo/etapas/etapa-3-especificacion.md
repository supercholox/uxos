# Etapa 3 — Especificación y handoff
Rol: especificador. Requiere C2 aprobada. Salida: `40-especificacion/spec.md` (+ archivos por componente si el volumen lo pide) → Compuerta C3 (ligera).

## Procedimiento

1. **Inventario de piezas:** listar componentes/flujos a especificar a partir de las recomendaciones aprobadas en C2. Priorizar lo que desarrollo necesita primero.
2. **Spec por componente/flujo** con TODOS los estados: normal, hover/foco, carga, vacío, error, éxito (y sin conexión si aplica). Estados de error/vacío redactados con la persona de diseño aprobada.
3. **Criterios de aceptación** dado/cuando/entonces, uno por comportamiento, verificables mirando el build (`cumple / no-cumple`). Incluir criterios no funcionales medibles: contraste, tamaño táctil mínimo (`[yablonski:fitts]`), respuesta <400 ms o feedback de progreso (`[yablonski:doherty]`).
4. **Tokens y anotaciones:** espaciado, tipografía, color, radios, sombras — en formato que desarrollo consuma (tabla o JSON simple).
5. **Copy final en español** por estado, consistente con la persona de diseño.
6. **Auto-chequeo:** ¿cada criterio es verificable sin interpretar? ¿cada estado existe? ¿alguna decisión nueva se coló sin aprobar? (si falta una decisión → elevarla al DC, no inventarla).
7. **Solicitar C3** (ligera): ¿la spec es fiel a la dirección?

## Regla de versiones
La spec aprobada es inmutable. Correcciones (incluidos retornos H9 desde QA) crean `spec-v2.md` con changelog al inicio.
