# NexoEntrega 360 - prototipo educativo SDD

Implementación de referencia del caso, **pendiente de contrastar contra el enunciado completo y la rúbrica oficial**. Usa Python 3.10+ sin dependencias externas. La asistencia automatizada es un **motor de reglas**, no una llamada a un modelo de IA generativa; las sugerencias requieren revisión humana y no realizan acciones automáticamente.

## Ejecutar

```bash
python -m app.server
```

En otra terminal:

```bash
python -m unittest discover -s tests -v
```

## Ejemplo de uso

```bash
curl -X POST http://localhost:8000/products -H 'Content-Type: application/json' -d '{"name":"Caja","stock":10}'
curl -X POST http://localhost:8000/requests -H 'Content-Type: application/json' -d '{"customer":"Ana","product_id":1,"quantity":2}'
curl -X POST http://localhost:8000/requests/1/reserve -H 'Content-Type: application/json' -d '{}'
curl -X POST http://localhost:8000/deliveries -H 'Content-Type: application/json' -d '{"request_id":1,"assignee":"Luis"}'
curl -X POST http://localhost:8000/requests/1/suggest -H 'Content-Type: application/json' -d '{}'
curl -X POST http://localhost:8000/decisions/1/review -H 'Content-Type: application/json' -d '{"reviewer":"Persona revisora","approved":true}'
```

Consultas GET: `/health`, `/products`, `/requests`, `/deliveries`, `/decisions`.

## Límites

Sin autenticación ni control de roles; solo para ejecución local académica. Persistencia SQLite local, no apto para producción. Los IDs de ejemplo asumen una base vacía. Ajustar HU y criterios a la fuente oficial antes de declarar aceptación.


## Estado de verificación
Se incluyen pruebas reproducibles y un flujo de CI configurado. La ejecución en GitHub Actions requiere publicar el repositorio y revisar la pestaña Actions. Los documentos SPEC necesitan aceptación humana efectiva.

## Evidencia y material adicional

- `docs/bitacora_ia_y_revision.md`: registro del apoyo de IA, decisiones técnicas y verificaciones objetivas.
- `docs/acta_revision_humana.md`: formato para registrar revisiones y aceptación humanas reales.
- `docs/datos_demostracion.md`: registros completamente ficticios para ilustrar el caso.

Los registros ficticios no constituyen pruebas, aprobación ni contribuciones reales. La ejecución de GitHub Actions, los enlaces, las revisiones y los commits deben corresponder a acciones efectuadas por el equipo.
