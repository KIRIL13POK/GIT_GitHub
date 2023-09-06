![git](https://git-scm.com/images/logos/1color-darkbg@2x.png)

En esta aprendemos trabajar con  comandos que son útiles cuando deseas realizar cambios en la estructura de tu proyecto Git, como cambiar nombres de archivos o directorios, o eliminar elementos, sin perder el historial de versiones y manteniendo un registro de los cambios realizados. También son útiles para mantener una buena organización en tu repositorio y facilitar la colaboración con otros desarrolladores.

1. Primero vamos a crear un archivo nuevo llamado "destruir_mundo.md"

![destruir_mundo](/img/303_destruir_mundo.png)

2. #### `git add ."` y #### `git commit -m "Destruir_mundo.md añadido"` 
 
 ![destruir_mundo](/img/303_destruir_mundoCommit.png)

Para agregar este archivo al seguimiento de Git. 

# Renombrar  Archivos a Través de Git

### `git mv <nombre-de-archivo> <nuevo_nombre>`

Es utilizado para renombrar o mover archivos en un repositorio Git. Permite cambiar el nombre de un archivo o directorio y automáticamente registra este cambio en el índice de Git, lo que significa que Git reconocerá el cambio como una operación de renombrar o mover en lugar de una eliminación y una adición por separado. Esto es útil para mantener un historial de cambios más limpio y coherente al trabajar con archivos que se renombran o se mueven en el proyecto.

![salvar_mundo](/img/303_salvarMundo.png)

Ahora es un archivo "salavar_mundo.md" con una "R" de renamed:

![salvar_mundo](/img/303_salvarMundoR.png)

ya esta en el stage y solo falata `git commit -m "Destruir_mundo.md renombrado a salvar_mundo.md"`

Resultado:

![resultado salvarMundo commit](/img/303_resultadoRenombradoSalvar_mundoCommit.png)

# Borrar Archivos a Través de Git

### `git rm <nombre_del_archivo>`

Se utiliza para eliminar archivos de seguimiento en tu repositorio Git.

Esto elimina el archivo especificado del directorio de trabajo y también lo marca para ser eliminado en el próximo commit.

![rm status](/img/303_rmStatus.png)

 Es decir, después de usar este comando, debes confirmar los cambios con un commit para que la eliminación sea efectiva en el historial del repositorio.

 ![eliminado](/img/303_salvar_mundoEliminado2.png)

 Se puede retroceder en el tiempo a un commit específico y volver al estado del repositorio en ese momento, incluyendo cambios en nombres de archivos. Esto significa que si renombraste un archivo en un commit anterior y luego realizas un reset --hard a ese commit, el archivo volverá a su nombre anterior y el contenido del repositorio se restaurará tal como estaba en ese commit. En este caso volveremos al momento donde el archivo fue renombrado:

 ![salvar mundo recuperado](/img/303_reset--hardSAlvar_mundo.png)














