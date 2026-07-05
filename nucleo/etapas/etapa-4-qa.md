# Etapa 4 — QA de implementación
Rol: qa-implementacion. Requiere C3 aprobada + build accesible. Salida: `50-qa/informe-qa.md` → Compuerta C4 (firma de release).

## Procedimiento

1. **Preparación:** verificar acceso al build (URL/staging/local). Sin build accesible → detenerse y pedirlo; no se hace QA sobre capturas ajenas salvo instrucción del DC (y se registra la limitación).
2. **Verificación por criterio:** recorrer cada criterio dado/cuando/entonces de la spec aprobada. Veredicto `cumple / no-cumple / no-verificable` + captura por ítem (`10-evidencia/qa-<flujo>-<criterio>.png`). Inspeccionar valores computados cuando el criterio es medible (contraste, tamaños, tiempos).
3. **Criterio ambiguo:** `no-verificable` + retorno H9 al especificador. QA no interpreta.
4. **Regresión heurística:** barrido Krug + Nielsen sobre lo construido: defectos nuevos que la spec no previó (foco perdido, feedback ausente, estados de runtime). Se reportan como hallazgos con las 6 reglas de evidencia.
5. **Verificación emocional:** provocar estados de error/vacío/espera reales y compararlos con la persona de diseño.
6. **Responsive y modo oscuro** si el alcance lo incluye: verificar en móvil/tablet/escritorio.
7. **Informe:** tabla de criterios con veredictos y evidencia, defectos nuevos por severidad, y **veredicto global recomendado**: listo para firma / devolver a desarrollo (con la lista mínima de bloqueos, típicamente todo `no-cumple` en criterios de severidad ≥3).
8. **Solicitar C4:** el DC firma el release o lo devuelve. La firma es humana siempre.
9. **Cierre y aprendizaje (tras la firma):** el orquestador propone registrar 1–3 patrones en `nucleo/memoria-patrones/` con `nucleo/plantillas/patron.md`: problema → recomendación aplicada → resultado (mejoró/empeoró/neutro/no-medido) → aprendizaje. Es lo que convierte cada proyecto en ventaja acumulada del estudio.
