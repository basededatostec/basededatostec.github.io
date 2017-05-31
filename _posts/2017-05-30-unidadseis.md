---
layout: post
title: Unidad 6
subtitle: Introducción al lenguaje SQL
tags: [unidad seis, resumen, sql]
---

### 6.1 CARACTERÍSTICAS

<p style="text-align: justify;">En informática, cuando se quiere hacer uso de un <b>lenguaje de programaicón</b> se requiere de una sintáxis para escribir de forma correcta cada una de las instrucciones. Para escribirlas adecuadamente se debe respetar una notación, es decir, las reglas que permiten la construcción de <b>instrucciones válidas</b>, en este caso, instrucciones que el compilador o sea capaz de entender.

<br><br>SQL es un lenguaje de consulta estrcuturado (Structured Query Language), se subdivide en otros lenguajes tales como:

<br><br><b>SDDL</b>: Lenguaje de deifinición de datos: crear las estructuras físicas donde se <b>almacenarán los objetos</b> de las bases de datos, crear tablas, índices, entre otros..

<br><br><b>SDML</b>: Lenguaje de manipulación de datos: contiene de las funciones para la consulta de información <b>SELECT</b>, también contiene <b>DELETE</b> para el borrado de datos, <b>UPDATE</b> para actualizar información, <b>INSERT</b> para insertar a la base de datos registros.</p>

### 6.2 LENGUAJE DE DEFINICIÓN DE DATOS(DDL)

<p style="text-align: justify;">Cuando se escriben sentencias SQL se recomienda por estandar que las palabras reservadas del lenguaje ya sea <b>DDL</b> o <b>DML</b> se escriban en mayúsculas.

<br><br>DDL tiene tres instrucciones básicas:

<br><br><b>CREATE</b> tipo_objeto Nombre Definición. Crea un objeto de un determinado tipo (DATABASE, TABLE, INDEX, etc.) con un nombre (por ejemplo Inventarios, Libros, Autores, etc.) y una definición (CodigoA, Nombre, etc.).

<br><br><b>DROP</b> tipo_objeto Nombre. Elimina un tipo de objeto  especificado mediante un nombre. Por ejemplo, la sentencia <b>DROP TABLE</b> Autores, borraría de la base de datos la tabla Autores junto con todos sus datos.

<br><br><b>ALTER</b> tipo_objeto Nombre Modificación. Modifica la definición de un objeto. Por ejemplo, la sentencia <b>ALTER TABLE</b> Autores <b>DROP COLUMN</b> nacionalidad, elminaría la columna nacionalidad de la tabla Autores.</p>

### DROP

<p style="text-align: justify;">El comando DROP es usado para el barrado de diversos objetos como tablas, indices y la propia base de datos.

<br><br>La sintaxis es muy sencilla y se muestra a continuación:

<br><br><b>DROP {DATABASE | SCHEMA | TABLE} nombre_del_objeto</b>

<br><br>Veamos los ejemplos:

<br><br><b>DROP DATABASE Blibioteca:</b>

<br><br>La instrucción anterior borrara toda la base de datos llamada Biblioteca.

<br><br><b>DROP TABLE Libro;</b>

<br><br>Esta instrucción realiza el borrado de la tabla Libro.</p>

### ALTER

<p style="text-align: justify;">Esta sentencia se utiliza para modificar la estructura de una tabla ya existente, mediante de esta podemos añadir, borrar y modificar los campos de nuestra tabla. 

<br><br>Su sintaxis es:

<br><br><b>ALTER [ONLINE] [IGNORE] TABLE tbl_name
alter_specification [, alter_specification]</b>
<br><br>Veamos algunos ejemplos:

<br><br>Renombrar Tabla: Se utiliza para cambiar el nombre a una tabla la sintaxis es:
<br><br><b>ALTER TABLE Libro RENAME TO ejemplares;</b>

<br><br>Añadir un campo (ADD COLUMN): Como su nombre lo indica nos permite añadir un campo a una tabla que ya habíamos creado, un ejemplo de su uso:
<br><br><b>ALTER TABLE Libro ADD COLUMN year_edición INT(4) NOT NULL;</b></p>

### CREATE

<p style="text-align: justify;">Se utiliza para crear una nueva base de datos vacía.

<br><br>Su sintaxis es la siguiente:

<br><br><b>CREATE [OR REPLACE] {DATABASE | SCHEMA} [IF NOT EXISTS] db_name
[create_specification] </b>
    
<br><br>Ejemplos:

<br><br>Si deseamos crear una base de datos llamada Libros escribimos lo siguiente:

<br><br><b>CREATE DATABASE Biblioteca;</b>

<br><br>Si deseamos crear una tabla llamada Libros escribimos lo siguiente:

<br><br><b>CREATE DATABASE Libros;</b></p>

### 6.3 LENGUAJE DE MANIPULACIÓN DE DATOS (LMD)


<p style="text-align: justify;">Las sentencias de lenguaje de manipulación de datos (DML) son utilizadas para gestionar datos dentro de los esquemas o relaciones de la base de datos.

<br><br>Existen diversos comandos del sub lenguaje LMD perteneciente al lenguaje SQL, en esta lección veremos los siguientes:</p>

<img src ="https://basededatostec.github.io/img/borra.png">


<p style="text-align: justify;">Los comandos para que adquieran mayor potencialidad pueden ser usados con diversas clausulas, las cuales son condiciones de modificación utilizadas para definir los datos que desea seleccionar o manipular.</p>

<img src ="https://basededatostec.github.io/img/borra2.png">

<p style="text-align: justify;">Además de las cláusulas se pueden emplear dentro de las condiciones tanto operadores lógicos como relaciones para poder realizar búsquedas avanzadas o mas precisas.

<br><br>Los operadores a emplear dentro de esta lección son lo siguientes:

<br><br>Operadores lógicos.</p>

<img src ="https://basededatostec.github.io/img/borrame3.png">

<p style="text-align: justify;">Operadores Relacionales.</p>

<img src ="https://basededatostec.github.io/img/borrame4.png">

__Fuentes de información__

[Fundamentos de Bases de Datos](http://fundamentosbditp.blogspot.mx/p/blog-page_16.html "fuente")

|  Acerca de: | 
| :------ | 
| Éste es un sitio creado por estudiantes del Instituto Tecnológico de Pachuca, para la asignatura en curso; Fundamentos de Bases de Datos. | 
| Equipo New Jackers: Hernández Salinas Lucio y Sanchez Casañas Jose María |
| <a href="https://basededatostec.github.io/unidadseis/">Actividades Unidad 6</a> |







