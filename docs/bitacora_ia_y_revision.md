# Bitácora de IA y verificaciones — NexoEntrega 360

## Naturaleza de la evidencia
Documento elaborado con asistencia de ChatGPT. Los campos relativos a actividad humana no acreditada se distinguen expresamente. No representa un acta firmada ni una revisión previa efectuada.

| Registro | Actividad asistida por IA | Decisión y justificación | Verificación objetiva | Validación humana |
|---|---|---|---|---|
| IA-01 | Propuesta de cinco HU para solicitudes, inventario, reservas, entregas y decisiones. | Descomponer el sistema en funcionalidades comprobables. | Documentos `specs/HU-01.md` a `HU-05.md` incluidos. | Pendiente de contraste con enunciado oficial. |
| IA-02 | Generación de API HTTP y esquema SQLite. | Biblioteca estándar para ejecutar sin dependencias externas. | Código en `app/server.py` y documentos de arquitectura. | Pendiente de aprobación del equipo. |
| IA-03 | Identificación de carrera en reservas concurrentes. | Usar `BEGIN IMMEDIATE` antes de leer stock y estado para serializar escrituras. | Prueba automatizada de concurrencia exitosa en entorno de preparación. | Pendiente de revisión humana del diff. |
| IA-04 | Diseño de pruebas negativas. | Agregar 404 de producto y decisión inexistentes, 409 de doble asignación, doble finalización, reserva concurrente. | 15/15 pruebas correctas en sesión de preparación. | Pendiente de reproducir en dispositivo del equipo. |
| IA-05 | Redacción del informe final. | Mantener trazabilidad explícita y no atribuir actividades inexistentes. | PDF y ZIP generados. | Pendiente de lectura y aceptación por cada integrante. |

## Controles humanos que deben realizarse
1. Leer la HU correspondiente y confirmar actor, precondiciones, reglas, códigos y casos de error.
2. Comparar la HU con el enunciado oficial y dejar constancia de desviaciones si las hay.
3. Ejecutar `python -m unittest discover -s tests -v` y guardar la salida propia.
4. Revisar si el comportamiento real del endpoint cumple cada criterio de aceptación.
5. Registrar nombre, fecha, hallazgo y decisión en `docs/acta_revision_humana.md`.

## Límite de la IA operativa
`/requests/{id}/suggest` implementa sugerencias basadas en reglas transparentes. No llama a un LLM; la asistencia de IA en el desarrollo es distinta de incorporar un modelo generativo en producción. Si la rúbrica exige esto último, la funcionalidad necesita ampliación.
