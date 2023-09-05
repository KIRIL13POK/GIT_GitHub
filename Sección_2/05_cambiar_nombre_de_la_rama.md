![git](https://git-scm.com/images/logos/1color-darkbg@2x.png)

En esta sección, exploramos el funcionamiento de las ramas en Git y aprendimos a cambiar el nombre de la rama principal. Las ramas en Git permiten trabajar en diferentes versiones del proyecto de forma paralela, y la rama principal generalmente se llama "master" o "main". Aprendimos a usar el comando `git branch `para verificar en qué rama estamos y cómo cambiar el nombre de la rama con `git branch -m <nombre-nuevo>` .

Además, vimos cómo establecer una configuración global para cambiar el nombre predeterminado de la rama principal en nuevos repositorios mediante `git config --global init.defaultBranch <nombre-nuevo>`. Esta configuración es útil para adoptar el término "main" en lugar de "master" como rama principal.

### `git branch`

![gitBranch](/img/gitBranch.png)

***
#### Rama principal

La rama principal, a menudo llamada **"main" o "master"**, es la base central de un repositorio Git. Contiene el código estable y funcional de un proyecto. Las ramas principales son cruciales para el desarrollo colaborativo, ya que proporcionan una versión estable del proyecto mientras se trabajan nuevas características y correcciones en ramas separadas. La principal se actualiza a través de fusiones de ramas cuando los cambios han sido probados y revisados. Mantener una rama principal limpia y funcional es esencial para asegurar la estabilidad del proyecto.

#### Ramas separadas

El trabajo con ramas en Git facilita el desarrollo paralelo y organizado. Cada rama representa un conjunto de cambios separados, permitiendo desarrollar características, correcciones y experimentos sin afectar la rama principal. Las ramas permiten pruebas, revisiones y desarrollo continuo antes de fusionar los cambios en la rama principal. Además, ofrecen la capacidad de mantener versiones y revertir cambios de manera controlada.

***

### `git branch -m  main`

Esto cambiará el nombre de la rama actual a 'main'. Si la rama principal ya se llama 'main', no se producirá ningún cambio.

### `git config --global init.defaultBranch <name>`

Se utiliza para configurar el nombre de la rama predeterminada que se crea cuando inicializas un nuevo repositorio Git de forma global. En lugar de `<name>`, debes reemplazarlo con el nombre de la rama que deseas establecer como predeterminada.

### `git config --global -e`

Se utiliza para abrir y editar la configuración global de Git en un editor de texto. Cuando ejecutas este comando, Git abrirá el archivo de configuración global en tu editor de texto predeterminado (como Nano o Vim en la terminal) para que puedas realizar cambios en la configuración.

![--global--e](/img/EgLOBAL.png)