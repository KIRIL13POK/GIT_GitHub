![git](https://git-scm.com/images/logos/1color-darkbg@2x.png)
# Untracked file -"u"
Un archivo que tiene una **"u"** en su nombre se llama **"archivo con cambios no seguibles"** o **"untracked file"** en inglés. En el contexto de Git, esto significa que el archivo existe en tu directorio de trabajo local pero no está siendo rastreado por Git. Esto ocurre cuando el archivo es nuevo o ha sido modificado desde la última confirmación y aún no se ha agregado al área de preparación (staging area) utilizando el comando git add.

Los archivos no seguibles son importantes en Git porque representan cambios en tu proyecto que Git no está supervisando de manera activa. Para incluir estos cambios en tus confirmaciones, debes usar `git add` para agregarlos al área de preparación y luego realizar una confirmación con `git commit`.

Esencialmente, los archivos no seguibles son aquellos que Git no tiene en cuenta a menos que los incluyas explícitamente en tus confirmaciones. Esto te brinda un mayor control sobre qué cambios se registran en el historial de tu proyecto.

![untracked_file](/img/untracked_file.png)

