---
layout: post
title: Unidad 6
subtitle: Introducción al lenguaje SQL
tags: [unidad seis, resumen, sql]
---

### 6.1 Características

<p style="text-align: justify;">En informática, cuando se quiere hacer uso de un <b>lenguaje de programaicón</b> se requiere de una sintáxis para escribir de forma correcta cada una de las instrucciones. Para escribirlas adecuadamente se debe respetar una notación, es decir, las reglas que permiten la construcción de <b>instrucciones válidas</b>, en este caso, instrucciones que el compilador o interprete de comando sea capaz de "entender" y hacer lo que nosotros estamos indicando.

<br><br>SQL es un lenguaje de consulta estrcuturado (Structured Query Language), se subdivide en otros lenguajes tales como:

<br><br><b>SDDL</b>: Lenguaje de deifinición de datos: crear las estructuras físicas donde se <b>almacenarán los objetos</b> de las bases de datos, crear tablas, índices, vistas, entre otros objetos de la base de datos.

<br><br><b>SDML</b>: Lenguaje de manipulación de datos: contiene de las funciones para la consulta de información de la base de datos (SELECT), también contiene <b>DELETE</b> para el borrado de datos, <b>UPDATE</b> para actualizar información, <b>INSERT</b> para insertar a la base de datos registros.</p>

### 6.2 Lenguaje de Definición de Datos (DDL)

<p style="text-align: justify;">Cuando se escriben sentencias SQL se recomienda por estandar que las palabras reservadas del lenguaje ya sea <b>DDL</b> o <b>DML</b> se escriban en mayúsculas.

<br><br>DDL tiene tres instrucciones básicas:

<br><br><b>CREATE</b> tipo_objeto Nombre Definición. Crea un objeto de un determinado tipo (DATABASE, TABLE, INDEX, etc.) con un nombre (por ejemplo Inventarios, Libros, Autores, etc.) y una definición (CodigoA, Nombre, etc.).

<br><br><b>DROP</b> tipo_objeto Nombre. Elimina un tipo de objeto  especificado mediante un nombre. Por ejemplo, la sentencia <b>DROP TABLE</b> Autores, borraría de la base de datos la tabla Autores junto con todos sus datos.

<br><br><b>ALTER</b> tipo_objeto Nombre Modificación. Modifica la definición de un objeto. Por ejemplo, la sentencia <b>ALTER TABLE</b> Autores <b>DROP COLUMN</b> nacionalidad, elminaría la columna nacionalidad de la tabla Autores.</p>

### DROP

<p style="text-align: justify;">El comando DROP es usado para el barrado de diversos objetos como tablas, indices y la propia base de datos.

<br><br>La sintaxis es muy sencilla y se muestra a continuación:

<br><br>Veamos los ejemplos:

<br><br><b>DROP DATABASE Blibioteca:</b>

<br><br>La instrucción anterior borrara toda la base de datos llamada Biblioteca.

<br><br><b>DROP TABLE Libro;</b>

<br><br>Esta instrucción realiza el borrado de la tabla Libro.

<br><br><b>DROP {DATABASE | SCHEMA | TABLE} nombre_del_objeto</b></p>

### ALTER

<p style="text-align: justify;">Esta sentencia se utiliza para modificar la estructura de una tabla ya existente, mediante de esta podemos añadir, borrar y modificar los campos de nuestra tabla. 

<br><br>Su sintaxis es:

<br><br><b>ALTER [ONLINE] [IGNORE] TABLE tbl_name
alter_specification [, alter_specification]</b>
<br><br>Veamos algunos ejemplos:

<br><br>Renombrar Tabla: Se utiliza para cambiar el nombre a una tabla la sintaxis es:
<br><br>ALTER TABLE Libro RENAME TO ejemplares;

<br><br>Añadir un campo (ADD COLUMN): Como su nombre lo indica nos permite añadir un campo a una tabla que ya habíamos creado, un ejemplo de su uso:
<br><br>ALTER TABLE Libro ADD COLUMN year_edición INT(4) NOT NULL;</p>



