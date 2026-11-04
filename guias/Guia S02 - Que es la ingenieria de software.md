# Guía S02 — Qué es la ingeniería de software

> **Léela de corrido.** Esta es la pregunta de cajón del examen: *¿qué es la ingeniería de software y por qué es importante?* Léela hasta poder explicarla sin mirar. Fecha de la sesión: 2026-09-30.

## 1. De la programación individual al software profesional
Escribir programas lo hace mucha gente: en Excel con macros, científicos que procesan datos, aficionados. Pero el software **profesional** tiene tres diferencias:
1. Lo usa **alguien distinto a quien lo escribió**.
2. Lo construyen **equipos**, no individuos. Nadie domina todas las especialidades (requerimientos, frontend, backend, seguridad, pruebas).
3. Se **mantiene y cambia** durante toda su vida.

La ingeniería de software existe para el segundo tipo de programación. Incluye técnicas para especificar, diseñar y evolucionar.

## 2. Cómo nació: la crisis del software
- En **1968**, en una conferencia de la **OTAN** en **Garmisch (Alemania)**, se reconoció la **crisis del software**: los sistemas crecían en complejidad más rápido de lo que se sabía construirlos bien.
- Los desarrolladores de hardware, que eran quienes sabían de software, se dieron cuenta de que conocían la máquina pero casi nada de **procesos, métodos y herramientas** de software.
- De ahí nace la ingeniería de software como disciplina de investigación.

> 🔎 **Buscar en internet:** *"NATO software engineering conference 1968 Garmisch crisis"*. Verás fotos de la conferencia y los documentos de la época. Basta con leer la primera página de un artículo.

> 🔎 **Buscar en SWEBOK v4:** pág. 38, en la misma sección 1 de la Introducción. Busca la palabra *Historically*.

**Dato del profesor (anécdota):** los años 70 se marcan con la programación estructurada; los 80 se bifurcan entre lenguajes y gestión; los 90 con la orientación a objetos (Smalltalk-80); los 2000 con las palabras de moda (*cloud*, IoT, microservicios, *digital twins*). Él dice que hay que ir acumulando términos y verificar cuáles sobreviven.

## 3. Qué es el software (la definición que te van a pedir)
Software = **tres cosas**, no solo código:
1. **Instrucciones** (programas) que, al ejecutarse, dan funciones, características y desempeño.
2. **Estructuras de datos** que permiten a los programas manipular la información.
3. **Información descriptiva** (documentación) sobre su operación y uso.

Y tiene un **rol dual**:
- Para el ingeniero es un **producto**.
- Para el usuario es una **herramienta** para generar otro producto: una orden de compra, una venta, un inventario.

El software entrega **información**. El profesor la explica con una escalera:

**Dato → Información → Conocimiento → Sabiduría**
- *Dato* es algo bruto.
- *Información* son datos con sentido.
- *Conocimiento* es la información que una persona ya interiorizó.
- *Sabiduría* es decidir con base en ese conocimiento.

> 🔎 **Buscar en internet:** *"DIKW pyramid data information knowledge wisdom"*. Es el modelo que el profesor usó para explicar la escalera. Hay buenas explicaciones en inglés y en español.

## 4. Qué es ingeniería
Ingeniería es el trabajo que toma la comprensión del mundo natural para **inventar, diseñar y construir** cosas que resuelven problemas prácticos. El ingeniero civil construye puentes, el naval barcos, el aeronáutico aviones. El ingeniero de software construye algo **abstracto**: no obedece leyes físicas, lo escriben personas para personas.

## 5. La definición de ingeniería de software (la que hay que memorizar)
Hay dos definiciones que el profesor usa como referencia. Puedes usar cualquiera, o una propia **si citas la fuente**.

> **SWEBOK:** define la ingeniería de software como la aplicación de un enfoque sistemático, disciplinado y cuantificable al desarrollo, la operación y el mantenimiento del software.

> **Sommerville:** la describe como una disciplina de ingeniería que cubre todos los aspectos de la producción de software, desde la especificación inicial hasta el mantenimiento cuando el sistema ya está en uso.

**Palabras clave del profesor:**
- **Sistemático:** no hacer las cosas al azar o por instinto. Tener un conjunto definido de herramientas y ejecutarlas en orden.
- **Cuantificable:** medir costo, plazo y calidad.
- **Desarrollo, operación y mantenimiento:** no solo desarrollo.

> 🔎 **Buscar en SWEBOK v4:** pág. 38 (sección 1 de la Introducción). Compara esa definición con la de arriba y fíjate en las palabras *sistemático*, *disciplinado* y *cuantificable*. ⚠️ Corrección: la primera área del SWEBOK es Requisitos (pág. 44); Professional Practice es la KA 14 (pág. 274).

> 🔎 **Buscar en Sommerville:** capítulo 1, sección *Software engineering*. Lee las primeras dos páginas.

## 6. Por qué es importante (dar dos razones)
1. **Permite construir sistemas complejos a tiempo, dentro del presupuesto y con calidad.** Hay un conflicto constante entre costo, calidad y plazo: si quieres el producto en tres meses, necesitas tres personas; si lo quieres en un mes, necesitas cinco. La IS te permite ver y justificar esa decisión.
2. **Es más barata a largo plazo.** No diseñar ni probar parece barato al inicio, pero si el software vive diez años, esas decisiones te cobran después.

Además: la IS **impone disciplina** a un trabajo que tiende al caos, pero **sin camisa de fuerza**. Los métodos son una **caja de herramientas**: eliges cuál sirve en cada momento.

## 7. Qué es calidad de software
> **Definición (Pressman):** capacidad del producto para satisfacer las **necesidades expresadas e implícitas** de los stakeholders, bajo condiciones específicas.

Dos ideas clave del profesor:
- **La calidad no es solo cumplir la especificación.** Si la especificación no refleja lo que el cliente espera, cumplirla no basta.
- **Ejemplo de los zapatos:** dos zapatos sirven para caminar y para jugar fútbol, pero uno es más cómodo. La comodidad no es funcionalidad: es un atributo de calidad que complementa la funcionalidad.

> 🔎 **Buscar en SWEBOK v4:** pág. 248 (KA 12, *Software Quality Fundamentals*). Busca la definición de calidad y los atributos de calidad.

## 8. Quién es el stakeholder
> **Stakeholder:** cualquiera que tenga interés en el éxito del proyecto. Pueden ser el dueño de la empresa, quien lo usa, quien patrocina la compra, el equipo de desarrollo o el soporte.

Hay stakeholders **positivos y negativos**. Algunos quieren que el proyecto fracase. Más adelante verás el mapa de stakeholders.

## 9. El proceso de software: cómo se organiza el trabajo
Un **proceso** es una secuencia de actividades que produce un producto de software.
- **Actividad:** objetivo amplio (comunicación con stakeholders).
- **Acción:** conjunto de tareas que produce un producto de trabajo grande (diseño arquitectónico).
- **Tarea:** objetivo pequeño y concreto (una prueba unitaria).

**Las cuatro actividades comunes a todo proceso (Sommerville):**
1. **Especificación:** qué software y con qué restricciones.
2. **Desarrollo:** diseño y programación.
3. **Validación:** comprobar que es lo que el cliente necesita.
4. **Evolución:** modificar el software cuando cambian las necesidades.

**Las cinco actividades del marco genérico (Pressman y Maxim):**
**Comunicación → Planificación → Modelado → Construcción → Despliegue.**

> 🔎 **Buscar en Pressman:** capítulo 2, *Software Engineering*. Busca la lista de cinco actividades y compara con la de Sommerville. Notarás que la de Pressman tiene un inicio más de cliente.

> 🔎 **Buscar en Sommerville:** capítulo 2, *Software processes*, sección *Software process activities*.

**Clave:** el proceso **no es una receta rígida**. Se adapta al problema, al proyecto, al equipo y a la cultura de la organización.

## 10. Un ejemplo que el profesor usa mucho: la cadena de la mala comunicación
Lo que el usuario necesita → lo que escribe el ingeniero de requerimientos → lo que diseña el arquitecto → lo que programa el programador. Cada eslabón cambia algo. El resultado final puede no tener nada que ver con la necesidad inicial.

La ingeniería de software busca que esa cadena sea **armónica**, no que el programador termine haciendo algo distinto.

---

## Autoevaluación (responde sin mirar)
1. Define ingeniería de software en 2-3 líneas. Cita la fuente.
2. Da dos razones por las que es importante.
3. ¿Qué tres cosas forman el software según Pressman?
4. Explica la diferencia entre dato, información, conocimiento y sabiduría con un ejemplo.
5. ¿Cuáles son las cuatro actividades comunes a todo proceso de software?
6. ¿Qué es calidad de software? Usa el ejemplo de los zapatos.

## Lo que no entra en esta guía
La historia detallada de los lenguajes de programación (solo importan las fechas de la crisis y los saltos conceptuales).
