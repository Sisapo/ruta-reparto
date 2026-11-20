# Ruta de reparto · versión de prueba 0.6.0-beta

App web instalable (PWA) para repartidores. Sirve para:

- escanear la etiqueta del paquete y leer el código de envío y la dirección (solo la calle, nunca el nombre),
- juntar los bultos que van a la misma dirección,
- elegir la oficina de Correos de salida y vuelta,
- encajar las oficinas rurales con horario (por ejemplo, Puerto Lápice de 10:00 a 10:30),
- ordenar la ruta y abrirla en Google Maps por tramos.

Todo se guarda solo en el móvil de cada persona. No hay servidor ni cuentas.

## Contenido de la carpeta

| Fichero | Para qué sirve |
|---|---|
| `index.html` | La app completa |
| `manifest.webmanifest` | Permite instalarla en el móvil como una app |
| `sw.js` | Hace que funcione sin cobertura una vez abierta |
| `icons/` | Iconos de la app |
| `datos/ruta-demo.csv` | Ruta de ejemplo con datos ficticios |
| `GUIA-PRUEBAS.md` | Lo que tienen que probar los compañeros |
| `.nojekyll` | Necesario para GitHub Pages |

## Publicarla para los compañeros (GitHub Pages, gratis)

La cámara, el GPS y la instalación solo funcionan si la app se abre desde una dirección **https**. GitHub Pages la da gratis.

1. Crea una cuenta en github.com si no la tienes.
2. Crea un repositorio nuevo, por ejemplo `ruta-reparto`. Puede ser público o privado. Con un plan gratuito, GitHub Pages solo funciona en repositorios públicos. La app no lleva datos personales, así que puede ser público.
3. En el repositorio, pulsa **Add file → Upload files** y arrastra **todo el contenido** de esta carpeta (incluido `.nojekyll` y las carpetas `icons` y `datos`).
4. Ve a **Settings → Pages**. En *Source* elige **Deploy from a branch**, rama `main`, carpeta `/ (root)` y guarda.
5. En uno o dos minutos tendrás la dirección: `https://TU-USUARIO.github.io/ruta-reparto/`. Esa es la que compartes.

Para publicar una versión nueva, sube los ficheros cambiados y cambia el número de `VERSION` en `sw.js`. Así los móviles se actualizan solos.

## Instalarla en el móvil

- **Android (Chrome):** abre la dirección, pulsa **Instalar en el móvil** (o menú ⋮ → *Añadir a pantalla de inicio*).
- **iPhone (Safari):** botón Compartir → *Añadir a pantalla de inicio*.

La primera vez pulsa **Oficina y ajustes → Dar permisos de cámara y GPS**.

## Clave de Google Maps (opcional)

Sin clave, la app localiza las direcciones con OpenStreetMap y abre las rutas en Google Maps con enlaces normales, sin coste.

Con clave, la localización de direcciones es más precisa:

1. Crea un proyecto en Google Cloud Console y activa la facturación.
2. Activa **Maps JavaScript API** y **Geocoding API**.
3. Crea una clave y restríngela:
   - *Restricción de API:* solo esas dos APIs.
   - *Restricción de aplicación:* sitios web, con tu dirección de GitHub Pages (`https://TU-USUARIO.github.io/*`).
4. Pon un presupuesto con alerta en la facturación.
5. Cada compañero pega la clave en **Oficina y ajustes** y pulsa **Probar clave**.

## Privacidad

- La app solo guarda el **código de envío** y la **dirección de entrega**. No lee ni guarda nombres de destinatarios.
- Los datos no salen del móvil, salvo la dirección que se consulta al servicio de mapas para situarla.
- Para las pruebas usad la **ruta de ejemplo** (datos ficticios). Si probáis con paquetes reales, borrad la ruta al terminar (**Vaciar ruta**).

## Limitaciones conocidas

- Las horas de llegada son estimadas: se calculan con la distancia en línea recta, un margen para las curvas y la velocidad media que pongas.
- La lectura de la etiqueta acierta la calle en buena parte de las fotos nítidas; las movidas o muy inclinadas hay que corregirlas a mano.
- Google Maps admite 9 paradas intermedias por enlace en la app y 3 si se abre en el navegador del móvil; por eso la ruta se parte en tramos.
