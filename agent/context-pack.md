# Paquete de contexto

Qué entregar a la IA en cada fase (además de `agent/AGENT.md`).

| Actividad | Entregar a la IA |
|---|---|
| 1 Intención | Problema y condiciones iniciales del taller |
| 2 Requisitos | `docs/intent.md` aprobado |
| 3 Producto | `docs/requirements.md` aprobado |
| 4 Diseño | `requirements.md` + `product-spec.md` |
| 5 Tareas | `technical-spec.md` + `requirements.md` |
| 6 Pruebas | `requirements.md` + `product-spec.md` |
| 7 Implementación | La TASK, su requisito, sección de diseño, sus TEST y restricciones |
| 8 Revisión | Todos los artefactos + resultados de pruebas |
| 9 Evolución | Nueva regla + `traceability.md` |

## Resumen del problema (para pegar)
Biblioteca universitaria pequeña que hoy usa hojas de cálculo. App de consola en Java para un bibliotecario: catálogo de libros (id, título, autor), préstamos (estudiante + fecha prevista de devolución) y devoluciones. Un ejemplar no puede prestarse a dos estudiantes a la vez. Sin autenticación, GUI ni integraciones externas.
