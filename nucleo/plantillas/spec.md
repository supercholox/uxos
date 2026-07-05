---
proyecto: <cliente>-<proyecto>
etapa: 3-especificacion
artefacto: spec
estado: borrador
autor-rol: especificador
fecha: <aaaa-mm-dd>
depende-de: [30-direccion/direccion.md]
version: 1
---

# Especificación — <componente/flujo>

<!-- Si es v2+: changelog aquí, con referencia a la versión anterior y al retorno H9 que la motivó. -->

## Estados
| Estado | Comportamiento | Copy (ES) | Referencia visual |
|---|---|---|---|
| Normal | | | |
| Hover / foco | | | |
| Carga | <!-- feedback si >400 ms [yablonski:doherty] --> | | |
| Vacío `[walter:estados-vacios]` | | | |
| Error `[walter:estados-error]` | <!-- qué pasó + qué hacer, voz de la persona --> | | |
| Éxito | | | |

## Criterios de aceptación
<!-- Uno por comportamiento. Verificable mirando el build: cumple / no-cumple. -->
| ID | Dado | Cuando | Entonces | Severidad si falla |
|---|---|---|---|---|
| CA-01 | | | | |

## Criterios no funcionales medibles
- Contraste texto/fondo ≥ 4.5:1 (cuerpo) / 3:1 (títulos grandes)
- Objetivo táctil ≥ 44×44 px `[yablonski:fitts]`
- Respuesta visible < 400 ms o indicador de progreso `[yablonski:doherty]`

## Tokens
| Token | Valor | Uso |
|---|---|---|

## Notas para desarrollo
<!-- Orden de tabulación, comportamiento de teclado, responsive, casos borde. -->
