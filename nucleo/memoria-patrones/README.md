# Memoria de patrones del estudio

Aquí se acumula lo que **el canon no puede dar: la experiencia propia del estudio.** Un archivo por patrón, creado con `nucleo/plantillas/patron.md`.

## Cuándo se escribe
- Al cerrar un proyecto (tras C4), el orquestador propone registrar 1–3 patrones: qué se recomendó, qué pasó, qué aprendimos.
- Cuando el QA o el cliente aporta evidencia posterior sobre una recomendación pasada (mejoró/empeoró), se actualiza el patrón correspondiente.

## Cuándo se lee
- En Etapa 1: el auditor revisa patrones del mismo tipo de producto/flujo antes de auditar.
- En Etapa 2: el director-diseño cita patrones propios junto al canon — `[patron:<slug>]` vale como fundamento complementario (no sustituye la cita del canon en hallazgos, pero sí refuerza recomendaciones).

## Reglas
- Un patrón sin campo "Resultado" honesto no se registra; "no-medido" es válido, inventar no.
- Si un patrón contradice el canon, se registra igual y se marca: la evidencia propia del estudio, acumulada, puede pesar más que el libro.
- Los patrones se nombran por el problema, no por el proyecto: `checkout-error-inline-vs-toast.md`, no `cliente-x-2026.md`.
