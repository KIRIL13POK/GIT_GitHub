En esta clase, conocemos conceptos básicos relacionados con Git y GitHub, así como el proceso de trabajar con repositorios remotos.

* **Repositorio Remoto**: Un repositorio remoto es una copia de tu proyecto en un servidor en línea, lo que te permite respaldar tu trabajo y colaborar con otros.

* **Push**: El comando "push" se utiliza para enviar tus cambios locales al servidor remoto, lo que actualiza el repositorio en línea con tus últimas modificaciones.

* **Pull**: Cuando otras personas quieren obtener tus cambios desde el servidor remoto, utilizan el comando "pull" para descargar esos cambios y fusionarlos en su copia local.

* **Colaboración en Git**: Git no controla el acceso a nivel de archivo, lo que significa que no puede restringir quién puede trabajar en qué partes del repositorio. Se necesitan servicios adicionales para gestionar el control de acceso.

* **Git y GitHub**: Git es el sistema de control de versiones, mientras que GitHub es una plataforma en línea que aloja proyectos Git. Son dos entidades diferentes.

* **GitHub Gratuito**: GitHub ofrece una versión gratuita con características poderosas, como repositorios ilimitados, páginas HTML, CSS, JS ilimitadas, push y pull ilimitados, organizaciones ilimitadas y participación gratuita en proyectos privados.

* **Repositorios Públicos vs. Privados**: Puedes crear repositorios públicos (accesibles para que otros los vean) o privados (accesibles solo para personas autorizadas). GitHub permite repositorios privados de forma gratuita desde enero de 2019.

* **Agregar un Repositorio Remoto**: Para conectar tu repositorio local con un repositorio remoto en GitHub, puedes usar el comando "git remote add origin URL". "Origin" es un nombre estándar, pero puedes personalizarlo. La URL es la ubicación del repositorio remoto.

* **Revisar Repositorios Remotos**: Puedes usar el comando "git remote -v" para ver una lista de repositorios remotos que están vinculados a tu repositorio local.

* **Git Push**: El comando "git push origin master" envía los cambios locales en la rama "master" al repositorio remoto denominado "origin". Puedes personalizar el nombre de la rama y el repositorio remoto según tus necesidades.

* **Credenciales de Acceso**: Cuando haces un push, GitHub te pedirá tus credenciales (usuario y contraseña). Se pueden configurar opciones para recordar estas credenciales de manera predeterminada.