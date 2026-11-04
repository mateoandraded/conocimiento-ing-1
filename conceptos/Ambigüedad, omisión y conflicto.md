---
tipo: concepto
curso: Ingeniería de Software I
fuente: "03a Requirements Engineering p. 21 y 44; Sesión 03"
examen: "ejercicio típico de examen"
---
# Ambigüedad, omisión y conflicto

**En una línea:** los tres defectos que hay que cazar en un texto de requerimientos.

## Definiciones
- **Ambigüedad:** puede ser interpretado de **distintas maneras** por distintos lectores.
- **Omisión:** algo que **no está** (se menciona un cálculo, valor o regla pero no se define).
- **Conflicto:** **contradicción** entre dos partes del texto (aquí dice blanco, más adelante negro).

Consecuencias: ambigüedad → retrabajo o **juicio**; conflicto → cada parte "se acoge a su línea"; omisión → los diseñadores **suponen** y diseñan cualquier cosa.

## Formato de respuesta en el examen
> **Tipo** · **línea N** · texto citado · por qué es un problema · (opcional) cómo corregirlo.

## Ejercicio resuelto de la clase (biblioteca)
> *Un estudiante podrá extender el periodo de préstamo de libros en préstamo en cualquier momento. El sistema puede aprobar o rechazar una extensión y debe notificar al prestamista de su decisión. El sistema debe estar disponible a toda hora.*

| # | Tipo | Texto | Problema |
|---|---|---|---|
| 1 | Ambigüedad | "a toda hora" | ¿hora laborable o calendario (24/7)? Sin métrica de disponibilidad |
| 2 | Omisión | "puede aprobar o rechazar" | ¿con qué criterios? |
| 3 | Omisión / ambigüedad | "en cualquier momento" | ¿antes o después del vencimiento?, ¿en horario laborable?, ¿cuántas veces? |
| 4 | Omisión | "extender el periodo" | ¿por cuánto tiempo? |
| 5 | Omisión | "debe notificar" | ¿por qué medio? (email, SMS, app) |
| 6 | Omisión | "el sistema puede aprobar" | ¿qué **rol** aprueba?, ¿es automático? |
| 7 | Conflicto | "podrá extender" vs. "puede aprobar o rechazar" | "podrá extender" suena a capacidad libre; si puede ser rechazada, es una **solicitud** |
| 8 | Ambigüedad | "prestamista" | ¿el estudiante (prestatario) o la biblioteca? Mal uso del término y posible sinónimo de "estudiante" |
| 9 | Omisión | (no aparece) | estados del libro, límite de extensiones, qué pasa con reservas de otros usuarios |

## Reglas de redacción que dio el profesor
- **No usar sinónimos**: un término = una sola palabra en todo el documento ("email" siempre "email"; "aprobación" nunca "autorización").
- Cuantificar siempre que se pueda; definir roles explícitamente.
- Revisar el documento **de forma holística** (que la p. 4 no contradiga la p. 36); versionarlo.

## Relacionado
- [[Requerimientos funcionales vs. no funcionales]] · [[Problemas en ingeniería de requerimientos]]
