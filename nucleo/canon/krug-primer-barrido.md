# Canon: Krug — No me hagas pensar
Fuente: *No me hagas pensar* (Don't Make Me Think), Steve Krug. PDF en `biblioteca/`.
Cómo citar: `[krug:<concepto>]`

Es el **checklist de primer barrido** de toda auditoría: rápido, brutal, desde los ojos de un usuario que escanea, no lee.

## Principios

- `[krug:autoevidencia]` — Primera ley: la página debe ser autoevidente. Si un usuario razonable tiene que pensar "¿esto es clicable?, ¿dónde estoy?, ¿por dónde empiezo?", hay un hallazgo.
- `[krug:escaneo]` — La gente no lee, escanea. Diseñar para el vistazo: jerarquía visual clara, convenciones, zonas delimitadas, lo clicable obvio, ruido mínimo.
- `[krug:jerarquia-visual]` — Lo más importante es más prominente; lo relacionado está agrupado visualmente; la anidación visual refleja la lógica.
- `[krug:convenciones]` — Las convenciones existen porque funcionan. Innovar solo si lo nuevo es tan claro que no cuesta aprenderlo.
- `[krug:omitir-palabras]` — Elimina la mitad de las palabras; luego la mitad de lo que queda. Happy talk e instrucciones largas mueren primero.
- `[krug:clics-sin-pensar]` — No importa cuántos clics, sino que cada clic sea una elección obvia y sin ambigüedad.

## Navegación — `[krug:navegacion]`

Toda página debe responder sin esfuerzo: **¿Qué sitio es este? ¿En qué página estoy? ¿Cuáles son las secciones principales? ¿Qué opciones tengo aquí? ¿Dónde estoy en el esquema general? ¿Cómo busco?**
- `[krug:prueba-del-tronco]` — Prueba del tronco: aterrizando en cualquier página interna al azar, esas preguntas deben responderse al instante (ID del sitio, secciones, navegación local, indicador de "estás aquí", búsqueda).
- `[krug:pagina-inicio]` — La portada debe comunicar el panorama general: qué es esto, qué puedo hacer aquí, por qué debería estar aquí y no en otro sitio.

## Cuándo NO aplica (anti-martillo)

- `[krug:omitir-palabras]` no aplica al contenido que el usuario vino a leer: artículos, documentación, condiciones legales, fichas de producto detalladas. Se poda la interfaz, no el contenido buscado.
- `[krug:autoevidencia]` se calibra por audiencia: en herramientas profesionales de uso diario, cierta curva de aprendizaje es aceptable si compra eficiencia (`[nielsen:flexibilidad-eficiencia]`).
- `[krug:convenciones]` no prohíbe innovar: prohíbe innovar *confuso*. Una solución nueva más clara que la convención es válida — pero se prueba, no se asume.
- `[krug:escaneo]` no convierte toda página en titulares: páginas de decisión compleja (comparativas, checkout) necesitan densidad informativa bien jerarquizada, no menos información.

## Método

- `[krug:test-pasillo]` — Pruebas de usabilidad baratas y frecuentes (3 usuarios, una mañana al mes) superan a la prueba perfecta que nunca se hace. Probar temprano, arreglar lo peor primero.
- `[krug:reserva-buena-voluntad]` — Cada fricción vacía la reserva de buena voluntad del usuario; cada gesto de ayuda la llena. Los hallazgos que "queman" buena voluntad (ocultar información, castigar el error) suben de severidad.
