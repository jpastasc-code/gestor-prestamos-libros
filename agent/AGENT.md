# INSTRUCCIONES PARA EL ASISTENTE DE IA

> Versión 2 · revisada con el Prompt 4.3 (ver `review/registro-ia.md`, IA-002).
> Se entrega al inicio de cada sesión con la IA, junto con los artefactos de la fase actual.

## Objetivo del proyecto
Aplicación de consola en **Java** para una biblioteca universitaria pequeña. Un **bibliotecario** administra el catálogo de libros (identificador, título, autor) y registra préstamos y devoluciones. Cada préstamo se asocia a un estudiante y a una fecha prevista de devolución. Un ejemplar no puede prestarse a dos estudiantes al mismo tiempo.

**Fuera de alcance:** autenticación, interfaz gráfica, integraciones externas, despliegue en servidor.

## Fase actual
`Actividad 1 — Intención de ingeniería` (siguiente: Actividad 2 — Requisitos)
(Actualizar en cada fase: 1 Intención · 2 Requisitos · 3 Producto · 4 Diseño · 5 Tareas · 6 Pruebas · 7 Implementación · 8 Revisión · 9 Evolución)

## Carpetas
| Carpeta | Uso |
|---|---|
| docs/ | Intención, requisitos, especificaciones, trazabilidad, decisiones |
| tasks/ | Una tarea por archivo (`TASK-NNN.md`) e índice |
| tests/ | Planes y casos de prueba |
| src/ | Código fuente Java |
| review/ | Revisiones, cambios y registro de interacciones con la IA |
| agent/ | Este archivo, contexto y prompts |
| ops/ | Guía de ejecución y mantenimiento |

Identificadores según `docs/convenciones.md` (HU, CU, RN, RNF, RES, TASK, TEST, DEC).

## Reglas
1. **Una fase a la vez.** Trabaja solo en la fase o tarea indicada. No generes artefactos de fases posteriores.
2. **Nada sin solicitar.** No agregues funcionalidades, campos, dependencias ni librerías que no estén en los requisitos aprobados. Si crees que falta algo, **propónlo por separado** y marca la sugerencia como `[SUGERENCIA]`.
3. **Límites de archivos.** Modifica solo los archivos que indique la tarea. Si necesitas tocar otro, detente y pregunta.
4. **Supuestos explícitos.** Antes de asumir algo que afecte alcance, datos, reglas de negocio o arquitectura, pregunta. Si debes continuar, etiqueta el supuesto como `[SUPUESTO]`.
5. **Fuente de verdad.** Los documentos aprobados en `docs/` prevalecen sobre cualquier propuesta tuya. Si detectas una contradicción entre documentos, señálala; no la resuelvas por tu cuenta.
6. **Trazabilidad.** Todo cambio de código debe citar la TASK, el requisito (HU/RN/RNF) y los TEST que lo verifican.
7. **Pruebas.** No des por terminada una tarea sin indicar las pruebas que deben ejecutarse y su resultado esperado. No modifiques ni elimines pruebas existentes para que pasen.
8. **Honestidad.** No afirmes que algo fue probado o ejecutado si no lo fue. Indica lo que no pudiste verificar.
9. **Simplicidad.** Prefiere la solución más simple que cumpla el requisito. Código Java estándar, nombres claros en español o inglés (consistentes), sin código muerto.
10. **Idioma.** Responde en español. Los identificadores de código siguen la convención que fije la especificación técnica.

## Formato de respuesta
- **Resumen** de lo realizado
- **Archivos** creados o modificados
- **Requisitos cubiertos** (IDs)
- **Pruebas** a ejecutar y resultado esperado
- **Supuestos, riesgos y sugerencias** (`[SUPUESTO]`, `[SUGERENCIA]`)
