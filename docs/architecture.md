# Arquitectura y modelo de datos

Cliente HTTP (JSON) -> Handler HTTP -> process (casos de uso) -> SQLite.

Entidades: products(id PK,name UNIQUE,stock CHECK >=0); requests(id PK,customer,product_id FK,quantity CHECK >0,status); deliveries(id PK,request_id UNIQUE FK,assignee,status); decisions(id PK,request_id FK,suggestion,rationale,approved,reviewer).

Máquina de estados: PENDIENTE -> RESERVADA -> ENTREGADA.

Decisiones: sugerencia generada por reglas explícitas; la persona revisora aprueba/rechaza. No se emplea un proveedor externo de modelos.

Errores: 400 validación, 404 inexistente, 409 conflicto, 201 creación, 200 éxito. Cuerpo JSON siempre.
