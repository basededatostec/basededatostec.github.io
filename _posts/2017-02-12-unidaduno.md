---
layout: post
title: Unidad 1. Introducción a las Bases de Datos
tags: [unidad uno, resumen, introducción]
---

### 1.1 CONCEPTOS BÁSICOS

<p style="text-align: justify;"><b>Base de datos</b>. Una base de datos es un gran almacén donde se guardan enormes cantidades de información organizada, 
de esta manera cuando se quieran utilizar estos datos se puedan encontrar rápidamente, así ahorramos espacio físico y tiempo.

<br><br>También se puede definir como un conjunto de datos relacionados y organizados, estos datos a su vez son recolectados y utilizados por grandes empresas e constituciones.

<br><br><b>Dato</b>. Un dato es información que refleja una característica de algún objeto, ya sea concreto, o imaginario, por ejemplo podemos crear una base de datos acerca de los datos de una persona, un dato posible, sería; la fecha de nacimiento.</p>

### 1.2 OBJETIVOS DE LAS BASES DE DATOS

Algunos de los principales objetivos de las bases de datos son:

__Disminuir la redundancia e inconsistencia de los datos__

<p style="text-align: justify;">Existe la posibilidad de que al no controlar el almacenamiento se origine redundancia en la información, esto quiere decir que se duplican los datos. Entonces aumenta en buena medida el costo de almacenamiento y acceso, además se origina inconsistencia. 

<br><br>Por lo que debe contener el máximo contenido semántico para que la información sea realmente verdadera. Debe ser comprensible e interesante, lo que supone no proporcionar a los usuarios un volumen grande de información que no pueda ser asimilada.</p>

__Reducir la dificultad para tener acceso a los datos__

<p style="text-align: justify;">Un buen sistema de base de datos debe tener un entorno de datos que le facilite al usuario el manejo de los mismos.</p>

__Evitar el aislamiento de los datos__

<p style="text-align: justify;">Si el nivel de aislamiento es relativamente bajo, la capacidad de los usuarios al acceder al mismo tiempo a los datos aumenta. Por el contrario, un mayor nivel de aislamiento reduce los tipos de efectos de la concurrencia que los usuarios pueden encontrar, pero requiere más recursos del sistema y aumenta las probabilidades de que una transacción bloquee a otra.</p>

__Corregir anomalías del acceso concurrente__

<p style="text-align: justify;">El sistema debe permitir que múltiples usuarios actualizen los datos de forma simultanea. Cuando esto ocurre pueden dar como resultado datos inconsistentes, por ello se recomienda, mantener una supervision al sistema muy detallada.</p>

__Disminuir los problemas de seguridad__

<p style="text-align: justify;">Los valores que se guardan en la base de datos debe satisfacer limitantes de consistencia, el sistema debe obligar el cumplimiento de estas limitantes.</p>

__Debe contar con integridad__

<p style="text-align: justify;">La información contendida en el sistema debe ser coherente y consistente con las reglas semánticas propias del mundo real.</p>
