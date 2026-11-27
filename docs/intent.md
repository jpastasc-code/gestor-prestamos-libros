# Engineering Intent Document

> Actividad 1 · Prompts 2.1–2.4 (Iroko, 2026, cap. 2). Proceso y revisión: `review/act-1-intencion.md`.
> **Versión:** 1.0 · **Estado:** [x] Aprobado por el equipo

## 1. Nombre del proyecto
**Gestor de préstamos de libros**

## 2. Problema
El **bibliotecario** de una biblioteca universitaria pequeña administra el catálogo y los préstamos en **hojas de cálculo**, sin control del estado de cada ejemplar. Por eso no puede saber con rapidez **qué ejemplares están disponibles o prestados ni qué préstamos están vencidos**, y corre el riesgo de prestar un ejemplar que ya está prestado.
El sistema debe **mantener el estado de cada ejemplar y de cada préstamo** y mostrarlo cuando se consulte.

## 3. Usuarios
| Tipo | Usuario | Relación con el sistema |
|---|---|---|
| Principal | Bibliotecario | Único usuario que opera la aplicación |
| Beneficiario (no usa el sistema) | Estudiante | Recibe ejemplares en préstamo; solo se registran su código y nombre |

## 4. Objetivos
| ID | Objetivo |
|---|---|
| OBJ-1 | Saber en todo momento si un ejemplar está disponible o prestado |
| OBJ-2 | Identificar los préstamos vencidos sin revisar registros a mano |
| OBJ-3 | Evitar que un ejemplar se preste a dos estudiantes al mismo tiempo |
| OBJ-4 | Reemplazar las hojas de cálculo por un registro único y persistente |

## 5. Capacidades principales (primera versión)
| ID | Capacidad |
|---|---|
| CAP-1 | Registrar y consultar libros (identificador, título, autor) |
| CAP-2 | Registrar los ejemplares de un libro, cada uno con su código |
| CAP-3 | Consultar el estado de los ejemplares (disponible / prestado) |
| CAP-4 | Registrar el préstamo de un ejemplar disponible a un estudiante (código y nombre), con la fecha prevista de devolución que ingresa el bibliotecario |
| CAP-5 | Registrar la devolución de un ejemplar prestado |
| CAP-6 | Consultar los préstamos activos y los vencidos |
| CAP-7 | Conservar los datos entre ejecuciones (archivo local) |

**Definiciones**
- **Ejemplar:** copia física de un libro; es lo que se presta.
- **Préstamo activo:** préstamo registrado cuyo ejemplar aún no ha sido devuelto.
- **Préstamo vencido:** préstamo activo cuya fecha prevista de devolución es **anterior** a la fecha actual.

## 6. Fuera de alcance
- Autenticación, usuarios y roles
- Interfaz gráfica
- Integraciones externas (correo, sistemas de la universidad)
- Registro o gestión de estudiantes
- Multas, reservas y renovaciones
- Reportes y estadísticas
- Despliegue en servidor

## 7. Restricciones
| ID | Restricción |
|---|---|
| R-1 | Aplicación de consola |
| R-2 | Lenguaje Java |
| R-3 | Un solo usuario operando (el bibliotecario) |
| R-4 | Datos en un archivo local, sin servidor de base de datos |
| R-5 | Ejecución local; sin despliegue |
| R-6 | Desarrollo por un equipo de 3 estudiantes, dentro del tiempo del taller |

## 8. Riesgos
| ID | Riesgo | Mitigación prevista |
|---|---|---|
| RG-1 | Confundir libro con ejemplar en reglas y datos | Definiciones explícitas (sección 5) en todos los artefactos |
| RG-2 | Fechas mal ingresadas (formato inválido o anterior al préstamo) | Validaciones definidas en los requisitos |
| RG-3 | Pérdida o daño del archivo de datos | Manejo de errores al leer y escribir |
| RG-4 | La IA agrega funcionalidades fuera de alcance | AGENT.md (regla 2) y revisión crítica en cada fase |

## 9. Criterios de éxito
| ID | Criterio verificable |
|---|---|
| CE-1 | El bibliotecario consulta si un ejemplar está disponible con **una sola** consulta |
| CE-2 | El sistema **rechaza siempre** el préstamo de un ejemplar que ya está prestado |
| CE-3 | El listado de vencidos muestra **exactamente** los préstamos activos con fecha prevista anterior a hoy |
| CE-4 | Tras registrar una devolución, el ejemplar aparece como disponible |
| CE-5 | Los datos registrados siguen disponibles al cerrar y volver a abrir la aplicación |

## 10. Preguntas abiertas (para la Actividad 2)
- ¿Se pueden **modificar o eliminar** libros y ejemplares? ¿Qué pasa si un ejemplar está prestado?
- ¿Los identificadores los ingresa el bibliotecario o los asigna el sistema?
