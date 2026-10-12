# database/ — PostgreSQL y PostGIS

**Estado:** hay una definición de contenedor local en docker-compose.yml, pero no existen todavía esquemas ni migraciones SQL de SIA.

- migrations/: scripts Flyway propuestos como V1__crear_esquema.sql.
- seeds/: datos sintéticos de prueba, nunca información personal de clientes.

Antes de modelar tablas, validar qué se necesita almacenar (por ejemplo: edificios ficticios, niveles, nodos y puntos de interés).

Para levantar solo la base de datos: copiar .env.example a .env, establecer una contraseña local y ejecutar docker compose up -d database.
