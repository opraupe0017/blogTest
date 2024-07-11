---
layout: post
title:  "¡Has tu propio blog usando Markdown, Jekyll y GitHub!"
date:   2024-07-09 22:03:09 -0500
categories: blog markdown jekyll github update
author: Oscar García
---

Crear tu propio blog nunca ha sido tan fácil. Con Markdown, Jekyll y GitHub, puedes configurar y personalizar un blog profesional de manera rápida y sencilla, sin necesidad de conocimientos avanzados de programación y totalmente gratis. ¡Sigue esta guía paso a paso para comenzar hoy mismo!

## Contenidos
{:.no_toc}

* TOC
{:toc}

## Cómo instalar software Ruby+Devkit y Jekyll en Windows 11

### Instalar Ruby+Devkit en Windows 11

En esta sección, las instrucciones para usuarios de Windows difieren de las de los usuarios de Mac. Debes hacer estos pasos únicamente si estás utilizando Windows.

1. Jekyll está basado en el lenguaje de programación Ruby que necesitaremos instalar en tu computadora. Visita [RubyInstaller](https://rubyinstaller.org/downloads/) y descarga la última versión de la instalación de DevKit (la página sugiere el instalador más apropiado para ti, simplemente busca el símbolo `=>` antes de cada enlace).

2. Ejecuta la instalación. Se sugiere que hagas una instalación estándar, pero si decides cambiarla, asegúrate de dejar seleccionada la opción de instalar “`MSYS2 development toolchain`.”

3. Espera a que termine la instalación, pero no la cierres una vez que todos los archivos hayan sido copiados. Antes de cerrar, aparecerá un mensaje preguntándote si quieres ejecutar “`ridk install`”. Deja la opción seleccionada y haz clic en “Finish” (Finalizar).

4. Después de cerrar la instalación, una nueva ventana de la línea de comandos te preguntará qué componentes deseas instalar. Escribe “3” (sin las comillas). Esto instalará “las herramientas de desarrollo MSYS2 y MINGW.” Esto puede tomar un par de minutos y mostrar algunos avisos mientras tanto, pero todo debería estar bien si ves el siguiente mensaje:
   
   `Install MSYS2 and MINGW development toolchain succeeded o Se han instalado con éxito las herramientas de desarrollo MSYS2 y MINGW`

### Intalar Jekyll en Windows 11

[Jekyll](https://jekyllrb.com/) es el código que crea o genera tu página web (por ejemplo, “generación de página), haciendo más fácil las tareas comunes como usar la misma plantilla (mismo logo, menú, información de autor…) en todas las páginas de entradas de blog. Ahora instalaremos Jekyll (si la Seguridad de Windows te muestra un aviso, ignóralo):

1. Sólo basta con ejecutar en una consola de `PowerShell` o `CMD` lo siguiente:

   ```cmd
   >> gem install jekyll bundler
   ```

2. Para asegurarte de que todo va bien, escribe `jekyll -v` en el aviso y presiona “`Intro`”. Debería de devolver la versión de Jekyll que tengas instalada en tu computadora en ese momento.

   Para la fecha en la que estoy escribiendo este post estoy usando actualmente esta versión.

   ```cmd
   >> jekyll -v
   jekyll 4.3.3
   ```

**¡Felicitaciones, hemos terminado de instalar todo lo necesario para crear nuestro sitio web!.**

## Crear tu cuenta en GitHub

### ¿Qué es una cuenta de GitHub?

La cuenta de usuario de GitHub nos permite alojar nuestro sitio web (ponerlo a disposición para que otros lo visiten) de forma gratuita en esa plataforma. Como beneficio adicional, también nos permite llevar un registro de las versiones de nuestro sitio y tu escritura a medida que crece o cambia con el tiempo.

### ¿Cómo crear tu cuenta en GitHub?

1. **Visita [GitHub.com](https://github.com)** y haz clic en el botón verde “Sign up” (Registrarse).

2. **Nombre de usuario:** En la página siguiente, ingresa el nombre de usuario deseado. El nombre de usuario es visible para otros usuarios, nos identifica en GitHub y también es parte de la URL de nuestro sitio. Por ejemplo, si el nombre de usuario de GitHub es `opraupe0017`, la URL del sitio será `http://opraupe0017.github.io/`. (Ten en cuenta que también puedes comprar tu propio nombre de dominio y usarlo para este sitio, pero eso no se tratará en este tutorial). Escribe una dirección de correo electrónico de uso habitual y añade una contraseña que contenga al menos un número y una letra minúscula.

3. **Verificar cuenta:** En el recuadro “Verify your account”, presiona el botón “Verify” (Verificar). Usa las flechas para poner la imagen en el sentido correcto. Finalmente, haz clic en “Select a plan” (Seleccionar un plan).

4. **Cuenta gratuira:** En la página siguiente, haz clic en el botón “Choose Free” (Seleccionar gratis).

5. **Completar configuración:** Baja hasta el final de la siguiente página y haz clic en “Complete Setup” (Completar configuración).

6. **Verificar email:** Ve a tu servicio de email y abre el correo de GitHub (si no aparece en la bandeja de entrada, búscalo en correo no deseado) y haz clic en el botón “Verify email address” (Verificar dirección de email).

7. **Opcional:** puedes visitar [GitHub Profile Settings](https://github.com/settings/profile) para agregar un nombre completo (puede ser tu nombre real, nombre de usuario de GitHub u otra cosa) y más información de perfil público, si lo deseas.

## Crea un proyecto en GitHub para tu blog

### ¿Qué es un proyecto en GitHub?

Un proyecto en GitHub es un repositorio que contiene los archivos y recursos relacionados con un proyecto de software específico. Cada proyecto tiene su propia página en GitHub, donde puedes ver el código, el historial de cambios, las discusiones y otros elementos relacionados con el proyecto.

### ¿Cómo crear un proyecto en GitHub?

1. **Accede a tu cuenta de GitHub:** Una vez que tengas una cuenta, inicia sesión en tu cuenta de GitHub en [https://github.com/](https://github.com/).

2. **Crea un nuevo repositorio:** En la esquina superior derecha de la página, haz clic en el botón "`+`" y selecciona "`Nuevo repositorio`".

3. **Completa los detalles del repositorio:** En la página de creación de repositorios, completa la siguiente información:

    - **Nombre del repositorio:** Introduce un nombre descriptivo para tu proyecto. Este nombre será visible en la URL de tu repositorio. Como ejemplo le daremos el nombre `comoHacerUnBlog`.
    - **El propietario (owner)** que aparece por defecto es tu usuario de GitHub, en este caso es `opraupe0017`.
    - **Descripción del repositorio:** Escribe una breve descripción de tu proyecto. Esta descripción ayudará a otros usuarios a comprender de qué trata tu proyecto. Como ejemplo pondré como descripción `Ejemplo de cómo hacer un blog con Markdown, Jekyll y GitHub`.
    - **Inicializar con un README:** Un archivo `README.md` es un archivo de texto que proporciona información sobre tu proyecto, a su vez se generará una rama llamada `main`. La rama `main` es la rama principal donde usualmente se tiene alojada la versión del proyecto más reciente y estable.
    - **El repositorio debe ser público:** Muy importante. de no ser así el blog no podrá publicarse en la red.

4. **Haz clic en "Crear repositorio":** Una vez que hayas completado la información, haz clic en el botón "Crear repositorio" para crear tu nuevo proyecto en GitHub. Este proyecto lo podrás encontrar en `https://github.com/[tu-usuario-de-github]/[tu-nombre-del-blog].git`.

**¡Felicidades!** Has creado un nuevo proyecto en GitHub. Ahora puedes comenzar a agregar archivos, realizar cambios y colaborar con otros en tu proyecto. **Cuando tu blog finalmente esté desarrollado** esta será la dirección web `https://[tu-usuario-de-github].github.io/[tu-nombre-del-blog]/`. En este ejemplo la dirección es [https://opraupe0017.github.io/comoHacerUnBlog/](https://opraupe0017.github.io/comoHacerUnBlog/).


### Bajar tu proyecto de remoto a local `git clone`

1. Busca una ruta adecuada en tu computador para alojar de manera local tu proyecto.
   <img src="/blogTest/assets/encontrando_un_lugar_github.gif" alt="gif: encontrando un lugar">

2. Ejecuta `git clone` de tu proyecto y ingresas a la carpeta del proyecto `[tu-nombre-del-blog]`:
   ```cmd
   $ git clone https://github.com/[tu-usuario-de-github]/[tu-nombre-del-blog].git
   $ cd [tu-nombre-del-blog]
   ```

A partir de este momento en tu carpeta `[tu-nombre-del-blog]` se encuentra una copia local de la rama `main` del proyecto.

Para nuestro ejemplo este sería el resultado:

```bash
USUARIO@DESKTOP MINGW64 ~/Documents/GitHub
$ git clone https://github.com/opraupe0017/comoHacerUnBlog.git
Cloning into 'comoHacerUnBlog'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.

USUARIO@DESKTOP MINGW64 ~/Documents/GitHub
$ cd comoHacerUnBlog/

USUARIO@DESKTOP MINGW64 ~/Documents/GitHub/comoHacerUnBlog (main)
$
```

## Crea tu nuevo blog con Jekyll

1. **Identifica la carpeta padre** donde está tu proyecto. En el ejemplo que tenemos aquí se llama `~/Documents/GitHub/`. Puedes uase el comando `cd ..`, ejemplo:

   ```cmd
   PS C:\Users\USUARIO\Documents\GitHub\comoHacerUnBlog> cd ..
   PS C:\Users\USUARIO\Documents\GitHub>
   ```

2. **Crea tu sitio web con Jekyll:** En una consola de `PowerShell` o `CMD` de Windows ejecuta `jekyll new [nombre-del-blog] --force`. En nuestro ejemplo quedaría así:

   ```cmd
   >> jekyll new comoHacerUnBlog --force
   ```

### Ejecutar tu blog localmente

Estamos a pocos pasos para lograr ver nuestro blog de forma local en nuestro computador.

### Error en la creación del blog por `wdm (0.1.1)`

Si nos sale este error al ejecutar `jekyll new [nombre-del-blog] --force`.

```cmd
  Bundler: An error occurred while installing wdm (0.1.1), and Bundler cannot continue.
  Bundler:
  Bundler: In Gemfile:
  Bundler: wdm
```

**Encontrar en tu proyecto el archivo** `Gemfile` y comentar (colocar al inicio de la línea el símbolo `#`) la línea gem `"wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]`

### Configura tu blog

#### Edita el archivo `_config.yml`

**Personaliza tu blog** indicando la información del mismo. En el archivo `_config.yml` podemos realizar tal acción. Originalmente aparece esta información:

```yaml
title: Your awesome title
email: your-email@example.com
description: >- # this means to ignore newlines until "baseurl:"
  Write an awesome description for your new site here. You can edit this
  line in _config.yml. It will appear in your document head meta (for
  Google search results) and in your feed.xml site description.
baseurl: "" # the subpath of your site, e.g. /blog
url: "" # the base hostname & protocol for your site, e.g. http://example.com
twitter_username: jekyllrb
github_username:  jekyll
```

En nuestro ejemplo esta será la información:

```yaml
title: Cómo hacer un blog
email: your-email@example.com
description: >- # this means to ignore newlines until "baseurl:"
  Aprende a crear y administrar tu propio blog con esta guía paso a paso. 
  Encuentra consejos sobre configuración, diseño, contenido y mucho más. 
  ¡Comienza a compartir tus ideas con el mundo hoy mismo!
baseurl: "" # the subpath of your site, e.g. /blog
url: "" # the base hostname & protocol for your site, e.g. http://example.com
twitter_username: opraupe0017
github_username:  opraupe0017
```

### Cómo insertar símbolos matemáticos en tu blog

1. **Crear carpeta `_layouts`:** En tu proyecto crea una carpeta llamada `.../[tu-nombre-del-blog]/_layouts/`.

2. **Crea el archivo** `.../[tu-nombre-del-blog]/_layouts/default.html`.

3. **El contenido de `default.html:`** Este debe ser el contenido de `.../[tu-nombre-del-blog]/_layouts/default.html`. 

   ```html
   [... contenido original de default.html ...]

   <script type="text/x-mathjax-config">
     MathJax.Hub.Config({
       tex2jax: {
         inlineMath: [['$','$'], ['\\(','\\)']],
         processEscapes: true
       }
     });
   </script>
   <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.0/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
   ```

### Insertar imágenes en tu blog

**Importante:** No será visible en la prueba local las imágenes, estas se verán en el despliegue.

1. **Crear carpeta `assets`:** En tu proyecto crea una carpeta llamada `.../[tu-nombre-del-blog]/assets/`.

2. **Inserta las imágenes en `assets`:** En esta carpeta y cuando estés haciendo un post puedes mostrar una imagen con este comando dentro de tu post (en Markdown):

   ```markdown
   <img src="/[tu-nombre-del-blog]/assets/mi_imagen.png" alt="gif: mi_imagen">
   ```

### Crea tu primer post

1. **Los post de tu blog en Jekyll son en Markdown**. Debes crear en el directorio `~/[tu-nombre-del-blog]/_posts/` un archivo markdown llamado `20YY-MM-DD-nombre-de-tu-post.markdown` el cual será visible en tu blog si la fecha no es a futuro. Para este ejemplo haremos el post `2024-07-10-post-de-ejemplo.markdown`.

2. **Contenido del post:** Este es un contenido de ejemplo del post:

```markdown
---
layout: post
title:  "Post de ejemplo"
date:   2024-07-10 21:41:13 -0500
categories: markdoown jekyll github update
author: Oscar García
---
Este es un post de ejemplo.

## Teorema de pitágoras

*Dado un triángulo rectángulo* $\triangle ABC$ *con ángulo recto en el punto* $C$ *se cumple que*

$$AB^2 = BC^2 + CA^2.$$

<img src="/comoHacerUnBlog/assets/tma_pitagoras.png" alt="img: teorema pitágoras">

Para más información visitar este [link][Teorema de Pitágoras en Wikipedia]

[Teorema de Pitágoras en Wikipedia]: https://es.wikipedia.org/wiki/Teorema_de_Pitágoras
```

### Personaliza página `About`

En tu blog encontrarás siempre arriba a la derecha el link `About`, este también es personalizable y ahí debes colocar algo acerca de ti y tu blog. Este es el contenido de ejemplo de mi `About`:

```markdown
---
layout: page
title: Acerca de Mí
permalink: /about/
---

¡Hola! Soy Oscar García, un matemático apasionado por la divulgación. En este blog, te guiaré paso a paso en el proceso de crear tu propio blog utilizando Markdown, Jekyll y GitHub. Aprenderás cómo:

* Instalar y configurar Jekyll y GitHub Pages
* Escribir contenido utilizando Markdown, un lenguaje sencillo y eficaz para la creación de contenido web
* Personalizar la apariencia de tu blog para que refleje tu estilo
* ¡Y mucho más!

Mi objetivo es que este blog te ayude a crear tu propio espacio en línea de forma fácil y gratuita, para que puedas compartir tus conocimientos e ideas con el mundo. 

Si tienes alguna pregunta o sugerencia, no dudes en contactarme. ¡Comienza tu aventura en el mundo de los blogs hoy mismo!
```

### Despliegue local (en tu computador)

1. **Para ver el contenido de tu post de forma local** y hacer posibles ajustes, ejecuta este comando:

   ```cmd
   >> bundle exec jekyll serve --watch
   ```

2. **Para acceder a la página local:** En el navegardor de tu preferencia, ingresa a la dirección local [http://127.0.0.1:4000/](http://127.0.0.1:4000/)

### Capturas del blog de ejemplo en local

A continuación comparto algunas capturas del blog de ejemplo `comoHacerUnBlog`:

#### Página principal
<img src="/blogTest/assets/pagina_ppal.png" alt="img: página principal">

#### About
<img src="/blogTest/assets/acerca_de.png" alt="img: acerca de mi">

#### Post de ejemplo
<img src="/blogTest/assets/post_ejm.png" alt="img: post de ejemplo">

**Si hasta este punto nuestro blog funciona bien localmente, sin mostrar imágenes, ¡estamos listos para prepararnos a subir a la web!**

## Hacer ajustes de tu blog local para que funciones en la web

Una vez validas que tu blog funciona de manera adecuada de forma local, salvo las imágenes (estas sólo funcionarán bien en la web), comencemos por hacer los ajustes previos a subir a remoto nuestro proyecto a GitHub.

1. **Encontrar en tu proyecto el archivo** `Gemfile` y descomentar (quitar al inicio de la línea el símbolo `#`) la línea gem `"wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]`

2. **Encontrar el archivo `_config.yml`** para agregar en `baseurl` el valor `[tu-nombre-del-blog]` y en la clave `url` colocar el valor `https://[tu-usuario-de-github].github.io/[tu-nombre-del-blog]`. En mi caso quedaría así:

   ```yml
   baseurl: "/comoHacerUnBlog"
   url: "https://opraupe0017.github.io/comoHacerUnBlog"
   ```

**¡Ahora estamos listos para subir a remoto!**

## Hacer tu blog visible en la red desplegándolo en GitHub

### Subir a remoto de GitHub el blog `git status, add, git commit`

Nuestro proyecto siempre estuvo en la rama main.

1. **Usar `git status`** para ver los cambios que hemos realizado en nuestro proyecto. Como aún no hemos subido nada de nuestro blog al proyecto esto es lo que aparece:

   ```bash
   USUARIO@DESKTOP-K7QQL5C MINGW64 ~/Documents/GitHub/comoHacerUnBlog (main)
   $ git status
   On branch main
   Your branch is up to date with 'origin/main'.

   Untracked files:
     (use "git add <file>..." to include in what will be committed)
           .gitignore
           404.html
           Gemfile
           Gemfile.lock
           _config.yml
           _layouts/
           _posts/
           about.markdown
           assets/
           index.markdown

   nothing added to commit but untracked files present (use "git add" to track)
   ```

2. **Usar `git add .`** para indicar que a todos los directorios y archivos del paso anterior los vamos a almacenar en un solo punto de la historia de nuestro control de versiones en GitHub.

3. **Usar `git commit -m "feat: nuevo blog"`** para indicar el motivo de fijar en la historia de nuestro proyecto de GitHub a todos los archivos y carpetas.

4. **Usar `git push`** para subir a remoto todos nuestro blog.

**¡Listo, ahora nuestro blog está en GitHub!** Pero aún no funciona como un sitio web, en la última sección veremos cómo lo logramos.

## "Hosting" en GitHub Pages

Estamos a nada de que tu blog lo pueda ver el mundo entero, sigue estos últimos pasos y tu blog será publicado en la web.

1. En la página de GitHub pages de tu proyecto encontrarás un desplegable en la sección **branch**. La página concreta debería ser:

   ```url
   https://github.com/[tu-usuario-de-github]/[tu-nombre-del-blog]/settings/pages
   ```

2. En la sección **Build and deployment**
   
   - Source debe estar en modo **Deploy from a btanch**. Esto permite hacer un despliegue desde una rama de tu proyecto de GitHub.

   - Branch debe estar en la rama **main**. Recuerda que todo el desarrollo del blog lo hiciste en la rama **main**.

   - **¡Selecciona la opción Save y listo!**

3. Para ver el proceso de despliegue de tu página web puedes ir a **Actions** para monitorear el estado del despliegue de tu blog sobre GitHub. Cuando todo esté en luz verde podrás acceder a la página. Recuerda que la página de tu blog será `https://[tu-usuario-de-github].github.io/[tu-nombre-del-blog]`.

¡Y esto es todo, ya tienes tu propio blog en línea y gratis!

### Capturas del blog de ejemplo

Para el ejemplo que he realizado en este post, el link del resultado final es este: [https://opraupe0017.github.io/comoHacerUnBlog/](https://opraupe0017.github.io/comoHacerUnBlog/)

Comparto las capturas del blog, nota que la url ya no es local.

#### Página principal
<img src="/blogTest/assets/pagina_ppal_2.png" alt="img: página principal">

#### About
<img src="/blogTest/assets/acerca_de_2.png" alt="img: acerca de mi">

#### Post de ejemplo ¡Ahora si aparece la imagen!
<img src="/blogTest/assets/post_ejm_2.png" alt="img: post de ejemplo">

**Muchas gracias por leer este post**
