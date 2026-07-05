# Etapa 1 — Investigación UX
Roles: auditor-ux, arquitecto-informacion (pueden alternarse por flujo). Salida: `20-hallazgos/informe.md` → Compuerta C1.

## Procedimiento

1. **Plan de barrido → investigaciones** (orquestador): dividir el alcance aprobado en **investigaciones con nombre propio** (slug de lo investigado: `checkout-movil`, `onboarding`, `arquitectura-navegacion`). Dar de alta cada una en la tabla `## Investigaciones` de `ESTADO.md` y crear sus carpetas: `10-evidencia/<slug>/` y `20-hallazgos/<slug>/`. Pueden correr en paralelo — incluso en plataformas distintas — porque cada una escribe solo dentro de sus carpetas.
2. **Captura de evidencia** (auditor-ux, por investigación): recorrer cada flujo con el navegador de la plataforma; capturar a `10-evidencia/<slug>/` con nombre por flujo y paso (`checkout-paso2.png`). La evidencia se captura ANTES de redactar hallazgos.
3. **Primer barrido Krug** por página: autoevidencia, escaneo, prueba del tronco (`[krug:prueba-del-tronco]`). Hallazgos rápidos, plantilla `hallazgo.md`.
4. **Evaluación heurística Nielsen** por flujo: las 10 heurísticas + severidad 0–4. Diagnóstico causal con Norman objetos (¿significante? ¿feedback? ¿modelo conceptual?) y justificación con Yablonski.
5. **Auditoría de IA** (arquitecto-informacion, en paralelo si hay capacidad): los 4 sistemas de Rosenfeld + prueba ascendente (aterrizar en páginas internas).
6. **Pasada emocional:** nivel afectado por hallazgo (visceral/conductual/reflexivo); en flujos de estrés, severidad +1 (`[norman-emocional:positivo-amplia]`).
6b. **Cierre de investigación:** al terminar un frente, marcar su fila como `completa` en `ESTADO.md` y anotarlo en `BITACORA.md`. Los hallazgos van namespaced (`H-<slug>-<nn>`) en `20-hallazgos/<slug>/`.
7. **Consolidación y síntesis** (orquestador, cuando las investigaciones planificadas están `completa` — o antes, si el DC pide C1 parcial marcando qué queda fuera): fusionar todas las investigaciones, deduplicar, priorizar por severidad × frecuencia y **sintetizar en 3–5 causas raíz** — la salida principal del informe; los hallazgos individuales quedan debajo como evidencia, con su triaje (mantener/mejorar/reemplazar/eliminar/testear/decisión-cliente). Más de 12 hallazgos ⇒ agrupación obligatoria. Separar "juicios de estudio" en su sección. Respetar el "Qué NO se debe cambiar" del brief: si la evidencia sugiere tocarlo, se redacta como tensión para el DC. Redactar `informe.md` con la plantilla.
8. **Validación de esquema:** ningún hallazgo sin evidencia + cita + severidad entra al informe (regla 6).
9. **Solicitar C1** al DC: resumen corto + los 3–5 puntos que requieren su criterio + opciones.

## Reglas de la etapa
- Prohibido proponer soluciones (máximo "pista de solución" de una línea).
- Cada hallazgo se escribe al encontrarse, no al final (resiliencia ante interrupciones).
- Sin acceso a un flujo: `no-verificable`, pedir capturas, seguir con el resto.
- Una sesión trabaja UNA investigación por vez y no toca las carpetas ni las filas de ESTADO.md de las demás.
