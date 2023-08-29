![git](https://git-scm.com/images/logos/1color-darkbg@2x.png)
### `git --version`
El comando `git --version` git --version se utiliza para mostrar la versión actual de Git que está instalada en tu sistema. Al ejecutar este comando en la línea de comandos, obtendrás la información sobre la versión de Git que tienes instalada en ese momento. Esto es útil para verificar qué versión de Git estás utilizando y si necesitas actualizarlo a una versión más reciente.
***
### `git help`
El comando git help se utiliza para acceder a la documentación y ayuda relacionada con los comandos de Git. Puedes usarlo para obtener información detallada sobre un comando de Git específico o para explorar diferentes secciones de la documentación.
***
### `git help commit`
Esto te proporcionará información completa sobre cómo usar el comando git commit, incluyendo su sintaxis, opciones y ejemplos de uso.
***
### `git config --global user.name "name"` 
Este comando establece tu nombre de usuario que se asociará con los commits que realices en tus repositorios Git. El nombre se utiliza para identificar quién realizó un cambio particular en el código. 

### `git config --global user.email "emailo@correo.com"`
 Este comando establece tu dirección de correo electrónico que se asociará con los commits. El correo electrónico es otra parte importante de la identificación del autor de un cambio en el código.

 La opción **--global** en ambos comandos significa que estas configuraciones se aplicarán a todos los repositorios en tu sistema. Si no utilizas la opción **--global**, las configuraciones se aplicarán solo al repositorio actual en el que estás trabajando.

 Estos valores de nombre de usuario y correo electrónico son importantes para que las colaboraciones y la trazabilidad en tus proyectos sean claras y precisas. Cuando realices un commit, estos valores se incluirán en la información del commit, lo que permite a otros colaboradores identificar quién realizó ciertos cambios y comunicarse contigo si es necesario.
 ***

 ### `git config --global -e`

Cuando ejecutas este comando Git abrirá el archivo de configuración global en el editor de texto predeterminado de tu sistema. Este archivo generalmente se encuentra en el directorio de tu perfil de usuario y se llama .gitconfig.

Dentro del archivo, encontrarás secciones que representan diferentes configuraciones, como tu nombre de usuario, dirección de correo electrónico, alias de comandos, entre otros. Puedes realizar cambios directamente en este archivo, guardar los cambios y cerrar el editor. Los cambios se aplicarán a todas tus operaciones de Git en cualquier repositorio en tu sistema.
***