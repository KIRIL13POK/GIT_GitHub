# Los alias en Git

 Son atajos o nombres cortos que puedes crear para comandos Git más largos y frecuentes. Se utilizan para simplificar la ejecución de comandos complejos o para personalizar los comandos según tus preferencias. Los alias permiten ahorrar tiempo y esfuerzo al evitar escribir comandos largos repetidamente. Puedes configurar alias globales que se aplican a todos tus repositorios, lo que facilita su uso en cualquier proyecto Git que tengas en tu sistema.
 ***
  ***En resumen, los alias son una herramienta útil para agilizar y personalizar tu flujo de trabajo con Git.***
  ***

### Modificadores y Banderas en Comandos

### `git status`

![gitStaus](/img/gitStatus_09.png)

### `git status --short`

 Proporciona una vista rápida y simplificada del estado de tus archivos en el repositorio, lo que facilita la identificación de cambios y archivos que necesitan ser confirmados o gestionados.

 ![gitStaus](/img/gitStatusShort_09.png)

  * **U:** Archivos no rastreados (untracked).
  * **A:** Archivos agregados al área de preparación (staging area).
  * **M:** Archivos modificados que aún no están en el área de preparación.
  * **D:** Archivos eliminados que aún no están en el área de preparación.
  * **R:** Archivos renombrados o movidos que aún no están en el área de preparación.
  * **C:** Archivos copiados que aún no están en el área de preparación.

### Para crear tu propio alias en Git, puedes seguir estos pasos:

1. 

### `git config --global alias.nombreAlias "comandoGit"`

Para crear el alias. Reemplaza "nombreAlias" por el nombre que deseas para tu alias y "comandoGit" por el comando de Git que deseas abreviar.

Por ejemplo, si deseas crear un alias para el comando `git status --short` :

```bash

git config --global alias.s "status --short"

```
Resultado:

![AliasResultado](/img/aliasResultado_09.png)

2. 
 ### `git log --oneline`

Es una forma abreviada y concisa de ver el historial de commits en Git. Muestra una lista de los commits en una sola línea, lo que facilita la lectura y la revisión del historial. 

![goiOneline](/img/log--oneline_09.png)

Cada línea muestra el hash del commit (por ejemplo, da97194) seguido de un mensaje que describe los cambios realizados en ese commit. Esto es útil para obtener una vista rápida del historial de commits sin detalles adicionales.

Este alias, llamado "lg" , está diseñado para personalizar la salida del comando git log y proporcionar una vista de registro más detallada y legible:

```bash
git config --global alias.lg "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"
```

Resultado:

![git lg](/img/09_gitLG.png)

***
 ***Para crear comandos detallados en Git requiere comprender las opciones disponibles, el formateo personalizado y experimentar para lograr el resultado deseado. La documentación oficial de Git es una excelente fuente de referencia para obtener información detallada sobre el funcionamiento de cada comando.***
*** 






