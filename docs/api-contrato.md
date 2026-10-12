# Contratos de API propuestos (no implementados)

### mobile → backend
Ruta base posible /api/v1. Recursos a consensuar: health, assistance/sessions, assistance/observations, assistance/instructions.

### backend → ai
Recepción autorizada de observaciones visuales y respuesta estructurada que distinga:
- tipo de objeto o texto detectado;
- confianza (si aplica) y resultado no reconocido;
- origen mock o inference;
- advertencia ante incertidumbre y errores controlados.

### Reglas
No afirmar que una detección es una ruta libre. Evitar persistir imágenes por defecto; limitar tamaño y tipo de archivo; verificar permisos. Los endpoints, modelos JSON, autenticación y códigos de error definitivos se definirán con OpenAPI al programarlos.

**Estado:** guía para discutir, no código ni endpoints existentes.
