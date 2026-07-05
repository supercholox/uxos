# Canon: Nielsen — Usability Engineering
Fuente: *Usability Engineering*, Jakob Nielsen (1993). PDF en `biblioteca/`.
Cómo citar: `[nielsen:<concepto>]`

## Escala de severidad (ESTÁNDAR OBLIGATORIO DE UXOS) — `[nielsen:severidad]`

| Grado | Nombre | Definición operativa |
|---|---|---|
| 0 | No es problema | Desacuerdo estético o de gusto; no afecta la tarea |
| 1 | Cosmético | Se corrige solo si sobra tiempo |
| 2 | Menor | Entorpece; prioridad baja |
| 3 | Mayor | Dificulta seriamente la tarea; prioridad alta |
| 4 | Catástrofe | Impide completar la tarea o causa pérdida (datos, dinero, confianza); bloquea release |

Justificación obligatoria por tres factores: **frecuencia** (¿cuántos usuarios lo encuentran?), **impacto** (¿qué tan difícil es superarlo?), **persistencia** (¿molesta una vez o siempre?).

## Las 10 heurísticas — claves de cita

1. `[nielsen:visibilidad-estado]` — El sistema informa siempre qué está pasando, con feedback oportuno.
2. `[nielsen:sistema-mundo-real]` — Habla el lenguaje del usuario; orden natural, no jerga interna.
3. `[nielsen:control-libertad]` — Salidas de emergencia: deshacer, rehacer, cancelar, volver.
4. `[nielsen:consistencia-estandares]` — Misma cosa = mismo nombre y comportamiento; seguir convenciones de plataforma.
5. `[nielsen:prevencion-errores]` — Mejor prevenir que curar: confirmaciones, restricciones, valores por defecto seguros.
6. `[nielsen:reconocer-vs-recordar]` — Opciones visibles; no obligar a memorizar entre pantallas.
7. `[nielsen:flexibilidad-eficiencia]` — Aceleradores para expertos sin castigar novatos.
8. `[nielsen:diseno-minimalista]` — Cada unidad extra de información compite con las relevantes.
9. `[nielsen:recuperacion-errores]` — Mensajes de error en lenguaje llano, con diagnóstico y solución.
10. `[nielsen:ayuda-documentacion]` — Si hace falta ayuda, que sea buscable, concreta y corta.

## Cuándo NO aplica (anti-martillo)

- `[nielsen:visibilidad-estado]` no aplica si la acción es instantánea y percibida: feedback añadido a lo obvio es ruido (choca con `[nielsen:diseno-minimalista]`).
- `[nielsen:prevencion-errores]` no justifica confirmaciones en cadena: la fatiga de confirmación entrena al usuario a aceptar sin leer — y anula la prevención.
- `[nielsen:diseno-minimalista]` no justifica esconder información que la tarea necesita: minimalismo es quitar lo irrelevante, no lo incómodo.
- `[nielsen:consistencia-estandares]` cede cuando la convención dominante es objetivamente dañina para esta audiencia; romperla es decisión de dirección (Etapa 2, con trade-off), no hallazgo automático.
- La severidad no se infla para "vender" el hallazgo: un grado 4 sin evidencia de bloqueo real destruye la credibilidad de todo el informe.

## Métodos que UXOS adopta

- `[nielsen:evaluacion-heuristica]` — Evaluación heurística: revisión sistemática contra las heurísticas, por evaluador, pantalla por pantalla y flujo por flujo. Es el método base de la Etapa 1.
- `[nielsen:test-5-usuarios]` — Pocos usuarios bastan: ~5 usuarios revelan la mayoría de los problemas; iterar vale más que muestras grandes.
- `[nielsen:ciclo-iterativo]` — Diseño iterativo: evaluar temprano y barato antes de construir caro.
