---
layout: post
title: Unidad 4
subtitle: Normalización de bases de datos
tags: [unidad cuatro, resumen, introducción, normalizado]
---
### 4.1 CONCEPTOS BÁSICOS

<p style="text-align: justify;">La normalización es el <b>proceso de organizar los datos</b>. Se incluye la creación de tablas y el establecimiento de relaciones entre ellas según reglas diseñadas tanto para proteger los datos como para hacer que la base de datos sea más <b>flexible</b>. 

<br><br>Los <b>datos redundantes</b> desperdician el espacio de disco y crean problemas de mantenimiento. Si hay que cambiar datos que existen en más de un lugar, se deben cambiar de la misma forma exactamente en todas sus ubicaciones. Un cambio en la dirección de un cliente es mucho más fácil de implementar si los datos sólo se almacenan en la <b>tabla Clientes</b> y no en algún otro lugar de la base de datos. 

<br><br>Uno de los parámetros que mide la calidad de una base de datos es la <b>forma normal</b> en la que se encuentra su diseño. Puede alcanzarse cumpliendo ciertas restricciones que impone cada forma normal al <b>conjunto de atributos</b> de un diseño. Obligar a los atributos de un diseño a cumplir ciertas formas normales se llama normalización.

<br><br>Las formas normales pretenden alcanzar dos objetivos:

<br><br><b>1.-</b> Almacenar en la base de datos cada hecho solo una vez, es decir, <b>evitar la redundancia</b> de datos. De esta manera se reduce el espacio de almacenamiento.

<br><br><b>2.-</b> Que los hechos distintos se <b>almacenen</b> en sitios distintos.</p>

### 4.2 PRIMERA FORMA NORMAL

<p style="text-align: justify;">Esta primera <b>forma normal</b>, nos lleva a no repetir datos en nuestras tablas. Si nuestra tabla de ventas repite una y otra vez, el <b>nombre</b>, el <b>domicilio</b> y otros datos del Cliente, es que no hemos aplicado esta normalizaciòn. Si tenemos una tabla <b>clientes</b>, en la tabla <b>ventas</b>, solo debería figurar el código del <b>cliente</b>, para que el resto de los datos se puedan referenciar automaticamente en el proceso.

<br><br>Lo mismo ocurriría en una tabla de <b>detalle de ventas</b>, si por cada producto vendido colocamos el detalle del producto, con su descripción , medidas, etc. Tendriamos un desaprovechamiento de espacio y recursos muy grande. Para ello, tendremos nuestra tabla maestra de <b>Productos</b> y con solo grabar el código de dicho producto.</p>

<img src="https://basededatostec.github.io/img/42normalizado.png">

### 4.3 DEPENDENCIAS FUNCIONALES Y TRANSITIVAS

<p style="text-align: justify;">Intentaremos aclarar este concepto tan teórico con un ejemplo. Si tenemos esta relación:

<br><br><b>Ciudades</b>(ciudad, población, superficie, renta, país, continente)

<br><br>Los atributos como <b>población</b>, <b>superficie</b> o <b>renta</b> tienen dependencia funcional de ciudad, así que de momento no nos preocupan.

<br><br>En esta relación podemos encontrar también las siguientes dependencias:
ciudad -> país, país -> continente. Además, país -> ciudad. Es decir, <b>cada ciudad pertenece a un país</b> y <b>cada país a un continente</b>, pero en cada país puede haber muchas ciudades. En este caso continente tiene una dependencia funcional transitiva con respecto a ciudad, a través de país. Es decir, cada ciudad está en un país, pero también en un continente.</p>

### 4.4 SEGUNDA FORMA NORMAL

<p style="text-align: justify;">La <b>Segunda Forma Normal</b> nos habla de que cada columna de la tabla debe depender de la clave. Esto significa que todo un registro debe depender únicamente de la <b>clave principal</b>, si tuvieramos alguna columna que se repite a lo largo de todos los registros, dichos datos deberian atomizarse en una nueva tabla.:</p>

<img src="https://basededatostec.github.io/img/43normalizado.png">

<p style="text-align: justify;">Si toda una venta tendrá el mismo numero de <b>Cliente</b> y la <b>misma Fecha</b>. ¿Por que no crear una Tabla de <b>VENTAS</b> y que contenga esos 2 datos? Es evidente que la columna <b>ClienteVenta</b> y <b>FechaVenta</b> se repetirán por cada venta realizada.</p>

<img src="https://basededatostec.github.io/img/44normalizado.png">

Y ahora nuestra nueva tabla:

<img src="https://basededatostec.github.io/img/45normalizado.png">

### 4.5 TERCERA FORMA NORMAL

<p style="text-align: justify;">La <b>Tercera Forma Normal</b> nos habla de que: <b>ninguna columna puede depender de una columna</b> que no tenga una clave y no puede haber datos derivados.

<br><br>En el ejemplo anterior se notan campos que dependian de la <b>clave principal</b> y que podrian incluirse en una tabla maestra. Pero supongamos un ejemplo donde ciertas columnas no dependen de la clave principal y si dependen de una columna.</p>

<img src="https://basededatostec.github.io/img/46normalizado.png">

<p style="text-align: justify;">Los campos <b>DESCRIPCION</b>, <b>MEDIDA</b> y <b>PROVEEDOR</b> no dependen de <b>VENTAID</b>, no deberian estar dentro de la tabla de detalle de ventas, ya que dependen de <b>PRODUCTOID</b>. No se trata ya de eliminar grupos repetidos de datos, sino que ante la inclusion de una clave perteneciente a otra tabla, cualquier campo que sea subordinado de dicha clave debe estar en otra tabla y no en nuestra tabla detalle.</p>

### 4.6 FORMA NORMAL BOYCE-CODD

<p style="text-align: justify;">Una relación está en <b>Forma Normal Boyce-Codd</b> si cualquier atributo sólo facilita información sobre claves candidatas, y no sobre atributos que no formen parte de ninguna clave candidata. Esto significa que no deben existir <b>interrelaciones</b> entre atributos fuera de las claves candidatas.

<br><br>Para ilustrar esta forma normal tomemos como ejemplo lo siguiente. 

<br><br>Las ocupaciones de habitaciones de un hotel.
<br><b>Ocupación</b>(No_cliente, Nombre_cliente, No_habitación, fecha_entrada)
<br><b>Habitación</b>(No_habitación(PK), precio_noche, tipo_habitación)

<br><br>En la primera relación los atributos <b>No_cliente</b> y <b>Nombre_cliente</b> sólo proporcionan información entre ellos mutuamente, pero ninguno de ellos es una clave candidata.

<br><br>Esta estructura puede producir redundancia, en <b>clientes habituales</b>, donde se repetirá la misma información cada vez que el mismo cliente se aloje en el hotel.

<br><br>La solución es simple, y consiste en separar esta relación en dos diferemtes:
<br><b>Ocupación</b>(No_cliente, No_habitación, fecha_entrada)
<br><b>Cliente</b>(No_cliente(PK), Nombre_cliente)
<br><b>Habitación</b>(No_habitación(PK), precio_noche, tipo_habitación)</p>

<img src="https://basededatostec.github.io/img/47normalizado.png">

### 4.7 OTRAS FORMAS NORMALES

<p style="text-align: justify;">Tomemos por ejemplo la <b>tabla Agenda</b>, dejando sólo los atributos multivaluados:

<b>Agenda</b>(nombre, teléfono, correo)

<br><br>Lo primero que debemos hacer es buscar las <b>claves</b> y las <b>dependencias</b>. Recordemos que las claves candidatas deben identificar de <b>forma unívoca</b> cada tupla. De modo que estamos obligados a usar los tres atributos para formar la clave candidata.

<br><br>Pero las dependencias que tenemos son:
<br>nombre ->-> <b>teléfono</b>
<br>nombre ->-> <b>correo</b>

<br><br>Y nombre no es <b>clave candidata</b> de esta relación.

<br><br>Debemos separar esta relación en varias, tantas como atributos multivaluados tenga.
<br><b>Teléfonos</b>(nombre, teléfono)
<br><b>Correos</b>(nombre, correo)

<br><br>Ahora en las dos relaciones se cumple la cuarta forma normal.</p>

__QUINTA FORMA NORMAL 5FN__

<p style="text-align: justify;">Existe una quinta forma normal, sirve para <b>eliminar dependencias de proyección</b>, que raramente se encuentran en las bases de datos vistas con regularidad.</p>

__Fuentes de información__

[Modelo Relacional: Normalización](http://valdezesquivel-bd.blogspot.mx/2014/09/actividad-8.html "fuente")

[Normalización de Bases de Datos](https://cvva.wordpress.com/2007/12/04/normalizacion-de-bases-de-datos-las-3-formas-normales/ "fuente")

|  Acerca de: | 
| :------ | 
| Éste es un sitio creado por estudiantes del Instituto Tecnológico de Pachuca, para la asignatura en curso; Fundamentos de Bases de Datos. | 
| Equipo New Jackers: Hernández Salinas Lucio y Sanchez Casañas Jose María |
| <a href="https://basededatostec.github.io/unidadcuatro/">Actividades Unidad 4</a> |

