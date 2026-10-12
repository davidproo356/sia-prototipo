# ai/ — Servicio de visión por computadora

**Stack:** Python 3.12 y FastAPI. **Estado:** directorios, dependencias y Dockerfile preparados; no existe FastAPI ni código YOLO/OCR, ni modelos descargados o entrenados.

| Carpeta | Qué desarrollar |
| --- | --- |
| app/api/ | Endpoints HTTP para observaciones visuales |
| app/schemas/ | Esquemas JSON de resultados, confianza y fallos |
| app/services/ | Lógica de coordinación |
| app/inference/ | Adaptadores YOLO y OCR futuros |
| tests/ | Pruebas de contrato y de casos adversos |
| models/ | Documentación de pesos; modelos binarios excluidos de Git |
| datasets/ | Documentación y licencias de datasets; datos excluidos de Git |

No inferir distancias seguras solo por reconocer objetos. Diseñar estados de no reconocimiento e informar límites de precisión.

**Primera tarea futura:** un servidor FastAPI con health check y respuesta mock claramente identificada como simulación. No implementado. Revisar docs/api-contrato.md.
