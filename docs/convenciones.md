# Convenciones de identificación

| Prefijo | Artefacto | Formato | Ejemplo | Archivo |
|---|---|---|---|---|
| HU | Historia de usuario | HU-NNN | HU-001 | docs/requirements.md |
| CA | Criterio de aceptación | HU-NNN-CAn | HU-001-CA1 | docs/requirements.md |
| RNF | Requisito no funcional | RNF-NNN | RNF-001 | docs/requirements.md |
| RN | Regla de negocio | RN-NNN | RN-001 | docs/requirements.md |
| RES | Restricción | RES-NNN | RES-001 | docs/requirements.md |
| CU | Caso de uso | CU-NNN | CU-001 | docs/product-spec.md |
| DEC | Decisión de diseño | DEC-NNN | DEC-001 | docs/decisions.md |
| TASK | Tarea de implementación | TASK-NNN | TASK-001 | tasks/TASK-001.md |
| TEST | Caso de prueba | TEST-NNN | TEST-001 | tests/*.md |

## Reglas
1. Los identificadores **no se reutilizan**. Si un elemento se elimina, se marca como `[ELIMINADO]` y se conserva su ID.
2. Numeración con 3 dígitos y secuencial por prefijo.
3. Toda TASK y todo TEST deben referenciar al menos una HU, RN o RNF.
4. Los commits mencionan el ID afectado: `TASK-003: implementa registro de préstamo`.
5. Los cambios de requisitos (ej. Act. 9) se registran en `review/change-log.md` antes de tocar el código.
