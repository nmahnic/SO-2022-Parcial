# SO-2022-Parcial
## Alumno: DELFINO JIMENEZ, Damian Ezequiel

1) ###

2) ###

3) ###

4) ### 

5) ### ¿Como es el proceso de abrir un archivo?

    El usuario, mediante el teclado (hardware), manda la indicacion al sistema operativo para abrir un archivo. El SO envia la señal a la memoria RAM para que abra un espacio y este le pide al storage la pila (en primer lugar), variantes y codigo del archivo solicitado y pueda pasar a "ready" y asi empezar a actuar.
*Si bien faltan pasos es medianamente correcto 0,5*

6) ### ¿Porque `Assembler` fue reemplazado por `C`?

    Esto se debio a que, en Assembler, su codigo fue escrito para cada procesador en especifico, y a la hora de salir un nuevo procesador, tenian que hacer de nuevo todo el codigo del sistema operativo, uno para cada procesador. A esta solucion aparecio C, que es un lenguaje de bajo nivel, al igual que Assembler, pero cuenta con un compilador para cada procesador, generando que sea el mismo codigo en C para todos los procesadores, solo lo que cambiaria seria el compilador.  
*Bien 1*
    
7) ### ¿Porque no es optimo subir a GitHub un archivo compilado?

    No es optimo subir en GitHub un archivo compilado, debido a, como aclaramos en el punto 6, cada procesador tiene su compilador, esto hace que cada computadora sea distinta y no corra el mismo programa en todas las computadoras, ya que estas pueden tener distintos sistemas operativos. Tambien el archivo compilado es muy pesado debido a que tiene varias bibliotecas instaladas. Por esto, lo mas optimo es subir solo el archivo sin compilar, para ser mas liviano y que cada usuario pueda compilar el archivo en su sistema operativo y con su procesador designado.
*Bien, parcialmente, la cuestion es si tiene el mismo procesador 0,5*

8) ### ¿Que significa que "TODO ES UN ARCHIVO"?

    Esto hace alusion que en Linux, los recursos del hardware (CPU, perifericos, etc) estan en bytes, pudiendo acceder a estos mismos como archivos. Esto facilita la comunicacion del sistema operativo y del CPU de forma directa.
    Se puede ver esto entrando a los dev donde estan todo esto en forma de archivos.

    [screen: dev.png y dev-las.png]
*Bien 1*

9) ### Nombre algunos comandos basicos de la terminal de `Linux`

    - cd = sirve para moverse dentro de los directorios
        - cd .. = es para dirigirse un directorio para arriba  
        - cd - = es para volver al ultimo un directorio
    - ls = sirve para listar el directorio donde estas parado y mostrar su contenido
        - ls -las= te muestra no solo los atchivos y directorios de donde estas, si no sus caracteristicas
        - ls -a = te muestra tambien los archivos ocultos
    
    - mkdir = sirve para crear un directorio nuevo
    
    - mv = sirve para mover de un directorio a otro un archivo o cambiarle el nombre
    
    - rm = sirve para borrar un directorio vacio o archivo
    -rmd = sirve para borrar un directorio completo
    - nano = sirve para editar un archivo, si no existe crea uno con el nombre solicitado
    - gcc = es el compilador de C
    - htop = es el administrador de tarea, te muestra los procesos que se estan ejecutando en vivo
    - ps -ely = es una impresion de los procesos que se estan ejecutando
    - kill = es para mandar una señal que sirve para cerrar un proceso
        - kill -15 "PDI proceso" : envia una señal de cierre no forzado, pide "permiso" para terminar el proceso
        - kill -9 "PDI proceso": envia una señal para cerrar determinadamente el proceso.

    [screen: punto9_...]
*Bien 1*

10) ### Ejemplifique como subir un repositorio a `GitHub` desde consola

    `Primer paso`= se crea un repositorio en GitHub

    `Segundo paso`= el repositorio nos entrega una url

    `Tercer paso`= hacemos git clone "url" - esto crea la carpeta del repositorio en nuestra maquina

    `Cuarto paso`= una vez finalizada nuestra tarea ponemos git add . - guarda todos los archivos para subirlos a la nube
        con git status muestra el estado de los archivos, en verde si los archivos fueron agregados, en rojo no
    
    `Quinto paso`= git commit "..." hacemos un comentario explicando lo que hicimos
    
    `Sexto paso`= git push origin master - "pusheamos" o subimos lo que hicimos a nuestro repositorio en GitHub, si lo subimos a un repo que no creamos nosotros, en vez de MASTER iria MAIN
        Nos va a pedir nombre de usuario y contraseña/token para subirlo
    

    [screen: punto10_...]
*Bien 1*

*Si bien falta manejo de algunos concpetos supiste demostrar los conocimientos del uso de consola, APROBADO, 5*