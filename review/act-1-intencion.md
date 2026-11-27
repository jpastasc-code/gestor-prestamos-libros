# Actividad 1 — Proceso con la IA (Prompts 2.1–2.4)

**Referencia:** Iroko (2026), cap. 2, secciones 2.1–2.7. **IA utilizada:** Claude. **Resultado final:** `docs/intent.md`.

---

## Prompt 2.1 — Clarify a raw idea

**Entrada:** problema y condiciones iniciales del taller (`agent/context-pack.md`).

**Preguntas de la IA y respuestas del equipo**
| # | Pregunta de la IA | Respuesta del equipo |
|---|---|---|
| P1 | El enunciado habla de "libro" y de "ejemplar": ¿un libro puede tener varios ejemplares? | Sí. Libro (id, título, autor) y ejemplares con código propio; se presta el ejemplar |
| P2 | ¿Se lleva un registro de estudiantes? | No. El préstamo guarda código y nombre del estudiante |
| P3 | ¿Los datos deben conservarse al cerrar la app? | Sí, en un archivo local |
| P4 | ¿Quién define la fecha prevista de devolución? | El bibliotecario la ingresa al prestar |

---

## Prompt 2.2 — Improve a problem statement

**Respuesta de la IA**
| Elemento | Contenido |
|---|---|
| Usuario afectado | Bibliotecario de una biblioteca universitaria pequeña |
| Dificultad actual | Registra catálogo y préstamos en hojas de cálculo, sin control del estado de cada ejemplar |
| Consecuencia | No sabe con rapidez qué ejemplares están disponibles o prestados ni qué préstamos están vencidos; puede prestar un ejemplar que ya está prestado |
| Mejora deseada | Una herramienta que mantenga el estado de cada ejemplar y de cada préstamo y lo muestre bajo consulta |

---

## Prompt 2.3 — Translate business need into software direction

**Respuesta de la IA**
| Elemento | Contenido |
|---|---|
| Usuarios principales | Bibliotecario (único operador) |
| Capacidades | Catálogo de libros y ejemplares; préstamo; devolución; consulta de disponibilidad; consulta de préstamos activos y vencidos |
| Datos clave | Libro (id, título, autor); Ejemplar (código, libro, estado); Préstamo (ejemplar, código y nombre del estudiante, fecha de préstamo, fecha prevista, fecha de devolución) |
| Calidad esperada | Datos consistentes (un ejemplar, un préstamo activo); validación de entradas; mensajes de error claros; persistencia confiable |
| Excluido de la v1 | Multas, reservas, renovaciones, notificaciones, gestión de estudiantes, reportes, autenticación, GUI |

---

## Prompt 2.4 — Create an Engineering Intent Document

**Entrada:** resultados de 2.1–2.3. **Salida:** `docs/intent.md`.

---

## Revisión crítica del equipo
> Esta sección la completan ustedes. Lo que encuentren incorrecto, incompleto o inadecuado se registra también en `review/registro-ia.md`.

| Verificar | ☐/☑ | Observación |
|---|---|---|
| El problema no contiene datos inventados (solo lo que dice el enunciado) | ☐ | |
| Ninguna capacidad excede las condiciones iniciales del taller | ☐ | |
| "Datos clave" de 2.3 no adelanta decisiones de diseño indebidas | ☐ | |
| Los criterios de éxito son verificables | ☐ | |
| Las exclusiones son correctas (¿falta o sobra alguna?) | ☐ | |
| La definición de "préstamo vencido" coincide con lo que espera la biblioteca | ☐ | |

**Estado:** ☐ Aprobado por el equipo
