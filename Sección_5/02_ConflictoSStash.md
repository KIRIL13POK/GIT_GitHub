![git](https://git-scm.com/images/logos/1color-darkbg@2x.png)

# Conflictos de Stash

1. Los conflictos al hacer el stash pueden ser más sencillos, como cuando Git detecta que los archivos no son idénticos, pero también reconoce que los cambios se realizan en diferentes partes del archivo y no se afectan entre sí. Esto significa que los cambios en una parte del archivo no interfieren con los cambios en otra parte, lo que facilita la resolución de conflictos ya que no es necesario combinar o elegir entre los cambios en conflicto, simplemente se pueden aplicar ambos conjuntamente sin problemas.


2.  Otro tipo de conflicto ocurre cuando Git necesita que el desarrollador revise el archivo y realice cambios manuales, similar al proceso de fusionar ramas durante un merge. En este caso, el desarrollador debe intervenir y ajustar manualmente las áreas en conflicto en el archivo. A pesar de que Visual Studio Code, como editor de código, puede facilitar este proceso, aún puede ser un desafío. Una vez que se resuelven manualmente los conflictos, se procede a realizar un commit para registrar los cambios resueltos en el historial del repositorio.
***
**Cuando tienes un conflicto y debes resolverlo manualmente, el stash no se borra automáticamente. El stash permanece en el historial de stashes de Git incluso después de resolver el conflicto y realizar un commit con los cambios resueltos.Git no elimina los registros del stash a menos que tú lo hagas explícitamente utilizando comandos como `git stash drop` o `git stash clear`. Esto significa que puedes volver a aplicar el stash en el futuro si lo necesitas, incluso después de haber resuelto un conflicto y realizado commits adicionales.Por lo tanto, puedes estar seguro de que tu trabajo almacenado en el stash se mantendrá en el historial de stashes hasta que decidas eliminarlo.**
***