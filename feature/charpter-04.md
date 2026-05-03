# Chapter IV: Product Architecture Design

## 4.1 Design Concepts, Viewpoints & ER Diagrams

### 4.1.1 Principles Statements  
### 4.1.2 Approaches Statements: Architectural Styles & Patterns  
### 4.1.3 Context Diagram  
### 4.1.4 Approach-Driven Viewpoints Diagrams  
### 4.1.5 Relational / Non-Relational Database Diagram 
Para el ecosistema de **Finteka**, se ha diseñado una arquitectura de persistencia políglota que separa las operaciones financieras críticas de los flujos de alta disponibilidad y datos no estructurados. Basándonos en los requerimientos del proyecto, se ha evolucionado el modelo original hacia una estructura híbrida:

1.  **Modelo Relacional (SQL):** Gestiona el núcleo de confianza (ACID). Se han reemplazado conceptos genéricos por entidades de dominio específicas como `Consultants`, `Advisory_Sessions` y `Payments`.
2.  **Modelo No Relacional (NoSQL):** Implementado para la gestión de mensajes de chat (US-04) y logs de auditoría (US-08), permitiendo escalabilidad horizontal sin degradar el rendimiento de la base de datos principal.

#### Diagrama de Base de Datos Híbrido

![Diagrama de Base de Datos Híbrido - Finteka](https://res.cloudinary.com/dx0i2vioe/image/upload/f_auto,q_auto/Captura_de_pantalla_2026-04-27_a_la_s_5.06.10_a._m._vi5c1x)

#### Explicación del Gráfico y Justificación Técnica

El diagrama presenta una arquitectura dividida en dos grandes bloques tecnológicos para optimizar los Atributos de Calidad del sistema:

**A. Bloque Relacional (Gestión Transaccional):**
* **Gestión de Perfiles (`USERS`, `CONSULTANTS`, `CLIENTS`):** Se utiliza una relación de especialización para diferenciar a los usuarios. Esto permite soportar el **Plan Premium** y las suscripciones mencionadas en la documentación, vinculando cada perfil con sus permisos específicos.
* **Núcleo de Intermediación (`ADVISORY_SESSIONS`):** Es la tabla central que conecta a clientes y asesores. Al ser relacional, garantiza que cada sesión agendada sea única y coherente.
* **Disponibilidad en Tiempo Real (`BOOKING_SLOTS`):** Esta tabla gestiona los bloques de tiempo. Su diseño permite consultas rápidas de disponibilidad, evitando el "double-booking" mediante restricciones de integridad referencial.
* **Transaccionalidad Financiera (`PAYMENTS`):** Crucial para el cobro de comisiones de la plataforma. Se ha diseñado para soportar el **patrón Saga**, permitiendo gestionar estados transaccionales (Pendiente, Completado, Fallido) en procesos distribuidos.

**B. Bloque NoSQL (Datos de Alto Volumen):**
* **Historial de Comunicación (`CHAT_MESSAGES`):** Colección basada en documentos que almacena la interacción entre cliente y asesor. Al ser NoSQL, permite una escritura veloz y flexible para mensajes de texto y metadatos del chat.
* **Auditoría y Seguridad (`USER_ACTIVITY_LOGS`):** Soporta el Atributo de Calidad de **Auditoría**. Almacena de forma inmutable cada acción crítica del usuario (logins, cambios de saldo, postulaciones) sin estresar las tablas transaccionales de la base de datos SQL.
### 4.1.6 Design Patterns  
### 4.1.7 Tactics  
Las tácticas arquitecturales son las decisiones técnicas concretas implementadas para satisfacer los Atributos de Calidad (Quality Attributes) exigidos por el ecosistema de **Finteka**. Estas decisiones permiten que el sistema sea resiliente, seguro y eficiente bajo las condiciones operativas de Nova Asesors.

#### Mapa de Tácticas Arquitecturales

![Mapa de Tácticas Arquitecturales - Finteka](https://res.cloudinary.com/dx0i2vioe/image/upload/f_auto,q_auto/Captura_de_pantalla_2026-04-27_a_la_s_5.12.24_a._m._mk0dic)

#### Justificación Técnica (Basada en los RNF del Proyecto)

Para garantizar que la arquitectura soporte los requerimientos no funcionales (RNF) detallados en el proyecto, se han aplicado las siguientes tácticas:

**A. SEGURIDAD (Security)**
* **Táctica:** *Authenticate Actors / Authorize.*
* **Implementación:** Se implementa una **Autenticación Descentralizada** mediante el estándar **OAuth2** utilizando tokens **JWT (JSON Web Tokens)**. 
* **Justificación:** Dado el carácter financiero de la aplicación, es imperativo asegurar que cada petición sea legítima. Se utiliza **RBAC (Control de Acceso Basado en Roles)** para diferenciar las capacidades entre Clientes y Asesores, protegiendo los endpoints sensibles de la API mediante un API Gateway (ej. Kong o AWS API Gateway).

**B. DISPONIBILIDAD (Availability)**
* **Táctica:** *Active Redundancy (Failover).*
* **Implementación:** La base de datos relacional core y los microservicios se despliegan en una arquitectura **Multi-AZ (Multi-Availability Zones)** con replicación síncrona.
* **Justificación:** El sistema debe garantizar un punto de recuperación de datos igual a cero (**RPO=0**). En caso de una caída en la zona principal, el balanceador de carga redirige el tráfico a la zona de reserva de forma transparente, asegurando la continuidad del servicio para las postulaciones y sesiones.

**C. RENDIMIENTO (Performance)**
* **Táctica:** *Manage Resources (Caching).*
* **Implementación:** Uso de **Redis Caching** como capa de almacenamiento en memoria para datos de lectura intensiva.
* **Justificación:** Para satisfacer los requerimientos de latencia ultra-baja (respuesta de API **<1s**), se cachean consultas frecuentes como los perfiles de asesores, balances de cuentas y bloques de disponibilidad. Esto reduce la carga sobre la base de datos relacional y acelera la experiencia del usuario en la aplicación móvil.

**D. INTEGRABILIDAD (Integrability)**
* **Táctica:** *External Integration Layer.*
* **Implementación:** Uso de microservicios especializados para la comunicación con pasarelas de pago externas y servicios de notificación.
* **Justificación:** Permite que Finteka interactúe con sistemas de terceros (ej. Stripe o PayPal) de forma desacoplada, facilitando el cobro de comisiones y la confirmación de asesorías sin comprometer la estabilidad del núcleo del sistema.
## 4.2 Architectural Drivers

### 4.1.8 Design Purpose

El propósito del diseño de **Finteka** es proporcionar una plataforma de intermediación financiera escalable, centrada en el usuario y técnicamente resiliente. Los objetivos principales son:

1.  **Fiabilidad Transaccional:** Garantizar que el flujo de agendamiento y pago sea atómico. Si una parte del proceso falla, el sistema debe revertir los cambios automáticamente (Patrón Saga).
2.  **Baja Latencia en Dispositivos Móviles:** Optimizar la comunicación mediante una capa de API Gateway que reduzca el "over-fetching" de datos, asegurando una experiencia fluida para el cliente.
3.  **Mantenibilidad Modular:** Mediante una arquitectura de microservicios, permitir que el equipo de Nova Asesors despliegue mejoras en el módulo de chat o pagos de forma independiente, reduciendo el riesgo de errores en producción.

---

### 4.1.9 Primary Functionality (Primary User Stories)

La arquitectura ha sido diseñada para dar soporte directo a las historias de usuario de mayor valor de negocio, asegurando que los flujos técnicos sean eficientes:

| ID | Historia de Usuario | Flujo Técnico de Arquitectura | Componente Crítico |
| :--- | :--- | :--- | :--- |
| **US-01** | **Agendar Sesión de Asesoría** | El `Booking Service` realiza una reserva atómica verificando la disponibilidad en tiempo real en la BD Relacional. | Booking Microservice |
| **US-02** | **Visualizar Perfil de Asesor** | Se utiliza una táctica de caché (`Read-through`) para servir la información del asesor desde **Redis**, minimizando la latencia. | Consultant Microservice / Redis |
| **US-03** | **Pago Seguro y Comisión** | Integración asíncrona con pasarelas de pago. El sistema calcula la comisión de Nova Asesors antes de confirmar la sesión. | Payment Gateway Service |
| **US-04** | **Chat en Tiempo Real** | Comunicación bidireccional mediante **WebSockets** con persistencia en el almacén de documentos NoSQL para historial inmediato. | Chat Service (WebSocket) |

### 4.1.10 Quality Attribute Scenarios

Los escenarios de atributos de calidad (Quality Attribute Scenarios) constituyen uno de los mecanismos más importantes para validar si la arquitectura propuesta para **FinTeka** será capaz de satisfacer las exigencias funcionales y no funcionales del negocio. Estos escenarios permiten transformar requerimientos abstractos —como seguridad, rendimiento o disponibilidad— en situaciones concretas medibles y verificables.

La definición de estos escenarios resulta crítica debido a que FinTeka opera sobre procesos sensibles relacionados con:
- Gestión de asesorías profesionales.
- Información personal de usuarios.
- Procesos de pago y comisiones.
- Comunicación en tiempo real.
- Disponibilidad continua del servicio.

Por ello, la arquitectura fue diseñada considerando atributos de calidad prioritarios alineados con las necesidades operativas de Nova Asesors y con las expectativas de confiabilidad propias de una plataforma financiera digital moderna.

Cada escenario se estructura bajo los siguientes elementos:
- **Fuente:** entidad que origina el evento.
- **Estímulo:** acción o evento que afecta al sistema.
- **Entorno:** contexto operativo donde ocurre el estímulo.
- **Artefacto:** componente arquitectónico impactado.
- **Respuesta:** comportamiento esperado del sistema.
- **Medida de Respuesta:** criterio cuantificable para evaluar el cumplimiento.

---

## A. Escenarios de Seguridad (Security)

La seguridad representa uno de los atributos arquitectónicos más críticos dentro del ecosistema FinTeka debido a que la plataforma procesa:
- Información financiera.
- Datos personales.
- Historial de pagos.
- Conversaciones privadas.
- Información sensible de autenticación.

El sistema debe protegerse frente a amenazas externas e internas garantizando:
- Confidencialidad.
- Integridad.
- Autenticidad.
- Trazabilidad.

---

### Escenario A1 — Acceso No Autorizado a Recursos Protegidos

| Elemento | Descripción |
| :--- | :--- |
| **Fuente** | Usuario malicioso o actor no autenticado |
| **Estímulo** | Intento de acceso a endpoints protegidos |
| **Entorno** | Operación normal del sistema |
| **Artefacto** | API Gateway / Authentication Service |
| **Respuesta** | El sistema valida el JWT y bloquea inmediatamente el acceso |
| **Medida de Respuesta** | Validación menor a 300 ms y rechazo del 100% de solicitudes inválidas |

#### Justificación Técnica
Debido a que múltiples servicios son expuestos mediante APIs públicas, FinTeka implementa:
- OAuth2 para autenticación descentralizada.
- JWT para validación stateless.
- API Gateway para centralizar políticas de acceso.
- Middleware de autorización RBAC.

La arquitectura evita exponer directamente microservicios internos, reduciendo riesgos de acceso indebido.

---

### Escenario A2 — Protección de Información Sensible

| Elemento | Descripción |
| :--- | :--- |
| **Fuente** | Usuario autenticado |
| **Estímulo** | Transmisión de información financiera |
| **Entorno** | Pago o reserva de sesión |
| **Artefacto** | Payment Service |
| **Respuesta** | La información se transmite mediante canales cifrados |
| **Medida de Respuesta** | 100% de comunicaciones bajo HTTPS/TLS |

#### Justificación Técnica
Toda la comunicación entre:
- Frontend.
- API Gateway.
- Microservicios.
- Servicios externos.

se realiza utilizando cifrado TLS para prevenir:
- Intercepción de tráfico.
- Ataques MITM.
- Manipulación de datos.

Adicionalmente:
- Las contraseñas se almacenan con hashing seguro.
- Los tokens poseen expiración controlada.
- Las credenciales nunca se almacenan en texto plano.

---

### Escenario A3 — Escalamiento de Privilegios

| Elemento | Descripción |
| :--- | :--- |
| **Fuente** | Usuario autenticado |
| **Estímulo** | Intento de ejecutar acciones de administrador |
| **Entorno** | Operación normal |
| **Artefacto** | Authorization Layer |
| **Respuesta** | El sistema verifica permisos RBAC y deniega la operación |
| **Medida de Respuesta** | 0 accesos exitosos fuera del rol autorizado |

#### Justificación Técnica
FinTeka distingue múltiples perfiles:
- Clientes.
- Consultores.
- Administradores.

Cada rol posee permisos específicos definidos centralizadamente mediante RBAC, evitando:
- Acceso indebido a datos.
- Manipulación administrativa.
- Ejecución de operaciones críticas no autorizadas.

---

## B. Escenarios de Disponibilidad (Availability)

La disponibilidad es fundamental debido a que FinTeka ofrece:
- Reservas en tiempo real.
- Procesamiento de pagos.
- Comunicación instantánea.
- Gestión continua de agendas.

La plataforma debe permanecer operativa incluso frente a:
- Fallas de infraestructura.
- Sobrecarga de tráfico.
- Errores de servicios.
- Caídas parciales.

---

### Escenario B1 — Falla de Zona de Disponibilidad

| Elemento | Descripción |
| :--- | :--- |
| **Fuente** | Infraestructura cloud |
| **Estímulo** | Caída completa de una Availability Zone |
| **Entorno** | Alta concurrencia |
| **Artefacto** | Base de datos relacional y microservicios |
| **Respuesta** | El tráfico es redirigido automáticamente hacia instancias secundarias |
| **Medida de Respuesta** | Recuperación menor a 30 segundos y RPO = 0 |

#### Justificación Técnica
La arquitectura utiliza:
- Replicación Multi-AZ.
- Balanceadores de carga.
- Failover automático.
- Replicación síncrona.

Esto permite garantizar continuidad operacional incluso ante fallos críticos de infraestructura.

---

### Escenario B2 — Reinicio Automático de Servicios

| Elemento | Descripción |
| :--- | :--- |
| **Fuente** | Error interno del microservicio |
| **Estímulo** | Excepción crítica o caída del contenedor |
| **Entorno** | Operación continua |
| **Artefacto** | Kubernetes / Container Runtime |
| **Respuesta** | El servicio es reiniciado automáticamente |
| **Medida de Respuesta** | Recuperación automática menor a 1 minuto |

#### Justificación Técnica
La orquestación mediante contenedores permite:
- Health checks automáticos.
- Reinicio de pods defectuosos.
- Autoescalado.
- Recuperación rápida.

Esto reduce intervención manual y mejora resiliencia.

---

## C. Escenarios de Rendimiento (Performance)

La experiencia de usuario depende directamente de la capacidad del sistema para responder rápidamente frente a:
- Búsquedas.
- Reservas.
- Carga de perfiles.
- Mensajería.
- Procesamiento financiero.

La arquitectura busca minimizar:
- Latencia.
- Tiempo de espera.
- Sobrecarga de recursos.

---

### Escenario C1 — Consulta de Perfiles de Consultores

| Elemento | Descripción |
| :--- | :--- |
| **Fuente** | Usuario móvil |
| **Estímulo** | Solicitud de búsqueda de especialistas |
| **Entorno** | Hora pico |
| **Artefacto** | Consultant Service / Redis |
| **Respuesta** | La información es servida desde caché |
| **Medida de Respuesta** | Tiempo promedio menor a 1 segundo |

#### Justificación Técnica
Redis permite:
- Evitar consultas repetitivas.
- Reducir carga SQL.
- Acelerar lecturas frecuentes.
- Mejorar experiencia móvil.

La arquitectura aplica:
- Caché Read-through.
- Expiración controlada.
- Invalidación automática.

---

### Escenario C2 — Alta Concurrencia de Chats

| Elemento | Descripción |
| :--- | :--- |
| **Fuente** | Usuarios concurrentes |
| **Estímulo** | Envío simultáneo de mensajes |
| **Entorno** | Alta actividad |
| **Artefacto** | Chat Service |
| **Respuesta** | El sistema distribuye conexiones mediante WebSockets |
| **Medida de Respuesta** | Latencia menor a 500 ms |

#### Justificación Técnica
El sistema utiliza:
- WebSockets persistentes.
- Persistencia NoSQL.
- Balanceo de conexiones.
- Comunicación asíncrona.

Esto garantiza mensajería fluida en tiempo real.

---

## D. Escenarios de Escalabilidad (Scalability)

FinTeka debe soportar crecimiento progresivo tanto en:
- Usuarios.
- Consultores.
- Reservas.
- Transacciones.
- Mensajes.

La arquitectura debe escalar sin rediseños estructurales.

---

### Escenario D1 — Incremento Masivo de Usuarios

| Elemento | Descripción |
| :--- | :--- |
| **Fuente** | Campaña comercial |
| **Estímulo** | Multiplicación de usuarios concurrentes |
| **Entorno** | Alta demanda |
| **Artefacto** | Microservicios |
| **Respuesta** | Se crean nuevas instancias automáticamente |
| **Medida de Respuesta** | SLA superior al 95% |

#### Justificación Técnica
La arquitectura desacoplada permite:
- Escalabilidad horizontal.
- Autoescalado dinámico.
- Distribución de carga.
- Aislamiento funcional.

Cada servicio puede escalar independientemente según necesidad.

---

## E. Escenarios de Integrabilidad (Integrability)

FinTeka depende de múltiples integraciones externas:
- Pasarelas de pago.
- Servicios de notificación.
- APIs de autenticación.
- Servicios cloud.

---

### Escenario E1 — Falla Temporal de Pasarela de Pago

| Elemento | Descripción |
| :--- | :--- |
| **Fuente** | Servicio externo |
| **Estímulo** | Timeout o indisponibilidad |
| **Entorno** | Pago en proceso |
| **Artefacto** | Payment Integration Service |
| **Respuesta** | El sistema activa Retry y Circuit Breaker |
| **Medida de Respuesta** | No pérdida de consistencia transaccional |

#### Justificación Técnica
Se utilizan patrones:
- Retry.
- Circuit Breaker.
- Timeout controlado.
- Cola de eventos.

Esto evita propagar fallas externas al núcleo del sistema.

---

## F. Escenarios de Auditabilidad (Auditability)

La auditabilidad es indispensable para:
- Seguridad.
- Trazabilidad.
- Monitoreo.
- Investigación de incidentes.

---

### Escenario F1 — Registro de Actividades Críticas

| Elemento | Descripción |
| :--- | :--- |
| **Fuente** | Usuario autenticado |
| **Estímulo** | Login, pago o modificación sensible |
| **Entorno** | Operación normal |
| **Artefacto** | User Activity Logs |
| **Respuesta** | El evento se registra de forma inmutable |
| **Medida de Respuesta** | Persistencia menor a 2 segundos |

#### Justificación Técnica
Los logs:
- Se almacenan en NoSQL.
- Son independientes del núcleo SQL.
- Permiten análisis posteriores.
- Facilitan observabilidad distribuida.

---

# 4.1.11 Constraints

Las restricciones arquitectónicas representan limitaciones obligatorias que condicionan el diseño técnico del ecosistema FinTeka. Estas restricciones pueden originarse desde:
- Necesidades del negocio.
- Limitaciones tecnológicas.
- Requerimientos regulatorios.
- Condiciones operativas.
- Estrategias organizacionales.

El cumplimiento de estas restricciones garantiza que la arquitectura permanezca:
- Viable.
- Escalable.
- Segura.
- Mantenible.
- Alineada con los objetivos de Nova Asesors.

---

## A. Restricciones Tecnológicas

### Arquitectura Basada en Microservicios

La solución debe implementarse obligatoriamente mediante microservicios independientes.

#### Implicancias
- Cada dominio funcional debe estar desacoplado.
- Los servicios deben desplegarse individualmente.
- La comunicación debe realizarse vía APIs o eventos.

#### Justificación
Esto permite:
- Escalabilidad independiente.
- Reducción de impacto ante fallos.
- Evolución modular.

---

### Persistencia Políglota

El sistema debe utilizar:
- SQL para operaciones críticas.
- NoSQL para datos de alta concurrencia.

#### Restricción
No se permite centralizar toda la información en una única base de datos.

#### Justificación
Cada tipo de persistencia responde mejor a necesidades específicas:
- ACID para pagos y reservas.
- Alta velocidad para chats y logs.

---

### Uso Obligatorio de APIs

Los microservicios:
- No pueden acceder directamente a bases de datos ajenas.
- Deben comunicarse únicamente mediante APIs y eventos.

#### Beneficios
- Bajo acoplamiento.
- Mejor mantenibilidad.
- Mayor seguridad.

---

## B. Restricciones Operacionales

### Alta Disponibilidad Obligatoria

La plataforma debe mantener continuidad operacional incluso ante:
- Fallas de servidores.
- Caídas parciales.
- Sobrecarga.

#### Requerimientos
- Multi-AZ.
- Replicación síncrona.
- Failover automático.

---

### Compatibilidad Multiplataforma

El sistema debe funcionar correctamente en:
- Web desktop.
- Navegadores móviles.
- Tablets.

#### Justificación
La mayoría de usuarios accederá desde dispositivos móviles.

---

## C. Restricciones de Seguridad

### Protección de Datos Sensibles

Toda información crítica debe:
- Estar cifrada.
- Transmitirse mediante HTTPS.
- Validarse mediante autenticación segura.

---

### Control de Acceso Basado en Roles

El sistema debe implementar RBAC para:
- Clientes.
- Consultores.
- Administradores.

No se permite acceso libre a operaciones sensibles.

---

## D. Restricciones de Negocio

### Gestión de Comisiones

La plataforma debe calcular automáticamente:
- Comisión de Nova Asesors.
- Estado financiero de cada transacción.

---

### Integración con Terceros

FinTeka debe integrarse con:
- Pasarelas de pago.
- Sistemas de notificación.
- Servicios cloud.

---

### Escalabilidad Comercial

La arquitectura debe soportar:
- Nuevos módulos.
- Nuevos tipos de asesoría.
- Incremento masivo de usuarios.

sin necesidad de rediseñar el núcleo del sistema.

---

# 4.1.12 Architectural Concerns

Las preocupaciones arquitectónicas representan los aspectos críticos que influyen directamente en las decisiones técnicas adoptadas para el diseño de FinTeka. Estas preocupaciones reflejan riesgos, desafíos y necesidades estratégicas que deben ser resueltos para garantizar que la plataforma opere de manera:
- Confiable.
- Segura.
- Escalable.
- Eficiente.
- Mantenible.

---

## A. Consistencia Transaccional Distribuida

Uno de los mayores desafíos arquitectónicos es garantizar consistencia entre:
- Reservas.
- Pagos.
- Disponibilidad.
- Confirmaciones.

Debido al uso de microservicios, las transacciones distribuidas pueden generar:
- Duplicidad de reservas.
- Estados inconsistentes.
- Cobros fallidos.

### Solución Arquitectónica
- Patrón Saga.
- Eventos compensatorios.
- Estados transaccionales.
- Validación distribuida.

---

## B. Seguridad Financiera

La plataforma gestiona:
- Pagos.
- Información personal.
- Datos financieros.

### Riesgos
- Robo de credenciales.
- Accesos indebidos.
- Intercepción de tráfico.
- Fraude.

### Mitigación
- OAuth2.
- JWT.
- RBAC.
- HTTPS/TLS.
- API Gateway.

---

## C. Rendimiento Bajo Alta Concurrencia

FinTeka debe responder rápidamente incluso bajo:
- Miles de usuarios concurrentes.
- Chats simultáneos.
- Reservas masivas.

### Riesgos
- Latencia elevada.
- Saturación SQL.
- Cuellos de botella.

### Mitigación
- Redis.
- Balanceadores.
- WebSockets.
- Persistencia NoSQL.
- Autoescalado.

---

## D. Complejidad de Microservicios

Aunque los microservicios aportan escalabilidad, también generan:
- Complejidad operacional.
- Dificultad de monitoreo.
- Mayor coordinación.

### Necesidades
- Observabilidad distribuida.
- Centralización de logs.
- Trazabilidad.

---

## E. Dependencia de Servicios Externos

FinTeka depende de:
- Pasarelas de pago.
- APIs externas.
- Servicios cloud.

### Riesgos
- Latencia.
- Caídas externas.
- Timeouts.

### Mitigación
- Circuit Breakers.
- Retries.
- Timeout controlado.
- Desacoplamiento mediante eventos.

---

## F. Evolución y Mantenibilidad

La plataforma debe evolucionar continuamente:
- Nuevos módulos.
- Nuevas integraciones.
- Nuevas reglas de negocio.

### Preocupación Principal
Evitar dependencias rígidas entre componentes.

### Estrategias
- Arquitectura desacoplada.
- APIs versionadas.
- Separación por dominios.
- Despliegues independientes.

---

## G. Observabilidad y Monitoreo

La naturaleza distribuida del sistema requiere:
- Monitoreo centralizado.
- Métricas en tiempo real.
- Detección temprana de fallos.

### Implementación
- Logs centralizados.
- Métricas de rendimiento.
- Distributed tracing.
- Alertas automatizadas.

---

## H. Experiencia de Usuario en Tiempo Real

El éxito de FinTeka depende de ofrecer:
- Fluidez.
- Baja latencia.
- Comunicación instantánea.

### Riesgos
- Retrasos en mensajes.
- Lentitud de búsqueda.
- Saturación de conexiones.

### Soluciones
- WebSockets.
- Redis.
- Balanceo de carga.
- Caché distribuida.

---

## I. Gestión de Datos Híbridos

La coexistencia entre SQL y NoSQL introduce desafíos relacionados con:
- Sincronización.
- Consistencia.
- Integridad de datos.

### Estrategias
- Separación por dominios.
- APIs especializadas.
- Eventos asincrónicos.
- Validaciones transaccionales.

---

## J. Continuidad Operacional y Recuperación

La plataforma debe recuperarse rápidamente ante:
- Errores críticos.
- Caídas parciales.
- Fallos cloud.

### Implementaciones
- Multi-AZ.
- Replicación.
- Failover automático.
- Backups continuos.

Esto garantiza resiliencia empresarial y continuidad de servicio para Nova Asesors. 

## 4.3 ADD Iterations

### 4.2.X Iteration N: <Iteration Name>

#### 4.2.X.1 Architectural Design Backlog N  
#### 4.2.X.2 Establish Iteration Goal by Selecting Drivers  
#### 4.2.X.3 Choose One or More Elements of the System to Refine  
#### 4.2.X.4 Choose One or More Design Concepts that Satisfy the Selected Drivers  
#### 4.2.X.5 Instantiate Architectural Elements, Allocate Responsibilities, and Define Interfaces  
#### 4.2.X.6 Sketch Views (C4 & UML) and Record Design Decisions  
#### 4.2.X.7 Analysis of Current Design and Review Iteration Goal (Kanban Board) (Progress 2)
