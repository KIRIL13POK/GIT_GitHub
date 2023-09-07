 ![git](https://git-scm.com/images/logos/1color-darkbg@2x.png)

 La principal diferencia radica en cómo Git registra y sigue los cambios. Usar comandos de Git para renombrar y eliminar archivos te permite tener un registro más preciso de la historia de tu repositorio, lo que facilita el seguimiento de los cambios y la colaboración con otros desarrolladores. Hacerlo a mano puede funcionar, pero puede llevar a confusiones y problemas de seguimiento si no se maneja correctamente.
 ***
 **Por lo tanto, se recomienda utilizar los comandos de Git para estas operaciones siempre que sea posible.**
 ***

 ### Cambia el nombre del archivo

Cambio en la carpeta "historia" : el archivo superman.historia.md renombrado por superman.md

Si cambias el nombre de un archivo manualmente fuera de Git, Git considerará que el archivo original fue eliminado y un archivo nuevo fue creado.Por esta razon podemos observar una "U" de untrack que nos indica que Git no le esta dando seguimiento:

 ![superman renombrado](/img/304_supermanRenombrado.png)

Cuando renombras un archivo manualmente fuera de Git, Git simplemente detectará el archivo original como eliminado y un nuevo archivo:

![superman.md status](/img/304_gitStatusSupermanDeleted.png)

Deberás eliminar el archivo antiguo y agregar el nuevo por separado utilizando `git add`.

Después de ejecutar **'git add'**, Git realiza un análisis de los archivos, y si detecta que dos de ellos son idénticos en contenido, reconoce esta situación como un posible caso de renombrado de un archivo. En tal caso, Git automáticamente cambia el estado de estos archivos al estado **'R'** (de renombrado) en su sistema de seguimiento de cambios, lo que indica que uno de los archivos ha sido renombrado desde su versión anterior:

![ssuperman status renombrado](/img/304_gitStausR.png)

A continuación un commit con sentido

Resultado: 

![lg resltado renombrado](/img/304_lg_Renombrado.png)

También es importante tener en cuenta que podemos retroceder en el tiempo utilizando el hash (identificador) del commit anterior en el que los cambios aún no se habían realizado. Esto nos permite volver a trabajar con el repositorio y los nombres de archivo que existían en el pasado, restaurando así versiones anteriores del proyecto si es necesario.
`git reset hard <hash-del-commit>`


### Eliminar archivos fuera de git.

Eliminamos el archivo batman.historia.md de un repositorio.
Si eliminas un archivo manualmente en tu sistema de archivos sin usar comandos de Git, Git detectará el cambio como una eliminación cuando hagas un seguimiento de los cambios con `git status`.

![ batman deleted](/img/304_batmanDeletedStatus.png)
 
Deberás usar `git add` para marcar la eliminación y luego confirmarla con `git commit`.

![ batman deleted](/img/304_batmaEliminadoCommit.png)


 