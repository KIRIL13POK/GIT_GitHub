![git](https://git-scm.com/images/logos/1color-darkbg@2x.png)

 Continuaremos trabajando en un proyecto proporcionado por el profesor, un proyecto que ha estado en seguimiento con Git durante bastante tiempo.

 En este punto, hemos construido una sólida base en Git, comprendiendo cómo gestionar commits, crear y fusionar ramas, y colaborar en proyectos. Ahora, es el momento de explorar una herramienta esencial: el "stash".

 ![inicio](/img/501_inicio.png)

 * Paso 1.

 Hacemos modificaciones en el archivo misiones.md en la rama master y añadimos una linea y de repente, tu jefe o alguien importante necesita que realices un despliegue de la versión principal en producción de manera urgente. Sin embargo, tienes cambios en tu rama que aún no están listos.

  Si te encuentras en una situación en la que necesitas deshacer los cambios realizados en tu rama actual, pero no deseas perderlos, puedes utilizar el "stash". El "stash" te permite guardar temporalmente tus cambios en un lugar especial para poder resolver la situación urgente. Luego, puedes recuperar tus cambios del "stash" y continuar trabajando donde lo dejaste.

  ### `git stash`

  ![git stash](/img/501_git-stash.png)

  A partir de este momento, todos mis cambios se encuentran guardados en el "stash":

  ![gig stash lg](/img/501_git%20-stash-lg.png)


  ### `git stash list`

  Se utiliza para mostrar la lista de registros temporales (stash) que has creado en tu repositorio Git. Cada registro en la lista representa un conjunto de cambios que has guardado temporalmente utilizando "git stash". Esta lista te proporciona una visión general de los registros en el stash, lo que te permite seleccionar uno específico para aplicar o eliminar si es necesario.

  ![git stash list](/img/501_git-stash-list.png)

  ***
  **Es posible crear múltiples registros en el stash, pero una buena práctica es trabajar con ramas, lo cual ayuda a evitar muchos conflictos.**
  ****

* Paso 2.

Modificaciones en el README.md y hacemos un commit respectivo:

![actualizado](/img/501_readme-actualizado.png)

Asi es como se ve ahora el historial de commits: 

![historial](/img/501_lg-historial.png)

* Paso 3.

### `git stash pop`

Se utiliza para aplicar el registro más reciente del stash (almacén de cambios temporales) a tu directorio de trabajo y eliminarlo del stash. En otras palabras, "git stash pop" recupera los cambios almacenados temporalmente en el stash y los aplica a tu rama actual, dejando tu stash limpio.

![git stash pop](/img/501_git_stash-pop.png)

Los cambios en README.md no generan ningún conflicto en este caso y podemos finalizar con un commit :

![commit misiones](/img/501_commit-misionespng.png)



