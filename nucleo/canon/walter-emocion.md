# Canon: Walter — Designing for Emotion
Fuente: *Designing for Emotion*, Aarron Walter (A Book Apart). PDF en `biblioteca/`.
Cómo citar: `[walter:<concepto>]`

Es el **motor de la Etapa 2**: convierte "queremos que se sienta humano" en artefactos concretos.

## Conceptos

- `[walter:piramide]` — Pirámide de necesidades del diseño: funcional → confiable → usable → **placentero**. No se construye deleite sobre una base rota; pero quedarse en "usable" es dejar la relación con el usuario sobre la mesa.
- `[walter:persona-de-diseno]` — Persona de diseño: la personalidad del producto documentada — nombre/arquetipo, rasgos (y qué NO es), voz y tono por contexto, ejemplos de copy, mapa visual (color, tipografía) alineado a la personalidad. Es el artefacto central de la dirección emocional; sin ella, cada pantalla habla con una voz distinta.
- `[walter:tono-por-contexto]` — La voz es constante; el tono cambia con el contexto emocional del usuario. Un error de pago no admite chistes; un logro sí admite celebración. Mapear: contexto → estado emocional del usuario → tono.
- `[walter:sorpresa-deleite]` — Sorpresa y deleite: recompensas variables, detalles inesperados, microcopy con personalidad. Dosificados: el deleite es condimento, no plato.
- `[walter:anticipacion]` — Anticipación: sembrar expectativa (onboarding progresivo, revelaciones) mantiene el interés.
- `[walter:compromiso-emocional]` — El diseño emocional construye relación: los usuarios perdonan errores a productos con los que tienen vínculo — si el producto se ha ganado esa confianza.

## Estados críticos (checklist de auditoría y spec)

- `[walter:estados-error]` — Errores con humanidad: qué pasó, qué hago ahora, sin culpar, con la voz de la persona de diseño.
- `[walter:estados-vacios]` — Estados vacíos como oportunidad: primera vez, sin resultados, sin datos — enseñan, orientan o deleitan; nunca un callejón en blanco.
- `[walter:tiempo-inactividad]` — Caídas y mantenimiento: honestidad + personalidad recuperan buena voluntad (cruza con `[krug:reserva-buena-voluntad]`).

## Cuándo NO aplica (anti-martillo)

- `[walter:sorpresa-deleite]` está prohibido en contextos de estrés o pérdida: errores de pago, datos borrados, fallos de seguridad. Ahí el tono es sobrio, claro y resolutivo (`[walter:tono-por-contexto]` manda sobre el deleite).
- `[walter:piramide]` es secuencial: no se recomienda deleite sobre una base funcional/confiable/usable rota. Primero los cimientos.
- Personalidad no es verborrea: si el microcopy con voz alarga la tarea o estorba al usuario recurrente, choca con `[krug:omitir-palabras]` — trade-off a compuerta.
- El humor viaja mal entre culturas y audiencias B2B: la persona de diseño define cuánta personalidad tolera ESTA audiencia; no se importa el tono de un producto de consumo a una herramienta corporativa.

## Regla de uso en UXOS
En Etapa 2, la persona de diseño es **obligatoria** como sección de `direccion.md`. En Etapas 3–4, los estados de error/vacío/espera se especifican y verifican contra esa persona.
