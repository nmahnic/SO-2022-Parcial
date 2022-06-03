# SO-2022-Parcial
## Alumno: Recalde, Alejandro

### 1) Explique los pasos a seguir para subir un archivo o cambios a un reposiorio de Git.

- Creamos nuestro repositororio en Github. -> '../screen/creando-repo.png'

- Clonamos el repositorio que creamos anteriormente a nuestra pc. -> '../screen/git-clone.png'

- Creamos por ejemplo un archivo README.md y guardamos el cambio. -> '../screen/readme.png'

- Con git status vemos los archivos modificados. -> '../screen/cambio.png'

- Con el comando git add "nombre del archivo" agregamos el archivo modificado para luego subirlo. -> '../screen/git-add.png'

- Con el comando git commit -m "firt commit" hacemos nuestro commit describiendo el cambio realizado -> '../screen/commit.png' 

- Con el comando git branch -M main especificamos nuestra rama de trabajo, en este caso "main" -> '../screen/rama.png'

- Por ultimo con el comando git push -u origin main subimos el archivo o cambios que hicimos a nuestro repositorio -> '../screen/git-push.png'
- Entramos a github y verificamos nuestros cambios -> '../screen/verificacion.png'
*Bien 1*

### 2) ¿Que podemos ver con el comando ps -ely?

- Con este comando podemos ver: -> '../screen/procesos.png'

    - UID: Este es el usuario que ejecuta el proceso.
    - PID: El id del proceso.
    - PPID: El id del padre del proceso ejecutado.
    - C: El uso del CPU.
    - PRI: La prioridad de los procesos.
    - CMD: El comando ejecutado para crear el proceso.
*Bien 1*

### 3) ¿Que recursos administra el SO?

- Los recursos que administra el Sistema Operativo son el CPU, la Memoria y los dispositivos de Entrada y Salida
*Simple pero correcto, 0,25*

### 4) Explique los siguientes comandos de linux: mkdir, cd y ls.

- mkdir: Este comando lo utilizamos para poder crear nuevos directorios.
- cd: Nos permite poder navegar entre directorios. 
- ls: Nos lista todos los directorios/archivos que tenemos dentro de donde estamos parados
- A continuacion podemos ver estos tres comando en uso -> '../screen/comandos.png'
*Bien 1*

### 5) "Every is a File". ¿Donde podemos encontrar a los dispositivos de Entradas y Salidas? ¿Como podemos acceder a ellos?

- A estos dispositivos los podemos encontrar en el directorio /dev -> '../screen/dispositivos.png' 
- Podemos acceder a ellos con los siguientesde la siguiente forma:

    - OPEN: Lo obtenemos.

    - READ: Lo leemos.

    - WRITE: Le enviamos informacion. 

    - IOCTL: Accedemos a su configuracion.
    
    - CLOSE: Una vez que terminamos lo devolvemos y liberamos el recurso usado.
*Bien 1*

### 6) ¿Que hace la CPU?

- La CPU lo que hace, a travez de 0 y 1 es recibir y ejecutar operaciones. Y es la unica en ejecutar procesos.
*Simple pero correcto, se puede desarrollar más 0.25*

### 7) ¿Porque no se pueden subir archivos compilados a git?

- No se pueden subir archvios compilados a git porque donde se compila ese archivo, es decir, en la computadora que lo hace no va a ser igual a ninguna otra. Lo que pasaria si bajamos ese archivo es que no nos funcione. Ademas este seria muy pesado.
*La razón princial esta mal explicada 0*

### 8) ¿Quienes son los usuario de los recursos del SO?

- Los usuarios de estos recursos son los procesos o tareas. Estos son los programas que se encuentran ejecutando en la memoria del sistema.
*Bien 1*

### 9) ¿Que es htop?

- Htop es un programa que se ejecuta directamente de la consola de linux, este nos muestra los procesos que estan corriendo en el sistema operativo en tiempo real. -> '../screen/htop.png'
*Bien, pregunta algo simple 0,5*

### 10) Enumere los espacio que hay en la memoria:

- Pila.
- Codigo.
- Datos
*Bien pero simple 0,25*

*Tiene manejo de los conceptos y uso de la consola, APROBADO, 6*