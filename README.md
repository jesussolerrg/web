# Web La Sala — prototipo

Prototipo de la home de Viveros y Semilleros La Sala, listo para publicar en GitHub Pages.

**Aviso:** es un prototipo. Los textos y las cifras marcadas en ámbar están pendientes de validación y no deben darse por buenos. La foto del hero es una imagen de ambientación generada: no representa las instalaciones ni una partida concreta de La Sala.

## Qué hay en esta carpeta

```
index.html     La web entera (HTML, CSS y JavaScript en un solo archivo)
fotos/         Las 15 imágenes que usa
.nojekyll      Archivo vacío. Evita que GitHub procese la web como un blog
README.md      Este documento
```

---

## Publicarla la primera vez

No hace falta instalar nada ni usar la terminal. Todo desde la web de GitHub.

**1. Crea la cuenta y el repositorio**

Entra en [github.com](https://github.com) y crea una cuenta si no la tienes. Luego pulsa el botón **+** arriba a la derecha → **New repository**.

- **Repository name:** `la-sala-web`
- Marca **Public** (con cuenta gratuita, Pages solo funciona en repositorios públicos)
- **No** marques "Add a README file"
- Pulsa **Create repository**

**2. Sube los archivos**

En la pantalla que aparece, pulsa el enlace **uploading an existing file**.

Arrastra a la ventana del navegador **el contenido de esta carpeta**, no la carpeta en sí:

- el archivo `index.html`
- la carpeta `fotos` entera
- el archivo `.nojekyll`

Abajo escribe `Primera versión` y pulsa **Commit changes**.

> Si `.nojekyll` no te deja arrastrarlo porque empieza por punto, no pasa nada: esta web funciona igual sin él.

**3. Activa GitHub Pages**

En el repositorio, ve a **Settings** (arriba) → **Pages** (menú de la izquierda).

- En *Source* elige **Deploy from a branch**
- En *Branch* elige **main** y la carpeta **/ (root)**
- Pulsa **Save**

Espera entre uno y dos minutos. Refresca la página y arriba aparecerá la dirección:

```
https://TU-USUARIO.github.io/la-sala-web/
```

Esa es la URL que puedes enviar a la agencia o a dirección.

---

## Actualizarla cuando haya cambios

### Cambiar los textos o el diseño

1. En el repositorio, pulsa sobre `index.html`
2. Pulsa el icono del lápiz (**Edit this file**)
3. Haz los cambios
4. Abajo, escribe brevemente qué has cambiado y pulsa **Commit changes**

En un minuto la web pública ya está actualizada.

### Sustituir el archivo completo

Cuando recibas una versión nueva de `index.html`:

1. Pulsa **Add file** → **Upload files**
2. Arrastra el `index.html` nuevo
3. **Commit changes**

GitHub reemplaza el anterior y guarda el historial, así que siempre se puede volver atrás.

### Añadir o cambiar fotos

1. Entra en la carpeta `fotos`
2. **Add file** → **Upload files** y arrastra las imágenes
3. **Commit changes**

Dos reglas con las fotos:

- **Nombres sin espacios, sin acentos y sin eñes.** Usa guiones: `hero-cosecha-tomate.jpg`, nunca `Hero Cosecha Tomate.jpg`
- **Optimizadas antes de subir.** Una foto de móvil pesa 4 MB y hace la web lenta. Redúcela a 1600–2000px de ancho y guárdala como JPEG de calidad 80–85. Como referencia, las de esta carpeta pesan entre 100 y 700 KB

Si cambias el nombre de un archivo, hay que actualizar también la referencia dentro de `index.html`.

---

## Si algo no se ve

**Las fotos no cargan.** Casi siempre es el nombre: comprueba que coincide exactamente, mayúsculas incluidas. En GitHub Pages `Foto.jpg` y `foto.jpg` son archivos distintos, mientras que en tu Mac son el mismo. Ese es el fallo más habitual.

**Sigo viendo la versión antigua.** Es la caché del navegador. Recarga forzando: **Cmd+Shift+R** en Mac.

**Sale error 404.** Revisa que el archivo se llame `index.html` en minúsculas y que esté en la raíz del repositorio, no dentro de otra carpeta.

**La tipografía se ve distinta.** La web carga la fuente Manrope desde Google Fonts, así que necesita conexión. Al publicarla en Pages funciona siempre.

---

## Un par de cosas a tener en cuenta

**Es público.** Cualquiera con el enlace puede verlo, y Google puede indexarlo. Mientras sea un prototipo con datos sin validar, conviene no difundir la URL más allá de quien deba revisarla. Para bloquear a los buscadores, añade esta línea dentro del `<head>` del `index.html`:

```html
<meta name="robots" content="noindex, nofollow">
```

**Dominio propio.** Si más adelante queréis publicarlo en un subdominio como `nueva.viveroslasala.com`, se hace en *Settings → Pages → Custom domain*, y requiere un cambio en el DNS del dominio.
