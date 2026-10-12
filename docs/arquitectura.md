# Arquitectura inicial propuesta

SIA es una **aplicación móvil Android**, no un sitio web.

```text
mobile/ (React Native + Expo + TypeScript)    [PENDIENTE]
                     |
                  JSON/HTTP
                     v
backend/ (Java 21 + Spring Boot)              [PENDIENTE]
             |                    |
             v                    v
ai/ (Python + FastAPI)       database/ (PostgreSQL + PostGIS)
futuros YOLO y OCR           mapas y datos futuros
[PENDIENTE]                  [contenedor preparado]
```

### Responsabilidades
- mobile/: UI, accesibilidad, permisos, cámara, lectura de voz y reproducción de instrucciones.
- backend/: API, validación y coordinación de lógica, BD e IA.
- ai/: futura inferencia visual, OCR, clasificación de confianza y errores.
- database/: datos estructurados mínimos y mapas de interiores ficticios, solo cuando se necesiten.

El móvil nunca debe conectarse directamente a la BD. La inferencia de IA no implica que un trayecto esté libre o sea seguro.

### Estado hoy
Solo hay carpetas, guías y configuraciones. Los Dockerfile de backend y ai son **preparaciones**, no servicios operativos. Véase [ADR del stack](decisiones/ADR-0001-stack.md).

### Contratos futuros
Las rutas, respuestas y errores se acordarán antes de desarrollar los servicios: [api-contrato.md](api-contrato.md).
