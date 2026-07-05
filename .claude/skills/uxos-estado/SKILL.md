---
name: uxos-estado
description: Estado y control de proyectos UXOS — vista de portafolio de todos los clientes, estado de un proyecto (etapa, compuertas, investigaciones, siguiente paso), registro de decisiones de compuerta del DC, y pausar/continuar proyectos para trabajo multi-cliente no lineal.
---

Adopta el rol `nucleo/roles/orquestador.md`. Contrato completo en `nucleo/contratos.md`.

**Portafolio:** sin proyecto especificado, lee `proyectos/PORTAFOLIO.md` y muestra todos los proyectos con estado, etapa y siguiente paso — la vista para decidir a qué volver.

**Pausar:** escribe la sección `## Reanudación` en el `ESTADO.md` del proyecto (siguiente paso concreto, qué quedó a medias, qué se necesita), márcalo `pausado` en `PORTAFOLIO.md` y anota en BITACORA. **Continuar:** lee `## Reanudación` + últimas líneas de BITACORA, confirma el siguiente paso en una línea y retoma — sin re-derivar nada desde el chat.

**Consulta:** lee `ESTADO.md` y las últimas ~20 líneas de `BITACORA.md` del proyecto (si hay varios en `proyectos/`, pregunta cuál) y resume en ≤10 líneas: etapa actual, compuertas y su estado, investigaciones en curso (slug + estado de cada una), bloqueos activos, y el siguiente paso concreto.

**Registro de compuerta:** si el DC comunica una decisión, regístrala textualmente en `ESTADO.md` con fecha y motivo, anota el evento en `BITACORA.md` y confirma qué etapa se desbloquea (o se reabre, conservando los artefactos `rechazado`). Nunca registres una aprobación que el DC no haya dado explícitamente. Todo en español.
