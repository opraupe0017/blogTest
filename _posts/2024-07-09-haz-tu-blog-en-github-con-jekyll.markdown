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

## Crea tu nuevo blog con Jekyll

### Ejecutar tu blog localmente

### Insertar imágenes en tu blog

### Insertar símbolos matemáticos en tu blog

### Crea tu primer post

## Hacer tu blog visible en la red desplegándolo en GitHub

### Guardar progreso del blog en Git local `git add, git commit, git pull`

### Guardar progreso del blog en Git Remoto `git push`

### “Hosting” en GitHub Pages
