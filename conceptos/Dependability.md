---
tipo: concepto
curso: Ingeniería de Software I
fuente: "03a Requirements Engineering p. 25-29 (Sommerville fig. 10.1); Sesión 03"
---
# Dependability

**En una línea:** la familia de "-ilities" que hacen que un sistema sea digno de confianza.

## Las 5 propiedades principales (Sommerville, fig. 10.1)
| Propiedad | Definición del slide | En palabras del profesor |
|---|---|---|
| **Availability** | Capacidad de entregar servicios **cuando se solicitan** | "Está ahí": lo consulto y está arriba |
| **Reliability** | Capacidad de entregar servicios **como se especificaron** | El resultado es exacto, "ni de más ni de menos" (calculadora de impuestos) |
| **Safety** | Operar **sin falla catastrófica** | Seguridad de **personas**: semáforos, UCI, torre de control |
| **Security** | Protegerse de **intrusión deliberada o accidental** | Seguridad informática, de las **cosas** |
| **Resilience** | **Resistir y recuperarse** de eventos dañinos | Adaptarse y continuar (la planta que dobla el tallo) |

## Propiedades relacionadas
- **Repairability:** diagnosticar y reparar rápido (mejor con acceso al código fuente).
- **Maintainability:** adaptarse económicamente a nuevos requerimientos con baja probabilidad de introducir errores.
- **Error tolerance:** (parte de usabilidad) evitar y tolerar errores de entrada del usuario.
- **Robustez:** "si se cae, se levanta" — redundancia (componente primario y secundario de distinto proveedor y tecnología, como en aviones o satélites).
- **Antifragilidad** (extra del profesor): no solo recuperarse, sino **aprender y salir más fuerte**.

## Se confunde con
- **Availability vs. reliability:** puede estar disponible y dar resultados incorrectos (disponible pero no confiable).
- **Safety vs. security:** personas vs. cosas/datos.
- **Resilience vs. robustness:** resiliencia = se adapta y sigue sin caerse; robustez = se cae y se levanta.
- ⚠️ En la Sesión 03 el profesor describió en un momento "reliability" como adaptarse y continuar: eso es **resilience** según el slide. En el examen, usar las definiciones del slide.

## Métricas
MTTF, MTTR (tiempo de reinicio), probabilidad de no disponibilidad, tasa de fallas (ROCOF), % de disponibilidad en una franja y para un % de usuarios, probabilidad de corrupción de datos, tasa de defectos (defectos/FP).

## Relacionado
- [[Taxonomía de RNF de Sommerville]]
