---
tipo: guia
tema: elicitacion
fecha: 2026-10-19
fuentes: [01TallerRequerimientos.pdf, 02FichasTallerRequerimientos.pdf, "[[2026-10-05 Sesión 03 - RF, RNF y elicitación]]"]
---

# Taller de elicitación — banco de preguntas para la entrevista

Relacionado: [[Elicitación de requerimientos]] · [[Stakeholder]] · [[Taxonomía de RNF de Sommerville]] · [[Guia S03 - Requerimientos funcionales y no funcionales]]

## Dinámica del taller (85 min, equipos de hasta 4, en parejas de equipos)

| Etapa | Tiempo | Qué hace el equipo analista | Peso |
|---|---|---|---|
| 1. Preparación | 20 min | Solo conoce el **nombre del sistema**. Asigna roles (entrevistador, anotador, facilitador). Arma la lista de chequeo y **≥ 10 preguntas abiertas**. | 15 % |
| 2. Entrevista | 20 min | Entrevista al equipo cliente, que responde **solo con lo de su tarjeta y solo lo que se le pregunta**. El anotador registra. Al final: **3 problemas/necesidades prioritarias**. Luego se invierten los roles. | 20 % |
| 3. Especificación | 25 min | 8 requerimientos de usuario en lenguaje natural + 5 RNF con **tipo Sommerville (P-O-E)**, **MoSCoW** y **cómo se validaría**. | 20 % + 20 % |
| 4. Validación | 20 min | El cliente marca cada requerimiento como correcto / ambiguo / incorrecto y dice qué falta de su tarjeta. El analista corrige. | 25 % |

Entregable: un PDF (integrantes y roles en la 1.ª página, preguntas, notas, lista inicial, hoja de validación firmada, lista corregida), subido por el equipo analista. Penalidades: −50 si no se sube; −2 por cada error ortográfico (máx. −20).

**La clave del taller:** cada tarjeta tiene un bloque *"Solo si preguntan"*. Esos datos ocultos son casi todos **RNF** (conectividad, dispositivos, volumen, picos de uso, auditoría, pagos, nivel de los usuarios). Si no haces la pregunta, el cliente no te los da, y en la validación te marca "faltan".

## ¿Para qué caso sirven las preguntas?

Para **cualquiera**. En la preparación no sabes qué tarjeta te toca (A veterinaria, B librería, C acopio de cacao, D taller mecánico, E biblioteca escolar, F lavandería). Por eso las preguntas son genéricas y en la entrevista reemplazas "el sistema" por el nombre real ("los turnos", "los préstamos", "los pesajes"...).

## Lista de chequeo + preguntas abiertas

### 1. Perfil del stakeholder
1. ¿Cuál es su cargo y de qué se encarga en el día a día?
2. ¿Quiénes más trabajan con usted y qué hace cada uno en este proceso?

### 2. Problema
3. ¿Cómo hacen hoy este proceso, paso a paso, desde que llega el cliente hasta que termina?
4. ¿Qué es lo que más se complica o sale mal? Cuénteme la última vez que pasó.
5. ¿Qué pasa cuando hay un reclamo o una discusión? ¿Cómo demuestran qué ocurrió?

### 3. Entorno
6. ¿Qué equipos y herramientas usan hoy (computadora, celular, cuadernos, WhatsApp) y cómo es la conexión a internet y la luz en el lugar?
7. ¿Cómo describiría a las personas que usarían el sistema: edad, costumbre con la tecnología, si alguno tiene dificultades para leer o escribir?
8. ¿En qué momentos del día, la semana o el año hay más trabajo? ¿Qué cantidades manejan (clientes, registros, productos)?

### 4. Solución
9. Si el sistema ya funcionara perfecto, ¿cómo sería un día normal de trabajo?
10. ¿Quién necesita enterarse de qué cosa y por qué medio prefieren que les llegue el aviso?
11. ¿Cómo se cobra o se paga hoy y qué excepciones hay (descuentos, crédito, facturas)?

### 5. Requerimientos no funcionales (preguntar por tipo Sommerville)
12. **Producto – usabilidad/eficiencia:** ¿Cuánto tiempo puede tomar registrar o consultar algo sin que se forme fila o el cliente se canse de esperar?
13. **Producto – disponibilidad/confiabilidad:** ¿Qué pasaría si el sistema se cae o se va el internet en plena atención? ¿Cuánto tiempo pueden trabajar sin él?
14. **Producto – seguridad:** ¿Quién debería poder ver o cambiar cada información y quién no?
15. **Organizacional – operacional/entorno:** ¿Con qué presupuesto, equipos y plazo cuentan? ¿Qué reglas internas o información de otras áreas tendría que respetar el sistema?
16. **Externo – legal/regulatorio:** ¿Hay leyes, entidades o documentos (facturas, reportes a una autoridad, datos personales de clientes) que tengan que cumplir?

### 6. Resumen (cierre obligatorio según el profesor)
17. Déjeme recapitular con mis palabras: los tres problemas más importantes son ___, ___ y ___. ¿Es correcto? ¿Cuál es el más urgente?
18. ¿Hay algo más que no le haya preguntado y que deba saber?

> Son 18; con 10–12 cumples. Si recortas, no quites 6, 8, 13 y 16: son las que destapan la mayoría de los datos ocultos.

## Por qué funcionan (contrástalo con las tarjetas *después* del taller)

| Dato oculto de la tarjeta | Pregunta que lo saca | RNF que puedes escribir |
|---|---|---|
| A: la recepcionista solo tiene celular | 6 | Producto (portabilidad/usabilidad) |
| A: emergencias pasan primero | 3, 4 | Más bien regla funcional; ojo al clasificar |
| B: todo el movimiento en 2 semanas; entran desde el celular | 8, 6 | Producto (eficiencia/rendimiento en picos) |
| C: sin internet y cortes de luz; socios que no leen bien | 6, 7, 13 | Producto (disponibilidad, usabilidad) |
| C: demostrar qué se anotó y cuándo | 5 | Producto (seguridad: trazabilidad/auditoría) |
| D: no usar otro número de WhatsApp | 10, 15 | Organizacional |
| E: un solo computador viejo; fila en el recreo | 6, 8, 12 | Organizacional (entorno) / Producto (eficiencia) |
| F: las empresas piden factura | 11, 16 | Externo (legal/tributario) |

## Errores que cuestan nota
- **Preguntas cerradas** ("¿Quiere una app?") → la rúbrica pide abiertas. Empieza con *qué, cómo, cuándo, quién, cuénteme*.
- **Proponer la solución antes de entender el problema** (lo recalcó el profesor en la sesión 03).
- **Olvidar el resumen con los 3 problemas prioritarios**: vale dentro del 20 % de la entrevista.
- **RNF sin métrica**: después necesitas decir cómo se validaría ("registrar un turno en ≤ 1 min", "funciona sin internet y sincroniza al reconectar").
- **Errores ortográficos**: −2 cada uno. Revisa el PDF antes de subirlo.

> Política de IA del curso: si entregas estas preguntas tal cual, hay que declararlo en un apéndice (herramienta, prompts, edición). Lo ideal es que el equipo las adapte y las redacte a su manera.
