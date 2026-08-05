# SimplePhotos Releases

Repositorio público de distribución de APK de SimplePhotos. No contiene código fuente.

Los releases se publican automáticamente desde el CI del repo privado en dos canales:

## RELEASE/
App de producción (canal `prod`), instalable por todos los usuarios.
- `SimplePhotos.apk` — APK firmado (Android).
- `SimplePhotos-linux.tar.gz` — bundle de Linux.
- Se publica automáticamente al pushear a `main` como release normal `vX.Y.Z`.

## ALPHA/
App de prueba (canal `alpha`), versión distinta que puede instalarse en paralelo a la de producción (otro nombre y paquete).
- `SimplePhotos-alpha.apk` — APK firmado (Android).
- `SimplePhotos-alpha-linux.tar.gz` — bundle de Linux.
- Se publica manualmente desde el repo privado: *Actions → Run workflow* (rama `develop`) como prerelease `vX.Y.Z-alpha`.
- La app de prueba no muestra avisos de actualización in-app.

## Nota
GitHub no permite "/" en los nombres de assets, así que los canales se distinguen
con el sufijo `-alpha` en el nombre del APK (y en el tag del release).

## Nota
Instalar un APK descargado requiere permitir "instalar apps de orígenes desconocidos".
