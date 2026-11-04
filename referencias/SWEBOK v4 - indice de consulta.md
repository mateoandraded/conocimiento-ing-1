# SWEBOK v4.0a — Índice de consulta

> **Fuente:** `material/swebok-v4 (1).pdf` (411 páginas, IEEE Computer Society).
> **"pág."** = número de página del **PDF** (el que muestra el visor al abrirlo), no el número impreso dentro del libro.
> Este archivo es la referencia para todas las guías y chats del curso. Su función es **decirte dónde buscar**, no resumir el contenido.

---

## Regla de uso (para Mateo y para cualquier chat que lea este archivo)

- Cuando Mateo pida información del SWEBOK o de un libro, responder con **página + sección + término a buscar**. No extraer ni resumir el texto del PDF, salvo que Mateo lo pida de forma explícita (p. ej. "extrae la definición").
- Cuando haya que comparar dos definiciones, dar pistas (qué palabras mirar), no la comparación completa.
- No reproducir pasajes largos del PDF.

---

## 1. Mapa del PDF

| Parte | Inicio (pág.) | Qué contiene |
|---|---|---|
| Portada, prólogos, índice | 1–18 | Índice real en págs. 6–17 |
| Introducción a la Guía | 38 | Definición de software e ingeniería de software; historia breve |
| KA 1 — Requisitos de software | 44 | Fundamentos, elicitación, análisis, especificación, validación, gestión |
| KA 2 — Arquitectura de software | 67 | Descripción de arquitecturas, estilos, proceso de arquitectura |
| KA 3 — Diseño de software | 84 | Fundamentos, calidades, registro de diseños, estrategias (incluye OO y basado en componentes) |
| KA 4 — Construcción de software | 100 | Gestión, tecnologías y herramientas de construcción |
| KA 5 — Pruebas de software | 118 | Niveles, técnicas, medidas, proceso de pruebas |
| KA 6 — Operaciones de ingeniería de software | 152 | Planificación y control de la operación |
| KA 7 — Mantenimiento de software | 168 | Fundamentos, problemas clave, procesos, técnicas |
| KA 8 — Gestión de configuración (SCM) | 186 | Identificación, control de cambios, auditoría |
| KA 9 — Gestión de ingeniería de software | 205 | Planificación, riesgos, estimación, calidad, medición |
| KA 10 — Proceso de ingeniería de software | 221 | Fundamentos, ciclos de vida, evaluación y mejora del proceso |
| KA 11 — Modelos y métodos | 233 | Tipos de modelos, análisis, métodos (incluye ágiles) |
| KA 12 — Calidad de software | 247 | Fundamentos, gestión y aseguramiento de la calidad |
| KA 13 — Seguridad de software | 264 | Gestión, ingeniería, herramientas de seguridad |
| KA 14 — Práctica profesional de la ingeniería de software | 274 | Profesionalismo, códigos de ética, dinámica de equipos, comunicación, trade-off |
| KA 15 — Economía de la ingeniería de software | 289 | Propuestas, flujo de caja, valor del dinero en el tiempo, comparación de alternativas |
| KA 16 — Fundamentos de computación | 313 | Base técnica general |
| KA 17 — Fundamentos matemáticos | 345 | Base matemática |
| KA 18 — Fundamentos de ingeniería | 367 | Métodos de ingeniería, toma de decisiones, medición |

> ⚠️ **Corrección:** la primera área de conocimiento **no** es *Software Engineering Professional Practice*. La primera es **Requisitos de software (KA 1, pág. 44)**. Professional Practice es la **KA 14 (pág. 274)**.

---

## 2. Definiciones (la búsqueda que hiciste en la Sesión 02)

| Qué buscar | Dónde | Cómo buscarlo |
|---|---|---|
| **Definición de ingeniería de software** | **Pág. 38**, sección 1 de la Introducción ("What Is Software Engineering?") | Lee el párrafo que empieza con la definición de *software* y sigue con la de *software engineering*. |
| Definición de *software* (la del estándar de vocabulario) | **Pág. 38**, mismo párrafo | Fíjate en que la definición de software incluye programas, procedimientos, documentación y datos. |
| Historia de la disciplina | **Pág. 38**, mismo párrafo (palabra clave: *Historically*) | Compara con lo que dijo el profesor sobre la crisis de 1968. |
| Definición de *Software Engineering Professional Practice* | **Pág. 274** (Introducción de KA 14) | Busca la frase que define *professional practice*. |
| Profesionalismo y códigos de ética | **Págs. 275–277** | Sección 1, "Professionalism" y "Code of Ethics". |

### Para comparar las definiciones (pistas, no respuestas)
- Compara la definición de la **pág. 38** con la de **Sommerville** (capítulo 1 de su libro).
- Pregúntate: ¿qué palabras aparecen en SWEBOK y no en Sommerville? Mira especialmente *sistemático*, *disciplinado*, *cuantificable* y *operación*.
- Después, pregúntate qué parte del ciclo de vida menciona cada una. Sommerville habla de "desde la especificación hasta el mantenimiento"; SWEBOK habla de "desarrollo, operación y mantenimiento".

---

## 3. Mapa por tema del curso

### Sesión 01 — presentación del curso
| Tema | Dónde (pág.) |
|---|---|
| Ciclo de vida: la operación dura más que la construcción | KA 10, *Life Cycles* (pág. 223) · KA 7, *Maintenance Fundamentals* (pág. 168) |
| Evolución y mantenimiento | KA 7 (pág. 168 y 171 *Key Issues*) |
| Ética profesional | KA 14 (pág. 275) |
| Trabajo en equipo y roles | KA 14, *Dynamics of Working in Teams* (sección 2, pág. 282) |

### Sesión 02 — qué es la ingeniería de software
| Tema | Dónde (pág.) |
|---|---|
| Qué es ingeniería de software | Intro, pág. 38 |
| Historia / crisis del software | Intro, pág. 38 |
| Calidad de software | KA 12, *Software Quality Fundamentals* (pág. 248) |
| Stakeholder | Búscalo con Ctrl+F en KA 1 (págs. 44–59) |
| Proceso de software: actividades | KA 10, *Process Fundamentals* (pág. 230) |
| Gestión de configuración (SCM) | KA 8 (pág. 186) |
| Economía de la ingeniería | KA 15 (pág. 289; fundamentos en pág. 307) |

### Sesión de modelos de proceso
| Tema | Dónde (pág.) |
|---|---|
| Cascada (waterfall) | KA 10, *Life Cycles* (págs. 225–227) |
| Espiral (spiral) | KA 10 (págs. 225–226) |
| RUP (Unified Process) | KA 10 (págs. 226, 229) |
| Scrum | KA 10 (págs. 227–230) |
| Métodos ágiles | KA 11, *Agile Methods* (pág. 241) |
| Desarrollo basado en componentes (CBSE) | KA 3, *Component-Based Design* (pág. 93) |
| Prototipado | KA 1 (págs. 49–50 y 57) |

### Sesión 03 — requerimientos funcionales y no funcionales
| Tema | Dónde (pág.) |
|---|---|
| Fundamentos de requisitos | KA 1, pág. 44 |
| Requisitos funcionales y no funcionales | KA 1, sección 1.5, *Nonfunctional Requirements* (pág. 46) |
| Métricas de requisitos | KA 1, figura de la KA (pág. 45) y sección 1.5 (pág. 46) |
| Elicitación | KA 1, sección 2, *Requirements Elicitation* (pág. 48) |
| Historias de usuario | KA 1, elicitación (pág. 49) y especificación (págs. 54–55) |
| Análisis (ambigüedad, conflicto) | KA 1, sección 3, *Requirements Analysis* (pág. 50) |
| Especificación | KA 1, sección 4, *Requirements Specification* (pág. 52) |
| Validación | KA 1, sección 5, *Requirements Validation* (pág. 57) |
| Gestión de requisitos | KA 1, sección 6, *Requirements Management* (pág. 58) |
| Dependability (availability, reliability, safety, security, resilience) | KA 12 (intro, pág. 246–247); KA 13 (pág. 264) |
| Disponibilidad y fiabilidad (conceptos) | Búscalos con Ctrl+F: *availability* aparece en págs. 43 y 62; *reliability* en págs. 46 y 50 |

### Otros temas que aparecerán en las próximas sesiones
| Tema | Dónde (pág.) |
|---|---|
| Arquitectura: cliente-servidor, capas, tubos y filtros | KA 2, *Architecture Patterns, Styles* (pág. 72) |
| Diseño UML (estructural y de comportamiento) | KA 3, *Recording Software Designs* (pág. 89) |
| Diseño orientado a objetos | KA 3, sección 5 (pág. 93–97) |
| Estimación de esfuerzo y costo | KA 9, *Effort, Schedule, and Cost Estimation* (pág. 209) |
| Riesgos | KA 9, sección 2.5, *Risk Management* (pág. 210) |
| Trade-off (decisiones con alternativas) | KA 14 (pág. 282) |

---

## 4. Lo que todavía no está indexado
- Índice alfabético de términos: no lo verifiqué. Si lo buscas, usa Ctrl+F en el visor.
- Capítulos de Sommerville, Pressman y Robertson: no están en el vault. Sus capítulos se indican en las guías, pero sin página.
