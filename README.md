# SimplePhotos Releases

Repositorio público de distribución de APK de SimplePhotos. No contiene código fuente.

Los releases se publican automáticamente desde el CI del repo privado en cuatro canales:

## RELEASE/ (prod)
App de producción, instalable por todos los usuarios.
- `SimplePhotos.apk` — APK firmado (Android).
- `SimplePhotos-linux.tar.gz` — bundle de Linux.
- Se publica automáticamente al pushear a `main` como release normal `vX.Y.Z`.

## RC/
App candidata a release (canal `rc`), versión de prueba que puede instalarse en paralelo a la de producción (otro nombre y paquete).
- `SimplePhotos-rc.apk` — APK firmado (Android).
- `SimplePhotos-rc-linux.tar.gz` — bundle de Linux.
- Se publica como prerelease `vX.Y.Z-rc` desde el repo privado al:
  - pushear a `qa` (automático), o
  - pushear a cualquier rama `rc/*` con `[rc]` en el mensaje del commit, o
  - usar *Actions → Run workflow* sobre una rama `rc/*`.

## BETA/
App de prueba (canal `beta`), versión distinta que puede instalarse en paralelo a la de producción.
- `SimplePhotos-beta.apk` — APK firmado (Android).
- `SimplePhotos-beta-linux.tar.gz` — bundle de Linux.
- Se publica automáticamente al pushear a `develop` como prerelease `vX.Y.Z-beta`.

## ALPHA/
App de desarrollo (canal `alpha`), versión inestable instalable en paralelo.
- `SimplePhotos-alpha.apk` — APK firmado (Android).
- `SimplePhotos-alpha-linux.tar.gz` — bundle de Linux.
- Se publica como prerelease `vX.Y.Z-alpha` desde el repo privado al:
  - pushear a cualquier rama `dev/*` con `[alpha]` en el mensaje del commit, o
  - usar *Actions → Run workflow* sobre una rama `dev/*`.

## Actualización in-app
Cada build solo busca actualizaciones dentro de su propio canal: la app de
producción busca releases estables, y cada build de prueba busca su propio
sufijo (`-rc`, `-beta`, `-alpha`).

## Nota
GitHub no permite "/" en los nombres de assets, así que los canales se distinguen
con el sufijo (`-rc`, `-beta`, `-alpha`) en el nombre del APK y en el tag del release.

## Nota
Instalar un APK descargado requiere permitir "instalar apps de orígenes desconocidos".
