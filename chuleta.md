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


### Configurar git para que trabaje tras un proxy:
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


### Replicar un repositorio remoto localmente en nuestra máquina:
Clonar un repositorio extrae una copia integral de todos los datos del mismo que GitHub.com tiene en ese momento, incluyendo todas las versiones para cada archivo y carpeta para el proyecto hacia nuestra maquina local.
Para ello abriremos git-bash en el directorio que queramos clonar el repositorio e introducimos:

    git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY


#### Replicar un repositorio local en un servidor remoto:
1. Creamos un repositorio en github.
1. Convertimos nuestro proyecto local en un repositorio git, para ello abrimos git-bash en el directorio deseado e introducimos: *git init*
1. Para añadir un repositorio remoto: *git remote add origin https://github.com/GitHub_UserName/Repository_Name*
1. Creamos una nueva rama y nos cambiamos a ella: *git branch -M main*
1. Añadimos los arcivos deseados: *git add nombre_proyecto*
1. Realizamos nuestro primer commit: *git commit -m "mensaje del commit"*
1. Hacemos push de todas las ramas a la main: *git push -u origin main*. 

#### Traer los cambios de un repositorio remoto a un repositorio local:
En este caso tenemos dos posibles opciones en función de nuestras necesidades:
	
1. Clonar el repositorio con *git clone* (solo lo podemos hacer si es la primera vez).
1. En el caso de que ya tengamos un repositorio local clonado de uno remoto y queramos copiar 
los cambios del repo remoto a nuestro repo local para actualizarlo, haremos: *git pull REMOTE-NAME BRANCH-NAME*

#### Resolver los conflictos que se puedan producir al traerse estos cambios:

### Enviar los cambios de un repositorio local a uno remoto:
Los pasos a realizar son tres:

1. *git add Archivo_o_Carpeta*
1. *git commit Archivo_o_Carpeta -m "Mensaje explicativo"*
1. *git push*

Es posible que al hacer un commit nos de un error por no estar identificados, en ese caso introduciremos:

* *git config --global user.name NombreDeUsuarioGit*
* *git config --global user.email NuestroCorreoGit@correo.com*.

También podemos comprobar el estado del repo antes y despues de la operación con *git status*

### Enviar una rama local al repositorio remoto:
En este caso suponemos que hemos estado trabajando en una rama y llega el momento de subir nuestro trabajo al repo remoto,
para esto, suponemos que ya se han hecho todos los adds y commits de manera local, entonces introducimos:
* *git push -u origin nombre_de_la_rama*

Si queremos enviar todas las ramas de nuestro repo local al remoto:
* *git push --all -u*

En caso de que a rama no esté creada en el repo remoto todavía:
* *git push --set-upstream origin oscar*

### Incorporar a ramas locales cambios que se producen en el repositorio remoto:
Usaremos : *git pull origin nombre_rama_remota*

### Realizar un pull request entre dos ramas de un repositorio remoto:
Es necesario para esto que hayamos hecho cambios en las ramas:
VAmos a github, entramos en el repositorio->code->branch->pull request (ver figura 1)
![Figura ](/pullrequest.png)
