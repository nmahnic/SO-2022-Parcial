# SO-2022-Parcial
## Alumno: RICHARD, Agustín

1) ¿Por qué los fabricantes de procesadores se esmeran tanto en agregar más caché a los procesadores en cada generación?

    Con la tecnología actual, realizar la "simple" tarea de hacer operaciones lógicas no es problema para los procesadores, el cuello de botella que encuentran los sistemas hoy en día está en el tiempo de acceso a la memoria, tanto para su lectura como escritura. Esto ocurre a tal nivel que resulta sustancial para los fabricantes de chips acercar tan solo unos milímetros la memoria al procesador.
Los fabricantes han estado incorporando memorias caché ultra rápidas (y ultra caras) lo más cerca posible del procesador para que este pueda tener acceso veloz a la información más importante. Esta única acción produce aumentos considerables de rendimiento. 

2) ¿Por qué se dice que en Linux "todo es un archivo"?

    Cuando Linux Torvald creó el so Linux lo hizo basándose en Unix, que ya empleaba el concepto de todo es un archivo. Linux introduce una manera de tratar archivos como streams de bytes y los archivos pueden ser abiertos, que no es otra cosa más que mover el archivo de la memoria donde es persistido (un hdd, un sdd), a la memoria ram, donde se lo podrá leer y escribir. En Linux ciertos espacios de la memoria ram están mappeados directamente al hardware. Escribir en el espacio mappeado al monitor de manera correcta desembocará en la aparición de letras en pantalla. Leer el buffer que genera la entrada del teclado en su espacio de memoria mappeado nos mostrará las úlltimas teclas apretadas. Entonces, si poseemos una abstracción provista por los drivers para abrir, leer y escribir el hardware, ¿cual es la diferencia con un archivo que también se puede abrir y también en la memoria ram leer y escribirlo? Ninguna, al menos para los ojos del usuario tratar con un archivo y tratar con el hardware será lo mismo. 

3) ¿Qué es un sistema operativo?
    Una máquina de escritorio con todos sus periféricos conectados, pero sin un software que coordine el acceso de estos al procesador, a la memoria, a la red, es inútil. Un sistema operativo es un planificador de procesos.  El sistema operativo es el proceso principal, tiene acceso absoluto, se comunica directamente al hardware mediante los drivers, tiene un espacio de memoria privado al que los procesos normales no pueden acceder. El so se encarga de las tareas principales como la seguridad, el gestionamiento de red, el acceso a memoria, se debe encargar de coordinar el uso de los recuros para que distintos procesos no se pisen al querer acceder a ellos.
    El sistema operativo tiene su propio espacio de memoria con su propia pila dentro de lo que es llamado el Kernel Space.
    El so se encarga de asignarle a los procesos tiempo de uso del procesador, de considerarlo pertinente, el so cortará el uso del cpu desde un proceso y lo mandará a volver a esperar a la fila de procesos que le solicitaron al so uso del cpu. Si un proceso es privado de continuar usando el procesador, el sistema operativo sacará una "screenshot" del estado que tenía el proceso en el procesador para que pueda retomar desde ahí cuando vuelva ser su turno.
    

4) ¿Qué es un proceso? 

    Un proceso es estado de ejecución de un programa. Los procesos poseen un espacio reservado en memoria al que solo pueden acceder ellos y el sistema operativo, no otros procesos. En este espacio de memoria en la ram cada proceso tendrá su id, el id de su proceso padre, el código, archivos necesarios para su ejecución, variables constantes y una pila, que será toda la memoria visible para el proceso. Para el proceso el primer lugar de memoria de la pila será la "dirección 0" por más que visto desde afuera no lo sea, por lo que directamente no sabrá como acceder a otras partes de la memoria que no se encuentren en el stack. Los procesos solicitan al so tiempo de uso del procesador cuando lo necesitan, se quedan en estado de espera cuando están esperando la liberación de un recurso o a la espera de un evento (como que llegue un paquete a un puerto http) y al salir de este estado vuelven a la lista de espera de uso del procesador. Los procesos pueden recibir entradas y generar salidas.

5) ¿Qué es una system call? Dar ejemplos
    
    Las system call son una especie de interfaz o api que ofrece el so, con estas se le pueden ejecutar pedidos al so para realizar acciones para las cuales solo él tiene acceso.
    Los procesos pueden hacer pedidos desde el user space al kernel space mediante las system call, para que luego el so con su acceso total, y en caso de que lo considere correcto lo haga. En caso de que un proceso quiera acceder al espacio de memoria de otro tmb dentro del user space (a no ser que sean threads que comparten memoria), debe pedirselo al so. Hay muchas system calls, dos ejemplos son las que piden matar o terminar un proceso. La diferencia entre matar y terminar un proceso con una system call está en que una call de matar irá directamente al proceso cuyo process id fue previsto en la llamada, lo sacará del uso del procesador si lo estaba usando y limpiará el espacio de memoria que estaban usando dejándolo libre para que el so lo use por ejemplo asignándoselo a otro proceso. En cambio una system call de pedido de terminar primero consultará al so si puede finalizar el proceso, en caso de no ser rechazado le pedirá al proceso que inicie un proceso de finalización limpia, en el que el proceso se tomará su tiempo para terminar todo lo que sea vital en el procesador, y guardar limpiamente los últimos cambios, tal vez por ejemplo escribiendo un archivo, guardando y devolviéndolo a la memoria de largo plazo.
    Si vemos dos htop corriendo en dos terminales distintas, agarrásemos sus pid y a uno hicieramos una syscall de kill el htop quedaría congelado en la terminal, mientras que le proceso al que se le pidió finalizar veríamos como cierra la consola.

6) ¿Es correcto subir a un sistema de control de versiones un archivo compilado?

    Sería un error por dos razones, la primera es que un archivo compilado es mucho más pesado, por lo que teniendo el código que se puede compilar es ocupar espacio en el servidor de forma innecesaria.
    La segunda y más importante es que el archivo compilado fue compilado específicamente para mí pc, no podrá correr en otras.
    El proceso de compilación es el "traducir" el código de un lenguaje de programación a código binario que es lo único con lo que puede trabajar el procesador. Distintos lenguajes encaran esta traducción de forma diferente. C se introdujo como el reemplazo de assembler por presentar un compilador, con lo que se obtiene acceso desde el lenguaje a interfaces que te permiten abstraerte de como se maneja la memoria entre otras cosas. Así la tarea pasa de tener que escribir un sistema operativo para cada procesador nuevo, a tener que escribir solo un nuevo compilador para cada arquitectura de procesadores distinta.
    Otro approach común son los lenguajes interpretados que van on runtime traduciendo linea a linea el código transformandolo en binario, como python.
    También hay rarezas como la máquina virtual de java, donde un código java se compila a bytecode, que es lo que recibe la javaVM y se encarga de compilar a binario para cada dispositivo. 

7) ¿Qué es un StackOverflow Exeption?

    El stack se maneja con LIFO, lo último que se mete en la pila es lo primero que sale, porque la pila esta pensada para información a la que se quiere acceder a la brevedad. El tamaño de la pila es limitado, por lo que en caso de por ejemplo descuidos al momento de programar podría generarse una referencia circular, una función que se llame infinitamente a si misma sin un caso de quiebre, irá almacenando en cada llamada la dirección en el stack de la función que la llamo a ella y el valor de los parámetros con los que lo hizo, por lo que es obvio que llegará el punto en el que el espacio finito del stack sea excedido y se genere la exeption.

9) ¿Que comandos de Linux son necesarios para llevar de inicio a fin la creación de un HolaMundo en java?
    Con ls uno puede ver que carpetas y archivos se encuentran en el directorio en el que está parado, con cd moverse al directorio que desee, ahí con mkdir crear una nueva carpeta, entrar, con por ejemplo nano crear un archivo java, dentro codear el HolaMundo, guardar, salir, con javac compilar el archivo, y con java + nombre del archivo correr el programa.

10) ¿Cómo se crea un nuevo proceso?

    Todo nuevo proceso nace de un proceso padre del cual se hace un fork, el fork es una especie de división como la que hacen las células para reproducirse, a partir del proceso padre se generan dos procesos idénticos excepto en sus pId, ppId y el espacio de memoria que ocupan.

11) ¿Como pueden comunicarse dos distintos programas codeados en distintos lenguajes?

    Hay varias maneras, dos de estas son los pipes y los puertos.
    Un pipe agarrará la salida de un programa y se lo pasará como parámetros de entrada a otro programa, esto de forma agnóstica al lenguaje, mediante el STIN y STOUT.
