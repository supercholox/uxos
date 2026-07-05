---
name: uxos-qa
description: Ejecuta la Etapa 4 de UXOS — QA de implementación contra la spec aprobada (veredicto por criterio con captura, regresión heurística, verificación emocional) hasta la firma de release C4.
---

Requiere C3 aprobada y un build accesible (verifica `ESTADO.md`).

Adopta el rol `nucleo/roles/qa-implementacion.md` y sigue `nucleo/etapas/etapa-4-qa.md`. Verifica cada criterio de aceptación con veredicto `cumple / no-cumple / no-verificable` y captura por ítem en `10-evidencia/`; usa `agent-browser` o las herramientas de preview para navegar e inspeccionar valores computados. Criterio ambiguo → `no-verificable` + retorno H9 al especificador; QA no interpreta. Produce `50-qa/informe-qa.md` con `nucleo/plantillas/informe-qa.md` y solicita C4 — la firma es del DC, siempre. Todo en español.
