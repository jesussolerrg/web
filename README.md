# Web La Sala — prototipo

Prototipo de la home de Viveros y Semilleros La Sala, listo para publicar en GitHub Pages.

**Aviso:** es un prototipo. Los textos siguen pendientes de validación. Las imágenes marcadas con "IMAGEN PROVISIONAL · IA" son de ambientación generada y no representan instalaciones ni partidas concretas: hay que sustituirlas por fotografía propia antes de publicar en el dominio real. Los tres vídeos de dron de las instalaciones están guardados aparte, fuera de esta carpeta, por si se recuperan más adelante.

## Qué hay en esta carpeta

```
index.html     La web entera (HTML, CSS y JavaScript en un solo archivo)
fotos/         Las imágenes que usa
videos/        El vídeo aéreo del bloque de cierre y su fotograma de respaldo
.nojekyll      Archivo vacío. Evita que GitHub procese la web como un blog
README.md      Este documento
```

Peso total: unos 11 MB, casi todo el vídeo del cierre. Muy por debajo del límite de GitHub Pages (1 GB por repositorio, 100 MB por archivo).

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

---

## Si algo no se ve

**Las fotos no cargan.** Casi siempre es el nombre: en GitHub Pages `Foto.jpg` y `foto.jpg` son archivos distintos, mientras que en tu Mac son el mismo. Es el fallo más habitual.

**Sigo viendo la versión antigua.** Caché del navegador: recarga con **Cmd+Shift+R**.

**Sale error 404.** El archivo debe llamarse `index.html` en minúsculas y estar en la raíz del repositorio.

---

## Un par de cosas a tener en cuenta

**Es público.** Cualquiera con el enlace puede verlo y Google puede indexarlo. Mientras sea un prototipo, conviene no difundir la URL. Para bloquear a los buscadores, añade esta línea dentro del `<head>` del `index.html`:

```html
<meta name="robots" content="noindex, nofollow">
```

**Dominio propio.** Para publicarlo en algo como `nueva.viveroslasala.com`: *Settings → Pages → Custom domain*, y requiere un cambio en el DNS.

### Cambiar el vídeo del cierre

Está en `videos/dron-completo.mp4`. Si lo sustituyes, mantén el nombre y no hay que tocar el `index.html`.

Requisitos: **MP4 (H.264), sin pista de audio y por debajo de 6 MB**. El actual está a 1600 px y calidad CRF 24. No se descarga al abrir la web: solo cuando el visitante llega a esa sección, y se pausa al salir de pantalla.

`poster-completo.jpg` es la imagen que se ve mientras carga y la que queda si el navegador tiene el ahorro de datos activado. Conviene cambiarla si cambias el vídeo.
