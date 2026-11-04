---
tipo: concepto
curso: Ingeniería de Software I
fuente: "03a Requirements Engineering p. 20-45; Sesión 03"
examen: garantizado
---
# Requerimientos funcionales vs. no funcionales

**En una línea:** RF = **qué hace** el sistema; RNF = **restricciones** sobre cómo lo hace, transversales a todo el sistema.

## Requerimientos funcionales (RF)
- Servicios que el sistema provee, cómo reacciona a entradas y se comporta en situaciones particulares.
- También pueden decir lo que el sistema **no** debe hacer.
- Son los más fáciles de identificar. Expresarlos **cuantitativamente** cuando se pueda (evita conflictos con el cliente).
- Ej.: "Cada empleado se identifica por su número de empleado de **8 dígitos**." · "Al dar clic en el ícono del vehículo se muestra placa, velocidad, rumbo, latitud, longitud y hora de su última ubicación."

## Requerimientos no funcionales (RNF)
- *Constraints* sobre los servicios: tiempos, proceso de desarrollo, estándares, leyes.
- **Aplican al sistema completo**, no a un módulo. Ej.: "cumplir la LOPDP" afecta a todos los roles.
- Se escriben en lenguaje natural y **con métricas** (si no hay número, la contraparte puede alegar que "buen desempeño" era 1 ms y no pagar).
- Un RNF puede **generar RF**: "solo usuarios autorizados" → ventana para gestionar la lista de autorizados, rechazo con mensaje XYZ, comparar login contra la lista.
- Clasificación: [[Taxonomía de RNF de Sommerville]].

## Prueba rápida para distinguirlos
¿Afecta a una funcionalidad concreta de un rol? → probablemente **RF**. ¿Es una cualidad o restricción que aplica a todo (rapidez, seguridad, plataforma, ley)? → **RNF**.

## Se confunde con
- "El sistema debe enviar un email" (RF) vs. "los emails deben enviarse en < 5 s" (RNF de desempeño).

## Relacionado
- [[Requerimientos de usuario vs. de sistema]] · [[Ambigüedad, omisión y conflicto]] · [[Dependability]]
