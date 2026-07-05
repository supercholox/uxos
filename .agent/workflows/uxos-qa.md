---
description: QA de implementación (Etapa 4) — verificar el build contra la spec aprobada, hasta la firma C4
---

Puedes EJECUTAR y navegar el build del cliente — nunca modificar su código. Los defectos se REPORTAN, no se arreglan. Requiere C3 aprobada + build accesible.

1. Adopta `nucleo/roles/qa-implementacion.md` y sigue `nucleo/etapas/etapa-4-qa.md`.
2. Verifica cada criterio de aceptación de la spec con veredicto `cumple / no-cumple / no-verificable` y CAPTURA POR ÍTEM en `10-evidencia/` (usa el navegador de Antigravity; inspecciona valores computados para contraste, tamaños y tiempos).
3. Criterio ambiguo ⇒ `no-verificable` + retorno al especificador. No interpretes.
4. Regresión heurística (Krug + Nielsen) + barrido de accesibilidad (`wcag-accesibilidad.md`: teclado, foco, contraste) + verificación emocional de estados de error/vacío contra la persona de diseño.
5. Produce `50-qa/informe-qa.md` con veredicto global recomendado. La firma C4 es del director creativo, no tuya: solicítala y DETENTE.

Contrato exacto: `nucleo/contratos.md` → uxos-qa. Todo en español.
