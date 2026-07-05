# Etapa 0 — Encuadre
Rol: orquestador. Salida: `00-brief/brief.md` con check C0 del DC.

1. **Crear el proyecto** si no existe: `proyectos/<cliente>/<aaaa-mm>-<proyecto>/` con las carpetas estándar, `ESTADO.md` y `BITACORA.md` desde `nucleo/plantillas/`. Darlo de alta en `proyectos/PORTAFOLIO.md` (crearlo desde la plantilla si no existe).
2. **Normalizar el brief** con la plantilla `brief.md`: objetivo de negocio, alcance (qué flujos/pantallas SÍ y cuáles NO), audiencia, restricciones (marca, técnica, plazos), definición de éxito, y tipo de encargo (auditoría / rediseño / producto nuevo / QA de build).
3. **Inventariar accesos:** URLs, staging, Figma, credenciales de prueba, capturas provistas. Lo inaccesible se anota desde ya como `no-verificable` potencial.
4. **Elegir profundidad:** auditoría exprés (solo barrido Krug + 1 flujo crítico) o completa (heurística + IA). Proponer al DC según alcance y plazo.
5. **Solicitar C0** (check ligero): ¿el encuadre es correcto? ok / corregir. Registrar en `ESTADO.md`.

**Errores comunes que esta etapa previene:** auditar flujos que a nadie importan, descubrir a mitad de auditoría que no hay credenciales, y "alcance infinito".
