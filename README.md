# SO-2022-Parcial
## Alumno: Delfino, Brian

1) ¿A que se debe el termino "Todo es un archivo"?
Para esta pregunta vamos a usar la imagen todoesunarchivo.png (carpeta "screen"). En ella observaremos varios archivos que se encuentran dentro del storage: particiones de disco (sda1/sda2/etc)hasta por ejemplo sectores del procesador (cpu, core,etc). 
*La explicación es un poco vaga, de hecho no se encuentra en el storage, es una represetnación virtual de hardward mapeado a memoria 0*


2)¿Cual son las funciones que realiza un sistema operativo?
Un sistema operativo (SO)es el intermediario entre el usuario (mediante el teclado,monitor,mouse) y un software. Este nos dará los permisos necesarios para: buscar, por ejemplo, un archivo en el storage, pausar un proceso para realizar otro, instalar programas, crear archivos,etc.
*Pregunta muy amplia y la respuesta muy escueta 0*

3)¿Qué es el Kernel y para que sirve?
Kernel es el sector e n donde se "hospeda" el SO dentro de la la memoria volatil, más conocida como RAM. Este mismo se aloja al instante en cuanto prendemos la PC. el mismo tiene su sector de pila, datos y proceso. luego de esta división queda libre un sector para el usuario, para poder guardar los demás procesos que haga. 
*El kernel no es un sector, es parte del sistema operativo, si se hospeda en RAM 0,25*

4)¿Para qué sirve el comando "htop"?
Este comando sirve para poder observar todos los procesos que se estan realizando en ese instante. 
Como se puede observar en la imagen (htop.png dentro de la carpeta Screen), se puede observar los nucleos del procesador, como tambien la memoria y como tambien procesos (la activacion del screenshot)
*Bien 1*

5)Breve explicación de la creación de los compiladores.
Los compiladores surgen de una problematica. Al principio para cada procesador se debia utilizar el Assembler (lenguaje de nivel alto), el cual era muy dificil de programar y  el cual demandaba mucho tiempo. EN 1991, llega Linux siendo un sistema operativo mas amigable de programar y por ultimo surge el lenguaje C (bajo nivel).
Gracias a estos dos ultimos surgimientos se era mas sencillo generar un compilador para cada procesador, utilizando C, que realizar un programa en Assembler para cada CPU (procesador).
*NO, C viene 20 años antes de Linux, assemble tambie usa compilador se llama nasm, 0*

6)¿Qué diferencia hay entre "htop" y "ps -ely"?
Ambos comandos realizan la misma funcion: mostrar los procesos que se estan ejecutando. La diferencia es que el ps -ely realiza una captura y en cambio el htop siguen corriendo varios procesos. Tambien podemos ver en la imagen (psely.png en la carpeta screen) que no podemos ver los nucleos del procesador en acción. Por ultimo podemos servir realizando codigos en la misma terminal, en cambio con el  otro comando deberiamos abrir otra terminal para seguir "codeando".
*Bien, 1*

7)Realizar desde la terminal, un archivo en .md y explicar sus pasos.
 Primero entramos en la terminal y buscamos la carpeta en donde queremos crear el archivo (../SO-2022-Parcial/code).Podemos usar el comando ls por si no recordamos el nombre de la carpeta a buscar.
 Una vez dentro de la carpeta, utilizamos el comando nano, el cual se utiliza para crear archivos. Le damos un nombre al mismo, en este caso prueba.md.
Dentro del mismo, generamos todos lo que haya que hacer y para guardar se utiliza el ctrl+o y cerramos con ctrl+x.
Y listo, tenemos el archivo guardado dentro de la carpeta. 
En la carpeta "code" se podrá ver el prueba.md y en código.png se puede ver los pasos realizados.
*La explicación de pasos dice "hacer todo lo que haya que hacer", no me explicas como hacerlo, 0*

8)Proceso ¿Qué es? ¿Y que puede hacer el SO con un proceso?
Un proceso, en el área de la programación, es una acción que se está realizando: tomemos como ejemplo un archivo Word.
Cuando vamos a crear un archivo Word, le pedimos al sistema operativo que busque en el HDD el archivo Word y lo guarde a un sector de la RAM. Eso es un proceso.
Este mismo queda activado o corriendo, generando espacio en la RAM y que el procesador realice más cálculos. 
El sistema operativo, si ve que el proceso no se esta usando o esta en segunto plano por mucho tiempo, puede borrarlo para darle prioridad a otro proceso que se este ejecutando en ese momento.
*Bien, pero no es buen ejemplo. 0,5*

9)

10)


*Falta profundizar los temas, EN PROCESO, 2,75*