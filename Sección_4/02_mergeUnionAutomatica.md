En el proyecto de la Sección 4, estamos considerando cambios en "villanos.md", pero su inclusión final es incierta. Por lo tanto, creamos una nueva rama para realizar estos cambios de forma aislada y evaluar si son necesarios en la versión final del proyecto. Esto nos permite mantener la flexibilidad y tomar decisiones más tarde sobre la incorporación o eliminación de estos cambios sin afectar la rama principal.

### `git checkout -b <nombre-de-rama> `

Crea una nueva rama con el nombre especificado y te cambia automáticamente a esa nueva rama. En otras palabras, este comando combina dos acciones en una sola:

1. Crea una nueva rama con el nombre que proporcionaste.
2. Cambia tu entorno de trabajo para que estés trabajando en la nueva rama recién creada.

Este comando es muy útil cuando deseas comenzar a trabajar en una nueva característica o solución en una rama separada y deseas hacerlo de manera eficiente, sin tener que ejecutar comandos adicionales para cambiar de rama después de crearla.

![gir checkout -b](/img/402-git-checkout-b.png)

* Paso 1.

Modificaciones en el villanos.md:

![doomsday](/img/402_cambios-Domsdaypng.png)

más cambios:

![doomsday](/img/402_cambios-notas.png)

* Paso 2.

Urgentemente, para continuar, debemos eliminar "Daredevil" del archivo "heroes.md", pero realizaremos este cambio en la rama "master"

![Daredevil](/img/402_Daredevil-FUERA.png)

* Paso 3.

A continuación, hemos realizado todos los cambios necesarios en ambas ramas y ahora estamos listos para fusionarlas en nuestro proyecto.
* `git checkout master` -Para unir los cambios, debes estar trabajando en la rama de destino, es decir, la rama en la que deseas incorporar los cambios de la otra rama.**Es importante estar en la rama de destino antes de realizar la fusión para asegurarte de que los cambios se incorporen en la rama correcta.**
`git merche <nombre-de-rama>`

Cuando no se identifican conflictos, logramos el resultado deseado: las dos ramas se unen, y la rama "master" con sus modificaciones incorpora todas las modificaciones de la rama "rama2-villanos":

![resultado de la union](/img/402_PUNTO-DE-UNION.png)

