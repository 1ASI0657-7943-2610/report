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

Los escenarios de atributos de calidad (*Quality Attribute Scenarios*) permiten validar de manera estructurada que la arquitectura propuesta para **FinTeka** será capaz de satisfacer los requerimientos no funcionales definidos por Nova Asesors. Estos escenarios transforman atributos abstractos como seguridad, disponibilidad o rendimiento en situaciones concretas, medibles y verificables dentro del contexto operativo de la plataforma.

Debido a que FinTeka gestiona:
- Procesos financieros,
- Información personal,
- Comunicación en tiempo real,
- Reservas de asesorías,
- Integraciones con terceros,

la arquitectura debe responder de manera resiliente, segura y eficiente frente a eventos de alta concurrencia, fallos de infraestructura y amenazas de seguridad.

Cada escenario arquitectónico se define mediante:
- **Fuente:** entidad que genera el evento.
- **Estímulo:** acción que afecta al sistema.
- **Entorno:** contexto operacional.
- **Artefacto:** componente impactado.
- **Respuesta:** comportamiento esperado.
- **Medida de Respuesta:** criterio cuantificable.

---

#### Justificación Técnica General

Los atributos de calidad definidos para FinTeka están directamente alineados con:
- Los requerimientos no funcionales del proyecto.
- La naturaleza financiera de la plataforma.
- La necesidad de escalabilidad futura.
- La experiencia móvil del usuario.
- La continuidad operacional de Nova Asesors.

La arquitectura basada en microservicios, persistencia políglota, API Gateway y despliegues distribuidos permite abordar estos escenarios mediante tácticas concretas de:
- redundancia,
- desacoplamiento,
- caché,
- observabilidad,
- autenticación,
- tolerancia a fallos.

---

### A. SEGURIDAD (Security)

La seguridad representa uno de los atributos críticos del ecosistema FinTeka debido a que la plataforma administra:
- información financiera,
- datos personales,
- sesiones privadas,
- autenticación de usuarios,
- historial de pagos y reservas.

El objetivo principal es garantizar:
- confidencialidad,
- integridad,
- autenticidad,
- trazabilidad de las operaciones.

---

##### Escenario A1 — Acceso No Autorizado

| Elemento | Descripción |
| :--- | :--- |
| **Fuente** | Usuario no autenticado o atacante externo |
| **Estímulo** | Intento de acceso a endpoints protegidos |
| **Entorno** | Operación normal |
| **Artefacto** | API Gateway / Authentication Service |
| **Respuesta** | El sistema valida el token JWT y bloquea automáticamente la solicitud |
| **Medida de Respuesta** | Tiempo de validación menor a 300 ms y 100% de rechazo de accesos inválidos |

###### Justificación Técnica

Para proteger los recursos críticos del sistema:
- se implementa OAuth2 para autenticación descentralizada,
- JWT para validación stateless,
- RBAC para control de permisos,
- API Gateway para centralización de políticas de seguridad.

Esto evita accesos indebidos y protege la información sensible de la plataforma.

---

##### Escenario A2 — Protección de Información Sensible

| Elemento | Descripción |
| :--- | :--- |
| **Fuente** | Usuario autenticado |
| **Estímulo** | Envío de información financiera |
| **Entorno** | Proceso de pago o reserva |
| **Artefacto** | Payment Service |
| **Respuesta** | La información se transmite mediante canales cifrados |
| **Medida de Respuesta** | 100% de las comunicaciones protegidas bajo HTTPS/TLS |

###### Justificación Técnica

Toda la comunicación entre:
- frontend,
- backend,
- microservicios,
- servicios externos,

se realiza utilizando HTTPS/TLS para prevenir:
- intercepción de datos,
- ataques MITM,
- manipulación de tráfico.

Adicionalmente:
- las contraseñas se almacenan mediante hashing seguro,
- los tokens poseen expiración limitada,
- no se almacenan credenciales en texto plano.

---

##### Escenario A3 — Escalamiento de Privilegios

| Elemento | Descripción |
| :--- | :--- |
| **Fuente** | Usuario autenticado |
| **Estímulo** | Intento de acceso a funciones administrativas |
| **Entorno** | Operación normal |
| **Artefacto** | Authorization Layer |
| **Respuesta** | El sistema valida permisos RBAC y deniega el acceso |
| **Medida de Respuesta** | 0 accesos exitosos fuera del rol autorizado |

###### Justificación Técnica

FinTeka diferencia:
- Clientes,
- Consultores,
- Administradores,

mediante RBAC, garantizando separación estricta de privilegios y evitando accesos no autorizados a funcionalidades críticas.

---

### B. DISPONIBILIDAD (Availability)

La disponibilidad es esencial debido a que FinTeka ofrece:
- reservas en tiempo real,
- pagos digitales,
- mensajería instantánea,
- gestión continua de agendas.

La plataforma debe mantenerse operativa incluso ante fallos parciales de infraestructura.

---

##### Escenario B1 — Falla de Infraestructura

| Elemento | Descripción |
| :--- | :--- |
| **Fuente** | Infraestructura cloud |
| **Estímulo** | Caída de una Availability Zone |
| **Entorno** | Alta concurrencia |
| **Artefacto** | Base de datos y microservicios |
| **Respuesta** | El tráfico es redirigido automáticamente hacia instancias secundarias |
| **Medida de Respuesta** | Recuperación menor a 30 segundos y RPO = 0 |

###### Justificación Técnica

La arquitectura implementa:
- despliegue Multi-AZ,
- replicación síncrona,
- balanceadores de carga,
- failover automático.

Esto garantiza continuidad operacional y evita pérdida de información crítica.

---

##### Escenario B2 — Recuperación Automática de Servicios

| Elemento | Descripción |
| :--- | :--- |
| **Fuente** | Error interno del servicio |
| **Estímulo** | Caída de un contenedor |
| **Entorno** | Operación continua |
| **Artefacto** | Kubernetes / Runtime de contenedores |
| **Respuesta** | El servicio se reinicia automáticamente |
| **Medida de Respuesta** | Recuperación menor a 1 minuto |

###### Justificación Técnica

El uso de contenedores permite:
- health checks automáticos,
- reinicio de instancias defectuosas,
- autoescalado,
- alta resiliencia operacional.

---

### C. RENDIMIENTO (Performance)

La experiencia del usuario depende directamente de la capacidad del sistema para responder rápidamente frente a:
- búsquedas,
- reservas,
- carga de perfiles,
- mensajería,
- procesos financieros.

La arquitectura busca minimizar:
- latencia,
- tiempos de espera,
- saturación de recursos.

---

##### Escenario C1 — Consulta de Perfiles de Consultores

| Elemento | Descripción |
| :--- | :--- |
| **Fuente** | Usuario móvil |
| **Estímulo** | Solicitud de búsqueda de consultores |
| **Entorno** | Hora pico |
| **Artefacto** | Consultant Service / Redis Cache |
| **Respuesta** | La información es servida desde caché |
| **Medida de Respuesta** | Tiempo promedio menor a 1 segundo |

###### Justificación Técnica

Redis permite:
- almacenar consultas frecuentes,
- reducir carga SQL,
- acelerar respuestas,
- mejorar experiencia móvil.

La arquitectura utiliza:
- caché Read-through,
- expiración controlada,
- actualización automática de datos.

---

##### Escenario C2 — Comunicación en Tiempo Real

| Elemento | Descripción |
| :--- | :--- |
| **Fuente** | Usuarios concurrentes |
| **Estímulo** | Envío simultáneo de mensajes |
| **Entorno** | Alta actividad |
| **Artefacto** | Chat Service |
| **Respuesta** | El sistema distribuye conexiones WebSocket eficientemente |
| **Medida de Respuesta** | Latencia menor a 500 ms |

###### Justificación Técnica

La comunicación en tiempo real se soporta mediante:
- WebSockets persistentes,
- almacenamiento NoSQL,
- balanceo de conexiones,
- procesamiento asíncrono.

Esto garantiza una experiencia fluida en la interacción cliente-consultor.

---

### D. ESCALABILIDAD (Scalability)

FinTeka debe soportar crecimiento continuo de:
- usuarios,
- consultores,
- reservas,
- mensajes,
- transacciones financieras.

La arquitectura debe escalar sin rediseñar el sistema completo.

---

##### Escenario D1 — Incremento Masivo de Usuarios

| Elemento | Descripción |
| :--- | :--- |
| **Fuente** | Campaña comercial o expansión del negocio |
| **Estímulo** | Incremento abrupto de usuarios concurrentes |
| **Entorno** | Alta demanda |
| **Artefacto** | Microservicios |
| **Respuesta** | Se crean nuevas instancias automáticamente |
| **Medida de Respuesta** | SLA superior al 95% |

###### Justificación Técnica

La arquitectura desacoplada permite:
- escalabilidad horizontal,
- autoescalado dinámico,
- distribución de carga,
- aislamiento funcional entre servicios.

Cada microservicio puede crecer independientemente según la demanda.

---

### E. INTEGRABILIDAD (Integrability)

FinTeka depende de múltiples servicios externos:
- pasarelas de pago,
- servicios cloud,
- APIs de autenticación,
- notificaciones.

La arquitectura debe garantizar integraciones resilientes y desacopladas.

---

##### Escenario E1 — Falla Temporal de Pasarela de Pago

| Elemento | Descripción |
| :--- | :--- |
| **Fuente** | Servicio externo |
| **Estímulo** | Timeout o indisponibilidad |
| **Entorno** | Pago en proceso |
| **Artefacto** | Payment Integration Service |
| **Respuesta** | El sistema activa Retry y Circuit Breaker |
| **Medida de Respuesta** | No pérdida de consistencia transaccional |

###### Justificación Técnica

Para reducir el impacto de fallos externos:
- se implementan Circuit Breakers,
- mecanismos Retry,
- colas asíncronas,
- timeouts controlados.

Esto evita propagar fallos hacia el núcleo del sistema.

---

### F. AUDITABILIDAD (Auditability)

La auditabilidad permite garantizar:
- trazabilidad,
- monitoreo,
- control de operaciones,
- análisis de incidentes,
- cumplimiento de seguridad.

---

##### Escenario F1 — Registro de Eventos Críticos

| Elemento | Descripción |
| :--- | :--- |
| **Fuente** | Usuario autenticado |
| **Estímulo** | Login, pago o modificación sensible |
| **Entorno** | Operación normal |
| **Artefacto** | User Activity Logs |
| **Respuesta** | El sistema registra el evento de forma inmutable |
| **Medida de Respuesta** | Persistencia menor a 2 segundos |

###### Justificación Técnica

Los logs de auditoría:
- se almacenan en NoSQL,
- están desacoplados del núcleo transaccional,
- soportan análisis posteriores,
- mejoran la observabilidad distribuida.

---

### 4.1.11 Constraints

Las restricciones arquitectónicas representan limitaciones técnicas, operacionales y de negocio que condicionan el diseño del ecosistema FinTeka. Estas restricciones aseguran que la solución permanezca:
- viable,
- escalable,
- segura,
- mantenible,
- alineada con los objetivos estratégicos de Nova Asesors.

---

#### Justificación Técnica General

Las restricciones definidas responden directamente a:
- la naturaleza financiera del sistema,
- la necesidad de escalabilidad futura,
- los requerimientos de alta disponibilidad,
- la integración con terceros,
- la protección de información sensible.

Estas limitaciones establecen lineamientos obligatorios para la implementación de la solución tecnológica.

---

### A. Restricciones Tecnológicas

#### Arquitectura Basada en Microservicios

La solución debe implementarse obligatoriamente mediante microservicios desacoplados.

##### Implicancias
- Cada dominio funcional debe operar independientemente.
- Los servicios deben desplegarse por separado.
- La comunicación debe realizarse mediante APIs o eventos.

##### Justificación Técnica

Esto permite:
- escalabilidad independiente,
- despliegues aislados,
- resiliencia,
- evolución modular del sistema.

---

#### Persistencia Políglota

La plataforma debe utilizar:
- SQL para operaciones ACID,
- NoSQL para mensajería y auditoría.

##### Restricción

No se permite centralizar toda la información en un único motor de base de datos.

##### Justificación Técnica

Cada tecnología responde mejor a necesidades específicas:
- consistencia transaccional,
- alta concurrencia,
- almacenamiento flexible,
- velocidad de escritura.

---

#### Comunicación Obligatoria Mediante APIs

Los microservicios:
- no pueden acceder directamente a bases de datos ajenas,
- deben comunicarse únicamente mediante APIs y eventos.

##### Justificación Técnica

Esto reduce:
- acoplamiento,
- dependencias rígidas,
- riesgos de seguridad.

---

### B. Restricciones Operacionales

#### Alta Disponibilidad Obligatoria

La plataforma debe mantenerse operativa incluso ante:
- fallos de infraestructura,
- sobrecarga,
- errores parciales.

##### Requerimientos
- Multi-AZ,
- replicación síncrona,
- failover automático.

---

#### Compatibilidad Multiplataforma

La solución debe funcionar correctamente en:
- navegadores modernos,
- dispositivos móviles,
- tablets.

##### Justificación Técnica

La experiencia móvil representa uno de los objetivos principales del proyecto.

---

### C. Restricciones de Seguridad

#### Protección de Información Sensible

Toda información crítica debe:
- transmitirse cifrada,
- almacenarse de forma segura,
- validarse mediante autenticación robusta.

---

#### Control de Acceso Basado en Roles

La plataforma debe implementar RBAC para:
- Clientes,
- Consultores,
- Administradores.

No se permite acceso libre a operaciones críticas.

---

### D. Restricciones de Negocio

#### Integración con Pasarelas de Pago

FinTeka debe integrarse con servicios externos para:
- procesamiento de pagos,
- cobro de comisiones,
- confirmación financiera.

---

#### Gestión Automática de Comisiones

El sistema debe calcular automáticamente:
- comisiones de Nova Asesors,
- montos netos,
- estados transaccionales.

---

#### Escalabilidad Comercial

La arquitectura debe soportar:
- crecimiento masivo de usuarios,
- nuevas categorías de asesoría,
- incorporación de nuevas funcionalidades,

sin rediseñar el núcleo del sistema.

---

### 4.1.12 Architectural Concerns

Las preocupaciones arquitectónicas (*Architectural Concerns*) representan los aspectos críticos que influyen directamente en las decisiones técnicas adoptadas para el diseño de FinTeka. Estas preocupaciones reflejan riesgos, desafíos y necesidades estratégicas que deben resolverse para garantizar:
- confiabilidad,
- seguridad,
- escalabilidad,
- rendimiento,
- mantenibilidad.

---

#### Justificación Técnica General

Debido a la naturaleza distribuida y financiera del ecosistema FinTeka, existen múltiples preocupaciones relacionadas con:
- consistencia transaccional,
- seguridad de la información,
- escalabilidad,
- dependencias externas,
- observabilidad,
- experiencia de usuario.

La arquitectura propuesta incorpora patrones, tácticas y estilos arquitectónicos destinados a mitigar dichos riesgos.

---

### A. Consistencia Transaccional Distribuida

Uno de los principales desafíos es garantizar consistencia entre:
- reservas,
- pagos,
- disponibilidad,
- confirmaciones.

#### Riesgos
- reservas duplicadas,
- pagos inconsistentes,
- estados inválidos.

#### Solución Arquitectónica

La plataforma implementa:
- patrón Saga,
- eventos compensatorios,
- control de estados,
- validación distribuida.

Esto permite mantener coherencia entre microservicios desacoplados.

---

### B. Seguridad Financiera

FinTeka administra:
- pagos,
- datos personales,
- información financiera,
- autenticación.

#### Riesgos
- robo de credenciales,
- accesos indebidos,
- manipulación de información.

#### Soluciones Implementadas
- OAuth2,
- JWT,
- RBAC,
- HTTPS/TLS,
- API Gateway.

---

### C. Rendimiento Bajo Alta Concurrencia

La plataforma debe responder eficientemente incluso bajo:
- miles de usuarios concurrentes,
- mensajería simultánea,
- operaciones financieras intensivas.

#### Riesgos
- latencia elevada,
- saturación SQL,
- cuellos de botella.

#### Estrategias Arquitectónicas
- Redis Cache,
- balanceadores de carga,
- WebSockets,
- persistencia NoSQL,
- autoescalado.

---

### D. Complejidad Operacional de Microservicios

La arquitectura distribuida introduce desafíos relacionados con:
- monitoreo,
- trazabilidad,
- coordinación,
- debugging distribuido.

#### Necesidades Técnicas
- centralización de logs,
- observabilidad distribuida,
- tracing,
- monitoreo continuo.

---

### E. Dependencia de Servicios Externos

FinTeka depende de:
- pasarelas de pago,
- APIs externas,
- servicios cloud.

#### Riesgos
- latencia externa,
- caídas de proveedores,
- timeouts.

#### Mitigación
- Circuit Breakers,
- Retry,
- timeout controlado,
- integración desacoplada.

---

### F. Evolución y Mantenibilidad

La plataforma debe evolucionar continuamente para soportar:
- nuevos módulos,
- nuevas reglas de negocio,
- nuevas integraciones.

#### Preocupación Principal

Evitar dependencias rígidas entre componentes.

#### Estrategias
- arquitectura desacoplada,
- APIs versionadas,
- separación por dominios,
- despliegues independientes.

---

### G. Observabilidad y Monitoreo

La naturaleza distribuida del sistema requiere:
- monitoreo centralizado,
- métricas en tiempo real,
- detección temprana de fallos.

#### Implementación
- logs centralizados,
- métricas de rendimiento,
- distributed tracing,
- alertas automatizadas.

---

### H. Experiencia de Usuario en Tiempo Real

El éxito de FinTeka depende de ofrecer:
- baja latencia,
- fluidez,
- comunicación instantánea.

#### Riesgos
- retrasos en mensajes,
- lentitud de consultas,
- saturación de conexiones.

#### Soluciones
- WebSockets,
- Redis,
- balanceadores,
- caché distribuida.

---

### I. Gestión de Datos Híbridos

La coexistencia entre SQL y NoSQL introduce desafíos relacionados con:
- sincronización,
- consistencia,
- integridad.

#### Estrategias
- separación por dominios,
- eventos asíncronos,
- APIs especializadas,
- validaciones transaccionales.

---

### J. Continuidad Operacional y Recuperación

La plataforma debe recuperarse rápidamente ante:
- fallos críticos,
- errores cloud,
- interrupciones parciales.

#### Implementaciones
- Multi-AZ,
- replicación síncrona,
- failover automático,
- backups continuos.

Esto garantiza continuidad operacional y resiliencia empresarial para Nova Asesors.

## 4.3 ADD Iterations

### 4.2.X Iteration N: <Iteration Name>

#### 4.2.X.1 Architectural Design Backlog N  
#### 4.2.X.2 Establish Iteration Goal by Selecting Drivers  
#### 4.2.X.3 Choose One or More Elements of the System to Refine  
#### 4.2.X.4 Choose One or More Design Concepts that Satisfy the Selected Drivers  
#### 4.2.X.5 Instantiate Architectural Elements, Allocate Responsibilities, and Define Interfaces  
#### 4.2.X.6 Sketch Views (C4 & UML) and Record Design Decisions  
#### 4.2.X.7 Analysis of Current Design and Review Iteration Goal (Kanban Board) (Progress 2)
