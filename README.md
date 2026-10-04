# rifa

Aplicación para el sorteo anual de la rifa Rett. Sin dependencias, sin servidor y funciona sin conexión.

**Abrir la app:** https://rett-spain.github.io/rifa/

## Instalar

| Dispositivo | Cómo |
|---|---|
| Android (Chrome) | Abre el enlace y pulsa **Instalar app** (o menú ⋮ → *Añadir a pantalla de inicio*). |
| iPhone / iPad (Safari) | Abre el enlace → botón **Compartir** → *Añadir a pantalla de inicio*. |
| Ordenador (Chrome / Edge) | Abre el enlace y pulsa **Instalar app** (o el icono de instalar en la barra de direcciones). |
| Sin internet | Descarga `index.html` y ábrelo con doble clic. |

Una vez abierta, la app queda guardada y funciona sin conexión. Los datos se guardan en el propio dispositivo; usa **Guardar copia** / **Cargar copia** (JSON) para pasarlos a otro.

## Funciones

- Total de tiras y números por tira configurables (por defecto 1.000 × 10).
- Exclusión de tiras no vendidas con números y rangos (`73, 288, 800-805`).
- Sorteo con `crypto.getRandomValues`, sin repetir tiras, con animación de revelado.
- Modo pantalla para proyectar; se puede sortear con Espacio, Enter o un mando de presentaciones.
- En móvil: botón de sorteo siempre visible, pantalla que no se apaga y vibración al sortear.
- Compartir los resultados (WhatsApp, correo…) o copiarlos al portapapeles.

Instrucciones del día del evento en [`LEEME.txt`](LEEME.txt).

## Desarrollo

Todo está en `index.html`. `sw.js` y `manifest.webmanifest` hacen que se pueda instalar y usar sin conexión: **si cambias algún fichero, sube la versión de `CACHE` en `sw.js`**. Al hacer push a `main` se publica en GitHub Pages (`.github/workflows/pages.yml`).

Para probar en local con el modo instalable: `python -m http.server` y abre http://localhost:8000.
