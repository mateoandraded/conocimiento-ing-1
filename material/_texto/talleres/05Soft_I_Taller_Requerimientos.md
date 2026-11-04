# 05Soft_I_Taller_Requerimientos

_Fuente: `05Soft_I_Taller_Requerimientos.pdf`_


## Página 1

ESCUELA SUPERIOR POLITÉCNICA DEL LITORAL
FACULTAD DE INGENIERÍA EN ELECTRICIDAD Y COMPUTACIÓN
INGENIERÍA DE SOFTWARE I
TALLER DE ESPECIFICACIÓN DE REQUERIMIENTOS
Objetivos específicos de la actividad
•
Organizar el desarrollo de un sistema de software mediante la conformación de equipos de trabajo
considerando roles y responsabilidades.
•
Aplicar normas y buenas prácticas de ingeniería de requerimientos para la generación de
especificaciones de requerimientos de software para un sistema de mediana complejidad.
Descripción
Cada equipo de trabajo debe preparar el documento de especificación de requerimientos (Historias de usuario
y criterios de aceptación) para el sistema de software del caso de estudio que se detalla a continuación.
Caso de estudio: Venta libros a través de Internet
Los clientes acceden a la información sobre los libros a través de la Web y realizan búsquedas por autor, título
o ISBN. A medida que navegan por las distintas páginas, y encuentran algún libro que les interesa, lo incluyen
en el carrito de la compra para efectuar al final el pedido correspondiente. Para realizar un pedido, un cliente
debe estar registrado. Esto significa introducir una serie de datos personales (nombre y apellidos, dirección,
localidad, código postal, país), datos de la tarjeta de crédito (tipo de tarjeta, número, fecha límite de validez) y
sus preferencias de envío (correo normal, expreso, internacional). Asociado a un pedido específico pueden
introducirse opciones de empaquetado (estándar o regalo), tarjeta con mensaje adicional cuando es un regalo,
o un nombre y dirección de otra persona a la que se le envía un pedido. Como es habitual en este tipo de
aplicaciones, debería elegir un nombre de usuario y una clave como método de autentificación para efectuar las
transacciones habituales con la librería. Cuando se han incluido en el carrito de compras el conjunto de los
libros deseados (cantidad, título y autor), se debe pasar al proceso de confirmar el pedido que debería requerir
un paso previo de seguridad para garantizar que el cliente es quien dice ser. Una vez introducidos todos los
datos adicionales, el cliente confirma el pedido que pasa a un estado de espera -90 minutos- durante el cual es
posible modificar algunos de los ítems del pedido (eliminar o cambiar cantidad) pero no añadir nuevos ítems.
Si se requieren más ítems, el cliente debe crear un nuevo pedido. Una vez transcurridos los 90 minutos, los
pedidos quedan confirmados definitivamente y no se pueden modificar ni anular. La empresa puede realizar
envíos parciales en función de la disponibilidad de los ítems, pero sin modificar el costo total de envío. El
sistema envía notificaciones al cliente para confirmarle el pedido, así como para confirmarle el envío o envíos
correspondientes.
El gerente comercial de la empresa define promociones mensuales. Es decir, otorga descuentos a libros de un
género literario en un mes en particular. Por ejemplo, todos los libros de misterios tienen un descuento del 30%

## Página 2

durante la última semana de octubre. Tales promociones pueden ser visualizadas por los clientes en el sitio
web.
El gerente literario de la empresa analiza las preferencias de los lectores, para lo cual requiere reportes
detallados por cada tipo de género y un reporte consolidado de géneros.
Requisitos del sistema
1. El sistema deberá permitir registrar usuarios
2. El sistema deberá permitir autentificación (log in) de clientes
3. El sistema deberá permitir realizar búsquedas de libros por autor, título o ISBN.
4. El sistema deberá permitir agregar un libro(ítem) al carrito de compra de un cliente.
5. El sistema deberá permitir confirmar una compra por parte de un cliente.
6. El sistema deberá permitir modificar un pedido ya confirmado, pero aún no enviado por parte de un
cliente.
7. El sistema deberá permitir realizar envíos parciales de pedidos.
8. El sistema podrá permitir distintas opciones de empaquetado para un pedido.
9. El sistema enviará notificaciones vía correo electrónico de confirmación de pedidos a los clientes.
10. El sistema debe permitir crear promociones.
11. El sistema debe generar reportes por géneros literarios
Entregables (en formato .docx y .pdf).
Una vez leído el caso, por favor realice lo siguiente:
•
Identifique los usuarios del sistema.
•
Redacte las historias de usuario 5, 6, 7, 8 y 10
•
Redacte los criterios de aceptación para la historia de usuario “Confirmación de compra”.
Consideraciones
•
El texto con el que se describe cada requerimiento debe cumplir con las características de un
requerimiento de calidad (correcto, no ambiguo, entendible, completos, consistente, factible,
priorizado, verificable, modificable, trazable, organizado, independiente del diseño).
Rúbrica
•
Identificación de todos los usuarios del sistema 5%.
•
Historias de usuario bien redactadas 80%
•
Criterios de aceptación para la historia de usuario “Confirmación de compra” 15%.