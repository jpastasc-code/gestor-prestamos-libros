# Registro de interacciones con la IA

Sirve para la entrega final: propuestas **incorrectas, incompletas o inadecuadas** de la IA y cómo se corrigieron.

| ID | Actividad | Prompt | Problema detectado en la respuesta | Corrección del equipo |
|---|---|---|---|---|
| IA-001 | 0 | 4.4 Generate a workspace plan | La propuesta seguía la plantilla genérica de la sección 4.9 sin adaptarla al taller: incluía `deployment-checklist.md` (no hay despliegue) y `TASK-001` antes de tener especificación; no incluía convenciones de ID, registro de IA ni `.gitignore` | Adaptaciones A1–A7 en `docs/workspace-plan.md` |
| IA-002 | 0 | 4.3 Improve an agent instruction file | La plantilla v1 tenía reglas vagas y límites faltantes (detalle abajo) | AGENT.md v2 |
| IA-003 | 1 | 2.1–2.4 | Sin hallazgos en la revisión del equipo | No aplica |

> Registren aquí solo problemas **reales** que ustedes detecten. No inventen errores.

---

## IA-002 · Revisión de AGENT.md

### AGENT.md v1 (plantilla de la sección 4.7)
```
Project goal: Aplicación de consola para préstamos de libros.
Current stage: intent
Use these folders: docs/, tasks/, tests/, src/, review/
Rules:
1. Follow the current task only.
2. Do not add unrequested features.
3. Do not change unrelated files.
4. Ask before making assumptions that affect scope, security, data, or architecture.
5. Explain important changes in simple language.
6. Connect every implementation change to a requirement and a test check.
Output format: Summary · Files affected · Requirement covered · Tests to run · Risks or assumptions
```

### Hallazgos de la revisión (Prompt 4.3)
| Tipo | Hallazgo | Cambio en v2 |
|---|---|---|
| Regla vaga | El objetivo no dice qué hace el sistema ni para quién | Objetivo con actor, datos y regla clave |
| Límite faltante | No declara lo que está fuera de alcance | Sección "Fuera de alcance" |
| Límite faltante | No impide generar artefactos de fases futuras | Regla 1 |
| Límite faltante | No impide agregar dependencias o librerías | Regla 2 |
| Regla vaga | "Unrelated files" no define qué hacer si se necesita otro archivo | Regla 3: detenerse y preguntar |
| Cambio no controlado | No indica qué hacer si debe continuar con un supuesto | Regla 4: etiqueta `[SUPUESTO]` |
| Cambio no controlado | No define qué documento manda ante contradicciones | Regla 5: `docs/` aprobados prevalecen |
| Pruebas faltantes | No prohíbe alterar pruebas para que pasen | Regla 7 |
| Pruebas faltantes | No exige honestidad sobre lo ejecutado | Regla 8 |
| Omisión | Faltaban `agent/` y `ops/` y las convenciones de ID | Tabla de carpetas + referencia a convenciones |
| Omisión | Lenguaje e idioma no definidos | Java; respuestas en español |

### Revisión del equipo
[x] El equipo validó que las reglas de la v2 son adecuadas y no sobrantes.
