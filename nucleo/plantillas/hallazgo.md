---
proyecto: <cliente>-<proyecto>
etapa: 1-investigacion
artefacto: hallazgo
estado: borrador
autor-rol: auditor-ux | arquitecto-informacion | qa-implementacion
fecha: <aaaa-mm-dd>
depende-de: [00-brief/brief.md]
id: H-<slug-investigacion>-<nn>
investigacion: <slug — debe existir en la tabla Investigaciones de ESTADO.md>
flujo: <checkout | onboarding | ...>
severidad: 0 | 1 | 2 | 3 | 4
canon: [nielsen:..., krug:...]
nivel-emocional: visceral | conductual | reflexivo
triaje: mantener | mejorar | reemplazar | eliminar | testear | decision-cliente
causa-raiz: <CR-n a la que pertenece, se asigna en consolidación>
---

# H-<slug>-<nn> — <título corto del problema>

## Qué se observó
<!-- Hecho, sin interpretación: "En el paso 2 del checkout, al enviar el formulario con un campo vacío, la página recarga sin mensaje alguno." -->

## Evidencia
<!-- Obligatoria (regla 1): ruta de captura en 10-evidencia/, URL y pasos reproducibles. -->
- Captura: `10-evidencia/<slug-investigacion>/<flujo>-<paso>.png`
- URL: 
- Pasos: 1) … 2) … 3) …

## Por qué es un problema
<!-- Obligatorio (regla 2): claves del canon + diagnóstico causal. -->
<!-- Ej.: [nielsen:visibilidad-estado] no hay feedback del envío; causa raíz [norman-objetos:golfo-evaluacion]; lo agrava [yablonski:pico-final] por ocurrir al final del flujo. -->

## Severidad y justificación
<!-- Obligatoria (regla 3): grado 0–4 por frecuencia × impacto × persistencia. Flujo de estrés ⇒ considerar +1 [norman-emocional:positivo-amplia]. -->

## Pista de solución (opcional, máx. 1 línea)
<!-- NO es una recomendación; solo orientación para Etapa 2. -->
