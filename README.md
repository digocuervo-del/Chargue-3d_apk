# CHARGE 3D — proyecto Android inicial

Proyecto Android nativo (Kotlin) con selección aleatoria de 3 escenas al conectar la alimentación, lectura del porcentaje real de batería, vista superpuesta, pantalla negra al completar y cierre al desconectar.

## Generar el APK con GitHub Actions

1. Creá un repositorio vacío en GitHub.
2. Subí el contenido de esta carpeta a la rama `main`.
3. Abrí la pestaña **Actions** y ejecutá **Build CHARGE 3D APK** (o esperá al build automático al subir a `main`).
4. En la ejecución, descargá el artefacto `CHARGE_3D_APK`. El APK está dentro como `app-debug.apk`.

## Instalar y configurar

1. Instalá el APK y abrí CHARGE 3D una vez.
2. Tocá **CONCEDER PERMISO DE PANTALLA** y habilitá “Mostrar sobre otras aplicaciones”.
3. Volvé a la app y tocá **PROBAR ANIMACIÓN** para verificar.
4. Conectá el cargador: se elige una escena aleatoria. Al desconectarlo, se cierra.
5. Durante la animación, dos toques en la pantalla la cierran manualmente.

## Estado y límites de esta entrega

Esta es una **base funcional de desarrollo**, no una versión final certificada. Las escenas se dibujan en tiempo real con Canvas (ilustración animada estilizada), no son modelos 3D fotorrealistas ni video cinematográfico. El comportamiento de inicio automático desde un receptor de energía puede variar según las restricciones de batería y software de Samsung/Motorola; por eso se requiere conceder el permiso de superposición y probar en el dispositivo. El permiso de notificaciones puede depender de la versión de Android. No se fuerza el desbloqueo ni se garantiza mantener la pantalla encendida si el fabricante bloquea el wake lock.

## Requisitos

- Android Studio reciente / JDK 17
- Gradle 8.11.1
- Android SDK 35
- minSdk 26 (Android 8.0)
