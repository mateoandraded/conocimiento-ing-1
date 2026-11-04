# Guía S03 — Requerimientos funcionales y no funcionales

> **Léela de corrido.** Este es el tema con más preguntas de examen. Los bloques **🔎** indican dónde buscar. Fecha de la sesión: 2026-10-05.

## 1. Qué es un requerimiento
Un **requerimiento** es una descripción de:
- los **servicios** que el sistema debe proveer, y
- las **restricciones** de su operación.

**Ingeniería de requerimientos** es el proceso de *descubrir (finding out), analizar, documentar y verificar* esos servicios y restricciones.

El profesor insiste en una diferencia de vocabulario: en español hablamos de "requerimientos" y "requisitos" como si fueran lo mismo. En este curso, **requerimiento** es el término técnico.

> 🔎 **Buscar en SWEBOK v4:** pág. 44 (KA 1, *Software Requirements Fundamentals*). Compara la definición de *requirement* con la de arriba.

## 2. Requerimientos de usuario y de sistema
Esta distinción es de Sommerville:
- **Requerimientos de usuario:** de alto nivel, en **lenguaje natural** (con diagramas si hace falta). Describen el **problema** y los servicios que el usuario espera. Si alguien no técnico no los entiende, están mal escritos.
- **Requerimientos de sistema:** detallados. Describen la **solución**: qué implementar exactamente. Un requerimiento de usuario puede convertirse en varios de sistema.

**Ejemplo del profesor (Mentcare):**
- Usuario: *el sistema generará reportes mensuales de costos de medicamentos prescritos por clínica.*
- Sistema: el último día laborable del mes se genera el resumen; se separa un reporte por dosis; el acceso está restringido a usuarios autorizados.

> 🔎 **Buscar en Sommerville:** capítulo 4 (*Requirements engineering*), sección *User and system requirements*. Lee la tabla comparativa.

## 3. Por qué la ingeniería de requerimientos es difícil
El profesor da una lista. Te la van a pedir de memoria, así que tradúcela a tu manera:
1. **Los stakeholders no saben lo que quieren**, o no lo pueden expresar.
2. **Creen que algo es obvio** porque lo hacen todos los días, y no lo escriben.
3. **Creen que saben lo que quieren hasta que les entregas lo que pidieron.** Y después dicen "eso no era lo que necesitaba".
4. **El analista cree que entiende el problema mejor que el cliente.** Mala idea.
5. **Nunca sabemos si tenemos todos los requerimientos.** La lista siempre crece después de la entrega.
6. **Los stakeholders tienen puntos de vista distintos** que pueden entrar en conflicto.
7. **El negocio cambia** (normativa, competencia, tecnología).
8. **Se piensa en la solución antes que en el problema.** En requerimientos hablamos del *qué*, no del *cómo*.
9. **El ingeniero no entiende el dominio** y propone una solución inadecuada.
10. **Los requerimientos se escriben desde cero** y no hay límites físicos. Por eso hay que conocer lo que es posible dentro de presupuesto y plazo.

> 🔎 **Buscar en Sommerville:** capítulo 4, sección *Requirements elicitation and analysis*. Compara con la lista.

## 4. Principios de comunicación (Pressman)
Estos son los diez principios que el profesor cita para conversar con el cliente. Te los van a pedir ordenados, así que aprende la regla mnemotécnica:

**Escuchar → Prepararse → Facilitar → Cara a cara → Notas**
**Colaborar → Modularizar → Dibujar → Avanzar → Negociar**

Dos ideas importantes:
- **Principio 9 (avanzar):** si acuerdas algo, avanza; si no acuerdas algo, avanza; si no se puede aclarar en el momento, avanza. No te estanques.
- **Principio 10 (negociar):** la negociación **no es una competencia**. Funciona cuando las dos partes ganan.

> 🔎 **Buscar en Pressman:** capítulo 7 (*Principles that guide practice*). Busca el apartado de **comunicación**.

## 5. Requerimientos funcionales (RF)
**Definición:** servicios que el sistema provee, cómo reacciona ante entradas y cómo se comporta en situaciones específicas. También pueden decir lo que el sistema **no** debe hacer.

**Son los más fáciles de identificar.** Siempre que se pueda, expresarlos con números o condiciones concretas, para evitar conflictos con el cliente.

Ejemplos del profesor:
- "Un usuario debe poder buscar las citas de todos los departamentos del hospital."
- "Cada empleado se identifica con su número de empleado de **8 dígitos**."
- "El profesor puede ingresar notas hasta **una semana** después del examen."
- "El sistema **no** debe permitir que un profesor altere una nota **24 horas** después de registrarla."

> 🔎 **Buscar en Pressman:** capítulo 8 (*Understanding requirements*), sección sobre requerimientos funcionales.

## 6. Requerimientos no funcionales (RNF)
**Definición:** restricciones sobre los servicios o funciones del sistema. Incluyen restricciones de tiempo, del proceso de desarrollo y de estándares.

**Diferencia clave:** un RF afecta a un módulo o a un rol (por ejemplo, descargar una lista de asistencia solo afecta al profesor). Un RNF afecta a **todo el sistema** de forma transversal (por ejemplo, cumplir la Ley Orgánica de Protección de Datos afecta a todos los módulos).

**Un RNF puede generar RF.** Ejemplo: "el sistema debe ser accesible solo para usuarios autorizados" (RNF de seguridad) implica:
- una pantalla para actualizar la lista de usuarios autorizados,
- el rechazo a usuarios no autorizados con un mensaje,
- una comparación de las credenciales contra la lista.

> 🔎 **Buscar en internet:** *"ISO/IEC/IEEE 29148 requirements quality characteristics"*. La norma es la que el curso cita para especificaciones; mira las características de un buen requerimiento (correcto, no ambiguo, verificable, consistente, completo).

## 7. La taxonomía de Sommerville (la que hay que memorizar)
El profesor dice: *"Debe aprendérsela, no solo para este curso."* Tiene tres grandes grupos. Memoriza la sigla **P-O-E**: Producto, Organizacional, Externo.

### 7.1 Producto (el sistema en sí)
- **Eficiencia:** desempeño (cuánto tarda, cuántas transacciones soporta) y espacio (cuánta memoria o almacenamiento usa).
- **Usabilidad:** qué tan fácil es de usar y qué tan tolerante es a errores.
- **Dependability (confiabilidad en sentido amplio):** disponibilidad, fiabilidad (*reliability*), robustez, reparabilidad, mantenibilidad. Ver sección 8.
- **Seguridad:** resistencia a intrusiones deliberadas o accidentales.

### 7.2 Organizacional (la empresa que construye o usa el sistema)
- **Ambiente:** plataforma de operación y portabilidad.
- **Operacional:** tiempo y costo de entrega, cómo se usa el sistema, interoperabilidad con otros sistemas.
- **Desarrollo:** lenguaje, método de diseño, estándares de proceso y herramientas obligatorias.

### 7.3 Externo (lo que viene de afuera)
- **Regulatorio:** organismos que regulan el sector (en Ecuador: Ministerio de Salud, IESS, SRI).
- **Ético:** aceptable para el cliente y el público; por ejemplo, un código de ética profesional.
- **Legislativo:** leyes (contabilidad, seguridad, protección de datos). El profesor separa **seguridad** (cosas y datos) de **safety** (personas).

> 🔎 **Buscar en Sommerville:** capítulo 4, sección *Non-functional requirements*. Compara sus tablas con esta lista.

## 8. Dependability: la familia de las "-ilidades"
El slide muestra cinco propiedades principales. Sus definiciones exactas del slide:
| Propiedad | Definición | En palabras del profesor |
|---|---|---|
| **Availability** | Entregar servicios **cuando se solicitan** | "Está ahí": lo consulto y está arriba |
| **Reliability** | Entregar servicios **como se especificaron** | El resultado es exacto, "ni de más ni de menos" |
| **Safety** | Operar **sin fallas catastróficas** | Personas: semáforos, cuidados intensivos |
| **Security** | Protegerse de **intrusiones** | Seguridad informática, de cosas y datos |
| **Resilience** | **Resistir y recuperarse** de eventos dañinos | Adaptarse y seguir funcionando (la planta que dobla el tallo para buscar luz) |

**Propiedades relacionadas:**
- **Reparability:** diagnosticar y reparar rápido.
- **Maintainability:** adaptarse a cambios sin introducir errores.
- **Error tolerance:** evitar y tolerar errores del usuario.
- **Robustez:** si se cae, se levanta (por ejemplo, componentes redundantes de distinto proveedor).
- **Antifragilidad:** no solo recuperarse, sino aprender y salir más fuerte. Es extra del profesor.

> ⚠️ **Confusión que el profesor corrigió:** en clase describió una vez "reliability" como adaptarse y seguir. Según el slide, eso es **resilience**. En examen usa las definiciones del slide.

> 🔎 **Buscar en Sommerville:** capítulo 10 (*Dependable systems*), sección *Dependability properties*. Lee la figura de las cinco propiedades.

> 🔎 **Buscar en internet:** *"availability vs reliability difference"* y *"resilience vs robustness software"*. Hay diagramas muy claros para comparar.

## 9. Métricas para RNF
El profesor insiste en que **un RNF sin métrica es ambiguo**. Las métricas típicas:
- **Velocidad:** transacciones por segundo, tiempo de respuesta, tiempo de refresco de pantalla.
- **Tamaño:** megabytes, número de chips de memoria.
- **Facilidad de uso:** tiempo de entrenamiento, número de pantallas de ayuda.
- **Reliability:** MTTF (tiempo medio entre fallas), probabilidad de no disponibilidad, tasa de fallas, disponibilidad.
- **Robustez:** MTTR (tiempo medio de reinicio), porcentaje de eventos que causan falla, probabilidad de corrupción de datos.
- **Portabilidad:** porcentaje de sentencias dependientes de plataforma, número de plataformas.

> 🔎 **Buscar en internet:** *"MTTF MTTR MTBF definition"*. Hay muchas definiciones; se confunden mucho en examen.

## 10. Plantillas para escribir RNF (cómo "mapear" en examen)
El profesor dice: aprende **dos ejemplos por tipo** y luego ajústalos al contexto del examen. Un ejemplo con su clasificación:

| RNF del slide | Tipo |
|---|---|
| El operador debe usar el sistema con media hora de entrenamiento | Producto · usabilidad |
| Las respuestas a estimaciones deben tomar menos de 2 segundos | Producto · eficiencia · desempeño |
| Disponible el 99 % del tiempo entre 08h00 y medianoche | Producto · dependability · availability |
| Las mejoras deben completarse en una semana | Producto · dependability · maintainability |
| El tiempo promedio de respuesta debe ser menor a 5 segundos | Producto · eficiencia · desempeño |
| El sistema debe estar disponible para el inicio del proyecto XYZ | Organizacional · operacional · entrega |
| Usar la librería de clases del servidor de desarrollo | Organizacional · desarrollo |
| Operar sobre Windows 11 y Linux | Organizacional · ambiente · portabilidad |
| Solo usuarios autorizados pueden acceder | Producto · seguridad |
| Cumplir la ley de protección de datos | Externo · legislativo |

**Errores que el profesor castiga:**
- "99 %" sin periodo (¿anual?, ¿mensual?, ¿continuo?). En un año, 1 % son unos 3,65 días de caída, que podrían caer justo en día de pago.
- "Buen desempeño" sin número.
- Decir "mi cliente no tiene RNF". Hay que provocarlos: siempre hay alguno.

> 🔎 **Buscar en el libro de Robertson:** *Mastering the Requirements Process*, capítulos que el profesor pidió (1, 10, 11, 14, 16, 17). Ahí está el detalle de cómo escribir requerimientos verificables.

## 11. Ambigüedad, omisión y conflicto (el ejercicio típico de examen)
- **Ambigüedad:** algo que puede interpretarse de distintas maneras.
- **Omisión:** algo que no está. Se menciona un cálculo o un valor, pero no se dice cómo calcularlo o qué valor es.
- **Conflicto:** dos partes del texto se contradicen.

**Forma de responder:** tipo + línea + texto citado + por qué es un problema + (opcional) cómo corregirlo.

**Ejercicio de la clase (biblioteca).** Léelo y busca 8 problemas antes de mirar la solución en [[Ambigüedad, omisión y conflicto]]:
> *Un estudiante podrá extender el periodo de préstamo de libros en préstamo en cualquier momento. El sistema puede aprobar o rechazar una extensión y debe notificar al prestamista de su decisión. El sistema debe estar disponible a toda hora.*

**Regla de redacción:** no uses sinónimos. Si escribiste "email", no escribas después "correo electrónico". Si escribiste "aprobación", no escribas "autorización".

## 12. Elicitación (cómo se descubren los requerimientos)
La clase solo empezó este tema. Lo que quedó:
- **Etnografía:** observar el trabajo. **Pasiva** (observas sin interrumpir) o **activa** (haces el trabajo y aprendes haciéndolo). Ventaja: descubre el proceso real y los requerimientos implícitos. Desventaja: consume tiempo y da una visión parcial.
- **Entrevistas:** casi siempre estructuradas, con una agenda preparada. Evita preguntas que inducen la respuesta, subjetivas o impositivas. Pide permiso para grabar, toma notas, genera un acta y que el entrevistado la apruebe.

> 🔎 **Buscar en Sommerville:** capítulo 4, sección *Requirements elicitation and analysis*. Hay una explicación de la etnografía con ejemplos.

> ⏳ **Próximamente:** cuestionarios, talleres, prototipos e **historias de usuario**. No hay guía todavía. Cuando llegue la sesión, se crea otra guía.

## 13. SWEBOK (esta sesión lo mencionó como control de lectura)
El profesor pidió leer el SWEBOK para poder definir en 2-3 líneas áreas como *software configuration management*, *software quality* o *software engineering economics*. No lo leas de corrido: busca cada término en el índice y lee solo esa sección.

> 🔎 **Buscar en SWEBOK v4:** págs. 43–44 (KA 1). Las áreas *software configuration management*, *software quality* y *software engineering economics* están en las págs. 186 (KA 8), 248 (KA 12) y 289 (KA 15).

---

## Autoevaluación (responde sin mirar)
1. Define requerimiento funcional y requerimiento no funcional. Da un ejemplo de cada uno.
2. ¿Qué significan P, O y E en la taxonomía de Sommerville? Da un ejemplo de RNF externo.
3. ¿Cuál es la diferencia entre *availability* y *reliability*?
4. Un texto dice: *"El sistema debe estar disponible el 99 % del tiempo."* ¿Qué le falta?
5. Clasifica: *"Las consultas deben responder en menos de un segundo."*
6. ¿Qué es una ambigüedad y qué es una omisión? Da un ejemplo de cada una.
7. Da dos razones por las que la ingeniería de requerimientos es difícil.

## Lo que no entra en esta guía
- La historia de la ingeniería de requerimientos antes de los años 90.
- Los detalles de las normas ISO más allá de sus características de calidad.
