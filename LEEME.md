# App "Horas" — cómo obtener el APK

## Opción A: GitHub (sin instalar nada)
1. Creá un repositorio nuevo en github.com (puede ser privado).
2. Subí TODO el contenido de esta carpeta (incluida la carpeta oculta `.github`).
   Lo más fácil: desde la compu, con git:
       git init && git add . && git commit -m "app horas"
       git branch -M main
       git remote add origin https://github.com/TU_USUARIO/TU_REPO.git
       git push -u origin main
3. Entrá a la pestaña **Actions** del repo → "Compilar APK" → esperá ~3 min.
4. Abrí la ejecución terminada y bajá el artefacto **HorasTrabajo-apk** (es un .zip con el .apk adentro).

## Opción B: Android Studio
1. File → Open → elegí esta carpeta. Esperá que sincronice Gradle.
2. Build → Build App Bundle(s) / APK(s) → Build APK(s).
3. El APK queda en `app/build/outputs/apk/`.

## Instalar en el celular
Pasá el .apk al teléfono, abrilo y aceptá "Instalar apps de origen desconocido".

## Notas
- Funciona 100 % sin internet. Los registros se guardan dentro del teléfono.
- Si desinstalás la app se borran: usá "Guardar respaldo" de vez en cuando.
- La app se firma siempre con `app/horas.keystore`, así podés instalar versiones nuevas encima sin perder datos.
- Para cambiar la interfaz, editá `app/src/main/assets/index.html`.
