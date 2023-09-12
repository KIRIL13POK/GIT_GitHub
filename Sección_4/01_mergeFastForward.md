![git](https://git-scm.com/images/logos/1color-darkbg@2x.png)

En esta sección, trabajaremos en un repositorio de Git que ya está configurado con un seguimiento activo, evidenciado por la existencia de un directorio .git. Además, en este repositorio, encontraremos una carpeta llamada .gitignore que se utiliza para especificar qué archivos o directorios deben ser excluidos del seguimiento de Git. Notablemente, este repositorio ya cuenta con una serie de commits realizados previamente como parte de nuestra actividad en el curso (profesor Fernando Herrera). Esta situación nos permitirá explorar y profundizar nuestros conocimientos sobre la gestión de versiones y las operaciones de Git en un proyecto que ya ha registrado cambios en etapas anteriores.

![lg inroduccion](/img/401_lg_de_introduccion.png)

* Paso 1.

Creamos un archivo nuevo villanos.md pero no sabemos  si esto va formar parte del proyectofinal.

### `git branch <nombre-de-rama>`

Se utiliza en Git para crear una nueva rama con el nombre especificado. Esta rama es una bifurcación independiente del flujo de desarrollo principal y se utiliza para trabajar en características, correcciones de errores u otras modificaciones sin afectar la rama principal (generalmente llamada "master" o "main").

![git bran rama-villanos](/img/401_git_branch_rama-villanos.png)


### `git branch`

Se utiliza para listar todas las ramas que existen en tu repositorio de Git. Cuando ejecutas este comando sin especificar un nombre de rama, Git te mostrará una lista de todas las ramas locales que has creado en tu proyecto y resaltará la rama actual en la que te encuentras trabajando. La rama actual se marcará con un asterisco (*).

![git bran rama-villanos](/img/401_git_branch.png)

### `git checkout <nombre-de-rama>`

Se utiliza en Git para cambiar de una rama a otra. Esto significa que te mueves del contexto de trabajo de una rama a otra rama en tu repositorio.

![git checkout <nombre-de-rama>](/img/401_git_checkout-nombre-de-rama.png)

* Paso 2.

Añadimos este archivo al historial con un `git add .`  y despues un commit con sentido :

![ULTIMO COMMIT](/img/401_ULTIMO-COMMIT-RAMA-VILLANOS.png)

* Paso 3.

Una modificacion en villanos.md 

![PASO 3](/img/401_PASO3.png)

***
Cuando cambias de una rama a otra en Git, el estado de los archivos en tu directorio de trabajo se actualiza para reflejar el estado de la rama a la que te has cambiado.

Si volvemos a la rama master vamos a observar que el archivo villanos.md es eliminado:

![vallnos eliminado](/img/401_checkout-master.png)

**En resumen, al cambiar de una rama a otra en Git, los archivos en tu directorio de trabajo se actualizan para reflejar el estado de la rama actual, y cualquier cambio que se haya realizado en otras ramas puede aparecer como una eliminación si no se ha fusionado o incorporado en la rama actual.**
***

### La unificación de ramas

Se refiere al proceso de combinar los cambios de una rama en otra. Esto generalmente implica tomar los cambios realizados en una rama y fusionarlos en otra rama, a menudo en la rama principal de un proyecto.

### `git merge`

Para fusionar los cambios de la rama rama-villanos en la rama master con el comando `git merge`, primero debes estar en la rama master. 

![git merge](/img/401_git-merge.png)

***
### Fast- forward

![fast-forward](/img/401_fast-forward.png)

Es una operación de fusión en Git que ocurre cuando se combinan dos ramas y la fusión se realiza de manera sencilla y lineal. Esto sucede cuando no se han realizado cambios en la rama de destino desde el punto en el que se separó la rama que se va a fusionar. En este caso, Git simplemente avanza la rama de destino hasta el punto donde está la rama que se está fusionando, ya que no hay conflictos ni cambios conflictivos para resolver. Es una fusión rápida y automática que mantiene una línea de tiempo lineal y simple en el historial de commits.
***

Es importante aclarar que cuando fusionas una rama en Git, como la rama "rama-villanos" en "master", el último commit de "master" no se cambia automáticamente. Lo que ocurre es que se crea un nuevo commit de fusión que refleja la combinación de ambas ramas. Este nuevo commit de fusión tiene dos padres, uno de la rama "master" y otro de la rama "rama-villanos", pero los commits anteriores en "master" no se alteran.

![rama master despues de union](/img/401_git-lg-master%20-despues-de-union.png)

Entonces, en el historial de commits de "master", verás una bifurcación en la línea de tiempo que muestra el punto en el que se unieron las dos ramas, pero los commits anteriores en "master" permanecen intactos. Los cambios realizados en "rama-villanos" se incorporan en "master" a través de este nuevo commit de fusión.


### `git branch -d  <nombre-de-rama>`

Se utiliza  para eliminar una rama que ya no es necesaria. Es importante destacar que este comando solo eliminará la rama si todos los cambios de la rama que se desea eliminar ya se han fusionado en otra rama. En otras palabras, si los cambios de la rama que deseas eliminar ya se incorporaron en la rama principal o en otra rama, puedes utilizar este comando de forma segura.

![git-branc-d](/img/401_git-branch-d.png)