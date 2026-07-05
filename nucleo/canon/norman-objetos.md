# Canon: Norman — La psicología de los objetos cotidianos
Fuente: *La psicología de los objetos cotidianos* (The Design of Everyday Things), Donald Norman. PDF en `biblioteca/`.
Cómo citar: `[norman-objetos:<concepto>]`

Es el **vocabulario causal** de UXOS: explica *por qué* algo falla, no solo que falla. Úsalo para diagnosticar la raíz de un hallazgo.

## Conceptos de diagnóstico

- `[norman-objetos:affordance]` — Affordance: lo que el objeto permite hacer en relación con quien lo usa. Un problema de affordance = la acción posible no existe o no es la esperada.
- `[norman-objetos:significante]` — Significante: la señal perceptible de qué se puede hacer y dónde. La mayoría de los "no sé que era clicable" son fallas de significante, no de affordance.
- `[norman-objetos:mapeo]` — Mapeo: relación entre control y efecto. Mapeo natural = la disposición del control refleja el resultado (controles de hornilla, flechas de orden).
- `[norman-objetos:feedback]` — Retroalimentación: toda acción necesita respuesta inmediata e informativa. Sin feedback, el usuario repite, duda o abandona.
- `[norman-objetos:modelo-conceptual]` — Modelo conceptual: la historia que el usuario se cuenta de cómo funciona el sistema. Si la imagen del sistema (lo visible) no comunica el modelo del diseñador, el usuario inventa uno equivocado.
- `[norman-objetos:restricciones]` — Restricciones (físicas, lógicas, semánticas, culturales) que guían la acción correcta antes de que ocurra el error.

## Los dos golfos

- `[norman-objetos:golfo-ejecucion]` — Golfo de ejecución: "sé lo que quiero, no sé cómo hacerlo aquí". Diagnóstico: faltan significantes, el mapeo es oscuro, las opciones no se descubren.
- `[norman-objetos:golfo-evaluacion]` — Golfo de evaluación: "hice algo, no sé si funcionó ni en qué estado quedé". Diagnóstico: feedback ausente, tardío o ilegible.
- `[norman-objetos:7-etapas]` — Las 7 etapas de la acción (meta → plan → especificar → ejecutar → percibir → interpretar → comparar) como guía de recorrido: ¿en qué etapa se rompe el flujo?

## Errores humanos

- `[norman-objetos:deslices]` — Deslices (slips): la intención era correcta, la ejecución falló (tocar el botón vecino, autocompletar traicionero). Se combaten con diseño: tamaño, separación, confirmación, deshacer.
- `[norman-objetos:equivocaciones]` — Equivocaciones (mistakes): el plan mismo era erróneo por un mal modelo conceptual. Se combaten con claridad del modelo, no con más confirmaciones.
- `[norman-objetos:culpar-usuario]` — Regla de oro: si "el usuario se equivoca" sistemáticamente, el error es del diseño. Prohibido cerrar un hallazgo con "error de usuario".

## Cuándo NO aplica (anti-martillo)

- `[norman-objetos:significante]` en exceso es ruido: señalizar todo equivale a no señalizar nada. El hallazgo correcto ante 12 significantes compitiendo es jerarquía, no "añadir otro".
- `[norman-objetos:restricciones]` excesivas frustran al experto: forzar un único camino válido en una herramienta flexible es un hallazgo en sí mismo (`[nielsen:control-libertad]`).
- `[norman-objetos:culpar-usuario]` aplica a patrones sistemáticos, no a todo tropiezo individual: un desliz aislado y recuperable con deshacer no es hallazgo de severidad.
- `[norman-objetos:modelo-conceptual]` no exige exponer el funcionamiento interno real: exige una historia útil y consistente. Simplificar el modelo mostrado es diseño legítimo mientras no traicione las expectativas que crea.
