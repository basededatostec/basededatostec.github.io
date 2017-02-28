---
layout: post
title: Unidad 1. Introducción a las Bases de Datos
tags: [unidad uno, resumen, introducción]
---
<center><img src="https://basededatostec.github.io/img/07bases.png" title="Introducción" alt="bases de datos"></center>
### 1.1 CONCEPTOS BÁSICOS

<p style="text-align: justify;"><b>Base de datos</b>. Una base de datos es un gran almacén donde se guardan enormes cantidades de información organizada, 
de esta manera cuando se quieran utilizar estos datos se puedan encontrar rápidamente, así ahorramos espacio físico y tiempo.

<br><br>También se puede definir como un conjunto de datos relacionados y organizados, estos datos a su vez son recolectados y utilizados por grandes empresas e constituciones.

<br><br><b>Dato</b>. Un dato es información que refleja una característica de algún objeto, ya sea concreto, o imaginario, por ejemplo podemos crear una base de datos acerca de los datos de una persona, un dato posible, sería; la fecha de nacimiento.</p>

### 1.2 OBJETIVOS DE LAS BASES DE DATOS


<center><img src="https://basededatostec.github.io/img/08objetivo.png" title="Objetivos" alt="objetivoss"></center>
Algunos de los principales objetivos de las bases de datos son:

__Disminuir la redundancia e inconsistencia de los datos__

<p style="text-align: justify;">Existe la posibilidad de que al no controlar el almacenamiento se origine redundancia en la información, esto quiere decir que se duplican los datos. Entonces aumenta en buena medida el costo de almacenamiento y acceso, además se origina inconsistencia. 

<br><br>Por lo que debe contener el máximo contenido semántico para que la información sea realmente verdadera. Debe ser comprensible e interesante, lo que supone no proporcionar a los usuarios un volumen grande de información que no pueda ser asimilada.</p>

__Reducir la dificultad para tener acceso a los datos__

<p style="text-align: justify;">Un buen sistema de base de datos debe tener un entorno de datos que le facilite al usuario el manejo de los mismos.</p>

__Evitar el aislamiento de los datos__

<p style="text-align: justify;">Si el nivel de aislamiento es bajo, la capacidad de los usuarios al acceder al mismo tiempo a los datos aumenta. Por el contrario, un mayor nivel de aislamiento reduce los tipos de efectos de la concurrencia que los usuarios pueden encontrar, pero requiere más recursos del sistema y se corre el riesgo de que una transacción bloquee a otra.</p>

__Corregir anomalías del acceso concurrente__

<p style="text-align: justify;">El sistema debe permitir que múltiples usuarios actualizen los datos de forma simultanea. Cuando esto ocurre pueden dar como resultado datos inconsistentes, por ello se recomienda, mantener una supervision al sistema muy detallada.</p>

__Disminuir los problemas de seguridad__

<p style="text-align: justify;">Los valores que se guardan en la base de datos debe satisfacer limitantes de consistencia, el sistema debe obligar el cumplimiento de estas limitantes.</p>

__Debe contar con integridad__

<p style="text-align: justify;">La información contendida en el sistema debe ser coherente y consistente con las reglas semánticas propias del mundo real.</p>

### 1.3 ÁREAS DE APLICACIÓN DE LAS BASES DE DATOS

Estás son las principales áreas en donde las bases de datos pueden ser usadas.

__Banca__: Información  ede los clientes, información de las cuentas, del registro de operaciones, de las operaciones con tarjeta de crédito, transacciones, préstamos, etc.

__Líneas aéreas__: Para reservar y contar con información de horarios, registro de clientes, registro de vuelos, destinos disponibles, etc. 

<p style="text-align: justify;"><b>Universidades</b>: Para poseer información de los estudiantes, matriculas en asignaturas, carreras, para registrar y ordenar horarios, materias, profesores, etc.</p>

<p style="text-align: justify;"><b>Transacciones de tarjeta de crédito</b>: Se registran las compras con tarjetas de crédito y la generación de los extractos mensuales.

<br><br><b>Producción</b>: Para la gestión de la cadena de proveedores y para el seguimiento de la producción de articulos, inventarios en los almacenamientos y pedidos.

<br><br><b>Telecomunicaciones</b>: Guardar registros de llamadas realizadas, generar facturas mensuales, mantener el saldo de las tarjetas y almacenar información sobre las redes.</p>

Su uso es muy amplio y se puede tener en cualquier sistema que aloje datos.

### 1.4 MODELOS DE BASES DE DATOS 

<p style="text-align: justify;">Además de la clasificación por la función de las bases de datos, éstas también se pueden clasificar de acuerdo a su modelo de administración de datos.</p>

<center><img src="https://basededatostec.github.io/img/09modelos.png" title="Modelos" alt="modelos"></center>

<p style="text-align: justify;">Un modelo de datos es <b>una descripción</b> de algo conocido como contenedor de datos, así como de los métodos para almacenar y recuperar información de esos contenedores. Los modelos de datos <b>no son físicos</b>: son abstracciones que permiten la implementación de un sistema eficiente de base de datos.</p>

Algunos modelos con frecuencia utilizados en las bases de datos:

#### Modelos de diseño:

__Modelo entidad-relación ER__

<p style="text-align: justify;">El modelo entidad-relación ER es un modelo de datos que permite representar cualquier abstracción, percepción y conocimiento en un sistema de información formado por un conjunto de objetos denominados entidades y relaciones, incorporando una representación visual conocida como diagrama entidad-relación. </p>

#### Modelos de representación:

__Modelo jerárquico__

<p style="text-align: justify;">En este modelo los datos se organizan en una <b>forma similar a un árbol</b>, en donde un nodo padre de información puede tener varios hijos. El nodo que no tiene padres es llamado <b>raíz</b>, y a los nodos que no tienen hijos se los conoce como <b>hojas</b>. Las bases de datos jerárquicas son especialmente útiles en el caso de aplicaciones que <b>manejan un gran volumen de información</b> y datos muy compartidos.</p>

<center><img src="https://basededatostec.github.io/img/10jerarquia.png" title="Jerárquias" alt="jerarquias"></center>

__Modelo de red__

<p style="text-align: justify;">Éste es un modelo ligeramente distinto del jerárquico; su diferencia fundamental es la modificación del concepto de nodo: se permite que <b>un mismo nodo tenga varios padre</b>. Ofrecía una solución eficiente al <b>problema de 
redundancia</b> de datos.</p>

__Modelo relacional__

<p style="text-align: justify;">Éste es el modelo utilizado en la actualidad para modelar <b>problemas reales</b> y administrar datos dinámicamente.Su idea fundamental es el uso de <b>relaciones</b>. Estas relaciones podrían considerarse en forma lógica como conjuntos de datos llamados <b>tuplas</b>.  La información puede ser recuperada o almacenada mediante <b>consultas</b> que ofrecen una amplia flexibilidad y poder para administrar la información.</p>

<center><img src="https://basededatostec.github.io/img/11relacion.png" title="Relacional" alt="relacional"></center>
__Modelo  transaccional__

<p style="text-align: justify;">Son bases de datos cuyo único fin es el <b>envío</b> y <b>recepción de datos</b> a grandes velocidades, estas bases son muy poco comunes y están dirigidas por lo general al entorno de análisis de calidad, es importante entender que su fin único es <b>recolectar</b> y <b>recuperar los datos</b> a la mayor velocidad posible, por lo tanto la redundancia y duplicación de información no es un problema como con las demás bases de datos.</p>

### 1.5 CLASIFICACIÓN DE LAS BASES DE DATOS

<p style="text-align: justify;">Las bases de datos se clasificarse de varias maneras, de acuerdo al contexto que se esté manejando, su utilidad o las necesidades que satisfagan.</p>

__Según la variabilidad de los datos almacenados__

<p style="text-align: justify;"><b>Bases de datos estáticas</b>. Bases de datos de sólo lectura, se utilizan primordialmente para almacenar <b>datos históricos,</b> para estudiar el comportamiento de un conjunto de datos a través del tiempo, realizar proyecciones y tomar decisiones.</p>

<p style="text-align: justify;"><b>Bases de datos dinámicas</b>. Éstas son bases de datos donde la información almacenada se modifica con el tiempo, permitiendo operaciones como <b>actualización</b> y <b>adición de datos</b>, además de las operaciones fundamentales de consulta.</p>

__Según el contenido__

<p style="text-align: justify;"><b>Bases de datos bibliográficas</b>. Sólo contienen un representante de la fuente primaria, que permite localizarla. Un registro típico de una <b>base de datos bibliográfica</b> contiene información sobre el autor, fecha de publicación, editorial, título, edición, de una determinada publicación, etc. Puede contener un resúmen o extracto de la publicación original, pero nunca el texto completo.</p>

<p style="text-align: justify;"><b>Bases de datos de texto completo</b>. Almacenan las <b>fuentes primarias</b>, por ejemplo, todo el contenido de las ediciones de una colección de revistas científicas.</p>

<p style="text-align: justify;"><b>Bases de datos de información química o biológica</b>. Son bases de datos que almacenan diferentes tipos de información proveniente de la <b>química</b>, las <b> de la vida</b> o <b>médicas</b>, almacenan secuencias de nucleótidos o proteínas.</p>

<p style="text-align: justify;"><b>Bases de datos de rutas metabólicas</b>. Bases de datos de estructura, comprende los registros
de datos experimentales sobre <b>estructuras 3D</b> de biomoléculas.</p>

### ARQUITECTURA DE BASE DE DATOS

<p style="text-align: justify;">La arquitectura de un sistema de base de datos está influenciada por el sistema informático que soporta la instalación del SGBD, lo que reflejará muchas de las características propias del sistema subyacente en el SGBD.

Las bases de datos respetan la arquitectura de tres niveles definida, para cualquier tipo de base de datos. En esta arquitectura la base de datos se divide en los niveles externo, conceptual e interno.

Nivel externo: es el nivel de mayor abstracción. A este nivel corresponden las diferentes vistas parciales que tienen de la base de datos los diferentes usuarios. En cierto modo, es la parte del modelo conceptual a la que tienen acceso.</p>

 Nivel conceptual: es el nivel medio de abstracción. Se trata de la representación de los datos realizada por la organización, que recoge las vistas parciales de los requerimientos de los diferentes usuarios y las aplicaciones posibles. Se configura como visión organizativa total, e incluye la definición de datos y las relaciones entre ellos.

Nivel interno: es el nivel más bajo de abstracción, y define cómo se almacenan los datos en el soporte físico, así como los métodos de acceso.</p>







