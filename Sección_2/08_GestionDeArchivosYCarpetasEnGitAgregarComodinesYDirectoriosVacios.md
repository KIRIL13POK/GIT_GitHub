![git](https://git-scm.com/images/logos/1color-darkbg@2x.png)

En el desarrollo de un proyecto a lo largo del tiempo, es común acumular muchas modificaciones en diversos tipos de archivos, como estilos, HTML, JavaScript, imágenes, etc. Para mantener un flujo de trabajo organizado, es importante agrupar estos cambios en "commits" significativos. Estos "commits" deben reflejar lógicamente las funcionalidades o actualizaciones realizadas, lo que facilita la gestión y revisión del código en el futuro. Es común darse cuenta de la necesidad de dividir grandes cambios en varios "commits" para mantener un historial claro y coherente del proyecto.

# Coomodines - Wildcards 

**Los comodines, o "wildcards"** en inglés, en Git se utilizan para seleccionar múltiples archivos que coincidan con un patrón determinado en un solo comando en lugar de tener que agregarlos uno por uno.
Por ejemplo, para agregar todos los archivos HTML en el directorio actual al área de preparación `git add *.html`.

![git add *.html](/img/gitAddComodines.png)

A continuación haciendo el "commit" ya le estamos dando el seguimiento.

***

Para usar comodines dentro de una carpeta específica del proyecto, como la carpeta llamada "js" que contiene todos los archivos JavaScript `git add js/*.js`

![git add comodin dentro de carpeta js](/img/git_add_ComodinJS.png)

A continuación haciendo el "commit" ya le estamos dando el seguimiento.

# Directorios Vacíos en Git

**Git no rastrea automáticamente directorios vacíos.**

### `.gitkeep`

Para mantener un directorio vacío en el repositorio, se puede agregar un archivo especial llamado `.gitkeep` en ese directorio. Aunque el archivo en sí no tiene contenido significativo, Git lo rastrea y permite mantener la estructura de carpetas.

Para colocarlo en el área de preparación dentro de la carpeta `uploads` el comando es `git add aploads/.gitkeep`
*(Asterisco sobra en este caso)*

![.gitkeep areaDePreparacion](/img/gitkeep.png)

A continuación haciendo el "commit" ya le estamos dando el seguimiento.

***

Para agregar todos los archivos dentro de la carpeta , incluyendo los archivos en subdirectorios y subcarpetas:


Por ejemplo en la carpeta "css" `git add css/`:

![comodinCss](/img/comodinCSS.png)

A continuación haciendo el "commit" ya le estamos dando el seguimiento.

***
Haciendo un `git log` podemos ver todos los commit realizados en esta clase:

![git log](/img/gitLog08.png)

***
