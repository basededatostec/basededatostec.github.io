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
<br>3.- Está fundamentado en una base matemática.

<br><br>En una base de datos relacional, los datos son recolectados mediante <b>relaciones</b>, y éstas a su vez son generalmente <b>representadas mediante tablas</b>. Una relación es un conjunto de <b>atributos</b>, cada uno de los cuales pertenece a un <b>dominio</b>, y que posee un nombre que identifica la relación. Se representa gráficamente mediante una tabla con <b>columnas</b> y <b>filas</b>. Para transformar un modelo diagrama-entidad relación a un modelo relacional, debemos conocer su estructura y algunos conceptos basicos:

<br><br><b>TABLAS</b>

<br><br>El modelo relacional proporciona una manera de <b>representar los datos</b>: una tabla bidimensional llamada relación. La relación Películas <b>maneja la información de las instancias</b> en la entidad Películas, cada renglón corresponde a una entidad película y cada columna corresponde a uno de los atributos de la entidad.

<center><img src="https://basededatostec.github.io/img/30relacional.png"></center>

<br><b>ATRIBUTOS</b>

<br><br>Los atributos son las columnas de un relación y describen <b>características</b> particulares, por ejemplo el color o tamaño de un artículo, el apellido, etc.

<br><br><b>TUPLAS</b>

<br><br>Cada uno de los renglones en una relación conteniendo <b>valores</b> para cada uno de los atributos.
(Star Wars, 1977, 124, color)

<br><br><b>DOMINIO</b>

<br><br>Conjunto de <b>valores permitidos</b> para un atributo, por ejemplo, cadenas de caracteres, números para la edad, valores como SI o NO, Masculino-Femenino, etc.

<br><br><b>CABECERA</b>

<br><br>Un conjunto de <b>atributos</b> de una relación conforma la cabecera de la relación.
Id-cliente nombre apellido-paterno apellido-materno 

<br><br><b>GRADO</b>

<br><br>Es el <b>número de columnas</b> que conforman la relación, este valor no cambia por lo que se dice es estático, solo puede ser modificado por necesidad de la organización.

<br><br><b>CARDINALIDAD</b>

<br><br>Es el <b>número de tuplas</b> o filas de una relación, este valor cambia de manera constante por lo que es dinámico, y que depende del agregado o eliminación de relaciones o tuplas.<br>

<center><img src="https://basededatostec.github.io/img/31relacional.jpg"></center>
<br><b>CLAVE</b>

<br><br>Una clave es un <b>conjunto de atributos</b> que identifican de forma única una ocurrencia de entidad. En este caso las claves pueden ser simples o compuestas.

<br><br><b>Superclave</b>: Identifican a una entidad (pueden ser no mínimas). Por ejemplo, el número-seguridad-social. O bien compuestas como RFC+Número-seguridad-social.

<br><br><b>Clave Candidata</b>: Es la mínima superclave, por ejemplo puede ser sólo el CURP.

<br><br><b>Clave Primaria (PK)</b>: Es la clave candidata elegida por el diseñador como clave definitiva.</p>

<p style="text-align: justify;"><br><br><b>Clave foránea (FK)</b>: Es un atributo de una entidad, que es la clave en otra entidad. Por ejemplo, el Id en la entidad Asignatura corresponde a una clave en otra entidad, como puderia ser Datos-Alumnos. Es una clave foránea en la tabla Asignatura.</p>

### 3.1 CONVERSIÓN DE MODELO E-R A MODELO RELACIONAL

<p style="text-align: justify;">Existen algunas reglas antes de convertir un modelo E-R a un modelo relacional.

<br><br><b>TODA ENTIDAD SE CONVIERTE A UNA RELACIÓN</b>

<br><br>Cada que encontremos una entidad en un modelo entidad relación, está debe ser convertida en una relación dentro del modelo relacional, la cual se representa mediante una tabla con <b>tres columnas</b> y un numero <b>indefinido</b> de filas.

<br><br>Esta a su vez tendrá como <b>encabezad</b> o el nombre de la entidad . buscamos el atributo identificador que se colocara en la primera fila de nuestra tabla, representando con el <b>prefijo PK</b>, que significa <b>llave primaria</b>. Ya después se colocan los demás atributos en las filas siguientes. Y en la tercer columna colocaremos una <b>N</b> porque el campo no puede contener valores nulos y una <b>S</b> si puede contenerlos.

<br><br><b>EN TODA INTERRELACIÓN DE UNO A MUCHOS SE PROPAGA LA LLAVE PRIMARIA</b>

<br><br>Cada que encontremos una interrelación de uno a muchos se debe realizar lo siguiente; al encontrar dos entidades por ejemplo, debemos convertir estas entidades a relaciones, y observamos cual es cardinalidad, para este caso es de 1 a muchos , se agrega un flecha apuntando hacia la izquierda para tener la cardinalidad entre nuestras relaciones, ahora si podemos realizar la propagación de la llave primaria.

<br><br>La relación que apunta con la flecha va a jalar la llave primaria de la relación a la que esta apuntando, cuando se toma la llave primaria de la relación apuntada se copia en la segunda relación pero en lugar de colocar PK se coloca FK, que significa llave foránea.

<br><br>TODA INTERRELACIÓN DE MUCHOS A MUCHOS SE CONVIERTE EN UNA RELACIÓN

<br><br>En una relación de muchos a muchos se deben aplicar todas las reglas posibles, convertir las entidades en relaciones, colocar las columnas y filas con los datos correspondientes,, la cardinalidad se cambia, se cambia de muchos a muchos a 1, imaginemos que quedan tren relaciones, la relación de en medio tendrá una cardinalidad de muchos a 1 con las dos relaciones que están a su costado, por lo que dicha relación jalara las llaves primarias de estas dos, pasando a ser llaves compuestas.</p>
