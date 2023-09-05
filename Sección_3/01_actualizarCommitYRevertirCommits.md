Vamos a profundizar en cómo editar y mejorar nuestros commits en Git y otros aspectos clave. A medida que avanzamos en nuestro proyecto, es común cometer errores o necesitar ajustar cosas. Git simplifica el proceso, permitiéndonos llevarlo a cabo de manera efectiva y sin inconvenientes, especialmente en lo que respecta a los commits y más.

### ``git commit -am "el mensaje"`

Git tome todos los cambios que hayas realizado en los archivos rastreados **(aquellos que ya han sido agregados previamente al repositorio)** y que los incluya en un nuevo commit con el mensaje que proporcionas. Esto es útil cuando realizas pequeñas modificaciones y deseas hacer un commit rápido sin pasar por el proceso de git add por separado. Sin embargo, ten en cuenta que este comando no agrega archivos nuevos al repositorio; solo funciona con archivos ya rastreados.

***
A continuación tenemmos un ejemplo de un comentario mal hecho:

![comit mal hecho](/img/3_1commitMalHEcho.png)

Hay varias formas de corregir este error:

### `git commit --amend -m "commit"`

Se utiliza  para corregir errores tipográficos, mejorar la descripción o agregar detalles adicionales a un commit anterior *( para el último commit en la rama actual)*. 

![amend-m](/img/301_amned-m.png)

### `git reset --soft HEAD^`

 Esto es útil si deseas agrupar cambios con el commit anterior o si cometiste un error en el commit anterior y deseas corregirlo. Sin embargo, ten en cuenta que, al igual que con otros comandos que modifican la historia, debes tener precaución al usarlo si ya has compartido el commit con otros colaboradores, ya que podría causar conflictos en la historia del repositorio.

 ![reset --soft HEAD^](/img/301_softHead.png)