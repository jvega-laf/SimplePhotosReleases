# SimplePhotos Releases

Repositorio público de distribución de APK de SimplePhotos. No contiene código fuente.

Los releases se publican automáticamente desde el CI del repo privado en dos canales:

## RELEASE/
App de producción (canal `prod`), instalable por todos los usuarios.
- `RELEASE/app.apk` — APK firmado de la versión estable.
- URL de descarga: `https://github.com/jvega-laf/SimplePhotosReleases/releases/download/vX.Y.Z/RELEASE/app.apk`
- Se publica automáticamente al pushear a `main`.

## ALPHA/
App de prueba (canal `alpha`), versión distinta que puede instalarse en paralelo a la de producción (otro nombre y paquete).
- `ALPHA/app.apk` — APK firmado de la versión de prueba (prerelease).
- URL de descarga: `https://github.com/jvega-laf/SimplePhotosReleases/releases/download/vX.Y.Z-alpha/ALPHA/app.apk`
- Se publica manualmente desde el repo privado: *Actions → Run workflow* (rama `develop`).
- La app de prueba no muestra avisos de actualización in-app.

## Nota
Instalar un APK descargado requiere permitir "instalar apps de orígenes desconocidos".
