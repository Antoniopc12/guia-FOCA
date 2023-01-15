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


### Chuleta de control de versiones con git

## 2. Comandos

### 2.1. Comandos básicos del terminal

Comando    | Argumentos              | Función 
-----------|-------------------------|------------
**pwd**    |                         | Muestra el directorio actual (Print Working Directory).
**mkdir**  | &lt;dir>                | Crea un directorio.
**cd**     | &lt;dir>                | Cambia de directorio (*'cd -': directorio previo*). Para ir a uno (o varios) atrás se pondrá cd ../.. (tantos pares de puntos como carpetas quiera ir atrás. Para ir varios adelante, se pueden enlazar las carpetas con /.
**ls**     | [-l] [-a]               | Muestra los archivos del directorio *(l: detallado; a: incluye ficheros ocultos).*
**rm**     | &lt;file>               | Elimina un fichero.
**mv**     | &lt;source> &lt;dest>   | Mueve o renombra un archivo. Source es el nombre del fichero a cambiar. En destino se especificará a dónde se quiere mover o el nombre nuevo del archivo o carpeta.

### Chuleta de control de versiones con git

## 3. Control de versiones locales

### 3.1. Comandos básicos del terminal

Comando           | Argumentos                                                                           | Función 
------------------|--------------------------------------------------------------------------------------|-----------------------------
**git init**      |                                                                                      | Al ejecutar este comando, se creará un nuevo subdirectorio .git en tu directorio de trabajo actual. También se creará una nueva rama principal..
**git add**       | &lt;file/files>                                				         | Prepara los archivos para ser confirmados en un repositorio local. Si hacer asterisco.formato, prepararás todos los archivos que sean de ese formato, y si directamente poner solo git add asterisco prepararás todo lo que haya en el directorio y que no se encuentre en el .gitignore (Pongo arterisco escrito porque el git detecta asterisco omo cursiva y no se ve).
**git commit**    | &lt; -m "(Información que quieras poner para identificar el commit)" [Puedes hacer -help para ver todos los argumentos] > | Confirma los cambios del repositorio local y agrega un mensaje informativo sobre el archivo.
**git reset**     |                                                                                      | Deshacer la operación de preparar.
**git reset**    	| &lt; --hard HEAD~1(Retrocedemos un commit y borramos los cambios)>    | Deshacer la operación de confirmar y retrocedemos un commit, borrando todos los cambios
**git reset**    	| &lt; --soft HEAD~1(retrocedemos un commit pero no perdemos los cambios y se quedan almacenados para un futuro commit) >                                                                                     | Deshacer la operación de confirmar pero no perdemos los cambios,quedandose almacenados para un futuro commit
**git status**    | 			                                                                     | Identificar el estado de un fichero o ficheros en un repositorio local
**git restore**   | &lt;Archivo>                                                  				   | Descartar los cambios de un fichero de trabajo mediante la recuperación de una versión almacendada en el repositorio local.
**git branch**    |                                                                			 | Muestra todas las ramas locales
**git branch**    | &lt;Nombre de la rama>                                                               | Crea una nueva rama local.
**git switch**    | &lt;Nombre de la rama>                                                               | Cambia a otra rama local.

### Chuleta de control de versiones con git

## Qué tenemos que saber hacer con Git (y GitHub)

### En el intérprete de comandos de git-bash
* Mostrar en qué directorio estamos.
* Crear un directorio.
* Cambiar de directorio.
* Mostrar la lista de ficheros de un directorio. 
* Borrar un fichero. 
* Cambiar (mover) un fichero de directorio. 


### Control de versiones centralizado:


## Configurar git para que trabaje tras un proxy:
* ***git config --global http.proxy  http://proxy.user:proxy.pass@proxy.name_or_ip:proxy.port***
*proxy.user* es el usuario que tiene permiso para acceder al proxy.
*proxy.pass* es la password de dicho usuario.
*proxy.name_or_ip* es el nombre DNS o la dirección IP de la máquina que hace de proxy de internet.
*proxy.port* es el puerto por el que se accede a comunicar con el proxy de internet.
*–global* le indica a git que la configuración es propia del usuario y sirve para todos sus repositorios.

* Para consultar el proxy configurado en git:
		***git config --global --get http.proxy***

* Para borrar el proxy configurado en git:
		***git config --global --unset http.proxy***


## Replicar un repositorio remoto localmente en nuestra máquina:
Clonar un repositorio extrae una copia integral de todos los datos del mismo que GitHub.com tiene en ese momento, incluyendo todas las versiones para cada archivo y carpeta para el proyecto hacia nuestra maquina local.
Para ello abriremos git-bash en el directorio que queramos clonar el repositorio e introducimos:

    git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY


## Replicar un repositorio local en un servidor remoto:
1. Creamos un repositorio en github.
1. Convertimos nuestro proyecto local en un repositorio git, para ello abrimos git-bash en el directorio deseado e introducimos: *git init*
1. Para añadir un repositorio remoto: *git remote add origin https://github.com/GitHub_UserName/Repository_Name*
1. Creamos una nueva rama y nos cambiamos a ella: *git branch -M main*
1. Añadimos los arcivos deseados: *git add nombre_proyecto*
1. Realizamos nuestro primer commit: *git commit -m "mensaje del commit"*
1. Hacemos push de todas las ramas a la main: *git push -u origin main*. 

## Traer los cambios de un repositorio remoto a un repositorio local:
En este caso tenemos dos posibles opciones en función de nuestras necesidades:
	
1. Clonar el repositorio con *git clone* (solo lo podemos hacer si es la primera vez).
1. En el caso de que ya tengamos un repositorio local clonado de uno remoto y queramos copiar los cambios del repo remoto a nuestro repo local para actualizarlo, haremos: *git pull origin BRANCH-NAME*

## Resolver los conflictos que se puedan producir al traerse estos cambios:
Puede haber solape entre lo que se cambió en el repo central y lo que nosotros hemos hecho en local, esto crea un conflicto al hacer el "pull".
La solución:
1. Hacer:  *git stash save* (stash nos permite guardar los cambios locales que no pasamos a commit en un universo medio paralelo)
1. Hacer ahora: *git pull*
1. Finalmente: *git stash pop*

## Enviar los cambios de un repositorio local a uno remoto:
Los pasos a realizar son tres:

1. *git add Archivo_o_Carpeta*
1. *git commit Archivo_o_Carpeta -m "Mensaje explicativo"*
1. *git push*

Es posible que al hacer un commit nos de un error por no estar identificados, en ese caso introduciremos:

* *git config --global user.name NombreDeUsuarioGit*
* *git config --global user.email NuestroCorreoGit@correo*

También podemos comprobar el estado del repo antes y despues de la operación con *git status*

## Enviar una rama local al repositorio remoto:
En este caso suponemos que hemos estado trabajando en una rama y llega el momento de subir nuestro trabajo al repo remoto,
para esto, suponemos que ya se han hecho todos los adds y commits de manera local, entonces introducimos:
* *git push -u origin nombre_de_la_rama*

Si queremos enviar todas las ramas de nuestro repo local al remoto:
* *git push --all -u*

En caso de que a rama no esté creada en el repo remoto todavía:
* *git push --set-upstream origin nombre_rama*

## Incorporar a ramas locales cambios que se producen en el repositorio remoto:
Usaremos : *git pull origin nombre_rama_remota*

## Realizar un pull request entre dos ramas de un repositorio remoto:
Es necesario para esto que hayamos hecho cambios en las ramas:
VAmos a github, entramos en el repositorio->code->branch->pull request (ver figura 1)
![Figura ](/pullrequest.png)
