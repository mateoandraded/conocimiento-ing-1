---
tipo: proyecto
nombre: CogniSync
documento: historias de usuario
version: 2
actualizado: 2026-10-26
fuente: Requerimientos_CogniSync-signed.pdf (Ing. Fabrizzio Ontaneda)
---
# CogniSync — Historias de usuario v2

> Versión con formato: `CogniSync - Historias de usuario v2.pdf` / `.docx` (misma carpeta). Contexto: [[CogniSync - contexto]].
> Valores con `*` = propuestos por el equipo, por confirmar con el cliente.

## Usuarios
| Usuario | Tipo | Descripción |
|---|---|---|
| Terapeuta | Usuario directo | Psicólogo o psicoterapeuta de la clínica. Registra pacientes, citas y notas clínicas, y revisa la evolución de sus pacientes. |
| Administrador de la clínica | Usuario directo | Responsable de la clínica. Registra, desactiva y reactiva las cuentas de los terapeutas. |
| Paciente | Stakeholder indirecto | No usa el sistema según el documento del cliente*, pero sus datos de salud mental son el centro del sistema. |
| Ing. Fabrizzio Ontaneda | Cliente | Autor del documento de requerimientos. Valida las historias y firma las actas de conformidad. |

## Épicas y prioridad
| Épica | ID | Historia | Prioridad |
|---|---|---|---|
| E1. Acceso y roles | HU-01 | Iniciar sesión | Must |
| E1. Acceso y roles | HU-02 | Cerrar sesión y expiración | Must |
| E1. Acceso y roles | HU-03 | Registrar terapeutas | Must |
| E1. Acceso y roles | HU-04 | Desactivar terapeutas | Should |
| E2. Expediente del paciente | HU-05 | Crear expediente | Must |
| E2. Expediente del paciente | HU-06 | Listar y buscar pacientes | Must |
| E2. Expediente del paciente | HU-07 | Editar expediente | Must |
| E2. Expediente del paciente | HU-08 | Archivar paciente | Must |
| E3. Agenda y asistencia | HU-09 | Registrar citas | Should |
| E3. Agenda y asistencia | HU-10 | Marcar asistencia | Should |
| E3. Agenda y asistencia | HU-11 | Alerta de deserción | Should |
| E4. Notas clínicas | HU-12 | Nota por texto | Must |
| E4. Notas clínicas | HU-13 | Nota por voz | Should |
| E4. Notas clínicas | HU-14 | Nota desde foto de apuntes | Could |
| E4. Notas clínicas | HU-15 | Estructurar en SOAP | Must |
| E4. Notas clínicas | HU-16 | Estructurar en DAP | Should |
| E4. Notas clínicas | HU-17 | Revisar y aprobar la nota | Must |
| E4. Notas clínicas | HU-18 | Resumen de la sesión anterior | Must |
| E4. Notas clínicas | HU-19 | Historial de notas | Must |
| E5. Análisis y evolución | HU-20 | Etiquetar síntomas | Should |
| E5. Análisis y evolución | HU-21 | Corregir etiquetas | Could |
| E5. Análisis y evolución | HU-22 | Gráfica de evolución | Should |
| E6. Cruce bibliográfico (futuro) | HU-23 | Sugerencias según manuales | Won't (esta versión) |

## E1. Acceso y roles

### HU-01 · Iniciar sesión
*Prioridad: Must · Origen: RF «Autenticación Segura»*

**Como** terapeuta, **quiero** iniciar sesión con mi correo y contraseña, **para** acceder solo yo a la información clínica de mis pacientes.

Criterios de aceptación:
- Verificar que un terapeuta con cuenta activa y credenciales correctas entra a su panel de pacientes.
- Verificar que con un correo o una contraseña incorrectos se muestra «Credenciales inválidas», sin indicar cuál de los dos campos falló.
- Verificar que una cuenta desactivada no puede iniciar sesión.
- Verificar que, tras 5* intentos fallidos seguidos, la cuenta se bloquea durante 15* minutos.

**Justificación:** Sale del requerimiento de autenticación segura y es la base de todas las demás historias. No menciona JWT porque esa es una decisión técnica y la historia debe ser independiente del diseño.

### HU-02 · Cerrar sesión y expiración
*Prioridad: Must · Origen: Omisión detectada (derivada de «Autenticación Segura»)*

**Como** terapeuta, **quiero** cerrar sesión y que mi sesión expire tras un periodo sin uso, **para** que nadie vea expedientes si dejo el equipo abierto en el consultorio.

Criterios de aceptación:
- Verificar que, al pulsar «Cerrar sesión», el usuario vuelve a la pantalla de inicio y el botón «atrás» del navegador no muestra datos de pacientes.
- Verificar que, tras 30* minutos sin actividad, la siguiente acción pide iniciar sesión de nuevo.
- Verificar que una nota en edición se conserva como borrador cuando la sesión expira.

**Justificación:** No está escrita en el documento, pero un inicio de sesión seguro con datos de salud mental no está completo sin ella. Se separó de HU-01 para que cada historia se pruebe por su cuenta.

### HU-03 · Registrar terapeutas
*Prioridad: Must · Origen: RF «Gestión de Roles»*

**Como** administrador de la clínica, **quiero** registrar a los terapeutas de mi clínica, **para** que puedan usar el sistema con el rol correcto.

Criterios de aceptación:
- Verificar que el administrador crea una cuenta con nombres, apellidos, correo y rol, y que esa cuenta puede iniciar sesión.
- Verificar que el sistema rechaza un correo que ya está registrado.
- Verificar que un usuario con rol Terapeuta no puede abrir la gestión de usuarios, ni desde el menú ni escribiendo la dirección de la página.

**Justificación:** Es el control de acceso por roles visto desde quien asigna los permisos. Sin ella, el rol de administrador no tendría ninguna función propia.

### HU-04 · Desactivar terapeutas
*Prioridad: Should · Origen: RF «Gestión de Roles»*

**Como** administrador de la clínica, **quiero** desactivar y reactivar la cuenta de un terapeuta, **para** que quien deja la clínica ya no pueda ver expedientes.

Criterios de aceptación:
- Verificar que un terapeuta desactivado no puede iniciar sesión y que su sesión abierta se cierra.
- Verificar que los expedientes y las notas del terapeuta desactivado se conservan.
- Verificar que el administrador puede reactivar la cuenta y que el terapeuta recupera el acceso a sus pacientes.

**Justificación:** Protege los datos cuando cambia el personal. Se separó de HU-03 para mantener las historias pequeñas.

## E2. Expediente del paciente

### HU-05 · Crear expediente
*Prioridad: Must · Origen: RF «Expediente Digital» (crear)*

**Como** terapeuta, **quiero** crear el expediente de un paciente nuevo con sus datos demográficos y antecedentes de consulta, **para** tener toda su información en un solo lugar desde la primera sesión.

Criterios de aceptación:
- Verificar que se guarda un paciente con los campos obligatorios: nombres, apellidos, fecha de nacimiento, sexo, teléfono y motivo de consulta*.
- Verificar que, si falta un campo obligatorio, el sistema señala cuál es y no guarda.
- Verificar que el paciente nuevo aparece en la lista del terapeuta que lo creó.

**Justificación:** Corresponde al «crear» del expediente digital. El documento solo dice «demografía básica», así que los campos exactos se validan con el cliente.

### HU-06 · Listar y buscar pacientes
*Prioridad: Must · Origen: RF «Expediente Digital» (leer)*

**Como** terapeuta, **quiero** ver la lista de mis pacientes y buscarlos por nombre, **para** encontrar el expediente correcto sin recorrer toda la lista.

Criterios de aceptación:
- Verificar que el panel muestra los pacientes activos del terapeuta, ordenados alfabéticamente por apellido.
- Verificar que, al buscar «per», aparecen solo los pacientes cuyo nombre o apellido contiene ese texto, sin distinguir mayúsculas ni tildes.
- Verificar que un terapeuta no ve los pacientes de otro terapeuta*.

**Justificación:** Corresponde al «leer» del expediente. El tercer criterio es una suposición de privacidad que el documento no define y que se confirma con el cliente.

### HU-07 · Editar expediente
*Prioridad: Must · Origen: RF «Expediente Digital» (actualizar)*

**Como** terapeuta, **quiero** actualizar los datos de un paciente, **para** que el expediente refleje su situación actual.

Criterios de aceptación:
- Verificar que un cambio guardado se ve al volver a abrir el expediente.
- Verificar que el sistema rechaza una fecha de nacimiento posterior a la fecha actual.
- Verificar que el expediente muestra la fecha de la última modificación y el usuario que la hizo.

**Justificación:** Corresponde al «actualizar» del expediente. Es pequeña e independiente una vez que existe el paciente.

### HU-08 · Archivar paciente
*Prioridad: Must · Origen: RF «Expediente Digital» (archivar)*

**Como** terapeuta, **quiero** archivar a un paciente que terminó o abandonó el proceso, **para** mantener ordenada mi lista sin perder su historial clínico.

Criterios de aceptación:
- Verificar que un paciente archivado no aparece en la lista principal.
- Verificar que las notas de un paciente archivado se conservan y se pueden consultar.
- Verificar que, con el filtro «Archivados», el paciente aparece y se puede reactivar.
- Verificar que el sistema no ofrece ninguna opción para eliminar pacientes.

**Justificación:** El cliente pidió «archivar», no «eliminar». En una historia clínica borrar datos no es adecuado, así que se respeta esa palabra.

## E3. Agenda y asistencia

### HU-09 · Registrar citas
*Prioridad: Should · Origen: Omisión detectada (módulo «Agenda» sin requerimientos)*

**Como** terapeuta, **quiero** registrar las citas de cada paciente con fecha y hora, **para** llevar el control de su asistencia.

Criterios de aceptación:
- Verificar que se crea una cita con paciente, fecha, hora de inicio y duración (50* minutos por defecto).
- Verificar que el sistema avisa si la cita se cruza con otra del mismo terapeuta.
- Verificar que la cita aparece en el expediente del paciente con el estado «Programada».

**Justificación:** El módulo se llama «Gestión de Pacientes y Agenda», pero no tiene ningún requerimiento de agenda. La alerta de deserción necesita el historial de citas, así que esta historia cubre esa omisión en su versión mínima.

### HU-10 · Marcar asistencia
*Prioridad: Should · Origen: Omisión detectada (dato que necesita la «Alerta de Deserción»)*

**Como** terapeuta, **quiero** marcar cada cita como asistida, cancelada o inasistencia, **para** que el sistema tenga el historial que necesita para detectar el riesgo de abandono.

Criterios de aceptación:
- Verificar que una cita pasada se puede marcar como «Asistida», «Cancelada» o «Inasistencia».
- Verificar que una cita futura no se puede marcar como «Asistida».
- Verificar que el expediente muestra el número de citas en cada estado.

**Justificación:** Separa el registro del dato de su análisis. Así HU-11 depende solo de este registro y no de toda la agenda.

### HU-11 · Alerta de deserción
*Prioridad: Should · Origen: RF «Alerta de Deserción»*

**Como** terapeuta, **quiero** ver una alerta en mi panel cuando un paciente tiene alto riesgo de abandonar la terapia, **para** contactarlo antes de que deje el proceso.

Criterios de aceptación:
- Verificar que aparece la alerta si el paciente tiene 2* cancelaciones o inasistencias seguidas.
- Verificar que aparece la alerta si el paciente perdió el 40 %* o más de sus citas en los últimos 60* días, con al menos 3 citas en ese periodo.
- Verificar con dos ejemplos: 5 citas con 2 perdidas (40 %) muestran la alerta; 5 citas con 1 perdida (20 %) no la muestran.
- Verificar que un paciente que no cumple ninguna de las dos reglas no muestra la alerta.

**Justificación:** «Alto riesgo» es ambiguo. Se propone una regla medible, con dos ejemplos de cálculo, para que la historia sea verificable y el cliente la acepte o la cambie.

## E4. Notas clínicas

### HU-12 · Nota por texto
*Prioridad: Must · Origen: RF «Flexibilidad de Captura» (texto manual)*

**Como** terapeuta, **quiero** escribir el resumen de la sesión en texto libre, **para** registrar lo ocurrido sin depender de otra herramienta.

Criterios de aceptación:
- Verificar que la nota se guarda asociada al paciente y a la fecha de la sesión.
- Verificar que la nota acepta hasta 5 000* caracteres.
- Verificar que el texto se guarda como borrador cada 30 segundos mientras se escribe.

**Justificación:** Es la primera de las tres vías de captura y la más simple. Las historias se separaron por vía porque cada una tiene un esfuerzo y un riesgo técnico distinto.

### HU-13 · Nota por voz
*Prioridad: Should · Origen: RF «Flexibilidad de Captura» (dictado por voz)*

**Como** terapeuta, **quiero** dictar la nota con mi voz y que se transcriba a texto, **para** registrar la sesión sin teclear.

Criterios de aceptación:
- Verificar que se puede grabar desde el navegador un audio de hasta 10* minutos y recibir el texto editable.
- Verificar que la transcripción de un audio de 5 minutos tarda 60* segundos o menos.
- Verificar que, si el audio no tiene voz reconocible, el sistema avisa y conserva lo que ya estaba escrito.
- Verificar que el audio se elimina después de transcribirlo*.

**Justificación:** Segunda vía de captura. Los tiempos dependen del servicio de transcripción, por eso se confirman con SPIKE-01.

### HU-14 · Nota desde foto de apuntes
*Prioridad: Could · Origen: RF «Flexibilidad de Captura» (carga de imágenes, OCR)*

**Como** terapeuta, **quiero** subir una foto de mis apuntes en papel y obtener el texto, **para** no transcribir a mano lo que escribí en la libreta.

Criterios de aceptación:
- Verificar que se aceptan imágenes JPG o PNG de hasta 10 MB.
- Verificar que se pueden subir hasta 5* fotos para una misma nota.
- Verificar que el texto extraído se muestra editable antes de guardarlo.
- Verificar que, si la imagen no tiene texto legible, el sistema lo avisa.

**Justificación:** Tercera vía de captura y la de mayor riesgo, porque leer letra manuscrita es poco fiable. Depende de SPIKE-02.

### HU-15 · Estructurar en SOAP
*Prioridad: Must · Origen: RF «Estructuración Automática»*

**Como** terapeuta, **quiero** que el sistema convierta mis apuntes en una nota con formato SOAP (Subjetivo, Objetivo, Análisis, Plan), **para** tener una nota clínica estandarizada sin redactarla yo.

Criterios de aceptación:
- Verificar que la nota resultante tiene las cuatro secciones Subjetivo, Objetivo, Análisis y Plan.
- Verificar que una sección sin datos en los apuntes aparece como «Sin información en los apuntes».
- Verificar con 10 apuntes de prueba que el cliente aprueba la estructuración de al menos 8 (aprobación de un experto).
- Verificar que, si el servicio de estructuración falla, el sistema lo avisa y conserva el texto original.

**Justificación:** Es el núcleo del producto. Se separó del formato DAP para que el cliente pueda priorizar uno de los dos.

### HU-16 · Estructurar en DAP
*Prioridad: Should · Origen: RF «Estructuración Automática»*

**Como** terapeuta, **quiero** que el sistema convierta mis apuntes en una nota con formato DAP (Datos, Análisis, Plan), **para** usar el formato que prefiero o que pide mi clínica.

Criterios de aceptación:
- Verificar que la nota resultante tiene las tres secciones Datos, Análisis y Plan.
- Verificar que el terapeuta elige SOAP o DAP antes de estructurar y puede fijar uno como predeterminado.
- Verificar que, si el servicio de estructuración falla, el sistema lo avisa y conserva el texto original.

**Justificación:** Mismo requerimiento que HU-15. Dividir por formato mantiene ambas historias pequeñas.

### HU-17 · Revisar y aprobar la nota
*Prioridad: Must · Origen: Propuesta del equipo*

**Como** terapeuta, **quiero** revisar y editar la nota estructurada antes de aprobarla, **para** asegurarme de que no tenga errores, porque yo respondo por su contenido.

Criterios de aceptación:
- Verificar que cada sección de la nota estructurada se puede editar.
- Verificar que una nota sin aprobar queda en estado «Borrador» y una aprobada en estado «Aprobada», con fecha y hora.
- Verificar que una nota aprobada no se edita directamente y solo admite una adenda con fecha*.
- Verificar con 3 terapeutas y 5 notas cada uno que el tiempo entre abrir la nota y aprobarla es de 3 minutos o menos en los 15 casos (RNF-04).

**Justificación:** La estructuración automática puede equivocarse y una nota clínica tiene peso legal y ético, así que el profesional debe aprobarla. Aquí se mide el límite de 3 minutos que pide el cliente.

### HU-18 · Resumen de la sesión anterior
*Prioridad: Must · Origen: RF «Memoria de Contexto»*

**Como** terapeuta, **quiero** ver un resumen de la sesión anterior al empezar una nueva nota del mismo paciente, **para** retomar el hilo sin releer todo el expediente.

Criterios de aceptación:
- Verificar que, al abrir una nota nueva, se muestra el resumen de la última nota aprobada del paciente, en 5* líneas o menos.
- Verificar que el resumen indica la fecha de esa sesión.
- Verificar que, si el paciente no tiene notas previas, se muestra «Primera sesión registrada».

**Justificación:** Sale del requerimiento de memoria de contexto. «Breve resumen» es ambiguo, por eso se propone un máximo de líneas.

### HU-19 · Historial de notas
*Prioridad: Must · Origen: Omisión detectada*

**Como** terapeuta, **quiero** ver todas las notas de un paciente ordenadas por fecha, **para** revisar su proceso completo.

Criterios de aceptación:
- Verificar que las notas se listan de la más reciente a la más antigua, con fecha, formato y estado.
- Verificar que, al elegir una nota, se muestra completa.
- Verificar que un terapeuta no puede abrir notas de pacientes de otro terapeuta*.

**Justificación:** El documento basa el análisis en las notas, pero nunca dice que se puedan consultar las anteriores. Esta historia cubre esa omisión.

## E5. Análisis y evolución

### HU-20 · Etiquetar síntomas
*Prioridad: Should · Origen: RF «Extracción de Síntomas»*

**Como** terapeuta, **quiero** que el sistema detecte y etiquete los síntomas mencionados en cada nota aprobada, **para** no tener que clasificarlos yo.

Criterios de aceptación:
- Verificar que una nota que menciona «insomnio» y «ataques de pánico» queda con esas dos etiquetas.
- Verificar que cada etiqueta pertenece al catálogo de síntomas acordado con el cliente* y tiene una intensidad de 1 a 10*.
- Verificar que una nota sin síntomas no recibe etiquetas.
- Verificar con 10 notas de prueba que el cliente aprueba las etiquetas de al menos 8.

**Justificación:** Sale del requerimiento de extracción de síntomas. Las gráficas de HU-22 necesitan una intensidad, pero el documento no dice cómo se mide; es la pregunta más importante de este módulo.

### HU-21 · Corregir etiquetas
*Prioridad: Could · Origen: Propuesta del equipo*

**Como** terapeuta, **quiero** agregar, quitar o corregir las etiquetas de síntomas de una nota, **para** que las gráficas de evolución se basen en datos correctos.

Criterios de aceptación:
- Verificar que una etiqueta quitada deja de contar en las gráficas.
- Verificar que un síntoma agregado desde el catálogo aparece en la nota y en las gráficas.
- Verificar que se puede cambiar la intensidad de una etiqueta.

**Justificación:** Mismo razonamiento que HU-17: el profesional valida lo que hace el sistema. Se separó de HU-20 para que el cliente decida si la quiere.

### HU-22 · Gráfica de evolución
*Prioridad: Should · Origen: RF «Mapas de Calor Longitudinales»*

**Como** terapeuta, **quiero** ver una gráfica de la intensidad y la frecuencia de los síntomas de un paciente a lo largo del tiempo, **para** evaluar si está mejorando.

Criterios de aceptación:
- Verificar que, con notas etiquetadas en al menos 2 fechas, se muestra una gráfica con un eje de fechas y una serie por síntoma.
- Verificar que, con menos de 2 notas etiquetadas, se muestra «No hay datos suficientes».
- Verificar que se puede filtrar por rango de fechas y que por defecto se muestran los últimos 3* meses.
- Verificar que la gráfica se lee completa en una pantalla de 360 px de ancho (RNF-03).

**Justificación:** Sale del requerimiento de mapas de calor longitudinales. Depende de HU-20, por eso va al final del flujo.

## E6. Cruce bibliográfico (futuro)

### HU-23 · Sugerencias según manuales
*Prioridad: Won't (esta versión) · Origen: RF «Cruce Bibliográfico» (marcado como futuro)*

**Como** terapeuta, **quiero** cruzar los síntomas del paciente con manuales terapéuticos, **para** recibir sugerencias de plan de intervención.

Criterios de aceptación:
- Sin criterios por ahora: se definen si el cliente la incluye en el alcance del proyecto.

**Justificación:** El cliente la marca como futura. Una historia lejana puede ser grande y se refina cuando se acerque su turno, como indica el criterio «Estimable» de INVEST.

## Spikes

### SPIKE-01 · Evaluar transcripción de voz (habilita HU-13)
Como equipo, queremos probar al menos 2 servicios de voz a texto con audios de prueba en español de Ecuador, para saber si HU-13 es viable y cuánto tarda.
- Verificar que se entrega una tabla con precisión aproximada, tiempo de respuesta y costo de cada opción.
- Duración máxima: 2* días.

### SPIKE-02 · Evaluar OCR de letra manuscrita (habilita HU-14)
Como equipo, queremos probar el reconocimiento de texto con fotos de apuntes manuscritos sin datos reales de pacientes, para saber si HU-14 es viable.
- Verificar que se entrega el porcentaje aproximado de palabras bien reconocidas con 5 fotos de prueba.
- Duración máxima: 2* días.

## RNF transversales
| ID | Requerimiento | Tipo (Sommerville) | Criterio de validación |
|---|---|---|---|
| RNF-01 | Los identificadores de usuarios, pacientes y notas son UUID no enumerables. | Producto · Seguridad | Un experto revisa la base de datos y confirma el tipo UUID. Además, cambiar el identificador en la dirección de una página no da acceso a otro registro. |
| RNF-02 | Toda conexión entre cliente y servidor usa HTTPS. | Producto · Seguridad | Prueba medible: el 100 % de las peticiones HTTP se redirigen a HTTPS y el certificado es válido. |
| RNF-03 | La interfaz es 100 % responsiva para PC, tablet y móvil. | Producto · Usabilidad | Prueba medible: cada pantalla se revisa a 360, 768 y 1366 px de ancho* sin desplazamiento horizontal. |
| RNF-04 | El registro de datos post-sesión toma 3 minutos o menos por paciente. | Producto · Usabilidad | Prueba de aceptación de usuario con 3 terapeutas y 5 notas cada uno (ver HU-17). |
| RNF-05 | El sistema está disponible el 99 %* del tiempo entre 07:00 y 21:00* de lunes a sábado*. | Producto · Confiabilidad (disponibilidad) | Prueba medible durante 30 días con un monitor de disponibilidad. El cliente solo indicó «alojado en un VPS», lo cual no es medible. |
| RNF-06 | El tratamiento de datos de pacientes cumple la Ley Orgánica de Protección de Datos Personales del Ecuador. | Externo · Legislativo y ético | Aprobación de un experto (el cliente o un asesor legal) sobre el consentimiento informado y el envío de datos a servicios externos*. |

## Trazabilidad
| Requerimiento del cliente | Historias |
|---|---|
| RF Gestión de Roles | HU-03, HU-04 |
| RF Autenticación Segura | HU-01, HU-02 |
| RF Expediente Digital | HU-05, HU-06, HU-07, HU-08 |
| RF Alerta de Deserción | HU-11 (con datos de HU-09 y HU-10) |
| RF Flexibilidad de Captura | HU-12, HU-13, HU-14 |
| RF Estructuración Automática | HU-15, HU-16 (revisión en HU-17) |
| RF Memoria de Contexto | HU-18 |
| RF Extracción de Síntomas | HU-20 (corrección en HU-21) |
| RF Mapas de Calor Longitudinales | HU-22 |
| RF Cruce Bibliográfico (futuro) | HU-23 |
| RNF Privacidad y Seguridad | RNF-01, RNF-02 |
| RNF Usabilidad | RNF-03, RNF-04 |
| RNF Disponibilidad | RNF-05 |
| Omisiones detectadas por el equipo | HU-02, HU-09, HU-10, HU-19, RNF-06 |
| Propuestas del equipo | HU-17, HU-21 |

## Preguntas para el cliente

### Alcance general
1. ¿El sistema es para una sola clínica o para varias clínicas con datos separados entre sí? (HU-03)
2. ¿Los pacientes usarán alguna parte del sistema? ¿Se necesita una aplicación móvil o basta con el diseño responsivo? (Usuarios)
3. ¿El cruce bibliográfico queda fuera del proyecto en Ingeniería de Software I y II? (HU-23)
4. ¿Cuántos terapeutas y cuántos pacientes por clínica se esperan al inicio? (General)
5. ¿Con qué frecuencia nos reunimos y quién firma las actas de conformidad de cada sprint? (General)

### Acceso y roles
6. ¿Se bloquea la cuenta tras varios intentos fallidos? ¿Cuántos intentos y por cuánto tiempo? (HU-01)
7. ¿Se necesita recuperar la contraseña por correo electrónico? (HU-01)
8. ¿Tras cuántos minutos sin uso debe expirar la sesión? (HU-02)
9. ¿Cómo recibe el terapeuta su contraseña inicial? (HU-03)
10. Al desactivar a un terapeuta, ¿sus pacientes se reasignan a otro? ¿Quién lo decide? (HU-04)
11. ¿El administrador puede ver los expedientes y las notas de todos los terapeutas? (HU-06, HU-19)

### Expediente del paciente
12. ¿Qué campos son obligatorios y cuáles opcionales en «demografía básica» y «antecedentes de consulta»? ¿Se registra la cédula? (HU-05)
13. ¿Un paciente puede ser atendido por más de un terapeuta? (HU-06)

### Agenda y asistencia
14. ¿Necesitan una agenda completa (calendario semanal) o solo el registro de citas? ¿Integración con Google Calendar o recordatorios a pacientes? (HU-09)
15. ¿Cuánto dura una sesión por defecto? (HU-09)
16. ¿Aceptan la regla de riesgo de deserción propuesta (2 faltas seguidas o 40 % de citas perdidas en 60 días)? (HU-11)
17. Cuando aparece la alerta, ¿el terapeuta solo la ve o también registra que contactó al paciente? (HU-11)

### Notas clínicas
18. ¿Cuál es la longitud máxima de una nota? (HU-12)
19. ¿Cuánto puede durar un dictado? ¿Se guarda el audio original o se elimina tras transcribirlo? (HU-13)
20. ¿Cuántas fotos por nota? ¿Se guardan las imágenes originales? (HU-14)
21. ¿Qué formato usa más la clínica, SOAP o DAP? ¿Tienen una plantilla propia de cada uno? (HU-15, HU-16)
22. ¿Cuánto tiempo máximo es aceptable para estructurar una nota? (HU-15)
23. ¿Aceptan que la nota quede como borrador hasta que el terapeuta la apruebe? ¿Una nota aprobada se puede editar o solo admite adendas? (HU-17)
24. ¿El resumen previo debe resumir solo la última sesión o varias? ¿Cuántas líneas como máximo? (HU-18)

### Análisis y evolución
25. ¿Existe una lista cerrada de síntomas? ¿Cuáles son? (HU-20)
26. ¿Cómo se mide la intensidad de un síntoma (escala de 1 a 10, leve/moderado/grave u otra)? (HU-20, HU-22)
27. Si una nota menciona ideación suicida, ¿el sistema debe mostrar una alerta especial? ¿Cuál es el protocolo de la clínica? (HU-20)
28. ¿Prefieren mapa de calor o líneas de tendencia? ¿Qué periodo se muestra por defecto? (HU-22)

### Requerimientos no funcionales
29. ¿Qué disponibilidad esperan (porcentaje, días y horario)? (RNF-05)
30. ¿Los pacientes firman un consentimiento para que sus datos se procesen con un servicio externo de inteligencia artificial? (RNF-06)
31. ¿Con qué frecuencia se deben respaldar los datos y por cuánto tiempo se conservan? (RNF-06)
