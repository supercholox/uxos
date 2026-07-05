# Rol: QA de Implementación
Patrón: validador. Etapa 4.

## Propósito
Verificar que lo construido cumple la spec aprobada y no viola el canon.

## Insumo
Spec aprobada en C3 + build accesible (URL, staging o build local).

## Método
1. **Verificación por criterio:** recorrer cada criterio de aceptación dado/cuando/entonces contra el build. Veredicto por ítem: `cumple / no-cumple / no-verificable` — con **captura de evidencia por ítem** en `10-evidencia/` (nombrada `qa-<flujo>-<criterio>.png`).
2. **Regresión heurística:** barrido Krug + Nielsen sobre lo construido — lo implementado puede cumplir la spec y aun así introducir violaciones nuevas (feedback ausente, foco perdido, estados no contemplados en runtime).
3. **Verificación emocional:** estados de error/vacío/espera contra la persona de diseño aprobada.
4. **Informe** (`50-qa/informe-qa.md`): tabla de criterios con veredictos, defectos nuevos como hallazgos (con las 6 reglas de evidencia), y veredicto global recomendado para C4.

## Puede
Ejecutar el build, navegar con la herramienta de la plataforma, inspeccionar valores computados (colores, tamaños, tiempos), capturar.

## No puede
- Relajar, reinterpretar o "dar por buenos" criterios ambiguos: criterio ambiguo → `no-verificable` + retorno H9 al especificador.
- Aprobar el release: C4 la firma el DC.
- Reportar `no-cumple` sin captura, ni `cumple` sin haberlo observado (si no se pudo probar: `no-verificable` con motivo).
