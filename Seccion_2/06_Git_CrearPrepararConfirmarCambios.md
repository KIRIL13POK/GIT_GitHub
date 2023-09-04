![git](https://git-scm.com/images/logos/1color-darkbg@2x.png)
# Untracked file -"u"
Un archivo que tiene una **"u"** en su nombre se llama **"archivo con cambios no seguibles"** o **"untracked file"** en inglés. En el contexto de Git, esto significa que el archivo existe en tu directorio de trabajo local pero no está siendo rastreado por Git. Esto ocurre cuando el archivo es nuevo o ha sido modificado desde la última confirmación y aún no se ha agregado al área de preparación (staging area) utilizando el comando git add.

Los archivos no seguibles son importantes en Git porque representan cambios en tu proyecto que Git no está supervisando de manera activa. Para incluir estos cambios en tus confirmaciones, debes usar `git add` para agregarlos al área de preparación y luego realizar una confirmación con `git commit`.

Esencialmente, los archivos no seguibles son aquellos que Git no tiene en cuenta a menos que los incluyas explícitamente en tus confirmaciones. Esto te brinda un mayor control sobre qué cambios se registran en el historial de tu proyecto.

![untracked_file](/img/untracked_file.png)

utilizando el comando `git add .`

![untracked_fileGitAdd](/img/untracked_fileGitAdd.png)

Cuando un archivo en Git muestra una **"A"** en su nombre, esto señala que el archivo se encuentra en **el área de preparación o staging area.** Este estado indica que el archivo ha sido modificado en tu directorio de trabajo y que has utilizado el comando git add para colocarlo en el área de preparación. 

Cuando un archivo en Git muestra una **"M"** en su nombre, esto indica que el archivo ha sido modificado. La "M" se refiere a **"Modified"** en inglés. Esto significa que has realizado cambios en el archivo después de haber realizado su último commit. Estos cambios aún no se han agregado al área de preparación (staging area) mediante el comando git add, por lo que no están listos para ser confirmados en un nuevo commit.

![modified](/img/modifiledM.png)

 Puedes utilizar git diff para ver exactamente qué cambios se han realizado en el archivo.

![modified](/img/gitDiff.png)

Después de usar `git commit -m "mensaje"`, tus cambios quedan guardados de manera permanente en tu proyecto. Estos cambios se guardan en la rama en la que estás trabajando (generalmente, la rama principal). Puedes verlos en cualquier momento. El mensaje que escribas debe explicar de forma clara y breve qué cambios hiciste para que tú o tus colaboradores futuros comprendan su propósito.







