Chuleta GitHub Parte 1


1-	Control de versiones

Un control de versiones es un sistema que registra los cambios realizados en un archivo o conjunto de archivos a lo largo del tiempo, de modo que puedas recuperar versiones específicas más adelante. Dicho sistema te permite regresar a versiones anteriores de tus archivos, regresar a una versión anterior del proyecto completo, comparar cambios a lo largo del tiempo, ver quién modificó por última vez algo que pueda estar causando problemas, ver quién introdujo un problema y cuándo, y mucho más. Usar un VCS también significa generalmente que si arruinas o pierdes archivos, será posible recuperarlos fácilmente. Adicionalmente, obtendrás todos estos beneficios a un costo muy bajo.

2-	Explicar los siguientes conceptos

o	Repositorio local (local repository): 

Un repositorio es una base de datos centralizado donde se guardan las distintas versiones de los ficheros sometidos a control de versiones. El repositorio local es el que se encuentra en nuestro ordenador.

o	Copia local (local copy):

Es la copia que hacen los usuarios de un fichero sometido a control de versiones.

o	Repositorio remoto (remote repository): 

Es una base de datos centralizada donde se guardan las distintas versiones de los ficheros sometidos a control de versiones, y reside en el servidor centralizado. 

o	log (Historial):

El comando git log es una herramienta básica de Git para explorar el historial del repositorio. Este comando se usa cuando necesitas buscar una versión concreta de un proyecto o saber los cambios que se introducirán mediante la fusión en una rama de función.

o	Conflicto (conflict):

Normalmente los conflictos surgen cuando dos personas han cambiado las mismas líneas de un archivo o si un desarrollador ha eliminado un archivo mientras otro lo estaba modificando. En estos casos, Git no puede determinar automáticamente qué es correcto.






3-	Explicar los siguientes estados de un fichero:

o	Sin seguimiento (no tracking):

Un archivo que no se ha preparado o confirmado.

o	Confirmado (commited file):

Es el fichero que ya está almacenado en el repositorio. La última versión y la copia local son iguales.

o	Modificado (modified file):

Es el fichero modificado en la copia local y existe una diferencia entre la copia local y la última versión en el repositorio. 

o	Preparado (staged file):

Es la copia del fichero modificado preparada para ser confirmada en la próxima operación de confirmación (COMMIT). La zona de preparación (staging area or index) contiene todos los ficheros preparados.

o	Ignorado (ignored file):

Un archivo que se le ha indicado expresamente a Git que ignore.

4-	Explicar las siguientes operaciones:

o	Clone (clonar):

Git clone se utiliza principalmente para apuntar a un repositorio existente y clonar o copiar dicho repositorio en un nuevo directorio, en otra ubicación.

o	Add (añadir):

 El comando git add añade un cambio del directorio de trabajo en el entorno de ensayo. De este modo, indica a Git que quieres incluir actualizaciones en un archivo concreto en la próxima confirmación.

o	Commit (confirmar):

El comando git commit captura una instantánea de los cambios preparados en ese momento del proyecto. Las instantáneas confirmadas pueden considerarse como versiones "seguras" de un proyecto: Git no las cambiará nunca a no ser que se lo pidas expresamente.





o	Push (enviar):

El comando git push se usa para cargar contenido del repositorio local a un repositorio remoto. El envío es la forma de transferir confirmaciones desde tu repositorio local a un repositorio remoto

o	Pull (traer):

El comando git pull se emplea para extraer y descargar contenido desde un repositorio remoto y actualizar al instante el repositorio local para reflejar ese contenido. La fusión de cambios remotos de nivel superior en tu repositorio local es una tarea habitual de los flujos de trabajo de colaboración basados en Git.

o	Fork (duplicar):

Es una de las operativas comunes con el trabajo en Git y GitHub. Básicamente sirve para crear una copia de un repositorio en tu cuenta de usuario.

o	Pull Request (entre repositorios):

Los pull requests son la forma de contribuir a un proyecto grupal o de código abierto.


5-	Nombrar al menos dos servicios de repositorio remoto para el control de versiones.

o	GitHub
o	GitLab
o	BitBucket

 
6-	Nombrar al menos un cliente gráfico para el control de versiones.

o	Gitg
o	Sourcetree
o	Gitblade

