# SIA — Prototipo académico

**Sistema Inteligente de Acompañamiento (SIA)**. Proyecto universitario de una **aplicación móvil** para apoyar a personas mayores o con baja visión durante trámites en entornos bancarios.

> **Estado: estructura y configuración inicial del repositorio.** No se han implementado pantallas, servicios de API, reconocimiento de voz, OCR, YOLO ni navegación. **No apto para guiar desplazamientos en un banco real.**

## Historia que orienta el prototipo

Carlos, un adulto mayor con baja visión, necesita apoyo para realizar una transacción. La experiencia propuesta contempla dos accesos de inicio —«Hablar con SIA» y «Ayúdame a realizar una transacción»— y un recorrido: encontrar una ticketera, reconocer qué botón presionar, identificar un ticket ficticio A32, escuchar la llamada a la ventanilla 6 y recibir indicaciones contextuales. Son **requisitos narrativos por implementar**, no funciones operativas.

## Estructura del monorepositorio

| Directorio | Tecnología propuesta | Responsabilidad |
| --- | --- | --- |
| [mobile/](mobile/) | React Native + Expo + TypeScript | Cliente Android, interfaz accesible, cámara y voz |
| [backend/](backend/) | Java 21 + Spring Boot | API principal, validaciones y coordinación |
| [ai/](ai/) | Python 3.12 + FastAPI | Servicio futuro para OCR/detección con IA |
| [database/](database/) | PostgreSQL + PostGIS | Base de datos y futuros mapas de interiores |
| [docs/](docs/) | Markdown | Arquitectura, alcance y guías del equipo |
| [.github/](.github/) | GitHub Actions | Validación de archivos y plantilla de Pull Request |

No existe un frontend web: **el frontend del producto es la app móvil**, dentro de mobile/.

## Para empezar a colaborar

1. Leer [índice de documentación](docs/README.md), [alcance](docs/alcance.md) y [arquitectura](docs/arquitectura.md).
2. Consultar [herramientas](docs/herramientas.md) y [primeras tareas](docs/primeras-tareas.md).
3. Crear una **rama propia solamente al comenzar cada tarea** y abrir un Pull Request hacia main. Ver [CONTRIBUTING.md](CONTRIBUTING.md).
4. Para usar **solo la base de datos local**, copiar .env.example a .env, cambiar DB_PASSWORD y ejecutar docker compose up -d database.
5. Backend y AI cuentan con Dockerfiles **de preparación**. No arrancan hasta que el equipo implemente sus puntos de entrada. Ver [docs/docker.md](docs/docker.md).

## Reglas

- No subir contraseñas, tokens, información de clientes, imágenes bancarias con personas ni grabaciones sin consentimiento.
- Simulaciones y modelos de IA deben distinguirse explícitamente.
- Revisar licencias de proyectos usados como inspiración; no copiar código sin permiso.
- Licencia del repositorio por definir por el equipo.

**Documentación:** [Docker](docs/docker.md) · [GitHub](docs/github.md) · [API propuesta](docs/api-contrato.md) · [Seguridad](docs/seguridad-accesibilidad.md).
