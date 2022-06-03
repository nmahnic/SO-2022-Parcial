# SO-2022-Parcial
## Alumno: GONZALEZ, IGNACIO

1) Explicar Everything is a file
Este concepto proveniente de UNIX, nos muestra no solo recursos como texto, imagenes y codigo son archivos sino que también las acciones ejecutadas por el sistema operativo estan almacenados en directorios dentro de nuestra pc y se lanzan desde un archivo ejecutable o cual fuere necesario. 

    Adjunto un ejemplo de donde estan almacenados y como un comando lanzado de la terminal se muestra como un proceso.
    (https://github.com/IgnacioNicolasGonzalez/SO-2022-Parcial/blob/main/screen/ejemploPunto1.png
    https://github.com/IgnacioNicolasGonzalez/SO-2022-Parcial/blob/main/screen/ejemploPunto1bis.png)
*Bien 1*

2) ¿Que tareas desempeña el scheduler?
El scheduler que provee el sistema operativo se encargará de poner en cola el proceso solicitado por el usuario asignandole el CPU que utilizará para desempeñarlo, en qué momento debe ejecutarse con el fin de no pisarse con otros procesos y asi mantener el flujo de datos e información sin dañarse.
*Falta 0,25*

3) ¿Que información contienen los procesos?
Estos poseen la imagen del proceso el cual se compone de la pila, datos y código del mismo pero además nos almacena información del estado de nuestro CPU y datos del proceso que nos permiten rastrearlo como el PID (Process ID), PPID (Parent Process ID), el comando que lo ejecuto, etc.
(https://github.com/IgnacioNicolasGonzalez/SO-2022-Parcial/blob/main/screen/ejemploPunto3.png)
*Bien 1*

4) Crear nueva carpeta en el repo del parcial/code con holamundo en python y que sea ejecutable
(https://github.com/IgnacioNicolasGonzalez/SO-2022-Parcial/blob/main/screen/ejemploPunto4.png)
*Bien 1*

5) ¿Por qué no debemos cargar archivos compilados a github?
Los archivos compilados corren única y exclusivamente en la maquina donde fueron compilados por lo que tenerlo en un repositorio remoto carece de sentido y también sería incómodo ya que un archivo pesado por las librerias que lleva consigo.
*Mal la explicacion de la razon principal, tiene que ver con la arquitectura del procesador, no de la computadora 0*

6) Defina thread
La traducción de esta palabra seria hilo y ayuda a entender la definición porque son procesos que pueden estar ejecutandose utilizando más recursos para desprenderse del mismo y realizar mas tareas a la vez durante el mismo proceso.
*Mal 0*

7) ¿Por qué se reemplazo Assembler por C?
El lenguaje de programación assembler utilizado para desarrollar sistemas operativos fue cambiado por C debido a que el mismo compilaba a un nivel muy bajo y solamente podia ser reproducido por el CPU que cumplia los requerimientos por este lenguaje.

    C permitió el desarrollo de SO que podia ser corrido en varias maquinas gracias a que no estaba en contacto directo o tan bajo nivel del Hardware como su antecesor.
*Bien, capaz no es la mejor forma de decirlo pero esta bien 0.75*

8) ¿Cómo funciona la comunicación entre procesos?
La mayoría de los procesos tendran un PPID desde donde fueron lanzados los cuales le proveerán información tambien y podrán ser matados desde ahi. Pero luego estos seran totalmente independientes aunque hayan sido creados desde el mismo PPID, dos procesos no se comunican de manera natural sino que necesitaremos enviarle una señal con la acción que queremos que suceda.
Conociendo el PID del proceso con el que deseamos comunicarnos podriamos usar los comandos SIGSTOP, SIGINT, etc... por ejemplo y enviarles una señal de interrupcion y cancelación de la ejecución del programa.

    El comando pipe nos muestra de manera visual como podemos conectar dos procesos a través de la terminal.
    (https://github.com/IgnacioNicolasGonzalez/SO-2022-Parcial/blob/main/screen/ejemploPunto8.png)
*Bien 1*

9) ¿Que función cumple el SO?
El sistema operativo es la capa entre el hardware y las aplicaciones de usuario a las que tenemos acceso diariamente. 
Estas envían datos e instrucciones que son almacenados por el SO en la memoria RAM y luego utiliza el CPU para ejecutarlos de manera ordenada y segura para no saturarlo de procesos. 

    Por lo tanto, al abrir una aplicacion o archivo estamos moviendolo de su almacenamiento estándar o fijo (HDD, SSD) a la RAM y accede al espacio donde se encuentren los recursos necesarios para que el CPU lo procese despues de convertirlo en el código binario el cual es necesario para ser ejecutado por este componente.
*Bien pero falta la parte mas importante, ADMINISTRA esos recursos, los lista, los ejecuta en cierto orden, etc 0,25*

10) lista de algunos comandos y sus funciones: 

    - ls: lista el contenido del directorio
    - cd: nos permite navegar por los directorios
    - cp: copia un archivo o directorio
    - htop: muestra los procesos con su info en tiempo real
    - rm: elimina un archivo o directorio
    - mkdir: crea un directorio
    - man: nos provee el manual del comando que deseemos
    - ps: muestra un screen de los procesos en ese momento
    - grep: permite filtrar en el output de algun comando
    - nano: accede al archivo
    - gcc: compilador para correr archivos en c
    - clear: limpia la consola
*Bien 1*

*Maneja los conceptos y uso de consola, APROBADO 6,25*