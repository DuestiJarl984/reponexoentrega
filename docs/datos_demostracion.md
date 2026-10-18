# Datos ficticios del caso para demostración

Son registros inventados **solo para ejemplificar** el funcionamiento de NexoEntrega 360; no equivalen a ejecuciones realizadas ni a evidencias externas.

| Tipo | Identificador de ejemplo | Nombre / dato | Cantidad / estado |
|---|---|---|---|
| Producto | DEMO-P01 | Cuaderno académico | 30 unidades |
| Producto | DEMO-P02 | Kit de laboratorio | 12 unidades |
| Producto | DEMO-P03 | Memoria USB de apoyo | 25 unidades |
| Solicitud | DEMO-S01 | Solicitante: Andrea Vega, Kit de laboratorio | 2 unidades, PENDIENTE |
| Solicitud | DEMO-S02 | Solicitante: Julián Soto, Cuaderno académico | 5 unidades, PENDIENTE |
| Entrega | DEMO-E01 | Operador de ejemplo: Laura Pérez | ASIGNADA |
| Decisión | DEMO-D01 | Sugerencia de reserva y aprobación supervisada | EJEMPLO, NO REGISTRO REAL |

## Ejemplo de aceptación funcional
Dado un producto con 12 unidades, cuando una solicitud pendiente reserva 2 unidades, el sistema debe guardar 10 unidades restantes y cambiar el estado a RESERVADA. Un nuevo intento de reservar esa misma solicitud debe devolver conflicto 409 sin volver a descontar existencias.
