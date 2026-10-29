# Multiherramientas (Flutter)

## Pasos
1. `flutter create --platforms=android,ios .`   (genera android/ e ios/ sin tocar lib/ ni pubspec)
2. En `android/app/src/main/AndroidManifest.xml` agrega dentro de <manifest>:
   `<uses-permission android:name="android.permission.INTERNET"/>`
   y dentro de <manifest> (para abrir enlaces):
   `<queries><intent><action android:name="android.intent.action.VIEW"/><data android:scheme="https"/></intent></queries>`
3. Cambia tu nombre en lib/about_page.dart y el sitio WordPress en lib/wordpress_page.dart. Agrega una foto de caja de herramientas en assets/toolbox.jpg.
4. `flutter pub get`
5. `dart run flutter_launcher_icons`   (icono = tu foto)
6. `flutter build apk --release`  ->  build/app/outputs/flutter-apk/app-release.apk
7. Sube el código: `git init && git add . && git commit -m "app" && git remote add origin <URL> && git push -u origin main`
8. Sube el APK a Releases de GitHub / Drive y genera el QR de ese enlace.

## Estructura (una pantalla por archivo, sin carpetas)
lib/main.dart, home_page.dart (menú), toolbox_page, gender_page, random_user_page,
universities_page, weather_page, pokemon_page, wordpress_page, about_page
