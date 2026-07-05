# Contratos de comando
Contrato exacto de cada comando UXOS. **Vinculante en todas las plataformas**: un comando que no cumple su salida obligatoria no está terminado. Los nombres de skill son de Claude Code/Cowork; en Codex y Antigravity se invoca pidiendo la etapa por nombre — el contrato es el mismo.

---

## uxos-iniciar
- **Entrada mínima:** cliente, nombre del proyecto, tipo de encargo, y el brief crudo (o una conversación con el DC para levantarlo).
- **Lee:** `nucleo/sistema.md`, `nucleo/etapas/etapa-0-encuadre.md`, `nucleo/plantillas/`.
- **Crea/modifica:** `proyectos/<cliente>/<aaaa-mm>-<proyecto>/` completo; `ESTADO.md`, `BITACORA.md`, `00-brief/brief.md`; alta del proyecto en `proyectos/PORTAFOLIO.md` (créalo desde la plantilla si no existe).
- **Salida obligatoria:** brief normalizado con TODOS los campos de la plantilla (incluidos "acción principal del usuario", "qué NO se debe cambiar" y "nivel de intervención"), inventario de accesos con estado, y solicitud de C0.
- **Compuerta requerida:** ninguna previa; produce C0.
- **Errores comunes:** aceptar alcance sin "Fuera:"; iniciar sin preguntar qué no se debe tocar; crear el proyecto sin registrar el evento en BITACORA.

## uxos-auditar
- **Entrada mínima:** C0 aprobada; **qué se investiga** (slug de la investigación — si no existe, se da de alta en `ESTADO.md` y se crean sus carpetas); acceso al producto (URL/credenciales) o capturas provistas.
- **Lee:** `ESTADO.md` (tabla Investigaciones incluida), `00-brief/brief.md`, `nucleo/canon/*`, `nucleo/roles/auditor-ux.md`, `nucleo/roles/arquitecto-informacion.md`, `nucleo/etapas/etapa-1-investigacion.md`.
- **Crea/modifica:** `10-evidencia/<slug>/*` (capturas), `20-hallazgos/<slug>/H-<slug>-*.md`, su fila en la tabla Investigaciones de `ESTADO.md`, `BITACORA.md`; el consolidado `20-hallazgos/informe.md` solo en la consolidación final. **Aislamiento:** jamás escribe en carpetas o filas de otra investigación — es lo que permite correr varias en paralelo.
- **Salida obligatoria:** **3–5 causas raíz sintetizadas** como conclusión principal; hallazgos individuales debajo como evidencia (agrupados obligatoriamente si superan 12); cada hallazgo con evidencia observable + cita del canon + severidad 0–4 + triaje (mantener/mejorar/reemplazar/eliminar/testear/decisión-cliente); flujos `no-verificable` listados con motivo; solicitud de C1.
- **Compuerta requerida:** C0. Produce C1.
- **Errores comunes:** listar 40 hallazgos sin síntesis; proponer soluciones (es Etapa 2); redactar hallazgos al final en vez de incrementalmente; citar el canon sin revisar su "Cuándo NO aplica".

## uxos-dirigir
- **Entrada mínima:** C1 aprobada con las decisiones del DC registradas.
- **Lee:** `ESTADO.md`, `20-hallazgos/informe.md` (aprobado), `nucleo/canon/walter-emocion.md`, `norman-emocional.md`, `yablonski-leyes.md`, `crampton-lentes.md`, `nucleo/etapas/etapa-2-direccion.md`.
- **Crea/modifica:** `30-direccion/direccion.md`, `BITACORA.md`.
- **Salida obligatoria:** lente del proyecto declarada; 3–6 principios ligados a hallazgos; persona de diseño completa con mapa de tono y ejemplos de copy en ES; intención emocional por nivel con método de verificación en QA; recomendaciones priorizadas con esfuerzo y trade-offs; tensiones redactadas para C2.
- **Compuerta requerida:** C1. Produce C2.
- **Errores comunes:** principios sin hallazgo que los motive; resolver tensiones en silencio; contradecir decisiones de C1 sin marcarlo; colar especificación de componentes.

## uxos-especificar
- **Entrada mínima:** C2 aprobada.
- **Lee:** `ESTADO.md`, `30-direccion/direccion.md` (aprobada), `nucleo/etapas/etapa-3-especificacion.md`, `nucleo/plantillas/spec.md`.
- **Crea/modifica:** `40-especificacion/spec*.md`, `BITACORA.md`.
- **Salida obligatoria:** todos los estados por componente (normal/foco/carga/vacío/error/éxito); criterios dado/cuando/entonces verificables `cumple/no-cumple`; criterios no funcionales medibles; tokens; copy final en ES fiel a la persona; solicitud de C3.
- **Compuerta requerida:** C2. Produce C3.
- **Errores comunes:** criterios no verificables ("debe sentirse fluido"); estados ausentes; inventar decisiones no aprobadas en vez de elevarlas; editar una spec aprobada en lugar de crear v2.

## uxos-qa
- **Entrada mínima:** C3 aprobada + build accesible (URL, staging o local).
- **Lee:** `ESTADO.md`, `40-especificacion/spec*.md` (aprobada), `nucleo/roles/qa-implementacion.md`, `nucleo/etapas/etapa-4-qa.md`.
- **Crea/modifica:** `10-evidencia/qa-*.png`, `50-qa/informe-qa.md`, `BITACORA.md`.
- **Salida obligatoria:** veredicto por criterio (`cumple/no-cumple/no-verificable`) con captura por ítem; lista de bloqueos (no-cumple con severidad ≥3); defectos nuevos de regresión con las 6 reglas; retornos H9 si hubo criterios ambiguos; veredicto global recomendado; solicitud de C4.
- **Compuerta requerida:** C3. Produce C4 (la firma es del DC).
- **Errores comunes:** interpretar criterios ambiguos en vez de devolverlos; `cumple` sin haberlo observado; QA sobre capturas ajenas sin instrucción del DC; olvidar la regresión heurística.

## uxos-informe
- **Entrada mínima:** al menos un artefacto de proyecto (cliente ⇒ solo `aprobado`); tipo y audiencia del informe.
- **Lee:** artefactos de las etapas cubiertas, `ESTADO.md` (decisiones), `10-evidencia/`, `nucleo/roles/redactor-informes.md`, `nucleo/etapas/informes.md`.
- **Crea/modifica:** `60-informes/informe-*.md` (+ .docx/.pptx/.pdf si se pide y la plataforma puede), `BITACORA.md`.
- **Salida obligatoria:** pirámide (resumen ejecutivo ≤ media página → 3–5 puntos con evidencia → anexo → próximos pasos); en modo informe, canon traducido a lenguaje llano y severidad en lenguaje de negocio; nota explícita de que requiere revisión del DC antes de salir.
- **Compuerta requerida:** ninguna para informes internos; revisión del DC obligatoria para material de cliente.
- **Errores comunes:** reciclar el tono crudo del modo interno; incluir artefactos `borrador`/`rechazado` en material de cliente; rellenar huecos con prosa en vez de devolverlos al orquestador.

## uxos-estado
Cuatro operaciones: **portafolio**, **consulta de proyecto**, **registro de compuerta**, **pausar/continuar**.
- **Entrada mínima:** ninguna para portafolio; proyecto identificado para el resto. Para registrar compuerta: la decisión textual del DC.
- **Lee:** `proyectos/PORTAFOLIO.md`; y del proyecto: `ESTADO.md`, últimas ~20 líneas de `BITACORA.md`.
- **Crea/modifica:** en registro de compuerta: `ESTADO.md` (decisión textual, fecha, motivo), `PORTAFOLIO.md` (estado `en-compuerta`/desbloqueado) y `BITACORA.md`. En **pausar**: sección `## Reanudación` del `ESTADO.md` (siguiente paso concreto, qué quedó a medias, qué se necesita), estado `pausado` en ambos, evento en BITACORA. En **continuar**: leer `## Reanudación`, actualizarla/limpiarla, estado `activo` en ambos.
- **Salida obligatoria:** portafolio = tabla de todos los proyectos con estado, etapa y siguiente paso. Consulta = resumen ≤10 líneas (etapa, compuertas, investigaciones en curso con su estado, bloqueos, siguiente paso concreto). Pausar = confirmación con la nota de reanudación escrita. Continuar = el siguiente paso confirmado en una línea antes de trabajar.
- **Compuerta requerida:** ninguna.
- **Errores comunes:** registrar una aprobación que el DC no dio explícitamente; resumir desde el historial de chat en vez de los archivos; pausar sin escribir la nota de reanudación; asumir el proyecto activo sin confirmar.
