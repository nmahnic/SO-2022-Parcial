# SO-2022-Parcial
## Alumno: APELLIDO, Nombre

1)enlista comandos que puedas usar en linux
- cd, se usa para moverte entre directorios 
-mkdir, crea una carpeta
-ls, para enlistar
-touch, crear un archivo
-ps, enlista procesos activos actualmente
-grep filta segun lo que pongas
*Bien, podria haber explicado un poco más, incluso usando ejemplos 0,75*

2)explica con tus palabras un proceso
un proceso basicamente son ordenes que recibe un procesador con un conjunto de variables y devuelve un resultado
*Muy basico 0,1*

3) en clase hablamos de pila datos y codigo que son?
al ejecutar un proceso se le asigna un espacio en la ram, dentro de este espacio asignado a este proceso individual se divide en 3:
pila se encarga de hacer los intercambios necesarios
datos almacena los variables que va a utilizar
codigo es la serie de acciones a realizar
*Bien 1*

4)partes de una computadora
memoria : Ram se va a encargar de ser el espacio de intercambio de datos para ejecutar los distintos procesos
procesador : va a recibir ordenes variables y devolver algo
storage : discos de almacenamiento va a guardar todos los archivos y programas(que tambien son archivos)
dispositivos de entrada y salida: perifericos(monitor, mouse, teclado, etc)
*Y el sistema operativo donde va? 0,5*

5)pipe que es y como se usa
pipe se usa para que un proceso reciba como variable el resultado de otro proceso ej
ps -a | grep $USER
*Bien 1*

6)scheduler que hace
en pocas palabras dentro del sistema operativo es el encargado de dar un orden a los distintos procesos que se quieren ejecutar, dar prioridad y o establecer en cuanto tiempo va a ejecutarse 
*Lo que dice es correcto pero le falta 0,25*

7) comandos git enumera y explica
git init crea repo
git clone url busca un repo de la url y te hace una copia de los archivos
git add . prepara los archivos nuevos o  que fueron modificados y prepara para subirlos
git push sube los archivos y actualiza el repo
*Bien, podria haber ejemplo 0,75*

8) que cambio trajo c
antes se creaba de cero sistema operativo por procesador con la llegada de c simplifica este proceso y solo se hace las ordenes para c haga funcionar todo y sea mas sencillo 
*Y el compilador de C? 0,5*

9)compilado vs interpretado
las 2 buscan lo mismo que el procesador ejecute una accion en concreto, pero cada lenguaje eligio(al crearlo) hacerlo de distinta manera. compilado, vos escibis tu programa y tenes que a travez de un compilador traducir esas ordenes a un idioma que el procesador entienda. el interprete hace que tu programa esta escrito en un lenguaje que el interprete se va a encargar de traducir de forma adecuada a un lenguaje que sea posible ejecutar. 
*Falta 0,5*

10)con tus palabras explcia el concepto "todo es un archivo"
basicamente la idea es que entre todas las posibles acciones que es capaz de realizar la computadora ej la consola, monitor, storage, etc, hay un archivo que guarda como administrarlo o como ejecutarlo.
*Bien 0,75*

*Maneja los conceptos, APROBADO, 6,1*