# Canon: WCAG — Accesibilidad
Fuente: WCAG 2.2 (W3C, estándar público — único archivo del canon que no proviene de un libro de la biblioteca).
Cómo citar: `[wcag:<criterio>]`

Cubre el barrido de accesibilidad de las Etapas 1 y 4. No es una auditoría WCAG formal de certificación: es el checklist operativo que evita publicar barreras evidentes. La severidad usa la escala Nielsen 0–4; una barrera que impide completar la tarea a un grupo de usuarios es grado 4, sin discusión.

## Perceptible

- `[wcag:contraste]` — Contraste de texto ≥ 4.5:1 (cuerpo) y ≥ 3:1 (texto grande y componentes de interfaz). Medible con inspección de valores computados: no se estima a ojo.
- `[wcag:alt]` — Toda imagen informativa tiene alternativa de texto; las decorativas la tienen vacía. Iconos-botón sin etiqueta accesible = hallazgo.
- `[wcag:no-solo-color]` — El color nunca es el único portador de información (estados de error, enlaces, gráficos).
- `[wcag:reflow]` — El contenido funciona a 320px de ancho y con zoom 200% sin scroll horizontal ni pérdida de contenido.

## Operable

- `[wcag:teclado]` — Todo lo operable con ratón es operable con teclado, sin trampas de foco. Prueba: recorrer el flujo crítico solo con Tab/Enter/Esc.
- `[wcag:foco-visible]` — El indicador de foco es visible siempre; suprimirlo con `outline: none` sin reemplazo es hallazgo automático.
- `[wcag:objetivo-tactil]` — Objetivos táctiles ≥ 24×24 px CSS mínimo WCAG; UXOS especifica 44×44 como criterio de spec (cruza con `[yablonski:fitts]`).
- `[wcag:sin-limite-abusivo]` — Sin límites de tiempo no ajustables ni contenido que parpadea >3 veces/segundo.

## Comprensible

- `[wcag:etiquetas]` — Todo campo de formulario tiene etiqueta visible y programática; el placeholder no es etiqueta.
- `[wcag:errores-descriptivos]` — Los errores de formulario identifican el campo y dicen cómo corregir (cruza con `[nielsen:recuperacion-errores]`).
- `[wcag:idioma]` — El idioma de la página está declarado (`lang="es"`); crítico para lectores de pantalla en un mercado hispanohablante.

## Robusto

- `[wcag:semantica]` — Encabezados jerárquicos reales (h1→h2→h3), listas como listas, botones como `<button>`, enlaces como `<a>`. El div-clicable es el hallazgo de robustez más común.
- `[wcag:nombre-rol-valor]` — Componentes custom exponen nombre, rol y estado (ARIA solo cuando el HTML nativo no alcanza; ARIA incorrecto es peor que ninguno).

## Cuándo NO aplica (anti-martillo)

- No convertir el informe en una auditoría WCAG de 200 puntos: en Etapa 1 esto es un barrido de barreras evidentes en los flujos críticos; la certificación formal es un encargo aparte.
- `[wcag:objetivo-tactil]` en interfaces densas de escritorio profesional admite el mínimo de 24px; los 44px son el criterio para móvil y público general.
- No citar ARIA como solución por defecto: la primera recomendación siempre es HTML semántico nativo.
