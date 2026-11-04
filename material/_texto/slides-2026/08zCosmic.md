# 08zCosmic

_Fuente: `08zCosmic.pdf`_


## Página 1

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
COSMIC
Método para estimar el tamaño de un software en base a su funcionalidad
Sesión 8b
[página sin texto: revisar visualmente]

## Página 2

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Agenda
1. Estimación en Ingeniería de Software
2. Estimación basada en funcionalidad
3. Método de estimación COSMIC
4. Fases del método de estimación COSMIC
5. Beneficios y limitaciones del uso de COSMIC
2

## Página 3

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Estimación en Ingeniería de Software
• Tiene por objetivo conocer el tamaño aproximado del
sistema a desarrollar con el objeto de establecer el costo, la
duración y los recursos necesarios para conseguirlo.
• Enfoques para estimación:
▪Valoraciones de expertos
▪Descomposición
▪Métodos evolucionarios y de prototipo
▪Métodos estadísticos
▪Uso de algoritmos: líneas de código [COCOMO], requerimientos
funcionales [FPA, COSMIC], pantallas/reportes/ módulos, etc .
[puntos de aplicación]
3

## Página 4

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Estimación basada en funcionalidad
• COSMIC es un método para estimar el tamaño de un software
basado en la especificación de sus requerimientos funcionales
[ISO/IEC 14143/1:2007].
• Elaborado por Common Software Measurement International
Consortium para:
▪Software de aplicaciones de negocios tales como banca, seguros,
manufactura, distribución, etc.
▪Software en tiempo real tales como software embebido en dispositivos
para
control
de
máquinas.
Ej.:
motores
de
autos,
aviones,
electrodomésticos, sistemas operativos, etc.
▪Híbridos de ambos, como por ejemplo un sistema para reservaciones
en aerolíneas.
• No
aplicable
para
sistemas
expertos,
simuladores,
procesamiento de imágenes, etc.
4

## Página 5

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Método de estimación COSMIC
5
Modelo del método de estimación COSMIC
Fuente: http://www.itba.edu.ar
FUR:
Requerimiento
funcional del
software
[página sin texto: revisar visualmente]

## Página 6

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Método de estimación COSMIC
Fuente: https://www.scopemaster.com/introduction-to-cosmic-function-points/
[página sin texto: revisar visualmente]

## Página 7

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Fases del método de estimación COSMIC
• Fase I: La fase de definición de la estrategia de medición
• Fase II: La fase de mapeo de FURs al modelo conceptual de
COSMIC
• Fase III: La fase de medición de COSMIC
• Fase IV: La fase del reporte de la medición
7

## Página 8

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Fases del método de estimación COSMIC
Fuente: https://cosmic-sizing.org/cosmic-fsm/
[página sin texto: revisar visualmente]

## Página 9

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Fase I: La fase de definición de la estrategia de medición
• Se establece el propósito de la medición, es decir, las
razones por las cuales se realiza la medición. Ej.:
▪Estimar el costo de un nuevo desarrollo de software.
▪Comparar el costo real con el costo estimado del software.
• Se define el alcance de la medición, es decir, el subconjunto
de requerimientos funcionales incluidos en la estimación.
9

## Página 10

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Fase II: La fase de mapeo de FURs al modelo conceptual
de COSMIC
• Algunos principios de los conceptos de COSMIC son:
1. El software está estructurado por capas
2. El software ejecuta funciones con base en eventos disparados
por los usuarios
3. Cada único evento dispara un único proceso funcional, el mismo
que está completo cuando se ha generado la respuesta al evento
4. Un proceso funcional comprende subprocesos que mueven o
manipulan datos.
10

## Página 11

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Fase II: La fase de mapeo de FURs al modelo conceptual
de COSMIC
5. Un movimiento de datos es el movimiento de un único grupo de
datos
6. Contempla cuatro subprocesos de movimientos de datos:
❖Entrada: transfiere datos desde los usuarios hacia el software
❖Salida: transfiere datos desde el software hacia los usuarios
❖Lectura: transfiere datos desde el almacenamiento
❖Escritura: transfiere datos hacia el almacenamiento
11

## Página 12

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Fase II: La fase de mapeo de FURs al modelo conceptual
de COSMIC
12
Flujo genérico de datos en COSMIC
Fuente: http://www.itba.edu.ar
[página sin texto: revisar visualmente]

## Página 13

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Fase II: La fase de mapeo de FURs al modelo conceptual
de COSMIC
[página sin texto: revisar visualmente]

## Página 14

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Fase II: La fase de mapeo de FURs al modelo conceptual
de COSMIC
14
Modelo general para el proceso de representación COSMIC
Fuente: http://www.itba.edu.ar
[página sin texto: revisar visualmente]

## Página 15

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Fase III: La fase de medición de COSMIC
• Toma como entrada una instancia del modelo de software
COSMIC
• Con base en reglas y procedimientos genera el valor que es
directamente proporcional al tamaño del software en
medición. Este valor es expresado en CFP [COSMIC Function
Point]
15

## Página 16

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Fase III: La fase de medición de COSMIC
16
Procedimiento general de la fase de medición
Fuente: http://www.itba.edu.ar
[página sin texto: revisar visualmente]

## Página 17

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Fase III: La fase de medición de COSMIC
• Identificar los movimientos de datos
• Aplicar la función de medición
• Agregar los resultados de la medición con base en las reglas
de agregación:
17

## Página 18

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Fase IV: La fase del reporte de la medición
• La medición es presentada en una matriz en donde las filas
representan los procesos funcionales agrupados por capas,
las columnas representan los grupos de datos y las celdas
identifican
los
subprocesos:
Entrada,
Salida,
Lectura,
Escritura.
18

## Página 19

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Fase IV: La fase del reporte de la medición
19
Matriz de medición del tamaño de un software con COSMIC
Fuente: http://www.cosmicon.com
[página sin texto: revisar visualmente]

## Página 20

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Beneficios del uso de COSMIC
• Compatible con los métodos modernos para documentación
de requerimientos de software.
• Exige realizar adecuadamente el proceso de levantamiento
de requerimientos de software
• Es fácil de aprender y tiene un adecuado balance costo-
beneficio
• Es posible automatizar el proceso de dimensionamiento de
los requerimientos que son manejados en herramientas
CASE
• Preciso independientemente del tamaño del software
20

## Página 21

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Limitaciones del uso de COSMIC
• No estima el esfuerzo en requerimientos no funcionales del
software
• Excluye los componentes físicos o técnicos relacionados con
el hardware.
21
[página sin texto: revisar visualmente]

## Página 22

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Puntos para recordar
• La entrada al método de estimación COSMIC son los
requerimientos funcionales del software.
• Es aplicable para software de negocios y software en tiempo
real.
• Depende de la calidad del proceso del levantamiento de
requerimientos.
• No estima el esfuerzo en requerimientos técnicos o de
calidad.
22

## Página 23

Software Engineering I
Dra. Villavicencio, Dr. Mera
2023
Unit 2
Further Reading
• COSMIC Organization, “The standard methodology for sizing
software”
• https://cosmic-sizing.org/cosmic-sizing/intro/
• Scope Master, Introduction to COSMIC Function Points
• https://www.scopemaster.com/introduction-to-cosmic-function-
points/
• Peter R. Hill, “Practical Software Project Estimation: A Toolkit
for Estimating Software Development Effort & Duration”
• Chapters 19, 20, 21