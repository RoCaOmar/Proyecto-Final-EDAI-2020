# Proyecto-Final-EDAI-2020
Poryecto final de EDAI 14/05/2020
Aqui se hara el proyecto final de Algoritmos 2020
Estructuras de Datos y Algoritmos I Proyecto Final 20202 página 1
ESTRUCTURAS DE DATOS Y ALGORITMOS I.
Proyecto Final 2020-2.
Objetivo: Desarrollar un programa que simule la operación de un Programador de Tareas (Job Scheduler) de un Sistema Operativo.
Uno de los componentes más importantes de los Sistemas Operativos es el llamado Programador de Tareas o Job Scheduler o simplemente Scheduler. Este programa se encarga de asignar el control del procesador a un proceso determinado. Para lograr este objetivo, el sistema utiliza una cola priorizada en donde introduce la información de cada uno de los procesos que se encuentran iniciados pero no activos, puesto que en un momento dado sólo puede haber un proceso activo en una máquina con un solo procesador. Cuando el proceso activo termina o pierde el control por algún evento que puede ser el agotamiento de su tiempo asignado o un evento de I/O, el Scheduler saca de la cola el proceso de más alta prioridad y lo pone en ejecución.
El proyecto a desarrollar es una pequeña y muy simplificada simulación de este proceso. Para esto hay que crear un programa (en C o en Python) que incluya la siguiente funcionalidad:
1. Defina una estructura de datos que contenga el identificador de un proceso cualquiera, que debe ser un número entero cualquiera y la prioridad del mismo, entero de 1 a 10 donde 1 representa la prioridad más alta y 10 la más baja.
2. Defina una cola priorizada implementada como un arreglo de las estructuras definidas en el punto anterior de un tamaño máximo razonable (entre 10 y 20).
3. Implemente la función insert que introduzca en la cola una estructura de proceso de acuerdo a su prioridad.
4. Implemente la función removeFirst que saque de la cola la primera estructura que es la de más alta prioridad.
5. Implemente la función display para desplegar el contenido de la cola. Esta función no es esencial para la ejecución del programa pero será muy útil durante el desarrollo.
6. Implemente la función create que inserte en la cola un número cualquiera de estructuras de procesos para poder contar con una cola de procesos no vacía.
7. Implemente la función main que lleve a cabo la ejecución del simulador de la manera siguiente:
a. Remueva el primer proceso de la cola, para simular que se encuentra en ejecución.
Estructuras de Datos y Algoritmos I Proyecto Final 20202 página 2
b. Despliegue un mensaje indicando que hay un proceso activo y los datos del mismo: identificador del proceso y prioridad.
c. Espere un tiempo en forma aleatoria. Se sugiere utilizar la función sleep para esperar y las funciones srand y rand para generar un número pseudoaleatorio. Esto es desde luego para simular el tiempo que tarda en ejecutar el proceso.
d. Una vez transcurrido el tiempo de espera desplegar otro mensaje indicando que el proceso perdió el control del procesador.
e. Disminuir o aumentar en forma aleatoria la prioridad del proceso que “perdió el control” para simular un cambio de prioridad realizado por el Scheduler en base al comportamiento del proceso. Esto deberá hacerse también en forma aleatoria pero cuidando que la nueva prioridad esté dentro de los valores aceptables (1 a 10).
f. Regresar el proceso a la cola de espera de acuerdo a su nueva prioridad.
g. Los pasos anteriores deben repetirse cierto número de veces para verificar la operación del simulador. Esto puede hacerse mediante un ciclo infinito cancelando el programa después de un tiempo razonable (más apegado quizá a la situación real) o mediante un ciclo con un número de iteraciones fijo.
La salida del programa deberá ser similar a la siguiente:
Procesos en cola:
Número: 3000 prioridad: 1
Número: 8000 prioridad: 2
Número: 5000 prioridad: 2
Número: 6000 prioridad: 3
Número: 4000 prioridad: 3
Número: 1000 prioridad: 5
Número: 2000 prioridad: 6
Número: 7000 prioridad: 8
Proceso 3000 está ejecutando con prioridad 1.
Procesando 4 segundos.
Proceso 3000 perdió control del CPU.
Nueva prioridad: 8
Se regresa a la cola de espera con prioridad 8.
Proceso 8000 está ejecutando con prioridad 2.
Procesando 4 segundos.
Proceso 8000 perdió control del CPU.
Nueva prioridad: 6
Estructuras de Datos y Algoritmos I Proyecto Final 20202 página 3
Se regresa a la cola de espera con prioridad 6.
Proceso 5000 está ejecutando con prioridad 2.
Procesando 2 segundos.
Proceso 5000 perdió control del CPU.
Nueva prioridad: 8
Se regresa a la cola de espera con prioridad 8.
Proceso 6000 está ejecutando con prioridad 3.
Procesando 4 segundos.
Proceso 6000 perdió control del CPU.
Nueva prioridad: 8
Se regresa a la cola de espera con prioridad 8.
Proceso 4000 está ejecutando con prioridad 3.
Procesando 4 segundos.
Proceso 4000 perdió control del CPU.
Nueva prioridad: 4
Se regresa a la cola de espera con prioridad 4.
Proceso 4000 está ejecutando con prioridad 4.
Procesando 3 segundos.
Proceso 4000 perdió control del CPU.
Nueva prioridad: 1
Se regresa a la cola de espera con prioridad 1.
Proceso 4000 está ejecutando con prioridad 1.
Procesando 2 segundos.
Proceso 4000 perdió control del CPU.
Nueva prioridad: 10
Se regresa a la cola de espera con prioridad 1.
Proceso 4000 está ejecutando con prioridad 1.
Procesando 5 segundos.
Proceso 4000 perdió control del CPU.
Nueva prioridad: 9
Se regresa a la cola de espera con prioridad 9.
Proceso 1000 está ejecutando con prioridad 5.
Procesando 1 segundo.
Proceso 1000 perdió control del CPU.
Nueva prioridad: 4
Se regresa a la cola de espera con prioridad 4.
Proceso 1000 está ejecutando con prioridad 4.
Estructuras de Datos y Algoritmos I Proyecto Final 20202 página 4
Procesando 5 segundos.
Proceso 1000 perdió control del CPU.
Nueva prioridad: 1
Se regresa a la cola de espera con prioridad 1.
Proceso 1000 está ejecutando con prioridad 1.
Procesando 1 segundo.
Proceso 1000 perdió control del CPU.
Nueva prioridad: 6
Se regresa a la cola de espera con prioridad 6.
Procesos en cola:
Número: 1000 prioridad: 6
Número: 8000 prioridad: 6
Número: 2000 prioridad: 6
Número: 6000 prioridad: 8
Número: 5000 prioridad: 8
Número: 3000 prioridad: 8
Número: 7000 prioridad: 8
Número: 4000 prioridad: 9
