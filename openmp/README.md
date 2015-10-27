#openmp

###Este repositorio contiene una colección de actividades que permiten comprender el manejo de la libreria de programación en paralelo OpenMP.

##Actividad 1 - Hola Mundo

###Archivo: helloword.c

####Iteración 0
#####Observación: 
Es el típico programa secuencial del hola mundo.

####Iteración 1
#####Observación: 
Para esta iteración se incluye la librería de c omp.h, y las instrucciones de incorporación de hilos: #pragma open parallel para crear los hilos y omp_get_thread_num() para capturar el identificador del hilo.

#####Cuántos hilos se ejecutan?
R/ En este momento se están ejecutando cuatro hilos, cada uno de ellos imprime la frase “hello (id) world (id)”. donde id va desde 0 hasta 3.

#####Resultado:

hello (0) world (0)

hello (3) world (3)

hello (1) world (1)

hello (2) world (2)

####Iteración 2
Observación: En esta iteración se cambia la instrucción de construcción de hilos de #pragma open parallel a #pragma open parallel num_thereads(5), esta vez especificamos el número de hilos que  deseamos crear, se crearán 5 hilos.

#####Cuántos hilos se ejecutan?
R/ Efectivamente como se había previsto se han creado 5 hilos que imprimen la frase hola mundo especificando su número de hilo.

#####Difiere el número de hilos de la iteración anterior?, por qué?
R/ Se diferencia el número de hilos de la iteración anterior, porque en la iteración anterior al no especificar el número de hilos que se requieren toma por defecto 4, el número de núcleos de la máquina. En la nueva iteración estamos especificando en el momento de la creación de los hilos que necesitamos que se creen 5.

#####Resultado:

hello (2) world (2)

hello (1) world (1)

hello (4) world (4)

hello (3) world (3)

hello (0) world (0)

##Actividad 2 - Revisión de programas

###Archivo: parallel_00.c 
####Observación:
En este código se puede ver en acción la invocación en paralelo de un bloque de código en C y como se especifica que una variable sea tomada como una variable privada y accesible solo para un hilo.

###Archivo: parallel_01.c 
####Observación:
En este programa se muestra como se puede indicar un número diferentes de hilos para llevar a cabo una tarea.

###Archivo: parallel_02.c 
####Observación:
En este programa se muestra como se puede paralelizar un ciclo for.

###Archivo: parallelblock_00.c 
####Observación:
En este programa se muestra como se pueden paralelizar diferentes bloques de código a través de las directivas sections y section.

###Archivo: parallelfor_00.c 
####Observación:
En este programa se muestra la paralelización de un ciclo for pero además muestra una directiva de compilación llamada reduction que permite consolidar el valor parcial de diferentes hilos en una sola variable.

##Actividad 3 - Ejercicios propuestos
###Se encuentran dos programas en C que sirven para calcular el valor de Pi.

####Archivo: pi.c 
usa una aproximación a través del cálculo del área bajo la curva. La gráfica muestra la aproximación que sigue el programa .c.

####Archivo: Montecarlopi.c 
usa una aproximación basada en el método Monte Carlo para de forma aleatoria se llegue a la estimación del valor de Pi.

#####Son incluidas las instrucciones en OpenMP que transforman estas versiones secuenciales del cálculo de Pi en versiones que se ejecuten en paralelo.

####Archivo: pi_OpenMP.c 
Basado en el programa original pi.c se incluyeron las siguientes instrucciones para la conversión a un programa en paralelo

#####inclusión de la libreria omp.h

####Archivo: Montecarlopi_OpenMP.c 
Basado en el programa original Montecarlopi.c se incluyeron las siguientes instrucciones para la conversión a un programa en paralelo

#####inclusión de la libreria omp.h
