# Samsung Remote PRO

App Android nativa para controlar Smart TV Samsung/Tizen por Wi‑Fi local.

## Funciones incluidas

- Conexión manual por IP.
- Búsqueda SSDP básica de TVs Samsung/Tizen en la red local.
- WebSocket Samsung Remote API: `ws://IP:8001` y `wss://IP:8002`.
- Emparejamiento: al conectar por primera vez, la TV puede pedir autorización.
- Guardado de token recibido por la TV.
- Botones: Power, Home, Back, Source, Info, Menu, Exit, volumen, mute, canales.
- Navegación: arriba, abajo, izquierda, derecha, OK.
- Touchpad básico: toque = OK, deslizamiento = flechas.
- Multimedia: play, pause, stop, rewind, fast-forward.
- Teclado numérico.
- Envío de texto básico.
- Accesos rápidos a apps por `ed.apps.launch` cuando el modelo lo permita.
- Wake-on-LAN por MAC, si la TV/red lo soporta.
- GitHub Actions para compilar APK online.

## Compatibilidad realista

Samsung no garantiza que todos los modelos acepten todos los comandos. En TVs modernas, normalmente debes aceptar el permiso en pantalla. En algunos modelos, el encendido remoto requiere habilitar `Encender con móvil`, `Wake on LAN/Wi‑Fi` o una opción similar en ajustes de red.

## Cómo compilar online con GitHub

1. Crea un repositorio en GitHub.
2. Sube todo el contenido de esta carpeta, no solo el ZIP.
3. Entra a la pestaña **Actions**.
4. Ejecuta **Build Android APK**.
5. Al terminar, descarga el artifact **SamsungRemotePRO-debug-apk**.

## Cómo compilar en Android Studio

1. Abre Android Studio.
2. File > Open > selecciona la carpeta `SamsungRemotePRO`.
3. Espera a que Gradle sincronice.
4. Build > Build APK(s).
5. El APK estará en `app/build/outputs/apk/debug/`.

## Uso

1. Conecta el celular y la TV a la misma red Wi‑Fi.
2. Abre la app.
3. Pulsa **Buscar** o escribe la IP de la TV.
4. Pulsa **Conectar**.
5. Acepta el permiso en la pantalla de la TV.
6. Usa los botones del control remoto.

## Mejoras recomendadas para versión comercial

- Migrar UI a Kotlin + Jetpack Compose o Material Components.
- Guardar historial de múltiples TVs.
- Detección mDNS/UPnP más profunda.
- Pantalla de onboarding.
- Íconos profesionales.
- Versión release firmada con keystore.
- Módulo SmartThings opcional mediante API oficial y OAuth.
