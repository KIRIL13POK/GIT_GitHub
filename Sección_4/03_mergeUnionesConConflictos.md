# Un conflicto

Un conflicto en Git es una situación en la que diferentes ramas o colaboradores han modificado la misma parte de un archivo o línea de código, y Git no puede combinar estos cambios automáticamente. Requiere la intervención manual de un desarrollador para decidir qué cambios se deben conservar y cómo se deben combinar. Resolver un conflicto implica examinar y editar el archivo en conflicto para asegurar que el resultado final sea coherente y funcional antes de continuar con la fusión de ramas. Es una parte esencial del trabajo colaborativo con Git para garantizar la integridad del código compartido.

* Paso 1.

Preparamos una nueva rama para realizar cambios y la hemos registrado.

Regresamos a la rama master para realizar modificaciones y registrarlos adecuadamente.

![master](/img/403_master-conflicto.png)
***
**Entonces, hemos creado un conflicto al modificar el mismo archivo en el mismo proyecto de diferentes maneras. Esto puede ocurrir con frecuencia cuando varios desarrolladores trabajan en equipo y realizan cambios simultáneos en el mismo archivo.**
***

* Paso 2 .

A continuación, vamos a explorar cómo Git se comporta cuando intentamos fusionar ramas utilizando git merge, y analizaremos su comportamiento y los mensajes de advertencia relacionados con conflictos que proporciona.

![conflicto muestra](/img/403_rama3-conflicto.png)

Esto lo que pasa si lo intentamos con el boton **Resolver en el Editor combinación**:

![solucion conflicto](/img//403_opciones-solucion-conflicto.png)

Elegimos como debe quedar nuestor archivo , de mejor manera y  un commit para el registro:

![conflicto solucion](/img/403_COMMIT-SOLUCION-REGISTRO.png)

Resultado final:

![resultado final](/img/403_PUNTO-UNION-CONFLICTO-RESUELTO.png)
