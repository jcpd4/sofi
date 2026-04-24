# Guía Paso a Paso: Cómo Subir y Actualizar tu Página Web

¡Hola Sofía! Esta es una guía sencilla para que puedas subir tu nueva página web a tu dominio, y también te explicamos cómo hacer cambios en el futuro. 

El proyecto web ha sido creado utilizando una herramienta moderna llamada **Vite**. Esto significa que los archivos en los que trabajas se "empaquetan" y se convierten en archivos súper rápidos antes de subirlos.

---

## PARTE 1: Cómo Subir la Web por Primera Vez

### 1. Preparar los archivos finales (El empaquetado)
Actualmente, la página está en una carpeta de desarrollo (llamada `web`). Cuando la web está lista para publicarse, hay que generar la versión "final". Para esto (si no lo han hecho ya por ti):
1. Abre tu terminal o consola y entra en la carpeta `web` de tu proyecto.
2. Asegúrate de tener instalado **Node.js** (es necesario para poder ejecutar los comandos).
3. Escribe e instala las dependencias (solo la primera vez): `npm install`
4. Ejecuta el comando de construcción: `npm run build`
5. ¡Listo! Se habrá creado una nueva carpeta llamada **`dist`** dentro de `/web`. **Los archivos dentro de esta carpeta `dist` son los únicos que debes subir a tu dominio.**

### 2. Acceder a tu Hosting (Donde vive tu dominio)
Tu dominio tiene asociado un servicio de "Alojamiento web" o "Hosting" (como Hostinger, Hostgator, cPanel, DonDominio, etc.).
1. Inicia sesión en la página web de tu proveedor de Hosting.
2. Busca la opción que dice **"Administrador de Archivos"** o **"File Manager"**.

### 3. Subir los Archivos
1. Dentro del Administrador de Archivos, busca la carpeta principal de tu sitio web. Por lo general se llama **`public_html`**, **`www`**, o el nombre de tu dominio.
2. **Elimina** cualquier archivo predeterminado que haya ahí (a veces hay un `default.html` o similar).
3. Sube **todo el contenido** que está *dentro* de la carpeta **`dist`** de tu computadora hacia esa carpeta en el hosting.
   *(Nota: No subas la carpeta `dist` entera como una sola carpeta, sube los archivos y carpetas que están adentro de forma que el archivo `index.html` quede suelto dentro de `public_html`).*
4. ¡Ya está! Entra a tu dominio en el navegador y deberías ver tu web en vivo.

---

## PARTE 2: Cómo Hacer Cambios en el Futuro

Si en unos meses quieres cambiar un texto, una foto o un color de la web, no edites directamente los archivos que subiste al hosting. Siempre debes modificar los archivos originales y luego volver a empaquetar.

**Paso a paso para futuras actualizaciones:**
1. Ve a la carpeta original del proyecto `/web` en tu computadora.
2. Para cambiar fotos, textos, o estilos, busca en los archivos que están en la carpeta **`/web/src/`** (ahí está el diseño y funcionamiento) o el archivo principal **`/web/index.html`**.
3. Realiza los cambios que necesites y guárdalos.
4. Abre tu terminal y, asegurándote de estar dentro de `/web`, ejecuta nuevamente el comando:
   `npm run build`
5. Esto actualizará los archivos de la carpeta **`dist`** con tus nuevos cambios.
6. Ve de nuevo a tu **Administrador de Archivos** en el Hosting, borra los archivos viejos de `public_html` (o sobrescríbelos) y sube los nuevos archivos generados dentro de `dist`.
7. ¡Tus cambios ya estarán en vivo en tu dominio!

*(Tip: A veces tu navegador guarda versiones antiguas de las webs. Si haces un cambio y no lo ves de inmediato, presiona `Ctrl + Shift + R` o `Cmd + Shift + R` en tu teclado para refrescar forzosamente).*
