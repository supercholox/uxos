---
description: Investigación UX (Etapa 1) — auditoría heurística, benchmark de competencia o test con usuarios, hasta C1
---

NO propongas rediseños ni escribas código: esta etapa OBSERVA y documenta. Requiere C0 aprobada (verifica `ESTADO.md`).

1. Adopta `nucleo/roles/auditor-ux.md` (o `arquitecto-informacion.md` para estructura/navegación) y sigue `nucleo/etapas/etapa-1-investigacion.md`.
2. Define qué se investiga y de qué tipo: auditoría propia (`<flujo>`), benchmark (`benchmark-<tema>`, plantilla `benchmark.md`, SIN severidad para competidores) o test de usuarios (`test-<tema>`, plantilla `test-usuarios.md`). Alta en la tabla Investigaciones de `ESTADO.md`; carpetas `10-evidencia/<slug>/` y `20-hallazgos/<slug>/`.
3. Usa el navegador de Antigravity para recorrer los flujos y CAPTURA EVIDENCIA ANTES de redactar: cada captura a `10-evidencia/<slug>/` nombrada por flujo y paso.
4. Redacta hallazgos incrementalmente con `nucleo/plantillas/hallazgo.md`: evidencia + cita del canon (`nucleo/canon/`, revisando su "Cuándo NO aplica") + severidad 0–4. IDs: `H-<slug>-<nn>`.
5. Incluye el barrido de accesibilidad (`wcag-accesibilidad.md`): teclado, foco, contraste, etiquetas.
6. Consolida: 3–5 CAUSAS RAÍZ como salida principal (plantilla `informe-hallazgos.md`); >12 hallazgos ⇒ agrupar.
7. Solicita C1 al director creativo y DETENTE.

Contrato exacto: `nucleo/contratos.md` → uxos-auditar. Todo en español.
