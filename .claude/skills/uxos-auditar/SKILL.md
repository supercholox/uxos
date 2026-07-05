---
name: uxos-auditar
description: Ejecuta la Etapa 1 de UXOS — investigación UX con evidencia en tres modalidades - auditoría heurística propia (Krug, Nielsen con severidad 0-4, Rosenfeld), benchmark de competencia (patrones dominantes, comparativa entre competidores), e investigación con usuarios (plan, guion y análisis de tests) - hasta la compuerta C1. Usar para auditar un sitio o app, analizar competidores, o preparar tests de usabilidad.
---

Requiere C0 aprobada (verifica `ESTADO.md`).

Pregunta (o deduce) **qué se investiga y de qué tipo**: auditoría propia (`checkout-movil`), benchmark de competencia (`benchmark-checkout`, plantilla `benchmark.md`, sin severidad para competidores) o investigación con usuarios (`test-navegacion`, plantilla `test-usuarios.md`). Alta en la tabla Investigaciones de `ESTADO.md`, carpetas `10-evidencia/<slug>/` y `20-hallazgos/<slug>/`, hallazgos `H-<slug>-<nn>`. Varias investigaciones pueden correr en paralelo; esta sesión no toca las carpetas ni filas de las demás. Contrato completo en `nucleo/contratos.md`.

Adopta los roles `nucleo/roles/auditor-ux.md` y `nucleo/roles/arquitecto-informacion.md` (alternándolos por flujo) y sigue `nucleo/etapas/etapa-1-investigacion.md` paso a paso. Los criterios citables están en `nucleo/canon/` — cada hallazgo cumple las 6 reglas de evidencia de `nucleo/sistema.md` sin excepción.

Usa `agent-browser` para navegar y capturar evidencia a `10-evidencia/` (antes de usarlo por primera vez en la sesión: `agent-browser skills get core --full`). Redacta hallazgos incrementalmente con `nucleo/plantillas/hallazgo.md`, consolida con `nucleo/plantillas/informe-hallazgos.md` y solicita C1 al DC. Todo en español.
