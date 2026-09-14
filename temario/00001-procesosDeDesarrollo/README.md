# Evolución de los procesos de desarrollo de software

## ¿Por qué?

[Un proceso de desarrollo software es un flujo de trabajo](/temario/contenidos/00000-acercaDe.md#cómo), no una simple lista de roles, actividades y artefactos. Ese flujo se puede organizar de formas muy distintas según cuándo y cómo se fijan los requisitos, cuánto se itera y cuánto se documenta. Conocer esas formas — y sus consecuencias — es lo que permite elegir con criterio, más adelante, cómo se organiza el trabajo en esta asignatura (RUP) y por qué existen alternativas.

## ¿Qué?

### Clasificación de metodologías

|Familia|Metodologías|
|-|-|
|**Sin requisitos**|Top-Down · Bottom-Up|
|**Con requisitos**|Cascada · V (doble cascada)|
|**Iterativas**|Rational Unified Process · Ágiles (XP, Scrum, Crystal, Kanban...)|

### Cronología

1. **Crisis del software** (años 60-70): proyectos que incumplen ámbito, tiempo y coste de forma sistemática.
2. **Metodología en Cascada**: primera respuesta formal a la crisis — planificar y documentar antes de codificar.
3. **Desarrollo Iterativo**: respuesta a la rigidez de la cascada — construir en incrementos con retroalimentación temprana. De aquí derivan tanto **Rational Unified Process** como **Scrum**.
4. **Manifiesto Ágil** (2001): síntesis de los valores comunes a las metodologías iterativas ligeras (XP, Scrum, Crystal...).
5. **Craftsmanship / Basic-Agile-Open Unified Process / ...**: evoluciones posteriores que insisten en la disciplina técnica (Craftsmanship) o en formalizar variantes del proceso unificado (AUP, OpenUP).

*Diagrama pendiente (PlantUML): cronología en árbol Crisis del Software → Cascada / Desarrollo Iterativo → RUP / Scrum → Manifiesto Ágil → Craftsmanship / Unified Process variants.*

*Diagrama pendiente (PlantUML): curva de popularidad 1960-2020 de Cascada (auge y declive), RUP y Ágil (crecimiento sostenido).*

## Metodología en Cascada

|Año|Autores|Publicación|Referencia|
|-|-|-|-|
|1911|F.W. Taylor|Producción en Cadena|Organización industrial del trabajo mediante la división de tareas del proceso de producción, para aumentar la productividad y evitar el control que el obrero podía tener sobre los tiempos de producción|
|1970|W.W. Royce|*Managing the development of large software systems*|IEEE WESCON Proceedings, pp. 1-9|

Fases secuenciales, sin retroceso: Requisitos → Diseño → Implementación → Pruebas → Despliegue → Mantenimiento.

|Ventajas|Desventajas|
|-|-|
|Modelos fáciles de implementar y entender, conocidos y utilizados con frecuencia|Cualquier error detectado en la etapa de prueba conduce necesariamente al rediseño y nueva programación del código afectado, aumentando los costes del desarrollo|
|Promueven una metodología de trabajo efectiva: definir antes que diseñar, diseñar antes que codificar|No hay método para gran parte del mantenimiento|

> Si el 90% o más de los requisitos de tu sistema se espera que sean estables a lo largo de la vida del proyecto, entonces aplicar una política dirigida por los requisitos es una oportunidad apropiada de dar razonablemente una solución óptima.
>
> — Booch, *Object Solutions*

> Otros grados menores de estabilidad en los requisitos requieren un enfoque de desarrollo diferente para dar un valor tolerable del coste total.
>
> — Booch, *Object Solutions*

|Aportaciones|Excesos|
|-|-|
|Formalización de disciplinas: metodologías Jackson, Warnier, Yourdon, DeMarco...|Enfoque en las primeras disciplinas (gestión, requisitos, análisis...), certificaciones, documentación, "abandonando" al humilde programador|
|Formalización de técnicas: DFD, E/R, acoplamiento aferente/eferente, cohesión, granularidad, métricas del software, diseño de pruebas de caja negra y caja blanca...|Planificaciones absurdas, control del calendario, *Big Design Up Front* (BDUF)|
|Herramientas CASE de gestión, requisitos, análisis, diseños... y generación de código|Excesiva documentación de dudosa calidad|
||Mantenimiento sin método, a veces el 80% del proyecto|

## Desarrollo Iterativo

### Leyes del Cambio Continuo (Lehman y Belady)

|Ley|Enunciado|
|-|-|
|**Del Cambio Continuo**|Un programa que se usa en un ámbito del mundo real necesariamente debe cambiar o convertirse cada vez en menos útil y menos satisfactorio para el usuario|
|**Del Crecimiento Continuado**|La funcionalidad ofrecida por los sistemas tiene que crecer continuamente para mantener la satisfacción de los usuarios|
|**De la Complejidad Creciente**|Debido a que los programas cambian por evolución, su estructura se convierte en más compleja a menos que se hagan esfuerzos activos para evitar este fenómeno|
|**Del Decremento de la Calidad**|La calidad de los sistemas software comenzará a disminuir a menos que dichos sistemas se adapten a los cambios de su entorno de funcionamiento|

### Cronología de las metodologías iterativas

|Año|Autores|Publicación|Aportación|
|-|-|-|-|
|1950|W.A. Shewhart, W.E. Deming|Ciclos de Deming-Shewhart|Espiral de mejora continua en 4 pasos (PDCA: Plan-Do-Check-Act), aplicada a calidad, medioambiente, seguridad...|
|1960|NASA|Proyecto Mercury|Primer programa de vuelo espacial humano de EE. UU., desarrollado de forma incremental|
|1965~|Taichi Ohno|Kanban (Toyota)|*Just-in-time manufacturing*; radiadores de información: burndowns, tareas...|
|1986|H. Takeuchi, I. Nonaka|*The New Product Development Game* (Harvard Business Review)|Origen del término **Scrum** (*melé*)|
|1988|B.W. Boehm|*A Spiral Model of Software Development and Enhancement* (IEEE, vol. 21, nº 5)|Modelo en espiral: ciclos de determinación de objetivos, análisis de riesgos, desarrollo y planificación de siguientes fases|
|1990|A. Cockburn|Crystal, marco metodológico (IBM)|Familia de metodologías graduadas por criticidad (vidas en juego) y tamaño de equipo (Clear, Yellow, Orange, Red, Maroon)|
|1991|J. Martin|*Rapid Application Development* (RAD)|Desarrollo rápido de aplicaciones|
|1997|J. De Luca, P. Coad|*Feature-driven development*|Modelado Java con UML por colores|
|1999|J. Highsmith|*Adaptive Software Development*|Desarrollo adaptativo|
|2003|J. Stapleton|*DSDM: The Method in Practice*|Dynamic Systems Development Method|

### Iteración e incremento

|Iteración / Sprint|Incremento|
|-|-|
|Conjunto distinto de actividades llevado a cabo de acuerdo con un plan dedicado y criterios de evaluación que se traduce en una entrega, ya sea interna o externa|Una parte del sistema pequeña y manejable, por lo general la diferencia entre dos construcciones sucesivas|

> Planificar de un poco. Especificar, diseñar e implementar un poco. Integrar, probar y ejecutar un poco en cada iteración.
>
> — Booch

|Entrega interna|Entrega externa|
|-|-|
|No expuesta a clientes ni usuarios; solo para el proyecto y sus miembros|Expuesta a clientes y usuarios externos al proyecto y a sus miembros|

|Ventajas|Desventajas|
|-|-|
|Permite la participación del usuario desde fechas tempranas para corregir desviaciones de sus necesidades|Dificultad para gestionar a los miembros del equipo en una iteración cerrada o con varias iteraciones abiertas en paralelo|
|Eleva el ánimo del equipo con las entregas externas que superan las pruebas de aceptación||
|Localiza con facilidad errores de programación y diseño en el incremento producido en la iteración vigente||

De esta corriente derivan tanto [**RUP**](/temario/00002-rup.md) como las metodologías ágiles ligeras — **Scrum** y **eXtreme Programming** — que se resumen a continuación.

## Scrum

|Año|Autor|Publicación|
|-|-|-|
|1995|K. Schwaber|*The Scrum development process* (OOPSLA '95)|

> Scrum es un marco ligero que ayuda a las personas, equipos y organizaciones a generar valor a través de soluciones adaptables para problemas complejos.
>
> — Ken Schwaber y Jeff Sutherland, *La Guía Scrum*

Deliberadamente incompleto: solo gestión, sin ningún aspecto técnico. Roles (Product Owner, Scrum Master, equipo), artefactos (Product Backlog, Sprint Backlog) y eventos (Sprint Planning, Daily Scrum, Sprint Review, Sprint Retrospective) organizados en sprints de 1 a 4 semanas.

## eXtreme Programming

|Año|Autor|Publicación|
|-|-|-|
|1999|Kent Beck|*Extreme Programming Explained: Embrace Change*|
|1999|Martin Fowler|*Refactoring: Improving the Design of Existing Code*|
|2000|Ron Jeffries|*Extreme Programming Installed*|
|2002|Kent Beck|*Test Driven Development: By Example*|

> Es un método ligero, eficiente, de bajo riesgo, predecible, científico y divertido para que equipos de tamaño mediano a pequeño (de 10 a 2 programadores) desarrollen software frente a requisitos imprecisos y muy cambiantes.
>
> — Kent Beck

A diferencia de Scrum, sí es prescriptivo sobre la forma técnica de entregar valor: *pair programming*, *test-driven development*, *refactoring*, integración continua.

## ¿Para qué?

RUP y Scrum+XP resuelven el mismo problema — desarrollo iterativo con requisitos cambiantes — con **énfasis distintos**, no con objetivos contrapuestos:

|Énfasis de RUP|Énfasis de Scrum+XP|
|-|-|
|Proyectos pequeños, medianos y grandes, sin límite de desarrolladores ni duración|Proyectos pequeños/medianos (40.000-50.000 líneas), 10 desarrolladores y 15 meses como máximo|
|Iteraciones de pocas semanas a pocos meses|Sprints de 2 o 3 semanas|
|Equipo variable, crece y decrece con el proyecto|Equipo constante durante todo el proyecto|
|Planifica con casos de uso priorizados por riesgo|Planifica con historias de usuario priorizadas por retorno de inversión|
|Arquitectura con diseño suficiente, previo al desarrollo|Arquitectura emergente, rediseñada con TDD y refactoring|
|Roles especializados: analista, arquitecto, integrador...|Desarrolladores multidisciplinares por funcionalidad|
|Gestión de documentación pesada o ligera según el proyecto|Poca documentación: la mejor documentación es el código|

Elegir uno u otro — o combinarlos — es una decisión de proyecto, no una cuestión de dogma. Ver la [comparativa detallada entre RUP y Scrum+XP](articulos/rupVsScrumXP.md).

## ¿Cómo?

En esta asignatura se sigue **RUP** como proceso de referencia — ver [RUP: Proceso Unificado de Desarrollo](/temario/00002-rup.md) — precisamente por lo que se acaba de ver aquí: es la metodología iterativa con mayor cobertura de disciplinas técnicas y de gestión, lo que la hace más adecuada para aprender el ciclo completo de un proyecto software antes de especializarse en un marco ágil concreto.

## ¿Y ahora qué?

### Profundización

- [Comparativa detallada entre RUP y Scrum+XP](articulos/rupVsScrumXP.md): correspondencia disciplina a disciplina, tabla de actividades equivalentes y las citas de John Smith sobre el falso enfrentamiento "proceso pesado vs. proceso ligero".

### Bibliografía

|Obra|Autor(es)|
|-|-|
|*Object Solutions: Managing the Object-Oriented Project*|Grady Booch|
|*Object Oriented Analysis and Design with Applications*|Grady Booch|
|*The Unified Modeling Language User Guide*|Grady Booch|
|*The Mythical Man-Month: Essays on Software Engineering*|Frederick P. Brooks|
|*Extreme Programming Explained: Embrace Change*|Kent Beck, Cynthia Andres|
|*Refactoring: Improving the Design of Existing Code*|Martin Fowler, Kent Beck, John Brant, William Opdyke, Don Roberts|
|*UML Distilled: A Brief Guide to the Standard Object Modeling Language*|Martin Fowler, Kendall Scott|
|*Patrones de diseño*|Erich Gamma et al.|
|*Clean Code: A Handbook of Agile Software Craftsmanship*|Robert C. Martin|
|*Object-Oriented Software Construction*|Bertrand Meyer|

> Contenido adaptado de la sesión "Proceso de Desarrollo Software" (Universo de Santa Tecla) — Prof. Luis Fernández Muñoz.
