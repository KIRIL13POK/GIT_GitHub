![git](https://git-scm.com/images/logos/1color-darkbg@2x.png)

***
**En Git, las "etiquetas" (tags) son simplemente mensajes o marcas que se asignan a puntos específicos en la historia de un repositorio, generalmente a commits. Estas etiquetas se utilizan para que puedas rápidamente identificar y hacer referencia a un commit en el futuro. En esencia, son nombres descriptivos que facilitan la gestión y el acceso a momentos importantes en la evolución de tu proyecto de software. Las etiquetas en Git te permiten recordar y encontrar fácilmente commits clave, como versiones de software estables o hitos significativos en el desarrollo.**
***

En este momento, hemos completado la versión 1 de nuestra aplicación y está lista para ser lanzada en un servidor de producción. 

![inicio](/img/405_inicio-de-clase.png)


### `git tag <nombre>`

Se utiliza para crear una nueva etiqueta (tag) en el repositorio actual. Debes reemplazar *nombre* con el nombre que deseas darle a la etiqueta que estás creando. Esta etiqueta generalmente se aplica al commit actual en el que te encuentras en ese momento.

![git tag](/img/405_git-tag.png)

### `git tag -d <nombre>`

Se utiliza para eliminar una etiqueta (tag) . Debes reemplazar *nombre* con el nombre de la etiqueta que deseas eliminar. Esta opción es útil cuando deseas eliminar una etiqueta que ya no es necesaria o que fue creada por error.

![eliminar tag](/img/405_git-tag-d.png)


***
 ### Versionado Semántico o Semantic Versioning.

 La versión semántica, a menudo referida como "Versionado Semántico" o "Semantic Versioning" en inglés, es un sistema de numeración de versiones utilizado comúnmente en el desarrollo de software para comunicar claramente los cambios en una biblioteca o proyecto y gestionar las dependencias de software de manera eficiente. Está diseñado para facilitar la comprensión de cómo una nueva versión afecta la compatibilidad y la funcionalidad del software existente.

El formato básico de una versión semántica es "X.Y.Z", donde:

* **X** representa la versión principal (major version).
* **Y** representa la versión menor (minor version).
* **Z** representa la versión de revisión o parche (patch version).

La idea detrás de la versión semántica es que:

*Incrementar la **versión principal (X)** indica cambios incompatibles en la API o funcionalidad del software que pueden requerir una revisión significativa en el código que lo utiliza.

Incrementar la **versión menor (Y)** indica la adición de nuevas funcionalidades de una manera compatible con versiones anteriores, lo que significa que el software existente debería seguir funcionando correctamente.

Incrementar la **versión de revisión (Z)** indica correcciones de errores o cambios menores que no afectan la compatibilidad y no introducen nuevas características.

Además de estos números, se pueden agregar etiquetas adicionales, como "alfa" o "beta", para indicar versiones de desarrollo o de prelanzamiento.

En el contexto de Git y las etiquetas (tags), una "versión semántica de un tag" generalmente se refiere a la práctica de nombrar etiquetas siguiendo el formato de versión semántica (por ejemplo, "v1.0.0", "v2.1.3"). Esto ayuda a los desarrolladores a comprender rápidamente la naturaleza de una versión etiquetada, ya que proporciona información sobre si se trata de una versión mayor, menor o de revisión, y si incluye nuevas características o correcciones de errores.

La versión semántica y el etiquetado siguiendo este formato son especialmente útiles en proyectos de desarrollo de software colaborativo, donde múltiples personas trabajan en el mismo código o cuando se gestionan dependencias de software, ya que ayudan a garantizar que las actualizaciones se realicen de manera controlada y predecible.
***

### `git tag -a <version> -m "mensaje"`

 Se utiliza para crear una nueva etiqueta anotada (annotated tag) y asociar un mensaje descriptivo a esa etiqueta.

*version*: Debes reemplazar esto con el nombre que deseas darle a la etiqueta que estás creando. Por lo general, se utiliza un formato de versión semántica, como "v1.0.0".

*-a*: Esta opción indica que estás creando una etiqueta anotada. Las etiquetas anotadas son objetos Git independientes que almacenan información adicional, como un mensaje descriptivo, el nombre del etiquetador y la fecha en que se creó la etiqueta.

*-m "mensaje"*: Esta parte del comando te permite adjuntar un mensaje descriptivo a la etiqueta. El mensaje debe estar entre comillas dobles y se utiliza para proporcionar información sobre la etiqueta, como por qué se creó o qué cambios importantes representa.

![verson semantica](/img/405_git-tag-a.png)

### `git tag -a v1.0 <hash> -m <mensaje>`

Esta etiqueta anotada proporciona una forma conveniente de referenciar y marcar un commit específico en la historia del repositorio, lo que facilita la identificación de versiones importantes o hitos en el desarrollo del proyecto.

![git-tag-hash](/img/405_git-tag-a-hash.png)

### `git show <Semantic-Versioning>`

Se utiliza para mostrar información detallada sobre el commit al que está asociada la etiqueta(v1.0.0)

![git show](/img/405_git-show.png)

* **Tagger:** Indica quién creó la etiqueta "v1.0.0" y su dirección de correo electrónico.

* **Date:** Muestra la fecha y la zona horaria en la que se creó la etiqueta "v1.0.0".

* **Mensaje de la etiqueta:** "Version 1.0.0 lista" es el mensaje descriptivo que se adjuntó a la etiqueta cuando se creó. Este mensaje proporciona información sobre la naturaleza de esta versión etiquetada.

* **Commit SHA:** "38a698985a5e34b07bd6ed2d6259a583a3d0f012" es el hash único que identifica este commit específico.

*  **Autor y fecha del commit:** Muestra quién realizó el commit, su dirección de correo electrónico y la fecha en que se realizó.

* **Mensaje del commit:** Proporciona un mensaje descriptivo sobre los cambios realizados en este commit en particular. En este caso, parece que se resolvió un conflicto en el archivo "misiones.md" como parte de este commit.

* **Diferencias (diff):** Muestra las diferencias en el archivo "misiones.md" antes y después de este commit. En este caso, parece que se realizaron cambios en las líneas 1, 2 y 3 del archivo.

Esta salida es útil para rastrear y entender los cambios en el proyecto, especialmente cuando se trabaja con etiquetas que marcan versiones específicas o hitos en la historia del repositorio. Te permite ver quién hizo el commit, cuándo se realizó y qué cambios se introdujeron en ese momento.