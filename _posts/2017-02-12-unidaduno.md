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

Un modelo de datos es <b>una descripción</b> de algo conocido como contenedor de datos, así como de los métodos para almacenar y recuperar información deesos contenedores. Los modelos de datos <b>no son físicos</b>: son abstracciones que permiten la implementación de un sistema eficiente de base de datos</p>

Algunos modelos con frecuencia utilizados en las bases de datos:


Dentro de los modelos e xistentes hoy en día podemos hacer dos clasificaciones:

Modelos de diseño: Predomina el modelo “Entidad/relación”.

Modelos de representación:

Primero apareció el modelo jerárquico o de tipo árbol.

<p style="text-align: justify;">Posteriormente se evolucionó hacia el modelo de red en el que se usan registros unidos por enlaces.

Actualmente el modelo más usado es el modelo relacional basado en tablas sin olvidar el Modelo Orientado a objetos.

Tambien podemos verlo de la siguiente forma:

Los Modelos Conceptuales: Los modelos conceptuales se utilizan para representar la realidad a un alto nivel de abstracción. Mediante los modelos conceptuales se puede construir una descripción de la realidad fácil de entender.

Los Modelos Lógicos: En los modelos lógicos, las descripciones de los datos tienen una correspondencia sencilla con la estructura física de la base de datos.</p>
