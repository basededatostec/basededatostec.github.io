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

<p style="text-align: justify;">Produce el conjunto de todas las tuplas t tales que t es el encadenamiento de una tupla <b>a</b> perteneciente a <b>A</b> y de una <b>b</b> que pertenece a <b>B</b>. se utiliza el <b>símbolo X</b> para representar el producto. Si R y S tienen atributos en común se <b>renombran</b>. Para evitar <b>ambigüedades</b> se precede el nombre del atributo con el nombre de la relación.</p>

Formato: <b> R X S</b>

__EJEMPLO__

<img src="https://basededatostec.github.io/img/55algebra.png">

### Intersección

<p style="text-align: justify;">Produce el conjunto de todas las tuplas <b>pertenecientes</b> a <b>A</b> y <b>B</b>. Al igual que en teoría de conjuntos el símbolo ∩ representa aquí la <b>intersección entre dos relaciones</b>. Dentro del conjunto de operaciones en el álgebra relacional aparecen estas operaciones que no añaden potencia al algebra, pero simplifican las consultas habituales.</p>

Cada operación re-emplaza un conjunto de operaciones “normales”.

- Intersección de conjuntos
- Reunión natural
- División

Formato: <b> R ∩ S = R – (R – S)</b>

__EJEMPLO__

<img src="https://basededatostec.github.io/img/56algebra.png">

### Join

<p style="text-align: justify;">El <b>JOIN Naturral</b> es una operación binaria que permite <b>combinar ciertas selecciones</b> y un <b>producto cartesiano</b> en una sola operación. Se denota por el símbolo: <b>⋈</b> </p>

La reunión natural expresada en operaciones básicas equivale a:

R (X1;X2; ... Xm; Y1;Y2; ... ;Yn)
<br>S (Y1;Y2; ... ;Yn; Z1; Z2; ... ; Zp)

<p style="text-align: justify;">Relación con atributos <b>X</b>, <b>Y</b>, <b>Z</b> y poblado por el <b>conjunto</b> de tuplas que <b>tienen igual valor</b> de Y en R y en S. π R U S (σ R.Y1=S.Y1 ^ R.Y2=S.Y2 ^...^ R.Yn=S.Yn (R X S))</p>

__EJEMPLO__

<img src="https://basededatostec.github.io/img/57algebra.png">

__Θ - Join__

<p style="text-align: justify;">Equivalente al <b>Join</b> sólo que se permite usar cualquier condición de comparación. <b>θ</b>.</p>

El resultado se construye:

- Toma el R X S
- Selecciona sólo las tuplas que satisfacen a θ.

Formato: <b> R ⋈θ S</b>

__EJEMPLO__

<img src="https://basededatostec.github.io/img/58algebra.png">

### División

<p style="text-align: justify;">Sean <b>R</b> y <b>S</b> dos relaciones con esquemas:

<br><br>(A1, ... ,An;B1, ... ,Bm) y (B1, ... , Bm) respectivamente.</p>

La operación: <B>(R ÷ S)</B> da como resultado otra relación.

- cuyo esquema es (A1, ... ,An)
- las tuplas tomadas a partir de las de r (R) tales que su valor (a1, ... ,an) está asociado en r (R) con TODOS los valores (b1, ... ,bm) que están en s (S)

Formato: <b> (R ÷ S)</b>

__EJEMPLO__

<img src="https://basededatostec.github.io/img/59algebra.png">


### 5.2 ÁLGEBRA RELACIONAL EXTENDIDA


<p style="text-align: justify;"><b>1.-</b> Una de las extensiones es permitir operaciones aritméticas como parte de la operación proyección (Proyección Generalizada).

<br><br><b>2.-</b> Permitir operaciones de agregación.

<br><br><b>PROYECCIÓN GENERALIZADA</b>

<br><br>Amplía la proyección permitiendo que se utilicen <b>funciones aritméticas</b> en la lista de proyección. La operación proyección generalizada tiene la forma siguiente:

<br><br><b>πF1, F2, ... ,Fn (E)</b>

<br><br>donde <b>E</b> es cualquier expresión del álgebra relacional y F1, F2, ... ,Fn son expresiones aritméticas que incluyen constantes y atributos pertenecientes al esquema E. Como caso especial la <b>expresión aritmética</b> puede ser simplemente un atributo o una constante. Cuando se hace uso de esta operación generalizada se recomienda dar nombre al atributo o columna generada con la función que se aplique.

<br><br>Ejemplo: Suponga el esquema <b>Tarjeta_credito</b> (num-tarjeta, credito-disponible, limite-credito, vigencia, tipo) y se desea conocer lo gastado.</p>

<img src="https://basededatostec.github.io/img/555algebra.png">


<p style="text-align: justify;">π num-tarjeta, (limite-credito - credito-disponible) AS credito-utilizado (Tarjeta_credito) la relación o esquema resultante sería a manera de ejemplo claro esta:</p>

<img src="https://basededatostec.github.io/img/556algebra.png">

<p style="text-align: justify;"><b>Funciones de agregación</b>

<br><br>Este tipo de operaciones se pueden como su nombre lo dice agregar a la operación de proyección, dichas operaciones toman un conjunto de valores y retornan o proyectan un valor ÚNICO. Las operaciones que veremos son:

<br><br>-SUM: retorna la suma de los valores
<br>-AVG: retorna la media de los valores
<br>-MIN: retorna el mínimo de los valores
<br>-MAX: retorna el máximo de los valores
<br>-COUNT: retorna el número de elementos del conjunto
<br><br>La forma general:
<br><br>g1, g2…gn G f1(a1), f2(a2).. Fm(am)(E)

<br><br>Donde:

<br><br>g1,g2,…gn constituye la lista de atributos que indica como se realiza la agrupación.

<br><br>i es una función de agregación y ai es un nombre del atributo.

<br><br>Considere el siguiente esquema Tarjeta-credito:</p>

<img src="https://basededatostec.github.io/img/557algebra.png">

<p style="text-align: justify;">Ejemplo de SUM

Supongamos que nos interesa conocer el total de credito que se otorga a todos los clientes.

G sum(limite-credito) (Tarjeta-credito)</p>

<img src="https://basededatostec.github.io/img/558algebra.png">

<p style="text-align: justify;">Ahora si deseamos conocer el total de los limites de créditos por tipo de tarjeta tendriamos lo siguiente:

tipo G tipo, sum(limite-credito) AS total-credito-tipo (Tarjeta-credito)</p>

<img src="https://basededatostec.github.io/img/559algebra.png">

<p style="text-align: justify;">Ejemplo de AVG

Supongase que se desea calcular el promedio de los créditos disponibles.

G avg(credito-disponible) (Tarjeta-credito)</p>
