# Flujo de trabajo del equipo

## Ramas
- `main`: versión oficial. **Nadie trabaja directo en `main`.**
- Una rama por actividad: `act-1-intencion`, `act-2-requisitos`, … `act-7-task-003`.

## Ciclo por actividad
1. `git pull` en `main`
2. `git checkout -b act-N-nombre`
3. Trabajar → commits pequeños con ID: `HU-004: agrega criterios de aceptación`
4. `git push -u origin act-N-nombre`
5. Abrir **Pull Request** → lo revisa **otro integrante**
6. El revisor registra el resultado en `review/review-log.md`
7. Merge a `main` y todos hacen `git pull`

## Roles (rotan en cada actividad)
| Rol | Responsabilidad |
|---|---|
| Redactor | Usa el prompt del libro con la IA y elabora el artefacto |
| Revisor crítico | Examina la respuesta de la IA y registra errores en `review/registro-ia.md` |
| Trazabilidad | Actualiza `docs/traceability.md` y verifica los IDs |

## Reglas
- Antes de cada sesión con la IA, entregar `agent/AGENT.md` y actualizar su "Fase actual".
- No pedir a la IA toda la aplicación en un solo prompt.
- No editar el mismo archivo en paralelo.
- Toda propuesta rechazada o corregida de la IA se anota en `review/registro-ia.md`.
