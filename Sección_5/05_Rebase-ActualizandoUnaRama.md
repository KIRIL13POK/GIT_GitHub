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
### La relevancia de completar un merge tras un rebase en Git

Cuando se realiza un rebase y avance rápido, todos los commits de la rama secundaria se "reproducen" en la rama principal, en este caso, "master". Como resultado, la rama principal ("master") ya contiene todos los commits de la rama secundaria ("rama-misiones-completadas"), y la historia de commits está ordenada y lineal.


Sin embargo, es importante tener en cuenta que el rebase solo afecta al historial de commits, no a los archivos del proyecto en sí. En algunos casos, puede haber archivos que solo estén presentes en la rama "rama-misiones-completadas" y no se hayan incluido en la rama principal("master").

Por lo tanto, realizar un merge después de un rebase sigue siendo importante para asegurarse de que todos los cambios, incluyendo los archivos, se hayan incorporado correctamente en la rama principal. Esto garantiza que el proyecto esté completo y que no falten archivos importantes.

**En resumen, mientras que el rebase ayuda a mantener un historial de commits limpio y lineal, el merge es esencial para garantizar la integridad y completitud del proyecto, especialmente cuando se trata de archivos que solo están presentes en la rama principal.**

***
#### En el caso de no tener que realizar un merge: 

En este caso  Git indica que se trata de eliminar la rama 'rama-misiones-completadas',y que  ha detectado que esta rama no ha sido completamente fusionada (merged) con la rama actual o con la rama principal, lo que podría resultar en la pérdida de cambios no incorporados.

![error](/img/505_git-branc-d.ERROr.png)

### `git branch D rama-misiones-completadas`

 La opción -D (mayúscula) forzará la eliminación de la rama sin importar si los cambios se han fusionado o no.





