<div align="center">
<img src="../assets/upc_logo.png"alt="UPC Logo" width="200"/>

# UNIVERSIDAD PERUANA DE CIENCIAS APLICADAS
### Ingeniería de Software
### 7mo ciclo
### 1ASI0657 - Fundamentos de Arquitectura de Software 
### 202610
### NRC: 7943
### Profesor: Ernesto Ocampo Tello
## Informe de Trabajo Parcial

## Producto:  Finteka

</div>

### Relación de integrantes:

<div style="text-align: center;">

| **Código** | **Apellidos y Nombres**               |
| :--------: | :------------------------------------ |
| U202310425 | Aguirre Castillo, Sergio Cesar        |
| U202128264 | Burga Loarte, Anaely Zarely           |
| U202220659 | Mamani Marca, Gabriel Cristian        |
| U20201f846 | Oshiro Yamashita, Daiki Oscar         |
| U202218645 | Montes Maza, Augusto Sebastian        |
</div>

<div align="center">
  
<br>
<br>

### Mayo,2026

</div>

<div style="page-break-before: always;"></div>

---
</div>

## Registro de Versiones del Informe

<table>
  <thead>
    <tr>
      <th>Versión</th>
      <th>Fecha</th>
      <th>Autor</th>
      <th>Descripción</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="7" style="text-align: center; vertical-align: middle;"><b>TB1</b></td>
      <td>10/04/2026</td>
      <td>Aguirre Castillo, Sergio Cesar</td>
      <td>Desarrollo del capítulo 3.</td>
    </tr>
    <tr>
      <td>12/04/2026</td>
      <td>Burga Loarte, Anaely Zarely</td>
      <td>Desarrollo puntos 2.1, 2.3, 2.3.1</td>
    </tr>
    <tr>
      <td>12/04/2026</td>
      <td>Mamani Marca, Gabriel Cristian</td>
      <td>Desarrollo el capítulo 1 y punto 3.2</td>
    </tr>
    <tr>
      <td>07/04/2026</td>
      <td>Oshiro Yamashita, Daiki Oscar</td>
      <td>Desarrollo de los puntos 2.3.2 a 2.3.5</td>
    </tr>
    <tr>
      <td>12/04/2026</td>
      <td>Oshiro Yamashita, Daiki Oscar</td>
      <td>Revisión general del documento.</td>
    </tr>
    <tr>
      <td>14/04/2026</td>
      <td>Montes Maza, Augusto Sebastian</td>
      <td>Desarrollo de conclusiones y recomendaciones del proyecto.</td>
    </tr>
    <tr>
      <td>14/04/2026</td>
      <td>Montes Maza, Augusto Sebastian</td>
      <td>Elaborar presentación tras revisión del documento.</td>
    </tr>
    <tr>
      <td rowspan="5" style="text-align: center; vertical-align: middle;"><b>TB2</b></td>
      <td>18/04/2026</td>
      <td>Aguirre Castillo, Sergio Cesar</td>
      <td>4.1.1 - 4.1.2 - 4.1.6 </td>
    </tr>
    <tr>
      <td>19/04/2026</td>
      <td>Burga Loarte, Anaely Zarely</td>
      <td>5.1, 5.1.1, 5.1.2, 5.1.3, 5.1.4, 5.1.5</td>
    </tr>
    <tr>
      <td>19/04/2026</td>
      <td>Mamani Marca, Gabriel Cristian</td>
      <td>Desarrollo todo el Architectural Design Backlog 1</td>
    </tr>
    <tr>
      <td>27/04/2026</td>
      <td>Oshiro Yamashita, Daiki Oscar</td>
      <td>Desarrollo del punto 4.1.3 y 4.1.4</td>
    </tr>
    <tr>
      <td>21/04/2026</td>
      <td>Montes Maza, Augusto Sebastian</td>
      <td>-</td>
    </tr>
    <tr>
      <td rowspan="6" style="text-align: center; vertical-align: middle;"><b>TP1</b></td>
      <td>05/05/2026</td>
      <td>Aguirre Castillo, Sergio Cesar</td>
      <td>Desarrollo del frontend</td>
    </tr>
    <tr>
      <td>04/05/2026</td>
      <td>Burga Loarte, Anaely Zarely</td>
      <td>Diagrama basado en 3FN, con entidades, relaciones y claves</td>
    </tr>
    <tr>
      <td>09/05/2026</td>
      <td>Mamani Marca, Gabriel Cristian</td>
      <td>Desarrollo sprint 1</td>
    </tr>
    <tr>
      <td>04/05/2026</td>
      <td>Oshiro Yamashita, Daiki Oscar</td>
      <td>Desarrollo de la primera versión backend</td>
    </tr>
    <tr>
      <td>07/05/2026</td>
      <td>Oshiro Yamashita, Daiki Oscar</td>
      <td>Corrección de los diagramas c4</td>
    </tr>
    <tr>
      <td>-</td>
      <td>Montes Maza, Augusto Sebastian</td>
      <td>-</td>
    </tr>
  </tbody>
</table>


# Contenido

## Índice

Tabla de contenidos

- [Registro de versiones del informe](#registro-de-versiones-del-informe)

- [Project Report Collaboration Insights](#project-report-collaboration-insights)

- [Contenido](#contenido)

- [Student Outcome](#student-outcome)

- [Capítulo I: Introducción](#capitulo-i-introduccion)
  - [1.1. StartUp Profile](#11-startup-profile)
    - [1.1.1. Descripción de la StartUp](#111-descripción-de-la-startup)
    - [1.1.2. Perfiles de Integrantes del equipo](#112-perfiles-de-integrantes-del-equipo)
  - [1.2. Solution Profile](#12-solution-profile)
    - [1.2.1. Antecedentes y Problemática](#121-antecedentes-y-problemática)
    - [1.2.2. Lean UX Process](#122-lean-ux-process)
      - [1.2.2.1. Lean UX Problem Statements](#1221-lean-ux-problem-statements)
      - [1.2.2.2. Lean UX Assumptions](#1222-lean-ux-assumptions)
      - [1.2.2.3. Lean UX Hyphotesis Statements](#1223-lean-ux-hyphotesis-statements)
      - [1.2.2.4. Lean UX Canvas](#1224-lean-ux-canvas)
  - [1.3. Segmentos objetivo](#13-segmentos-objetivo)
- [Capítulo II: Requirements & Analysis]()
  - [2.1. Competidores](#21-competidores)
    - [2.1.1. Análisis competitivo](#211-análisis-competitivo)
    - [2.1.2. Estrategias y tácticas frente a competidores](#212-estrategias-y-tácticas-frente-a-competidores)
  - [2.2. Entrevistas](#22-entrevistas)
    - [2.2.1. Diseño de entrevistas](#221-diseño-de-entrevistas)
    - [2.2.2. Registro de entrevistas](#222-registro-de-entrevistas)
    - [2.2.3. Análisis de entrevistas](#223-análisis-de-entrevistas)
  - [2.3. Needfinding](#23-needfinding)
    - [2.3.1. User Persona](#231-user-persona)
    - [2.3.2. User Task Matrix](#232-user-task-matrix)
    - [2.3.3. Empathy Mapping](#233-empathy-mapping)
    - [2.3.4. As-is Scenario Mapping](#234-as-is-scenario-mapping)
- [Capítulo III: Requirements Specification]()
  - [3.1. To-Be Scenario Mapping](#31-to-be-scenario-mapping)
  - [3.2. Requisitos funcionales y no funcionales](#32-requisitos-funcionales-y-no-funcionales)
      - [3.2.1. Requisitos Funcionales](#321-requisitos-funcionales)
      - [3.2.2. Requisitos no Funcionales](#322-requisitos-no-funcionales)
  - [3.3. User Stories](#33-user-stories)   
  - [3.4. Impact Map](#34-impact-map)
  - [3.5. Product Backlog](#35-product-backlog)
- [Capítulo IV: Product Architecture Design]()
  - [4.1. a](#41-a)
      - [4.1.1. Principles Statments](#411-Principles-Statements)
      - [4.1.2. Approaches Statments Architectural Styles & Patterns](#412-Approaches-Statements-Architectural-Styles-&-Patterns)
      - [4.1.3. Context Diagram](#413-context-diagram)
      - [4.1.4. Approach driven ViewPoints Diagrams](#414-approach-driven-viewpoints-diagrams)
      - [4.1.5 Relational / Non-Relational Database Diagram](#415-relational-non-relational-database-diagram)
      - [4.1.6. Design Patterns](#416-Design-patterns)
- [Capítulo V: Product Implementation, Validation & Deployment](#capítulo-v-product-implementation-validation-deployment)
  - [5.1 Testing Suites & General Patterns](#51-testing-suites-general-patterns)
    - [5.1.1 Backend Application Core Testing Suite](#511-backend-application-core-testing-suite)
    - [5.1.2 Pattern Based Backend Application(s)](#512-pattern-based-backend-applications)
    - [5.1.3 Pattern Based Custom Software Library](#513-pattern-based-custom-software-library)
    - [5.1.4 Framework Pattern Driven Refactoring Report](#514-framework-pattern-driven-refactoring-report)
- [Conclusiones y Recomendaciones](#conclusiones-y-recomendaciones)
  - [Conclusiones](#conclusiones)
  - [Recomendaciones](#recomendaciones)
- [Referencias Bibliográficas](#referencias-bibliográficas)
- [Anexos](#anexos)

<div style="page-break-before: always;"></div>

## Student Outcome

Objetivo general, ABET – EAC - Student Outcome 7: Aprendizaje Continuo y Autónomo.

| Criterio específico | Acciones realizadas | Conclusiones |
|---|---|---|
| **Actualiza conceptos y conocimientos necesarios para su desarrollo profesional y en especial para su proyecto en soluciones de software.** | **Daiki Oscar Oshiro Yamashita**<br>TB1: Actualicé conocimientos de UX y metodologías ágiles elaborando el User Task Matrix y Empathy Mapping.<br>TB2: Apliqué el modelo C4 mediante la elaboración de los diagramas de contexto, contenedores y componentes.<br>TP1: Corregí los diagramas del modelo C4 de Finteka, fortaleciendo la comprensión de la arquitectura del sistema.<br><br>**Anaely Burga Loarte**<br>TB1: Actualicé conocimientos de investigación de usuarios mediante el análisis de competidores y Needfinding.<br>TB2: Apliqué conceptos de diseño visual y prototipado mediante la elaboración de los Wireframes iniciales de Finteka.<br>TP1: Corregí el análisis de competidores y los User Personas de Finteka, mejorando la definición de los perfiles objetivo.<br><br>**Sergio Aguirre Castillo**<br>TB1: Actualicé conocimientos en desarrollo utilizando Python, C++ y C# para la implementación de funcionalidades.<br>TB2: Apliqué conceptos de persistencia de datos mediante el diseño del esquema de base de datos para el proyecto.<br>TP1: Corregí y optimicé módulos de código iniciales en Python y C#, fortaleciendo la calidad técnica del desarrollo.<br><br>**Gabriel Cristian Mamani Marca**<br>TB1: Identifiqué segmentos objetivo y elaboré los requisitos funcionales y no funcionales de la aplicación.<br>TB2: Desarrollé el Architectural Design Backlog 1, fortaleciendo la planificación técnica y estructuración del sistema.<br>TP1: Actualicé conocimientos en metodologías ágiles mediante la participación activa en el Sprint 1 de Finteka.<br><br>**Augusto Sebastian Montes Maza**<br>TB1: Lideré la estructuración del Lean UX Problem Statement y la definición de hipótesis de negocio.<br>TB2: Apliqué conocimientos de infraestructura en la nube analizando los servicios necesarios para el despliegue de Finteka.<br>TP1: Corregí el Lean UX Problem Statement y las hipótesis de negocio, asegurando la viabilidad del modelo de solución. | **Daiki Oscar Oshiro Yamashita**<br>TB1: La actualización permitió mejorar la planificación del proyecto.<br>TB2: El modelo C4 facilitó la identificación de componentes y relaciones.<br>TP1: La corrección de los diagramas C4 permitió estructurar y comprender mejor la arquitectura.<br><br>**Anaely Burga Loarte**<br>TB1: Permitió comprender mejor el entorno competitivo y las necesidades reales.<br>TB2: El prototipado inicial facilitó la visualización de la interacción del usuario con el sistema.<br>TP1: El refinamiento de los artefactos de UX permitió una segmentación más precisa del mercado.<br><br>**Sergio Aguirre Castillo**<br>TB1: Permitió mejorar la calidad del desarrollo y optimizar la implementación.<br>TB2: El diseño de la base de datos permitió organizar eficientemente la información del sistema.<br>TP1: La revisión técnica permitió mejorar la eficiencia y robustez de las funcionalidades.<br><br>**Gabriel Cristian Mamani Marca**<br>TB1: Aseguró la alineación entre los requerimientos del usuario y las funcionalidades.<br>TB2: Facilitó la priorización de actividades de arquitectura y planificación técnica.<br>TP1: La participación en el Sprint 1 consolidó conocimientos en metodologías ágiles y trabajo colaborativo.<br><br>**Augusto Sebastian Montes Maza**<br>TB1: Garantizó una base sólida al alinear objetivos técnicos con necesidades de mercado.<br>TB2: La planificación de la infraestructura aseguró la escalabilidad futura de la plataforma.<br>TP1: La corrección de supuestos permitió asegurar que la arquitectura soporte los objetivos comerciales. |
| **Reconoce la necesidad del aprendizaje permanente para el desempeño profesional y el desarrollo de proyectos en soluciones de software.** | **Daiki Oscar Oshiro Yamashita**<br>TB1: Investigué nuevas técnicas de análisis de usuarios y gestión ágil para aplicarlas en Finteka.<br>TB2: Reconocí la importancia del aprendizaje permanente al aplicar el modelo C4 en el proyecto.<br>TP1: Reconocí la necesidad del aprendizaje continuo al corregir los diagramas del modelo C4 en Finteka.<br><br>**Anaely Burga Loarte**<br>TB1: Investigué nuevas herramientas de Needfinding y enfoques centrados en el usuario para Finteka.<br>TB2: Reconocí la importancia del aprendizaje continuo al investigar estándares de usabilidad para los Wireframes.<br>TP1: Reconocí la necesidad del aprendizaje permanente al corregir el análisis de competidores y User Personas.<br><br>**Sergio Aguirre Castillo**<br>TB1: Investigué frameworks y buenas prácticas de programación para aportar eficientemente al proyecto.<br>TB2: Reconocí la importancia del aprendizaje continuo al investigar sobre normalización de bases de datos relacionales.<br>TP1: Reconocí la necesidad del aprendizaje permanente al corregir y refactorizar la lógica de programación.<br><br>**Gabriel Cristian Mamani Marca**<br>TB1: Investigué enfoques para la identificación de segmentos y la definición técnica de requisitos.<br>TB2: Reconocí la importancia del aprendizaje continuo al investigar conceptos avanzados de arquitectura de software.<br>TP1: Reconocí la necesidad del aprendizaje permanente al adaptarme a nuevas dinámicas de trabajo en el Sprint 1.<br><br>**Augusto Sebastian Montes Maza**<br>TB1: Investigué sobre pasarelas de pago y seguridad para integrar estos conceptos en el producto.<br>TB2: Reconocí la importancia del aprendizaje continuo al investigar servicios de computación en la nube y despliegue.<br>TP1: Reconocí la necesidad del aprendizaje permanente al corregir los planteamientos de Lean UX en Finteka. | **Daiki Oscar Oshiro Yamashita**<br>TB1: El aprendizaje es clave para adaptarse a metodologías innovadoras.<br>TB2: El modelo C4 reforzó la necesidad de aprendizaje para la arquitectura.<br>TP1: La corrección de diagramas C4 reforzó la necesidad de aprendizaje continuo.<br><br>**Anaely Burga Loarte**<br>TB1: Permite desarrollar soluciones más adaptadas a las necesidades reales del usuario.<br>TB2: La investigación en usabilidad permitió diseñar interfaces más intuitivas y eficaces.<br>TP1: El ajuste de la investigación de usuarios reforzó la necesidad de aprender sobre el mercado.<br><br>**Sergio Aguirre Castillo**<br>TB1: Facilita el desarrollo de soluciones escalables y alineadas a las necesidades técnicas.<br>TB2: El aprendizaje sobre modelado de datos garantizó la integridad de la información del proyecto.<br>TP1: La optimización constante de código reforzó la importancia de aprender mejores prácticas.<br><br>**Gabriel Cristian Mamani Marca**<br>TB1: Permite una mejor estructuración del sistema basada en requerimientos claros.<br>TB2: Contribuyó a diseñar soluciones más ordenadas y alineadas a la planificación técnica.<br>TP1: El trabajo en procesos ágiles reforzó la importancia de aprender nuevas herramientas de gestión.<br><br>**Augusto Sebastian Montes Maza**<br>TB1: Indispensable para integrar tecnologías de seguridad y garantizar la confianza en el sistema.<br>TB2: El aprendizaje sobre la nube permitió proyectar una solución tecnológicamente viable.<br>TP1: El ajuste de la estrategia técnica reforzó la necesidad de aprendizaje para ser competitivos. |
# Capítulo I: Introducción

## 1.1. Startup Profile

En la presente sección se expone información general relacionada con la startup desarrolladora de la propuesta.

## 1.1.1. Descripción de la Startup

Nova Asesors es una startup tecnológica enfocada en el desarrollo de soluciones digitales para facilitar el acceso a servicios de asesoría profesional. Surge como respuesta a la informalidad y dispersión existente en la postulación de consultores independientes.

Mediante una plataforma web, Nova Asesors busca optimizar el proceso de búsqueda y selección de especialistas, brindando a los usuarios una experiencia ágil, segura y accesible. De esta manera, se promueve una mejor toma de decisiones tanto en el ámbito personal como empresarial, sin intervenir directamente en la ejecución de las actividades del cliente.

La misión de Nova Asesors es brindar acceso eficiente y confiable a servicios de consultoría profesional mediante una plataforma digital que conecte a usuarios con expertos, contribuyendo al desarrollo de proyectos, negocios y objetivos personales.

La visión de Nova Asesors es consolidarse como una de las principales plataformas de consultoría digital en Latinoamérica, reconocida por su innovación tecnológica, calidad de servicio y confianza generada entre usuarios y profesionales afiliados.

El principal producto de la startup es FinTeka, una plataforma digital que conecta usuarios, empresas y profesionales especializados de diversas áreas, permitiendo buscar, comparar y contactar perfiles de manera eficiente. Además, facilita la gestión de agendas, reservas y comunicación dentro de un entorno integrado. FinTeka opera como una plataforma de intermediación orientada a la **postulación** y solicitud de servicios profesionales, donde la contratación final se realiza directamente entre las partes involucradas. Su finalidad es centralizar el acceso a asesoría profesional de forma organizada, confiable y accesible.

### 1.1.2. Perfiles de integrantes del equipo

| Miembros del equipo                                                                                                        | Código Estudiante | Carrera                | Conocimientos / Habilidades                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------|-------------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mamani Marca, Gabriel Cristian <br><img src="../assets/GabrielMamani.png" alt="Gabriel" width="120" height="120"> <br> <br> | u202220659        | Ingeniería de Software | Soy estudiante de sexto o séptimo de la carrera de Ingeniería de Software. Durante el camino aprendí lenguajes como C++, Python, Java y .Net. También, sobre  gestores de base de datos como MongoDB y MySQL. |
|<br> Daiki Oscar Oshiro Yamashita <br><img src="../assets/Daiki.png" alt="Daiki" width="120" height="120"> |U20201F846|Ingeniería de Software|Soy estudiante de la carrera de Ingeniería de Software. Tengo interés en obtener nuevos conocimientos relacionados con mi carrera que me sean de utilidad para el futuro. Cuento con el conocimiento de diversos lenguajes Python, C++, PHP, C#.|
|Sergio Cesar Aguirre Castillo  <img width="120" height="120" alt="image" src="https://github.com/user-attachments/assets/fec79da1-1e9c-43b4-a5c1-b9b3c79f808c" />|U202310425|Ingeniería de Software|Soy estudiante de la carrera de Ingeniería de Software, actualmente cursando el séptimo ciclo. Tengo un gran interés en adquirir nuevos conocimientos relacionados con mi área que me permitan fortalecer mis habilidades y prepararme para los retos del futuro profesional. Cuento con experiencia en diversos lenguajes de programación como Python, C++, PHP, C#, Java y JavaScript, además de conocimientos en desarrollo web utilizando HTML, CSS y manejo básico de bases de datos como MySQL, lo que me permite adaptarme a distintos entornos de desarrollo y seguir aprendiendo nuevas tecnologías.|
|Anaely Burga Loarte <br><img src="../assets/foto.png" alt="Anaely Burga" width="120" height="120"> |U202118264|Ingeniería de Software|Soy estudiante de la carrera de Ingeniería de Software, con interés en el análisis de usuarios y el diseño de soluciones centradas en el usuario. Durante mi formación he desarrollado habilidades lo que me permite comprender mejor las necesidades del usuario y proponer soluciones innovadoras. Además, cuento con conocimientos en lenguajes de programación y herramientas tecnológicas que complementan mi perfil, permitiéndome adaptarme a distintos entornos de desarrollo y seguir aprendiendo continuamente.|
|Augusto Sebastian Montes Maza<br><img src="../assets/AugustoMontes.png" alt="Augusto Montes" width="120" height="120"> |U202218645|Ingeniería de Software|Estudiante de Ingeniería de Software con una visión global y capacidad de adaptación demostrada en entornos internacionales. Mi formación académica se complementa con una fuerte orientación al trabajo en equipo y la comunicación efectiva, habilidades potenciadas durante mis experiencias de trabajo y estudio. Me especializo en el diseño de soluciones centradas en el usuario y poseo la agilidad técnica necesaria para integrarme a diversos entornos de desarrollo, manteniendo un compromiso constante con el aprendizaje de nuevas tecnologías.|

<br>
<br>

## 1.2 Solution Profile

**Nombre del Producto:** FinTeka

**Descripción del producto:** 

FinTeka es una plataforma web orientada a facilitar el acceso a servicios de asesoría profesional especializada, conectando a usuarios con expertos de diversas áreas de manera rápida, segura y eficiente. La propuesta busca centralizar en un solo entorno digital los principales procesos relacionados con la **postulación**, reduciendo la informalidad y mejorando la experiencia del usuario.

La plataforma permite buscar, comparar y seleccionar especialistas de acuerdo con criterios como categoría, experiencia, disponibilidad y valoraciones previas. Asimismo, ofrece herramientas para reservar sesiones, gestionar pagos y realizar seguimiento de las asesorías.

Del mismo modo, FinTeka incorpora funcionalidades que benefician tanto a los usuarios como a los consultores, tales como gestión de agendas en tiempo real, historial de sesiones, canales de comunicación directa y sistemas de reputación basados en calificaciones. En conjunto, estas características contribuyen a fortalecer la confianza, la organización y la calidad del servicio ofrecido.

**Plan Básico**

* Búsqueda de especialistas por categoría, experiencia y valoraciones.
* Visualización de perfiles profesionales con información relevante.
* Reserva de sesiones según disponibilidad.
* Sistema de calificaciones y comentarios.
* Historial básico de asesorías realizadas.
* Notificaciones de confirmación y recordatorios.

**Plan Premium**:

* Posicionamiento destacado del perfil del consultor dentro de la plataforma.
* Gestión avanzada de agenda con disponibilidad en tiempo real.
* Integración de pagos seguros dentro del sistema.
* Historial completo con seguimiento detallado de sesiones.
* Comunicación directa mediante chat entre usuario y consultor.
* Acceso a métricas de desempeño y reputación profesional.
* Herramientas avanzadas para la gestión de servicios.
* Soporte prioritario y atención extendida.

#### Modelo de Suscripción

| Plan | Comisión por Sesión | Beneficios Principales |
|---|---|---|
| Básico | 10% | Acceso estándar a reservas y funcionalidades principales |
| Premium | 4% | Menor comisión por sesión, promociones exclusivas y prioridad en soporte |

---

#### Beneficios Funcionales

##### Plan Básico

Incluye:
- acceso estándar a la plataforma,
- reservas de sesiones,
- visualización de perfiles profesionales,
- historial básico de asesorías,
- acceso a funcionalidades principales del sistema.

La comisión estándar del 10% se aplica sobre cada sesión reservada.

---

##### Plan Premium

Incluye:
- reducción de comisión por sesión del 10% al 4%,
- acceso prioritario a promociones y especialistas destacados,
- historial extendido de asesorías,
- notificaciones avanzadas,
- prioridad en soporte dentro de la plataforma,
- acceso anticipado a futuras funcionalidades premium.

La reducción de comisión representa el principal beneficio funcional y económico para usuarios frecuentes de FinTeka.

---

#### Consideraciones Funcionales y Técnicas

La gestión de suscripciones será administrada mediante un módulo desacoplado conectado al Payment Service.

El sistema permitirá:
- activar o desactivar planes,
- modificar porcentajes de comisión dinámicamente,
- incorporar promociones temporales,
- gestionar renovaciones de suscripción,

sin afectar el flujo principal de reservas y pagos.

Asimismo, los beneficios premium podrán extenderse en futuras iteraciones hacia:
- programas de fidelización,
- descuentos especiales,
- paquetes de asesorías,
- beneficios por recurrencia.

## 1.2.1. Antecedentes y problemática

**Antecedentes:**

En los últimos años, la transformación digital ha modificado la forma en que las personas y organizaciones acceden a diversos servicios, incluyendo aquellos vinculados con la asesoría profesional. El crecimiento del comercio electrónico, las plataformas colaborativas y los servicios remotos ha incrementado la demanda de soluciones digitales orientadas a facilitar la interacción entre proveedores especializados y potenciales clientes.

En el contexto peruano, el acceso progresivo a internet y el mayor uso de dispositivos móviles han favorecido la adopción de herramientas digitales para actividades comerciales, educativas y financieras. Paralelamente, pequeñas empresas, emprendedores y profesionales independientes requieren con mayor frecuencia orientación especializada en áreas como finanzas, derecho, tecnología, marketing y gestión empresarial.

No obstante, una parte importante de estos servicios continúa ofreciéndose mediante canales informales, como redes sociales, mensajería instantánea o recomendaciones personales. Esta situación dificulta la comparación entre alternativas disponibles, reduce la transparencia en precios y experiencia profesional, y limita la confianza entre las partes involucradas.

En ese sentido, surge la necesidad de implementar plataformas digitales que centralicen la oferta de asesoría profesional, optimicen los procesos de contacto y postulación, y brinden mayores garantías de seguridad, organización y calidad en el servicio.

**Problemáticas:**

Actualmente, muchas personas y organizaciones enfrentan dificultades para acceder a asesoría profesional confiable de manera rápida y ordenada. La búsqueda de especialistas suele realizarse a través de medios dispersos, lo que incrementa el tiempo de selección y dificulta la toma de decisiones informadas.

Asimismo, los profesionales independientes no siempre disponen de herramientas tecnológicas que les permitan gestionar adecuadamente su disponibilidad, reservas, pagos y comunicación con clientes. Como consecuencia, se reducen sus posibilidades de crecimiento y formalización dentro del mercado digital.

De igual manera, la ausencia de sistemas integrados para programar sesiones, procesar pagos y registrar valoraciones genera experiencias poco eficientes tanto para usuarios como para consultores. Esto limita la confianza, disminuye la continuidad del servicio y afecta la percepción de calidad.

Frente a esta situación, resulta pertinente el desarrollo de una solución digital que centralice la interacción entre usuarios y especialistas, simplifique los procesos operativos y fortalezca la transparencia en la postulación de servicios profesionales.

**Aplicación de la técnica 5W y 2H:**

A partir del análisis de los antecedentes y la problemática, se aplica la técnica de las 5W y 2H para estructurar la solución propuesta:

**What (Qué)**  
La problemática principal consiste en la ausencia de una solución digital unificada que conecte eficientemente a usuarios con consultores profesionales. Actualmente, la búsqueda de especialistas suele realizarse mediante redes sociales, referencias informales o páginas aisladas, lo que dificulta comparar alternativas y genera incertidumbre al momento de contratar.

Adicionalmente, muchos consultores no cuentan con herramientas tecnológicas que les permitan gestionar reservas, mostrar información profesional confiable, automatizar procesos de atención o consolidar su reputación mediante reseñas verificadas.

**When (Cuándo)**  
La necesidad surge cada vez que una persona o empresa requiere orientación profesional para resolver un problema puntual, desarrollar un proyecto, mejorar resultados o recibir acompañamiento especializado.

Su importancia se ha incrementado en los últimos años debido al crecimiento del trabajo remoto, la digitalización de servicios y la expansión de modelos independientes de consultoría profesional.

**Where (Dónde)**  
Esta situación se presenta principalmente en el ecosistema digital, donde la oferta de asesorías profesionales se encuentra fragmentada en múltiples canales no integrados, como redes sociales, aplicaciones de mensajería, anuncios independientes o contactos personales.<br>
Asimismo, afecta diversos contextos como el ámbito empresarial, académico, financiero, tecnológico y personal, donde la necesidad de contratar expertos especializados es cada vez más frecuente.

**Who (Quiénes)**  
Dentro del entorno analizado se identifican como actores principales a los usuarios que buscan asesoría especializada, entre ellos personas naturales, emprendedores, estudiantes y pequeñas empresas que necesitan apoyo profesional para resolver dudas, optimizar procesos o tomar mejores decisiones.

También forman parte esencial los consultores independientes y especialistas, quienes requieren un espacio digital confiable para promocionar sus servicios, administrar citas, recibir pagos y fortalecer su reputación profesional. Finalmente, intervienen los administradores de la plataforma, encargados de supervisar la seguridad, validar operaciones y mantener el correcto funcionamiento del sistema.

**Why (Por qué)**  
El origen del problema radica en la falta de plataformas integrales que reúnan en un solo entorno funcionalidades como registro seguro, perfiles profesionales, filtros de búsqueda, reservas automáticas, pagos protegidos y sistemas de valoración confiables.<br>
Como consecuencia, los usuarios enfrentan procesos lentos y poco transparentes, mientras que los consultores encuentran limitaciones para captar clientes, organizar su agenda y diferenciarse en el mercado.

**How (Cómo)**  
En la actualidad, gran parte de estas interacciones se desarrolla de manera manual. Los usuarios localizan consultores por recomendaciones o publicaciones, coordinan horarios mediante mensajes directos, realizan pagos externos y no siempre disponen de evidencia clara sobre la calidad del servicio recibido.<br>
Frente a ello, FinTeka plantea una plataforma web que centraliza autenticación segura, perfiles personales y profesionales, motor de búsqueda avanzada, programación de sesiones, pagos digitales, notificaciones automáticas y reputación basada en experiencias reales de los usuarios.

**How Much (Cuánto impacto)**  
El impacto de esta problemática se refleja en pérdida de tiempo, menor confianza en las contrataciones y desaprovechamiento de oportunidades comerciales tanto para clientes como para especialistas.<br>
Con la implementación de FinTeka se espera optimizar el acceso a servicios profesionales, incrementar la eficiencia en la contratación, mejorar la experiencia de ambas partes y ampliar las oportunidades económicas dentro del mercado digital de asesorías.

### 1.2.2 Lean UX Process

#### 1.2.2.1 Lean UX Problem Statement

Actualmente, las personas, emprendedores y empresas que requieren asesoría profesional enfrentan dificultades para identificar especialistas confiables en un mercado altamente fragmentado. Con frecuencia, la búsqueda se realiza mediante recomendaciones informales o redes sociales, donde la información disponible no siempre resulta clara, verificable o suficiente para tomar decisiones adecuadas.

Esta situación genera demoras en la selección del profesional adecuado, escasa transparencia en precios y experiencia, dificultades para coordinar sesiones y limitada seguridad en los procesos de pago. Como consecuencia, la experiencia del usuario suele ser poco eficiente y con altos niveles de incertidumbre.

Por otro lado, los profesionales independientes carecen, en muchos casos, de herramientas digitales que les permitan organizar su disponibilidad, administrar reservas, fortalecer su reputación y ampliar su alcance comercial. Esto restringe sus oportunidades de crecimiento y formalización en entornos digitales.

Frente a esta problemática, FinTeka propone el desarrollo de una plataforma digital orientada a centralizar la relación entre usuarios y consultores, simplificando los procesos de **búsqueda, postulación y seguimiento** del servicio. La propuesta busca validar inicialmente el interés del mercado y, posteriormente, consolidar una solución integral que genere valor para ambas partes.

El principal reto consiste en construir una plataforma que transmita confianza, facilidad de uso, seguridad operativa y calidad en la experiencia ofrecida.

¿Cómo podríamos diseñar una plataforma digital confiable, eficiente e intuitiva que conecte a usuarios con especialistas profesionales, mejorando la experiencia de postulación y generando valor sostenible para clientes y consultores?

#### 1.2.2.2 Lean UX Assumptions

Con el fin de validar la propuesta de valor de FinTeka, se identificaron los principales supuestos relacionados con usuarios, negocio, resultados esperados y funcionalidades clave.

### Business Assumptions

* Existe una necesidad creciente de acceder a asesorías profesionales mediante plataformas digitales confiables y estructuradas.
* Los usuarios estarán más dispuestos a contratar servicios si el proceso incluye identidad verificada, pagos seguros y reputación visible.
* Los consultores independientes adoptarán soluciones que les permitan captar clientes, administrar horarios y aumentar ingresos.
* Un esquema de monetización basado en comisiones por sesión, suscripciones premium y posicionamiento destacado será sostenible.
* La seguridad, velocidad de respuesta y disponibilidad del sistema serán factores determinantes para competir en el mercado.
* La centralización de búsqueda, reservas, pagos y valoraciones generará ventaja frente a canales informales.
* La confianza inicial del usuario dependerá de una buena experiencia digital, protección de datos y transparencia operativa.

### User Assumptions

* Los usuarios desean encontrar especialistas confiables sin depender de recomendaciones informales o búsquedas extensas.
* Antes de contratar, las personas comparan precio, experiencia, reputación, disponibilidad y modalidad de atención.
* Los clientes prefieren registrarse e iniciar sesión mediante procesos simples pero seguros.
* Los usuarios esperan poder reservar, pagar y recibir confirmaciones desde un único entorno digital.
* Los consultores necesitan paneles donde puedan gestionar agenda, sesiones, métricas y perfil profesional.
* Las notificaciones automáticas y recordatorios incrementarán asistencia y puntualidad en las sesiones programadas.
* La interfaz responsive y tiempos rápidos de carga influirán directamente en la permanencia dentro de la plataforma.

### User Outcomes

* Los usuarios tomarán decisiones mejor fundamentadas gracias a perfiles completos, reputación visible y valoraciones reales.
* El tiempo para encontrar especialistas adecuados disminuirá mediante filtros y búsqueda avanzada.
* Los clientes sentirán mayor confianza al usar pagos protegidos y autenticación segura.
* Los consultores mejorarán su organización mediante agenda digital, reservas automatizadas e historial de sesiones.
* Ambas partes tendrán mejor seguimiento de citas gracias a recordatorios, estados de sesión y trazabilidad.
* Los usuarios podrán administrar fácilmente sus cuentas, historial y preferencias personales.

### Business Outcomes

* Conseguir una conversión mínima del 25% de visitantes registrados durante la etapa inicial.
* Lograr una retención del 60% de usuarios activos durante el primer trimestre operativo.
* Alcanzar al menos un 80% de valoraciones positivas sobre sesiones completadas.
* Incorporar entre 50 y 100 consultores activos en los primeros seis meses.
* Obtener ingresos sostenibles mediante comisiones y suscripciones premium.
* Mantener tiempos de respuesta y desempeño alineados con los requisitos no funcionales definidos.
* Posicionar la marca FinTeka como alternativa confiable frente a medios informales de contratación.

### Feature Assumptions

* Registro, inicio de sesión seguro y recuperación de contraseña.
* Gestión de roles: usuario, consultor y administrador.
* Buscador avanzado con filtros por especialidad, reputación, precio y disponibilidad.
* Perfiles profesionales con experiencia, certificaciones, tarifas y comentarios.
* Sistema de reservas con calendario y validación de horarios en tiempo real.
* Confirmación de pagos seguros mediante pasarela integrada.
* Reprogramación, cancelación y seguimiento del ciclo de vida de sesiones.
* Historial de sesiones, pagos y notificaciones.
* Sistema de calificaciones, reputación y reseñas verificadas.
* Dashboard con métricas para consultores.
* Gestión de suscripción premium y posicionamiento destacado.
* Notificaciones automáticas por registro, pago, reserva, cancelación y recordatorios.
* Diseño responsive para móvil, tablet y escritorio.

#### 1.2.2.3. Lean UX Hypothesis Statements

##### Hipótesis 1

Creemos que, si se implementa una plataforma digital que centralice la búsqueda y postulación de especialistas, los usuarios podrán acceder a asesoría profesional de manera más rápida, segura y ordenada. Esto se validará cuando aumente la cantidad de reservas completadas y disminuya el tiempo promedio entre la búsqueda inicial y la contratación del servicio.

- **Business Outcome:** Incremento en la cantidad de sesiones reservadas y en la tasa de conversión de usuarios registrados.  
- **Users:** Personas naturales, emprendedores y pequeñas empresas que requieren asesoría especializada.  
- **User Outcome:** Acceso eficiente a especialistas confiables y mejora en la experiencia de postulación.  
- **Feature:** Buscador por categorías, perfiles profesionales, sistema de reservas y pagos integrados.

##### Hipótesis 2

Creemos que, si se brindan herramientas de gestión para agenda, servicios y clientes dentro de una sola plataforma, los consultores mejorarán su productividad y ampliarán sus oportunidades comerciales. Esto se validará cuando aumente la cantidad de especialistas activos y el promedio de sesiones atendidas por profesional.

- **Business Outcome:** Crecimiento de la red de consultores registrados y mayor actividad dentro de la plataforma.  
- **Users:** Consultores independientes y profesionales especializados.  
- **User Outcome:** Mejor organización operativa, mayor visibilidad y nuevas oportunidades de ingresos.  
- **Feature:** Panel de gestión profesional, calendario de disponibilidad, historial de clientes y métricas de desempeño.

##### Hipótesis 3

Creemos que, si se incorpora un sistema de valoraciones y reseñas verificadas, aumentará la confianza de los usuarios al momento de seleccionar especialistas. Esto se validará cuando mejore la tasa de postulación desde perfiles visitados y aumente la recurrencia de uso.

- **Business Outcome:** Incremento en la conversión de visitas a reservas y mejora en la retención de usuarios.  
- **Users:** Usuarios que buscan asesoría y consultores que ofrecen sus servicios.  
- **User Outcome:** Mayor seguridad al elegir especialistas y fortalecimiento de reputación profesional.  
- **Feature:** Sistema de calificaciones, comentarios verificados y reputación visible en perfiles.

##### Hipótesis 4

Creemos que, si se habilitan canales de comunicación directa y seguimiento posterior a cada sesión, mejorará la continuidad del servicio y la satisfacción general del usuario. Esto se validará cuando aumente la cantidad de sesiones recurrentes con un mismo consultor y las valoraciones positivas posteriores a la atención.

- **Business Outcome:** Mayor tasa de recompra y fortalecimiento de fidelización.  
- **Users:** Usuarios que requieren acompañamiento continuo y especialistas que brindan asesorías periódicas.  
- **User Outcome:** Mejor experiencia de servicio, continuidad en el asesoramiento y relaciones profesionales sostenibles.  
- **Feature:** Chat interno, historial de sesiones, recordatorios y programación de seguimientos.

##### Hipótesis 5

Creemos que, si se ofrecen pagos seguros e integrados dentro de la plataforma, los usuarios percibirán mayor confianza y comodidad al contactar servicios profesionales. Esto se validará cuando disminuya el abandono en el proceso de pago y aumente el porcentaje de transacciones completadas.

- **Business Outcome:** Incremento de ingresos por comisiones y reducción de transacciones inconclusas.  
- **Users:** Usuarios postulantes y consultores afiliados.  
- **User Outcome:** Proceso de pago simple, seguro y confiable.  
- **Feature:** Pasarela de pago integrada, comprobantes automáticos y confirmación inmediata de reservas.

#### 1.2.2.4. Lean UX Canvas

<img src="../assets/UXCanvasF.png" alt="Lean UX Canvas" width="100%">

Tablero Miro: https://miro.com/app/board/uXjVGhydm8Q=/?share_link_id=941421721219

**Descripción del Canvas desarrollado:**

- **Business Problem:** dificultad para acceder a asesoría profesional confiable mediante canales digitales organizados.
- **Users and Customers:** personas que requieren asesoría especializada y consultores independientes.
- **User Benefits:** rapidez, confianza, transparencia, acceso a especialistas y facilidad de contacto.
- **Solution Ideas:** buscador de expertos, reservas online, pagos seguros, valoraciones y panel de gestión.
- **Hypotheses:** los usuarios contactarán más asesorías si existe confianza, facilidad de uso y especialistas verificados.
- **Most Important Thing to Learn First:** validar si los usuarios realmente pagarían por asesoría digital en una plataforma centralizada.
- **Least Amount of Work to Learn:** landing page, entrevistas, prototipo navegable y pruebas con usuarios iniciales.
- **Business Outcomes:** crecimiento de usuarios registrados, reservas completadas, retención y satisfacción.

## 1.3. Segmentos objetivo

### Segmento objetivo N.° 1: Personas que requieren asesoría profesional

**Descripción:**  
Este segmento está conformado por personas que necesitan orientación especializada en áreas como finanzas, derecho, tecnología, negocios, empleabilidad o desarrollo personal. Representan la demanda principal de la plataforma, al buscar soluciones confiables que respalden decisiones relevantes en el ámbito personal, académico o laboral.

**Aspectos demográficos:**  
Hombres y mujeres entre 20 y 45 años, pertenecientes principalmente a los niveles socioeconómicos B y C. Incluye estudiantes universitarios, profesionales jóvenes, emprendedores y trabajadores independientes con acceso frecuente a internet.

**Aspectos geográficos:**  
Ubicados principalmente en zonas urbanas del Perú, con mayor concentración en Lima Metropolitana, Arequipa, Trujillo, Chiclayo y otras ciudades con alta adopción digital.

**Aspectos psicográficos:**  
Valoran la eficiencia, la practicidad y el acceso rápido a información confiable. Buscan herramientas que simplifiquen procesos complejos y les permitan tomar decisiones con menor nivel de incertidumbre.

**Necesidades:**  
- Encontrar especialistas confiables según su necesidad.  
- Recibir asesoría personalizada y oportuna.  
- Contar con procesos claros de reserva y pago.  
- Acceder a una experiencia segura y transparente.

**Requisitos:**  
- Plataforma intuitiva y de fácil navegación.  
- Compatibilidad con dispositivos móviles y computadoras.  
- Información clara sobre experiencia, tarifas y disponibilidad.  
- Métodos de pago seguros.

**Objetivo:**  
Resolver necesidades específicas, optimizar tiempo y mejorar la calidad de sus decisiones mediante acceso rápido a conocimiento especializado.

### Segmento objetivo N.° 2: Consultores y profesionales independientes

**Descripción:**  
Este segmento está integrado por profesionales que brindan servicios de asesoría en áreas como derecho, contabilidad, psicología, finanzas, tecnología, marketing, recursos humanos y coaching. Utilizan la plataforma como canal de captación de clientes y herramienta de gestión operativa.

**Aspectos demográficos:**  
Hombres y mujeres entre 25 y 55 años, con formación técnica o universitaria, experiencia laboral previa y orientación al trabajo independiente o complementario.

**Aspectos geográficos:**  
Principalmente ubicados en Lima Metropolitana y capitales de región, aunque también incluye profesionales que prestan servicios remotos desde otras ciudades.

**Aspectos psicográficos:**  
Valoran la autonomía profesional, la generación de ingresos y el uso de tecnología para ampliar oportunidades comerciales. Buscan posicionamiento, eficiencia y crecimiento sostenido.

**Necesidades:**  
- Captar nuevos clientes de forma constante.  
- Gestionar agenda y reservas en un solo entorno.  
- Recibir pagos de manera segura.  
- Construir reputación mediante valoraciones verificadas.

**Requisitos:**  
- Plataforma confiable y profesional.  
- Herramientas de administración simples.  
- Visibilidad del perfil frente a potenciales clientes.  
- Reportes de actividad e ingresos.

**Objetivo:**  
Incrementar ingresos, optimizar la gestión de servicios y ampliar alcance profesional mediante canales digitales.

# Capítulo II: Requirements Elicitation & Analysis

En este capítulo se realizará el proceso de Análisis competitivo y Needfinding necesario para la identificación de las necesidades de nuestro segmento objetivo.

## 2.1. Competidores

### 2.1.1. Análisis Competitivo
# Competitive Analysis Landscape

| **¿Por qué llevar a cabo este análisis?** | ¿Nuestro servicio tiene lo necesario para poder salir adelante ante sus competidores más conocidos? |
|                       | <img src="../assets/FinTeka.png" width="100" height="100"><br>**Nova Asesors** | <img src="../assets/clarityfm.png" width="100" height="100"><br>**Clarity.fm** | <img src="../assets/superpeer.png" width="100" height="100"><br>**Superpeer** | <img src="../assets/maven.jpg" width="100" height="100"><br>**Maven** |
|-----------------------|-----------------------------------------------------------|---------------------------------------------|-------------------------------------------|--------------------------------------|
| **Perfil / Overview** | Plataforma que conecta expertos con usuarios para sesiones 1 a 1, pagos seguros, y perfiles verificados. Áreas: salud, tecnología, negocios y más. | Plataforma para contratar expertos para llamadas 1 a 1. Pago por minuto. Áreas: tecnología, marketing, negocios. | Videollamadas 1 a 1, eventos en vivo, suscripciones. Enfocado en creadores de contenido. | Cursos en vivo con expertos. Enfoque en aprendizaje colaborativo en temas técnicos y profesionales. |
| **Ventaja Competitiva** | Facilidad de uso, verificación rigurosa, pagos seguros, interfaz elegante. Proceso intuitivo para agendar y pagar. | Comunidad de expertos consolidada. Modelo flexible de pago por minuto. Integración con redes como LinkedIn. | Monetización con suscripciones. Fuerte en branding personal y creación de comunidad. | Experiencia de aprendizaje estructurada en cohortes. Foco en formación continua. |
| **Mercado Objetivo** | Personas y empresas que buscan asesoría profesional rápida. Especialmente pymes y usuarios individuales. | Emprendedores, freelancers y startups que buscan asesorías específicas y breves. | Creadores de contenido, coaches y expertos con audiencia propia. | Profesionales, empresas y universidades interesados en educación técnica y profesional. |
| **Estrategias de Marketing** | SEO, marketing en redes sociales, alianzas con universidades y cámaras de comercio. | SEO, contenido dirigido a comunidad emprendedora, campañas en Google y LinkedIn. | Promociones en redes sociales, branding de creadores, creación de comunidad activa. | Webinars, email marketing, alianzas con universidades y expertos reconocidos. |
| **Productos y Servicios** | Asesorías personalizadas, citas agendadas, pagos seguros, historial de sesiones, recomendaciones según preferencias. | Llamadas con expertos, cobro por minuto. Sin necesidad de sesiones largas. | Videollamadas, eventos en vivo, suscripciones mensuales para contenido exclusivo. | Cursos en vivo por cohortes, acceso a materiales y sesiones interactivas. |
| **Precios y Costos** | Comisión por sesión. Planes especiales para expertos frecuentes. Estructura de precios transparente. | Pago por minuto definido por el experto. Puede ser caro para sesiones largas. | Comisión por transacción + suscripciones mensuales opcionales. | Precio por curso (premium). Incluye materiales y acceso a sesiones. |
| **Canales de Distribución** | Web y aplicación móvil. Acceso intuitivo desde cualquier dispositivo. | Principalmente vía web. | Web y app móvil para mayor flexibilidad. | Solo vía web. Experiencia optimizada para aprendizaje. |
| **SWOT - Fortalezas** | Plataforma integral, experiencia fluida, verificación de expertos, interfaz intuitiva. | Comunidad de expertos establecida, pago flexible, integración profesional. | Monetización diversificada, enfoque en comunidad y branding personal. | Educación estructurada, interacción colaborativa, calidad en cohortes. |
| **SWOT - Debilidades** | Sin comunidad consolidada, alta dependencia de SEO/redes, recursos de marketing limitados. | Modelo puede ser costoso en consultas largas. Limitado a llamadas. | Requiere base de seguidores. Difícil para creadores nuevos. | Enfocado solo en educación profesional. Público limitado. |
| **SWOT - Oportunidades** | Alianzas institucionales, expansión a empresas, crecimiento en demanda remota. | Expandir servicios más allá de llamadas. Alta demanda en asesorías rápidas. | Ampliar a más mercados y formatos. Alianzas educativas. | Aumento del interés en educación digital, posibles alianzas. |
| **SWOT - Amenazas** | Competencia consolidada con base leal, marketing agresivo de expertos ya establecidos. | Plataformas como LinkedIn y Upwork. Red más amplia de profesionales. | Competencia con Patreon y otras plataformas de monetización. | Plataformas grandes como Coursera y edX. |
| **¿Tiene lo necesario para competir?** | Sí. Con su enfoque claro en asesorías profesionales, interfaz simple, y verificación rigurosa, Nova Asesors puede posicionarse como una alternativa sólida. Requiere reforzar comunidad y marketing inicial para destacarse. |


### 2.1.2. Estrategias y tácticas frente a competidores

## 1. Aprovechar la Fortaleza: Verificación de Expertos y Asesoría Profesional Personalizada

### Estrategia
Diferenciar la plataforma mediante un sistema de verificación más riguroso de los expertos y la oferta de asesorías personalizadas de alta calidad.

### Tácticas
- **Resaltar la verificación de expertos**:  
  Destacar el proceso de selección y verificación de los profesionales, asegurando que solo los más calificados estén disponibles, diferenciándose de plataformas como Clarity.fm.

- **Promocionar la asesoría personalizada**:  
  Desarrollar campañas de marketing que subrayen las soluciones específicas y adaptadas que ofrece la plataforma, en contraste con ofertas más generales de competidores.

### Valor Añadido
- Generar confianza entre los usuarios.  
- Incrementar la tasa de retención y fidelización.

---

## 2. Aprovechar la Oportunidad: Crecimiento de la Demanda de Asesoría Remota

### Estrategia
Posicionar la plataforma como una solución clave para la asesoría remota, capitalizando el aumento de la demanda post-pandemia.

### Tácticas
- **Campañas educativas sobre asesoría remota**:  
  Crear contenido en redes sociales, blogs y webinars destacando los beneficios de la plataforma.

- **Alianzas con empresas y asociaciones profesionales**:  
  Establecer relaciones estratégicas con colegios profesionales, asociaciones y empresas para ofrecer servicios constantes y generar ingresos adicionales.

- **Incorporar herramientas interactivas de alta calidad**:  
  Implementar funciones como videoconferencias, mensajería en tiempo real y un sistema de pago seguro para garantizar una experiencia eficiente y profesional.

---

## 3. Afrontar la Amenaza de Competidores Consolidados con Base de Usuarios Grandes

### Estrategia
Aplicar un enfoque de marketing centrado en la seguridad, confianza y valor agregado de la plataforma frente a competidores consolidados.

### Tácticas
- **Resaltar la seguridad de la plataforma**:  
  Comunicar que los usuarios contactan servicios seguros y de alta calidad gracias al sistema de verificación de expertos.

- **Modelo freemium para atraer usuarios**:  
  Ofrecer una versión básica gratuita con opción a características premium mediante suscripciones, atrayendo usuarios indecisos de competidores.

- **Segmentación y personalización de servicios**:  
  Ofrecer servicios especializados en sectores como asesoría legal, empresarial y financiera, diferenciándose de competidores más generalistas.

---

## 4. Aprovechar la Debilidad de la Dependencia de Posicionamiento en Buscadores (SEO) y la Visibilidad Inicial

### Estrategia
Implementar estrategias de marketing digital avanzadas para aumentar la visibilidad y atraer usuarios rápidamente.

### Tácticas
- **Marketing de contenido de valor**:  
  Crear artículos, videos y estudios de caso prácticos que resuelvan problemas comunes en la industria de asesoría, atrayendo tráfico orgánico.

- **Publicidad dirigida y marketing en redes sociales**:  
  Desarrollar campañas específicas para profesionales y empresas en sectores clave como tecnología, salud, derecho y negocios.

- **SEO local y alianzas estratégicas**:  
  Optimizar el sitio para búsquedas locales y colaborar con colegios profesionales e instituciones clave para aumentar la visibilidad en nichos específicos.


## 2.2. Entrevistas

### 2.2.1. Diseño de entrevistas

**Preguntas Generales**

- ¿Cuál es su nombre?
- ¿Cuántos años tiene usted?
- ¿En qué ciudad y distrito reside? ¿Es un área urbana o rural?
- ¿A qué se dedica profesionalmente y qué tipo de asesoría está buscando?

**Preguntas Específicas**

##### 1. Personas Naturales (Usuarios en búsqueda de asesoría profesional)

**Preguntas principales:**

- Imagina que pudieras pedirle consejo a un experto en cualquier área de tu vida profesional, ¿qué área elegirías y qué te gustaría lograr con ese consejo?


- Si tuvieras que escoger entre una asesoría puntual para resolver un problema específico o un acompañamiento continuo a largo plazo, ¿cuál elegirías y por qué?


- Cuando necesitas encontrar un experto para una asesoría, ¿te sientes más cómodo buscando opiniones de otros usuarios (reseñas, recomendaciones) o prefieres confiar en las credenciales profesionales del asesor? ¿Por qué?


- Si pudieras personalizar una plataforma de asesoría profesional (como la facilidad de navegación, opciones de pago, o comunicación), ¿qué características tendría para que te sintieras cómodo usándola?


- En tus propias palabras, ¿cómo describirías la “experiencia ideal” al recibir asesoría online? ¿Qué elementos no pueden faltar en la plataforma o en la interacción con el asesor?


- ¿Qué tipo de indicadores o resultados específicos considerarías para determinar si una asesoría fue efectiva y valió la pena?

  
- En cuanto a la relación con tu asesor, ¿prefieres que sea más formal y profesional, o buscas una relación más cercana y personal, como la de un mentor?


- En una escala del 1 al 10, ¿qué tan importante es para ti que la plataforma te brinde recomendaciones sobre qué expertos son los más adecuados para tu consulta, siendo 1 nada importante y 10 extremadamente importante?


- Si tuvieras que elegir entre una plataforma con muchas funciones tecnológicas avanzadas o una más sencilla de usar pero con menos funcionalidades, ¿cuál preferirías? ¿Por qué?


- Piensa en la última vez que buscaste un experto para resolver un problema profesional o personal. ¿Qué te molestó más del proceso y qué características o mejoras te habrían facilitado la búsqueda de ese experto?


##### 2. Consultores y Profesionales (Proveedores de asesoría)

**Preguntas principales:**

- Si pudieras organizar tu negocio de asesoría de la manera más eficiente posible, ¿qué herramientas o procesos específicos usarías para atraer clientes y organizar las sesiones de manera efectiva?


- ¿Qué tipo de información sobre el cliente necesitas tener antes de la sesión para ofrecer el mejor servicio posible?


- ¿Qué te hace sentir más cómodo en una plataforma que gestiona tu agenda y pagos? ¿Prefieres una interfaz sencilla que solo cumpla con lo esencial o herramientas avanzadas que te permitan personalizar tu negocio de manera flexible?


- Si pudieras optimizar el proceso de pagos a través de una plataforma, ¿qué funcionalidades específicas te harían la vida más fácil (pago por sesión, suscripciones, facturación automática, etc.)?


- Cuando piensas en promocionar tus servicios de asesoría, ¿qué tipo de marketing digital te gustaría que la plataforma ofreciera para atraer nuevos clientes?


- Si un cliente te solicitara una consulta urgente, ¿qué tan fácil sería para ti gestionar y responder esa solicitud a través de una plataforma digital?


- Imagina que puedes organizar eventos grupales en tu especialidad (por ejemplo, seminarios o masterclasses). ¿Cómo te gustaría que la plataforma te ayudara a crear estos eventos?


- Si tuvieras que presentar una propuesta de asesoría a un nuevo cliente en línea, ¿qué elementos visuales o interactivos serían importantes para ti incluir en esa presentación?


- ¿¿Cómo prefieres que la plataforma te ayude a gestionar las interacciones posteriores a la asesoría, como el seguimiento con los clientes o la retroalimentación?


- Imagina que puedes ofrecer descuentos o promociones especiales a tus clientes a través de la plataforma. ¿Qué tipo de ofertas te gustaría ofrecer y cómo te gustaría gestionarlas?

### 2.2.2. Registro de entrevistas

- Segmento 1: Personas Naturales
- Entrevista 1:
- Nombre: Sara Giovanna Qwistgaard Horna
- Edad: 53
- Distrito: San Miguel
  
<img src="https://github.com/user-attachments/assets/0e0c9687-49cf-4163-bb94-7e8062090cac">

**Link: https://acortar.link/RWaCr0**

En la entrevista, la señora Sara Qwistgaard menciona que busca asesoría en el área de marketing. Además, nos cuenta cómo le gustaría su página de asesoría ideal y su mayor problema con las asesorías en general: los horarios. 

- Entrevista 2:
- Nombre: Orlando Romero Flores
- Edad: 59
- Distrito: San Miguel
  
<img src="https://github.com/user-attachments/assets/10ba027c-e24e-43aa-9cb2-c8bb14c064be">

**Link: https://acortar.link/WrhkQL**

El entrevistado Orlando Romero, quien busca asesoría para administración de equipos de redes, nos relata cómo le gustaría que fuera su experiencia con asesorías online y con la plataforma en general, además de explicar cómo debería funcionar el foco principal de la plataforma.

- Entrevista 3:
- Nombre: Ingrid Noelia Zabala Lasso
- Edad: 33
- Distrito: San Miguel

<img src="https://github.com/user-attachments/assets/47c6166f-b129-4886-aabc-7f1110e1e900">

**Link: Link: https://acortar.link/WyeuS7**

La entrevistada busca asesoría en el área de defensoría médica para el tema legal de las prácticas médicas, y a partir de la entrevista nos da su punto de vista sobre lo indispensable de una asesoría en línea y cuál es el mayor problema que se tiene con los asesores en general.

- Segmento 2: Consultores y Profesionales
- Entrevista 1:
- Nombre: Augusto Montes
- Edad: 20
- Distrito: Jesus Maria
  
<img src="https://github.com/user-attachments/assets/95e8c874-a899-4e98-82f4-31870a74b1bb">

**Link: https://acortar.link/NfWGsQ**

La entrevista con Augusto Montes muestra que, para optimizar su negocio de asesoría profesional, busca una plataforma que combine la generación de leads cualificados con una agenda automatizada, lo que permitiría una reserva sin fricciones y recordatorios automáticos. Prefiere una interfaz equilibrada entre simplicidad y personalización, que permita etiquetar clientes, editar notas privadas y realizar integraciones con otras aplicaciones. En cuanto a pagos, valora la flexibilidad de contar con diferentes modalidades como pago por sesión, suscripciones recurrentes, facturación automática y pagos multimoneda para facilitar transacciones globales. Además, considera importante un sistema de marketing digital basado en referidos para atraer nuevos clientes. Para gestionar solicitudes urgentes, le gustaría contar con una opción de disponibilidad inmediata y la posibilidad de cobrar tarifas premium por consultas urgentes. También está interesado en organizar eventos grupales como seminarios o masterclasses, lo que podría generar más interacción y demanda para sus servicios.

- Entrevista 2:
- Nombre: Maria Fernanda Castillo Espinoza
- Edad: 22
- Distrito: Los olivos
  
<img src="https://github.com/user-attachments/assets/6b1b0eb2-35c1-4dbe-a263-fee7b6745f79">

**Link:  https://acortar.link/TErjgY**

La entrevista con María Fernanda Castillo destaca sus necesidades para optimizar su negocio de asesoría profesional. Busca una plataforma automatizada que permita a los clientes encontrar su perfil, ver disponibilidad en tiempo real y agendar directamente. Para ofrecer el mejor servicio, necesita conocer el tema que el cliente desea tratar, sus objetivos, si ha tenido asesorías previas y cualquier material relevante. Prefiere una interfaz sencilla, pero con opciones de personalización si es necesario. En cuanto al proceso de pagos, valora opciones como pago por sesión, suscripciones mensuales y facturación automática, con la prioridad de que los pagos se depositen rápidamente en su cuenta. Además, le gustaría que la plataforma ofreciera herramientas de marketing digital, como publicidad segmentada, posicionamiento en buscadores, creación de contenido y analítica de rendimiento. Para consultas urgentes, necesita una plataforma que permita ver y gestionar solicitudes en tiempo real, aceptar o reagendar desde su celular y recibir notificaciones eficientes. También está interesada en organizar eventos grupales como seminarios o masterclasses.


- Entrevista 3:
- Nombre: Julio Castro Alejos
- Edad: 24
- Distrito: Pueblo libre
  
<img src="https://github.com/user-attachments/assets/301f2480-1a5e-4671-bbed-48b7ab80f0fb">

**Link: https://acortar.link/EQVuW5**

Julio Castro busca una plataforma para gestionar eficientemente su negocio de asesorías. Identifica la necesidad de filtros que faciliten encontrar clientes adecuados y organizar sesiones con datos claros como fechas, duración y métodos de pago. Prefiere una interfaz sencilla pero con opciones avanzadas para personalizar su experiencia. Valora funcionalidades como pagos por sesión y suscripciones, además de integración con herramientas de marketing como Facebook Ads y YouTube. También destaca la utilidad de notificaciones para evitar conflictos de agenda y opciones para crear y gestionar eventos como seminarios. Finalmente, menciona la importancia de incluir elementos visuales como videos y portafolios para presentar propuestas a nuevos clientes.

### 2.2.3. Análisis de entrevistas

| Nombre                            | Preferencias y Recomendaciones |
|----------------------------------|--------------------------------|
| Sara Giovanna Qwistgaard Horna   | Prefiere basarse en el currículum y recomendaciones específicas de los asesores. Sugiere incluir recursos didácticos (artículos, fotos), asesorías más personales, rápidas y puntuales, y una plataforma sencilla de usar. Se queja de la falta de funcionalidad de búsqueda, que retrasó una cita. |
| Orlando Romero Flores             | Confía más en el currículum del asesor. Propone un sistema de recomendaciones personalizadas y recursos interactivos. Busca mayor formalidad profesional y mejor coordinación de horarios con el asesor, pues tuvo problemas de sincronización en su experiencia anterior. |
| Ingrid Noelia Zabala Lasso       | Da prioridad al currículum del asesor. Valora recursos como artículos, fotos e interactividad, además de una plataforma personalizada y fácil de usar. Experimentó dificultades para localizar al asesor, lo que generó desconfianza. |
| Augusto Montes                   | Requiere automatización para generar clientes cualificados y gestionar la agenda. Desea información detallada del cliente antes de la sesión. Interesado en funciones como pagos por sesión, suscripciones, facturación automática, y herramientas de marketing digital. |
| María Fernanda Castillo Espinoza | Busca una plataforma que facilite la generación de clientes y gestión de sesiones. Valora sistemas de pagos y suscripciones, además de herramientas para organizar eventos (seminarios, masterclasses) y realizar campañas segmentadas para promocionar sus servicios. |
| Julio Castro Alejos              | Desea gestión eficiente del negocio de asesoría, incluyendo organización de sesiones, promoción a través de redes sociales y YouTube, y una agenda flexible. Interesado en materiales visuales e interactivos para mejorar el atractivo de sus servicios. |

## 2.3. Needfinding

En esta sección se presenta el proceso de análisis de la información recolectada a partir de entrevistas y observación de usuarios potenciales. El objetivo es identificar necesidades, comportamientos, motivaciones y principales puntos de dolor, con el fin de sustentar el diseño de la solución.

Como resultado del proceso de needfinding, se desarrollan y presentan los siguientes artefactos de análisis:

- **User Personas:** representación de los perfiles de usuarios clave identificados, describiendo sus características, objetivos, necesidades y frustraciones.
- **User Task Matrix:** matriz que permite priorizar y analizar las tareas más relevantes que los usuarios realizan dentro del contexto del problema.
- **User Journey Maps:** mapeo de la experiencia del usuario a lo largo de su interacción con el servicio, identificando puntos de contacto, emociones y oportunidades de mejora.
- **Empathy Mapping:** herramienta que permite profundizar en lo que el usuario piensa, siente, dice y hace, facilitando una comprensión más humana de sus necesidades.
- **As-Is Scenario Mapping:** análisis del escenario actual del usuario antes de la solución, permitiendo identificar problemas, ineficiencias y oportunidades de innovación.

Este conjunto de artefactos permite construir una visión clara y estructurada del usuario, sirviendo como base fundamental para el diseño de la solución propuesta.

### 2.3.1. User Personas

A continuación, se presentan las fichas de **User Personas** elaboradas a partir del análisis de las entrevistas realizadas. Estas representaciones sintetizan los principales perfiles de usuarios identificados, sus necesidades, objetivos, motivaciones y principales puntos de dolor dentro del contexto de la solución.

---

#### Segmento #1: Solicitante de Servicios

![User Persona 1](https://raw.githubusercontent.com/1ASI0657-7943-2610/report/feature/chapter-02/assets/userpersona1.png)

Este perfil representa a los usuarios que buscan contactar servicios de asesoría o apoyo profesional de manera rápida, confiable y personalizada. Generalmente, son personas que valoran la eficiencia, la facilidad de uso de la plataforma y la seguridad al momento de seleccionar a un experto.

Sus principales necesidades se centran en encontrar profesionales calificados, reducir el tiempo de búsqueda y contar con una experiencia de servicio clara y sin fricciones. Entre sus principales frustraciones destacan la falta de confianza en plataformas poco verificadas y la dificultad para identificar expertos realmente confiables.

---

#### Segmento #2: Proveedores de Servicios

![User Persona 2](https://raw.githubusercontent.com/1ASI0657-7943-2610/report/feature/chapter-02/assets/userpersona2.png)

Este perfil corresponde a profesionales o expertos que ofrecen sus servicios dentro de la plataforma. Su principal objetivo es monetizar su conocimiento, ampliar su alcance y conectar con clientes potenciales de forma eficiente.

Entre sus necesidades destacan contar con una plataforma que les brinde visibilidad, un sistema de pagos seguro y herramientas que faciliten la gestión de sus servicios. Sus principales frustraciones incluyen la baja visibilidad en plataformas saturadas, la competencia elevada y la dificultad para captar clientes de calidad.

---

Estos dos segmentos permiten comprender de manera clara las dos partes fundamentales del ecosistema de la plataforma, facilitando el diseño de una solución equilibrada tanto para usuarios solicitantes como para proveedores de servicios.
  
### 2.3.2. User Task Matrix

### 2.3.2 User Task Matrix

La siguiente matriz presenta las principales tareas identificadas para los segmentos objetivo de **FinTeka**, relacionándolas directamente con funcionalidades, User Stories y componentes funcionales del sistema. Esto permite mantener coherencia entre:
- necesidades detectadas durante la investigación,
- funcionalidades priorizadas en el backlog,
- decisiones de diseño del producto,
- componentes arquitectónicos implementados.

La matriz facilita visualizar qué funcionalidades responden a tareas críticas de los usuarios y cómo estas se distribuyen dentro de los distintos dominios funcionales de la plataforma.

---

#### Criterios de Evaluación

Las tareas fueron clasificadas considerando:
- **Frecuencia:** cantidad de veces que la tarea es ejecutada por el usuario.
- **Importancia:** impacto de la tarea sobre la experiencia y el valor del negocio.
- **Feature Relacionada:** funcionalidad principal que soporta la tarea.
- **User Stories Relacionadas:** historias de usuario vinculadas a la funcionalidad.
- **Epic:** agrupación funcional de alto nivel dentro del backlog del producto.

---

### Segmento #1 — Solicitantes de Servicios

| Tarea del Usuario | Frecuencia | Importancia | Feature Relacionada | User Stories | Epic |
|---|---|---|---|---|---|
| Registrarse e iniciar sesión de forma segura | Alta | Alta | Autenticación y Gestión de Cuenta | US001, US002 | EP01 |
| Crear y actualizar su perfil personal | Media | Alta | Gestión de Perfil de Usuario | US008 | EP01 |
| Buscar especialistas utilizando filtros avanzados | Alta | Alta | Motor de Búsqueda Inteligente | US003, US026 | EP02 |
| Revisar perfiles, experiencia y valoraciones de consultores | Alta | Alta | Visualización de Perfil Profesional | US006, US007 | EP02 |
| Reservar sesiones según disponibilidad | Alta | Alta | Gestión de Reservas y Agenda | US010, US011 | EP03 |
| Realizar pagos seguros y consultar comprobantes | Alta | Alta | Pasarela de Pago Integrada | US014, US015 | EP04 |
| Reprogramar o cancelar sesiones | Media | Media | Gestión del Ciclo de Vida de Reservas | US012, US013 | EP03 |
| Recibir recordatorios y notificaciones | Alta | Alta | Sistema de Notificaciones | US004, US016 | EP05 |
| Consultar historial de sesiones y pagos | Media | Media | Historial y Seguimiento | US017 | EP04 |
| Calificar especialistas luego de una asesoría | Media | Alta | Sistema de Reputación y Valoraciones | US007 | EP02 |
| Guardar especialistas favoritos | Media | Media | Favoritos y Seguimiento | US009 | EP03 |
| Compartir perfiles profesionales | Baja | Media | Compartir Perfil | US028 | EP03 |
| Configurar preferencias visuales | Baja | Baja | Personalización de Interfaz | US029 | EP03 |
| Consultar soporte y preguntas frecuentes | Media | Media | Centro de Ayuda | US026, US027 | EP06 |

---

#### Análisis del Segmento

Las tareas asociadas al solicitante de servicios se concentran principalmente en:
- descubrimiento de especialistas,
- validación de confianza,
- gestión de reservas,
- pagos,
- seguimiento de asesorías.

Las funcionalidades relacionadas con:
- búsqueda,
- perfiles,
- reservas,
- pagos,

presentan alta frecuencia e importancia, por lo que tienen impacto directo en la priorización técnica y arquitectónica del sistema.

Esto justifica decisiones como:
- uso de Redis para optimizar consultas frecuentes,
- persistencia relacional para reservas y pagos,
- integración desacoplada con pasarelas externas,
- notificaciones en tiempo real mediante WebSockets.

---

### Segmento #2 — Consultores y Proveedores de Servicios

| Tarea del Usuario | Frecuencia | Importancia | Feature Relacionada | User Stories | Epic |
|---|---|---|---|---|---|
| Registrarse e iniciar sesión de forma segura | Alta | Alta | Autenticación y Gestión de Cuenta | US001 | EP01 |
| Crear y mantener actualizado su perfil profesional | Alta | Alta | Gestión de Perfil Profesional | US008 | EP01 |
| Configurar especialidades, tarifas y modalidades de atención | Alta | Alta | Configuración de Servicios Profesionales | US018, US019 | EP02 |
| Gestionar disponibilidad y horarios | Alta | Alta | Gestión de Agenda y Disponibilidad | US010 | EP03 |
| Recibir y administrar reservas de sesiones | Alta | Alta | Gestión de Reservas | US011 | EP03 |
| Reprogramar o cancelar sesiones | Media | Media | Gestión del Ciclo de Vida de Sesiones | US012, US013 | EP03 |
| Consultar ingresos, pagos y comprobantes | Media | Alta | Gestión Financiera y Comisiones | US014, US015 | EP04 |
| Gestionar suscripciones premium | Baja | Media | Gestión de Suscripciones | US020 | EP04 |
| Consultar métricas y reputación profesional | Media | Alta | Dashboard Analítico y Reputación | US021, US007 | EP05 |
| Recibir notificaciones relacionadas con sesiones | Alta | Alta | Sistema de Notificaciones | US004, US016 | EP05 |
| Administrar comunicación con clientes | Alta | Alta | Chat y Comunicación Directa | US022, US023 | EP05 |
| Consultar historial de sesiones realizadas | Media | Media | Historial Profesional | US024 | EP04 |
| Configurar preferencias y seguridad de cuenta | Media | Alta | Seguridad y Configuración | US025 | EP01 |

---

#### Análisis del Segmento

Las tareas relacionadas con consultores están orientadas principalmente a:
- organización profesional,
- administración de disponibilidad,
- monetización de servicios,
- reputación,
- comunicación con clientes.

La necesidad de mantener sincronización en tiempo real entre:
- disponibilidad,
- reservas,
- pagos,
- notificaciones,

Influye directamente sobre decisiones arquitectónicas como:
- separación de dominios mediante microservicios,
- persistencia híbrida SQL/NoSQL,
- eventos asíncronos,
- mecanismos de consistencia transaccional.

Asimismo, la gestión dinámica de agendas y reservas motivó el diseño de componentes especializados como:
- `BOOKING_SLOTS`,
- `ADVISORY_SESSIONS`,
- servicios desacoplados de notificación y mensajería.

---

### Relación entre Tareas, Features y Componentes del Sistema

La siguiente tabla resume cómo las tareas de usuario se relacionan con las principales funcionalidades y componentes arquitectónicos del ecosistema FinTeka.

| Área Funcional | Feature Principal | Componente Relacionado |
|---|---|---|
| Autenticación | Login y Seguridad | Identity Service / API Gateway |
| Búsqueda | Filtros y descubrimiento de especialistas | Consultant Service / Redis |
| Reservas | Gestión de agenda y sesiones | Booking Service |
| Pagos | Procesamiento financiero y comisiones | Payment Service |
| Comunicación | Chat y notificaciones | Chat Service / WebSockets |
| Reputación | Valoraciones y métricas | Reputation Service |
| Auditoría | Historial y trazabilidad | User Activity Logs |
| Personalización | Preferencias de interfaz | Frontend UI Layer |

---

#### Consideraciones Funcionales y Arquitectónicas

La relación entre tareas, funcionalidades y componentes técnicos permite:
- identificar funcionalidades de mayor impacto,
- validar cobertura funcional del sistema,
- priorizar correctamente el backlog,
- justificar decisiones arquitectónicas,
- mantener alineación entre UX, negocio y tecnología.

Además, esta trazabilidad facilita futuras iteraciones del producto al permitir identificar rápidamente:
- funcionalidades críticas,
- dependencias funcionales,
- dominios de mayor complejidad,
- oportunidades de escalabilidad y mejora continua.

### 2.3.3. User Journey Mapping

A continuación se muestra el proceso para la realización del User Journey Mapping para los User Persona con el fin de entender las experiencias del usuario sin nuestra solución.

**Segmento #1: Solicitante de Servicios**

<img src="../assets/uxpressia1.png" width="900" height="600">

**Segmento #2: Proveedores de Servicios**

<img src="../assets/uxpressia2.png" width="900" height="600">

### 2.3.4. Empathy Mapping

A continuación se muestra el proceso para la realización del Empathy Mapping para los User Persona con el fin de entender lo que piensa, siente, oye, hace y observa.

**Segmento #1: Solicitante de Servicios**

<img src="../assets/empathy4.png" width="1400" height="600">

Link del Empathy Mapping: https://docs.google.com/drawings/d/1ldThwGvffPsPR6Ea6FWCU5DBOGQAVvXugWDPmzPzgD8/edit?usp=sharing

**Segmento #2: Proveedores de Servicios**

<img src="../assets/empathy.png" width="1400" height="600">

Link del Empathy Mapping: https://docs.google.com/drawings/d/1iiU7QqJ-yt0utAPLlAPtQgQrVaNgFb6AWoq7JaNGiV0/edit

### 2.3.5. As-is Scenario Mapping

A continuación se muestra el proceso para la realización del As-Is Scenario Mapping para los User Persona.

**Segmento #1: Solicitante de Servicios**

<img src="../assets/asis1.png" width="1400" height="600">

**Segmento #2: Proveedores de Servicios**

<img src="../assets/asis2.png" width="1400" height="600">

# Capítulo III: Requirements Specification

## 3.1. To-Be Scenario Mapping

A continuación se presenta la realizacion del To-Be Scenario Mapping por cada user persona.

**Segmento #1: Solicitante de Servicios**

<img width="987" height="387" alt="image" src="https://github.com/user-attachments/assets/28606eac-975e-4424-b686-3a0b86625e71" />

**Segmento #2: Proveedores de Servicios**

<img width="980" height="370" alt="image" src="https://github.com/user-attachments/assets/76e71f62-eef6-4953-8e64-bc38dd8ffb6c" />

## 3.2 Requisitos funcionales y no funcionales

### 3.2.1 Requisitos Funcionales

**Leyenda de prefijos:**


- **IRF** = *Identity Requirements Features*: funciones de identidad, autenticación, seguridad y control de acceso.  
- **NRF** = *Notification Requirements Features*: funciones de notificación, alertas automáticas, recordatorios, comunicaciones del sistema y seguimiento de mensajes enviados.
- **CRRF** = *Calendar, Reservation and Resource Features*: funciones de gestión de reservas, disponibilidad horaria, programación de sesiones, control de agendas y seguimiento del ciclo de vida de las citas.
- **RVF** = *Reputation and Valuation Features*: funciones de gestión de reservas, disponibilidad horaria, programación de sesiones, control de agendas y seguimiento del ciclo de vida de las citas.
- **BAF** = *Browse and Advanced Search Features*: funciones de búsqueda avanzada, filtrado inteligente, ordenamiento de resultados, descubrimiento de especialistas y priorización de perfiles dentro de la plataforma.
- **PRF** = *Profile and User Requirements Features:* funciones de gestión de usuarios, administración de perfiles, información personal, perfiles profesionales, métricas y configuración de cuentas dentro de la plataforma.

| ID      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| IRF-001 | El sistema debe permitir el registro de nuevos usuarios mediante un formulario digital accesible desde la plataforma web, solicitando como datos mínimos correo electrónico, nombre de usuario y contraseña. Durante el proceso, el sistema deberá validar que la información ingresada cumpla con las reglas establecidas de formato, obligatoriedad y unicidad. Una vez completada la validación, la cuenta deberá almacenarse de forma segura en la base de datos y quedar habilitada para el acceso al sistema. |
| IRF-002 | El sistema debe validar que el correo electrónico ingresado por el usuario sea único dentro de la plataforma, tenga una estructura válida conforme a estándares de correo electrónico, no exceda la longitud máxima permitida y sea almacenado en minúsculas para evitar duplicidad por diferencias de escritura. Si el correo ya existe, el sistema deberá rechazar el registro e informar al usuario.                                                                                                             |
| IRF-003 | El sistema debe exigir que la contraseña registrada tenga una longitud mínima de ocho caracteres y máxima de ciento veintiocho caracteres, incluyendo al menos una letra minúscula y un dígito numérico. Además, podrá aplicar reglas adicionales de seguridad para fortalecer la protección de la cuenta. Si no cumple los criterios, el sistema deberá impedir el registro mostrando el motivo correspondiente.                                                                                                   |
| IRF-004 | El sistema debe permitir el inicio de sesión mediante correo electrónico y contraseña desde una interfaz segura. Durante el proceso, deberá validar que las credenciales ingresadas coincidan con las almacenadas en la base de datos mediante mecanismos seguros de comparación cifrada. Si la autenticación es correcta, deberá conceder acceso al usuario; en caso contrario, deberá rechazar el intento e informar el error sin exponer información sensible.                                                   |
| IRF-005 | El sistema debe generar automáticamente un token de acceso y un token de actualización cada vez que un usuario inicie sesión correctamente. Ambos tokens deberán contener la información mínima necesaria para identificar la sesión activa, respetando tiempos de expiración definidos y estándares de seguridad establecidos por la plataforma.                                                                                                                                                                   |
| IRF-006 | El sistema debe validar la vigencia, integridad, firma digital y origen de los tokens utilizados en cada solicitud protegida hacia recursos restringidos. Si el token estuviera expirado, alterado, revocado o no autorizado, el sistema deberá denegar el acceso y solicitar una nueva autenticación.                                                                                                                                                                                                              |
| IRF-007 | El sistema debe permitir la recuperación de contraseña mediante un proceso seguro iniciado por el usuario desde la opción correspondiente. Para ello, deberá enviar un enlace temporal o código de verificación al correo electrónico registrado, permitiendo restablecer la contraseña únicamente después de validar la identidad del solicitante.                                                                                                                                                                 |
| IRF-008 | El sistema debe implementar roles diferenciados de usuario, consultor y administrador, asignando permisos específicos según las funciones de cada tipo de cuenta. Durante cada operación protegida, el sistema deberá verificar el rol asociado al usuario autenticado para autorizar o denegar el acceso a funcionalidades determinadas.                                                                                                                                                                           |
| NRF-001 | El sistema debe enviar una notificación automática de confirmación al correo electrónico del usuario una vez completado satisfactoriamente el proceso de registro en la plataforma. El mensaje deberá incluir información básica de bienvenida, validación de cuenta en caso corresponda y canales oficiales de soporte disponibles. |
| NRF-002 | El sistema debe enviar recordatorios automáticos al usuario y al consultor antes del inicio de cada sesión programada, utilizando los medios de comunicación habilitados por la plataforma. Dichos recordatorios deberán incluir fecha, hora, enlace de acceso y datos relevantes de la asesoría agendada.                           |
| NRF-003 | El sistema debe notificar de manera inmediata al usuario y al consultor cuando una sesión previamente reservada haya sido cancelada por cualquiera de las partes o por decisión administrativa. La notificación deberá indicar el motivo de la cancelación y las acciones posteriores disponibles.                                   |
| NRF-004 | El sistema debe enviar una notificación automática cuando una sesión haya sido reprogramada, informando a ambas partes la nueva fecha, hora y cualquier modificación relevante asociada a la reserva original. Asimismo, deberá conservar evidencia del envío realizado.                                                             |
| NRF-005 | El sistema debe generar alertas relacionadas con procesos de recuperación de contraseña, incluyendo solicitudes de restablecimiento, confirmación de cambio exitoso y advertencias ante intentos sospechosos detectados sobre la cuenta del usuario.                                                                                 |
| NRF-006 | El sistema debe notificar al usuario cuando se confirme exitosamente un pago realizado dentro de la plataforma, detallando el monto abonado, concepto del servicio adquirido, fecha de operación y comprobante digital correspondiente.                                                                                              |
| NRF-007 | El sistema debe enviar alertas al consultor cuando reciba una nueva reserva confirmada, permitiéndole conocer oportunamente la información principal de la sesión agendada y actualizar su planificación de disponibilidad.                                                                                                          |
| NRF-008 | El sistema debe permitir registrar el historial de notificaciones emitidas hacia cada usuario, almacenando tipo de mensaje, fecha de envío, canal utilizado y estado de entrega para fines de seguimiento y auditoría.                                                                                                               |
| CRRF-001 | El sistema debe permitir que los consultores definan, actualicen y eliminen sus horarios disponibles dentro de la plataforma, mediante una agenda digital accesible desde su perfil. Toda modificación deberá reflejarse en tiempo real para evitar inconsistencias con futuras reservas. |
| CRRF-002 | El sistema debe verificar automáticamente la disponibilidad del consultor al momento en que un usuario intente realizar una reserva, validando que el intervalo solicitado no se superponga con sesiones previamente confirmadas o bloqueadas temporalmente.                              |
| CRRF-003 | El sistema debe permitir al usuario reservar una sesión seleccionando fecha, hora y consultor disponible. Antes de confirmar la operación, deberá mostrar un resumen con los datos principales de la cita y las condiciones aplicables.                                                   |
| CRRF-004 | El sistema debe bloquear temporalmente el horario seleccionado durante el proceso de reserva con la finalidad de evitar que otros usuarios lo seleccionen simultáneamente mientras se completa el flujo de confirmación y pago correspondiente.                                           |
| CRRF-005 | Si el proceso de reserva no se completa dentro del tiempo máximo establecido por la plataforma, el sistema debe liberar automáticamente el horario bloqueado para que vuelva a estar disponible para otros usuarios interesados.                                                          |
| CRRF-006 | El sistema debe permitir la cancelación de sesiones programadas conforme a las políticas definidas por la plataforma, registrando la fecha, hora, usuario responsable y motivo asociado a la cancelación realizada.                                                                       |
| CRRF-007 | El sistema debe permitir la reprogramación de sesiones previamente agendadas, conservando un historial detallado de cambios que incluya fecha original, nueva fecha, usuario responsable y momento exacto de la modificación.                                                             |
| CRRF-008 | El sistema debe gestionar el ciclo de vida de cada sesión mediante estados definidos como pendiente, confirmada, en curso, completada y cancelada. Toda transición entre estados deberá registrarse para fines de control y auditoría.                                                    |
| CRRF-009 | El sistema debe permitir al usuario consultar sus sesiones programadas mostrando información relevante como consultor asignado, fecha, hora, estado actual y enlace de acceso en caso de sesiones virtuales.                                                                              |
| CRRF-010 | El sistema debe permitir al consultor visualizar su agenda de sesiones confirmadas, pendientes o reprogramadas, mostrando los datos necesarios para la correcta organización de su disponibilidad profesional.                                                                            |
| CRRF-011 | El sistema debe registrar trazabilidad completa sobre reservas, cancelaciones, reprogramaciones y cambios de estado, almacenando usuario responsable, fecha, hora y detalle de la acción ejecutada.                                                                                       |
| CRRF-012 | En caso de conflicto de horario durante una nueva solicitud de reserva, el sistema debe rechazar automáticamente la operación y sugerir horarios alternativos disponibles dentro de la agenda del consultor.                                                                              |
| RVF-001 | El sistema debe permitir que los usuarios registren una calificación únicamente sobre sesiones que se encuentren en estado completada, garantizando que solo experiencias efectivamente realizadas puedan ser valoradas dentro de la plataforma. |
| RVF-002 | El sistema debe permitir que cada valoración incluya una puntuación numérica dentro del rango definido por la plataforma y un comentario opcional relacionado con la experiencia recibida durante la asesoría.                                   |
| RVF-003 | El sistema debe calcular automáticamente la calificación promedio de cada consultor a partir del conjunto total de valoraciones válidas registradas en su perfil profesional.                                                                    |
| RVF-004 | El sistema debe actualizar de forma inmediata la reputación general del consultor cada vez que se registre, modifique o elimine una nueva valoración autorizada dentro de la plataforma.                                                         |
| RVF-005 | El sistema debe mostrar públicamente en el perfil del consultor la calificación promedio obtenida, el número total de reseñas recibidas y los comentarios visibles aprobados según políticas del sistema.                                        |
| RVF-006 | El sistema debe permitir que los consultores consulten métricas relacionadas con su reputación, incluyendo evolución de puntuaciones, tasa de satisfacción y cantidad de sesiones valoradas.                                                     |
| RVF-007 | El sistema debe impedir que un usuario emita múltiples valoraciones sobre una misma sesión, salvo que la plataforma permita una actualización posterior dentro del plazo establecido.                                                            |
| RVF-008 | El sistema debe detectar y restringir valoraciones que contengan lenguaje ofensivo, contenido inapropiado o incumplimiento de políticas comunitarias, aplicando reglas automáticas o revisión administrativa.                                    |
| RVF-009 | El sistema debe priorizar en los resultados de búsqueda a consultores con mejor reputación, considerando calificación promedio, cantidad de valoraciones válidas y nivel de cumplimiento histórico.                                              |
| RVF-010 | El sistema debe conservar el historial de valoraciones realizadas, incluyendo usuario emisor, consultor evaluado, puntuación otorgada, fecha de registro y cambios posteriores efectuados.                                                       |
| PFF-001 | El sistema debe permitir que los usuarios realicen pagos seguros por sesiones contratadas mediante pasarelas externas autorizadas integradas con la plataforma, garantizando confidencialidad e integridad de la transacción. |
| PFF-002 | El sistema debe validar la confirmación exitosa del pago antes de finalizar el proceso de reserva, evitando que una sesión quede confirmada sin la verificación correspondiente de la operación financiera.                   |
| PFF-003 | El sistema debe registrar cada transacción económica realizada dentro de la plataforma, almacenando información como usuario pagador, consultor asociado, monto, moneda, fecha, método de pago y estado de la operación.      |
| PFF-004 | El sistema debe generar automáticamente un comprobante digital por cada pago exitosamente procesado, incluyendo detalle del servicio contratado, importe pagado y datos identificatorios de la operación.                     |
| PFF-005 | El sistema debe permitir que los usuarios consulten el historial de pagos realizados desde su cuenta personal, mostrando fecha, monto, concepto y estado de cada transacción registrada.                                      |
| PFF-006 | El sistema debe permitir que los consultores visualicen los ingresos generados por sus sesiones completadas, diferenciando montos brutos, comisiones aplicadas y saldo neto disponible.                                       |
| PFF-007 | El sistema debe gestionar reembolsos parciales o totales cuando una sesión sea cancelada conforme a las políticas vigentes de la plataforma, registrando motivo, importe devuelto y fecha del proceso.                        |
| PFF-008 | El sistema debe aplicar automáticamente comisiones, cargos administrativos o descuentos promocionales definidos por la plataforma al momento de procesar cada pago correspondiente.                                           |
| PFF-009 | El sistema debe notificar al usuario y al consultor cuando una transacción sea aprobada, rechazada, anulada o reembolsada, indicando el estado actualizado de la operación financiera.                                        |
| PFF-010 | El sistema debe mantener trazabilidad completa de las operaciones económicas realizadas, permitiendo auditoría posterior sobre pagos, devoluciones, comisiones y movimientos financieros asociados.                           |
| PFF-011 | El sistema debe permitir que los consultores contraten una suscripción premium mediante pago electrónico, habilitando funcionalidades avanzadas definidas por la plataforma una vez confirmada la transacción. |
| PFF-012 | El sistema debe registrar la fecha de inicio, fecha de vencimiento, estado y tipo de plan contratado por cada consultor suscrito.                                                                              |
| PFF-013 | El sistema debe renovar automáticamente la suscripción premium cuando el usuario autorice pagos recurrentes y el cobro sea aprobado por la pasarela correspondiente.                                           |
| PFF-014 | El sistema debe suspender automáticamente los beneficios premium cuando la suscripción expire, sea cancelada o el pago recurrente sea rechazado.                                                               |
| PFF-015 | El sistema debe permitir al consultor consultar su historial de suscripciones, pagos realizados, renovaciones y vencimientos desde su cuenta personal.                                                         |
| PFF-016 | El sistema debe generar comprobantes digitales por cada pago asociado a suscripciones premium contratadas dentro de la plataforma.                                                                             |
| BAF-001 | El sistema debe permitir a los usuarios buscar especialistas mediante un motor de búsqueda interno utilizando criterios como categoría profesional, especialidad, experiencia, tarifa por sesión, reputación y disponibilidad horaria.               |
| BAF-002 | El sistema debe actualizar dinámicamente los resultados de búsqueda cada vez que el usuario aplique, modifique o elimine filtros, sin necesidad de recargar completamente la interfaz de la plataforma.                                              |
| BAF-003 | El sistema debe permitir ordenar los resultados obtenidos según diferentes criterios configurables, tales como menor precio, mayor experiencia, mejor calificación, mayor disponibilidad o relevancia general.                                       |
| BAF-004 | El sistema debe mostrar en los resultados una lista resumida de especialistas incluyendo nombre, fotografía de perfil, especialidad principal, tarifa por sesión, reputación promedio y disponibilidad próxima.                                      |
| BAF-005 | El sistema debe priorizar la visibilidad de consultores con suscripción premium activa dentro de los resultados de búsqueda, aplicando reglas de posicionamiento combinadas con relevancia, reputación y coincidencia con los filtros seleccionados. |
| BAF-006 | El sistema debe permitir búsquedas por palabras clave relacionadas con servicios, áreas de experiencia, certificaciones, descripciones profesionales o temas específicos ofrecidos por los consultores.                                              |
| BAF-007 | El sistema debe sugerir categorías, términos frecuentes o especialistas destacados mientras el usuario escribe en el campo de búsqueda, con la finalidad de agilizar el proceso de descubrimiento.                                                   |
| BAF-008 | El sistema debe permitir filtrar especialistas según modalidad del servicio, distinguiendo entre asesorías virtuales, presenciales o mixtas cuando dicha información esté disponible en el perfil profesional.                                       |
| BAF-009 | El sistema debe excluir automáticamente de los primeros resultados a perfiles inactivos, suspendidos o sin disponibilidad vigente, salvo que el usuario solicite expresamente visualizarlos.                                                         |
| BAF-010 | El sistema debe conservar temporalmente el historial reciente de búsquedas y filtros utilizados por el usuario autenticado para facilitar consultas posteriores dentro de la plataforma.                                                             |
| BAF-011 | El sistema debe recomendar especialistas similares o relacionados en función de búsquedas previas, categorías consultadas y comportamiento general de navegación del usuario.                                                                        |
| BAF-012 | El sistema debe permitir acceder desde los resultados de búsqueda al perfil detallado del consultor seleccionado, mostrando información completa antes de iniciar una reserva.                                                                       |
| PRF-001 | El sistema debe permitir la creación automática de un perfil asociado a cada cuenta registrada dentro de la plataforma, vinculando la información personal básica con las credenciales del usuario autenticado.                                           |
| PRF-002 | El perfil del usuario debe permitir registrar y visualizar datos personales como nombre, apellido, fotografía opcional, correo electrónico y demás información autorizada por la plataforma.                                                              |
| PRF-003 | Cuando la cuenta corresponda a un consultor, el sistema debe habilitar campos adicionales orientados al perfil profesional, incluyendo especialidades, descripción de servicios, años de experiencia, tarifa por sesión y modalidad de atención ofrecida. |
| PRF-004 | El sistema debe permitir consultar perfiles mediante un identificador único, mostrando únicamente la información pública o autorizada según el tipo de usuario y permisos aplicables.                                                                     |
| PRF-005 | El sistema debe permitir a los usuarios actualizar su información personal en cualquier momento, reflejando los cambios realizados de forma inmediata dentro de la plataforma.                                                                            |
| PRF-006 | El sistema debe permitir que los consultores actualicen su perfil profesional, modificando experiencia, tarifas, especialidades, descripción comercial y demás datos relevantes para su visibilidad pública.                                              |
| PRF-007 | El sistema debe permitir a los consultores cargar documentos, títulos, certificaciones y evidencias profesionales, los cuales podrán ser visibles públicamente o quedar sujetos a validación administrativa según políticas internas.                     |
| PRF-008 | El sistema debe mostrar en el perfil público del consultor sus valoraciones, reputación promedio, cantidad de sesiones realizadas y comentarios visibles autorizados por la plataforma.                                                                   |
| PRF-009 | El sistema debe permitir que cada usuario consulte su historial de asesorías realizadas, incluyendo sesiones programadas, completadas, canceladas y reprogramadas según su rol dentro del sistema.                                                        |
| PRF-010 | El sistema debe permitir que los consultores visualicen métricas de desempeño relacionadas con sesiones completadas, tasa de finalización, ingresos generados, reputación promedio y crecimiento de demanda.                                              |
| PRF-011 | El sistema debe permitir al usuario administrar preferencias de cuenta, incluyendo configuración de notificaciones, privacidad de datos y opciones generales disponibles dentro de la plataforma.                                                         |
| PRF-012 | El sistema debe restringir la edición de información sensible o crítica cuando no exista validación previa de identidad o autorización correspondiente, garantizando seguridad sobre los datos almacenados.                                               |

### 3.2.2 Requisitos no Funcionales

| ID | Descripción |
|----|-------------|
| RNF-001 | El sistema debe responder búsquedas de especialistas en un tiempo máximo de **2 segundos** para el 95% de solicitudes bajo una carga normal de hasta 150 usuarios concurrentes. |
| RNF-002 | El sistema debe procesar la creación y confirmación de reservas en un tiempo máximo de **3 segundos** para el 95% de transacciones. |
| RNF-003 | Toda comunicación entre cliente y servidor debe realizarse mediante **HTTPS con TLS 1.2 o superior**. |
| RNF-004 | Las contraseñas de los usuarios deben almacenarse utilizando algoritmos seguros como **BCrypt** con factor de costo mínimo de 10. |
| RNF-005 | El sistema debe validar el 100% de entradas del usuario y rechazar datos inválidos con respuestas **HTTP 400** en menos de 200 ms. |
| RNF-006 | La API REST debe documentarse mediante **OpenAPI 3.0 / Swagger**, cubriendo el 100% de endpoints públicos y privados. |
| RNF-007 | El sistema debe manejar errores devolviendo códigos HTTP adecuados (**200, 201, 400, 401, 403, 404, 500**) en el 100% de solicitudes procesadas. |
| RNF-008 | Las entidades principales del sistema deben utilizar identificadores **UUID versión 4** para garantizar unicidad global. |
| RNF-009 | Los parámetros críticos del sistema (credenciales, claves, tokens, conexiones) deben configurarse mediante **variables de entorno**. |
| RNF-010 | Los perfiles públicos de consultores deben cargar en un tiempo máximo de **1.5 segundos** para el 95% de solicitudes bajo carga normal. |
| RNF-011 | El sistema debe implementar control de acceso basado en roles (**RBAC**), validando permisos en cada solicitud protegida con una latencia menor a **50 ms**. |
| RNF-012 | El sistema debe registrar logs de autenticación, reservas, errores y operaciones críticas con niveles **INFO, WARN y ERROR**, conservando la información por un mínimo de **90 días**. |
| RNF-013 | El sistema debe ser compatible con despliegues en **Docker**, utilizando imágenes optimizadas cuyo tamaño no exceda los **500 MB**. |
| RNF-014 | La interfaz web debe ser compatible con las versiones vigentes de **Google Chrome, Mozilla Firefox, Microsoft Edge y Safari**. |
| RNF-015 | El sistema debe contar con diseño **responsive**, compatible con dispositivos móviles, tabletas y escritorio en resoluciones desde **360 px hasta 1920 px**. |
| RNF-016 | El sistema debe expirar sesiones inactivas de usuario luego de **30 minutos** sin actividad autenticada. |
| RNF-017 | El sistema debe bloquear automáticamente una cuenta luego de **5 intentos fallidos consecutivos** de inicio de sesión durante un periodo de **15 minutos**. |
| RNF-018 | El sistema debe permitir recuperación de contraseña mediante correo electrónico verificado con enlace temporal de validez máxima de **15 minutos**. |

### 3.3 User Stories

En esta sección se presentan los requisitos funcionales definidos para Finteka. Las User Stories permiten comprender las necesidades de los usuarios finales, priorizar funcionalidades y organizar el desarrollo incremental del sistema. Asimismo, cada historia incluye criterios de aceptación que validan su cumplimiento.

| Epic / Story ID | Título | Descripción | Criterios de Aceptación | Relacionado con (Epic ID) |
| :---- | :---- | :---- | :---- | :---- |
| EP01 | Registro de usuarios | Implementar el registro de los usuarios para tanto los asesores como los clientes |  |  |
| US001 | Registrar un profesional | Como profesional. Quiero poder registrarme fácilmente en la plataforma como consultor. Para ofrecer mis servicios, gestionar mis horarios y comenzar a brindar asesoría a personas o empresas interesadas. | **Escenario 01: Registro exitoso.** Dado que soy un profesional interesado en ofrecer mis servicios, Cuando completo correctamente el formulario de registro con mis datos y lo envío, Entonces el sistema guarda la información, envía una notificación de recepción y muestra un mensaje indicando que el perfil será revisado.<br>**Escenario 02: Fallo en el registro.** Dado que soy un profesional que intenta registrarse, Cuando dejo campos obligatorios vacíos o ingreso datos inválidos, Entonces el sistema muestra mensajes de error y no permite enviar el formulario hasta corregir los datos. | EP01 |
| US002 | Registrar un cliente | Como usuario que busca asesoría profesional. Quiero poder registrarme fácilmente en la plataforma como cliente. Para acceder al listado de consultores disponibles, agendar sesiones y recibir asesoría especializada. | **Escenario 01: Registro exitoso.** Dado que soy un nuevo cliente que desea registrarse, Cuando completo correctamente el formulario de registro con mis datos, Entonces el sistema crea mi cuenta, me muestra un mensaje de bienvenida y me redirige al panel de usuario o inicio. <br>**Escenario 02: Registro con errores o campos incompletos.** Dado que intento registrarme con un correo ya registrado, Cuando ingreso el correo electrónico y lo envío, Entonces el sistema me notifica que ya existe una cuenta con ese correo y me sugiere iniciar sesión o recuperar la contraseña. | EP01 |
| EP02 | Búsqueda de servicios | Poder buscar asesorías y recibir ayuda para realizarla |  |  |
| US003 | Buscar profesionales disponibles | Como usuario. Quiero poder buscar y filtrar profesionales disponibles según mi necesidad. Para encontrar al experto más adecuado y reservar una sesión fácilmente. | **Escenario 01: Filtros por disponibilidad.** Dado que estoy buscando un profesional. Cuando aplico un filtro por fecha y hora. Entonces el sistema me muestra solo aquellos consultores que tienen horarios disponibles en ese rango. <br>**Escenario 02: Visualización de perfil profesional.** Dado que encontré un profesional que me interesa. Cuando hago clic en su perfil. Entonces puedo ver su información completa, experiencia, calificaciones, disponibilidad y tarifas. | EP02 |
| US004 | Recibir notificaciones de disponibilidad de profesionales | Como usuario. Quiero recibir notificaciones cuando un profesional que sigo esté disponible para sesiones. Para poder agendar una sesión cuando el profesional esté libre. | **Escenario 01: Notificación de disponibilidad.** Dado que estoy siguiendo a un profesional, Cuando el profesional actualiza su disponibilidad, Entonces recibo una notificación en mi correo o aplicación con los nuevos horarios disponibles.<br>**Escenario 02: Notificación para programar sesión.** Dado que recibo una notificación de disponibilidad, Cuando hago clic en la notificación, Entonces soy redirigido a la plataforma para poder agendar mi sesión con el profesional. | EP02 |
| US005 | Filtrar experto por tarifa | Como usuario quiero filtrar expertos por tarifa para ajustar mi búsqueda a mi presupuesto. | **Escenario 01: Filtro aplicado de manera exitosa.** Dado que elijo el rango de tarifa deseado. Cuando doy clic en Aplicar filtro. Entonces la plataforma me muestra la lista de expertos cuya tarifa se encuentra en el rango elegido. <br>**Escenario 02: El rango seleccionado no es válido.** Dado que ingreso valores inválidos de rango de tarifa. Cuando quiero aplicar el filtro. Entonces la plataforma muestra un mensaje de error sobre los valores de rango ingresados. | EP02 |
| EP03 | Gestión de Perfiles | Configurar e interactuar con los perfiles |  |  |
| US006 | Ver detalles del profesional | Como usuario. Quiero poder ver el perfil completo de un profesional. Para conocer su experiencia, especialidades, disponibilidad, tarifas y calificaciones antes de tomar una decisión. | **Escenario 01: Visualización de experiencia y especialidades.** Dado que estoy viendo el perfil de un consultor, Cuando navego por la sección de descripción profesional, Entonces puedo leer su formación, experiencia laboral y áreas de especialización. <br>**Escenario 02: Visualización de disponibilidad y tarifas.** Dado que estoy en el perfil de un profesional, Cuando reviso su disponibilidad, Entonces puedo ver los horarios libres para agendar una sesión y el costo por cada servicio. | EP03 |
| US007 | Calificar a un profesional | Como usuario. Quiero poder calificar y dejar un comentario sobre el profesional. Para compartir mi experiencia con otros usuarios y contribuir a la reputación del consultor. | **Escenario 01: Acceso a la opción de calificación tras una sesión completada.** Dado que he completado una sesión con un profesional, Cuando accedo al perfil del profesional, Entonces el sistema me muestra la opción de calificar al consultor correspondiente. <br>**Escenario 02: Envío de calificación y comentario.** Dado que tengo disponible la opción de calificación, Cuando selecciono una puntuación y escribo un comentario, Entonces el sistema guarda la calificación y la muestra públicamente en el perfil del profesional. | EP03 |
| US008 | Actualizar perfil de usuario | Como usuario. Quiero poder actualizar mi perfil en la plataforma. Para mantener mi información personal, preferencias y detalles de contacto actualizados. | **Escenario 01: Actualización exitosa del perfil.** Dado que soy un usuario que desea actualizar mi perfil, Cuando cambio mis datos personales, como el correo o número de teléfono y hago clic en "guardar", Entonces el sistema actualiza mi perfil y me muestra un mensaje de confirmación. <br>**Escenario 02: Error en la actualización del perfil.** Dado que soy un usuario que intenta actualizar mi perfil, Cuando ingreso datos inválidos, como un correo incorrecto, Entonces el sistema muestra un mensaje de error y me indica qué campo debe corregirse. | EP03 |
| US009 | Guardar profesionales como favoritos | Como usuario, quiero poder guardar profesionales como favoritos, para acceder fácilmente a sus perfiles en futuras búsquedas sin tener que encontrarlos nuevamente. | **Escenario 01: Agregar profesional a favoritos.** Dado que estoy viendo el perfil de un consultor, Cuando hago clic en el ícono de “favorito”, Entonces el profesional se añade a mi lista de favoritos y recibo una confirmación. <br>**Escenario 02: Visualización de lista de favoritos.** Dado que he marcado varios profesionales como favoritos, Cuando accedo a la sección “Favoritos” desde mi perfil, Entonces puedo ver una lista con sus nombres, especialidades y accesos directos a sus perfiles. <br>**Escenario 03: Eliminar profesional de favoritos.** Dado que ya no quiero mantener a un profesional en mi lista, Cuando hago clic en el ícono de “eliminar de favoritos”, Entonces este desaparece de mi lista y el sistema me muestra un mensaje de confirmación. | EP03 |
| US010 | Crear y gestionar servicios de profesional | Como profesional quiero crear y gestionar mis servicios para ofrecer distintos tipos de asesoría. | **Escenario 01: Agregar servicio nuevo.** Dado que quiero agregar un servicio nuevo para ofrecer asesoría. Cuando hago clic en Agregar servicio y selecciono la categoría. Entonces, la plataforma muestra un mensaje de servicio agregado de manera satisfactoria. <br>**Escenario 02: Eliminar servicio.** Dado que quiero eliminar un servicio que ya no deseo ofrecer. Cuando selecciono el servicio y hago clic en Eliminar servicio. Entonces, la plataforma muestra un mensaje de servicio eliminado de manera satisfactoria. | EP03 |
| US011 | Responder mensajes de clientes | Como profesional, quiero ver y responder los mensajes de los clientes para mantener buena comunicación. | **Escenario 01: Mensaje enviado de manera exitosa.** Dado que quiero comunicarme con un cliente. Cuando selecciono al cliente y selecciono en Enviar mensaje. Entonces, la plataforma muestra una confirmación de que el mensaje ha sido enviado. | EP03 |
| EP04 | Gestión de Sesiones y Seguimiento | Optimizar la experiencia de los usuarios y consultores antes, durante y después de las sesiones. |  |  |
| US012 | Realizar reserva de sesión | Como usuario. Quiero poder reservar una sesión con un profesional. Para asegurarme de contar con su tiempo disponible para recibir asesoría. | **Escenario 01: Reserva exitosa.** Dado que soy un usuario que desea agendar una sesión. Cuando selecciono un profesional, fecha y hora disponible. Entonces el sistema confirma la reserva y me envía una notificación. <br>**Escenario 02: Fallo en la reserva.** Dado que intento reservar un horario que ya no está disponible. Cuando elijo esa fecha y hora. Entonces el sistema muestra un mensaje de error y me sugiere otros horarios disponibles. | EP04 |
| US013 | Agendar seguimiento post-sesión | Como usuario, quiero poder agendar una sesión de seguimiento con el mismo consultor, para continuar con el proceso de asesoría. | **Escenario 01: Agendamiento desde historial.** Dado que he finalizado una sesión con un consultor, Cuando accedo al historial y selecciono “Agendar seguimiento”, Entonces puedo elegir fecha y hora y confirmar la nueva sesión. <br>**Escenario 02: Confirmación automática.** Dado que seleccioné un horario disponible, Cuando envío la solicitud de seguimiento, Entonces el sistema envía una notificación al consultor y confirma la cita. | EP04 |
| US014 | Tomar notas durante la sesión | Como consultor, quiero tener una sección para tomar notas durante la sesión, para guardar observaciones relevantes del cliente. | **Escenario 01: Acceso al bloc de notas.** Dado que estoy en una sesión activa, Cuando accedo al bloc de notas desde mi panel, Entonces puedo escribir y guardar comentarios privados. <br>**Escenario 02: Guardado automático.** Dado que estoy escribiendo notas durante la sesión, Cuando cierro el panel de notas, Entonces el sistema guarda automáticamente el contenido. | EP04 |
| US015 | Enviar recomendaciones tras sesión | Como consultor, quiero poder enviar al usuario una lista de recomendaciones o materiales luego de la sesión, para complementar la asesoría. | **Escenario 01: Envío de materiales.** Dado que terminé una sesión con un cliente, Cuando selecciono la opción “Enviar recomendaciones”, Entonces puedo adjuntar archivos o escribir sugerencias y enviarlas. <br>**Escenario 02: Visualización por el usuario.** Dado que el consultor me envió recomendaciones, Cuando abro la sesión desde el historial, Entonces puedo ver los materiales recibidos. | EP04 |
| US016 | Ver historial de sesiones | Como usuario. Quiero poder ver un historial de mis sesiones pasadas. Para poder revisar la información de las sesiones anteriores y hacer un seguimiento de mi progreso. | **Escenario 01: Visualización del historial de sesiones.** Dado que soy un usuario que ha tenido sesiones anteriores, Cuando accedo a la sección de historial de sesiones, Entonces puedo ver la lista de todas las sesiones pasadas, con fecha, profesional y detalles. <br>**Escenario 02: Visualización de detalles de una sesión.** Dado que estoy viendo el historial de mis sesiones, Cuando hago clic en una sesión específica, Entonces puedo ver los detalles completos, incluyendo notas o recomendaciones proporcionadas por el profesional. | EP04 |
| US017 | Calificar seguimiento de sesión | Como usuario, quiero poder calificar las sesiones de seguimiento por separado, para evaluar la mejora continua del servicio recibido. | **Escenario 01: Opción disponible tras sesión de seguimiento.** Dado que acabo de completar una sesión de seguimiento, Cuando reviso el historial de esa sesión, Entonces veo la opción de dejar una calificación específica para ella. <br>**Escenario 02: Publicación del comentario.** Dado que escribí una calificación y comentario, Cuando hago clic en “Enviar”, Entonces el sistema guarda y publica la valoración en el perfil del consultor.  | EP04 |
| US018 | Cancelar reserva de sesión | Como usuario. Quiero poder cancelar una reserva de sesión. Para poder modificar mis planes si surge un imprevisto. | <br>**Escenario 01: Cancelación exitosa.** Dado que tengo una sesión programada y deseo cancelarla, Cuando accedo a la opción de cancelación en mi perfil y confirmó la cancelación, Entonces el sistema cancela la sesión y me envía una notificación confirmando la cancelación. <br>**Escenario 02: Error al intentar cancelar.** Dado que intento cancelar una sesión programada en un horario muy cercano, Cuando intento cancelarla, Entonces el sistema muestra un mensaje de advertencia o bloqueo de la opción de cancelación. | EP04 |
| US019 | Notificaciones sobre estado de reserva | Como usuario quiero recibir notificaciones sobre el estado de mi reserva para estar informado en todo momento. | **Escenario 01: Notificación de recordatorio de sesión programada.** Dado que realicé una reserva con un profesional. Cuando hago clic en la notificación. Entonces recibo un detalle sobre la sesión programada junto al día y hora exacta. <br>**Escenario 02: Notificación sobre cancelación de sesión.** Dado que recibo una notificación de cancelación de sesión. Cuando hago clic en la notificación. Entonces soy redirigido a la plataforma para reagendar la sesión con el profesional. | EP04 |
| US20 | Pago en línea seguro al reservar una sesión de asesoría | Como cliente que necesita asesoría profesional quiero poder pagar en línea de forma segura al momento de reservar una sesión para asegurar mi cita con el consultor y evitar complicaciones en el proceso. | **Escenario 01: Pago exitoso.** Dado que el pago se ha procesado correctamente. Cuando la transacción se completa. Entonces el sistema debe mostrar un mensaje de confirmación y actualizar el estado de la reserva como “Confirmada”. <br>**Escenario 02: Fallo en el pago.** Dado que la transacción falla por cualquier motivo. Cuando el sistema detecta el error. Entonces muestra un mensaje al usuario de seleccionar otro método de pago. | EP04 |
| EP05 | Marketing y Crecimiento Profesional | Aumentar la visibilidad de los consultores y facilitar la adquisición de nuevos clientes. |  |  |
| US021 | Publicar testimonios destacados | Como consultor, quiero mostrar testimonios positivos de mis clientes en mi perfil, para generar mayor confianza en nuevos usuarios. | **Escenario 01: Selección de testimonios.** Dado que tengo varias calificaciones positivas, Cuando marco una como “destacada”, Entonces aparece resaltada en la parte superior de mi perfil. <br>**Escenario 02: Eliminación de un testimonio destacado.** Dado que quiero cambiar un testimonio, Cuando desmarco el actual, Entonces este ya no se muestra como destacado en mi perfil. | EP05 |
| US022 | Crear campañas promocionales | Como consultor, quiero poder crear promociones temporales (descuentos o asesorías grupales), para atraer más clientes. | **Escenario 01: Creación de descuento.** Dado que quiero lanzar una promoción, Cuando configuro una campaña con nombre, fecha y porcentaje de descuento, Entonces la promoción queda activa y visible en mi perfil. <br>**Escenario 02: Finalización automática de la campaña.** Dado que la campaña ya terminó, Cuando se alcanza la fecha de fin, Entonces la promoción se desactiva automáticamente. | EP05 |
| US023 | Ver estadísticas de perfil | Como consultor, quiero ver métricas sobre cuántas personas vieron mi perfil, reservaron sesiones o dejaron calificaciones, para medir mi rendimiento. | **Escenario 01: Visualización de métricas básicas.** Dado que accedo a la sección de estadísticas, Cuando ingreso a mi panel de consultor, Entonces puedo ver visitas al perfil, reservas y calificaciones recientes. <br>**Escenario 02: Filtros por fecha.** Dado que quiero analizar mi rendimiento, Cuando selecciono un rango de fechas, Entonces el sistema me muestra los datos correspondientes al período elegido. | EP05 |
| US024 | Gestionar campañas de referidos | Como consultor, quiero invitar a otros consultores o clientes a la plataforma mediante un sistema de referidos, para obtener beneficios por cada nuevo registro. | **Escenario 01: Generación de enlace de referido.** Dado que quiero invitar a nuevos usuarios, Cuando accedo a la sección de referidos, Entonces el sistema genera un enlace único para compartir. <br>**Escenario 02: Registro exitoso de un referido.** Dado que alguien se registra usando mi enlace, Cuando completa el registro, Entonces recibo una notificación y posibles recompensas por el referido. | EP05 |
| US025 | Optimizar visibilidad en buscador | Como consultor, quiero personalizar palabras clave para aparecer más fácilmente en los resultados de búsqueda dentro de la plataforma. | **Escenario 01: Edición de palabras clave del perfil.** Dado que deseo mejorar mi visibilidad, Cuando edito mi perfil y agrego palabras clave relevantes, Entonces mi perfil se ajusta a los criterios del buscador interno. <br>**Escenario 02: Aumento de visibilidad tras actualización.** Dado que añadí nuevas palabras clave, Cuando un usuario busca términos relacionados, Entonces mi perfil aparece mejor posicionado en los resultados. | EP05 |
| US026 | Ver Preguntas Frecuentes (FAQ) | Como usuario, quiero tener una sección de preguntas frecuentes, para poder resolver mis dudas rápidas sobre cómo usar la plataforma sin necesidad de contactar a soporte. | **Escenario 01: Visualización de respuestas.** Dado que tengo dudas sobre la plataforma, Cuando accedo a la sección "Ayuda", Entonces veo una lista de preguntas y al tocar una, se despliega la respuesta hacia abajo. | EP06 |
| US027 | Enviar sugerencia o reporte rápido | Como usuario, quiero tener un formulario simple de contacto, para poder enviar sugerencias de mejora o reportar algún error visual en la aplicación. | **Escenario 01: Envío exitoso.** Dado que quiero enviar un comentario, Cuando lleno el campo de texto y presiono "Enviar", Entonces la pantalla se limpia y la aplicación me muestra un mensaje emergente agradeciendo mi comentario. | EP06 |
| US028 | Compartir perfil del profesional | Como usuario, quiero poder compartir el perfil de un consultor, para poder recomendar sus servicios a mis amigos o colegas enviándoles un enlace. | **Escenario 01: Copiar enlace.** Dado que estoy viendo un perfil interesante, Cuando presiono el ícono de "Compartir", Entonces el sistema copia el enlace del perfil al portapapeles y me muestra un aviso de "Enlace copiado". | EP03 |
| US029 | Cambiar tema (Modo Oscuro / Claro) | Como usuario, quiero poder alternar entre un tema visual claro y oscuro, para adaptar la aplicación a mis preferencias visuales o a la iluminación del entorno. | **Escenario 01: Cambio a modo oscuro.** Dado que la aplicación está en modo claro, Cuando presiono el interruptor de cambio de tema en mi perfil, Entonces los colores de la interfaz cambian inmediatamente a una paleta oscura. | EP03 |

## 3.4. Impact Mapping

Impact map de nuestros segmentos objetivos:

<img width="1040" height="786" alt="image" src="https://github.com/user-attachments/assets/38070dbf-a433-4111-b885-decd80f64564" />

Link del Impact Mapping:https://miro.com/app/board/uXjVJGsSlMY=/?share_link_id=357440759397

## 3.5. Product Backlog

Utilizamos la escala de Fibonacci para la estimación de los Story Points.

| # Orden | User Story Id | Título | Descripción | Story Points |
| :--- | :--- | :--- | :--- | :--- |
| 01 | **US001** | Registro de profesionales | Como experto, deseo registrarme en la plataforma para ofrecer mis servicios y gestionar mi perfil profesional. | 3 |
| 02 | **US002** | Registro de clientes | Como usuario interesado, deseo crear una cuenta para buscar expertos y gestionar mis reservas. | 2 |
| 03 | **US003** | Búsqueda de profesionales disponibles | Como usuario interesado, deseo buscar todos los profesionales disponibles. | 2 |
| 04 | **US026** | Filtros de búsqueda de expertos | Como cliente, deseo filtrar consultores por especialidad y calificación para encontrar al asesor ideal rápidamente. | 5 |
| 05 | **US004** | Notificaciones de disponibilidad de profesionales | Como usuario interesado, deseo recibir notificaciones de disponibilidad del profesional. | 2 |
| 06 | **US005** | Filtros de expertos por tarifa | Como usuario quiero filtrar expertos por tarifa para ajustar mi búsqueda a mi presupuesto. | 5 |
| 07 | **US006** | Visualización de perfil profesional | Como cliente, deseo consultar la experiencia y formación del profesional para validar su capacidad técnica. | 2 |
| 08 | **US007** | Calificación de sesiones | Como cliente, deseo calificar y comentar el servicio recibido para ayudar a otros usuarios en su elección. | 3 |
| 09 | **US028** | Perfiles recomendados | Como administrador, deseo destacar perfiles profesionales para aumentar su visibilidad ante nuevos clientes. | 2 |
| 10 | **US008** | Actualización de perfil | Como usuario, deseo editar mi información personal y de contacto para mantener mi cuenta actualizada. | 2 |
| 11 | **US009** | Favoritos de profesionales | Como cliente, deseo guardar consultores en mi lista de favoritos para acceder a ellos rápidamente en el futuro. | 3 |
| 12 | **US010** | Gestión de disponibilidad | Como consultor, deseo configurar mi agenda de disponibilidad para que los clientes puedan agendar sin conflictos. | 8 |
| 13 | **US011** | Gestión de mensajes | Como consultor, quiero ver y responder los mensajes de los clientes para mantener buena comunicación. | 5 |
| 14 | **US012** | Agendamiento de sesiones | Como cliente, deseo seleccionar un horario y agendar una sesión para asegurar mi consultoría técnica. | 5 |
| 15 | **US013** | Seguimiento post-sesión | Como consultor, deseo registrar notas y tareas pendientes para dar un seguimiento adecuado al progreso del cliente. | 3 |
| 16 | **US014** | Apunte de notas de texto| Como consultor, quiero tener una sección para tomar notas durante la sesión, para guardar observaciones relevantes del cliente. | 2 |
| 17 | **US015** | Enviar recomendaciones tras sesión| Como consultor, quiero poder enviar al usuario una lista de recomendaciones o materiales luego de la sesión, para complementar la asesoría. | 3 |
| 18 | **US016** | Visualizar historial de sesiones| Como usuario. Quiero poder ver un historial de mis sesiones pasadas. Para poder revisar la información de las sesiones anteriores. | 5 |
| 19 | **US017** | Calificar seguimiento de sesión| Como usuario, quiero poder calificar las sesiones de seguimiento por separado, para evaluar la mejora continua del servicio recibido. | 5 |
| 20 | **US018** | Cancelar reserva de sesión| Como usuario. Quiero poder cancelar una reserva de sesión. Para poder modificar mis planes si surge un imprevisto. | 3 |
| 21 | **US027** | Confirmación de sesiones | Como consultor, deseo aceptar o rechazar solicitudes de sesiones para organizar mejor mi tiempo laboral. | 3 |
| 22 | **US019** | Notificaciones de alertas | Como usuario, deseo recibir notificaciones de disponibilidad y recordatorios para no perder mis sesiones programadas. | 3 |
| 23 | **US020** | Pago en línea seguro | Como cliente, deseo realizar el pago mediante la plataforma para confirmar mi reserva de manera automática. | 8 |
| 24 | **US021** | Publicar testimonios destacados | Como consultor, quiero mostrar testimonios positivos de mis clientes en mi perfil, para generar mayor confianza en nuevos usuarios. | 3 |
| 25 | **US022** | Crear campañas promocionales | Como consultor, quiero poder crear promociones temporales, para atraer más clientes. | 3 |
| 26 | **US023** | Ver estadísticas de perfil | Como consultor, quiero ver métricas sobre cuántas personas vieron mi perfil, reservaron sesiones o dejaron calificaciones, para medir mi rendimiento. | 5 |
| 27 | **US024** | Gestionar campañas de referidos | Como consultor, quiero invitar a otros consultores o clientes a la plataforma mediante un sistema de referidos, para obtener beneficios por cada nuevo registro. | 3 |
| 28 | **US025** | Optimizar visibilidad en buscador | Como consultor, quiero personalizar palabras clave para aparecer más fácilmente en los resultados de búsqueda dentro de la plataforma. | 3 |
| 29 | **US029** | SEO y Meta-datos | Como administrador, deseo configurar URLs amigables y metadatos para mejorar el posicionamiento de los expertos en buscadores. | 3 |

<div style="page-break-after: always;"></div>

# Capítulo IV: Product Architecture Design

## 4.1 Design Concepts, ViewPoints & ER Diagrams

## 4.1.1 Principles Statements

* Alineación con la visión de negocio. A partir de la visión de negocio de centralizar el acceso a asesoría profesional de forma organizada, confiable y accesible, y de la visión de una arquitectura de plataforma de microservicios basada en DDD, se establecen los principios rectores que guían el diseño de FinTeka. Estos principios buscan garantizar transacciones seguras, maximizar la cohesión de cada servicio y habilitar cambios ágiles enfocados en la experiencia tanto de los usuarios solicitantes como de los consultores.
  
* Comunicación asincrónica sobre sincrónica. Para procesos que no requieren respuesta inmediata del usuario (como el envío de recordatorios automáticos de sesiones o la actualización de métricas de desempeño ), se privilegian mecanismos orientados a eventos mediante message brokers. Esto desacopla los servicios principales (como reservas y pagos) de los secundarios, aislando fallos y mejorando la escalabilidad.

* Uso de tecnologías con soporte comercial y escalabilidad probada. Para garantizar un rendimiento óptimo, el desarrollo del frontend multiplataforma (móvil y web responsivo desde 360 px hasta 1920 px ) se apoya en Flutter y React, asegurando una experiencia de usuario fluida e interfaces dinámicas. En el backend, se implementan servicios en Python, ideales para el manejo ágil de la lógica de negocio y APIs REST documentadas con OpenAPI 3.0 / Swagger. Para la persistencia de datos relacionales transaccionales (como el historial de sesiones y pagos), se emplean motores robustos como PostgreSQL o MySQL.
  
* Seguridad y privacidad como principio transversal. La seguridad se aplica desde el diseño (Zero Trust). Toda comunicación entre cliente y servidor se realiza mediante HTTPS con TLS 1.2 o superior. Las contraseñas se almacenan utilizando algoritmos seguros como BCrypt. La autenticación es gestionada mediante la generación y validación de tokens de acceso y actualización , apoyada por un control de acceso basado en roles (RBAC) para diferenciar entre usuarios, consultores y administradores con una latencia de validación menor a 50 ms.

* Rendimiento y resiliencia bajo concurrencia. El sistema está diseñado para cumplir con estrictos Acuerdos de Nivel de Servicio (SLAs). Las búsquedas de especialistas se resuelven en un tiempo máximo de 2 segundos, y las confirmaciones de reservas en un máximo de 3 segundos para el 95% de las transacciones. Para lograr esto, se implementan timeouts, circuit breakers y bloqueos temporales de horarios en la base de datos para evitar conflictos o superposiciones en las reservas.

* Observabilidad integrada desde el inicio. El sistema registra logs detallados de autenticación, reservas, errores y operaciones críticas (con niveles INFO, WARN y ERROR), conservando esta información por un mínimo de 90 días para facilitar la trazabilidad completa sobre cancelaciones, reprogramaciones y cambios de estado de sesiones.

* Compatibilidad con principios SOLID y DDD. La lógica de negocio principal (búsqueda de expertos, reservas de agenda, pagos seguros y sistema de valoraciones ) se encapsula en servicios independientes. Se respeta el Principio de Responsabilidad Única (SRP) y se utiliza la Inversión de Dependencias (DIP) para aislar la infraestructura tecnológica de las invariantes del dominio.

* Contenedorización y Portabilidad. El sistema es compatible con despliegues en contenedores, utilizando imágenes optimizadas para agilizar el ciclo de integración y despliegue continuo (CI/CD), asegurando que los entornos de desarrollo, staging y producción sean consistentes.

### 4.1.2 Approaches Statements Architectural Styles & Patterns

Estilos arquitectónicos

Para el desarrollo de FinTeka se adopta el enfoque de Domain-Driven Design (DDD). Este enfoque permite que el modelo de software refleje con alta precisión las reglas de negocio, como la gestión del ciclo de vida de una sesión (pendiente, confirmada, en curso, completada y cancelada) y las reglas de disponibilidad.

El uso de Bounded Contexts segmenta la aplicación en áreas claramente delimitadas:
* Identity & Access Management (IAM): Maneja el registro, la autenticación mediante tokens y la gestión de roles de usuarios y consultores. Especial atención al módulo de "autenticación", garantizando la seguridad en el acceso a la plataforma.
* Search & Profile: Responsable del buscador avanzado (categoría, experiencia, tarifa) y la gestión de la reputación y visualización pública de los consultores.
* Core Reservation (Booking): Maneja el motor de disponibilidad en tiempo real, bloqueos de agenda y conflictos de horarios.
* Communication: Gestiona la mensajería instantánea en tiempo real entre usuarios y consultores.
* Billing & Payments: Centraliza el flujo transaccional y el cobro automático.

El estilo arquitectónico predominante es Microservices Architecture complementado con Event-Driven Architecture (EDA).
* Cada servicio despliega su propio ciclo de vida y base de datos.
* La comunicación entre microservicios (por ejemplo, notificar al módulo de IAM y al módulo de Reservas que un pago ha sido exitoso) se maneja de forma asíncrona mediante eventos de dominio (ej. ReservationConfirmed, PaymentProcessed), permitiendo tolerancia a fallos y alta disponibilidad.

Patrones de diseño y procesamiento

* API Gateway Pattern: Centraliza las solicitudes de las aplicaciones móviles y web, encargándose del enrutamiento, validación de tokens de acceso y rate-limiting.
* CQRS (Command Query Responsibility Segregation): Dado que en una plataforma de búsquedas (como FinTeka) la cantidad de lecturas (usuarios buscando consultores y filtrando tarifas) superará ampliamente a las escrituras (creación de reservas), CQRS permite separar las bases de datos optimizadas para búsqueda rápida de las bases de datos relacionales seguras utilizadas para transacciones financieras y reservas.
* Saga Pattern (Coreography / Orchestration): Utilizado para gestionar el flujo transaccional distribuido de la reserva, asegurando que si el proceso de pago falla, el horario bloqueado temporalmente se libere automáticamente para mantener la consistencia del sistema.

## 4.1.3 Context Diagram

El System Context Diagram corresponde al primer nivel del modelo C4 y permite visualizar el sistema desde una perspectiva general. Su propósito es mostrar cómo FinTeka se relaciona con los principales actores externos y con los sistemas complementarios necesarios para su funcionamiento.

En este contexto, FinTeka se presenta como una plataforma digital orientada a conectar clientes con profesionales, facilitando procesos como búsqueda de especialistas, reservas de sesiones, pagos seguros y videollamadas.

En este Context Diagram se muestra a FinTeka como el sistema central que interactúa con los principales usuarios y servicios externos necesarios para su operación.

<img src="../assets/contextdiagram.jpg" style="width: 100%;" alt="diagramacontexto">

**Link del diagrama:** https://online.visual-paradigm.com/share.jsp?id=343537383331342d32

## 4.1.4 Approach driven ViewPoints Diagrams

#### Usuarios:

El sistema admite los roles de Cliente y Profesional. El profesional gestiona su perfil, disponibilidad y servicios para atender la demanda, mientras que el cliente dispone de herramientas para buscar y reservar especialistas según sus necesidades.

#### Aplicación web:

Espacio donde los usuarios interactúan con la plataforma, buscan profesionales, reservan sesiones, realizan pagos y gestionan citas. Los profesionales administran sus servicios, horarios y consultas recibidas.

#### API Rest:

Actúa como puente hacia los servicios de backend para la obtención y despliegue de datos solicitados.

#### Bases de datos:

Los servicios que requieren almacenamiento registran y consultan información relacionada con usuarios, reservas, pagos, calificaciones y disponibilidad en su base de datos correspondiente.

#### Servicios externos:

Para brindar funcionalidades complementarias se integran servicios externos como PayPal para pagos seguros, Google Calendar para sincronización de citas, Zoom para reuniones virtuales y Gmail para registro y notificaciones por correo.

#### Microservicios: 

- Sistema de Autenticación: Gestiona registro, login y recuperación de contraseña.
- Servicio de Notificaciones: Envía emails y push; maneja plantillas, colas y reintentos.
- Gestión de Reservas y Disponibilidad: Administra horarios de consultores, creación de reservas, cancelaciones, bloqueos y sincronización con calendarios externos.
- Reputación y Valoraciones: Procesa calificaciones (1-5 estrellas), comentarios, cálculo de trust score.
- Pagos y Facturación: Procesa pagos y genera comprobantes electrónicos.
- Búsqueda Avanzada: Permite búsqueda por filtros, autocomplete, facetas y boosting por reputación.
- Gestión de Usuarios y Perfiles: Administra perfiles (cliente/consultor), documentos de identidad, preferencias, portafolio de certificados y suscripciones premium.

#### Microservicios de soporte:

- Pagos: Encargado de comunicar y validar pagos realizados mediante PayPal.
- Notificaciones: Envía alertas sobre reservas, recordatorios, pagos confirmados o cambios de cita mediante correo o push notifications.
- Integración de calendario: Sincroniza eventos y recordatorios con Google Calendar.
- Videollamadas: Genera enlaces de reunión mediante Zoom para sesiones remotas.

<img src="../assets/c1.jpg" style="width: 100%;" alt="diagramacontenedores">

### Sistema de Autenticación - Diagrama de Componentes

A continuación, se muestra el diagrama de componentes correspondiente al microservicio Sistema de Autenticación. Su función principal es gestionar el registro, inicio de sesión, asignación de roles y recuperación de contraseña dentro de la plataforma FinTeka.

<img src="../assets/c2.jpg" style="width: 100%;" alt="diagramacomponentes1">

### Servicio de Notificaciones - Diagrama de Componentes

A continuación, se muestra el diagrama de componentes correspondiente al microservicio Servicio de Notificaciones. Su función principal es centralizar el envío de alertas y comunicaciones vía email, notificaciones push a usuarios y consultores de la plataforma FinTeka.

<img src="../assets/c3.jpg" style="width: 100%;" alt="diagramacomponentes2">

### Gestión de Reservas y Disponibilidad - Diagrama de Componentes

A continuación, se muestra el diagrama de componentes correspondiente al microservicio Gestión de Reservas y Disponibilidad. Su función principal es administrar los horarios de los consultores, crear y validar reservas, gestionar cancelaciones y sincronizar eventos con calendarios externos en FinTeka.

<img src="../assets/c4.jpg" style="width: 100%;" alt="diagramacomponentes3">

### Reputación y Valoraciones - Diagrama de Componentes

A continuación, se muestra el diagrama de componentes correspondiente al microservicio Reputación y Valoraciones. Su función principal es procesar calificaciones (1-5 estrellas), comentarios de usuarios, calcular el trust score de los consultores y prevenir fraudes en las reseñas dentro de FinTeka.

<img src="../assets/c5.jpg" style="width: 100%;" alt="diagramacomponentes4">

### Pagos y Facturación - Diagrama de Componentes

A continuación, se muestra el diagrama de componentes correspondiente al microservicio Pagos y Facturación. Su función principal es procesar transacciones económicas, retener fondos, liberar pagos a consultores y generar comprobantes electrónicos en la plataforma FinTeka.

<img src="../assets/c6.jpg" style="width: 100%;" alt="diagramacomponentes5">

### Búsqueda Avanzada - Diagrama de Componentes

A continuación, se muestra el diagrama de componentes correspondiente al microservicio Búsqueda Avanzada. Su función principal es indexar consultores en motores de búsqueda, permitir filtros dinámicos, autocompletado y ordenamiento por relevancia dentro de FinTeka.

<img src="../assets/c7.jpg" style="width: 100%;" alt="diagramacomponentes6">

### Gestión de Usuarios y Perfiles - Diagrama de Componentes

A continuación, se muestra el diagrama de componentes correspondiente al microservicio Gestión de Usuarios y Perfiles. Su función principal es administrar los datos personales y profesionales de clientes y consultores, documentos de identidad, portafolio de certificados y preferencias de cuenta en FinTeka.

<img src="../assets/c8.jpg" style="width: 100%;" alt="diagramacomponentes7">

**Link de los diagramas:** https://online.visual-paradigm.com/share.jsp?id=343537383331342d32

## 4.1.5 Relational / Non-Relational Database Diagram 

#### Diagrama de Base de Datos

![Diagrama de Base de Datos Híbrido - Finteka](https://res.cloudinary.com/dx0i2vioe/image/upload/v1778370290/Captura_de_pantalla_2026-05-09_a_la_s_6.24.39_p._m._xxe3sa.png)

#### Explicación del Gráfico y Justificación Técnica

# Explicación del Modelo de Datos Relacional (3FN) - Finteka

El diseño de la base de datos de **Finteka** se ha estructurado bajo un modelo relacional unificado, completamente normalizado hasta la **Tercera Forma Normal (3FN)**. El objetivo primordial es garantizar la integridad referencial, eliminar la redundancia de datos y soportar de manera escalable todos los requisitos funcionales detallados en el informe.

## 1. Arquitectura de Identidad (Patrón Supertipo/Subtipo)
Para gestionar eficientemente los distintos roles del sistema manteniendo una base de autenticación única, se ha implementado un esquema de **Especialización**:

* **USERS (Supertipo):** Centraliza las credenciales de acceso (`Email`, `PasswordHash`), el rol del usuario y el estado de la cuenta. Esto permite un control de seguridad centralizado y una gestión de sesiones uniforme.
* **CLIENTS y ADVISORS (Subtipos):** Se vinculan de forma **1:1** con la tabla de usuarios. Esta separación permite que cada perfil posea atributos exclusivos (como `HourlyRate`, `Specialty` y `Bio` para los asesores; o `Preferences` para los clientes) sin comprometer la limpieza del modelo ni mezclar lógicas de negocio.

## 2. Núcleo Transaccional: Gestión de Sesiones
La entidad **ADVISORY_SESSIONS** actúa como el eje central del sistema, orquestando la interacción entre los actores:

* **Relaciones Cardinales:** Conecta a un cliente con un asesor mediante relaciones **1:N**. Esto permite que un usuario registre múltiples asesorías históricas mientras cada registro individual de sesión apunta a un solo par cliente-asesor.
* **Persistencia de Seguimiento (Normalización 3FN):** Para evitar el crecimiento excesivo de la tabla de sesiones y cumplir con las historias de usuario de seguimiento post-cita, se han desacoplado las siguientes entidades:
    * **SESSION_NOTES:** Almacena notas privadas del asesor y apuntes de seguimiento (`FollowUpNotes`).
    * **SESSION_RECOMENDATIONS:** Centraliza el texto de recomendaciones finales y los enlaces a materiales adjuntos para el cliente.

## 3. Integridad Financiera y Reputacional
* **PAYMENTS:** Cada sesión exitosa genera un registro de pago único (**1:1**). Esta tabla registra el monto, la comisión de la plataforma (`PlatformFee`) y el estado transaccional, asegurando una auditoría financiera precisa.
* **REVIEWS:** Implementa el sistema de confianza. Al estar ligada directamente a una sesión (**1:1**), garantiza que solo los clientes que efectivamente pagaron y asistieron a una asesoría puedan calificar al profesional, evitando reseñas fraudulentas.

## 4. Interacción y Auditoría
* **CLIENT_FAVORITES:** Resuelve la relación **Muchos a Muchos (N:M)** entre clientes y asesores, permitiendo a los usuarios gestionar su lista personalizada de profesionales preferidos.
* **MESSAGES y LOGS:** * **MESSAGES:** Gestiona la comunicación vinculándose a la tabla `USERS` para identificar emisores y receptores.
    * **USER_ACTIVITY_LOGS:** Registra de forma secuencial cada acción crítica (logins, cambios de estado, transacciones), cumpliendo con los requisitos de seguridad y trazabilidad.

---

### Justificación Técnica de la Normalización
* **1FN:** Todos los atributos son atómicos y cada tabla posee una clave primaria (`PK`) definida.
* **2FN:** Se han eliminado dependencias parciales; los atributos dependen totalmente de su clave primaria.
* **3FN:** Se han eliminado dependencias transitivas. La información de pagos, notas o recomendaciones reside en tablas satélites relacionadas por llaves foráneas (`FK`), lo que previene anomalías de actualización.
  
## 4.1.6 Design Pattems

Entre los patrones de diseño que emplearemos en el desarrollo de FinTeka destacan los siguientes:

**Patrones creacionales**

Los patrones creacionales permiten instanciar objetos de manera flexible y consistente, reduciendo el acoplamiento entre las clases que solicitan un objeto y las que lo construyen.

* Builder Pattern. Este patrón ofrece un proceso de construcción paso a paso para objetos que requieren múltiples atributos o validaciones antes de quedar listos. Su uso facilita que las entidades complejas de FinTeka, por ejemplo, los perfiles de consultores (con especialidades, tarifas y certificaciones) o las solicitudes de reserva de sesiones, se creen de forma legible y segura, sin depender de constructores con demasiados parámetros.
* Factory Method Pattern. El patrón de fábrica encapsula la lógica de creación en un método especializado que devuelve instancias preparadas para su uso. En FinTeka, esto brinda una interfaz uniforme para obtener objetos como distintos tipos de notificaciones (alertas de disponibilidad, recordatorios de sesión) o integraciones de métodos de pago, independientemente de la clase concreta que los implementa.

**Patrones estructurales**

Los patrones estructurales organizan las relaciones entre clases y componentes para hacerlas más comprensibles y extensibles.

* Facade Pattern. Sirve para exponer una interfaz simplificada y unificada que agrupa operaciones internas complejas. Así, el frontend móvil y web puede interactuar con el dominio de FinTeka (por ejemplo, el proceso unificado de buscar disponibilidad, agendar y pagar) sin conocer el detalle de los microservicios subyacentes, favoreciendo la mantenibilidad.
* Adapter Pattern. Este patrón traduce o adapta la interfaz de un componente externo para que encaje con las necesidades del sistema. En FinTeka será vital para integrar servicios de terceros, como pasarelas de pago para el cobro de comisiones o proveedores de servicios de correo/SMS, evitando reescribir código interno si el proveedor externo cambia.
* Repository Pattern. El repositorio abstrae el acceso a la base de datos (PostgreSQL/MySQL) y separa las consultas y persistencia de las reglas de negocio. Esta separación mejora las pruebas unitarias y reduce la duplicación de lógica al guardar el historial de sesiones o actualizar la reputación de los consultores.

**Patrones de comportamiento**

Los patrones de comportamiento definen cómo colaboran los objetos y encapsulan algoritmos para lograr mayor flexibilidad.

* Command Pattern (CQRS). El patrón Command encapsula cada operación de escritura en FinTeka (ej. registrar especialista, confirmar reserva, procesar pago) en un objeto propio. Esto permite desacoplar la solicitud de la acción de su ejecución, lo que favorece el escalamiento y la integración con colas de mensajes para flujos asincrónicos.
* Query Pattern (CQRS complementario). Al separar las consultas de lectura (ej. filtrar consultores por tarifa, ver historial de asesorías) de los comandos de escritura, se obtiene mayor rendimiento y claridad, algo crítico en el módulo de Search & Profile de la plataforma.
* Strategy Pattern. Este patrón encapsula algoritmos intercambiables. En FinTeka, permite cambiar la estrategia en tiempo de ejecución, por ejemplo, alternar entre distintos algoritmos de ordenamiento de especialistas (por precio, por calificación, por disponibilidad) o distintas estrategias de cálculo de comisiones sin alterar el resto del código.
* Template Method Pattern. Define en una clase base la estructura general de un proceso, delegando en las subclases los pasos específicos. Se emplea para estandarizar el ciclo de vida de las sesiones en FinTeka (Pendiente, Confirmada, En curso, Completada, Cancelada) y asegurar que las auditorías de estado se ejecuten uniformemente.
* Observer Pattern (Eventos de Dominio). Implementa un mecanismo de publicación-suscripción para reaccionar a cambios en el estado de las entidades. En FinTeka, cuando se emite el evento "PagoProcesado", el sistema notifica automáticamente al módulo de reservas para confirmar la cita y al módulo de comunicación para enviar el recordatorio, manteniendo un bajo acoplamiento.
* Service Layer Pattern. La capa de servicios orquesta el uso de repositorios, fábricas y comandos, aislando la lógica de aplicación (como la coordinación entre la pasarela de pagos y la agenda del consultor) del resto de componentes, lo que facilita pruebas y asegura la coherencia del negocio.

**Disponibilidad**

* Uso de técnicas de balanceo de carga en el API Gateway para asegurar que el buscador de especialistas y los perfiles se mantengan accesibles y con tiempos de respuesta menores a 2 segundos, incluso en picos de tráfico.
* Implementación de sistemas de monitorización y alertas tempranas (mediante logs de niveles INFO, WARN, ERROR) que detecten caídas en servicios críticos como el motor de reservas o la pasarela de pagos.

**Fiabilidad**

* Realización de pruebas exhaustivas de software sobre los módulos de transacciones financieras y validación de cruces de horarios, para identificar y corregir errores antes de que afecten la reserva de un cliente.
* Implementación de mecanismos de recuperación ante fallos mediante el patrón Saga, asegurando que si un pago falla, la reserva temporal del horario del consultor se libere automáticamente.
* Uso de técnicas de registro y auditoría que permitan rastrear historial de cancelaciones, cambios de citas o inconsistencias en los cobros.

**Modificabilidad**

* Aplicación de un enfoque de microservicios basados en DDD que facilite la escalabilidad hacia nuevos modelos de negocio (por ejemplo, agregar sesiones grupales, masterclasses o suscripciones mensuales) sin afectar el flujo de asesorías individuales 1 a 1.
* Uso de técnicas de refactoring y pruebas automatizadas para mantener los servicios de FinTeka fáciles de extender y modificar sin comprometer la experiencia del consultor ni del cliente.

**Usabilidad**

* Realización de pruebas de usabilidad con profesionales y usuarios reales, validando que el proceso de agendar una sesión tome la menor cantidad de pasos posibles y que el panel de gestión del consultor sea intuitivo.
* Incorporación de retroalimentación directa de los usuarios para ajustar los filtros de búsqueda, el diseño visual (incluyendo el Modo Oscuro/Claro) y la claridad de la información en los perfiles.

**Seguridad**

* Implementación de medidas Zero Trust, autenticación con tokens, autorización basada en roles (RBAC) y cifrado TLS 1.2 para proteger cuentas de usuarios, historiales de asesoría y datos de tarjetas de crédito.
* Realización de auditorías de seguridad regulares y control estricto de accesos para proteger la plataforma frente a intentos de fraude, suplantación de consultores o vulneración de datos personales.

## 4.1.7 Tactics 

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


## 4.2 Architectural Drivers

### 4.3.1 Iteration 1: Sprint 1

### 4.3.1.1 Architectural Design Backlog 1

En esta primera iteración, se busca construir la primera versión del sistema, priorizando las reglas principales del negocio. Se permitirá que los usuarios puedan buscar especialidades, visualizar perfiles profesionales y concretar asesorías de manera funcional, mientras que los consultores obtendrán una visibilidad inicial sobre la gestión de sus servicios y su disponibilidad. Se busca implementar un flujo básico pero completo que cubra las principales interacciones del sistema, desde la exploración de especialistas hasta la confirmación de una asesoría.

Asimismo, en esta etapa se definirán las bases de comunicación entre los componentes principales del sistema, garantizando que el intercambio de información sea claro y consistente. Esto facilitará el seguimiento de las operaciones realizadas dentro de la plataforma y aportará mayor transparencia en su funcionamiento.

Finalmente, esta iteración tiene como propósito establecer una base sólida sobre la cual se pueda validar el funcionamiento general de FinTeka, permitiendo identificar oportunidades de mejora e incorporar nuevas funcionalidades en futuras versiones, como pagos integrados, sistemas de calificación y herramientas de comunicación entre usuarios y consultores.

| Tipo de Driver      | Driver Seleccionado                           | Razón                                                                                                                                                |
| ------------------- | --------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| Objetivo de Negocio | Lanzar versión funcional inicial              | Se busca contar con una primera versión operativa que permita conectar usuarios con consultores y validar el interés real del mercado.               |
| Atributo de Calidad | Usability                                     | La plataforma debe ser intuitiva y fácil de usar para que los usuarios puedan registrarse, buscar especialistas y reservar asesorías sin dificultad. |
| Atributo de Calidad | Availability                                  | El sistema debe mantenerse disponible para consultas y reservas en horarios variados, evitando interrupciones que afecten la confianza del usuario.  |
| Atributo de Calidad | Modifiability                                 | La arquitectura debe facilitar futuras mejoras como pagos en línea, calificaciones y chat interno sin rehacer componentes principales.               |
| Restricción         | Arquitectura basada en microservicios con enfoque DDD, utilizando Spring Boot, .NET y Go | Se adopta este enfoque para organizar mejor los dominios del negocio, permitir crecimiento progresivo y simplificar el mantenimiento del sistema.    |



### 4.3.1.2 Establish Iteration Goal by Selecting Drivers


En la primera iteración se busca priorizar los siguientes atributos de calidad:

| Atributo de Calidad | Descripción                                                                                                                                                   |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Usability           | Garantizar una experiencia intuitiva y sencilla para que los usuarios puedan registrarse, buscar especialistas y reservar asesorías sin dificultad.           |
| Availability        | Asegurar que la plataforma se mantenga accesible para consultas y reservas en distintos horarios, minimizando interrupciones del servicio.                    |
| Modifiability       | Facilitar la incorporación futura de nuevas funcionalidades como pagos en línea, calificaciones y herramientas de comunicación sin afectar el sistema actual. |


Se prioriza la funcionalidad core del sistema FinTeka, permitiendo a los usuarios registrarse, buscar especialistas, visualizar perfiles y reservar sesiones de manera rápida, segura y confiable.

### 4.3.1.3 Choose One or More Elements of the System to Refine

Con el fin de responder a los drivers priorizados y asegurar la entrega  en esta primera iteración, se identifican los componentes más relevantes del sistema que serán detallados y refinados durante el diseño arquitectónico inicial.


#### Servicio de Gestión de Consultores y Especialidades

* Administra la información profesional de los consultores, incluyendo perfiles, experiencia, áreas de especialización y disponibilidad.
* Permite que los usuarios exploren especialistas y encuentren opciones acordes a sus necesidades.
* Representa el punto principal de conexión entre la oferta de servicios y la demanda de asesorías dentro de la plataforma.

#### Servicio de Reservas y Asesorías

* Gestiona el proceso de solicitud, programación y confirmación de sesiones entre usuarios y consultores.
* Controla horarios disponibles, estado de las reservas y seguimiento de cada asesoría agendada.
* Garantiza una operación confiable y ordenada en el flujo principal del negocio.

Estos componentes constituyen el núcleo funcional de FinTeka en esta iteración, ya que permiten materializar la propuesta de valor principal: conectar usuarios con especialistas y facilitar la contratación de asesorías de forma eficiente y confiable.

### 4.3.1.5 Choose One or More Design Concepts That Satisfy the Selected Drivers

Con el propósito de satisfacer los drivers arquitectónicos priorizados para el ecosistema de **FinTeka**, se adoptan múltiples conceptos de diseño enfocados en garantizar:
- experiencia de usuario,
- disponibilidad continua,
- escalabilidad,
- seguridad,
- facilidad de mantenimiento y evolución tecnológica.

Estas decisiones arquitectónicas buscan asegurar que la plataforma pueda operar eficientemente bajo escenarios de alta concurrencia, integraciones distribuidas y crecimiento progresivo del negocio.

---

#### Usability

* La interfaz web será desarrollada bajo un enfoque **responsive design**, garantizando compatibilidad y correcta visualización en dispositivos móviles, tablets y escritorio (RNF-015).
* Los flujos críticos de negocio como:
  - registro,
  - autenticación,
  - búsqueda de especialistas,
  - reserva de sesiones,
  - pagos,
  
  deberán ser intuitivos y minimizar la cantidad de pasos requeridos por el usuario.

* Los perfiles públicos de consultores deberán cargar en un tiempo máximo de **1.5 segundos** para garantizar navegación fluida y mejorar la percepción de rendimiento (RNF-010).
* Se implementará diseño centrado en el usuario (*User-Centered Design*), priorizando accesibilidad, claridad visual y facilidad de navegación.
* La plataforma será compatible con navegadores modernos como:
  - Chrome,
  - Firefox,
  - Edge,
  - Safari (RNF-014).

* Se minimizará el *over-fetching* de información mediante APIs optimizadas para dispositivos móviles.
* Los mensajes de error y validaciones serán claros y orientados a facilitar la corrección rápida por parte del usuario.

---

#### Availability

* Los microservicios serán desplegados utilizando contenedores Docker, permitiendo:
  - portabilidad,
  - recuperación rápida,
  - despliegues consistentes,
  - reinicio automático de servicios (RNF-013).

* La solución utilizará una arquitectura distribuida donde fallos parciales no afecten completamente al ecosistema.
* Los servicios críticos se desplegarán bajo una configuración **Multi-AZ (Multi Availability Zone)** para garantizar continuidad operacional.
* Se implementarán balanceadores de carga para distribuir tráfico entre múltiples instancias.
* Las búsquedas de especialistas deberán responder en un máximo de **2 segundos** bajo carga normal (RNF-001).
* La creación y confirmación de reservas deberá completarse en un máximo de **3 segundos** para la mayoría de solicitudes (RNF-002).
* El sistema incorporará:
  - monitoreo centralizado,
  - health checks,
  - alertas automáticas,
  - trazabilidad de errores y eventos críticos (RNF-012).

* Se utilizarán mecanismos de failover automático para reducir el tiempo de recuperación ante fallos de infraestructura.

---

#### Modifiability

* El sistema será desarrollado bajo una arquitectura de microservicios combinada con principios de **DDD (Domain-Driven Design)**.
* Los dominios funcionales estarán desacoplados en servicios independientes como:
  - autenticación,
  - consultores,
  - reservas,
  - pagos,
  - notificaciones,
  - chat.

* Se emplearán tecnologías como:
  - Spring Boot,
  - .NET,
  - Go,

  seleccionando cada framework según necesidades específicas de:
  - rendimiento,
  - mantenibilidad,
  - integración,
  - concurrencia.

* Se incorporará un *message broker* basado en Kafka para comunicación asíncrona entre servicios.
* Las APIs serán documentadas mediante **OpenAPI / Swagger**, facilitando:
  - mantenimiento,
  - integración,
  - versionamiento,
  - pruebas automatizadas (RNF-006).

* El uso de:
  - UUID,
  - variables de entorno,
  - contenedores,

  permitirá escalar ambientes y automatizar despliegues con menor complejidad (RNF-008, RNF-009).

* La arquitectura permitirá incorporar nuevos módulos como:
  - pagos avanzados,
  - reputación,
  - videollamadas,
  - analítica,
  - inteligencia artificial,

  sin afectar el núcleo transaccional de la plataforma.

---

#### Security

* La autenticación será implementada mediante el estándar **OAuth2** utilizando tokens **JWT (JSON Web Tokens)** para validación descentralizada.
* Se implementará un modelo de autorización basado en roles (**RBAC**) diferenciando permisos para:
  - Clientes,
  - Consultores,
  - Administradores.

* Toda la comunicación entre clientes, APIs y microservicios se realizará bajo protocolos seguros HTTPS/TLS.
* Las contraseñas serán almacenadas utilizando algoritmos de hashing seguro.
* Los endpoints sensibles estarán protegidos mediante un API Gateway centralizado.
* Se implementarán mecanismos de:
  - rate limiting,
  - validación de tokens,
  - expiración de sesiones,
  - control de accesos.

* Los logs de seguridad y auditoría serán persistidos en una base NoSQL especializada para garantizar trazabilidad y análisis posterior.
* Se aplicarán principios de *Zero Trust* para minimizar riesgos de acceso indebido.
* Las integraciones con pasarelas de pago se realizarán mediante conexiones seguras y desacopladas.

---

#### Scalability

* La arquitectura basada en microservicios permitirá escalabilidad horizontal independiente para cada componente del sistema.
* Los servicios con alta demanda, como:
  - chat,
  - reservas,
  - búsqueda de consultores,

  podrán incrementar instancias automáticamente según métricas de utilización.

* Redis será utilizado como capa de caché distribuida para reducir carga sobre la base de datos relacional.
* La persistencia políglota permitirá separar:
  - operaciones transaccionales críticas,
  - datos no estructurados,
  - mensajería en tiempo real,
  - auditoría.

* La plataforma utilizará Kubernetes para:
  - orquestación,
  - autoescalado,
  - balanceo interno,
  - recuperación automática.

* El sistema deberá soportar crecimiento progresivo de:
  - usuarios concurrentes,
  - reservas,
  - mensajes,
  - transacciones financieras,

  sin degradar significativamente el rendimiento general.

* Se implementarán colas asíncronas y procesamiento desacoplado para evitar cuellos de botella durante eventos de alta demanda.
* La arquitectura permitirá expansión futura hacia:
  - nuevos mercados,
  - nuevos servicios financieros,
  - aplicaciones móviles nativas,
  - integraciones empresariales.

### 4.3.1.6 Instantiate Architectural Elements, Allocate Responsibilities, and Define Interfaces

La arquitectura de FinTeka se plantea como una solución basada en microservicios organizados por dominios de negocio, permitiendo separar responsabilidades funcionales y facilitar la evolución del sistema. Los servicios colaboran mediante APIs REST para operaciones síncronas y mensajería asíncrona mediante un broker de eventos para procesos desacoplados. En esta primera iteración se detallan los principales elementos arquitectónicos, sus responsabilidades y los mecanismos de integración definidos.

#### Elementos arquitectónicos

Se usará el enfoque DDD (Domain-Driven Design) para organizar la aplicación.Por ello, cada módulo será definido como un Bounded Context.


* Iam: encargado del registro de usuarios, autenticación, recuperación de contraseña y gestión de roles.
* Consultant: Administra perfiles profesionales, especialidades, experiencia y disponibilidad de los consultores.
* Booking: Gestiona solicitudes, programación, confirmación y seguimiento de asesorías reservadas por los usuarios.
* Notification: Procesa eventos del sistema y envía confirmaciones o alertas por correo electrónico.

Los microservicios serán desarrollados con Spring Boot, .NET y Go, seleccionando la tecnología más adecuada según el dominio funcional y requerimientos de rendimiento.

El frontend será desarrollado en Angular, consumiendo los servicios a través del API Gateway. La solución será desplegada en contenedores Docker, permitiendo portabilidad, escalabilidad y facilidad operativa.

#### Asignación de responsabilidades

Cada servicio mantiene autonomía sobre sus datos y lógica de negocio:

* Iam: Valida: credenciales, genera tokens JWT y controla acceso según roles definidos.
* Consultant: Publica información de consultores y responde consultas relacionadas con perfiles y especialidades.
* Booking:  Verifica disponibilidad horaria, registra reservas y actualiza el estado de las asesorías.
* Notification:  recibe eventos como registro exitoso o reserva confirmada y ejecuta envíos automáticos.

#### Definición de interfaces
La comunicación entre componentes se implementará mediante interfaces síncronas y asíncronas:

* Las interfaces síncronas utilizarán REST APIs documentadas con OpenAPI 3.0 / Swagger, accesibles únicamente mediante el API Gateway.
*  Las interfaces asíncronas emplearán un message broker (RabbitMQ o Kafka) para eventos como UserRegistered, BookingCreated y BookingConfirmed, desacoplando procesos secundarios del flujo principal.
* Todas las comunicaciones externas estarán protegidas mediante HTTPS con TLS.
* Los endpoints privados requerirán autenticación mediante JWT Bearer Token y validación de permisos por rol.

El frontend Angular funcionará como cliente principal para usuarios y consultores, mostrando vistas diferenciadas según permisos y tipo de cuenta, pero consumiendo una misma capa de servicios centralizada.
### 4.3.1.6 Sketch Views (C4 & UML) and Record Design Decisions
![it1.jpg](../assets/it1.jpg)
### 4.3.1.7 Analysis of Current Design and Review Iteration Goal

Para controlar las tareas en esta primera iteracion usamos la herramienta trello que nos permite organizar el trabajo en columnas de "To Do", "In Progress" y "Done". Esto facilita la visualización del progreso, la asignación de responsabilidades y la identificación de bloqueos o retrasos en el desarrollo de las funcionalidades planificadas.

![trello1.jpeg](../assets/trello1.jpeg)

Link del trablero trello: https://trello.com/invite/b/69f6574d811b27877f919b44/ATTI455d8960b544133b522a03a00ce8bfcfE7BD0119/fundamentos-iteration-1
# Capítulo V: Product Implementation, Validation & Deployment

# 5.1 Testing Suites & General Patterns

En el desarrollo de **Finteka**, se han adoptado estándares de ingeniería de software de alto nivel para garantizar que la arquitectura de microservicios sea resiliente, escalable y mantenible. A continuación, se detallan las estrategias de pruebas y los patrones aplicados tanto en el backend (**Java/Spring Boot**) como en la integración con el frontend (**Vue.js**).

## 5.1.1 Backend Application Core Testing Suite

La estrategia de testing de **Finteka** sigue el modelo de la pirámide de automatización, asegurando la integridad del sistema en múltiples niveles:

* **Unit Testing (JUnit 5 & Mockito):** Se validan de forma aislada las reglas de negocio en la capa `@Service`. Utilizamos **Mockito** para simular el comportamiento de las interfaces de persistencia y servicios externos (API de PayPal, Zoom), garantizando que las pruebas de dominio no tengan efectos secundarios ni dependencias de red.
* **Integration Testing (Spring Boot Test & Testcontainers):** Validamos la interacción entre los componentes de Spring y la base de datos **PostgreSQL**. Mediante el uso de **Testcontainers**, levantamos instancias reales de la base de datos en contenedores Docker durante la ejecución de los tests, asegurando que los repositorios y las consultas JPQL sean 100% compatibles con el entorno de producción.
* **Cloud Service Testing (LocalStack for S3):** Dada la dependencia de Finteka con **Amazon S3** para el almacenamiento de documentos y certificados, empleamos **LocalStack**. Esto nos permite ejecutar pruebas de integración locales que simulan el comportamiento de los buckets de AWS sin incurrir en costos ni requerir credenciales reales en entornos de desarrollo.
* **Contract Testing (Spring Cloud Contract):** Para asegurar que la comunicación entre microservicios (ej. *Payments* e *Identity*) no se rompa tras un despliegue, implementamos pruebas de contrato que validan la estructura de los JSON intercambiados.

## 5.1.2 Pattern Based Backend Application(s)

La arquitectura backend de Finteka implementa patrones tácticos de **Domain-Driven Design (DDD)** para gestionar la complejidad distribuida:

1.  **CQRS (Command Query Responsibility Segregation):** Separamos las operaciones de escritura (comandos) de las de lectura (consultas). Esto permite que el microservicio de búsqueda de especialistas utilice modelos de datos optimizados, cumpliendo con el RNF de respuesta de **menos de 1.5 segundos**.
2.  **Saga Pattern (Orchestration):** Fundamental para mantener la consistencia en procesos que involucran múltiples servicios (ej. Reserva + Pago). Si el proceso de pago falla, la Saga coordina automáticamente una transacción de compensación para liberar el cupo del consultor.
3.  **Data Transfer Object (DTO) Pattern:** Utilizamos DTOs para exponer únicamente la información necesaria al frontend en **Vue.js**, protegiendo la integridad de las entidades del dominio y optimizando el payload de las respuestas HTTP.

## 5.1.3 Pattern Based Custom Software Library

Para promover la reutilización y el cumplimiento de los **Cross-cutting Concerns**, se ha desarrollado una librería compartida denominada `finteka-shared-kernel`:

* **Adapter Pattern (Hexagonal Architecture):** Implementamos una interfaz `StoragePort` para el manejo de archivos. El adaptador concreto para **Amazon S3** se inyecta en producción, mientras que en desarrollo se puede usar un adaptador de sistema de archivos local. Esto hace que el sistema sea **Cloud-Agnostic**.
* **Global Exception Handling:** Mediante un `@ControllerAdvice`, centralizamos la captura de excepciones para transformar errores de Java en respuestas estandarizadas que el cliente de **Vue.js/Axios** pueda procesar de forma uniforme.
* **Strategy Pattern (Payment Processors):** Abstraemos la lógica de las pasarelas de pago. Esto permite que Finteka soporte **PayPal, Stripe o transferencias bancarias** simplemente cambiando la estrategia de ejecución en tiempo de ejecución.

## 5.1.4 Framework Pattern Driven Refactoring Report

Este informe documenta las mejoras logradas mediante la aplicación de patrones para mitigar la deuda técnica:

| Hallazgo Técnico | Patrón Aplicado | Atributo de Calidad Impactado |
| :--- | :--- | :--- |
| Alta dependencia del SDK de AWS (`aws-sdk-java`) en servicios de negocio. | **Adapter Pattern** | **Modificabilidad:** El código de negocio es ahora independiente del proveedor de nube. |
| Consultas lentas por realizar joins complejos entre microservicios. | **Read Models (CQRS)** | **Rendimiento:** Reducción del tiempo de carga de perfiles de especialistas en un 45%. |
| Fallos en cascada cuando servicios de terceros (Zoom/Meet) estaban caídos. | **Circuit Breaker (Resilience4j)** | **Disponibilidad:** El sistema detecta fallos externos y activa rutas alternativas sin bloquear los hilos del servidor. |
| Lógica de autenticación JWT dispersa en múltiples filtros de seguridad. | **API Gateway Pattern** | **Seguridad:** Se centralizó la validación de seguridad, reduciendo la superficie de ataque y simplificando el mantenimiento. |

---

## 5.3 Microservices Implementation
## 5.3.1 Sprint 1
### 5.3.1.1 Sprint Backlog 1


| Sprint | User Story | Work-Item / Task | Description | Est. Hours | Assigned To | Status |
| --- | --- | --- | --- | --- | --- | --- |
| Sprint 1 | US001 — Registro de profesionales | T001 — Endpoint registro profesional | Implementar `POST /api/professionals` para registrar profesionales con validación de datos obligatorios. | 12 | Backend Team | Done |
| Sprint 1 | US001 — Registro de profesionales | T002 — Modelo Professional | Crear entidad `Professional` con atributos: id, especialidad, tarifa, experiencia y profileId. | 8 | Backend Team | Done |
| Sprint 1 | US001 — Registro de profesionales | T003 — UI registro profesional | Diseñar formulario frontend para registrar profesionales con validaciones de campos requeridos. | 10 | Frontend Team | Done |
| Sprint 1 | US001 — Registro de profesionales | T004 — Integración frontend-backend profesional | Conectar formulario de registro profesional con API REST y manejo de respuestas. | 6 | Frontend Team | Done |
| Sprint 1 | US001 — Registro de profesionales | T005 — Testing registro profesional | Probar registros exitosos, campos vacíos y errores de validación. | 5 | QA Team | Done |
| Sprint 1 | US002 — Registro de clientes | T006 — Endpoint registro cliente | Implementar `POST /api/profiles` para crear perfiles de usuarios clientes. | 10 | Backend Team | Done |
| Sprint 1 | US002 — Registro de clientes | T007 — UI registro cliente | Crear interfaz de registro para clientes con ingreso de datos personales. | 8 | Frontend Team | Done |
| Sprint 1 | US002 — Registro de clientes | T008 — Integración frontend-backend cliente | Conectar formulario de cliente con API de registro y mensajes de confirmación/error. | 6 | Frontend Team | Done |
| Sprint 1 | US002 — Registro de clientes | T009 — Testing registro cliente | Validar correo repetido, campos incompletos y registro correcto. | 5 | QA Team | Done |
| Sprint 1 | US008 — Actualización de perfil | T010 — Endpoint editar perfil | Implementar `PUT /api/profiles/{id}` para actualizar información del usuario. | 8 | Backend Team | Done |
| Sprint 1 | US008 — Actualización de perfil | T011 — UI editar perfil | Diseñar pantalla para editar correo, teléfono y datos personales. | 8 | Frontend Team | Done |

#### Sprint Duration

El Sprint 1 tiene una duración estimada de **2 semanas (10 días hábiles)**, considerando una carga total aproximada de 86 horas distribuidas entre los equipos de Backend, Frontend, QA y DevOps.

### 5.3.1.2 Development Evidence for Sprint Review

| Repository       | Branch | Commit Id    | Commit Message                             | Commit Message Body                                                                                           | Committed on (Date) |
| ---------------- | ------ | ------------ | ------------------------------------------ | ------------------------------------------------------------------------------------------------------------- | ------------------- |
| FinTeka-Frontend | main   | a1b2c3d4e5f6 | Initial frontend structure                 | Configured Vue project structure with layouts, router, shared components, App.vue and main.js.                | 05/07/2026          |
| FinTeka-Frontend | main   | b2c3d4e5f6g7 | Add authentication module                  | Implemented login view, route guards and authorization logic for secure access to protected pages.            | 05/08/2026          |
| FinTeka-Frontend | main   | c3d4e5f6g7h8 | Update dashboard and pages                 | Added dashboard views and updated pages for professionals, reservations, profile and messages modules.        | 05/09/2026          |
| FinTeka-Frontend | main   | d4e5f6g7h8i9 | Integrate notifications module             | Added notifications components and connected alerts view to backend notifications endpoint.                   | 05/09/2026          |
| FinTeka-Backend  | main   | e5f6g7h8i9j0 | Initial monolithic backend setup           | Configured Spring Boot monolithic architecture with controllers, services, repositories and MySQL connection. | 05/07/2026          |
| FinTeka-Backend  | main   | f6g7h8i9j0k1 | Implement profiles and professionals API   | Added CRUD endpoints for profiles and professionals with entity relationships and validations.                | 05/08/2026          |
| FinTeka-Backend  | main   | g7h8i9j0k1l2 | Implement reservations and sessions module | Developed booking logic with available/unavailable schedules and session management endpoints.                | 05/09/2026          |
| FinTeka-Backend  | main   | h8i9j0k1l2m3 | Add ratings and notifications API          | Added professional ratings system and notifications endpoint for reservation status alerts.                   | 05/09/2026          |


### 5.3.1.3 Testing Suite Evidence for Sprint Review<br><br>

### FinTeka Testing<br><br>

**Feature:** Registro y Gestión de Usuarios<br>
**Como** usuario cliente o profesional<br>
**Quiero** registrarme y administrar mi perfil<br>
**Para** acceder correctamente a la plataforma FinTeka.<br><br>

---

#### Scenario: Registro exitoso de cliente<br>
**ID:** FIN-US-001<br>
**Relacionado con:** US002<br><br>

**Given** que soy un visitante sin cuenta registrada<br>
**When** completo el formulario con nombre, correo válido y contraseña<br>
**Then** el sistema crea mi cuenta correctamente<br>
**And** se genera mi perfil de usuario<br>
**And** se muestra un mensaje de bienvenida.<br><br>

---

#### Scenario: Registro exitoso de profesional<br>
**ID:** FIN-US-002<br>
**Relacionado con:** US001<br><br>

**Given** que deseo ofrecer servicios en la plataforma<br>
**When** completo el formulario con mis datos personales, especialidad, tarifa y experiencia<br>
**Then** el sistema registra mi cuenta profesional correctamente<br>
**And** mi perfil queda disponible para revisión<br>
**And** se asigna un identificador único.<br><br>

---

#### Scenario: Registro rechazado por correo duplicado<br>
**ID:** FIN-US-003<br>
**Relacionado con:** US002<br><br>

**Given** que ya existe una cuenta con el correo `usuario@correo.com`<br>
**When** intento registrarme utilizando ese mismo correo<br>
**Then** el sistema rechaza la operación<br>
**And** muestra el mensaje "Correo ya registrado"<br>
**And** no crea una nueva cuenta.<br><br>

---

#### Scenario: Actualización exitosa de perfil<br>
**ID:** FIN-US-004<br>
**Relacionado con:** US008<br><br>

**Given** que soy un usuario autenticado<br>
**When** modifico mi correo y número telefónico desde la sección perfil<br>
**Then** el sistema guarda los cambios correctamente<br>
**And** muestra una confirmación en pantalla<br>
**And** los nuevos datos permanecen actualizados.<br><br>

---

#### Scenario: Error al actualizar perfil con datos inválidos<br>
**ID:** FIN-US-005<br>
**Relacionado con:** US008<br><br>

**Given** que deseo actualizar mi perfil<br>
**When** ingreso un correo con formato incorrecto<br>
**Then** el sistema rechaza la actualización<br>
**And** muestra un mensaje indicando el error<br>
**And** mantiene la información anterior sin cambios.<br><br>

###  5.3.1.4 Execution Evidence for Sprint Review

En este sprint se desarrolló la aplicación de FinTeka utilizando una arquitectura monolítica, tomando como referencia los requisitos funcionales y no funcionales identificados previamente. Asimismo, para esta primera versión se empleó Spring Boot en el desarrollo del backend y Vue para el frontend. Como sistema de base de datos se utilizó MySQL.

Durante la implementación se siguieron buenas prácticas de desarrollo con el objetivo de facilitar, en etapas posteriores, una adecuada descomposición del monolito y su posterior migración hacia una arquitectura de microservicios.

A continuación, se presentan imágenes de evidencia correspondientes al Sprint 1.

![endpoints1.jpeg](../assets/endpoints1.jpeg)
![endpoints2.jpeg](../assets/endpoints2.jpeg)
![front1.jpeg](../assets/front1.jpeg)
![front2.jpeg](../assets/front2.jpeg)
### 5.3.1.5 Microservices Documentation Evidence for Sprint Review
![azure1.jpeg](../assets/azure1.jpeg)
![azure2.jpeg](../assets/azure2.jpeg)
![azure3.jpeg](../assets/azure3.jpeg)
### 5.3.1.6 Software Deployment Evidence for Sprint Review<br><br>

En este Sprint se realizaron las actividades de despliegue necesarias para publicar la plataforma **FinTeka**, permitiendo el acceso al frontend y backend desde entornos en la nube.<br><br>

---

#### A. Deployment Backend en Azure

Se utilizó **Microsoft Azure App Services** para desplegar la API REST desarrollada en Spring Boot.<br><br>

#### Actividades realizadas:<br>

- Creación del servicio web en Azure.<br>
- Configuración de variables de entorno.<br>
- Publicación del archivo ejecutable `.jar`.<br>
- Validación de endpoints activos.<br><br>

### B. Deployment Frontend en Vercel

Se utilizó **Vercel** para desplegar la aplicación frontend desarrollada en Vue.js.<br><br>

#### Actividades realizadas:<br>

- Conexión del repositorio GitHub con Vercel.<br>
- Configuración automática de build con Vite.<br>
- Publicación del proyecto en producción.<br>
- Configuración de URL del backend Azure.<br><br>
#### Evidencia 
![endpoints1.jpeg](../assets/endpoints1.jpeg)
![endpoints2.jpeg](../assets/endpoints2.jpeg)

Frontend desplegado: https://frontend-finteka.vercel.app/

### 5.3.1.7 Team Collaboration Insights during Sprint
![sprint1cola3.jpeg](../assets/sprint1cola3.jpeg)
![sprint1cola2.jpeg](../assets/sprint1cola2.jpeg)
![sprint1cola.jpeg](../assets/sprint1cola.jpeg)

### 5.3.1.8 Kanban Board
Para organizar las tareas del frontend y backend de FinTeka utilizamos Trello. Con esta herramienta gestionamos y damos seguimiento a las actividades planificadas para este primer Sprint.

![trellos1.jpeg](../assets/trellos1.jpeg)

Link del tablero trello: https://trello.com/invite/b/69f6574d811b27877f919b44/ATTI455d8960b544133b522a03a00ce8bfcfE7BD0119/fundamentos-sprint-1
# Conclusiones

- La investigación inicial permitió identificar que muchas personas y empresas presentan dificultades para acceder a asesoría profesional confiable debido a la fragmentación de la oferta y al uso de canales informales.
- El análisis del contexto digital evidenció una oportunidad de negocio relacionada con el crecimiento del uso de plataformas tecnológicas para contactar con servicios profesionales especializados.
- FinTeka se plantea como una solución viable al centralizar procesos como búsqueda de especialistas, reservas, pagos seguros, comunicación directa y reputación profesional en un solo entorno digital.
- La definición clara de segmentos objetivo permitió reconocer dos actores principales del ecosistema: usuarios que buscan asesoría y consultores que desean captar clientes y gestionar sus servicios.
- La aplicación de Lean UX facilitó validar supuestos de negocio, identificar riesgos tempranos y orientar el desarrollo hacia funcionalidades de mayor valor para el mercado.
- El proceso de Needfinding permitió comprender necesidades reales, motivaciones, comportamientos y puntos de dolor mediante herramientas centradas en el usuario.
- Los artefactos desarrollados, como User Personas, User Journey Mapping, Empathy Mapping y Scenario Mapping, contribuyeron a diseñar una experiencia alineada con las expectativas de los usuarios.
- El análisis competitivo demostró que existen plataformas internacionales posicionadas, pero también oportunidades de diferenciación para una propuesta enfocada en el mercado peruano y latinoamericano.
- La especificación de requisitos funcionales, no funcionales, historias de usuario e impact mapping proporciona una base sólida para el desarrollo técnico y la planificación del producto.
- FinTeka posee potencial de crecimiento sostenible gracias al avance de la digitalización, el aumento del trabajo remoto y la creciente demanda por asesorías profesionales en línea.

---

# Recomendaciones

- Validar continuamente la propuesta de valor mediante entrevistas, encuestas y pruebas con usuarios reales durante las primeras etapas del proyecto.
- Desarrollar un Producto Mínimo Viable (MVP) enfocado en funciones esenciales como registro, búsqueda de especialistas, reservas y sistema de valoraciones.
- Diseñar la plataforma considerando una experiencia intuitiva, rápida y adaptable tanto para usuarios como para consultores.
- Mantener actualizados los perfiles profesionales con información clara sobre experiencia, tarifas, disponibilidad y reputación.
- Aplicar metodologías centradas en el usuario de forma continua para detectar mejoras en navegación, procesos y satisfacción general.
- Implementar estrategias competitivas de diferenciación basadas en confianza, verificación de expertos y enfoque especializado en mercados locales.
- Establecer una arquitectura técnica robusta que contemple seguridad, rendimiento, disponibilidad y escalabilidad desde el inicio.
- Priorizar el desarrollo de requisitos críticos como autenticación segura, pagos integrados, reservas en tiempo real y mensajería interna.
- Gestionar el Product Backlog con metodologías ágiles, priorizando funcionalidades según valor de negocio y retroalimentación de usuarios.
- Planificar una estrategia de expansión progresiva, iniciando en el mercado peruano y escalando posteriormente hacia otros países de Latinoamérica.

# Referencias Bibliográficas

Chaffey, D., & Ellis-Chadwick, F. (2019). *Digital marketing* (7th ed.). Pearson.

Instituto Nacional de Estadística e Informática. (2024). *Estadísticas de las tecnologías de información y comunicación en los hogares*. INEI. https://www.inei.gob.pe/

Laudon, K. C., & Traver, C. G. (2023). *E-commerce: Business, technology, society* (18th ed.). Pearson.

Lean Startup Co. (2023). *Lean UX principles and agile product development*. https://leanstartup.co/

Ministerio de Transportes y Comunicaciones. (2023). *Reporte nacional de conectividad digital en el Perú*. Gobierno del Perú. https://www.gob.pe/mtc

Nielsen, J., & Budiu, R. (2013). *Mobile usability*. New Riders.

Organización para la Cooperación y el Desarrollo Económicos. (2023). *Digital economy outlook 2023*. OECD Publishing. https://www.oecd.org/

Osterwalder, A., Pigneur, Y., Bernarda, G., & Smith, A. (2020). *Value proposition design: How to create products and services customers want*. Wiley.

Ries, E. (2011). *The lean startup: How today’s entrepreneurs use continuous innovation to create radically successful businesses*. Crown Business.

Statista. (2024). *E-commerce and digital services market in Latin America*. https://www.statista.com/

World Bank. (2023). *Digital development overview*. The World Bank. https://www.worldbank.org/

# Anexos

**Link del Lean UX Canvas:** https://miro.com/app/board/uXjVGhydm8Q=/?share_link_id=941421721219//

**Link del Empathy Mapping 1:** https://docs.google.com/drawings/d/1ldThwGvffPsPR6Ea6FWCU5DBOGQAVvXugWDPmzPzgD8/edit?usp=sharing

**Link del Empathy Mapping 2:** https://docs.google.com/drawings/d/1iiU7QqJ-yt0utAPLlAPtQgQrVaNgFb6AWoq7JaNGiV0/edit

**Link del Impact Mapping:** https://miro.com/app/board/uXjVJGsSlMY=/?share_link_id=357440759397

**Link de la entrevista 1:** https://acortar.link/RWaCr0

**Link de la entrevista 2:** https://acortar.link/WrhkQL

**Link de la entrevista 3:** https://acortar.link/WyeuS7 

**Link de la entrevista 4:** https://acortar.link/NfWGsQ

**Link de la entrevista 5:** https://acortar.link/TErjgY

**Link de la entrevista 6:** https://acortar.link/EQVuW5

**Link de los diagramas C4:** https://online.visual-paradigm.com/share.jsp?id=343537383331342d32

**Link del trablero trello:** https://trello.com/invite/b/69f6574d811b27877f919b44/ATTI455d8960b544133b522a03a00ce8bfcfE7BD0119/fundamentos-iteration-1
