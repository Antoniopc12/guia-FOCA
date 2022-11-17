### Chuleta de control de versiones con git

## 3. Control de versiones locales

### 3.1. Comandos básicos del terminal

Comando           | Argumentos                                                                           | Función 
------------------|--------------------------------------------------------------------------------------|-----------------------------
**git init**      |                                                                                      | Al ejecutar este comando, se creará un nuevo subdirectorio .git en tu directorio de trabajo actual. También se creará una nueva rama principal..
**git add**       | &lt;file/files>                                				               | Prepara los archivos para ser confirmados en un repositorio local.
**git commit**    | &lt;Hacer -help para ver todos los argumentos (Nosotros estamos usando -m "Mensaje"> | Confirma los cambios del repositorio local y agrega un mensaje informativo sobre el archivo.
**git reset**     |                                                                                      | Deshacer la operación de preparar.
**git reset**    | &lt; --hard HEAD~1 (Retrocedemos un commit y borramos los cambios) ; --soft HEAD~1 (retrocedemos un commit pero no perdemos los cambios y se quedan almacenados para un futuro commit)>                                                                                     | Deshacer la operación de confirmar.
**git status**    | 			                                                                     | Identificar el estado de un fichero o ficheros en un repositorio local
**git restore**   | &lt;Archivo>                                                  				   | Descartar los cambios de un fichero de trabajo mediante la recuperación de una versión almacendada en el repositorio local.
**git branch**    | &lt;Nombre de la rama>                                                               | Crea una nueva rama local.
**git switch**    | &lt;Nombre de la rama>                                                               | Cambia a otra rama local.
