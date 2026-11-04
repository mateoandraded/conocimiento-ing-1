---
tipo: concepto
curso: Ingeniería de Software I
fuente: "03a Requirements Engineering p. 4-7; Sesión 02"
---
# Requerimientos de usuario vs. de sistema

**En una línea:** usuario = alto nivel, dominio del **problema**; sistema = detallado, dominio de la **solución**.

## Definición (Sommerville)
- **Requerimientos de usuario:** enunciados en **lenguaje natural** (+ diagramas) sobre qué servicios dará el sistema y sus restricciones. Cualquiera debe poder entenderlos; si no, están mal escritos.
- **Requerimientos de sistema:** descripción detallada de funciones, servicios y restricciones operativas; define **exactamente qué implementar** (a veces se llama *functional specification*).
- Un requerimiento de usuario se expande en **varios** de sistema.

## Ejemplo (Mentcare)
- Usuario: *"El sistema generará reportes mensuales de gestión con el costo de los medicamentos prescritos por cada clínica durante ese mes."*
- Sistema: el último día laborable del mes se genera el resumen; disponible para imprimir después de las 17:30; un reporte por clínica con nombre del medicamento, número de prescripciones, dosis y costo; si hay varias unidades de dosis, reportes separados; acceso restringido a usuarios autorizados.

## Qué es un requerimiento
Descripción de los **servicios** que el sistema debe proveer y de las **restricciones** de su operación. Ingeniería de requerimientos = el proceso de *descubrir (finding out), analizar, documentar y verificar* esos servicios y restricciones.

## Relacionado
- [[Requerimientos funcionales vs. no funcionales]] · [[Problemas en ingeniería de requerimientos]]
