# mobile/ — Aplicación Android

**Tecnologías propuestas:** React Native, Expo y TypeScript. **Estado actual: no hay pantallas implementadas ni archivo de entrada.** package.json y app.json preparan el módulo; npm run start no podrá iniciar la app hasta que se cree su punto de entrada.

| Carpeta | Qué desarrollará el compañero |
| --- | --- |
| src/screens/ | Inicio, ticketera, lectura de ticket, espera y ventanilla |
| src/components/ | Botones grandes, mensajes y controles accesibles |
| src/navigation/ | Flujo entre pantallas |
| src/services/ | Comunicación con API y futuros adaptadores de voz/cámara |
| src/accessibility/ | Contraste, TalkBack, mensajes por voz y alternativas a micrófono |
| src/types/ | Interfaces de datos |
| src/hooks/ | Lógica compartida de React |
| assets/ | Imágenes y recursos propios autorizados |
| __tests__/ | Pruebas de interacción y accesibilidad |

## Preparación
Se requieren Node.js, npm, Expo, Android SDK y un emulador o teléfono. Verificar compatibilidad de las dependencias antes del primer npm install y añadir un package-lock.json en la primera implementación.

Copiar .env.example a .env y editar EXPO_PUBLIC_API_BASE_URL. **Nunca usar EXPO_PUBLIC_ para secretos**.

**Primera tarea futura:** crear el punto de entrada, la pantalla inicial y dos opciones: «Hablar con SIA» y «Ayúdame a realizar una transacción». No implementado.
