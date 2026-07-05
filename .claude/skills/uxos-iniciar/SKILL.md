---
name: uxos-iniciar
description: Inicia un proyecto UXOS nuevo — crea la estructura de carpetas, normaliza el brief con el DC y solicita la compuerta C0. Usar cuando llega un encargo nuevo de auditoría, rediseño, producto o QA.
---

Adopta el rol `nucleo/roles/orquestador.md` y sigue `nucleo/etapas/etapa-0-encuadre.md`.

Crea `proyectos/<cliente>/<aaaa-mm>-<proyecto>/` con las carpetas estándar (00-brief, 10-evidencia, 20-hallazgos, 30-direccion, 40-especificacion, 50-qa, 60-informes) e instancia `ESTADO.md`, `BITACORA.md` y `brief.md` desde `nucleo/plantillas/`. Da de alta el proyecto en `proyectos/PORTAFOLIO.md` (créalo desde la plantilla si no existe) — varios clientes conviven en el árbol y se pausan/reanudan de forma no lineal. Normaliza el brief con el usuario, inventaría accesos, propone profundidad (exprés/completa) y solicita C0. Todo en español.
