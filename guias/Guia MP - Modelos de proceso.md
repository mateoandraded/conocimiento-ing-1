# Guía MP — Modelos de proceso de software

> **Léela de corrido.** Esta guía se basa **solo en los slides** (deck 02). No tengo transcripción de la clase correspondiente, así que cuando el profesor haya dicho algo que no aparece en los slides, esta guía no lo recoge.

## 1. Qué es un modelo de proceso
Un **modelo de proceso** (también llamado SDLC o *ciclo de vida*) es una representación **simplificada** del proceso de software. Cada modelo muestra el proceso desde una perspectiva y, por eso, solo da información parcial. Por ejemplo, un diagrama de actividades muestra qué se hace y en qué orden, pero no quién lo hace.

Son **marcos**, no recetas: se extienden y adaptan para crear procesos específicos.

> 🔎 **Buscar en Sommerville:** capítulo 2 (*Software processes*), sección *Software process models*. Lee la primera página, que compara modelos.

## 2. Cascada (waterfall)
**Idea:** etapas en secuencia. Cada etapa debe estar completa y correcta antes de pasar a la siguiente.

- Se publicó por primera vez en **1970**, derivado de procesos de ingeniería de sistemas militares.
- Es un **proceso dirigido por plan**: planificas y programas todas las actividades antes de empezar.
- El producto **no se entrega hasta la prueba de aceptación** del sistema completo.

**Cuándo sirve:**
- Sistemas **embebidos**, donde el software depende del hardware.
- Sistemas **críticos**, donde hay que analizar seguridad y riesgos antes de construir.
- Sistemas grandes desarrollados por **varias empresas**, que necesitan especificaciones completas.

**Cuándo no sirve:** cuando los requerimientos cambian rápido y la comunicación informal es posible.

**Debilidades:** lento, el retrabajo es costoso, las pruebas quedan al final, el cliente solo participa al inicio y al final, y los requerimientos deben estar claros desde el principio (algo difícil de lograr).

> 🔎 **Buscar en internet:** *"Royce 1970 Managing the Development of Large Software Systems"*. Es el artículo que se cita como origen de la cascada. Léele el resumen y la figura principal. Verás que Royce describe limitaciones del modelo, no solo sus ventajas.

## 3. Modelo V
Es una **variante de la cascada**. Las etapas de la izquierda (requerimientos, diseño, construcción) tienen su equivalente de prueba a la derecha. Cada prueba valida el modelo correspondiente.

> Clave para el examen: el modelo V es cascada con énfasis en el control de calidad.

## 4. Incremental
**Idea:** entregar el sistema en **partes funcionales** (incrementos). La **primera parte es el núcleo del producto**: los requerimientos básicos, con muchas funciones adicionales pendientes.

- El cliente usa el núcleo o lo evalúa, y con esa experiencia se planifica el siguiente incremento.
- Es un **término medio** entre cascada y evolutivo.

**Ventajas:** entregas tempranas, cada fase necesita menos recursos, se reduce el riesgo, y los servicios más importantes se prueban primero.

**Desventajas:** el producto final puede tardar más y costar más; cuesta definir incrementos que sean útiles por sí solos; la estructura se degrada con cada incremento.

## 5. Modelos evolutivos
**Idea:** el sistema se construye en **versiones cada vez más completas**. Se usan cuando los requerimientos cambian durante el desarrollo o cuando hay que entregar algo limitado por presión comercial.

### 5.1 Prototipado
1. **Comunicación:** definir objetivos y requerimientos conocidos.
2. **Diseño rápido:** enfocado en lo que el usuario ve (interfaz, salidas).
3. **Prototipo:** se construye y los stakeholders lo evalúan.
4. **Iteración:** se ajusta según la retroalimentación.

**Problema que señala el profesor:** el cliente puede creer que el prototipo es el sistema real. Y el ingeniero puede tomar decisiones rápidas (lenguaje, algoritmo) que después nadie revisa.

> 🔎 **Buscar en Pressman:** capítulo 4 (*Process models*), sección *Prototyping*. Compara su figura con la de este resumen.

### 5.2 Espiral (Boehm)
**Idea:** combina el carácter iterativo del prototipado con el control sistemático de la cascada. Es un **generador de modelos guiado por riesgo**: en cada vuelta de la espiral se reduce el riesgo y se aumenta el grado de definición.

Tiene **hitos de anclaje** que aseguran el compromiso de los stakeholders con una solución factible.

> 🔎 **Buscar en internet:** *"Boehm 1988 A spiral model of software development and enhancement"*. El artículo es corto y tiene la figura original.

## 6. Modelos concurrentes
Representan las actividades como **estados** que cambian por eventos. Por ejemplo, durante el diseño puede aparecer una inconsistencia en el modelo de requerimientos. Ese evento dispara una transición de estado en la actividad de requerimientos.

Se usa cuando el **cronograma es crítico**.

## 7. Desarrollo basado en componentes (CBSE)
**Idea:** construir reutilizando **componentes** independientes, con interfaces bien definidas, e integrarlos en un marco común.

- Los componentes pueden ser **servicios web**, **colecciones de objetos** para un framework (.NET, JEE) o **sistemas comerciales listos para usar (COTS)**.
- Hay un **modelo de componentes** que define estándares de implementación, documentación y despliegue (ejemplos: EJB, .NET, CORBA).

**Ventajas:** menos software que escribir, menos costo y riesgo, entregas más rápidas.
**Limitaciones:** pierdes control sobre la evolución si las versiones de los componentes no las controla tu organización; y ajustar los requerimientos a los componentes puede dar un sistema que no es lo que el usuario necesita.

> 🔎 **Buscar en SWEBOK v4:** pág. 93 (KA 3, sección 5.6, *Component-Based Design*). Para modelos y métodos en general: pág. 233 (KA 11).

## 8. RUP (Rational Unified Process)
**Idea:** separa las **fases** de las **actividades**. Las actividades (requerimientos, análisis, diseño, implementación, pruebas) se repiten en cada fase con distinto énfasis.

Las **cuatro fases:**
1. **Inception (inicio):** caso de negocio, arquitectura preliminar, plan iterativo.
2. **Elaboration (elaboración):** entender el dominio, refinar casos de uso, arquitectura.
3. **Construction (construcción):** diseño, programación y pruebas. Se construyen los componentes de cada caso de uso.
4. **Transition (transición):** despliegue, pruebas beta, manuales y soporte.

> 🔎 **Buscar en Pressman:** capítulo 4, sección *Unified Process*. Es mejor leer la tabla de fases que la explicación larga.

## 9. Desarrollo ágil
**Por qué surge:** los negocios cambian rápido y es casi imposible tener un conjunto estable de requerimientos desde el inicio. Los métodos ágiles aparecen a finales de los 90: **XP (1999)**, **Scrum (2001)** y **DSDM (2003)**.

**Filosofía:**
- Satisfacción del cliente con **entregas tempranas e incrementales**.
- Equipos pequeños y muy motivados.
- Métodos informales, productos de trabajo mínimos.
- **Entregar valor antes que analizar en exceso**, sin descartar el análisis.

**Características:**
- Especificación, diseño e implementación van **entrelazados**.
- El sistema se entrega en **incrementos**, y los usuarios participan en cada uno.
- Usa **herramientas** de soporte (pruebas automáticas, control de versiones, integración continua).

### Historias de usuario
En ágil no hay una actividad separada de requerimientos. La herramienta es la **historia de usuario**: un escenario de uso escrito en una tarjeta.
- Es fácil de entender para todos (ventaja).
- Es difícil saber si cubren todos los requerimientos esenciales; los usuarios expertos a menudo omiten lo que les parece obvio (desventaja).

> 🔎 **Buscar en el libro de Cohn:** *User Stories Applied*, busca el capítulo sobre la estructura de una historia. Busca el formato *As a… I want… So that…*.

> 🔎 **Buscar en Sommerville:** capítulo 3 (*Agile software development*). Ahí están los principios del manifiesto.

## 10. Ágil frente a dirigido por plan
Esto es clave para elegir modelo. El profesor lo presenta como cuatro grupos de factores:

**Sistema:**
- ¿Qué tan grande es? El ágil funciona mejor con equipos pequeños que se comunican informalmente.
- ¿Requiere mucho análisis antes de programar (tiempo real, requerimientos complejos)? Entonces conviene el dirigido por plan.
- ¿Cuánto vivirá? Los sistemas de larga vida necesitan más documentación para el equipo de soporte.
- ¿Está regulado? Si un regulador debe aprobarlo, hace falta documentación detallada.

**Equipo:**
- ¿Qué tan buenos son los desarrolladores? El ágil exige más habilidad.
- ¿Está distribuido o tercerizado? Entonces necesitas documentos de diseño.
- ¿Qué herramientas tienen?

**Organización:**
- ¿Hace falta una especificación detallada por contrato? Entonces puedes usar un proceso dirigido por plan para requerimientos y ágil para la construcción.
- ¿Es realista una entrega incremental? ¿El cliente tiene tiempo para participar?
- ¿La cultura de la organización es de ingeniería tradicional?

> 🔎 **Buscar en internet:** *"David Boddy project profile tool life cycle"*. Es la herramienta que el profesor cita para elegir el ciclo de vida. Busca una explicación corta.

## 11. Cómo elegir el modelo (la respuesta que pide el profesor)
- **Cascada:** proyectos pequeños o medianos, requerimientos bien entendidos, restricciones claras de tiempo y costo.
- **Incremental:** proyectos que se pueden dividir en mini-proyectos, alto riesgo o escasez de recursos.
- **Evolutivo:** requerimientos inciertos y calidad más importante que tiempo o costo. **No** sirve para sistemas críticos ni regulados.
- **Híbrido:** cuando hay una arquitectura estable pero queda incertidumbre.

**Forma de responder en examen:** primero identifica las características del proyecto (tamaño, incertidumbre de requerimientos, regulación, equipo), luego elige el modelo y justifica con dos o tres de esas características.

---

## Autoevaluación (responde sin mirar)
1. ¿Por qué la cascada sirve para sistemas embebidos?
2. ¿Qué problema tiene el prototipado para el cliente?
3. ¿Qué es un modelo de proceso y por qué es simplificado?
4. ¿Qué ventaja tiene el incremental frente a la cascada?
5. Un proyecto tiene requerimientos inciertos y un cliente que quiere ver avances cada dos semanas. ¿Qué modelo elegirías y por qué?
6. ¿Qué es una historia de usuario y qué debilidad tiene?

## Lo que no entra en esta guía
Las lecturas de componentes específicos (EJB, CORBA) y los detalles de cada framework ágil más allá de su filosofía.
