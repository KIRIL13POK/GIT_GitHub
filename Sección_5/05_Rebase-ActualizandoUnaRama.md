![git](https://git-scm.com/images/logos/1color-darkbg@2x.png)

Para este ejercicio, tenemos un seguimiento de Git con el siguiente historial de commits en este momento:

![inicio](/img/505_inicio.png)

En el historial de commits de Git, tenemos dos ramas principales: **master** y **rama-misiones-completadas**. Hace algún tiempo, se creó una separación en el historial cuando se actualizó la rama-misiones-completadas. Esto resultó en la aparición de la rama misiones completadas. Sin embargo, esta última rama no está fusionada con master, lo que significa que algunos commits en misiones completadas aún no se incluyen en master. La tarea es incorporar esos commits en misiones completadas, y esto se puede hacer mediante rebase o merge desde master.

* PAso 1.
Para unir los commits de la rama "rama-misiones-completadas" al "master" utilizando el comando de rebase, debes estar situado en la rama "rama-misiones-completadas". 

### `git checkout rama-misiones-completadas`

* Paso 2.
### `git rebase master`

![git rebase](/img/505_git-rebase.png)

Este comando tomará los commits de la rama "rama-misiones-completadas" y los aplicará uno por uno encima de la rama "master", lo que resultará en una línea de tiempo de commits más lineal y limpia en la rama "master". Asegúrate de haber guardado tus cambios antes de realizar el rebase, ya que podría haber conflictos que necesiten ser resueltos manualmente.

Resultado:

![resuktado](/img/505_resultado-rebasepng.png)

* Paso 3.

### `git branch -d <rama-misiones-completadas>`

Se utiliza para eliminar una rama en Git. En este caso, rama-misiones-completadas es el nombre de la rama que deseas eliminar.

***
**Cuando se realiza un rebase y avance rápido, todos los commits de la rama secundaria se "reproducen" en la rama principal, en este caso, "master". Como resultado, la rama principal ("master") ya contiene todos los commits de la rama secundaria ("rama-misiones-completadas"), y la historia de commits está ordenada y lineal.**

**En este contexto, no es necesario realizar un merge adicional porque la rama principal ya incluye los cambios de la rama secundaria y no hay bifurcación en el historial de commits. Los cambios de ambas ramas se han incorporado con éxito en la rama principal mediante el rebase.**

**Por lo tanto, en este caso específico, puedes eliminar la rama secundaria ("rama-misiones-completadas") después de un rebase exitoso sin necesidad de realizar un merge adicional. Sin embargo, siempre es importante verificar que todos los cambios se hayan incorporado correctamente antes de eliminar cualquier rama.**
***

