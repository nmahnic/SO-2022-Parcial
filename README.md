# SO-2022-Parcial
## Alumno: Gamboa, Gerardo

## 1) ¿Qué propone la frase "everything is a file"?

Los sistemas operativos de tipo UNIX, al permitirnos un acceso abierto al sistema operativo en sí, nos muestra la existencia e interacción del mismo con cada uno de los componentes de la computadora. Esto se refleja en archivos que contienen distintos formatos de código (dependiendo del componente), lo cual permite el uso correcto del componente y el manejo de su proceso(s) en el CPU y la memoria RAM.

Cualquier proceso y/o componente (hardware) se puede observar a través de la consola. Por ejemplo, en la siguiente captura de pantalla podemos que dentro del directorio /dev (hace referencia a "devices"), se encuentran todos los dispositivos de entrada y salida. Los mismos poseen sus propios directorios y archivos.

--Abrir archivo "screen_1.png" dentro del directorio img--
*Simple pero correcto, hubiera hablado de las 5 APIs del sistema para operar cualquier perisferico como archivo para que estuviera mas correcta. 0,75*

## 2) Señale y desarrolle brevemente 2 razones por las que es necesario un sistema operativo en un computador

* Hardware: un computador no es más que un conjunto de circuitos electrónicos unidos entre sí. Para que estos circuitos funcionen e interactúen entre sí y con el usuario, es necesario un software que pueda acceder a él, interpretarlo, recibir y darle órdenes.

* Interacción usuario-computador: luego de analizar y procesar cada uno de los componentes dentro del computador, el sistema operativo cumple con la función de reflejar en un interfaz gráfica lo que el usuario del mismo va a observar. No sólo se limita a esto, ya que a través del sistema operativo, el usuario puede ver y/o modificar características de los componentes según él/ella desee (dependiendo del sistema operativo).
*Mal, la explicacion no es correcta, pero la pregunta es buena 0,1*

## 3) Describa el ciclo de vida de un proceso

* Inicio: un proceso es iniciado por el sistema operativo o el usuario.

* Ready (esperando): el proceso se encuentra ocupando un lugar en la memoria y está en espera de una señal para realizar una nueva acción/interacción.

* Ready (ejecutando): el proceso pasa a realizar la acción para la cual fue llamado.

* Close: el proceso, luego de ser ejecutado, procede a ser terminado y a ceder su lugar en la memoria para un nuevo proceso.
*Un proceso se crea a partir de un fork de otro proceso, falta waiting for resources. Falta desarrollar mas, pero es buena pregunta 0,4*

## 4) ¿Un sistema operativo de tipo UNIX maneja de mejor manera los procesos? ¿Por qué?

Desde su aparición y constante desarrollo, se ha observado que los sistemas operativos de tipo UNIX aprovechan de mejor manera el uso del CPU y la memoria RAM de un computador; manejando de manera más práctica la cantidad de procesos y subprocesos que se ejecutan al mismo tiempo, limitando su peso y periodo de estadía dentro de la memoria y dando paso a que otros nuevos procesos puedan ejecutarse e interactuar entre sí. Gracias a esto, los sistemas operativos de tipo UNIX tienen la "fama" de ser mucho más ligeros y funcionales para casi cualquier tipo de hardware.
*Su fama no se debe a esto, sino a su alta compatibilidad con hardware legacy 0,25*

## 5) Señale y desarrolle brevemente 3 diferencias entre un sistema operativo de código abierto y uno restringido

* El sistema operativo de código abierto puede ser visualizado a nivel de código e infraestructura por cualquier usuario, mientras que el sistema operativo restringido sólo puede ser visualizado internamente por sus desarrolladores.

* Al poder visualizar y modificar el código dentro del sistema operativo de código abierto, el usuario puede personalizarlo a su antojo, crear/modificar programas/procesos o, inclusive, otros sistemas operativos.

* Por lo general, los sistemas operativos de código abierto son fuertemente respaldados por comunidades que ofrecen preguntas, respuestas y soluciones a interrogantes y problemas cotidianos dentro del mismo, lo que puede suponer una solución más rápida y práctica. En un sistema operativo restringido, el usuario debe esperar por una respuesta por parte del equipo de soporte del sistema.
*Bien 1*

## 6) ¿Por qué es importante la  interacción entre el sistema operativo con el CPU y la memoria RAM y para qué sirve?

El sistema operativo administra todos y cada uno de los procesos que corren a través de los diferentes software y hardware dentro del computador. Sin este tipo de "intermediario" realizando un correcto manejo de los procesos, todos los componentes accederán al mismo tiempo al sistema, provocando un colapso del CPU y la memoria RAM y, a su vez, de los procesos en sí.
*Mal pero la pregunta está buena 0*

## 7) Señale 10 comandos de Linux vitales para un usuario de nivel principiante/intermedio y explique qué función cumple cada uno

* pwd: imprime en pantalla (dentro de la consola) el directorio actual en el que se encuentra el usuario.

* ls: muestra los archivos y directorios que contiene el directorio actual.

* cd: permite cambiar de directorio; ya sea al anterior, al siguiente o a uno especificado por el usuario.

* touch: crear un archivo (touch + nombre_del_archivo).

* mkdir: crear un directorio (mkdir + nombre_del_directorio).

--Abrir archivo "screen_7-1.png" dentro del directorio img para ver ejemplos de los comandos señalados hasta este punto--

* man: muestra al usuario la función y diferentes combinaciones que posee un comando (man + comando).

--Abrir archivo "screen_7-2.png dentro del directorio img para ver un ejemplo de este comando--

* htop: muestra al usuario los procesos en ejecución dentro del sistema operativo en tiempo real, el uso de CPU, memoria RAM,y, especificando los IDs de cada proceso, de donde vienen, hacia donde van, cuándo se ejecutaron, a qué comando pertenecen, etc.

--Abrir archivo "screen_7-3.png dentro del directorio img para ver un ejemplo de este comando--

* ps: parecido al comando htop, pero este muestra en pantalla un screenshot de los procesos que se estaban ejecutando a este ese momento, de una manera más simple y sin los detalles del comando anterior. Además, al ser "un screenshot", no es en tiempo real. Es mucho más útil al ser utilizado junto con sus diferentes combinaciones (por ejemplo: "ps -ely").

--Abrir archivo "screen_7-4.png dentro del directorio img para ver un ejemplo de este comando--

* kill: permite al usuario enviar una señal a un proceso. Esta señal puede ser diferente dependiendo de las combinaciones que se utilicen, pero por lo general,se utiliza para terminar un proceso. Por lo general el mismo puede hacerlo utilizando Ctrl+C, pero el comando kill (junto con sus diferentes combinaciones) permite una terminación mucho más exacta del proceso especificado.

--Abrir archivo "screen_7-5.png dentro del directorio img para ver un ejemplo del comando htop ejecutándose--

--Abrir archivo "screen_7-6.png dentro del directorio img para ver un ejemplo del comando htop siendo terminado por el comando kill--

* sudo: permite al usuario ejecutar un comando con permisos de administrador del sistema.

--Abrir archivo "screen_7-7.png dentro del directorio img para ver un ejemplo de este comando--
*Bien 1*

## 8) ¿Qué es el kernel y para qué sirve?

Es el sistema operativo en sí. Cumple la función de administrar y separar los procesos (permitir la interacción entre ellos)entre los espacios propios del kernel y del usuario. No todos los procesos son visibles para el usuario en el primer momento a menos que él/ella acceda a los mismos, por lo que se necesitará de una visualización detallada de cada proceso (con el comando htop y sus combinaciones por ejemplo) para ver en dónde se encuentra cada proceso.
*La explicación es muy basica 0*

*El manejo de los conceptos es superficial, es necesario profundizar. Demuestra manejo practico de la consola, EN PROCESO, 3,5*