---
tipo: concepto
curso: Ingeniería de Software I
fuente: "02 Process Models (80 p.)"
temario: "1.4 y 1.5 — 1.ª evaluación"
---
# Modelos de proceso de software

**En una línea:** formas de organizar las actividades del [[Proceso de software]]; se elige el que más valor agregue según el proyecto.

## Resumen comparativo
| Modelo | Idea | Úsalo cuando | Debilidades |
|---|---|---|---|
| **Cascada** (1970, plan-driven) | Etapas en secuencia; cada una completa antes de la siguiente | Requerimientos claros y estables; sistemas **embebidos**, **críticos** (análisis de safety/security), o grandes con varias empresas socias; proyectos pequeños parecidos a otros | Lento, retrabajo, pruebas solo al final, cliente solo al inicio y al final, producto entregado al final |
| **Modelo V** | Variante de cascada: cada etapa de la izquierda tiene su prueba a la derecha | Igual que cascada, con énfasis en QA | Igual que cascada |
| **Incremental** | Entregas parciales usables; la 1.ª es el **producto núcleo** | Se necesita funcionalidad pronto; proyectos divisibles en mini-proyectos; alto riesgo o pocos recursos | Más largo y caro en total; difícil definir incrementos; proceso poco visible; la estructura se degrada |
| **Evolutivo: prototipado** | Comunicación → diseño rápido → prototipo → retroalimentación | Requerimientos poco claros (UI, algoritmos complejos) | El cliente cree que el prototipo es el sistema; decisiones "rápidas" que se quedan |
| **Evolutivo: espiral** (Boehm) | Iterativo + controlado; **dirigido por riesgo**; *anchor point milestones* | Proyectos grandes con riesgo alto | Requiere experiencia en gestión de riesgo |
| **Concurrente** | Actividades con estados que cambian por eventos | El cronograma es crítico | Complejo de gestionar |
| **Basado en componentes (CBSE)** | Reutilizar componentes/COTS y integrarlos | Portafolio de sistemas; hay componentes reutilizables | Pérdida de control de la evolución; ajustar requerimientos a componentes |
| **RUP** | Separa **fases** (Inception, Elaboration, Construction, Transition) de actividades; iterativo e incremental | Proyectos medianos/grandes orientados a casos de uso | Pesado |
| **Ágil** (XP 1999, Scrum 2001, DSDM) | Entregas incrementales, equipos pequeños, comunicación continua, historias de usuario | Sistemas pequeños/medianos, pocos stakeholders, sin contrato fijo, documentación poco importante | Choca con contratos legales, mantenimiento, equipos distribuidos |

## RUP — fases
1. **Inception:** caso de negocio, comunicación + planificación, arquitectura preliminar.
2. **Elaboration:** entender el dominio y la arquitectura; refinar casos de uso.
3. **Construction:** diseño, programación y pruebas.
4. **Transition:** despliegue, beta testing, manuales.

## Ágil vs. dirigido por plan — factores (Sommerville)
- **Sistema:** tamaño, tipo (¿requiere mucho análisis previo?), vida útil esperada, ¿regulación externa?
- **Equipo:** habilidad de los desarrolladores, ¿distribuido o tercerizado?, herramientas disponibles.
- **Organización:** ¿se necesita especificación detallada por contrato?, ¿entrega incremental realista y cliente disponible?, cultura de la organización.

## Cómo elegir (slide "Choosing the best life-cycle")
- **Cascada:** proyectos pequeños/medianos, requerimientos bien entendidos, restricciones de tiempo y costo.
- **Incremental:** proyectos divisibles, alto riesgo o escasez de recursos; requerimientos generales entendidos.
- **Evolutivo:** requerimientos inciertos; la calidad pesa más que tiempo/costo; **no** para sistemas críticos o regulados.
- **Híbrido:** arquitectura estable pero con incertidumbre.

## Cómo lo puede preguntar el profesor
- Dado un proyecto, **elegir y justificar** el modelo de proceso (objetivo 1 del curso: "identificar un modelo que agregue valor analizando el proyecto").
- Ventajas/desventajas de un modelo.

## Relacionado
- [[Proceso de software]] · [[Elicitación de requerimientos]] (historias de usuario)
