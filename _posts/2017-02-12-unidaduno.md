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

<center><img src="https://basededatostec.github.io/img/08objetivo.png" title="Objetivos" alt="objetivoss"></center>
Estas son las principales areas en donde las bases de datos pueden ser usadas.

__Banca__: información de clientes, cuentas, transacciones, préstamos, et

__Líneas aéreas__: Clientes, horarios, vuelos, destinos, etc. (1ras bases distribuidas geográficamente)

__Universidades__: Estudiantes, carreras, horarios, materias, etc.

<p style="text-align: justify;"><b>Transacciones de tarjeta de crédito</b>: Para comprar con tarjetas de crédito y la generación de los extractos mensuales.

<br><br><b>Telecomunicaciones</b>: para guardar registros de llamadas realizadas, generar facturas mensuales, mantener el saldo de las tarjetas, telefónicas de prepago y almacenar información sobre las redes..</p>

__Medicina__: Registro de enfermedades, datos biológicos, etc.

En realidad su uso es muy amplio y se puede tener en cualquier sistema.



