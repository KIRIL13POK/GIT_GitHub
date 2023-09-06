![git](https://git-scm.com/images/logos/1color-darkbg@2x.png)

La clase subraya la importancia de mantener un historial de versiones limpio y organizado en un repositorio Git, así como la necesidad de comprender los comandos antes de usarlos, especialmente aquellos que pueden tener un impacto destructivo en el proyecto. También la práctica  de trabajar con ramas para evitar problemas con el historial principal del repositorio.

****
***El uso de ramas en Git es una práctica común en el desarrollo de software. Las ramas permiten a los desarrolladores trabajar en nuevas funcionalidades o correcciones de errores de forma aislada, sin afectar el historial principal del repositorio. En Git, la rama principal suele denominarse "main" o "master".***

***La importancia de trabajar con ramas radica en mantener un historial de versiones limpio y organizado. Al utilizar ramas, los cambios y experimentos pueden realizarse en un entorno separado, lo que facilita la colaboración en equipo y la gestión de proyectos más grandes. Cuando una funcionalidad está completa y probada, se fusiona con la rama principal, asegurando que solo los cambios confirmados y estables se reflejen en el historial principal.***

***A pesar de estas prácticas, a veces es necesario retroceder en el tiempo para deshacer cambios, ya sea debido a errores o para corregir fusiones incorrectas. Git proporciona comandos como "git reset" para realizar estas operaciones de manera controlada y recuperar el estado deseado del repositorio. Esto es fundamental para mantener la integridad del historial y asegurarse de que el repositorio refleje el estado correcto del proyecto***

***

# Revertir Cambios y Navegar en la Historia

Para esta clase, hemos preparado un repositorio en el cual Git ya está realizando un seguimiento y que ya cuenta con un historial de "commits" que vamos a modificar y mejorar a lo largo de la lección:

![repositorio](/img/302_repositorioParaTrabajar.png)

* Paso 1.

La última modificación en el archivo "heroes.md" incluyó la adición de Robin, y debemos actualizar el comentario para reflejar este cambio.

### `git reset --soft <hash-del-commit>`

El comando `git reset --soft ` permite retroceder el historial de confirmaciones (commits) de Git al punto específico identificado por el hash.
![el hash](/img/302_hashDelCommit.png)

*Este comando puede ser útil si deseas reorganizar o ajustar tu historial de commits sin perder los cambios realizados en esos commits posteriores. Después de ejecutar este comando, puedes realizar nuevos commits para incorporar estos cambios de manera organizada en tu historial.*

 A continuación  `git commit -am " "` para dejar el commit con Robin mencionado: 

 ![resultado resfr--soft](/img/302_resultadoResft--soft.png)

 * Paso 2.

 Sin embargo, a veces surge la necesidad de retroceder en el tiempo en nuestro repositorio Git, regresando a un punto anterior en el que nuestro proyecto estaba en buen estado. Imaginemos que todo estaba funcionando correctamente antes de realizar el commit de 'ciudades' y despues todo empezo a salir mal.

 ### `git reset --mixed <hash-del-commit>`

  se utiliza para retroceder el historial de cambios de Git a un commit específico, pero  no eliminará permanentemente los cambios en el directorio de trabajo ni en el área de preparación (staging). En cambio, los cambios realizados después del commit al que te estás moviendo se desharán en la rama actual, pero esos cambios se mantendrán en tu directorio de trabajo sin preparar.

  ![reset --mixed](/img/302_reset--mixed.png)

  Resultado :

  ![commit reset --mixed](/img/302_reset--mixedCommit.png)

  * Paso 3.

Pero todo las modificaciones aun siguen existiendo:

### `git reset --hard <hash-del-commit>`

Se utiliza para retroceder el historial de cambios de Git a un commit específico y eliminar permanentemente todos los commits y cambios que se realizaron después de ese commit en la rama actual.

![reset --hard](/img/302_antesDeReset--hard.png)

Resultado:

![reset --hard](/img/302_despuesReset--hard.png)

No solo se desharán los commits posteriores, sino que también se eliminarán los cambios en el directorio de trabajo y el área de preparación (staging).

* Paso 4.

Ahora nos interesa retroceder hasta donde agregamos los heroes y con `gir reser --hard <hash-del-commit>`retrocedemos en el tiempo y como no le esta dando el segumiento nos borra el archivo **, Git eliminó los cambios y archivos que se hicieron después de ese commit, incluido el archivo que mencionaste.** y tambien borramos otros archivos dejando solo 2:

![resto de archivos](/img/302_restoDeArchivos.png)

Sin embargo, aquí viene el factor sorpresa: cuando inicialmente incluimos a Linterna Verde y Robin, estábamos en el camino correcto. Ahora, nuestra misión es volver a ese momento en el tiempo donde todo estaba en perfecto orden.

### `git reglog` 

El comando "git reflog" muestra un registro de referencia en Git. Muestra un historial de referencias, incluidas las ramas y los commits a los que se ha hecho referencia recientemente en el repositorio. Cada entrada en el registro reflog incluye información como el hash del commit, la acción realizada (por ejemplo, reset, merge, commit, etc.), y la ubicación del encabezado HEAD (la referencia actual).

![git reflog](/img/302_reflog.png)

`git reflog` es una herramienta útil para realizar un seguimiento de los cambios en un repositorio Git y puede ser especialmente útil para la recuperación de datos en situaciones inesperadas.

A continuación, nos enfocaremos en el hash del commit de **heroes.md: Agregamos a Robin y Linterna Verde**, y mediante el comando git reset --hard <hash-del-commit>, restauraremos todo mi repositorio a exactamente cómo estaba en ese punto.

![reset --hard Recuperacion](/img/302_resert--hardRecuperacion.png)



















 