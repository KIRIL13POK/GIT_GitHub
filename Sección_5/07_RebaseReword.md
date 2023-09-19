
![git](https://git-scm.com/images/logos/1color-darkbg@2x.png)

# Rebase - Reword

**La operación reword se utiliza para cambiar el mensaje de confirmación de un commit específico durante un rebase interactivo.**

* Seleccionar un Commit para Modificar: Cuando realizas un rebase interactivo y llegas a la lista de commits, puedes elegir reword junto al commit que deseas modificar.

  ![reword](/img/507_rebase-1.png)

* Edición del Mensaje de Confirmación: Después de seleccionar reword y guardar el archivo de rebase, Git abrirá un editor de texto (a menudo Vim) que te permite editar el mensaje de confirmación del commit seleccionado.

  ![reword](/img/507_rebase-2.png)

* Modificar el Mensaje: En el editor de texto, puedes cambiar el mensaje de confirmación de acuerdo a tus necesidades. Esto es útil si deseas corregir errores tipográficos, mejorar la claridad del mensaje o proporcionar una descripción más precisa.

* Guardar y Continuar: Una vez que hayas realizado las modificaciones necesarias en el mensaje de confirmación, guarda y cierra el editor de texto. Git continuará con el proceso de rebase.

**Resultado: Después de completar el rebase, el commit en cuestión tendrá el nuevo mensaje de confirmación que especificaste.**

El uso de reword es útil cuando necesitas hacer ajustes en los mensajes de confirmación de commits individuales sin cambiar el contenido de los commits en sí. Esto puede ayudarte a mantener un historial de confirmaciones más claro y significativo.

***
**Es importante recordar que, una vez que se ha realizado un push de un commit a un repositorio remoto, no se debe utilizar reword en ese commit, ya que modificaría la historia de confirmaciones compartida, lo que podría causar conflictos en colaboraciones y dificultades para otros miembros del equipo. Por lo tanto, se recomienda usar reword principalmente en commits que aún no se han compartido con otros.**
***

![reword](/img/507_rebase-resultado.png)