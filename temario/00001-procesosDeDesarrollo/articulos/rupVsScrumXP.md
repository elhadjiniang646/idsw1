# Comparativa entre RUP y Scrum+XP

> Continúa [Evolución de los procesos de desarrollo de software](../README.md).

## Fases equivalentes

|Fases de RUP (por perfil del proyecto)|Fases de Scrum/XP (ciclo trimestral)|
|-|-|
|Inicio|Exploración / Sprint 0?|
|Elaboración|Planificación / Sprint 0?|
|Construcción|Producción|
|Transición|Mantenimiento|
||Muerte|

## Disciplinas y actividades equivalentes

|Disciplinas en RUP|Actividades en Scrum/XP|
|-|-|
|Requisitos y Análisis|Escuchar|
|Diseño|Diseñar|
|Implementación|Programar|
|Pruebas|Probar|

|Disciplina de Requisitos (RUP)|Sprint Planning (Scrum)|
|-|-|
|Casos de Uso|Historias de Usuario|
|Disciplina de Análisis|Tareas: *To Do*, *Doing*, *Done* del Burndown|

|Test-Last / Test-First / Test-Driven Development|Test-Driven Development (Scrum/XP)|
|-|-|
|Disciplina de Diseño|Disciplina de Pruebas / Diseño de la interfaz del SUT (*rojo*)|
|Disciplina de Pruebas|Disciplina de Programación (*verde*)|
|Disciplina de Programación|Disciplina de Diseño: *refactoring*|

## Tabla de correspondencias por actividad

|Actividad RUP|Concepto ágil|Fuente ágil|
|-|-|-|
|Modelo del Dominio|Contextos, *Values*, Entidades...|Domain-Driven Design|
|Encontrar Actores y Casos de Uso|Roles e Historias de Usuario|Scrum / eXtreme Programming|
|Priorizar Casos de Uso por Riesgo|Priorización por Retorno de Inversión|Scrum / eXtreme Programming|
|Detallar Caso de Uso|Historias de Usuario, Aceptación y Conversación|Scrum / eXtreme Programming|
|Estructurar Casos de Uso|TDD, Refactoring|Scrum / eXtreme Programming|
|Prototipar Interfaz de Usuario|Historias de Usuario, Prototipo de Interfaz|Scrum / eXtreme Programming|
|Análisis de la Arquitectura|Sprint 0|¿?|
|Análisis de Caso de Uso|Sprint Planning|Scrum / eXtreme Programming|
|Análisis de Clase|TDD, Refactoring|eXtreme Programming|
|Análisis de Paquete|TDD, Refactoring|eXtreme Programming|
|Diseño de la Arquitectura|Sprint 0 y *Spike*|¿? / eXtreme Programming|
|Diseño de Caso de Uso|TDD, escuelas Clásica vs. Londres|eXtreme Programming|
|Diseño de Clase|TDD, Refactoring|eXtreme Programming/*Growing Object-Oriented Software*|
|Diseño de Paquete|TDD, Refactoring|eXtreme Programming|
|Implementar la Arquitectura|Arquitectura emergente|eXtreme Programming|
|Integración de Sistemas|Sprint Backlog|Scrum / eXtreme Programming|
|Implementar Clase|TDD, código mínimo|eXtreme Programming|
|Pruebas Unitarias|TDD, prueba primero|eXtreme Programming|
|Implementar Subsistema|—|eXtreme Programming|
|Planificar / Diseñar / Implementar Pruebas|Integración continua|Continuous Delivery / Análisis y Diseño Orientado a Objetos|
|Realizar Pruebas de Integración y de Sistemas, Evaluar Pruebas|Integración continua|Continuous Delivery / Análisis y Diseño Orientado a Objetos|
|Apertura de la Iteración|Planificación del Sprint|Scrum / eXtreme Programming|
|Realización de la Iteración (dirigida por casos de uso y riesgos)|Realización del Sprint (dirigida por el retorno de inversión de las historias de usuario)|Scrum / eXtreme Programming|
|Cierre de la Iteración|Demo del Sprint|Scrum / eXtreme Programming|
|Cierre/Apertura de Fase|Retrospectiva del Sprint|Scrum / eXtreme Programming|

## Énfasis de cada enfoque

|Énfasis de RUP|Énfasis de Scrum+XP|
|-|-|
|Pequeños/medianos/grandes proyectos (millones de líneas de código), sin límite de desarrolladores ni duración|Pequeños/medianos proyectos (40.000-50.000 líneas de código), con 10 desarrolladores máximo durante 15 meses como máximo|
|Iteraciones entre pocas semanas y pocos meses, dependiendo del proyecto|Sprints de 2 o 3 semanas|
|Equipo variable en el proyecto, crece y decrece|Equipo constante, se mantiene|
|Entrevistas con el cliente en cada iteración, cada vez menos, y en cada entrega|Entrevistas con el cliente *in situ* durante toda o parte del proyecto|
|Planifica con Casos de Uso priorizados por riesgos técnicos, políticos... del proyecto|Planifica con Historias de Usuario priorizadas por el retorno de inversión (ROI) del cliente|
|Diseño de la Arquitectura con diseño suficiente (análisis) previo al desarrollo|Arquitectura emergente según se rediseña (TDD y refactoring)|
|Roles especializados por desarrollador: analista de sistemas, arquitecto del software, ingeniero de componentes, integrador de sistemas...|Desarrolladores multidisciplinares por funcionalidad: *product owner*, equipo, gestor/*scrum master*|
|Gestión de documentación de requisitos, análisis y diseño: pesadas o ligeras|Poca documentación, porque la mejor documentación es el código: ligeras|
|Artefactos/documentación: entre 23 y más de 100. Modelo del Dominio; 4+1 vistas (Casos de Uso, Diseño, Implementación, Despliegue, Procesos). Equipo jerarquizado|Beneficio mutuo, con 30 artefactos (historias de usuario, restricciones, tareas, pruebas de aceptación, metáforas, diseño...). Equipo como una unidad, programación por pares, propiedad compartida del código, el equipo debe estar junto, radiadores de información, horas razonables para ser productivo|

Las analogías habituales — RUP como una orquesta sinfónica dirigida, Scrum+XP como un combo de jazz que improvisa sobre una estructura mínima — ilustran la diferencia de gestión, no una diferencia de calidad técnica entre ambos enfoques.

## Sobre el falso enfrentamiento "proceso pesado vs. proceso ligero"

> Etiquetar RUP como peso pesado y XP como liviano sin más calificaciones perjudica a ambos al oscurecer lo que cada uno pretendía hacer. Y, cuando se hace de manera peyorativa, es simplemente una postura sin sentido. Son las implementaciones de estos procesos las que serán "pesadas" o "livianas", y deberían ser tan pesadas o livianas como las circunstancias lo requieran.
>
> — John Smith, *A Comparison of the IBM Rational Unified Process and eXtreme Programming*

> XP no está libre de forma, no todo vale: se enfoca estrictamente en un aspecto particular del desarrollo de software y una forma de entregar valor, y es bastante prescriptivo sobre la forma en que se debe lograr.
>
> — John Smith, *A Comparison of the IBM Rational Unified Process and eXtreme Programming*

> La cobertura de RUP es mucho más amplia e igual de profunda, lo que explica su aparente "tamaño". Sin embargo, en el nivel micro del proceso, RUP ocasionalmente permite y ofrece alternativas igualmente válidas donde XP no lo hace; por ejemplo, la práctica de la programación en pareja. Esto no pretende ser una crítica a XP; simplemente una ilustración de cómo XP, como su nombre lo indica, ha reducido su enfoque.
>
> — John Smith, *A Comparison of the IBM Rational Unified Process and eXtreme Programming*

## Síntesis

Todo proceso de desarrollo — sea RUP, Scrum, XP o cualquier otro — gestiona la misma tensión entre seis fuerzas: **Gestión** de un proyecto acotado por **Tiempo**, **Coste**, **Riesgo** y **Cambio**, frente a unos **Requisitos** que se satisfacen mediante **Programación**, **Pruebas**, **Diseño** y **Despliegue**. Lo que distingue a cada metodología es en qué orden y con qué énfasis se atiende a cada una de esas fuerzas — no cuáles de ellas decide ignorar.

*Diagrama pendiente (PlantUML): estrella de seis puntas con Gestión/Tiempo-Coste/Riesgo-Cambio/Requisitos en el triángulo exterior y Programación/Pruebas/Diseño/Despliegue en el interior.*
