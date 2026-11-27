# Plan del espacio de trabajo — Actividad 0

**Referencia:** Iroko (2026), cap. 4, secciones 4.2–4.9. **Prompt usado:** 4.4 *Generate a workspace plan*.

## 1. Prompt enviado a la IA

```
I am starting a new spec-driven AI engineering project.
Project idea: A console application (Java) for a small university library. One librarian
manages the book catalog (id, title, author) and records loans and returns. Each loan is
linked to a student and an expected return date. A copy cannot be lent to two students at
the same time. No authentication, no GUI, no external integrations.
Create a local workspace plan using docs, tasks, tests, src, review, agent, and ops. For each
folder, list the first files I should create and what each file should contain. Keep everything
self-contained inside the book workflow.
```

## 2. Propuesta de la IA (resumen)

| Carpeta | Archivos iniciales | Contenido |
|---|---|---|
| docs/ | intent.md, requirements.md, product-spec.md, technical-spec.md, traceability.md, decisions.md | Intención, HU y RNF, casos de uso, diseño, trazabilidad, decisiones |
| tasks/ | task-index.md, TASK-001.md | Índice de tareas y primera tarea |
| tests/ | test-plan.md, acceptance-tests.md, unit-tests.md, integration-tests.md, failure-tests.md | Estrategia y casos de prueba |
| src/ | README.md | Código fuente |
| review/ | change-log.md, review-log.md | Cambios y revisiones |
| agent/ | AGENT.md, context-pack.md, prompt-library.md | Reglas, contexto y prompts de la IA |
| ops/ | deployment-checklist.md, maintenance-notes.md | Despliegue y mantenimiento |

## 3. Revisión crítica y adaptaciones del equipo

| # | Propuesta de la IA | Decisión | Justificación |
|---|---|---|---|
| A1 | `ops/deployment-checklist.md` | **Reemplazado** por `ops/guia-ejecucion.md` | El taller no exige despliegue en servidor; basta la ejecución local (Act. 8) |
| A2 | `tasks/TASK-001.md` desde el inicio | **Rechazado por ahora** | Las tareas se derivan de la especificación técnica (Act. 5); crearla ahora sería adelantarse |
| A3 | Sin archivo de convenciones de ID | **Agregado** `docs/convenciones.md` | El taller exige convenciones para HU, CU, TASK y TEST |
| A4 | Sin registro de interacciones con IA | **Agregado** `review/registro-ia.md` | La entrega final pide documentar propuestas incorrectas de la IA y su corrección |
| A5 | Sin `.gitignore` ni guía de colaboración | **Agregados** `.gitignore` y `CONTRIBUTING.md` | Trabajo en grupo de 3 con Git; el PDF del libro no debe versionarse |
| A6 | Ubicación de pruebas automatizadas en Java | **Pendiente (Act. 4)** | Maven/Gradle usan `src/test/java`; el taller pide pruebas en `tests/`. Se decide con el diseño técnico (ver `decisions.md`, DEC-001) |
| A7 | Resto de la estructura | **Aceptado** | Coincide con la estructura mínima del taller |

## 4. Estructura final aprobada

```
app_Especidicaciones_IA/
├── README.md · CONTRIBUTING.md · .gitignore
├── docs/    intent · requirements · product-spec · technical-spec · traceability · decisions · convenciones · workspace-plan
├── tasks/   task-index
├── tests/   test-plan · acceptance-tests · unit-tests · integration-tests · failure-tests
├── src/     README
├── review/  change-log · review-log · registro-ia
├── agent/   AGENT · context-pack · prompt-library
└── ops/     guia-ejecucion · maintenance-notes
```

**Estado:** ☐ Aprobado por el equipo
