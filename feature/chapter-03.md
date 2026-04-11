# Capítulo III: Requirements Specification

## 3.1. To-Be Scenario Mapping

A continuación se presenta la realizacion del To-Be Scenario Mapping por cada user persona.

**Segmento #1: Solicitante de Servicios**

<img width="987" height="387" alt="image" src="https://github.com/user-attachments/assets/28606eac-975e-4424-b686-3a0b86625e71" />

**Segmento #2: Proveedores de Servicios**

<img width="980" height="370" alt="image" src="https://github.com/user-attachments/assets/76e71f62-eef6-4953-8e64-bc38dd8ffb6c" />

## 3.2. User Stories


| Epic / Story ID | Título | Descripción | Criterios de Aceptación | Relacionado con (Epic ID) |
| :---- | :---- | :---- | :---- | :---- |
| EP01 | Registro de usuarios | Implementar el registro de los usuarios para tanto los asesores como los clientes |  |  |
| US01 | Registrar un profesional | Como profesional. Quiero poder registrarme fácilmente en la plataforma como consultor. Para ofrecer mis servicios, gestionar mis horarios y comenzar a brindar asesoría a personas o empresas interesadas. | Escenario 01: Registro exitoso. Dado que soy un profesional interesado en ofrecer mis servicios, Cuando completo correctamente el formulario de registro con mis datos y lo envío, Entonces el sistema guarda la información, envía una notificación de recepción y muestra un mensaje indicando que el perfil será revisado. Escenario 02: Fallo en el registro. Dado que soy un profesional que intenta registrarse, Cuando dejo campos obligatorios vacíos o ingreso datos inválidos, Entonces el sistema muestra mensajes de error y no permite enviar el formulario hasta corregir los datos. | EP01 |
| US02 | Registrar un cliente | Como usuario que busca asesoría profesional. Quiero poder registrarme fácilmente en la plataforma como cliente. Para acceder al listado de consultores disponibles, agendar sesiones y recibir asesoría especializada. | Escenario 01: Registro exitoso. Dado que soy un nuevo cliente que desea registrarse, Cuando completo correctamente el formulario de registro con mis datos, Entonces el sistema crea mi cuenta, me muestra un mensaje de bienvenida y me redirige al panel de usuario o inicio. Escenario 02: Registro con errores o campos incompletos. Dado que intento registrarme con un correo ya registrado, Cuando ingreso el correo electrónico y lo envío, Entonces el sistema me notifica que ya existe una cuenta con ese correo y me sugiere iniciar sesión o recuperar la contraseña. | EP01 |
| EP02 | Búsqueda de servicios | Poder buscar asesorías y recibir ayuda para realizarla |  |  |
| US03 | Buscar profesionales disponibles | Como usuario. Quiero poder buscar y filtrar profesionales disponibles según mi necesidad. Para encontrar al experto más adecuado y reservar una sesión fácilmente. | Escenario 01: Filtros por disponibilidad. Dado que estoy buscando un profesional. Cuando aplico un filtro por fecha y hora. Entonces el sistema me muestra solo aquellos consultores que tienen horarios disponibles en ese rango. Escenario 02: Visualización de perfil profesional. Dado que encontré un profesional que me interesa. Cuando hago clic en su perfil. Entonces puedo ver su información completa, experiencia, calificaciones, disponibilidad y tarifas. | EP02 |
| US04 | Recibir notificaciones de disponibilidad de profesionales | Como usuario. Quiero recibir notificaciones cuando un profesional que sigo esté disponible para sesiones. Para poder agendar una sesión cuando el profesional esté libre. | Escenario 01: Notificación de disponibilidad. Dado que estoy siguiendo a un profesional, Cuando el profesional actualiza su disponibilidad, Entonces recibo una notificación en mi correo o aplicación con los nuevos horarios disponibles. Escenario 02: Notificación para programar sesión. Dado que recibo una notificación de disponibilidad, Cuando hago clic en la notificación, Entonces soy redirigido a la plataforma para poder agendar mi sesión con el profesional. | EP02 |
| US05 | Filtrar experto por tarifa | Como usuario quiero filtrar expertos por tarifa para ajustar mi búsqueda a mi presupuesto. | Escenario 01: Filtro aplicado de manera exitosa. Dado que elijo el rango de tarifa deseado. Cuando doy clic en Aplicar filtro. Entonces la plataforma me muestra la lista de expertos cuya tarifa se encuentra en el rango elegido. Escenario 02: El rango seleccionado no es válido. Dado que ingreso valores inválidos de rango de tarifa. Cuando quiero aplicar el filtro. Entonces la plataforma muestra un mensaje de error sobre los valores de rango ingresados. | EP02 |
| EP03 | Gestión de Perfiles | Configurar e interactuar con los perfiles |  |  |
| US06 | Ver detalles del profesional | Como usuario. Quiero poder ver el perfil completo de un profesional. Para conocer su experiencia, especialidades, disponibilidad, tarifas y calificaciones antes de tomar una decisión. | Escenario 01: Visualización de experiencia y especialidades. Dado que estoy viendo el perfil de un consultor, Cuando navego por la sección de descripción profesional, Entonces puedo leer su formación, experiencia laboral y áreas de especialización. Escenario 02: Visualización de disponibilidad y tarifas. Dado que estoy en el perfil de un profesional, Cuando reviso su disponibilidad, Entonces puedo ver los horarios libres para agendar una sesión y el costo por cada servicio. | EP03 |
| US07 | Calificar a un profesional | Como usuario. Quiero poder calificar y dejar un comentario sobre el profesional. Para compartir mi experiencia con otros usuarios y contribuir a la reputación del consultor. | Escenario 01: Acceso a la opción de calificación tras una sesión completada. Dado que he completado una sesión con un profesional, Cuando accedo al perfil del profesional, Entonces el sistema me muestra la opción de calificar al consultor correspondiente. Escenario 02: Envío de calificación y comentario. Dado que tengo disponible la opción de calificación, Cuando selecciono una puntuación y escribo un comentario, Entonces el sistema guarda la calificación y la muestra públicamente en el perfil del profesional. | EP03 |
| US08 | Actualizar perfil de usuario | Como usuario. Quiero poder actualizar mi perfil en la plataforma. Para mantener mi información personal, preferencias y detalles de contacto actualizados. | Escenario 01: Actualización exitosa del perfil. Dado que soy un usuario que desea actualizar mi perfil, Cuando cambio mis datos personales, como el correo o número de teléfono y hago clic en "guardar", Entonces el sistema actualiza mi perfil y me muestra un mensaje de confirmación. Escenario 02: Error en la actualización del perfil. Dado que soy un usuario que intenta actualizar mi perfil, Cuando ingreso datos inválidos, como un correo incorrecto, Entonces el sistema muestra un mensaje de error y me indica qué campo debe corregirse. | EP03 |
| US09 | Guardar profesionales como favoritos | Como usuario, quiero poder guardar profesionales como favoritos, para acceder fácilmente a sus perfiles en futuras búsquedas sin tener que encontrarlos nuevamente. | Escenario 1: Agregar profesional a favoritos. Dado que estoy viendo el perfil de un consultor, Cuando hago clic en el ícono de “favorito”, Entonces el profesional se añade a mi lista de favoritos y recibo una confirmación. Escenario 2: Visualización de lista de favoritos. Dado que he marcado varios profesionales como favoritos, Cuando accedo a la sección “Favoritos” desde mi perfil, Entonces puedo ver una lista con sus nombres, especialidades y accesos directos a sus perfiles. Escenario 3: Eliminar profesional de favoritos. Dado que ya no quiero mantener a un profesional en mi lista, Cuando hago clic en el ícono de “eliminar de favoritos”, Entonces este desaparece de mi lista y el sistema me muestra un mensaje de confirmación. | EP03 |
| US10 | Crear y gestionar servicios de profesional | Como profesional quiero crear y gestionar mis servicios para ofrecer distintos tipos de asesoría. | Escenario 01: Agregar servicio nuevo. Dado que quiero agregar un servicio nuevo para ofrecer asesoría. Cuando hago clic en Agregar servicio y selecciono la categoría. Entonces, la plataforma muestra un mensaje de servicio agregado de manera satisfactoria. Escenario 02: Eliminar servicio. Dado que quiero eliminar un servicio que ya no deseo ofrecer. Cuando selecciono el servicio y hago clic en Eliminar servicio. Entonces, la plataforma muestra un mensaje de servicio eliminado de manera satisfactoria. | EP03 |
| US11 | Responder mensajes de clientes | Como profesional, quiero ver y responder los mensajes de los clientes para mantener buena comunicación. | Escenario: Mensaje enviado de manera exitosa. Dado que quiero comunicarme con un cliente. Cuando selecciono al cliente y selecciono en Enviar mensaje. Entonces, la plataforma muestra una confirmación de que el mensaje ha sido enviado. | EP03 |
| EP04 | Gestión de Sesiones y Seguimiento | Optimizar la experiencia de los usuarios y consultores antes, durante y después de las sesiones. |  |  |
| US12 | Realizar reserva de sesión | Como usuario. Quiero poder reservar una sesión con un profesional. Para asegurarme de contar con su tiempo disponible para recibir asesoría. | Escenario 01: Reserva exitosa. Dado que soy un usuario que desea agendar una sesión. Cuando selecciono un profesional, fecha y hora disponible. Entonces el sistema confirma la reserva y me envía una notificación. Escenario 02: Fallo en la reserva. Dado que intento reservar un horario que ya no está disponible. Cuando elijo esa fecha y hora. Entonces el sistema muestra un mensaje de error y me sugiere otros horarios disponibles. | EP04 |
| US013 | Agendar seguimiento post-sesión | Como usuario, quiero poder agendar una sesión de seguimiento con el mismo consultor, para continuar con el proceso de asesoría. | Escenario 1: Agendamiento desde historial Dado que he finalizado una sesión con un consultor, Cuando accedo al historial y selecciono “Agendar seguimiento”, Entonces puedo elegir fecha y hora y confirmar la nueva sesión. Escenario 2: Confirmación automática Dado que seleccioné un horario disponible, Cuando envío la solicitud de seguimiento, Entonces el sistema envía una notificación al consultor y confirma la cita. | EP04 |
| US014 | Tomar notas durante la sesión | Como consultor, quiero tener una sección para tomar notas durante la sesión, para guardar observaciones relevantes del cliente. | Escenario 1: Acceso al bloc de notas Dado que estoy en una sesión activa, Cuando accedo al bloc de notas desde mi panel, Entonces puedo escribir y guardar comentarios privados. Escenario 2: Guardado automático Dado que estoy escribiendo notas durante la sesión, Cuando cierro el panel de notas, Entonces el sistema guarda automáticamente el contenido. | EP04 |
| US015 | Enviar recomendaciones tras sesión | Como consultor, quiero poder enviar al usuario una lista de recomendaciones o materiales luego de la sesión, para complementar la asesoría. | Escenario 1: Envío de materiales Dado que terminé una sesión con un cliente, Cuando selecciono la opción “Enviar recomendaciones”, Entonces puedo adjuntar archivos o escribir sugerencias y enviarlas. Escenario 2: Visualización por el usuario Dado que el consultor me envió recomendaciones, Cuando abro la sesión desde el historial, Entonces puedo ver los materiales recibidos. | EP04 |
| US016 | Ver historial de sesiones | Como usuario. Quiero poder ver un historial de mis sesiones pasadas. Para poder revisar la información de las sesiones anteriores y hacer un seguimiento de mi progreso. | Escenario 01: Visualización del historial de sesiones. Dado que soy un usuario que ha tenido sesiones anteriores, Cuando accedo a la sección de historial de sesiones, Entonces puedo ver la lista de todas las sesiones pasadas, con fecha, profesional y detalles. Escenario 02: Visualización de detalles de una sesión. Dado que estoy viendo el historial de mis sesiones, Cuando hago clic en una sesión específica, Entonces puedo ver los detalles completos, incluyendo notas o recomendaciones proporcionadas por el profesional. | EP04 |
| US017 | Calificar seguimiento de sesión | Como usuario, quiero poder calificar las sesiones de seguimiento por separado, para evaluar la mejora continua del servicio recibido. | Escenario 1: Opción disponible tras sesión de seguimiento Dado que acabo de completar una sesión de seguimiento, Cuando reviso el historial de esa sesión, Entonces veo la opción de dejar una calificación específica para ella. Escenario 2: Publicación del comentario Dado que escribí una calificación y comentario, Cuando hago clic en “Enviar”, Entonces el sistema guarda y publica la valoración en el perfil del consultor.  | EP04 |
| US018 | Cancelar reserva de sesión | Como usuario. Quiero poder cancelar una reserva de sesión. Para poder modificar mis planes si surge un imprevisto. | Escenario 01: Cancelación exitosa. Dado que tengo una sesión programada y deseo cancelarla, Cuando accedo a la opción de cancelación en mi perfil y confirmó la cancelación, Entonces el sistema cancela la sesión y me envía una notificación confirmando la cancelación. Escenario 02: Error al intentar cancelar. Dado que intento cancelar una sesión programada en un horario muy cercano, Cuando intento cancelarla, Entonces el sistema muestra un mensaje de advertencia o bloqueo de la opción de cancelación. | EP04 |
| US019 | Notificaciones sobre estado de reserva | Como usuario quiero recibir notificaciones sobre el estado de mi reserva para estar informado en todo momento. | Escenario 01: Notificación de recordatorio de sesión programada. Dado que realicé una reserva con un profesional. Cuando hago clic en la notificación. Entonces recibo un detalle sobre la sesión programada junto al día y hora exacta. Escenario 02: Notificación sobre cancelación de sesión. Dado que recibo una notificación de cancelación de sesión. Cuando hago clic en la notificación. Entonces soy redirigido a la plataforma para reagendar la sesión con el profesional. | EP04 |
| US20 | Pago en línea seguro al reservar una sesión de asesoría | Como cliente que necesita asesoría profesional quiero poder pagar en línea de forma segura al momento de reservar una sesión para asegurar mi cita con el consultor y evitar complicaciones en el proceso. | Escenario 01: Pago exitoso. Dado que el pago se ha procesado correctamente. Cuando la transacción se completa. Entonces el sistema debe mostrar un mensaje de confirmación y actualizar el estado de la reserva como “Confirmada”. Escenario 02: Fallo en el pago. Dado que la transacción falla por cualquier motivo. Cuando el sistema detecta el error. Entonces muestra un mensaje al usuario de seleccionar otro método de pago. | EP04 |
| EP05 | Marketing y Crecimiento Profesional | Aumentar la visibilidad de los consultores y facilitar la adquisición de nuevos clientes. |  |  |
| US021 | Publicar testimonios destacados | Como consultor, quiero mostrar testimonios positivos de mis clientes en mi perfil, para generar mayor confianza en nuevos usuarios. | Escenario 1: Selección de testimonios Dado que tengo varias calificaciones positivas, Cuando marco una como “destacada”, Entonces aparece resaltada en la parte superior de mi perfil. Escenario 2: Eliminación de un testimonio destacado Dado que quiero cambiar un testimonio, Cuando desmarco el actual, Entonces este ya no se muestra como destacado en mi perfil. | EP05 |
| US022 | Crear campañas promocionales | Como consultor, quiero poder crear promociones temporales (descuentos o asesorías grupales), para atraer más clientes. | Escenario 1: Creación de descuento Dado que quiero lanzar una promoción, Cuando configuro una campaña con nombre, fecha y porcentaje de descuento, Entonces la promoción queda activa y visible en mi perfil. Escenario 2: Finalización automática de la campaña Dado que la campaña ya terminó, Cuando se alcanza la fecha de fin, Entonces la promoción se desactiva automáticamente. | EP05 |
| US023 | Ver estadísticas de perfil | Como consultor, quiero ver métricas sobre cuántas personas vieron mi perfil, reservaron sesiones o dejaron calificaciones, para medir mi rendimiento. | Escenario 1: Visualización de métricas básicas Dado que accedo a la sección de estadísticas, Cuando ingreso a mi panel de consultor, Entonces puedo ver visitas al perfil, reservas y calificaciones recientes. Escenario 2: Filtros por fecha Dado que quiero analizar mi rendimiento, Cuando selecciono un rango de fechas, Entonces el sistema me muestra los datos correspondientes al período elegido. | EP05 |
| US024 | Gestionar campañas de referidos | Como consultor, quiero invitar a otros consultores o clientes a la plataforma mediante un sistema de referidos, para obtener beneficios por cada nuevo registro. | Escenario 1: Generación de enlace de referido Dado que quiero invitar a nuevos usuarios, Cuando accedo a la sección de referidos, Entonces el sistema genera un enlace único para compartir. Escenario 2: Registro exitoso de un referido Dado que alguien se registra usando mi enlace, Cuando completa el registro, Entonces recibo una notificación y posibles recompensas por el referido. | EP05 |
| US025 | Optimizar visibilidad en buscador | Como consultor, quiero personalizar palabras clave para aparecer más fácilmente en los resultados de búsqueda dentro de la plataforma. | Escenario 1: Edición de palabras clave del perfil Dado que deseo mejorar mi visibilidad, Cuando edito mi perfil y agrego palabras clave relevantes, Entonces mi perfil se ajusta a los criterios del buscador interno. Escenario 2: Aumento de visibilidad tras actualización Dado que añadí nuevas palabras clave, Cuando un usuario busca términos relacionados, Entonces mi perfil aparece mejor posicionado en los resultados. | EP05 |

## 3.1. User Stories v2

En esta sección se presentan los requisitos funcionales definidos para **Finteka**, junto con el conjunto de **Epics** y **User Stories** identificados a partir del Product Backlog elaborado previamente. Las User Stories permiten comprender las necesidades de los usuarios finales, priorizar funcionalidades y organizar el desarrollo incremental del sistema. Asimismo, cada historia incluye criterios de aceptación que validan su cumplimiento.

| Epic / Story ID | Título | Descripción | Criterios de Aceptación | Relacionado con |
|---|---|---|---|---|
| EPIC-01 | Gestión de autenticación | Como usuario, quiero registrarme e iniciar sesión de forma segura para acceder a la plataforma. | - | - |
| EPIC-02 | Gestión de sesiones financieras | Como usuario, quiero registrar y visualizar mis sesiones financieras para administrar mis operaciones. | - | - |
| EPIC-03 | Gestión de clientes | Como administrador, quiero registrar y administrar clientes para controlar sus operaciones dentro del sistema. | - | - |
| EPIC-04 | Dashboard y reportes | Como usuario, quiero visualizar métricas y reportes para analizar resultados financieros. | - | - |
| EPIC-05 | Alertas y monitoreo | Como usuario, quiero recibir alertas configurables para actuar oportunamente ante incidencias. | - | - |
| EPIC-06 | Configuración del sistema | Como administrador, quiero parametrizar salas, horarios y reglas del sistema para adaptarlo a cada operación. | - | - |
| EPIC-07 | Backend API | Como desarrollador, quiero disponer de una API RESTful para integrar frontend, mobile y servicios externos. | - | - |

| Epic / Story ID | Título | Descripción | Criterios de Aceptación | Relacionado con |
|---|---|---|---|---|
| US-001 | Registro de cuenta | Como usuario, quiero registrarme en Finteka para acceder a la plataforma. | **Escenario 01:** Dado que estoy en registro, cuando completo datos válidos, entonces la cuenta se crea correctamente.<br>**Escenario 02:** Si el correo ya existe, entonces se muestra mensaje de error. | EPIC-01 |
| US-002 | Iniciar sesión | Como usuario, quiero iniciar sesión con mis credenciales para acceder a mis funciones. | **Escenario 01:** Dado credenciales válidas, cuando inicio sesión, entonces ingreso al dashboard.<br>**Escenario 02:** Si son incorrectas, entonces se muestra error. | EPIC-01 |
| US-003 | Cerrar sesión | Como usuario, quiero cerrar sesión para proteger mi información. | **Escenario 01:** Dado que estoy autenticado, cuando selecciono cerrar sesión, entonces regreso al login. | EPIC-01 |
| US-004 | Registrar cliente | Como administrador, quiero registrar nuevos clientes para asignarlos al sistema. | **Escenario 01:** Dado formulario completo, cuando guardo, entonces el cliente queda registrado.<br>**Escenario 02:** Si faltan datos obligatorios, se muestra error. | EPIC-03 |
| US-005 | Editar cliente | Como administrador, quiero actualizar información de clientes para mantener datos correctos. | **Escenario 01:** Dado cliente existente, cuando modifico datos, entonces se actualiza correctamente. | EPIC-03 |
| US-006 | Registrar sesión financiera | Como usuario, quiero crear sesiones operativas para registrar actividad financiera. | **Escenario 01:** Dado formulario válido, cuando guardo sesión, entonces se registra exitosamente. | EPIC-02 |
| US-007 | Ver listado de sesiones | Como usuario, quiero ver todas mis sesiones para revisarlas rápidamente. | **Escenario 01:** Dado que ingreso al módulo sesiones, entonces se muestra lista paginada. | EPIC-02 |
| US-008 | Ver detalle de sesión | Como usuario, quiero visualizar información detallada de una sesión para analizar resultados. | **Escenario 01:** Al seleccionar una sesión, entonces se muestran métricas y movimientos asociados. | EPIC-02 |
| US-009 | Dashboard general | Como usuario, quiero ver indicadores clave para conocer el estado actual de la operación. | **Escenario 01:** Al ingresar al dashboard, entonces se muestran KPIs actualizados. | EPIC-04 |
| US-010 | Reporte por fechas | Como usuario, quiero filtrar reportes por rango de fechas para evaluar desempeño histórico. | **Escenario 01:** Al seleccionar fechas válidas, entonces se muestran resultados filtrados. | EPIC-04 |
| US-011 | Exportar reporte | Como usuario, quiero exportar reportes en Excel o PDF para compartir información. | **Escenario 01:** Al elegir formato, entonces se descarga el archivo generado. | EPIC-04 |
| US-012 | Configurar alertas | Como usuario, quiero definir rangos de colores y tiempos para monitoreo automático. | **Escenario 01:** Al guardar configuración, entonces queda almacenada para futuras sesiones. | EPIC-05 |
| US-013 | Recibir alerta automática | Como usuario, quiero recibir alertas visuales cuando una sala supere tiempos establecidos. | **Escenario 01:** Si se supera rango rojo, entonces el sistema muestra alerta inmediata. | EPIC-05 |
| US-014 | Monitorear salas en tiempo real | Como usuario, quiero ver el estado de salas actualizado automáticamente. | **Escenario 01:** La pantalla se refresca periódicamente mostrando colores actuales. | EPIC-05 |
| US-015 | Configurar horarios por sala | Como administrador, quiero asignar horarios distintos por sala para personalizar operación. | **Escenario 01:** Al guardar horario, queda asociado a la sala correspondiente. | EPIC-06 |
| US-016 | Gestionar tipos de sala | Como administrador, quiero registrar tipos de sala para clasificar operaciones. | **Escenario 01:** Se puede crear, editar y desactivar tipos de sala. | EPIC-06 |
| US-017 | Visualizar usuarios del sistema | Como administrador, quiero ver todos los usuarios registrados para gestionarlos. | **Escenario 01:** Se muestra lista con roles y estados. | EPIC-06 |
| TS-001 | Endpoint Auth | Como desarrollador, quiero endpoints de autenticación para login seguro desde frontend. | **Escenario 01:** POST /login devuelve token válido. | EPIC-07 |
| TS-002 | Endpoint Sessions | Como desarrollador, quiero endpoints para crear y consultar sesiones. | **Escenario 01:** GET /sessions devuelve listado.<br>**Escenario 02:** POST /sessions crea sesión nueva. | EPIC-07 |
| TS-003 | Endpoint Clients | Como desarrollador, quiero endpoints para gestionar clientes desde frontend. | **Escenario 01:** CRUD disponible con respuestas estándar. | EPIC-07 |
| TS-004 | Endpoint Monitoring | Como desarrollador, quiero endpoints para monitoreo en tiempo real. | **Escenario 01:** GET /monitor devuelve estados actualizados. | EPIC-07 |


## 3.3. Impact Mapping

Impact map de nuestros segmentos objetivos:

<img width="1636" height="355" alt="image" src="https://github.com/user-attachments/assets/3a8766c1-3535-4e9f-99c5-ecfe28c4e847" />

Link del Impact Mapping:https://miro.com/app/board/uXjVGjii0aI=/?share_link_id=36870517906

Link del Impact Mapping: https://miro.com/app/board/uXjVJGsSlMY=/?share_link_id=506673032577b (cambiar el contenido que esto es de otro tema) 

## 3.4. Product Backlog

Utilizamos la escala de Fibonacci para la estimación de los Story Points.

| # Orden | User Story Id | Título | Descripción | Story Points |
| :--- | :--- | :--- | :--- | :--- |
| 1 | **US201** | Filtros de búsqueda de expertos | Como cliente, deseo filtrar consultores por especialidad y calificación para encontrar al asesor ideal rápidamente. | 5 |
| 2 | **US402** | Agendamiento de sesiones | Como cliente, deseo seleccionar un horario y agendar una sesión para asegurar mi consultoría técnica. | 5 |
| 3 | **US405** | Pago en línea seguro | Como cliente, deseo realizar el pago mediante la plataforma para confirmar mi reserva de manera automática. | 8 |
| 4 | **US401** | Gestión de disponibilidad | Como consultor, deseo configurar mi agenda de disponibilidad para que los clientes puedan agendar sin conflictos. | 8 |
| 5 | **US301** | Visualización de perfil | Como cliente, deseo consultar la experiencia y formación del profesional para validar su capacidad técnica. | 2 |
| 6 | **US101** | Registro de profesionales | Como experto, deseo registrarme en la plataforma para ofrecer mis servicios y gestionar mi perfil profesional. | 3 |
| 7 | **US102** | Registro de clientes | Como usuario interesado, deseo crear una cuenta para buscar expertos y gestionar mis reservas. | 2 |
| 8 | **US302** | Calificación de sesiones | Como cliente, deseo calificar y comentar el servicio recibido para ayudar a otros usuarios en su elección. | 3 |
| 9 | **US403** | Confirmación de sesiones | Como consultor, deseo aceptar o rechazar solicitudes de sesiones para organizar mejor mi tiempo laboral. | 3 |
| 10 | **US202** | Notificaciones de alertas | Como usuario, deseo recibir notificaciones de disponibilidad y recordatorios para no perder mis sesiones programadas. | 3 |
| 11 | **US404** | Seguimiento post-sesión | Como consultor, deseo registrar notas y tareas pendientes para dar un seguimiento adecuado al progreso del cliente. | 3 |
| 12 | **US304** | Favoritos de profesionales | Como cliente, deseo guardar consultores en mi lista de favoritos para acceder a ellos rápidamente en el futuro. | 3 |
| 13 | **US501** | Perfiles recomendados | Como administrador, deseo destacar perfiles profesionales para aumentar su visibilidad ante nuevos clientes. | 2 |
| 14 | **US303** | Actualización de perfil | Como usuario, deseo editar mi información personal y de contacto para mantener mi cuenta actualizada. | 2 |
| 15 | **US502** | SEO y Meta-datos | Como administrador, deseo configurar URLs amigables y metadatos para mejorar el posicionamiento de los expertos en buscadores. | 3 |


<div style="page-break-after: always;"></div>


## 3.4 Product Backlog v2

Utilizamos la escala de Fibonacci para la estimación de los Story Points.

| Orden | User Story Id | Título | Descripción | Story Points (1/2/3/5/8) |
|------|--------------|--------|------------|--------------------------|
| 1 | US-001 | Navegar en la página principal | Como visitante, quiero acceder a la página principal de FinTeka y visualizar un botón de Call to Action para registrarme o buscar expertos, para acceder rápidamente a la plataforma. | 1 |
| 2 | US-002 | Ver información de servicios | Como visitante, quiero visualizar los servicios de consultoría disponibles, para conocer las áreas de asesoría que ofrece la plataforma. | 2 |
| 3 | US-003 | Ver beneficios para clientes | Como visitante, quiero conocer los beneficios de contratar expertos mediante FinTeka, para tomar la decisión de registrarme. | 2 |
| 4 | US-004 | Ver beneficios para consultores | Como profesional, quiero conocer las ventajas de afiliarme a FinTeka, para ofrecer mis servicios en la plataforma. | 2 |
| 5 | US-005 | Revisar testimonios | Como visitante, quiero visualizar reseñas y testimonios de otros usuarios, para conocer experiencias previas antes de registrarme. | 3 |
| 6 | US-006 | Ver información del footer | Como visitante, quiero acceder a enlaces rápidos de contacto, redes sociales y soporte, para navegar fácilmente. | 1 |
| 7 | US-007 | Enviar mensaje de contacto | Como visitante, quiero enviar un mensaje desde la web, para resolver dudas o solicitar información. | 2 |
| 8 | US-008 | Registrar cliente | Como usuario, quiero crear una cuenta en FinTeka para acceder a expertos y reservar sesiones. | 3 |
| 9 | TS-001 | Endpoint User | Como desarrollador frontend, quiero consumir endpoints de usuarios para registrar, autenticar y obtener perfiles desde la app web. | 5 |
| 10 | TS-002 | Endpoint Consultant | Como desarrollador frontend, quiero consumir endpoints de consultores para mostrar perfiles y disponibilidad. | 5 |
| 11 | US-009 | Registrar consultor | Como profesional, quiero registrarme como consultor para ofrecer mis servicios de asesoría. | 3 |
| 12 | US-010 | Buscar expertos | Como cliente, quiero buscar consultores por especialidad, para encontrar al profesional adecuado. | 5 |
| 13 | US-011 | Filtrar por tarifa | Como cliente, quiero filtrar consultores por precio, para ajustarme a mi presupuesto. | 3 |
| 14 | US-012 | Ver perfil profesional | Como cliente, quiero revisar experiencia, especialidades, tarifas y calificaciones de un consultor antes de contratarlo. | 2 |
| 15 | US-013 | Guardar favoritos | Como cliente, quiero guardar consultores favoritos, para acceder rápidamente en futuras búsquedas. | 2 |
| 16 | US-014 | Calificar consultor | Como cliente, quiero dejar una reseña luego de una sesión, para compartir mi experiencia. | 3 |
| 17 | US-015 | Actualizar perfil | Como usuario, quiero editar mis datos personales y de contacto, para mantener mi cuenta actualizada. | 2 |
| 18 | US-016 | Gestionar servicios | Como consultor, quiero crear y administrar mis servicios profesionales, para ofrecer distintas asesorías. | 5 |
| 19 | US-017 | Configurar disponibilidad | Como consultor, quiero establecer horarios disponibles, para recibir reservas sin conflictos. | 5 |
| 20 | TS-003 | Endpoint Schedule | Como desarrollador frontend, quiero consumir endpoints de agenda para reservas y disponibilidad. | 5 |
| 21 | US-018 | Reservar sesión | Como cliente, quiero agendar una sesión con un consultor, para recibir asesoría profesional. | 8 |
| 22 | US-019 | Cancelar reserva | Como cliente, quiero cancelar una sesión programada, para reorganizar mi agenda. | 2 |
| 23 | US-020 | Ver historial de sesiones | Como usuario, quiero revisar sesiones anteriores, para dar seguimiento a mis procesos. | 3 |
| 24 | US-021 | Confirmar reserva | Como cliente, quiero recibir confirmación de mi sesión reservada, para asegurar la cita. | 2 |
| 25 | US-022 | Pago seguro en línea | Como cliente, quiero pagar desde la plataforma de forma segura, para confirmar mi reserva automáticamente. | 8 |
| 26 | TS-004 | Integración pasarela de pago | Como desarrollador, quiero integrar una pasarela de pagos segura para procesar transacciones online. | 5 |
| 27 | US-023 | Recibir notificaciones | Como usuario, quiero recibir recordatorios y alertas sobre mis sesiones programadas. | 3 |
| 28 | TS-005 | Sistema de notificaciones | Como desarrollador, quiero implementar notificaciones por correo y plataforma para sesiones y cambios de estado. | 5 |
| 29 | US-024 | Agendar seguimiento | Como cliente, quiero reservar una sesión de seguimiento con el mismo consultor, para continuar mi asesoría. | 3 |
| 30 | US-025 | Enviar recomendaciones | Como consultor, quiero compartir materiales o recomendaciones después de la sesión, para complementar el servicio. | 3 |
| 31 | US-026 | Responder mensajes | Como consultor, quiero responder mensajes de clientes, para mantener buena comunicación. | 3 |
| 32 | US-027 | Ver estadísticas de perfil | Como consultor, quiero visualizar visitas, reservas y valoraciones, para medir mi rendimiento. | 5 |
| 33 | US-028 | Crear promociones | Como consultor, quiero lanzar descuentos temporales, para atraer nuevos clientes. | 5 |
| 34 | US-029 | Publicar testimonios destacados | Como consultor, quiero mostrar opiniones positivas destacadas en mi perfil, para generar confianza. | 2 |
| 35 | US-030 | Gestionar referidos | Como consultor, quiero invitar nuevos usuarios mediante enlaces de referido, para obtener beneficios. | 3 |

