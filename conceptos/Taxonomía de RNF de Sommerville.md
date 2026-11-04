---
tipo: concepto
curso: Ingeniería de Software I
fuente: "03a Requirements Engineering p. 22-45; Sesión 03"
examen: garantizado — "usted debe aprendérsela"
---
# Taxonomía de RNF de Sommerville

**Mnemotecnia del profesor: P-O-E** → **P**roducto · **O**rganizacional · **E**xterno.

## Mapa
- **Producto**
  - **Eficiencia** → desempeño (*performance*) · espacio (*space*)
  - **Usabilidad** (facilidad de uso, tolerancia a errores)
  - **Dependability** → availability · reliability · robustness · repairability · maintainability (ver [[Dependability]])
  - **Seguridad** (*security*: resistencia a intrusión deliberada o accidental)
- **Organizacional**
  - **Ambiente / entorno** (*environmental*): plataforma de operación, portabilidad
  - **Operacional**: tiempo y costo de entrega, cómo se usa, **interoperabilidad**
  - **Desarrollo**: lenguaje, método de diseño, estándares de proceso (ISO 9001, CMM, PRINCE2, herramienta CASE)
- **Externo**
  - **Regulatorio** (organismos reguladores: MSP, IESS, SRI, superintendencias)
  - **Ético** (aceptable para cliente y público; privacidad; código de ética de ESPOL o del gremio)
  - **Legislativo** → contable · *safety* · seguridad/privacidad (LOPDP)

## Métricas por propiedad (slide 40)
| Propiedad | Métrica |
|---|---|
| Velocidad | transacciones/s · tiempo de respuesta · tiempo de refresco de pantalla |
| Tamaño | MB · número de chips ROM |
| Facilidad de uso | tiempo de entrenamiento · número de pantallas de ayuda |
| Reliability | MTTF · probabilidad de no disponibilidad · tasa de ocurrencia de fallas · disponibilidad |
| Robustez | tiempo de reinicio tras falla · % de eventos que causan falla · probabilidad de corrupción de datos |
| Portabilidad | % de sentencias dependientes de plataforma · número de plataformas objetivo |

Usabilidad además: tareas típicas en *x* minutos, conformidad con un *look & feel* (Windows/Apple o la línea gráfica de la empresa), manuales/ayuda, errores a ritmo normal, tiempo de instalación. Mantenibilidad: tiempo para hacer un cambio **simple / moderado / complejo**.

## Ejemplos del slide con su clasificación (memorizar)
| RNF | Tipo |
|---|---|
| El operador debe poder usar el sistema con media hora de entrenamiento | Producto · usabilidad |
| Las respuestas a solicitudes de estimación deben tomar < 2 s | Producto · eficiencia · desempeño |
| Disponible el 99 % del tiempo entre 08h00 y medianoche | Producto · dependability · availability |
| Las mejoras deben completarse en una semana | Producto · dependability · maintainability |
| Tiempo promedio de respuesta < 5 s | Producto · eficiencia · desempeño |
| Disponible para el inicio del proyecto XYZ | Organizacional · operacional · entrega |
| Un director de proyecto experimentado lo usa tras 1 h de entrenamiento | Producto · usabilidad |
| Usar la librería de clases del servidor de desarrollo | Organizacional · desarrollo |
| Operar sobre Windows 11/10 y Linux | Organizacional · ambiente · plataforma/portabilidad |
| Accesible solo para usuarios autorizados | Producto · seguridad (también Externo · ético) |
| Las estimaciones actualizan la BD histórica del sistema CostXpert | Organizacional · operacional · interoperabilidad |
| Cumplir la ley de protección de datos | Externo · legislativo · seguridad |

## Plantillas para "mapear" en el examen (2 por tipo)
- **Desempeño:** "La consulta de <X> debe responder en menos de <n> s para el 95 % de las solicitudes con <m> usuarios concurrentes."
- **Espacio:** "Las imágenes subidas deben comprimirse a ≤ 500 KB."
- **Usabilidad:** "Un <rol> debe poder <tarea> de forma independiente tras un taller de ≤ <n> h." / "Registrar <X> debe tomar ≤ 2 min a un usuario promedio."
- **Availability:** "Disponible el 99,5 % del tiempo **mensual**, entre <hora> y <hora>, con caídas de máx. <n> min continuos." (siempre periodo + franja)
- **Reliability:** "MTTF ≥ 500 h para fallas críticas." · **Robustez:** "Reiniciar en < 5 min tras una falla."
- **Maintainability:** "Un cambio simple en ≤ 1 día; moderado ≤ 1 semana."
- **Seguridad:** "Contraseñas almacenadas con hash bcrypt; bloqueo tras 5 intentos fallidos."
- **Ambiente:** "Funcionar en Chrome ≥ 120 y Android ≥ 11."
- **Operacional:** "Entrega a más tardar el <fecha>; presupuesto máx. <USD>." · "Integrarse con los web services del SRI para facturación electrónica."
- **Desarrollo:** "Backend en .NET 8 porque es el estándar de la empresa." · "Diseño en Visual Paradigm."
- **Regulatorio:** "Cumplir las normas del MSP sobre historias clínicas."
- **Ético:** "No mostrar datos de salud a roles no médicos."
- **Legislativo:** "Cumplir la Ley Orgánica de Protección de Datos Personales (LOPDP)."

## Errores que el profesor castiga
- RNF **sin métrica** ("buen desempeño", "a toda hora").
- Availability **sin periodo** ("99 %": ¿anual? ¿mensual? ¿continuo?).
- Decir "mi cliente no tiene RNF": hay que provocarlos.

## Relacionado
- [[Requerimientos funcionales vs. no funcionales]] · [[Dependability]]
