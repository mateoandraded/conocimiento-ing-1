---
tipo: proyecto
nombre: CogniSync
actualizado: 2026-10-12
---
# CogniSync — contexto del proyecto

> Proyecto de Ingeniería de Software I / II. Aquí vive el contexto estable. Las tareas se gestionan en Azure DevOps.

## Datos generales
- **Cliente / autor del documento de requerimientos:** Ing. Fabrizzio Ontaneda (documento firmado electrónicamente).
- **Qué es:** SaaS para gestionar clínicas de salud mental. Busca reducir la carga administrativa de los terapeutas con notas clínicas automáticas (SOAP/DAP) mediante IA y análisis de la evolución del paciente.
- **Documento fuente:** `Requerimientos_CogniSync-signed.pdf` (2 páginas, en Descargas).
- **Azure DevOps:** organización `https://dev.azure.com/matanand`, proyecto `CogniSync`, equipo `CogniSync Team`.
  - CLI: Azure CLI 2.91.0 con la extensión `azure-devops` 1.0.8, ya instalada y probada.
  - Defaults configurados: organización y proyecto.
  - Autenticación: variable de entorno de usuario `AZURE_DEVOPS_EXT_PAT`. **El token nunca se guarda en el vault.**
  - Proceso: **Scrum** (cambiado desde Basic el 2026-10-12). Columnas del tablero de backlog: New, Approved, Committed, Done.
  - Iteración creada: `Sprint 1`.
  - Work items creados el 2026-10-12: 6 épicas (#1, #4, #7, #13, #17, #23) y 20 features, con etiquetas RF, RT y RNF según el documento del cliente.
  - Los 5 integrantes son Project Administrators del proyecto.

## Equipo (invitado a la organización el 2026-10-12, licencia Basic, invitaciones aceptadas)
- matanand@espol.edu.ec (Mateo, propietario)
- analsalt@espol.edu.ec
- dxparral@espol.edu.ec
- juaffern@espol.edu.ec
- vicmmora@espol.edu.ec

## Resumen de requerimientos del cliente

### Funcionales (RF)
| Módulo | Requerimiento |
|---|---|
| Autenticación y autorización | Acceso por roles (RBAC), mínimo Administrador/Clínica y Terapeuta/Usuario. Inicio de sesión seguro con tokens JWT |
| Pacientes y agenda | Expediente digital (crear, leer, actualizar, archivar) con demografía y antecedentes. Alerta visual de riesgo de deserción según asistencia y cancelaciones |
| Notas clínicas (núcleo) | Captura por texto manual, dictado por voz (audio a texto) y carga de imágenes (OCR). Estructuración automática con IA en formatos SOAP o DAP. Resumen de la sesión anterior al iniciar una nueva nota |
| Análisis y evolución (IA) | Extracción y etiquetado automático de síntomas. Mapas de calor o líneas de tendencia de intensidad y frecuencia. Cruce bibliográfico con manuales terapéuticos (**futuro**) |

### No funcionales (RNF)
- **Privacidad y seguridad:** identificadores no enumerables (UUID) y conexiones cifradas (HTTPS).
- **Usabilidad:** volcado de datos post-sesión en **no más de 3 minutos por paciente**; diseño 100 % responsivo (PC, tablet, móvil).
- **Disponibilidad:** alojado en un VPS.

### Requerimientos técnicos
- Monorepo híbrido: `apps/web` (cliente) y `apps/api` (servicios).
- Frontend: React + TypeScript + Tailwind CSS, con un wrapper `httpClient.ts` para tipado de extremo a extremo.
- Backend: FastAPI (Python), llamadas asíncronas a la API de OpenAI, autenticación JWT, persistencia con SQLAlchemy.
- Base de datos: PostgreSQL nativo en el servidor, puerto 5433. Tablas principales: `roles`, `users`, `patients`, `clinical_notes`.
- Despliegue: VPS Ubuntu, Nginx como servidor web y proxy inverso con SSL (`/api/*` a FastAPI, el resto a los estáticos de React), FastAPI como servicio `systemd` con Gunicorn y workers Uvicorn.

## Observaciones del tutor (mi lectura, no están en el documento del cliente)
Estas son cosas que conviene resolver al escribir el ERS, porque el profesor las evalúa:
1. **Componente móvil:** la política del curso pide web **y** móvil, o solo móvil. El documento solo exige diseño responsivo. Hay que confirmar con el profesor si eso cumple.
2. **Disponibilidad sin métrica:** "alojado en un VPS" no es un RNF medible. El profesor pide métricas (porcentaje, franja horaria, periodo).
3. **Términos sin definir** (posibles ambigüedades u omisiones): "alto riesgo de abandono" (¿qué umbral?), "breve resumen" de la sesión anterior (¿qué longitud?), "múltiples vías" de captura (¿cuántas y con qué calidad mínima?).
4. **Datos de salud mental:** aplica la Ley Orgánica de Protección de Datos Personales. Además se envían notas a la API de OpenAI. Esto es un RNF **externo (legislativo)** y puede ser también ético. El documento no lo menciona.
5. **Tiempo de respuesta de la IA:** el RNF de 3 minutos incluye el procesamiento de IA, pero no hay un límite para la latencia de la transcripción ni del OCR.

## Pendientes
- Confirmar que el proyecto fue aprobado (la fecha límite era 2026-10-07) y registrarlo en `PROJECTS.md`.
- Que los cuatro compañeros acepten la invitación y se agreguen al equipo `CogniSync Team`.
- Escribir los PBI (historias de usuario) de cada feature y planificar el Sprint 1. → **v2 (2026-10-26):** [[CogniSync - Historias de usuario v2]] (+ `.pdf`/`.docx` con formato ESPOL): 23 HU con criterios de aceptación, MoSCoW (12 Must · 8 Should · 2 Could · 1 Won't), 2 spikes, 6 RNF con criterio de validación, trazabilidad y 31 preguntas para el cliente. Pendiente: revisión del equipo, validación con el cliente, estimación y autores por historia.
- **Azure (cargado el 2026-10-26, a pedido de Mateo):** 6 épicas (#27–#32, «E1 · Acceso y roles»…) → 23 PBI (#33–#55, «HU-01 · …») + 2 spikes (#56–#57, bajo E4). Sin nivel Feature. Cada PBI: historia + origen + justificación en *Description*, criterios en *Acceptance Criteria*, *Priority* 1–4 = Must/Should/Could/Won't, etiquetas (MoSCoW; RF cliente / Omisión / Propuesta equipo / Spike), orden del backlog = orden del story map. Todo en estado New, sin sprint, sin estimación ni responsable. (Las épicas y features anteriores las borró Mateo el 2026-10-12 a propósito; siguen en la papelera.)

## Lo que pide la spec del ERS (Proyecto Parcial, 2026-11-04) — fuente: `material/proyecto-plantillas/01bMidtermProjectSpec1.2_es.pdf` (versión 2024, igual al que pasaron al equipo)
- PDF basado en Robertson, Pressman, Sommerville, IEEE 830, ISO/IEC/IEEE 29148, Cohn y la plantilla **Volere**.
- Primera página con integrantes; luego **índice de contenido, índice de tablas e índice de figuras**.
- RNF clasificados según **Sommerville** y con **criterio de validación**.
- **Repositorio público** con evidencias de técnicas de levantamiento y metodologías + el prototipo.
- **Apéndices:** acta de conformidad firmada por el cliente; capturas del prototipo y su flujo de ventanas.
- Secciones finales obligatorias: **"Contribuciones Individuales"** y **"Declaración de Autoría"**.
- Plantilla: **LaTeX de ETS ("Writing guidelines and templates") con logo de ESPOL**. Bonificación +3 por LaTeX **e** inglés.
- Penalidades: sin carta de aceptación del cliente −100; cada error ortográfico o gramatical −2 (máx. −20); no subir co-evaluación −50 individual.
- Ojo: la spec 2024 dice "hasta 4 estudiantes"; las políticas 2026 dicen hasta 5. Confirmar con el profesor si aplica.
- Decidir quién hace de Product Owner y de Scrum Master dentro del equipo.
