# UXOS — Sistema Operativo de Diseño UX/UI

> UXOS es un sistema operativo interno para convertir observación UX/UI en decisiones de diseño, especificaciones implementables y QA verificable — manteniendo evidencia, canon, estado y compuertas humanas en archivos portables entre agentes.

**What is this?** *(EN)* — UXOS is a portable, file-based "design operating system" for a Spanish-speaking creative agency. It turns any coding/desktop AI agent (Claude Code, Claude Cowork, Codex, Google Antigravity) into a disciplined UX/UI practice: evidence-backed audits graded on Nielsen's 0–4 severity scale, design direction with an explicit emotional intent, dev-ready specs, and implementation QA — with a human creative director approving every gate. All knowledge lives in plain markdown (`nucleo/`), all project state lives in files (`ESTADO.md`, `BITACORA.md`), so any agent on any platform can pause, switch projects, and resume where another left off. The evaluation criteria are distilled from eight foundational UX books (Nielsen, Krug, Norman ×2, Yablonski, Walter, Rosenfeld, Crampton Smith) into citable principle files — every finding must cite observable evidence plus a canon principle, or it doesn't ship. Working language of all outputs: Spanish.

Uso interno del estudio. Idioma de trabajo: **español**. Es un sistema de archivos, no un mega-prompt.

## Cómo usarlo

Abre esta carpeta (`uxos/`) como espacio de trabajo en cualquiera de las plataformas soportadas — el adaptador correspondiente carga el sistema automáticamente:

| Plataforma | Adaptador | Fuerte para |
|---|---|---|
| Claude Code | `CLAUDE.md` + `.claude/skills/` | Pipeline completo basado en archivos, specs, handoff, QA técnico; navegador **si está configurado** (`agent-browser`, Playwright o MCP) |
| Claude Cowork | `CLAUDE.md` + `.claude/skills/` | Dirección interna, compuertas del DC, informes, revisión estratégica |
| Codex | `AGENTS.md` | Implementación, QA pegado al código, lectura de repo, testing |
| Google Antigravity | `GEMINI.md` + Rules del workspace | QA visual, evidencia de navegación, verificación interactiva |

Las capacidades de navegador dependen de la configuración de cada instalación, no del adaptador: si no hay navegador disponible, el sistema degrada a trabajar sobre capturas provistas y lo registra (regla de `nucleo/sistema.md`). En Antigravity, además de `GEMINI.md`, conviene crear una Rule de workspace que apunte a `nucleo/sistema.md`.

Flujo típico: `uxos-iniciar` → `uxos-auditar` → (C1) → `uxos-dirigir` → (C2) → `uxos-especificar` → (C3) → `uxos-qa` → (C4). En cualquier momento: `uxos-informe` para generar informes y `uxos-estado` para consultar o registrar compuertas. En plataformas sin skills, basta pedir la etapa por nombre: el adaptador enruta a `nucleo/etapas/`.

## Estructura

```
nucleo/                  ← fuente única de verdad (constitución, roles, etapas, plantillas, canon)
nucleo/contratos.md      ← contrato exacto de cada comando (entrada, archivos, salida, compuerta)
nucleo/memoria-patrones/ ← learning loop: patrones propios del estudio, un archivo por aprendizaje
biblioteca/              ← los 8 libros PDF de referencia (fuente del canon; NO se versiona, ver .gitignore)
proyectos/               ← un directorio por proyecto + PORTAFOLIO.md como índice (NO se versiona: confidencial)
CLAUDE.md / AGENTS.md / GEMINI.md  ← adaptadores finos por plataforma
```

## Multi-proyecto no lineal

Varios clientes conviven en `proyectos/` y se trabaja de forma no lineal: pausar uno, atender otro, volver. `proyectos/PORTAFOLIO.md` es el índice vivo (estado, etapa y siguiente paso de cada proyecto); al pausar se escribe una nota de `## Reanudación` en el `ESTADO.md` del proyecto, y al continuar se retoma desde ella — en cualquier plataforma, sin re-explicar nada. Un proyecto jamás lee ni escribe en la carpeta de otro; lo único compartido es el núcleo y la memoria de patrones.

**Orden de adopción recomendado** (no intentes usarlo todo el primer día): (1) `uxos-iniciar` + `uxos-auditar` + `uxos-estado` en un proyecto real hasta C1; (2) `uxos-qa` si hay build; (3) `uxos-dirigir` y `uxos-especificar`; (4) `uxos-informe` para cliente; (5) memoria de patrones al cerrar los primeros proyectos.

## Reglas que definen el sistema

1. **Evidencia o nada:** todo hallazgo lleva evidencia observable + cita del canon + severidad Nielsen 0–4. La opinión es legítima pero se etiqueta "juicio de estudio".
2. **Compuertas humanas:** el director creativo aprueba encuadre, hallazgos, dirección, spec y release. Sin auto-aprobación, sin timeouts.
3. **Estado en archivos:** `ESTADO.md` y `BITACORA.md` por proyecto. Cualquier plataforma retoma donde otra dejó.
3b. **Investigaciones paralelas:** cada frente de investigación tiene carpeta propia nombrada por lo que investiga (`10-evidencia/<slug>/`, `20-hallazgos/<slug>/`), hallazgos namespaced (`H-<slug>-<nn>`) y su fila en `ESTADO.md` — varias pueden correr a la vez, incluso desde plataformas distintas, sin colisionar.
4. **Canon citable con límites:** los 8 libros destilados en `nucleo/canon/` con claves `[archivo:concepto]` — Nielsen, Krug, Yablonski, Norman (×2), Walter, Rosenfeld, Crampton Smith. Cada archivo incluye su "Cuándo NO aplica": un principio usado fuera de su dominio es un hallazgo falso.
5. **Síntesis antes que volumen:** la salida principal de una auditoría son 3–5 causas raíz; los hallazgos individuales son evidencia debajo. Más de 12 ⇒ agrupación obligatoria.
6. **Contratos por comando:** `nucleo/contratos.md` define entrada mínima, archivos y salida obligatoria de cada comando — igual en las 4 plataformas.

La arquitectura completa está documentada en `../ARQUITECTURA-UXOS.md`.

## Publicación en GitHub

El repo publica **el sistema**, no el material sensible. El `.gitignore` ya excluye:
- `biblioteca/` — los PDF son libros con copyright: no se suben a ningún repo. El canon destilado en `nucleo/canon/` es autosuficiente para operar; quien clone el repo consigue los libros por su cuenta.
- `proyectos/` (salvo su README) — trabajo de clientes y `PORTAFOLIO.md` son confidenciales. Cada instalación genera los suyos.

Con eso, publicar es: `git init` (si esta carpeta no es ya un repo), commit, y `gh repo create` — el clon queda operativo de inmediato: los adaptadores, el núcleo y las skills viajan completos.
