# Disciplinas del Software

## ¿Por qué?

La [inefectividad, ineficacia e ineficiencia del proyecto software](/temario/contenidos/00000-acercaDe.md#por-qué) tiene, en el fondo, cuatro fuentes de complejidad distintas, y cada una exige su propia disciplina para dominarla:

|Complejidad|Causa|Disciplina que la aborda|
|-|-|-|
|**Del dominio del problema**|Los requisitos son a menudo contradictorios, ambiguos u omitidos, y cambian durante el propio desarrollo|Requisitos|
|**De las limitaciones de la capacidad humana**|Número mágico de Miller (7±2): no existen estándares de industria comparables a los de la construcción, así que el desarrollo sigue siendo trabajo intensivo|Análisis, en busca de mantenibilidad|
|**Del comportamiento de los sistemas discretos**|Cientos o miles de variables, varios hilos de control: es imposible para una sola persona seguir todo el estado de la aplicación a la vez (crecimiento exponencial)|Diseño, en busca de reusabilidad; Pruebas y Despliegue|
|**De gestionar el propio proceso de desarrollo**|Sistemas de cientos de miles o millones de líneas de código, frente a los pocos miles que marcaban los límites de la ingeniería del software hace unas décadas|Gestión|

> Los problemas en los proyectos se pueden remontar a alguien que no dijo a otro algo importante. La mala comunicación no sucede por casualidad.
>
> — Kent Beck, *eXtreme Programming*

El software es, ante todo, un problema de comunicación entre cliente, analista de negocio y desarrollador — como el teléfono escacharrado.

## ¿Qué?

||||
|-|-|-|
Ingeniería de software es la aplicación práctica del conocimiento científico al diseño y construcción de programas de computadora y a la documentación asociada requerida para desarrollarlos, operarlos y mantenerlos. Se conoce también como desarrollo de software o producción de software.|El software es sagrado — y lo importante requiere de un ritual.|Las Disciplinas son contenedores usados para organizar las actividades del proceso, que representan una partición de todos los roles, artefactos y actividades en agrupaciones lógicas por áreas de asuntos o especialidades.
|<div align=right>*Boehm, 1976*</div>|<div align=right>*Booch / sentido común*|<div align=right>*Booch*

<div align=center>

|Disciplinas técnicas|Disciplinas de soporte|
|-|-|
|Modelado del Dominio|Gestión del Proyecto|
|Requisitos|Gestión del Ecosistema (forja del *devop* para desarrollo colaborativo)|
|Análisis|Entorno|
|Diseño|Configuración y Gestión de Cambios|
|Implementación||
|Pruebas||
|Despliegue||

</div>

## ¿Para qué?

Un proyecto que separa correctamente estas disciplinas tiende a la [efectividad, eficacia y eficiencia](/temario/contenidos/00000-acercaDe.md#para-qué) — no por acumular heurísticas sueltas, sino por disciplina real:

> No se convierte uno en maestro del software aprendiendo una lista de heurísticas. El profesionalismo y la maestría provienen de valores que impulsan las disciplinas.
>
> — Martin Fowler, *Refactoring*

## ¿Cómo?

### Disciplina de Requisitos

Dirigir el desarrollo hacia el **sistema correcto**, describiendo los requisitos de forma que se alcance el acuerdo entre clientes, usuarios y desarrolladores sobre lo que el sistema debería hacer: establecer y mantener ese acuerdo, definir los límites del sistema, y proveer las bases para planificar y estimar el desarrollo.

|Requisitos funcionales|Requisitos no funcionales|
|-|-|
|Enfocados en el problema: la correspondencia entre entradas (ratón, teclado, interfaces de comunicaciones) y salidas|Enfocados en la solución: restricciones sobre eficiencia, usabilidad, interoperabilidad, seguridad, mantenibilidad, lenguaje, protocolos, plataformas...|

**Artefactos**: diagramas de Casos de Uso y de Estados, Historias de Usuario, Prototipo de Interfaz, Interfaz de Comunicaciones.

### Disciplina de Análisis

Analizar los requisitos mediante su refinamiento y estructura, para lograr una comprensión más precisa de ellos, fácil de mantener y que ayude a estructurar el sistema: dar una especificación más precisa, describir en el lenguaje de los desarrolladores, y estructurar los requisitos facilitando su comprensión y su cambio.

**Artefactos**: diagrama de Clases MVC, diagrama de Colaboración, partición en clases y en métodos.

|Requisitos|Análisis|
|-|-|
|Descrito usando el lenguaje del cliente|Descrito usando el lenguaje de los desarrolladores (diagramas de clases)|
|Visión externa del sistema|Visión interna del sistema|
|Estructurado por requisitos: da estructura a la vista externa|Estructurado por clases estereotipadas y paquetes: da estructura a la vista interna|
|Contrato entre clientes y desarrolladores sobre lo que el sistema debería hacer|Usado por los desarrolladores para decidir qué forma debería tener el sistema|
|Contiene redundancias e inconsistencias entre los requisitos|No debería contener redundancias ni inconsistencias|
|Captura la funcionalidad del sistema, incluida la arquitectónicamente significativa|Esboza cómo realizar esa funcionalidad|

### Disciplina de Diseño

Desarrollar enfocándose en los requisitos no funcionales y en el dominio de la solución, preparando la implementación y las pruebas: comprender a fondo las limitaciones de lenguajes de programación, reutilización de componentes, sistemas operativos, distribución y concurrencia, bases de datos, interfaz de usuario, gestión de transacciones...

**Artefactos**: diagramas de Despliegue, diagramas de Secuencia.

|Análisis|Diseño|
|-|-|
|Modelo conceptual: abstracción del sistema que evita cuestiones de implementación|Modelo físico: esbozo de la implementación|
|Menos formal|Más formal|
|Genérico, aplicable a varios diseños concretos|Específico de una implementación, no genérico|
|Tres estereotipos conceptuales en las clases: modelo, vista, controlador|Cualquier número de estereotipos físicos, según el lenguaje|
|Menos costoso (proporción 1:5 frente al diseño)|Más costoso (proporción 5:1 frente al análisis)|
|Pocas capas arquitectónicas|Muchas capas arquitectónicas|
|Puede no mantenerse durante todo el ciclo de vida|Debería mantenerse durante todo el ciclo de vida|
|Creado principalmente en trabajo de campo y talleres|Creado principalmente por "programación visual" (ingeniería directa e inversa)|
|Define la estructura, entrada esencial para dar forma al sistema|Da forma al sistema preservando la estructura del análisis|
|Enfatiza la investigación del problema y sus requisitos|Enfatiza la solución conceptual, más que su implementación|
|Enfocado en los requisitos funcionales: hacer lo correcto|Enfocado en los requisitos no funcionales: hacerlo correctamente|

### Disciplina de Implementación

Implementar el sistema en términos de componentes (código, *scripts*, binarios, ejecutables): organizar el código en subsistemas por capas, implementar clases y objetos como componentes, probar el desarrollo como unidades, e integrar en un sistema ejecutable el resultado de implementadores o equipos individuales.

### Disciplina de Pruebas

Comprobar el resultado de la implementación probando cada versión, interna o final: encontrar y documentar fallos, avisar a la gestión sobre la calidad percibida, evaluar las asunciones de diseño y de requisitos mediante demostraciones concretas, y validar que el software trabaja como fue diseñado y que los requisitos están implementados apropiadamente.

### Disciplina de Despliegue

Permitir el acceso de los usuarios finales a los componentes software en el entorno de producción: probar el software en ese entorno, configurar y distribuir los componentes, instalarlos, formar a los usuarios finales y migrar las bases de datos.

### Gestión del Ecosistema

Un conjunto de servicios integrados orientados al desarrollo de software, para acelerar su producción, controlar su calidad y monitorizar su gestión a lo largo de todas las disciplinas.

|Disciplina|Necesidad|Herramienta|
|-|-|-|
|Requisitos|Entorno colaborativo con editores, historial y autoría donde escribir y leer los requisitos centralizados|Wiki de GitHub|
|Análisis y Diseño|Herramienta CASE para editar diagramas (casos de uso, clases, secuencia, despliegue...) con trazabilidad|MagicDraw|
|Análisis y Diseño|Métricas del software que determinen automáticamente la bondad de la arquitectura|SonarQube|
|Programación|Entorno de desarrollo integrado para editar, compilar y ejecutar código|Eclipse|
|Programación|Cumplimiento de reglas de estilo (formato, identificadores...)|Eclipse, Checkstyle, PMD, FindBugs, SonarQube|
|Programación|Automatización de la refactorización (renombrado, extraer método...)|Eclipse|
|Programación|Registro de trazas, depuración y errores en ejecución|Log4j|
|Programación|Control de versiones del repositorio común (ramas de desarrollo, entregas, producción)|GitHub|
|Pruebas|Gestión de pruebas: edición, ejecución, evaluación|JUnit, Selenium...|
|Pruebas|Integración continua tras cada cambio|Travis|
|Pruebas|Cobertura de pruebas|SonarQube|
|Despliegue|Automatización de la construcción de entregables (compilación, pruebas, empaquetado)|Maven|
|Gestión|Gestión de tickets: asignación, tiempo estimado/real, cierre|Tickets de GitHub|

## Síntesis

|Disciplina|Enfoque del sistema|
|-|-|
|Modelo del Dominio|Sistema de información del mundo real|
|Requisitos|Sistema informático como caja negra|
|Análisis|Sistema informático como caja blanca, sin decisiones tecnológicas|
|Diseño|Sistema informático como caja blanca, con decisiones tecnológicas|
|Implementación|Sistema informático como caja blanca, con tecnologías|
|Pruebas|Sistema informático como caja blanca y/o negra, con tecnologías|
|Despliegue|Usuario con el sistema informático|

## ¿Y ahora qué?

Con el panorama completo de las disciplinas, toca profundizar en la primera de ellas: [Disciplina de Requisitos](/temario/00003-disciplinaDeRequisitos.md).

### Bibliografía

Ver [Bibliografía de la evolución de los procesos de desarrollo de software](/temario/00001-procesosDeDesarrollo/README.md#bibliografía) — comparte fuentes (Booch, Brooks, Beck, Fowler, Gamma, Martin, Meyer).

> Contenido adaptado de la sesión "Disciplinas del Software" (Universo de Santa Tecla) — Prof. Luis Fernández Muñoz.
