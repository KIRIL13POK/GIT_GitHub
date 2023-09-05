![git](https://git-scm.com/images/logos/1color-darkbg@2x.png)

En esta clase seguimos trabajando t con un proyecto ya existente para aprender sobre los comandos de Git. Aprendimos a inicializar un repositorio con "git init". Exploramos cómo Git rastrea y no rastrea archivos en función de las modificaciones que realizamos, y vimos que después de agregar cambios con "git add .", los archivos están listos para ser comprometidos. Además, comprendimos el uso de "git reset" para revertir cambios en archivos específicos. Luego, realizamos un commit con "git commit -m 'mensaje'" para guardar los cambios en un punto específico y vimos cómo el comando "git checkout -- ." puede restaurar los archivos a su estado en el último commit. Este proceso ayuda a mantener un historial seguro y a recuperar versiones anteriores del proyecto en caso de problemas.

### `git checkout -- .`

Por alguna razón, enfrentamos un problema y perdimos gran parte de nuestro código en index.html:

![errorHtml](/img/errorHTML.png)

Sin embargo, después de ejecutar `"git checkout -- ."` , logramos recuperarlo tal como lo habíamos dejado en el último commit:

![errorHtml](/img/gitCheckout.png)

***

#### `git checkout -- .` 

***es un comando que actúa como un salvavidas en Git. Cuando ejecutas este comando, le estás diciendo a Git que restaure los archivos en el directorio actual y sus subdirectorios al estado en el que estaban en el último commit. Es especialmente útil cuando has realizado cambios no deseados o te encuentras en una situación en la que deseas deshacer las modificaciones y volver al último estado registrado en el repositorio. En resumen, git checkout -- . permite recuperar los archivos eliminados o modificados a su estado anterior sin afectar los commits realizados.***

***
