# Contribuciones, revisión y aceptación — NexoEntrega 360

## Participantes y responsabilidades acordables

Este documento contiene una **propuesta de asignación** que el equipo debe aceptar o corregir. No implica que las personas hayan escrito código, aprobado las especificaciones o realizado commits.

| Integrante | Responsabilidad sugerida | Evidencia mínima para confirmar |
|---|---|---|
| Natalia Baena Torres | Revisar HU-01 y HU-02, criterios de aceptación | Observaciones fechadas y aprobación explícita de las HU revisadas |
| Ricardo Lora Gutiérrez | Revisar arquitectura y modelo de datos, HU-03 | Revisión firmada o comentario identificable de arquitectura y HU-03 |
| Samuel Ortega Carrascal | Revisar API, HU-04 y correspondencia código/SPEC | Informe de diferencias y constancia de revisión |
| Carlos Ovalle Castaño | Ejecutar pruebas, revisar HU-05, verificar CI | Registro de comando, fecha, resultado y URL de Actions si existe |
| Valeria Patrón García | Revisar bitácora IA, trazabilidad y PDF final | Observaciones y constancia de validación final |

## Registro de aprobación humana

Una persona del equipo que **realmente realice** la revisión puede llenar en `docs/acta_revision_humana.md` su nombre, fecha actual, especificaciones revisadas, correcciones y resultado. Importante: una revisión hecha después de programar es posterior; **no puede declararse retroactivamente previa a la implementación**.

## Aceptación técnica reproducible

- [x] Las 15 pruebas automatizadas pasan en el entorno de preparación (registro en `evidencia_pruebas.txt`).
- [x] El workflow de CI está preparado en `.github/workflows/ci.yml`.
- [x] Existe estructura de proyecto y documentos SPEC versionables.
- [ ] Cada revisor confirmó su trabajo y la fecha real.
- [ ] El equipo verificó el enunciado y el anexo 09 completos.
- [ ] El repositorio fue publicado en GitHub.
- [ ] El workflow se ejecutó en GitHub Actions.
- [ ] El PDF incluye URL pública/privada accesible al docente y SHA/tag final.

## Cómo terminar sin falsas evidencias

1. Cada integrante lee los apartados a su cargo y envía un mensaje explícito de aprobación/corrección con fecha; transcribir únicamente lo que realmente diga.
2. Publicar el repositorio usando `GUIA_PUBLICACION.md`; verificar `Actions`.
3. Copiar URL, SHA y enlaces de evidencia al PDF antes de entregarlo.
