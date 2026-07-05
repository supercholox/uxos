# Canon: Rosenfeld — Information Architecture (el oso polar)
Fuente: *Information Architecture: For the Web and Beyond*, Rosenfeld, Morville & Arango. PDF en `biblioteca/`.
Cómo citar: `[rosenfeld:<concepto>]`

Es el **motor del rol arquitecto-informacion**: estructura, navegación, etiquetado y búsqueda.

## Marco general

- `[rosenfeld:ecologia]` — Toda IA equilibra tres círculos: **contexto** (negocio, objetivos, recursos), **contenido** (volumen, formatos, dueños, dinamismo) y **usuarios** (necesidades, vocabulario, comportamiento de búsqueda). Una IA copiada de otro sitio ignora dos de los tres.
- `[rosenfeld:encontrabilidad]` — Si el usuario no puede encontrarlo, no existe. La pregunta de auditoría: ¿puede el usuario encontrar lo que busca por navegación, por búsqueda y por casualidad razonable?
- `[rosenfeld:necesidades-informacion]` — Los usuarios no siempre buscan "la respuesta exacta": hay búsqueda de ítem conocido, exploración, investigación exhaustiva y re-encuentro. Cada modo exige soportes distintos.

## Los cuatro sistemas (estructura de auditoría de IA)

- `[rosenfeld:organizacion]` — Sistemas de organización: esquemas exactos (alfabético, cronológico, geográfico) vs. ambiguos (por tema, por tarea, por audiencia, híbridos). Los ambiguos son más útiles y más difíciles; el pecado común es el esquema híbrido incoherente en un mismo menú.
- `[rosenfeld:etiquetado]` — Sistemas de etiquetado: las etiquetas hablan el idioma del usuario, no el organigrama. Consistencia en estilo, granularidad y sintaxis; una etiqueta que necesita explicación es un hallazgo.
- `[rosenfeld:navegacion]` — Sistemas de navegación: global, local, contextual y suplementaria (mapas, índices, guías). Deben responder ¿dónde estoy? y ¿a dónde puedo ir? (cruza con `[krug:prueba-del-tronco]`).
- `[rosenfeld:busqueda]` — Sistemas de búsqueda: cuándo amerita buscador, qué se indexa, cómo se presentan resultados, qué pasa con cero resultados. Un buscador malo es peor que ninguno.

## Vocabulario y modelos

- `[rosenfeld:taxonomia]` — Taxonomías y vocabularios controlados: términos preferentes, sinónimos, jerarquías. Controlan la ambigüedad del lenguaje.
- `[rosenfeld:metadatos]` — Metadatos y modelos de contenido: qué atributos tiene cada tipo de contenido y cómo se relacionan; la base de navegación por facetas y contenido conectado.
- `[rosenfeld:top-down-bottom-up]` — IA descendente (del mapa del sitio hacia abajo) e IA ascendente (del contenido hacia arriba: "¿dónde estoy?, ¿qué hay aquí?, ¿qué se relaciona?"). Auditar ambas: llegar desde Google a una página interna es la prueba ascendente.

## Métodos
- `[rosenfeld:inventario-contenido]` — Inventario y auditoría de contenido antes de opinar sobre estructura.
- `[rosenfeld:card-sorting]` — Card sorting (abierto/cerrado) para descubrir el modelo mental del usuario; tree testing para validar jerarquías.

## Cuándo NO aplica (anti-martillo)

- La maquinaria completa (taxonomías, vocabularios controlados, facetas) no aplica a sitios pequeños: para 10–30 páginas, una navegación clara y etiquetas honestas bastan; recomendar infraestructura de IA pesada ahí es sobre-ingeniería.
- `[rosenfeld:busqueda]` no siempre amerita: un buscador mediocre en un sitio chico es peor que una buena navegación. "Agregar buscador" no es la recomendación por defecto.
- `[rosenfeld:organizacion]` no exige pureza absoluta de esquema: los híbridos funcionan si cada bloque es internamente coherente y está visualmente separado; el hallazgo es la mezcla *indistinguible*, no la mezcla.
- La IA no se audita contra un ideal abstracto sino contra la ecología (`[rosenfeld:ecologia]`): la estructura "correcta de manual" puede ser incorrecta para este contenido y estos usuarios.
