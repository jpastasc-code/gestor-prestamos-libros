# Biblioteca de prompts

Prompts del libro (Iroko, 2026) usados en el taller. Se copian tal cual y se rellenan los `[ ]`.

| Prompt | Nombre | Actividad | Estado |
|---|---|---|---|
| 4.4 | Generate a workspace plan | 0 | Usado (IA-001) |
| 4.3 | Improve an agent instruction file | 0 | Usado (IA-002) |
| 2.1 | Clarify a raw idea | 1 | Pendiente |
| 2.2 | Improve a problem statement | 1 | Pendiente |
| 2.3 | Translate business need into software direction | 1 | Pendiente |
| 2.4 | Create an Engineering Intent Document | 1 | Pendiente |
| 3.1 | Draft requirements from intent | 2 | Pendiente |
| 3.2 | Turn a spec into tasks | 5 | Pendiente |
| 3.3 | Implement one controlled task | 7 | Pendiente |
| 3.4 | Stage gate review | 8 | Pendiente |

---

## Prompt 4.4 — Generate a workspace plan
```
I am starting a new spec-driven AI engineering project.
Project idea: [describe idea]
Create a local workspace plan using docs, tasks, tests, src, review, agent, and ops. For each
folder, list the first files I should create and what each file should contain. Keep everything
self-contained inside the book workflow.
```

## Prompt 4.3 — Improve an agent instruction file
```
Review this agent instruction file for a beginner spec-driven AI engineering project.
Instruction file: [paste AGENT.md]
Find vague rules, missing boundaries, missing test expectations, and anything that could allow
the assistant to make uncontrolled changes. Return a cleaner version.
```
