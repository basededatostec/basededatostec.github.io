---
layout: post
title: Modelo Relacional Normalizado
subtitle: (caso práctico) TIENDA DE APARATOS ELECTRÓNICOS
tags: [unidad cuatro, modelo, relacional, normalizado]
---

<p style="text-align: justify;">En esta tarea perteneciente a la unidad 4, construimos el <b>Modelo Relacional Normalizado</b> que se construyo con la herramienta <b>WorkBench</b>, partiendo del <a href="https://basededatostec.github.io/2017-03-24-mrelacional/">Modelo relacional</a> de nuestra tarea anterior.</p>
     | 
Por lo que nuestro modelo relacional es el siguiente.

<img src="https://basededatostec.github.io/img/29modelo.png">

Descarga este modelo dando clic en el siguiente [enlace](https://drive.google.com/uc?export=download&id=0B0tLjk4fF3eYa2RHUzltVEtMUDQ "clic para descargar el modelo")  

#### CONCLUSIONES

<p style="text-align: justify;">Debido a la práctica que tuvimos creando nuestro modelo normalizado podemos llegar a la conclusión que la normalización puede considerarse como un proceso con el cual los esquemas o modelos de de relación que no cumplen ciertas reglas o son poco eficaces, se pueden descomponer repartiendo sus atributos entre esquemas de relación más pequeños que poseen atributos mucho mejor estructurados.

<br><br>El objetivo de la normalización desde nuestro punto de vista es garantizar que no ocurran anomalías en el sistema, evitar datos repetidos, ahorrar espacio en el sistema y tener un sistema ligero y eficaz.

<br><br>Ahora somos capaces de usar WorkBench y sus herramientas, conocemos el valor de una llave primaria y una llave foránea. Así como las primeras tres formas normales que de acuerdo a la referencia y las fuentes de información que seguimos. la primer forma normal 1FN debe tener campos atómicos, por lo que revisamos y efectuamos esta regla en nuestro modelo, dentro de la segunda forma normal 2FN cada uno de los campos de las tablas existentes tienen que depender de su llave primaria, y la tercer forma normal 3FN indica que no deben existir llaves transitivas, por ejemplo ninguna columna puede depender de una columna que no tenga una llave primaria.

|  Acerca de: | 
| :------ | 
| Éste es un sitio creado por estudiantes del Instituto Tecnológico de Pachuca, para la asignatura en curso; Fundamentos de Bases de Datos. | 
| Equipo New Jackers: Hernández Salinas Lucio y Sanchez Casañas Jose María |
| <a href="https://basededatostec.github.io/unidadtres/">Actividades Unidad 3</a> |
