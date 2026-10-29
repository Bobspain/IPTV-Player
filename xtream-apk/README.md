# Reproductor Xtream (APK para Android TV Box y móvil)

Reproductor para servicios Xtream Codes (TV en directo, películas y series), empaquetado como app Android con Capacitor.
Está adaptado para Android TV / TV Box: se maneja con el mando a distancia y aparece en el launcher de TV.

## Cómo obtener el APK

1. Crea un repositorio nuevo en GitHub (puede ser privado).
2. Sube todo el contenido de esta carpeta (incluida `.github/workflows`).
3. Ve a la pestaña **Actions** -> **Compilar APK**. Se ejecuta solo al subir los archivos; si no, pulsa **Run workflow**.
4. Cuando termine (unos 5-8 minutos), entra en la ejecución y descarga `reproductor-xtream-apk` desde **Artifacts**. Dentro está `app-debug.apk`.

## Instalar en el TV Box

- Opción USB: copia el APK a un pendrive, conéctalo al TV Box y ábrelo con un explorador de archivos.
- Opción red: sube el APK a tu nube y descárgalo con la app "Downloader" (o similar) del TV Box.
- Hay que permitir "instalar apps de orígenes desconocidos" para esa app.

## Manejo con el mando

- Cruceta: moverte por categorías, lista y pestañas. OK/Enter: seleccionar.
- Al reproducir, se abre en pantalla completa.
  - Arriba / Abajo: canal anterior / siguiente (TV en directo).
  - Izquierda / Derecha: retroceder / adelantar 10 s (películas y series).
  - OK: pausa / reanudar.
  - Atrás: salir de la pantalla completa; Atrás otra vez sale de la app.

## Notas

- Las llamadas a la API se hacen con HTTP nativo: sin problemas de CORS y con servidores `http://`.
- El vídeo usa el reproductor del WebView de Android. HLS (.m3u8) es el formato recomendado; el MPEG-TS puro (.ts) puede no funcionar.
- En TV Box muy antiguos, el WebView puede estar desactualizado y fallar. Si no tienes Play Store, prueba a actualizar "Android System WebView".
- El APK es de depuración (firmado con la clave debug): sirve para instalar, no para publicar en Google Play.
