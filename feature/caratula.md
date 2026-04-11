<div align="center">
<img src="../assets/upc_logo.png"alt="UPC Logo" width="200"/>

# UNIVERSIDAD PERUANA DE CIENCIAS APLICADAS
### Carrera: Ingeniería de Software
### Ciclo: 7mo ciclo
### Fundamentos de Arquitectura de Software - Presencial (1ASI0657)
### NRC: 7943
### Profesor: Ernesto Ocampo Tello
## Informe de TB1

## Startup: 
## Producto: MealFlow 

### Relación de integrantes:

<div style="text-align: center;">

| **Código** | **Apellidos y Nombres**               |
| :--------: | :------------------------------------ |
| U202310425 | Aguirre Castillo, Sergio Cesar        |
| U202220659 | Mamani Marca, Gabriel Cristian        |
| U20201f846 | Oshiro Yamashita, Daiki Oscar         |
</div>

### Abril,2026

---
</div>

## Registro de Versiones del Informe

| Versión |  Fecha     |                                       Autor                                   |            Descripción de modificación                                                   |
| :-----: | :--------: | :---------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------: |
| TB1     | 04/06/2026 | Todos los integrantes del equipo                                              |                                                                                          |

# Contenido

## Índice

Tabla de contenidos

- [Registro de versiones del informe](#registro-de-versiones-del-informe)

- [Project Report Collaboration Insights](#project-report-collaboration-insights)

- [Contenido](#contenido)

- [Student Outcome](#student-outcome-1)

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
  - [3.2. User Stories](#32-user-stories)
  - [3.3. Impact Map](#33-impact-map)
  - [3.4. Product Backlog](#34-product-backlog)
- [Capítulo IV: Product Architecture Design]()
  - [4.1. Desing Concepts, ViewPoints & ER Diagrams](#41-desing-concepts-viewpoints-&-er-diagrams)
    - [4.1.1. Principles Statements](#411-principles-statements)
    - [4.1.2. Approaches Statements Architectural Styles & Patterns](#412-approaches-statements-architectural-styles-&-patterns)
    - [4.1.3. Context Diagram](#413-context-diagrams)
    - [4.1.4. Approach driven ViewPoints Diagrams](#414-approach-driven-viewpoints-diagrams)
    - [4.1.5. Relational/Non Relational Database Diagram](#415-relational-non-relational-database-diagrams)
    - [4.1.6. Design Patterns](#416-design-patterns)
    - [4.1.7. Tactics](#417-tactics)
  - [4.2. Architectural Drivers](#42-architectural-drivers)


- [Capítulo V: Product Implementation, Validation & Deployment]()
  - [5.1. Testing Suites & General Patterns](#51-testing-suites-&-general-patterns)
    - [5.1.1. Backend Application Core Testing Suite](#511-backend-application-core-testing-suite)
    - [5.1.2. Pattern Based Backend Application(s)](#512-pattern-based-backend-application(s))
    - [5.1.3. Pattern Based Custom Software Library](#513-pattern-based-custom-software-library)
    - [5.1.4. Framework Pattern Driven Refactoring Report](#514-framework-pattern-driven-refactoring-report)
  - [5.2. Software Configuration Management](#52-software-configuration-management)
    - [5.2.1. Software Development Environment Configuration](#521-software-development-environment-configuration)
    - [5.2.2. Source Code Management](#522-source-code-management)
    - [5.2.3. Source Code Style Guide & Conventions](#523-source-code-style-guide-&-conventions)
    - [5.2.4. Software Deployment Configuration](#524-software-deployment-configuration)
  - [5.3. Microservices Implementation](#53-microservices-implementation)
    - [5.2.1. Sprint 1](#521-sprint-1)
      - [5.2.1.1. Sprint Backlog 1](#5211-sprint-backlog-1)
      - [5.2.1.2. Development Evidence for Sprint Review](#5212-development-evidence-for-sprint-review)
      - [5.2.1.3. Testing Suite Evidence for Sprint Review](#5213-testing-suite-evidence-for-sprint-review)
      - [5.2.1.4. Execution Evidence for Sprint Review](#5214-execution-evidence-for-sprint-review)
      - [5.2.1.5. Microservices Documentation Evidence for Sprint Review](#5215-microservices-documentation-evidence-for-sprint-review)
      - [5.2.1.6. Software Deployment Evidence for Sprint Review](#5216-software-deployment-evidence-for-sprint-review)
      - [5.2.1.7. Team Collaboration Insights during Sprint](#5217-team-collaboration-insights-during-sprint)
      - [5.2.1.8. Kanban Board](#5218-kanban-board)
    - [5.2.2. Sprint 2](#522-sprint-2)
      - [5.2.2.1. Sprint Backlog 2](#5221-sprint-backlog-2)
      - [5.2.2.2. Development Evidence for Sprint Review](#5222-development-evidence-for-sprint-review)
      - [5.2.2.3. Testing Suite Evidence for Sprint Review](#5223-testing-suite-evidence-for-sprint-review)
      - [5.2.2.4. Execution Evidence for Sprint Review](#5224-execution-evidence-for-sprint-review)
      - [5.2.2.5. Microservices Documentation Evidence for Sprint Review](#5225-microservices-documentation-evidence-for-sprint-review)
      - [5.2.2.6. Software Deployment Evidence for Sprint Review](#5226-software-deployment-evidence-for-sprint-review)
      - [5.2.2.7. Team Collaboration Insights during Sprint](#5227-team-collaboration-insights-during-sprint)
      - [5.2.2.8. Kanban Board](#5228-kanban-board)
    - [5.2.3. Sprint 3](#523-sprint-3)
      - [5.2.3.1. Sprint Backlog 3](#5231-sprint-backlog-3)
      - [5.2.3.2. Development Evidence for Sprint Review](#5232-development-evidence-for-sprint-review)
      - [5.2.3.3. Testing Suite Evidence for Sprint Review](#5233-testing-suite-evidence-for-sprint-review)
      - [5.2.3.4. Execution Evidence for Sprint Review](#5234-execution-evidence-for-sprint-review)
      - [5.2.3.5. Microservices Documentation Evidence for Sprint Review](#5235-microservices-documentation-evidence-for-sprint-review)
      - [5.2.3.6. Software Deployment Evidence for Sprint Review](#5236-software-deployment-evidence-for-sprint-review)
      - [5.2.3.7. Team Collaboration Insights during Sprint](#5237-team-collaboration-insights-during-sprint)
      - [5.2.3.8. Kanban Board](#5238-kanban-board)
    - [5.2.4. Sprint 4](#524-sprint-4)
      - [5.2.4.1. Sprint Backlog 4](#5241-sprint-backlog-4)
      - [5.2.4.2. Development Evidence for Sprint Review](#5242-development-evidence-for-sprint-review)
      - [5.2.4.3. Testing Suite Evidence for Sprint Review](#5243-testing-suite-evidence-for-sprint-review)
      - [5.2.4.4. Execution Evidence for Sprint Review](#5244-execution-evidence-for-sprint-review)
      - [5.2.4.5. Microservices Documentation Evidence for Sprint Review](#5245-microservices-documentation-evidence-for-sprint-review)
      - [5.2.4.6. Software Deployment Evidence for Sprint Review](#5246-software-deployment-evidence-for-sprint-review)
      - [5.2.4.7. Team Collaboration Insights during Sprint](#5247-team-collaboration-insights-during-sprint)
      - [5.2.4.8. Kanban Board](#5248-kanban-board)
  - [5.4. Microservices Deployment](#54-microservices-deployment)
    - [5.3.1. Cloud Architecture Diagram](#531-cloud-architecture-diagram)
    - [5.3.2. Cloud Architecture Deployment](#532-cloud-architecture-deployment)
- [Conclusiones](#conclusiones)
  - [Conclusiones y recomendaciones](#conclusiones-y-recomendaciones)
  - [Video About-The-Team](#video-about-the-team)
- [Referencias Bibliográficas](#referencias-bibliograficas)
- [Anexos](#anexos)
- [Link](#links)

## Student Outcome

Objetivo general, ABET – EAC - Student Outcome 7: Aprendizaje Continuo y Autónomo.

|Criterio específico|Acciones realizadas|Conclusiones|
|---|---|---|
|Actualiza conceptos y conocimientos necesarios para su desarrollo profesional y en especial para su proyecto en soluciones de software.|
Daiki Oscar Oshiro Yamashita <br>**TB1**: Actualicé y apliqué conocimientos de UX y metodologías ágiles durante el desarrollo de Finteka, elaborando el User Task Matrix, Empathy Mapping, As-is Scenario Mapping y revisando el Product Backlog para mejorar la definición del proyecto.<br> |
Daiki Oscar Oshiro Yamashita <br>**TB1**: La actualización constante de conocimientos permitió mejorar el análisis, organización y planificación del proyecto de software.<br> |
|Reconoce la necesidad del aprendizaje permanente para el desempeño profesional y el desarrollo de proyectos ensoluciones de software.|
Daiki Oscar Oshiro Yamashita <br>**TB1**: Reconocí la necesidad del aprendizaje continuo al investigar nuevas técnicas de análisis de usuarios, priorización de requerimientos y gestión ágil, aplicándolas en el proyecto Finteka para mejorar la calidad de la solución propuesta.<br> |
Daiki Oscar Oshiro Yamashita <br>**TB1**: El aprendizaje permanente es clave para adaptarse a nuevas metodologías y desarrollar soluciones más eficientes e innovadoras.<br> |
