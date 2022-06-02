# SO-2022-Parcial
## Alumno: PACIFICO FERREIRA, Nicolas Rubén

1) **¿Qué función cumple la CPU en una computadora?**

1. La CPU es el único componente capaz de recibir datos y con ellos ejecutar procesos (siempre en lenguaje binario) para devolver la información o el resultado correspondiente.

2) **¿Qué significa "abrir" y "cerrar" un archivo o aplicación?**

2. En el momento donde decidimos abrir un archivo o aplicación, estamos llamando al Sistema Operativo y solicitando que lo "mueva" del storage a la RAM para que pueda ejecutarse y/o modificarse. Una vez realizada la tarea deseada, al cerrarlo, volverá al storage. Ésto es debido al tipo de funcionamiento de ambos componentes, es por eso que al tener mas RAM, las computadoras pueden realizar mas tareas al mismo tiempo-

3) **A grandes rasgos, ¿De qué modo se relaciona un Sistema operativo con las aplicaciones y el Hardware?**

3. Para que una aplicación o archivo se abran, primero debemos entender que nunca es SOLO ESO lo que se está ejecutando. Por ejemplo, el sólo prender la computadora significa que se empezarán a utilizar varios procesos, tales como el uso de la pantalla, mouse y teclado, en algunos casos un antuvirus, por ejemplo, la utilización del wifi, etc. Por lo que el usuario no es únicamente quien decide que aplicaciones/procesos se ejecutan. Esa función también está a cargo del Sistema Operativo, ya que es quien decide el orden de prioridades de los procesos a ejecutar y cuando hacerlo (y cuando no tambien, ya que también puede solicitar cerrarlo o decidir "matarlo" en algunas ocaciones). Para que una computadora, por ejemplo, funcione, el Sistema Operativo debe administrar y decidir cuándo un proceso puede iniciar y qué parte del hardware utilizará, como si fuera un Director Técnico decidiendo qué cambios hacer y en qué posición jugarán los jugadores. Al fin y al cabo, es el S.O. quien decide si finalmente "deja" al usuario realizar las peticiones de abrir o no una app y que recursos utilizaran éstas.

4) **¿Qué beneficios trajo el lenguaje C en relación a Assembler?**

4. Assembler es uno de los lenguajes de mas bajo nivel existentes, que posee la particularidad de interactuar directamente con el hardware de la computadora, por lo que también resulta eficiente a la hora de ser ejecutado. Sin embargo, al tener la particularidad de interactuar con el hardware, surge la dificultad de que cada computadora con apenas una mini diferencia en sus componentes debe tener que tener un código entero propio para funcionar. Cuando el lenguaje C (también un lenguaje de muy bajo nivel) apareció en escena, tuvo la distinción de que no interactuaba directamente con el hardware, si no que éste era compilado para poder ejecutarse. En el caso de C, un mismo código podía funcionar más de una computadora aunque su hardware no fuera el mismo. En el caso de que una computadora tuviera otro procesador, aún se mantiene el mismo código de C, solo que debe modificarse el compilador.

5) **Suponiendo que estás en Github viendo el código de un examen y querés completarlo para subirlo a tu repositorio, ¿Cuáles son los pasos que debés seguir?**

5. Lo primero que debemos hacer es click en el botñon *Code* verde y copiar el link que aparece (De acá en adelante se puede cerrar el navegador si así lo deseás). Luego debés " *forkear* " (descargar) el repo en tu computadora con el código "```git clone www.github.com/etc```. Luego, una vez cargado, podemos modificarlo a nuestra necesidad. Una vez realizados los mismos, colocamos ```git add . ``` (el punto significa que agregue todos) y ``` git commit -a ``` para agregar los cambios realizados. Finalmente, colocamos ``` git push origin master ``` para enviar nuestro examen a github. Luego de este último comando, se solicitarán los datos de nuestra cuenta de Github para que el nuevo repo se suba a nuestra cuenta.

En el caso de que deseemos subir una carpeta de nuestra computadora a git, el comando a realizar es ``` git init ``` y el directorio en donde nos encontremos será el nuevo repositorio.

6) **¿Cuáles son los comandos mas utilizados en este primer cuatrimestre para navegar entre directorios y qué variaciones tienen?**

6. Primero, para saber qué directorios o archivos hay donde estamos parados, colocamos ``` ls ```, si deseamos entrar en un directorio existente, entramos con ``` cd NombreDirectorio ```, en el caso de que queramos crear uno nuevo, lo haremos con ``` mkdir ``` y, en el caso de que hayamos entrado a uno por error, podremos "ir para atrás" con la opción ``` cd .. ```. También, en caso de que ya sepamos en qué ubicación queremos estar, en vez de avanzar directorio por directrio podemos escribir ``` cd ruta/completa/NombreDirectorio ```. Suponiendo que en donde estamos queremos eliminar un archivo o directorio vacío, colocaremos ``` rm nombreArchivoODirectorio ```, en el caso de que el directorio tenga contenido en su interior y querramos borrarlos todos, usaremos ``` rm -dr NombreDirectorio ```, y si queremos borrar parte de su contenido de una manera un poco mas rápida que borrando uno a uno colocando siempre el mismo código, usaremos ``` rm -r NombreDirectorio``` ya que así, la terminal nos pregunta uno por uno si deseamos eliminar los archivos en su interior. Si elegimos la opción de eliminar los archivos de un directorio con ``` rm - r NombreDirectorio ``` y ya sabemos que borramos los que queríamos pero aún siguen apareciendo las opciones de otros archivos, podemos cortar el proceso que la terminal está realizando con CTRL + C.

7) **¿Cómo ejemplificarías el concepto de "Everything is a file"?**

7. El concepto *"Everything is a file"* se popularizó con UNIX y el *stream de bytes* y significa que no importa qué estemos usando en la computadora, todo lo utilizado finalmente es en realidad un archivo ejecutable. Una de las formas por las cuales podemos comprobar esto es viendo el contenido del directorio "dev" [/img/ls_dev] desde la terminal de linux, donde figuran varios archivos y, entre ellos, podemos reconocer al teclado y a la pantalla llamados "stdin" y "stdout" respectivamente. Otro ejemplo donde podemos encontrar esto es en la carpeta "bin", donde encontramos como archivos a los comandos vistos anteriormente entre otros [/img/ls_bin].

8) **¿Cuál es el método utilizado cuando hay varios procesos esperando a ser ejecutados?**

8. En principio, como mencionamos anteriormente, el SO orquesta los recursos para que sean utilizados. Cuando hay varios procesos ejecutándose, el SO decide dejar a un lado los procesos que están llevando mucho tiempo de espera de ejecución o que estén esperando algún dato resultante de otro proceso. Ésto lo hace "copiando" el estado del proceso en el cual se encuentran para luego, cuando vuelvan a ser procesados, lo hagan desde donde se quedaron.

9) **¿Cuáles son las partes de la memoria y qué diferencias tienen?**

9.

10) ****

10.