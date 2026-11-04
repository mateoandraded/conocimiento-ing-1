---
tipo: clase
fecha: 2026-10-05
sesion: 3
temas: [requerimientos-funcionales, requerimientos-no-funcionales, taxonomia-sommerville, dependability, swebok, elicitacion]
transcripcion: "[[2026-10-05 Sesion 03]]"
slides: ["03a Requirements Engineering (p. 20-46)"]
---
# Sesión 03 — RF, RNF y elicitación (2026-10-05)

## Temas vistos
1. [[Requerimientos funcionales vs. no funcionales]]
2. Ejercicio de la biblioteca → [[Ambigüedad, omisión y conflicto]]
3. [[Taxonomía de RNF de Sommerville]] (Producto / Organizacional / Externo) con métricas
4. [[Dependability]]: availability, reliability, safety, security, resilience; robustez; antifragilidad
5. SWEBOK v4 como mapa del área (control de lectura)
6. [[Elicitación de requerimientos]]: proceso (elicitar → analizar → validar → gestionar), etnografía y entrevistas

## Definiciones (como las dio el profesor)
- **RF:** lo que el sistema debe hacer o proveer, cómo reacciona ante entradas; también lo que **no** debe hacer ("el sistema no debe permitir que un profesor altere la nota 24 h después…").
- **RNF:** *constraints*, restricciones sobre cómo se proveen los servicios (tiempo, proceso de desarrollo, estándares, leyes). **Aplican a todo el sistema de forma transversal**, no a un módulo (ej.: cumplir la Ley Orgánica de Protección de Datos afecta a todos los módulos).
- **Ambigüedad:** algo que distintos lectores pueden interpretar de distintas maneras. **Omisión:** algo que no está (se menciona un cálculo pero no cómo se hace). **Conflicto:** contradicción entre dos partes del texto.
- **Availability:** el sistema "está ahí" cuando lo consulto. **Reliability:** lo que entrega es exacto, "ni de más ni de menos". **Safety:** opera sin fallas que comprometan vidas (semáforos, UCI, torre de control). **Security:** se protege de ataques. **Resilience:** se adapta ante la dificultad y continúa (la planta que dobla el tallo para buscar la luz). **Antifragilidad:** además aprende y sale más fuerte. **Robustez:** si se cae, se levanta (redundancia: componentes duplicados de distinto proveedor y tecnología, como en aviones y satélites).
- **Etnografía pasiva** (observar sin interrumpir) vs. **activa** (hacer el trabajo del rol, aprender haciendo).

## Ejemplos dichos en clase (no están en slides)
- RF del sistema académico: el profesor ingresa notas hasta una semana después del examen; notificación por email al estudiante; no se puede alterar la nota 24 h después.
- RNF de usabilidad: "un profesor agregado debe poder usar el sistema académico con un taller de no más de 5 horas".
- RNF de desempeño: transacción interbancaria ≤ 3 s; consulta de stock de un medicamento < 1 s.
- RNF organizacional: entrega para agosto 2027; presupuesto máx. 200 000 USD; integrarse con los web services del SRI; usar .NET porque "todos mis sistemas están en .NET".
- RNF externo: regulaciones del MSP y del IESS para un hospital; LOPDP; código de ética de ESPOL.
- **"99 % del tiempo" sin periodo está incompleto**: si es anual, son 3,65 días de caída que podrían caer justo en día de pago (o en la final del Mundial).
- Un RNF de seguridad genera RF: "solo usuarios autorizados" → mantener e imprimir lista de usuarios autorizados.
- Anécdota: un director de tecnología del SRI, ex-IBM, "podía quebrar a cualquier proveedor" leyendo sus requerimientos.
- **Protocolo de comunicación con el cliente**: actas obligatorias y "si no responde en 48 h, el documento se da por pre-aprobado" (con recordatorio gentil a los 2 días).
- La mayoría de empresas ecuatorianas **no tienen documentados sus procesos**: hay que levantar lo que no existe.
- Un error de requerimientos es el más caro de corregir (más que errores de pruebas, código o diseño UML).

## ⚠️ Énfasis / "esto entra al examen"
- Ejercicio típico: texto de requerimientos → encontrar *N* **ambigüedades, conflictos u omisiones** (decir tipo, línea, texto y por qué).
- Luego: escribir *N* **requerimientos de usuario** claros (con suposiciones razonables).
- Luego: proponer *N* **RNF**, indicar **tipo según Sommerville** y **métrica**. "Son preguntas garantizadas."
- **Aprenderse la taxonomía de Sommerville** (mnemotecnia del profe: **P-O-E** = Producto, Organizacional, Externo).
- Tener **2-3 RNF modelo por tipo** memorizados y mapearlos al contexto del examen.
- **En requerimientos no se usan sinónimos**: si dijiste "email", siempre "email"; si dijiste "aprobación", nunca "autorización".
- SWEBOK: poder definir en 2-3 líneas áreas como *software quality*, *software configuration management*, *software engineering economics*.

## Tareas y anuncios
- **Tarea con deadline 2026-10-06** (se iba a explicar al final; la transcripción se corta). → revisar Canvas.
- Control de lectura del **SWEBOK v4** (indicará capítulos) + videos del webinar de lanzamiento.
- Lectura sobre **atributos de calidad de un requerimiento** (Wiegers / Leffingwell).
- En el proyecto: 1 escribe el requerimiento, 1 lo revisa y 3 hacen de abogado del diablo; revisión holística del documento completo (que la p. 4 no contradiga la p. 36). El ERS debe estar **versionado**.
- Para el proyecto hay que **provocar** RNF con el cliente: "no pueden decir que su usuario no tiene RNF".

## Preguntas abiertas
- ¿Cuál era la tarea que vencía el 2026-10-06?
- Ver contradicción reliability/resilience en [[COURSE_CONTEXT#Preguntas abiertas / contradicciones entre fuentes]].

## Próxima sesión
Resto de técnicas de elicitación (cuestionarios, talleres, prototipos) e **historias de usuario**.
