# Kaeru-Ski (Android)

Proyecto de Android Studio que empaqueta el juego **Kaeru-Ski** dentro de un WebView
(el juego va incluido en `app/src/main/assets/index.html`, no necesita internet para jugar).

Desarrollo por Shikakusan7 y Claude.ia. Musica por Game Guild (Mad Dex 2 y Mad Dex Arena).

## Como obtener el APK

### Opcion A: GitHub (sin instalar nada)
1. Crea un repositorio nuevo en GitHub y sube **todo el contenido de esta carpeta** (incluida la carpeta oculta `.github`).
2. Ve a la pestana **Actions**, elige **Build APK** y pulsa **Run workflow**.
3. Cuando termine (3-6 minutos), abre la ejecucion y descarga el artefacto **Kaeru-Ski-APK** (contiene `Kaeru-Ski.apk`).

### Opcion B: Android Studio
1. Abre Android Studio -> **Open** -> selecciona esta carpeta y espera a que termine la sincronizacion de Gradle.
2. Menu **Build -> Build Bundle(s) / APK(s) -> Build APK(s)**.
3. El archivo queda en `app/build/outputs/apk/debug/app-debug.apk`.

## Instalar en el telefono
Copia el APK al celular, abrelo y acepta **Instalar apps de origen desconocido** cuando Android lo pida.
Este APK esta firmado con la clave de depuracion: sirve para instalar y compartir, pero no para subirlo a Google Play
(para Play Store hay que generar una clave propia y un AAB: Build -> Generate Signed Bundle / APK).

## Notas
* Tipografia: el juego usa la fuente "Press Start 2P" de Google Fonts. La primera vez necesita internet para descargarla
  (despues el WebView la guarda en cache). Sin ella se ve con una fuente alternativa.
* Orientacion vertical, pantalla completa, el boton **Atras** pausa/continua el juego y sale de la app desde el menu.
* El icono esta en `app/src/main/res/mipmap-*` (adaptativo + redondo + monocromo para Android 13). `icono-512.png` es la version para tiendas.
* Para actualizar el juego, reemplaza `app/src/main/assets/index.html`.
