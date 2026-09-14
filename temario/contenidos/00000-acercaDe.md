# Ingeniería de software

## ¿Por qué?

### Breve historia del Software y el Hardware

La humanidad, gracias a sus herramientas y en particular al conocimiento (ciencias, ingenierías...), ha construido grandes sistemas artificiales — acueductos, telares con tarjetas perforadas, red eléctrica, red telefónica... — para automatizar tareas, es decir, simplificar y reutilizar.

|Año|Hito|
|-|-|
|8000 a.e.c.|Los sumerios construyen telares para cubrirse|
|1642|Blaise Pascal construye la Pascalina, primera calculadora mecánica girando ruedas|
|1801|Jacquard construye el primer telar mecánico y automático con tarjetas perforadas para definir los dibujos|
|1812-13|Charles Babbage, en Londres, diseña la Máquina Analítica retomando las tarjetas perforadas de los telares; no llegó a funcionar, pero Ada Lovelace ya escribió sobre ella las primeras líneas de código de la historia|
|1884|Hollerith desarrolla la Máquina Tabuladora de tarjetas perforadas para el registro de propiedad en la conquista del Oeste|
|1936|Konrad Zuse diseña y fabrica la Z1, considerada por muchos la primera computadora programable de la historia|

Charles Babbage ocupó la Cátedra Lucasiana (la misma que Newton o Hawking); construyó la **Máquina Analítica**, el *hardware*. Ada Lovelace — matemática, hija de Lord Byron — es considerada la primera programadora del mundo: aportó el concepto de **software**.

### Inefectividad del Proyecto Software

|Objeto|Capacidad cuantitativa|Capacidad cualitativa|
|-|-|-|
|Ser humano|Muy mala: pequeña, errores por cansancio, desmotivación... y muy lento|Muy buena: reconocimiento de patrones, asociaciones, recursividad...|
|Hardware|Muy buena: sin errores y a toda velocidad|Muy mala: ningún computador ha superado la prueba de Turing|

Un proyecto de software sin un proceso que lo gobierne tiende a la **inefectividad, ineficacia e ineficiencia**, porque tiene:

#### Malas variables en su economía: ámbito, tiempo y coste

No hay una relación sencilla entre estas variables. Por ejemplo, no se puede reducir el tiempo a la mitad gastando el doble.

> Nueve mujeres no pueden tener un bebé en un mes; dieciocho mujeres aún no pueden tener un bebé en un mes.
>
> — Brooks

> La forma de jugar a este juego del desarrollo de software es que las fuerzas externas (clientes, directores de proyecto) eligen los valores de tres variables cualquiera; el equipo de desarrollo determina el valor resultante de la cuarta.
>
> — Kent Beck, 1999

> Algunos directores de proyecto y clientes creen que pueden escoger el valor de las cuatro variables. Cuando esto sucede, la calidad siempre desaparece, ya que nadie hace bien su trabajo bajo una fuerte presión. Y, probablemente, el tiempo también estará fuera de control.
>
> — Kent Beck, 1999

|Variable|Consecuencia de gestionarla mal|
|-|-|
|**Ámbito**|Es la más importante. Poco ámbito permite entregar más rápido, con más calidad y más barato. Es muy variable porque los requisitos nunca están claros al principio, y cambian tan pronto el cliente ve la primera versión y aprende lo que realmente quería|
|**Tiempo**|Poco tiempo perjudica la calidad, junto con el ámbito. Demasiado tiempo también perjudica: la retroalimentación desde producción es de más calidad que cualquier otra|
|**Coste**|Al comienzo no se puede gastar mucho: la inversión crece con el tiempo. Demasiado dinero crea más problemas de los que resuelve; poco dinero no permite resolver el problema del cliente|

#### Mala calidad del software

|Característica|Consecuencia|
|-|-|
|**Fiabilidad**|No cumple su función bajo ciertas condiciones durante un tiempo determinado|
|**Extensibilidad**|No admite nuevas funcionalidades|
|**Usabilidad**|No es sencillo de usar, no facilita la lectura ni presenta funciones y menús sencillos|
|**Accesibilidad**|No puede ser accedido y usado por el mayor número posible de personas|
|**Seguridad**|No preserva confidencialidad, integridad ni disponibilidad de los datos|
|**Interoperabilidad**|Dos o más sistemas o componentes no pueden intercambiar información ni usar la intercambiada|
|**Portabilidad**|No se puede reutilizar al pasar de una plataforma a otra|
|**Escalabilidad**|No reacciona ni se adapta sin perder calidad cuando aumenta el tamaño del sistema|

Todas estas *-ilities* dependen, en última instancia, de la **mantenibilidad**: la habilidad de conservar el funcionamiento normal, o de restituirlo tras un fallo o un nuevo requisito (correctiva, perfectiva y adaptativa, respectivamente).

|No mantenible|Explicación|
|-|-|
|**Viscoso**, porque no se puede entender con facilidad|Es fácil hacer las cosas mal, pero difícil hacer lo correcto. Ocurre tanto por viscosidad del diseño (preservarlo es más difícil que tomar atajos) como del entorno (compilaciones o *commits* lentos que tientan a atajos que no preservan el diseño)|
|**Rígido**, porque no se puede cambiar con facilidad|Cada cambio provoca una cascada de cambios en los módulos dependientes: un cambio de dos días se convierte en un maratón de semanas. Cuando el miedo de los gestores a esto se instala como política, la rigidez pasa de ser un defecto de diseño a una política de gestión adversa|
|**Frágil**, porque no se puede probar con facilidad|El software se estropea en muchos lugares cada vez que se cambia, a menudo sin relación conceptual con lo modificado. La probabilidad de error crece con el tiempo hasta hacerlo imposible de mantener|
|**Inmóvil**, porque no se puede reutilizar con facilidad|Un módulo similar a uno ya existente tiene demasiado "equipaje" del que depende; separar las partes deseables sale más caro que reescribirlo desde cero|

> El principal enemigo de la fiabilidad, y tal vez de la calidad del software en general, es la complejidad.
>
> — Meyer

> Cuanto más complejo es un sistema, más abierto está al colapso total. Gran parte de la complejidad que hay que dominar es **complejidad arbitraria** — la que no impone el problema, sino la falta de método.
>
> — Booch

#### Crisis del Software

La incapacidad para dominar la complejidad de los proyectos software, con sus defunciones, accidentes, desastres y ruinas. Según estadísticas del Standish Group sobre 50.000 proyectos, los motivos más frecuentes de proyectos fracasados o problemáticos (entregados tarde, con deficiencias funcionales o por encima de presupuesto) son:

|Categoría|Motivo|Incidencia|
|-|-|-|
|**Gestión**|Falta de involucración del usuario|31,0%|
||Poco apoyo de las gerencias|12,8%|
||Falta de recursos|7,5%|
||Tiempos poco realistas|6,4%|
|**Requisitos**|Requerimientos y especificaciones poco claras|35,3%|
||Cambio de requerimientos y especificaciones|12,3%|
||Expectativas poco realistas|11,8%|
||Objetivos poco claros|5,9%|
|**Tecnologías**|Tecnología deficiente|10,7%|
||Nuevas tecnologías|7,0%|
|**Otros**||23,0%|

> El software no se muere, se convierte en un zombi.

## ¿Qué?

### Software

> Software es la información que suministra el desarrollador a la computadora para que manipule de forma automática la información que suministrará el usuario.
>
> — Brad Cox

Software es programas en lenguajes de programación (Java, C/C++...), *scripts* de bases de datos (SQL) o de páginas dinámicas (JSP, PHP...), presentaciones en lenguajes de formato (HTML, CSS...), datos de configuración (texto libre, XML, JSON...) y multimedia (imagen, sonido, vídeo) para la interfaz de usuario.

### Sistema de Información

> Un sistema de información es un conjunto de elementos orientados al tratamiento y administración de datos e información, organizados y listos para su uso posterior, generados para cubrir una necesidad o un objetivo.
>
> — Wikipedia

Su tratamiento se reduce, en última instancia, a la **gestión (CRUD)** de esa información: altas (*Create*), bajas (*Delete*), modificaciones (*Update*) y consultas (*Read*).

### Complejidad del Proyecto Software

> El trabajo con software es el más complejo que jamás haya emprendido la humanidad.
>
> — F. Brooks

|Proyecto software mediano|El Quijote de la Mancha|
|-|-|
|Extensión: ~100.000 líneas / ~3 palabras por línea|Extensión: 300.000 palabras|
|Entidades: centenares|Entidades: decenas (Dulcinea, Sancho Panza...)|
|Autor: 6-8 personas|Autor: Miguel de Cervantes|
|Duración: entre 6 meses y años|Duración: 18 años|
|Coste: miles de euros|Coste: gratis, en la cárcel|
|Ámbito: cambiante, de otra persona (el cliente)|Ámbito: propio del autor|

El software de una aplicación media excede con creces la capacidad intelectual humana para abarcarlo de una vez, por su estructura jerárquica (herencia, composición, paquetes...), sus elementos primitivos relativos al lenguaje, la separación de asuntos por encapsulación y modularidad, sus patrones comunes de paso de mensajes, y sus formas intermedias estables gracias a las metodologías iterativas.

### Proceso de Desarrollo Software

> **Proceso de Desarrollo Software**: el conjunto total de actividades necesarias llevadas a cabo por distintos roles para transformar los requerimientos del cliente en un conjunto consistente de artefactos que representan un producto software y, en un momento posterior, para transformar los cambios de estos requerimientos en una nueva versión del producto software.
>
> — Booch, 1985

Sinónimos: **Metodología** / **Método de Desarrollo Software**, **Ciclo de Vida del Desarrollo Software**.

|Unidad|Definición|Ejemplo|Características|
|-|-|-|-|
|**Actividad**|Unidad de trabajo que puede ser solicitada o realizada por un rol individual y que produce un resultado significativo en el contexto del proyecto|especificar un caso de uso, implementar una clase, ejecutar pruebas de rendimiento...|Propósito claro expresado en crear o modificar artefactos; asignada a un rol específico; afecta a uno o a un pequeño número de artefactos; granularidad de unas horas a unos pocos días|
|**Rol**|Define el comportamiento y responsabilidad de un individuo o de un grupo de individuos juntos como un equipo|analista de sistemas, ingeniero de componentes, integrador de sistemas...|Comportamiento expresado en actividades; responsabilidad expresada en los artefactos que crea, modifica o controla; no son individuos, son títulos de trabajo intercambiables|
|**Artefacto**|Pieza de información que es producida, modificada o usada por un proceso|código fuente, especificación de un caso de uso, arquitectura del software...|Formales, típicamente no documentos abiertos; productos tangibles; entrada y salida de las actividades; sujetos al control de versiones y a la gestión de la configuración|

El ciclo de vida de un producto software alterna dos grandes etapas, tantas veces como el producto siga vivo:

|Producción|Evolución|
|-|-|
|Desarrollo de la versión v1|Sucesivas explotaciones (v1, v2, v3...) del producto en producción, mientras se desarrolla y despliega su mantenimiento|

## ¿Para qué?

Un proyecto gobernado por un proceso tiende a la **efectividad, eficacia y eficiencia**: gestión de sistemas de información requeridos por clientes para distintos usuarios, con eficacia (sin errores en cálculos, filtrados, secuencias de acciones...) y eficiencia (escaso consumo de *hardware*, energía y tiempo del usuario para aprender y explotar el producto). Porque tiene:

- **Buenas variables en su economía**: ámbito cumplido y tiempo cumplido y coste cumplido.
- **Buena calidad del software**: fiabilidad, extensibilidad, usabilidad, accesibilidad, seguridad, interoperabilidad, portabilidad, escalabilidad...
- **Buena mantenibilidad**:
  - **Fluido**, porque se puede entender con facilidad y/o
  - **Flexible**, porque se puede cambiar con facilidad y/o
  - **Fuerte**, porque se puede probar con facilidad y/o
  - **Reusable**, porque se puede reutilizar con facilidad.
- **Complejidad inherente**: solo la que impone el problema, ninguna añadida por falta de método.

> No se convierte uno en maestro del software aprendiendo una lista de heurísticas. El profesionalismo y la maestría provienen de valores que impulsan las disciplinas.
>
> — Martin Fowler, *Refactoring*

## ¿Cómo?

Una mera enumeración de roles, actividades y artefactos no constituye un proceso. Un **proceso** es un flujo de trabajo: una secuencia de actividades que produce valor observable en artefactos y muestra las interacciones entre roles.

No existe una única forma de organizar ese flujo de trabajo — ver [evolución de los procesos de desarrollo de software](/temario/00001-procesosDeDesarrollo/README.md).

## Evolución histórica de la Ingeniería del Software

|1950 - 1965|1965 - 1972|1972 - 1985|1985 - 1995|2000 - 2022|2022 - Hoy|
|-|-|-|-|-|-|
|Codificar y Corregir.|Objetivo: simplificar código|Microprocesadores.|Impacto colectivo de software.|Codificar y Corregir.|"Codificar" y Corregir 2.0|
|No planificación.|Multiprogramación y Multiusuarios.|Sistemas distribuidos.|Redes de información|No planificación.|No planificación (pero con IA)|
|No documentación.|Tiempo real, toma de decisiones.|Complejidad en los sistemas de información.|Tecnologías orientadas a objetos|No documentación.|¿Documentación? (la IA la genera después)|
|Pocos métodos formales|Software como producto.|LAN & WAN|Redes neuronales|Pocos métodos formales|La IA sabe por nosotros|
|Pocos creyendo en ellos|Crisis del software.||Sistemas expertos|Pocos creyendo en ellos|total, ya le pregunto a la IA|
|Desarrollo a base de prueba y ensayo.|||Inteligencia artificial.|Desarrollo a base de prueba y ensayo.|Desarrollo a base de prompt y ensayo|
|-|-|-|La información como activo de valor.|-|Cualquiera genera código|
|-|-|-|-|-|**"Funciona, no me preguntes por qué"**|
|-|-|-|-|-|***Stack Overflow → Chat GPT***|

> Contenido adaptado de la sesión "Software" (Universo de Santa Tecla) — Prof. Luis Fernández Muñoz.
