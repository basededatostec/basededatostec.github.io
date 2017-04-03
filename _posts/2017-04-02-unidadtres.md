---
layout: post
title: Unidad 3
subtitle: Modelo relacional
tags: [unidad tres, resumen, modelo relacional]
---
### 3.1 INTRODUCCIÓN AL MODELO RELACIONAL

<p style="text-align: justify;">El <b>objetivo del modelo relacional</b> es proteger al usuario de la obligación de conocer la estructura física de los datos. Sus características principales son:

<br><br>1.- La relación es el elemento fundamental del modelo.
<br>2.- Es independiente de la forma en que se almacenan los datos y su representación.
<br>3.- Esta fundamentado en una base matemática.

<br><br>En una base de datos relacional, los datos son recolectados mediante <b>relaciones</b>, y éstas a su vez son generalmente <b>representadas mediante tablas</b>. Una relación es un conjunto de <b>atributos</b>, cada uno de los cuales pertenece a un <b>dominio</b>, y que posee un nombre que identifica la relación. Se representa gráficamente mediante una tabla con <b>columnas</b> y <b>filas</b>. Para transformar un modelo diagrama-entidad relación a un modelo relacional, debemos conocer su estructura y algunos conceptos basicos:

<br><br><b>TABLAS</b>

<br><br>El modelo relacional proporciona una manera de <b>representar los datos</b>: una tabla bidimensional llamada relación. La relación Películas <b>maneja la información de las instancias</b> en la entidad Películas, cada renglón corresponde a una entidad película y cada columna corresponde a uno de los atributos de la entidad.<br><br>

<img src="https://basededatostec.github.io/img/30relacional.png">

<br><br><b>ATRIBUTOS</b>

<br><br>Los atributos son las columnas de un relación y describen <b>características</b> particulares, por ejemplo el color o tamaño de un artículo, el apellido, etc.

<br><br><b>TUPLAS</b>

<br><br>Cada uno de los renglones en una relación conteniendo <b>valores</b> para cada uno de los atributos.
(Star Wars, 1977, 124, color)

<br><br><b>DOMINIO</b>

<br><br>Conjunto de valores permitidos para un atributo, por ejemplo, cadenas de caracteres, números para la edad, valores como SI o NO, Masculino-Femenino, valores de fecha (dd-mm-aaaa), etc..

<br><br><b>CABECERA</b>

<br><br>Un conjunto de <b>atributos</b> de una relación conforma la cabecera de la relación.
Id-cliente nombre apellido-paterno apellido-materno 

<br><br><b>GRADO</b>

Es el número de columnas que conforman la relación, este valor no cambia por lo que se dice es estático, solo puede ser modificado por necesidad de la organización.

<br><br><b>CARDINALIDAD</b>

Es el número de tuplas o filas de una relación, este valor cambia de manera constante por lo que es dinámico, y que depende del agregado o eliminación de relaciones o tuplas.

<br><br><b>CLAVE</b>

<br><br>Una clave es un conjunto de atributos que identifican de forma única una ocurrencia de entidad. En este caso las claves pueden ser simples o compuestas.

<br><br>Superclave: Identifican a una entidad (pueden ser no mínimas). Por ejemplo, el número-seguridad-social, CURP. O bien compuestas como RFC+Número-seguridad-social.

<br><br>Clave Candidata: Es la mínima superclave, por ejemplo puede ser solo el RFC, CURP, entre otros.

<br><br>Clave Primaria (PK): Es la clave candidata elegida por el diseñador como clave definitiva.

<br><br>Clave foránea (FK): Es un atributo de una entidad, que es la CLAVE en otra entidad. Por ejemplo, el NC (número de control) en la entidad Asignatura corresponde a una clave en otra entidad, como puderia ser Datos-alumnos. En este caso es una clave foránea en la tabla Asignatura.


</p>
