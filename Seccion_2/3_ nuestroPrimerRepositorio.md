![git](https://git-scm.com/images/logos/1color-darkbg@2x.png)

En esta clase, nos centraremos en un proyecto web preexistente, desarrollado por terceros, con el propósito de aprender y practicar los conceptos fundamentales de Git y el control de versiones. Trabajaremos con un proyecto llamado "01_baces", que ya contiene contenido web implementado utilizando la tecnología Bootstrap.

 Lista de los comandos que se abordarán en esta clase:
 ```bash
    git init
    git config --global init.defaultBranch main
    git status
    git add <archivo>
    git add .
    git commit -m "Mensaje del commit"
    git log
 
 ```

Estos comandos son fundamentales para trabajar con Git y permitirán que comprendas cómo se gestionan los cambios y cómo se crean versiones en un proyecto.


# Repositorio
Un repositorio en Git es un contenedor que almacena y gestiona el historial de versiones de un proyecto. Actúa como una base de datos que registra todos los cambios rea
lizados en los archivos a lo largo del tiempo. Esto permite a los desarrolladores trabajar en diferentes versiones, colaborar eficientemente y realizar un seguimiento preciso de las modificaciones. Los repositorios en Git mantienen información sobre commits, ramas y etiquetas, permitiendo a los equipos desarrollar software de manera estructurada y rastreable.

1. ###  `git init`
Inicializa un nuevo repositorio en el directorio actual.

![gitInit](/img/gitInitTerminal.png)

Resultado:

![gitInit](/img/gitInitResultado.png)

El directorio **.git** creado después de ejecutar git init es esencial en Git, ya que almacena el historial completo de versiones, ramas y configuraciones del repositorio. Contiene información crítica para realizar seguimiento de cambios, revertir acciones y colaborar en el desarrollo de software. **No se debe modificar manualmente para evitar problemas en la integridad del repositorio.**

2. ### `git status`
 Muestra el estado actual del repositorio, resaltando cambios y archivos sin seguimiento.

![gitInit](/img/gitStatusTerminal.png)

En este punto, Git indica que los archivos mencionados no están siendo rastreados por el sistema, lo que significa que no se están registrando sus cambios ni se incluirán en los próximos commits.

3. ### `git add <archivo>` / `git add .`
    * Añade un archivo específico al área de preparación (stage) para ser incluido en el próximo commit.

     * Añade todos los archivos modificados al área de preparación.

![gitAddPunto(/img/gitAddPunto.png)]  

Después de ejecutar `git add .`, Git comienza a rastrear los archivos mencionados, lo que implica que se están preparando para ser incluidos en el próximo commit y se registrarán sus cambios.

![gitStatusSeguimiento](/img/gitStatusTerminalSeguimiento.png)

4. ### `git reset <archivo>`/ `git reset`
    *  Quita un archivo específico del área de preparación sin cambiar su contenido en el directorio de trabajo.

    * Quita todos los archivos del área de preparación sin cambiar el directorio de trabajo. 

5. ### `git commit -m `"Mensaje del commit"
 Crea un nuevo commit con los archivos preparados y un mensaje descriptivo.

 ![gitCommit](/img/gitCommit-m.png)

  Git creará un nuevo commit con los cambios preparados en el área de preparación (stage) y el mensaje especificado. El estado del repositorio será el siguiente:

* Los cambios realizados en los archivos que estaban en el área de preparación se guardarán en un nuevo commit.

* El área de preparación estará vacía, ya que los cambios se han comprometido.

* Al ejecutar git status, mostrará que no hay cambios pendientes para hacer commit y que la rama actual está "limpia".

 ![gitCommit](/img/gitCommit-mStatus.png)

En resumen, los cambios se han registrado en un nuevo commit y el repositorio estará actualizado en relación con la rama actual.

6. ### `git log`
 Muestra el historial de commits realizados en el repositorio.

 ![gitLog](/img/gitLog.png)

Un commit en Git debe realizarse después de completar una funcionalidad importante, un conjunto coherente de cambios o una mejora significativa en el proyecto.