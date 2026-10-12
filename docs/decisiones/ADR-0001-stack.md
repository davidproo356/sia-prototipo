# ADR-0001 — Stack inicial SIA

**Estado: decisión propuesta, revisable. Fecha: octubre de 2026.**

Los materiales técnicos del proyecto proponen una app móvil, una API y un servicio de visión por computadora. Para organizar los módulos sin mezclar responsabilidades se adopta preliminarmente:

- React Native + Expo + TypeScript en mobile/.
- Spring Boot + Java 21 en backend/.
- Python 3.12 + FastAPI en ai/.
- PostgreSQL + PostGIS en database/, solo si se necesita almacenamiento.
- Docker Compose para backend, IA y base de datos. Android se ejecuta fuera de Docker.

**Ventaja:** responsabilidad por módulos y trabajo paralelo de tres personas. **Costo:** más configuración y tres lenguajes. Flutter + FastAPI se consideró como alternativa; si se cambia, registrar otra ADR y actualizar las carpetas sin sostener dos frontends.

No se afirma que exista implementación funcional.
