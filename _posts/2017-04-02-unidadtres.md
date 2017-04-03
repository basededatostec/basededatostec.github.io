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

<br><br>El modelo relacional proporciona una manera de <b>representar los datos</b>: una tabla bidimensional llamada relación. La relación Películas <b>maneja la información de las instancias</b> en la entidad Películas, cada renglón corresponde a una entidad película y cada columna corresponde a uno de los atributos de la entidad.</p>

<center><img src="https://basededatostec.github.io/img/30relacional.png"></center>
<p style="text-align: justify;"><b>ATRIBUTOS</b>

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

<br><br>Es el <b>número de tuplas</b> o filas de una relación, este valor cambia de manera constante por lo que es dinámico, y que depende del agregado o eliminación de relaciones o tuplas.<br></p>

<center><img src="https://basededatostec.github.io/img/31relacional.jpg"></center>
<b>CLAVE</b>

<p style="text-align: justify;">Una clave es un <b>conjunto de atributos</b> que identifican de forma única una ocurrencia de entidad. En este caso las claves pueden ser simples o compuestas.

<br><br><b>Superclave</b>: Identifican a una entidad (pueden ser no mínimas). Por ejemplo, el número-seguridad-social. O bien compuestas como RFC+Número-seguridad-social.

<br><br><b>Clave Candidata</b>: Es la mínima superclave, por ejemplo puede ser sólo el CURP.

<br><br><b>Clave Primaria (PK)</b>: Es la clave candidata elegida por el diseñador como clave definitiva.

<br><br><b>Clave foránea (FK)</b>: Es un atributo de una entidad, que es la clave en otra entidad. Por ejemplo, el Id en la entidad Asignatura corresponde a una clave en otra entidad, como puderia ser Datos-Alumnos. Es una clave foránea en la tabla Asignatura.</p>

### 3.2 CONVERSIÓN DE MODELO E-R A MODELO RELACIONAL

<p style="text-align: justify;">Existen algunas reglas antes de convertir un modelo E-R a un modelo relacional.

<br><br><b>TODA ENTIDAD SE CONVIERTE A UNA RELACIÓN</b>

<br><br>Cada que encontremos una entidad en un modelo entidad relación, está debe ser convertida en una relación dentro del modelo relacional, la cual se representa mediante una tabla con <b>tres columnas</b> y un numero <b>indefinido</b> de filas.

<br><br>Esta a su vez tendrá como <b>encabezad</b> o el nombre de la entidad . buscamos el atributo identificador que se colocara en la primera fila de nuestra tabla, representando con el <b>prefijo PK</b>, que significa <b>llave primaria</b>. Ya después se colocan los demás atributos en las filas siguientes. Y en la tercer columna colocaremos una <b>N</b> porque el campo no puede contener valores nulos y una <b>S</b> si puede contenerlos.

<br><br><b>EN TODA INTERRELACIÓN DE UNO A MUCHOS SE PROPAGA LA LLAVE PRIMARIA</b>

<br><br>Cada que encontremos una <b>interrelación de uno a muchos</b> se debe realizar lo siguiente; al encontrar dos entidades por ejemplo, debemos convertir estas entidades a relaciones, y observamos cual es <b>cardinalidad</b>, para este caso es de uno a muchos , se agrega un <b>flecha apuntando hacia la izquierda</b> para tener la cardinalidad entre nuestras relaciones, ahora si podemos realizar la propagación de la llave primaria.

<br><br>La relación que apunta con la flecha va a jalar la llave primaria de la relación a la que esta apuntando, cuando se toma la llave primaria de la relación apuntada se copia en la segunda relación pero en lugar de colocar <b>PK se coloca FK</b>, que significa llave foránea.

<br><br><b>TODA INTERRELACIÓN DE MUCHOS A MUCHOS SE CONVIERTE EN UNA RELACIÓN</b>

<br><br>En una <b>relación de muchos a muchos</b> se deben aplicar todas las reglas posibles, convertir las entidades en relaciones, colocar las columnas y filas con los datos correspondientes,, la cardinalidad se cambia, se cambia de <b>muchos a muchos a uno</b>, imaginemos que quedan tres relaciones, la relación de en medio tendrá una cardinalidad de muchos a uno con las dos relaciones que están a su costado, por lo que dicha relación jalara las llaves primarias de estas dos, pasando a ser <b>llaves compuestas</b>.</p>
<center><iframe width="560" height="315" src="https://www.youtube.com/embed/s9zOOxIZnYI" frameborder="0" allowfullscreen></iframe></center>

### 3.3 ESQUEMA DE LA BASE DE DATOS

<p style="text-align: justify;">El Esquema de una Base de datos <b>describe la estructura</b> de dicha base con la que se este trabajando, define sus <b>tablas</b>, sus <b>campos</b> en cada tabla y las <b>relaciones</b> entre cada campo y cada tabla. A su vez el es almacenado en un Diccionario de Datos.

<br><br><b>NIVELES DE ESQUEMA DE BASE DE DATOS</b>

<br><br>Esquema <b>Conceptual</b>, un mapa de conceptos y sus relaciones.
<br>Esquema<b> Lógico</b>, un mapa de las entidades y sus atributos y las relaciones.
<br>Esquema <b>Físico</b>, una aplicación de un esquema lógico.
<br>Esquema <b>Objeto</b>, Base da datos Oracle Objeto.

<br><br>Resulta conveniente dar un <b>nombre a los esquemas</b> de las relaciones, igual que se dan nombres a las definiciones de tipos en los lenguajes de programación. Se adopta el convenio de utilizar <b>nombres en minúsculas</b> para las relaciones y nombres que comiencen por una letra mayúscula para los <b>esquemas</b> de las relaciones. Siguiendo esta notación se utilizará Esquema-cuenta como ejemplo:

<br><br><b>Esquema-cuenta</b> = (número-cuenta, nombre-sucursal, saldo)

<br><br>Los esquemas de las relaciones incluyen una <b>lista de los atributos</b> y de sus dominios correspondientes. Siguiendo con el ejemplo de la relación sucursal. Observemos que el esquema de esa relación es la siguiente:

<br><br><b>Esquema-relación</b> = (nombre-sucursal, ciudad-sucursal, activos)

<br><br>Obsérvese que el atributo <b>nombre de la sucursal</b> aparece tanto en <b>Esquema-sucursal</b> como en <b>Esquema-cuenta</b>. Esta duplicidad no es una coincidencia. Utiliza lo atributos comunes en los esquemas de las relaciones es una manera de relacionar las tuplas de relaciones diferentes. Supóngase que se desea obtener información sobre todas las cuentas abiertas en sucursales ubicadas en Arganzuela.</p>

<center><img src="https://basededatostec.github.io/img/32relacional.jpg"></center>

<p style="text-align: justify;">Primero se busca en la <b>relación sucursal</b>para encontrar los nombres de todas las sucursales sitas en Arganzuela. Luego, para cada una de ellas, se mira en la relación cuenta para encontrar la información sobre las cuentas abiertas en esa sucursal. Esto no es sorprendente: recuérdese que los atributos que forma la <b>clave primaria</b> de un conjunto de entidades fuertes aparecen en la tabla creada para representar el <b>conjunto de entidades</b>, así como en las tablas creadas para crear relaciones en las que participar el conjunto de entidades.</p>
