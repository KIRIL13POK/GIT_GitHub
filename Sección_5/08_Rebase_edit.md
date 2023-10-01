# Rebase Edit

La operación edit te permite hacer *cambios en el contenido de un commit* específico durante un rebase interactivo. Aquí tienes algunos puntos clave sobre cómo funciona:

* Seleccionar un Commit para Editar: Cuando realizas un rebase interactivo y llegas a la lista de commits, puedes elegir edit junto al commit que deseas modificar.

* Realizar los Cambios Necesarios: Después de seleccionar edit y guardar el archivo de rebase, Git aplicará el commit que has seleccionado y te llevará al punto en la historia justo antes de ese commit.

* Modificar el Contenido: Aquí, puedes realizar los cambios necesarios en los archivos de tu proyecto para corregir errores, ajustar el código, agregar o eliminar archivos, etc.

* Preparar los Cambios: Una vez que hayas realizado las modificaciones, utiliza los comandos de Git (git add para preparar los cambios y git commit para confirmarlos) para registrar las ediciones que has realizado.

* Continuar con el Rebase: Después de haber registrado los cambios, puedes continuar con el proceso de rebase utilizando git rebase --continue.

* Resultado: Una vez que hayas completado el rebase, el commit que seleccionaste para editar tendrá el contenido modificado según tus cambios.

***
 **Reword se utiliza para cambiar el mensaje de confirmación de un commit sin afectar su contenido, mientras que Edit te permite hacer cambios en el contenido del commit. El resultado final puede ser similar en términos de historial de confirmaciones, pero la diferencia radica en el alcance de los cambios permitidos por cada operación.**

***

* Paso 1. 

3 modificaciones en el proyecto en 3 archivos diferentes:

![git status](/img/508_git-status-paso1.png)

### `git checkout -- readme.md `

Se utiliza para descartar los cambios no confirmados en el archivo readme.md y revertirlo a su estado tal como está en el commit más reciente del área de trabajo o el índice. En otras palabras, este comando deshace las modificaciones locales no confirmadas y restaura el archivo readme.md a su estado previo al cambio.

* Paso 2 

Vamos a consolidar los cambios en los 2 archivos restantes que aún tienen el estado 'M' en un solo commit. Sin embargo, el mensaje de commit actual es demasiado genérico y no proporciona información útil. Esto podría dificultar el seguimiento del historial en el futuro por alguna razón.

![commit](/img/506_commit.png)

* Paso 3.

### `git rebase -i HEAD~4`

Después de ejecutar el comando git  y seleccionar la opción "edit" para el commit que te interesa, el proceso de rebase se pausará en ese commit específico. En este punto, Git te proporcionará instrucciones sobre cómo proceder. Normalmente, verás un mensaje que te indica que estás en medio de un rebase y que puedes realizar cambios en el commit actual.

![stoped-edit](/img/508_stoped-edit.png)
***
`git staus` 

![git](/img/508_git-status2.png)

Este mensaje indica que estás en medio de un proceso de rebase interactivo en Git. En particular, estás editando un commit específico durante este proceso. El rebase interactivo te permite reorganizar y editar commits en la historia de tu rama. En este caso, se te está dando la oportunidad de hacer cambios en el commit actual antes de continuar con el rebase.
***

En resumen, después de seleccionar "edit" en el commit deseado, Git te permitirá realizar modificaciones en ese commit, como cambiar su mensaje o hacer cambios en los archivos. Luego, debes seguir las instrucciones de Git para finalizar el proceso de rebase y aplicar tus cambios.

### `git reset HEAD^`` 

El comando `git reset HEAD^` te permite retroceder en la historia justo antes del commit en el que estabas trabajando, dejando los archivos en el estado en el que tenían sus respectivos cambios sin registrar. Esto te proporciona la oportunidad de hacer commits individuales para cada archivo por separado si así lo deseas, en lugar de consolidar todos los cambios en un solo commit. Esto puede ser útil cuando quieres tener un historial de commits más granular y separado para cada archivo o cuando necesitas revisar y validar los cambios en cada archivo antes de confirmarlos en el repositorio.


