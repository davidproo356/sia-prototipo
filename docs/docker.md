# Guía Docker de SIA

En fase 0 se puede levantar **solamente PostgreSQL/PostGIS**. Backend y ai necesitan código futuro.

1. Copia .env.example a .env (en PowerShell: Copy-Item .env.example .env).
2. Cambia DB_PASSWORD por tu contraseña local, nunca la subas a Git.
3. Desde la raíz del proyecto ejecuta:

```bash
docker compose config
docker compose up -d database
docker compose ps
docker compose down
```

Puerto local de PostgreSQL: 127.0.0.1:5433 por defecto. docker compose down conserva el volumen; docker compose down -v **borra los datos locales**.

**Más adelante**, cuando existan clase principal Spring Boot y ai/app/main.py, el equipo podrá probar:

```bash
docker compose --profile app up --build
```

Ese último comando **fallará ahora** porque los módulos todavía no contienen código de aplicación. Android se ejecutará en emulador/teléfono, no en Docker.
