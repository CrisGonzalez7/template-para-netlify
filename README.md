# Netlify + Angular
![netlify + angular logo](https://res.cloudinary.com/dzkoxrsdj/image/upload/v1646339469/angular_wzrs5o.png)

Este es un proyecto angular básico que contiene todo lo necesario para implementarlo directamente en [Netlify](https://netlify.com). 

Para inicializarlo haz clic en el siguiente botón, presionando la tecla `Ctrl`:

[![Deploy to Netlify Button](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/veronica-gonzalez/plantilla-netlify-angular)

Esto te llevará a una pestaña que dice: `Welcome to Netlify! Get your site in 1 min.`

- Presiona el botón que dice `Connect to GitHub`
- Luego en `Configure your site`, aparece un campo que dice `Repository name`. Escribe aquí el nombre de tu proyecto.
- Haz clic en `Save & Deploy`

Esto te crea automáticamente un repositorio en GitHub con el nombre de tu proyecto y te crea un sitio en Netlify linkeado a ese repositorio. 

## Índice:

- [Trabajando en el Proyecto](#trabajando-en-el-proyecto)
  - [Cambiar nombre al proyecto](#cambiar-nombre-al-proyecto)
  - [Subir los cambios](#subir-los-cambios)
- [Trabajando con GitHub](#trabajando-con-github)
  - [Mezclando con Main](#mezclando-con-main)
- [Configurando Netlify con GitHub](#configurando-netlify-con-github)
- [Agradecimientos](#agradecimientos)


## Trabajando en el Proyecto

Para poder empezar a trabajar en tu proyecto de Angular, lo primero que debes hacer es clonar el repositorio de GitHub en tu computador.

Para clonar tu repositorio y realizar modificaciones desde tu PC, sigue los siguientes pasos:
- Ve al sitio de administrador en Netlify del sitio web que haz creado.
- Ve a la sección `Deploys` en el menú superior.
- En `Deploys for [NOMBRE]` sale el link de tu sitio y debajo dice `Deploys from [REPOSITORIO]`. 
- Haz clic en el link del repositorio.
- Una vez en la página de tu repositorio, haz clic en `Code` y copia el link que aparece en `HTTPS`

En tu computador: 
- Crea una carpeta donde almacenarás el proyecto
- Abre la carpeta en [Visual Studio Code](https://code.visualstudio.com)
- Ve al menú superior de Visual Studio Code y abre un terminal

- Ejecuta el siguiente comando 

```bash
git clone [PEGA AQUÍ EL LINK DE TU REPOSITORIO] 
```

- Luego, entra a la carpeta del proyecto con el comando:

```bash
cd [NOMBRE CARPETA]
```
> El nombre de la carpeta es el mismo nombre que pusiste en el repositorio. 

Para instalar los paquetes necesarios ejecuta el siguiente comando:

```bash
npm install
```

Para verificar que esté todo funcionando de manera correcta, puedes levantar un servidor local con el comando:

```bash
ng serve
```

> Si te lanza el siguiente mensaje `? Port 4200 is already in use. Would you like to use a different port?` pon la letra `Y` y presiona `enter`
Si todo salió correctamente, te debería lanzar el siguiente mensaje `** Angular Live Development Server is listening on localhost:[NUMERO], open your browser on http://localhost:[NUMERO]/ **`

<br>
Puedes ingresar directamente al link haciendo clic con la tecla `Ctrl` presionada. 

> Para dejar de ejecutar el servidor presiona `Ctrl` + `C` en la terminal de Visual Studio Code. 

### Cambiar nombre al proyecto

En este momento tu proyecto tiene el nombre `angular-quickstart` por defecto. 

Para ponerle un nombre personalizado, en VSCode presiona `Ctrl` + `Shift` + `F`, esto debería abrirte el buscador

> Si no te funciona, puedes ir directamente a la lupa en el panel izquierdo y esto te abrirá el buscador.
Busca: 

```bash
angular-quickstart
```

Deberían aparecer `22 resultados en 9 archivos`

- En la parte izquierda del buscador aparece una flecha `>`, haz clic ahí y te aparecerá un campo que dice `Reemplazar`. 
- Pon el nombre de tu proyecto en ese campo.
- En la parte derecha del campo, hay un botón que al poner el cursor sobre él dice `Reemplazar todo`
- Haz clic en `Reemplazar todo` y te aparecerá un mensaje que dice `Reemplazar 22 apariciones en 9 archivos por "[NOMBRE INGRESADO]"`
- Haz clic en `Reemplazar`

Para verificar que los cambios se guardaron correctamente `Ctrl` + `Shift` + `G`, esto debería abrirte el panel de Git.

> Si no te funciona, puedes ir directamente a la opción bajo la lupa en el panel izquierdo, la cual se llama `Control de código fuente`.
Y debería aparecer un listado con 9 archivos que han sufrido modificaciones. 

### Subir los cambios

Vamos a actualizar los archivos en GitHub para que contengan el nuevo nombre del proyecto. Para esto vamos a verificar que esté bien linkeado nuestro proyecto con el repositorio de GitHub.

- Ejecuta el siguiente comando: 

```bash
git remote -v
```

Esto debería darte como resultado el link de tu repositorio. 

- Para ver los archivos que han sido modificados ejecuta: 

```bash
git status
```

- Para poder subir los cambios a GitHub ejecuta: 

```bash
git add .
git commit -m "[DESCRIPCION DEL COMMIT]"
```

- Y luego: 

```bash
git push -u origin main
```

> Si deseas verificar que los cambios fueron subidos correctamente, ingresa al link de tu repositorio y debería aparecer el nombre del commit que haz realizado.
¡Ya puedes empezar a trabajar en tu proyecto!

## Trabajando con GitHub 

Te recomiendo trabajar en una rama aparte de `main`.

- Para crear una rama ejecuta: 

```bash
git branch [NOMBRE DE LA RAMA]
```

> Generalmente en mis proyectos personales creo una rama llamada `rama` y así no me complico la vida ;)

- Para cambiar a la rama creada ejecuta:

```bash
git checkout [NOMBRE DE LA RAMA]
```

Haz los cambios que desees en tu proyecto.

Para ver los archivos que han sido modificados ejecuta: 

```bash
git status
```

Para poder subir los cambios a GitHub ejecuta: 

```bash
git add .
git commit -m "[DESCRIPCION DEL COMMIT]"
```

Y luego: 

```bash
git push -u origin [NOMBRE DE LA RAMA]
```

### Mezclando con Main 

Para mezclar la rama creada con la rama main (que es la principal), debes ir al link de tu repositorio en [GitHub](https://github.com/)

> Si lo olvidaste el link de tu repositorio puedes acceder a él con el comando `git remote -v`
- Una vez en GitHub, es probable que te aparezca un mensaje como este ` [NOMBRE DE LA RAMA] had recent pushes [TIEMPO] ago`, y al lado un botón que diga `Compare & pull request`

> Si no te sale ese mensaje puedes hacer clic en `main` luego ir a la rama en cuestión y en `contribute` hacer clic en `Open Pull Request`
En Write puedes escribir una descripción de tu proyecto (si quieres) y presionar `Create pull request`

Luego, si te dice `This branch has no conflicts with the base branch` significa que está todo correcto y al hacer clic en `Merge pull request` y luego en `Confirm merge` los cambios serán enviados a la rama `main`

Puedes ir a la pestaña `Code` para ver los cambios

## Configurando Netlify con GitHub

En este momento tu proyecto en Netlify está linkeado con tu repositorio en GitHub. Para comprobar esto ejecuta: 

```bash
netlify open
```

Esto te abrirá una pestaña en el navegador con la página de administración de tu sitio. 

- Debajo del link de tu web haz clic en `GitHub`, esto te abrirá el repositorio al cual está linkeado.

Por último, haz clic en el link de tu sitio para verificar que se haya desplegado de forma correcta.

Desde este momento, cada vez que actualices la rama `Main`, los cambios se verán reflejados en Netifly de forma automática. 

## Agradecimientos

Si este tutorial fue de ayuda para ti, te invito a que me agradezcas dándome una estrella en el [Proyecto Original](https://github.com/veronica-gonzalez/plantilla-netlify-angular), compartiendo este tutorial en tus Redes Sociales, o directamente con tus amigos, y [comentando](https://github.com/veronica-gonzalez/template-para-netlify/issues/new) en caso de algún error o problema que hayas tenido. 
