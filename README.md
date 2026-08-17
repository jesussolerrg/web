# Web La Sala — prototipo

Prototipo de la home de Viveros y Semilleros La Sala, listo para publicar en GitHub Pages.

**Aviso:** es un prototipo. Los textos siguen pendientes de validación. Las imágenes marcadas con "IMAGEN PROVISIONAL · IA" son de ambientación generada y no representan instalaciones ni partidas concretas: hay que sustituirlas por fotografía propia antes de publicar en el dominio real. Los vídeos del hero sí son grabaciones reales de las instalaciones.

## Qué hay en esta carpeta

```
index.html     La web entera (HTML, CSS y JavaScript en un solo archivo)
fotos/         Las imágenes que usa
videos/        Los 3 vídeos de dron del hero (0,8 MB cada uno) y su fotograma de respaldo
.nojekyll      Archivo vacío. Evita que GitHub procese la web como un blog
README.md      Este documento
```

Peso total: unos 7 MB. Muy por debajo del límite de GitHub Pages (1 GB por repositorio, 100 MB por archivo).

---

## Publicarla la primera vez

No hace falta instalar nada ni usar la terminal.

**1. Crea el repositorio**

En [github.com](https://github.com), botón **+** arriba a la derecha → **New repository**.

- **Repository name:** `la-sala-web`
- Marca **Public** (con cuenta gratuita, Pages solo funciona en repositorios públicos)
- **No** marques "Add a README file"
- **Create repository**

**2. Sube los archivos**

Pulsa el enlace **uploading an existing file** y arrastra **el contenido de esta carpeta**, no la carpeta en sí:

- `index.html`
- la carpeta `fotos`
- la carpeta `videos`
- `.nojekyll`

Abajo escribe `Primera versión` y **Commit changes**.

> Si `.nojekyll` no te deja arrastrarlo porque empieza por punto, no pasa nada: esta web funciona igual sin él.

**3. Activa GitHub Pages**

**Settings** → **Pages**.

- *Source*: **Deploy from a branch**
- *Branch*: **main**, carpeta **/ (root)**
- **Save**

En uno o dos minutos aparece arriba la dirección:

```
https://TU-USUARIO.github.io/la-sala-web/
```

---

## Actualizarla cuando haya cambios

### Sustituir el archivo completo

Cuando recibas un `index.html` nuevo:

1. **Add file** → **Upload files**
2. Arrastra el `index.html` nuevo
3. **Commit changes**

GitHub reemplaza el anterior y guarda el historial, así que siempre se puede volver atrás.

### Retocar textos sin salir del navegador

1. Pulsa sobre `index.html`
2. Icono del lápiz (**Edit this file**)
3. Cambia lo que quieras y **Commit changes**

### Añadir o cambiar fotos

1. Entra en la carpeta `fotos`
2. **Add file** → **Upload files**, arrastra y **Commit changes**

Dos reglas: **nombres sin espacios, sin acentos y sin eñes** (`hero-cosecha-tomate.jpg`, nunca `Hero Cosecha Tomate.jpg`), y **optimizadas antes de subir** (1600–2000 px de ancho, JPEG de calidad 80–85). Si cambias el nombre de un archivo, hay que actualizar la referencia dentro de `index.html`.

### Cambiar los vídeos del hero

Van en `videos/` y se llaman `dron-1.mp4`, `dron-2.mp4` y `dron-3.mp4`. Si los sustituyes, mantén los mismos nombres y no hay que tocar el `index.html`.

Requisitos: **MP4 (H.264), sin pista de audio, unos 5 segundos y por debajo de 1,5 MB**. Un vídeo de dron sin comprimir pesa 12–15 MB y hace la web inservible en móvil. Los actuales están a 1600 px de ancho y calidad CRF 27, que es un buen punto de equilibrio.

`poster-dron.jpg` es el fotograma que se ve mientras el vídeo carga. Si cambias los vídeos, conviene cambiarlo también.

---

## Si algo no se ve

**Las fotos no cargan.** Casi siempre es el nombre: en GitHub Pages `Foto.jpg` y `foto.jpg` son archivos distintos, mientras que en tu Mac son el mismo. Es el fallo más habitual.

**Los vídeos no arrancan.** Es normal en móvil: ahí se muestra a propósito una foto fija para no consumir datos del visitante. También se desactivan si el sistema tiene puesto "reducir movimiento" en accesibilidad. En un ordenador deberían reproducirse solos y en bucle; si no, mira la consola del navegador.

**Sigo viendo la versión antigua.** Caché del navegador: recarga con **Cmd+Shift+R**.

**Sale error 404.** El archivo debe llamarse `index.html` en minúsculas y estar en la raíz del repositorio.

---

## Un par de cosas a tener en cuenta

**Es público.** Cualquiera con el enlace puede verlo y Google puede indexarlo. Mientras sea un prototipo, conviene no difundir la URL. Para bloquear a los buscadores, añade esta línea dentro del `<head>` del `index.html`:

```html
<meta name="robots" content="noindex, nofollow">
```

**Dominio propio.** Para publicarlo en algo como `nueva.viveroslasala.com`: *Settings → Pages → Custom domain*, y requiere un cambio en el DNS.
