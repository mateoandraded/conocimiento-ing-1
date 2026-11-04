# 07SchedulingandResourceAllocation

_Fuente: `07SchedulingandResourceAllocation.pdf`_


## Página 1

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Resources and Scheduling
Lecture 7
[página sin texto: revisar visualmente]

## Página 2

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Agenda
• Scheduling with Activity-on-Arrow Networks
▪Analysis of an Activity-on-Arrow Network
▪Determining the Critical Path of a Software Project
• Resources and Scheduling
▪Time-Limited Scheduling
▪Resource-Limited Scheduling

## Página 3

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Analysis of an Activity-on-Arrow Network
[página sin texto: revisar visualmente]

## Página 4

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Análisis de la Red
• Una vez que la red ha sido dibujada y a cada actividad se le
ha asignado una duración estimada, se necesita calcular el
earliest time -lo más temprano- que podemos llegar a un
nodo.
• Luego, necesitamos conocer el latest time -lo más tarde- que
un nodo puede ser alcanzado.
• En general cada nodo estará asociado con dos tiempos, el
earliest time y el latest time.

## Página 5

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Análisis de la red
[página sin texto: revisar visualmente]

## Página 6

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Análisis de la Red
• El earliest event time es lo más pronto que un nodo puede
ser alcanzado.
• El latest event time es lo más tarde que un nodo puede ser
alcanzado si el proyecto debe ser completado a tiempo.

## Página 7

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Calculating the Earliest Event Time
[página sin texto: revisar visualmente]

## Página 8

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Calculando Earliest Event Times
• El cálculo del earliest event time para cada nodo es hecho a
través del forward pass a través de la red, iniciando desde el
único nodo de inicio y terminando en el único nodo de
terminación del proyecto.
• El earliest event time en cada nodo es el tiempo en el cual
cada actividad predecesora ha sido completada.

## Página 9

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Calculando Earliest Event Times
[página sin texto: revisar visualmente]

## Página 10

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Calculando Earliest Event Times
[página sin texto: revisar visualmente]

## Página 11

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Calculation of the Latest Event Time
[página sin texto: revisar visualmente]

## Página 12

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Calculando Latest Event Times
• Estos tiempos son calculados en el backward pass.
• Indica cuan rápido el proyecto puede ser terminado.
• Sin embargo, dada una fecha de fin, no solo estamos
interesados en saber cuán rápido un proyecto puede ser
terminado sino también lo más tarde que cada evento puede
ocurrir si el proyecto debe ser terminado en esa fecha.

## Página 13

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Calculando Latest Event Times
[página sin texto: revisar visualmente]

## Página 14

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Calculando Latest Event Times
[página sin texto: revisar visualmente]

## Página 15

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Calculando Latest Event Times
[página sin texto: revisar visualmente]

## Página 16

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Critical Path
[página sin texto: revisar visualmente]

## Página 17

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Calculando EST, EFT, LST, LFT
• EST (Earliest Start Time)
▪es el earliest event time del nodo de inicio
• EFT (Earliest Finish Time)
▪es el earliest event time del nodo de inicio + duración
• LST (Latest Start Time)
▪es el latest event time del nodo de fin - duración
• LFT (Latest Finish Time)
▪es el latest event time del nodo de fin

## Página 18

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Float y Critical Path
• Algunas actividades podrían incrementar su duración y aún
así el proyecto podría completarse en la fecha establecida. Se
dice que esas actividades tienen float.
• Float es el exceso de tiempo disponible en una actividad al
de su tiempo estimado de duración.
• Path float o total float es el tiempo que una actividad se
puede expandir o retrasar su inicio y el proyecto aún se
cumplirá en la fecha establecida.

## Página 19

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Float y Critical Path
• Total float =
▪latest time of finish event - earliest time of start event - duration
• En el ejemplo, la actividad buscar un lápiz tiene un float de 4
minutos: 5-0-1
• Path es cualquier secuencia de actividades que podrían ser
descritas siguiendo las flechas de actividades desde el inicio
al final del proyecto.

## Página 20

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Float y Critical Path
• El critical path es el path con menos float.
[página sin texto: revisar visualmente]

## Página 21

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Activity-on-Arrow Network
[página sin texto: revisar visualmente]

## Página 22

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Activity-on-Arrow network
• La red para el proyecto sería:
[página sin texto: revisar visualmente]

## Página 23

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
More Examples
[página sin texto: revisar visualmente]

## Página 24

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Tabla de Datos de Actividades Ejemplo 5
Actividad
Duración
(semanas)
Dependencia con
Personas
A
10
Ninguna
1
B
5
Ninguna
2
C
10
A y B
2
D
10
C
1
E
5
C
1
[página sin texto: revisar visualmente]

## Página 25

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Activity-on-Arrow Networks Ejemplo 5
[página sin texto: revisar visualmente]

## Página 26

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Activity-on-Arrow Networks Ejemplo 5
[página sin texto: revisar visualmente]

## Página 27

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Activity-on-Arrow Networks Ejemplo 5
[página sin texto: revisar visualmente]

## Página 28

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Activity-on-Arrow Networks Ejemplo 5
• Tabla de análisis para la red
[página sin texto: revisar visualmente]

## Página 29

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Una Red Completa
[página sin texto: revisar visualmente]

## Página 30

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Resources and Scheduling
[página sin texto: revisar visualmente]

## Página 31

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Resources and Scheduling
• En la mayoría de los proyectos la disponibilidad de recursos
es limitada: incluyendo diseñadores, ingenieros, vendedores,
instalaciones compartidas e incluso el flujo de caja.
• En vista que los recursos son finitos sería necesario
programar las actividades no lo más pronto posible sino en el
momento que se haga un mejor uso de los recursos
disponibles.

## Página 32

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Resources and Scheduling
• Existen dos escenarios posibles:
▪El caso de recursos ilimitados en un tiempo de duración fija para el
proyecto.
▪El caso de recursos limitados pero en un tiempo de proyecto flexible.
• En la primera situación es vital cumplir la fecha de entrega del
proyecto.
▪Por lo tanto el director de proyecto puede contratar personal adicional,
pagar sobretiempo, contratar servicios, rentar instalaciones y lo que sea
necesario para cumplir la fecha.
• En la segunda situación, el director de proyectos no puede contar
con más personal, ni pagar horas extras, ni contratar más
servicios.
▪Por lo tanto estas limitaciones podrían prolongar la fecha de entrega.

## Página 33

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Resources and Scheduling
• La
primera
situación
se
conoce
como
time-limited
scheduling.
• La segunda se denomina resource-limited scheduling.
• Si el director de proyecto tiene que enfrentar ambos tipos de
limitaciones, se deberá realizar primero un enfoque y luego
el otro; intentando buscar una solución compatible.
▪Caso contrario, se deberá negociar opciones de factibilidad con el
cliente.

## Página 34

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Resources and Scheduling
[página sin texto: revisar visualmente]

## Página 35

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Time-limited Scheduling
[página sin texto: revisar visualmente]

## Página 36

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Time-limited Scheduling
• Los objetivos de la programación en una situación con
limitaciones de tiempo son:
▪Calcular los requerimientos de recursos de tal manera que puedan
estar disponibles en el momento indicado.
▪Programar cada actividad para que la carga de recursos sea tan
fluida (nivelada) como sea posible.
• Se denomina resource smoothing. Aunque se asume que los
recursos son infinitos en una programación limitada por
tiempo.

## Página 37

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Time-limited Scheduling
[página sin texto: revisar visualmente]

## Página 38

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Time-limited Scheduling
[página sin texto: revisar visualmente]

## Página 39

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Time-limited Scheduling
• Los pasos para producir un time-limited schedule son:
1. Elaborar un diagrama de red de actividades
2. Elaborar una tabla mostrando para cada actividad el recurso
requerido, la duración, EST, float y LFT.
3. Listar las actividades en orden creciente de float (y en orden de
latest finish time para las actividades con el mismo float)
4. Grafique un initial resource loading chart con cada actividad
programada a su earliest start time. Esto produce un diagrama
con las actividades más críticas abajo y las que tienen mayor
float arriba.

## Página 40

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Time-limited Scheduling
• Continuación de pasos:
5. Reordenar las actividades dentro de su float para alcanzar un
cuadro tan nivelado como sea posible dentro de las “reglas” (es
decir, la duración de las actividades no debe ser cambiada en
este paso y las dependencias deben ser preservadas)
6. Use su criterio para interpretar y mejorar las carga por medio del
cambio de “reglas” (esto es, replantear dependencias y
considerar sobretiempo trabajando en el pico).

## Página 41

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Time-limited Scheduling
[página sin texto: revisar visualmente]

## Página 42

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Time-limited Scheduling Ejemplo 3
[página sin texto: revisar visualmente]

## Página 43

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Time-limited Scheduling
[página sin texto: revisar visualmente]

## Página 44

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Resource-limited Scheduling
[página sin texto: revisar visualmente]

## Página 45

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Resource-limited Scheduling
• Time-limited scheduling: límite fijo de tiempo
• Resource-limited scheduling es el punto de vista opuesto:
debemos ajustar la asignación de recursos con un límite fijo
de recursos.
• A diferencia del time-limited scheduling, resource-limited
scheduling hace uso de conjunto elemental de reglas.

## Página 46

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Resource-limited Scheduling
• Parallel scheduling [programación en paralelo] es un método
de scheduling en el cual las actividades elegibles son
consideradas en paralelo.
• Serial scheduling [programación serial] es un método de
scheduling que considera cada actividad en algún orden
predefinido; por ejemplo en orden creciente de float.

## Página 47

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Resource-limited Scheduling
• Reglas elementales:
▪Regla 1: De entre las actividades elegibles,
❖Seleccione primero la actividad que tenga la fecha más temprana para el
latest start time.
❖Si varias actividades elegibles tienen el mismo latest start time entonces
seleccione primero la que tenga la menor duración.
❖Si aún hay dos o más, entonces otros distintivos tales como escoger la
actividad con el mayor requerimiento de recursos podría seguir.

## Página 48

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Resource-limited Scheduling
▪Regla 2: Siempre continuar con una actividad que ya ha sido
iniciada hasta que haya sido completada, es decir, actividades no
pueden ser interrumpidas.
▪Regla 3: Nunca permitir a un recurso estar desocupado si hay una
actividad elegible que puede ser iniciada.
▪Regla 4: Una actividad no puede ser iniciada solo con recursos
parciales.

## Página 49

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Resource-limited Scheduling
[página sin texto: revisar visualmente]

## Página 50

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Resource-limited Scheduling
[página sin texto: revisar visualmente]

## Página 51

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Resource-limited Scheduling
[página sin texto: revisar visualmente]

## Página 52

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Resource-limited Scheduling
[página sin texto: revisar visualmente]

## Página 53

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Resource-limited Scheduling
Tiempo
Personas
libres
Actividades
elegibles en
orden de LST
Personas
LST
Comentarios
0
2
A
1
0
Aceptar regla 1
1
B
2
5
Personas insuficientes regla 4
10
2
B
2
5
Aceptar regla 1
15
2
C
2
10
Aceptar regla 1
25
2
D
1
20
Aceptar regla 1
1
E
1
25
Aceptar regla 1

## Página 54

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Resource-limited Scheduling
[página sin texto: revisar visualmente]

## Página 55

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Next On
[página sin texto: revisar visualmente]

## Página 56

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Take Away Points
• Las actividades van en las flechas
• Los eventos van en los nodos
• Earliest event time y Latest event time
• Identificar unidades y convenciones en los gráficos
• Utilizar el menor número de actividades dummies
• Time-limited vs. Resource limited scheduling
• Las reglas del resource-limited scheduling
• La reducción del recurso pico

## Página 57

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Further Reading
• Field and Keller, “Project Management”
• Chapter 3: Planning
[página sin texto: revisar visualmente]

## Página 58

Software Engineering I
© Dra. Villavicencio, © Dr. Mera-Gómez
2026
Unit 2
Next Lecture
• Software size and estimation
[página sin texto: revisar visualmente]