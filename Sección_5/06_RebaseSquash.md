![git](https://git-scm.com/images/logos/1color-darkbg@2x.png)

El ****Rebase - Squash** es una operación en Git que combina varios commits contiguos en uno solo, lo que ayuda a mantener un historial de cambios más limpio y coherente. Este proceso se llama **aplastamiento** (squash en inglés) porque reduce múltiples commits en uno, lo que facilita la revisión y la comprensión del historial de cambios. El objetivo principal del **Rebase - Squash** es simplificar la historia del repositorio y agrupar cambios relacionados en un único commit significativo.

* Paso 1.

Hacemos unos cambios en misiones.md y misiones-completadas.md y los confirmamos con un commit:

![inicio](/img/506_inicio.png)

Es relevante notar que se realizaron actualizaciones en las misiones completadas en un commit anterior, y luego se hicieron cambios en dos misiones adicionales en el commit siguiente. A pesar de las diferencias en las modificaciones específicas, ambas acciones están relacionadas, lo que sugiere la posibilidad de unificar estos dos commits, ya que representan esencialmente la misma tarea.


### `git rebase -i HEAD~N` 

Para unificar estos commits, podemos utilizar el siguiente comando Git en modo interactivo: donde N es el número de commits que deseamos unificar.
***
*El carácter ~ , tilde o virgulilla El signo ~ corresponde al carácter ASCII numero 126. En un PC hay dos maneras de obtenerlo: - Pulsar la tecla Alt y, sin soltarla, utilizar el teclado numérico, a la derecha, para pulsar sucesivamente los números 1, 2 y 6; luego soltar la tecla Alt, y aparecerá el signo ~.*
***

A continuación: 

![cuadro](/img/506_head~.png)

Cuando ejecutas el comando git rebase `-i HEAD~N`, donde N es el número de commits que deseas incluir en la operación de rebase, Git te abrirá un editor de texto con una lista de esos últimos commits. Cada línea representará un commit y tendrá una serie de opciones que puedes elegir para cada commit. Estas opciones suelen ser:

1. pick: Mantén el commit tal como está.
2. reword: Cambia el mensaje del commit.
3. edit: Pausa el rebase para que puedas hacer cambios en ese commit.
4. squash: Combina este commit con el commit anterior.
5. fixup: Similar a squash, pero descarta el mensaje de este commit.
6. exec: Ejecuta un comando personalizado.
7. drop: Elimina el commit.

Debes seleccionar una opción para cada commit que aparece en la lista, luego guardar y cerrar el editor. Git seguirá tus instrucciones y realizará el rebase según las opciones que hayas seleccionado.

![squash](/img/506_squash.png)

***
*Cuando ejecutas el comando git rebase -i HEAD~N, Git abrirá un archivo de texto en un editor de texto interactivo. El editor de texto que se utiliza por defecto en este caso depende de la configuración de Git y de tu sistema operativo. En muchos casos, Git abrirá el editor Vim para que puedas realizar la edición interactiva del rebase.*

*Una vez realizados los  cambios para salir debemos pulsar `ESC` y escrebir  `:wq!` se utiliza en el editor de texto Vim para guardar los cambios en un archivo y salir del editor.*

* **:** -*Esto coloca Vim en el modo de comando, lo que significa que estás dando un comando a Vim en lugar de escribir texto.*

* **w** - *Esto es parte del comando :w, que se utiliza para guardar (escribir) los cambios en el archivo.*

* **q** - *Esto es parte del comando :q, que se utiliza para salir de Vim.*

* **!** - *Esto se agrega al final para forzar la salida, incluso si hay cambios no guardados en el archivo.*

*Entonces, `:wq! ` en Vim guarda los cambios en el archivo y luego sale del editor, incluso si hay cambios no guardados. Es una forma común de guardar y salir en Vim.*

 ![:wq!](/img/506_wq!.png)

***

A continuacion : 

![squash](/img/506_squash-commits.png)

Este mensaje es la ventana de edición que se muestra durante un rebase interactivo en Git. Durante el rebase interactivo, puedes combinar dos o más commits en uno solo, y esta ventana te permite editar los mensajes de commit relacionados con esta acción. En este contexto, estás viendo el mensaje de commit que se está creando al fusionar dos commits previos en uno solo, utilizando la opción "squash" de Git.

En este ejerciocio lo vamos a dejar tal y como esta y saldremos de editor Vim co `:wq!`

![rebase squash exitoso](/img/506_rebase-squesh-exitoso.png)

Resultado:

![resultado squash](/img/506_resultado-squash.png)

# NOTA IMPORTANTE

**El rebase interactivo se debe utilizar con precaución, especialmente cuando los commits ya se han compartido en el repositorio remoto. Si ya has realizado un push de tus cambios, es preferible dejar esos commits tal como están. Esto se debe a que esos cambios podrían haber sido descargados por otros colaboradores, lo que podría generar conflictos innecesarios que alguien más deberá resolver.**

**Por lo tanto, se recomienda utilizar el rebase interactivo solo cuando sea absolutamente necesario y estés seguro de que tus modificaciones no han salido del entorno local de tu computadora**
***

