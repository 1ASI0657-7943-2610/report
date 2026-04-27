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
### 4.1.11 Constraints  
### 4.1.12 Architectural Concerns  

## 4.3 ADD Iterations

### 4.2.X Iteration N: <Iteration Name>

#### 4.2.X.1 Architectural Design Backlog N  
#### 4.2.X.2 Establish Iteration Goal by Selecting Drivers  
#### 4.2.X.3 Choose One or More Elements of the System to Refine  
#### 4.2.X.4 Choose One or More Design Concepts that Satisfy the Selected Drivers  
#### 4.2.X.5 Instantiate Architectural Elements, Allocate Responsibilities, and Define Interfaces  
#### 4.2.X.6 Sketch Views (C4 & UML) and Record Design Decisions  
#### 4.2.X.7 Analysis of Current Design and Review Iteration Goal (Kanban Board) (Progress 2)
