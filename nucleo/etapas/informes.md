# Transversal — Generación de informes
Rol: redactor-informes. Disponible en cualquier momento del proyecto. Salida: `60-informes/`.

## Cuándo se dispara
- El DC pide un informe (interno o de cliente) de cualquier etapa.
- Al cerrar una compuerta, el orquestador ofrece generar el informe correspondiente.
- Al firmar C4: informe de cierre de proyecto (opcional pero recomendado).

## Procedimiento

1. **Definir tipo y audiencia:** interno (equipo/DC) o cliente. Cliente ⇒ solo artefactos `aprobado`.
2. **Recolectar la base:** artefactos de las etapas cubiertas + decisiones registradas en `ESTADO.md` + evidencia de `10-evidencia/`.
3. **Redactar en pirámide** (plantilla `informe-cliente.md` / `informe-interno.md`):
   - Resumen ejecutivo ≤ media página: situación → hallazgo/decisión central → recomendación.
   - Los 3–5 puntos que importan, con captura y severidad traducida a negocio ("impide completar la compra en móvil", no "catástrofe heurística grado 4").
   - Detalle completo en anexo.
   - Próximos pasos con responsable propuesto.
4. **Traducir el canon a lenguaje llano** en informes de cliente: `[nielsen:visibilidad-estado]` → "el sistema no informa qué está pasando (principio de visibilidad del estado, Nielsen)". La fuente da autoridad; la jerga se queda en casa.
5. **Formato final:** markdown siempre; si la plataforma tiene las herramientas, exportar a .docx (informes) o .pptx (presentación de dirección) a pedido.
6. **Revisión del DC antes de salir del estudio.** Sin excepción para material de cliente.

## Reglas
- El informe reporta, no re-decide: hueco descubierto al redactar → devolver al orquestador.
- Severidades no se suavizan; se reformulan con tacto.
- Nada de métricas inventadas.
