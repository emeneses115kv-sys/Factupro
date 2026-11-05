---
name: Aplicación Android
description: Resuelve dependencias Gradle, configura y valida una aplicación Android, la ejecuta o genera un artefacto de prueba; prepara distribución de forma segura.
---

Trabaja con el módulo Android de este repositorio. Inspecciona `AGENTS.md`, README, `settings.gradle(.kts)`, los archivos `build.gradle(.kts)`, catálogos de versiones, wrapper y módulos para identificar la estructura y requisitos.

## Preparación y arranque

- Usa `./gradlew` o `gradlew.bat` del repositorio para resolver dependencias y compilar; respeta las versiones fijadas. No instales herramientas globales si ya hay wrapper.
- Comprueba Java/Android SDK disponibles y configura solo lo que el proyecto documenta. No inventes secretos de Firebase, API, firma ni producción; nunca versionas archivos locales con credenciales.
- Ejecuta tareas disponibles como `./gradlew test`, `./gradlew lint` y `./gradlew assembleDebug`. Si hay emulador/dispositivo y se solicita, instala/arranca la variante debug y comprueba el resultado.
- Si faltan SDK, dispositivo, configuración de servicios o secretos, continúa las verificaciones posibles y describe el bloqueo exacto.

## Distribución/despliegue

- Distingue compilar un APK/AAB de publicarlo. Genera artefactos de debug o release solo según lo pedido y la configuración del proyecto.
- No firmes con claves de producción, publiques a Play Store, distribuyas APK ni alteres servicios remotos sin indicación y confirmación explícitas. No compartas ni registres contraseñas o claves de firma.
- Si se pide preparar una distribución, valida build y documenta los secretos/permisos que la persona debe configurar, sin incluir valores reales.

## Informe

Indica módulos/plataforma detectados, tareas Gradle ejecutadas, resultado, ruta del artefacto si existe y requisitos manuales pendientes. No afirmes que se instaló o ejecutó en un dispositivo si no se verificó.
