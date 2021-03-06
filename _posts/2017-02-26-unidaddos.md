---
layout: post
title: Unidad 2
subtitle: Diseño de Bases de Datos con el modelo E-R
tags: [unidad dos, resumen, modelo E-R]
---
### 2.1 EL PROCESO DE DISEÑO

<p style="text-align: justify;">El diseño de una base de datos consiste en extraer todos los elementos relevantes de un problema, por ejemplo, saber que<b> datos estàn implicados en el proceso de facturación de una empresa</b> que vende refacciones automotrices, los datos necesarios para el proceso de inscripción de alumnos, etc.

<br><br>Para la extracción de los datos se debe realizar un análisis minucioso del dominio del problema, y saber, de esta forma, que <b>datos</b> son los <b>puramente necesarios</b> o esenciales para almacenar en la base de datos y eliminar o simplemente no considerar aquellos datos o información que no sea de utilidad.

<br><br>Una vez extraidos los datos se da inicio al <b>MODELADO</b>, es decir, la construcción, mediante alguna herramienta de diseño de base de datos, un esquema o gráfico que represente con<b>PRECISIÓN TODOS los datos</b> que el problema requiere almacenar.

<br><br>Normalmente la recopilación de la información del problema se obtiene mediante reuniones con quienes será los usuarios del sistema, a través de <b>entrevistas</b>, <b>platicas formales</b> e <b>informales</b> y <b>cuestionarios</b>. Ahora bien, el problema no se resuelve con solo poner a disposición del usuario final la base de datos, sino que va a requerir un conjunto de programas o software que automaticen el acceso a los datos y su gestión.

<br><br>Derivado de las diversas reuniones con los usuarios finales se extrae el documento de <b>Especificaciones de Requisitos Software </b>o <b>E.R.S.</b> y partir de éstos se obtiene la información necesaria para la modelización de los datos.

<br><br>El modelado consiste en<b> representar el problema realizando múltiples abstracciones</b> para entender toda la información de un problema, y de esta manera, generar un mapa donde estén identificados todos los objetos de la base de datos.

<br><br><b>El modelado de una base de datos considera lo siguiente:</b>

<br><br><b>1.</b> La persona que modeliza la base de datos en la mayoría de las ocasiones no es experta en el dominio del problema a modelar, por lo que es indispensable contar con el apoyo de una persona experta en área del problema a resolver.

<br><br><b>2.</b> Se debe modelar siguiendo estándares para que el producto se entienda y sea comprensible por la comunidad informática. Esto implica el uso de herramientas de software del mercado para realizar diseños.

<br><br><b>3.</b> La base de datos estará gestionada por un SGBD, de esta manera no se tratará igual la implantación de la base de datos en un sistema MySQL que en Oracle.

<br><br><b>Pasos para lograr la interacción y la calidad del modelado:</b>

<br><br>Se negocia con el usuario final el modelo conceptual, para después transformar el modelo conceptual a modelo lógico y este modelo lógico a físico.</p>

### 2.2 MODELO ENTIDAD-RELACIÓN

<p style="text-align: justify;">El modelo conceptual es representado a través del <b>modelo entidad-relación</b>, el cual coloca el resultado del análisis del problema real mediante uno o varios <b>diagramas</b>, los cuales son elaborados mediante una serie de figuras, las cuales representan los diversos elementos e información del problema.

<br><br><b>ENTIDAD</b>

<br><br>Cualquier tipo de objeto o concepto sobre el que se recoge información: <b>cosa</b>, <b>persona</b>, <b>concepto abstracto</b> o <b>suceso</b>. Se representa mediante un cuadro o rectángulo.

<br><br>Existen 2 tipos que son: <b>entidad fuerte</b> y <b>entidad débil</b>, éstas últimas son representadas por un recuadro doble y su existencia depende de una entidad fuerte. Una ocurrencia de una entidad se refiere a una instancia o unidad dentro de la entidad.

<br><br><b>RELACIÓN</b>

<br><br>Es la asociación entre dos o más entidades, las relaciones se identifican con un <b>nombre el cual expresa la finalidad de la relación</b>, no se deben usar nombres que signifiquen muchas cosas. Las relaciones son representadas mediante <b>rombos</b> y el nombre debe colocarse dentro del símbolo sin excepción.

<br><br>El nombre de una relación generalmente debe ser un <b>verbo</b>, ya que las relaciones describen acciones entre dos o más entidades. Las relaciones están clasificadas según su <b>grado</b>, éste se refiere al número de entidades que participan en la relación. Se recomienda que todas las relaciones sean binarias.</p>

<center><img alt="modelado" border="0" src="https://basededatostec.github.io/img/22relacion.png" title="modelado"></center>

<b>PARTICIPACIÓN</b>

<p style="text-align: justify;">La participación de una ocurrencia de una entidad, indica, mediante una <b>pareja de números</b>, el mínimo y máximo número de veces que puede aparecer en la relación asociada a otra ocurrencia de entidad, éstas son:

<br><br>(0,1)  --------------------------&gt; Mínimo cero, máximo uno
<br>(1,1)  --------------------------&gt; Mínimo uno, máximo uno
<br>(0,n) --------------------------&gt;  Mínimo cero, máximo n (muchos)
<br>(1,n) --------------------------&gt;  Mínimo uno, máximo n (muchos)

<br><br><b>CARDINALIDAD</b>

<br><br>La cardinalidad de una relación se calcula <b>a través de las participaciones</b> de sus ocurrencias. Se toma el número máximo de participaciones de cada una de ellas.</p>

<center><img alt="modelado" src="https://basededatostec.github.io/img/23cardinalidad.png" title="modelado"></center>

<b>ATRÍBUTOS</b>

<p style="text-align: justify;">Los atributos de una entidad son las <b>características</b> o <b>propiedades </b>que la definen como entidad. Se representan mediante elipses que se conectan a la entidad.

<br><br><b>ATRÍBUTO CLAVE</b>

<br><br>Designa a un <b>campo que no puede repetirse</b>. Además es posible tener un atributo clave constituido por más de un campo. Cuando se tiene una clave como esta se denomina <b>clave compuesta</b>. Cuando es formada por un único atributo se dice que es atómica.

<br><br><b>ATRÍBUTO DE RELACIÓN</b>

<br><br>Propio de una <b>relación</b> y que no puede ser cedido a las entidades.</p>

<center><img alt="modelado" border="0" src="https://basededatostec.github.io/img/24atributo.png" title="modelado"></center>

<b>TIPOS DE ATRÍBUTOS</b>

<p style="text-align: justify;"><b>Atributos simples</b>: Son aquellos que no están divididos en sub partes.
<br><br><b>Atributo compuesto</b>: Cuando está formado por más de un atributo.
<br><br><b>Atributos monovalorados</b>: Son los que tienen un solo valor
<br><br><b>Atributos multivalorado</b>: Son atributos que pueden representar varios valores simultáneamente para una misma ocurrencia de una entidad.
<br><br><b>Atributos almacenado</b>: Son los atributos cuyo valor guardan una cantidad que se utiliza para realizar cálculos con otros atributos en otras entidades o en la misma entidad.
<br><br><b>Atributo derivado</b>: Son aquellos cuyo valor se puede derivar del valor de otros atributos.
<br><br><b>Atributos con valor nulo</b>: Toma un valor nulo cuando una entidad no tiene un valor.</p>

<center><img alt="modelado" border="0" src="https://basededatostec.github.io/img/25dominio.png" title="modelado"></center>

<b>DOMINIOS</b>

<p style="text-align: justify;">El dominio representa la <b>naturaleza del dato</b>, es decir, el conjunto de valores permitidos para un atributo dentro de la figura que le corresponde.</p>

### 2.3 DISEÑO CON DIAGRAMAS E-R

<p style="text-align: justify;">El modelo de datos E-R da una flexibilidad sustancial en el diseño de un <b>esquema de bases de datos para modelar una empresa dada</b>. Un diseñador de bases de datos puede seleccionar entre el amplio rango de alternativas, éstas son:

<br><br>Si se usa un atributo o un conjunto de entidades para representa un <b>objeto</b>.

<br><br>Si un concepto del <b>mundo real</b> se expresa más exactamente mediante un conjunto de <b>entidades </b>o mediante un conjunto de <b>relaciones</b>.

<br><br>Si se usa una relación ternaria o un par de <b>relaciones binaras</b>.

<br><br>Un conjunto de <b>entidades fuertes</b> y sus conjuntos de <b>entidades débiles</b> dependientes se pueden considerar como un objeto en la base de datos, debido a que la existencia de las entidades débiles depende de la entidad fuerte.

<br><br>Un modelo de datos de<b> alto nivel</b> sirve para proporcionar un marco conceptual en el que especificar de forma sistemática los requisitos de datos de los usuarios de la base de datos que existen, y cómo se estructurará la base de datos para completar estos requisitos. La fase inicial del diseño de bases de datos, por tanto, es caracterizar completamente las necesidades de datos esperadas por los usuarios de la base de datos. El resultado de esta fase es una especificación de <b>requisitos del usuario</b>. Esta estructura general se puede expresar gráficamente mediante un diagrama E-R.

<br><br>El diseñador elige un <b>modelo de datos</b> y, aplicando los conceptos del modelo de datos elegido, traduce estos requisitos a un esquema conceptual. El esquema desarrollado en esta fase de diseño conceptual proporciona una <b>visión detallada del desarrollo</b>.

<br><br>El diseñador <b>revisa el esquema</b> para confirmar que todos los requisitos de datos se satisfacen realmente y no hay conflictos entre sí. También se examina el diseño para <b>eliminar características redundantes</b>. Lo importante en este punto es describir los datos y las relaciones, más que especificar detalles del almacenamiento físico.

<br><br>Un esquema conceptual completamente desarrollado indicará también los<b> requisitos funcionales</b> de la empresa. En una especificación de requisitos funcionales los usuarios describen los tipos de operaciones que se realizarán sobre los datos.

<br><br>El proceso de trasladar un modelo abstracto de datos a la implementación de la base de datos consta de dos fases de diseño finales. En la fase de <b>diseño lógico</b>, el diseñador traduce el esquema conceptual de alto nivel al modelo de datos de la implementación del sistema de base de datos que se usará. El diseñador usa el esquema resultante, en la que se especifican las <b>características físicas</b> de la base de datos.</p>

### 2.4 MODELO E-R EXTENDIDO

<p style="text-align: justify;">El Modelo Entidad-Relación Extendido incluye todos los conceptos del <b>Entidad-Relación</b> e incorpora los <b>conceptos de Subclase</b> y <b>Superclase</b> con los conceptos asociados de <b>Especialización</b> y <b>Generalización</b> respectivamente.

<br><br><b>ESPECIALIZACIÓN:</b>

<br><br>El proceso por el que se definen las <b>diferentes subclases</b> de una <b>superclase</b> se conoce como especialización. El conjunto de subclases se define <b>basándonos en características</b> diferenciadoras de las ocurrencias de entidad de la superclase. Por ejemplo, el conjunto se subclases {SECRETARIA, INGENIERO, TECNICO} es una especialización de la <b>superclase EMPLEADO</b> mediante la distinción del tipo de trabajo en cada ocurrencia de entidad. Podemos tener varias especializaciones de una misma entidad. Por ejemplo, otra especialización de <b>EMPLEADO</b> podría dar lugar a las subclases <b>ASALARIADO</b> y <b>SUBCONTRATADO</b>, dependiendo del tipo de contrato.</p>

<center><img src="https://basededatostec.github.io/img/26extendido.png" alt="modelo" title="modelo"></center>

<b>GENERALIZACIÓN:</b>

<p style="text-align: justify;">Es el <b>proceso inverso</b> al de la especialización. Se aplican ambos procesos para construir el esquema E-R extendido. Se basa simplemente en agrupar entidades con atributos comunes en una entidad superior de nivel más alto.

<br><br>Es decir "La generalización es el resultado de <b>tomar la unión de dos o más conjuntos</b> disjuntos de entidades para producir un conjunto de entidades de <b>nivel más alto</b>.

<br><br><b>Entidades agrupadas</b>: subclases de nivel más bajo.

<br><br>Proceso aplicado dentro de una estrategia de diseño bottom-up, definiendo entidades simples y agrupándolas. Agrupamiento de entidades elimina la redundancia. El proceso de diseño puede ser también de <b>forma ascendente en vez de descendente</b>, de manera que distintos grupos de entidades se sintetizan en grupos de entidades de nivel más alto. Basada en sus similitudes, la generalización sintetiza distintos conjuntos de entidades en uno sólo.  La generalización es la <b>inversa de la especialización</b>.

<br><br><b>AGREGACIÓN</b>

<br><br>La agregación es una abstracción a través de la cual las<b> relaciones se tratan como entidades </b>de nivel más alto. Así, se considera el conjunto de relacionestrabaja-en como un conjunto de entidades de nivel más alto denominado trabaja-en.

<br><br>Tal conjunto de entidades se trata de la misma forma que cualquier otro conjunto de entidades. Se puede crear una <b>relación binaria</b> dirige entre trabaja-en y director para representar quién dirige las tareas, como se muestra a continuación.</p>

<center><img src="https://basededatostec.github.io/img/27modelo.jpg" alt="modelo" title="modelo"></center>

### 2.5 LA NOTACIÓN E-R CON UML


<p style="text-align: justify;">Los diagramas entidad-relación <b>ayudan a modelar el componente de representación</b> de datos de un sistema software. La representación de datos, sólo forma parte de un diseño completo de un sistema complejo de notaciones.

<br><br>Otros componentes son modelos de interacción del usuario con el sistema, especificación de módulos funcionales del sistema y su interacción, etc. El lenguaje de modelado unificado, propuesto para la creación de especificaciones de componentes de un sistema software. Algunas de las partes principales de UML son:

<br><br><b>Diagrama de clase</b>. Un diagrama de clase es similar a un diagrama E-R.
<br><b>Diagrama de caso de uso</b>. Los diagramas de caso de uso muestran la interacción entre los usuarios y el sistema, en particular los pasos de las tareas que realiza el usuario.
<br><b>Diagrama de actividad</b>. Los diagramas de actividad describen el flujo de tareas entre varios componentes del sistemaa que se encuentra en uso.
<br><b>Diagrama de implementación</b>. Muestran los componentes del sistema y sus interconexiones tanto en el nivel del componente software como el hardware.

<br><br>La siguiente figura muestra varios constructores de diagramas E-R y sus constructores equivalentes de los diagramas de clase UML. UML muestra los conjuntos de entidades como<b> cuadros </b>y a diferencia de E-R, muestra los atributos dentro del cuadro en lugar de como <b>elipses separadas</b>. Unified Modeling Language modela realmente objetos, mientras que E-R modela entidades. Los objetos son como entidades y tienen atributos, pero además proporcionan un conjunto de funciones que se pueden invocar para calcular valores en términos de los atributos de los objetos, o para modificar el propio objeto. Los diagramas de clase pueden describir métodos además de atributos.

<br><br>Los conjuntos de relaciones binarias se representan en UML <b>dibujando simplemente una línea</b> que conecte los conjuntos de entidades. Se escribe el nombre del conjunto de relaciones adyacente a la línea. También se puede especificar el papel que juega un conjunto de entidades en un conjunto de relaciones escribiendo el nombre del papel en un cuadro, junto con los atributos del conjunto de relaciones, y conectar el cuadro con una línea discontinua a la línea que describe el conjunto de relaciones.

<br><br>Este cuadro se puede tratar entonces como un <b>conjunto de entidades</b>. Las relaciones no binarias no se pueden representar directamente en UML se deben convertir en relaciones binarias . Las restricciones de cardinalidad se especifican en UML de la misma forma que en los diagramas E-R, de la forma i..s, donde i denota el mínimo y s el máximo número de relaciones en que puede participar una entidad.

<br><br>Sin embargo, se debería ser <b>consciente que la ubicación de las restricciones</b> es exactamente el inverso de la ubicación de las restricciones en los diagramas Entidad-Relación, como se muestra en la siguiene figura a continuación.</p>

<center><img src="https://basededatostec.github.io/img/28modelo.png" alt="uml" title="UML"></center>

__Fuentes de Información__

<a href="http://tavoberry.com/MER/diagramas_er.html" target="_blank">Modelo entidad relación</a>

|  Acerca de: | 
| :------ | 
| Éste es un sitio creado por estudiantes del Instituto Tecnológico de Pachuca, para la asignatura en curso; Fundamentos de Bases de Datos. | 
| Equipo New Jackers: Hernández Salinas Lucio y Sanchez Casañas Jose María |
| <a href="https://basededatostec.github.io/unidaddos/">Actividades Unidad 2</a> |
