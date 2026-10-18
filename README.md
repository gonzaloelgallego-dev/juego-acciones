# Juego de acciones

App web instalable (PWA) para aprender a reconocer acciones: se ve un vídeo y se toca la palabra correcta.

- `app.html`: toda la app (HTML, CSS y JS en un solo archivo). Es lo que se publica como vista previa.
- `index.html`: se genera con `sh build.sh` a partir de `app.html`, añadiendo el manifiesto y el service worker para instalarla.
- `manifest.webmanifest`, `sw.js`, `icon.svg`: piezas de la PWA.

Los vídeos se guardan en el propio dispositivo (IndexedDB, base `juego-acciones`, almacenes `meta` y `files`). Nada sale del móvil.

Para servirla como app instalable con funcionamiento sin conexión, basta con subir `index.html`, `manifest.webmanifest`, `sw.js` e `icon.svg` a cualquier hosting estático con HTTPS (por ejemplo GitHub Pages).
