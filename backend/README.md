# backend/ — API principal

**Stack:** Spring Boot y Java 21. **Estado:** configuración de Maven y Docker únicamente; no hay clases Java, controladores, servidor ni tests.

| Carpeta | Responsabilidad futura |
| --- | --- |
| src/main/java/pe/sia/prototipo/controller/ | Endpoints REST versionados |
| dto/ | Contratos HTTP y validaciones |
| service/ | Lógica de negocio y flujo de asistencia |
| client/ | Comunicación con ai/ |
| config/ | Seguridad, CORS, errores y perfiles |
| model/ y repository/ | Entidades y acceso a BD solo si son necesarios |
| src/main/resources/ | Configuraciones Spring por entornos |
| src/test/java/ | Pruebas unitarias e integración |

La app móvil no accede a PostgreSQL directamente: usa la API. El Dockerfile de este módulo está preparado, pero la construcción falla hasta que se programe una aplicación principal.

**Primera tarea futura:** Spring Boot mínimo con endpoint de salud, manejo de errores y contrato de entrada/salida. Revisar docs/api-contrato.md.
