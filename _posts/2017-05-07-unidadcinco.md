---
layout: post
title: Unidad 5
subtitle: Algebra relacional 
tags: [unidad cinco, resumen, introducción, algebra relacional]
---
<p style="text-align: justify;">El álgebra relacional consiste de algunas simples maneras de construir <b>nuevas relaciones</b> a partir de otras. Si pensamos que las relaciones iniciales son los <B>datos almacenados</B>, las nuevas relaciones se pueden ver como respuestas a algunas consultas deseadas.

<br><br>Es un lenguaje de consulta procedural. Consta de un <b>conjunto de operaciones</b> que toman como entrada una o dos relaciones y producen como resultado una nueva relación, por lo tanto, es posible <b>unir</b> y <b>combinar operadores</b>. Hay ocho operadores en el álgebra relacional que construyen relaciones y manipulan datos.</p>

### 5.1 OPERACIONES FUNDAMENTALES DEL ÁLGEBRA RELACIONAL

<p style="text-align: justify;">Ocho operadores, algunos de ellos son <b>básicos</b> o <b>fundamentales</b> y otros son <b>derivados</b> o forman parte de los operadores de extensión del álgebra relacional.</p>

<img src="https://basededatostec.github.io/img/50algebra.png">

### Selección

<p style="text-align: justify;">El operador de selección opta por tuplas que satisfagan cierto predicado, se utiliza la letra griega sigma minúscula <b>(σ)</b> para señalar la selección. El predicado aparece como <b>subíndice de σ</b>. La Relación que constituye el argumento se da entre paréntesis después de la <b>σ</b>. Utiliza operadores lógicos y matemáticos.</p>

Formato: <b>σ (condición) (R)</b> Nombre de la Relación

__EJEMPLO__

<img src="https://basededatostec.github.io/img/51algebra.png">

### Proyección

<p style="text-align: justify;">La operación de proyección permite <b>quitar ciertos atributos</b> de la relación, esta operación es unaria, copiando su relación base dada como argumento y quitando ciertas columnas, La proyección se señala con la letra griega pi
mayúscula <b>(Π)</b>. Como subíndice de <b>Π</b> se coloca una <b>lista de todos los atributos</b> que se desea aparezcan en el resultado. La relación argumento se escribe después de <b>Π</b> entre paréntesis.</p>

Formato: <b>π lista de atributos (R)</b> Nombre de la Relación

__EJEMPLO__

<img src="https://basededatostec.github.io/img/52algebra.png">

### Unión

<p style="text-align: justify;">Conjunto de todas las tuplas que pertenecen ya sea a A o a B o a Ambas. Al igual que en teoría de conjuntos el <b>símbolo ∪</b> representa aquí la <b>unión</b> de dos relaciones.</p>

<p style="text-align: justify;">Al adaptar los operadores de conjuntos a relaciones se debe asegurar que exista compatibilidad entre ellas.</p>
- Tienen el mismo grado.
- Los atributos tienen el mismo nombre.
- El dominio del atributo-i de R es el mismo que el dominio del atributo-i en S, ∀i

Formato: <b> R ∪ S</b>

__EJEMPLO__

<img src="https://basededatostec.github.io/img/53algebra.png">

### Diferencia

<p style="text-align: justify;">Produce el conjunto de todas las tuplas t que <b>pertenecen</b> a <b>A</b> y <b>no pertenecen</b> a <b>B</b>, el simbolo utilizado es el clasio de la resta <b>-</b>. </p>

Formato: <b> R - S</b>

__EJEMPLO__

<img src="https://basededatostec.github.io/img/54algebra.png">

### Producto cartesiano

<p style="text-align: justify;">Produce el conjunto de todas las tuplas t tales que t es el encadenamiento de una tupla <b>a</b> perteneciente a <b>A</b> y de una <b>b</b> que pertenece a <b>B</b>. se utiliza el <b>símbolo X</b> para representar el producto.

<br><br>Si R y S tienen atributos en común es necesario renombrarlos. Para evitar ambigüedades se precede el nombre del atributo con el nombre de la relación.</p>

Formato: <b> R X S</b>

__EJEMPLO__

<img src="https://basededatostec.github.io/img/55algebra.png">
