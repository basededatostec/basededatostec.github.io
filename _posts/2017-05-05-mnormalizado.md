---
layout: post
title: Modelo Normalizado
subtitle: (caso práctico) TIENDA DE APARATOS ELECTRÓNICOS
tags: [unidad cuatro, modelo, relacional, normalizado]
---

<p style="text-align: justify;">En esta tarea perteneciente a la unidad cuatro del curso en turno, construimos el <b>Modelo Relacional Normalizado</b> que se construyo con la herramienta <b>WorkBench</b>, partiendo del <a href="https://basededatostec.github.io/2017-03-24-mrelacional/">Modelo relacional</a> de nuestra tarea anterior.</p>

Nuestro modelo relacional normalizado es el siguiente.

<img src="https://basededatostec.github.io/img/41normalizado.png">

Descarga este modelo dando clic en el siguiente [enlace](https://drive.google.com/uc?export=download&id=0B0tLjk4fF3eYa2RHUzltVEtMUDQ "clic para descargar el modelo")  

#### CONCLUSIONES

<p style="text-align: justify;">Debido a la práctica que tuvimos creando nuestro modelo normalizado podemos llegar a la conclusión que la normalización puede considerarse como un proceso con el cual los esquemas o <b>modelos de de relación que no cumplen ciertas reglas o son poco eficaces</b>, se pueden descomponer repartiendo sus atributos entre esquemas de relación más pequeños que poseen atributos mucho mejor estructurados.

<br><br>El objetivo de la normalización desde nuestro punto de vista es garantizar que no ocurran <b>anomalías en el sistema</b>, evitar <b>datos repetidos</b>, ahorrar <b>espacio</b> en el sistema y tener un sistema ligero y eficaz.

<br><br>Ahora somos capaces de usar <b>WorkBench</b> y sus herramientas, conocemos el valor de una <b>llave primaria</b> y una <b>llave foránea</b>. Así como las primeras tres <b>formas normales</b> que de acuerdo a la referencia y las fuentes de información que seguimos. la primer forma normal <b>1FN</b> debe tener campos atómicos, por lo que revisamos y efectuamos esta regla en nuestro modelo, dentro de la segunda forma normal <b>2FN</b> cada uno de los campos de las tablas existentes tienen que depender de su llave primaria, y la tercer forma normal <b>3FN</b> indica que no deben existir <b>llaves transitivas</b>, por ejemplo ninguna columna puede depender de una columna que no tenga una llave primaria.</p>

__REFERENCIAS__

__Vídeo en linea__<br>
_Zuzunaga, David. (2016, Mayo 16). Ejemplo de normalizacion.<br>
Recuperado de: https://www.youtube.com/watch?v=igctJY-YIjY_

__Pagina Web__<br>
_Coronado, Pozo, Salvador. (2004, Diciembre, 10). MySQL con clase.<br>
Recuperado de: http://mysql.conclase.net/curso/?cap=004#NOR_1FN_

|  Acerca de: | 
| :------ | 
| Éste es un sitio creado por estudiantes del Instituto Tecnológico de Pachuca, para la asignatura en curso; Fundamentos de Bases de Datos. | 
| Equipo New Jackers: Hernández Salinas Lucio y Sanchez Casañas Jose María |
| <a href="https://basededatostec.github.io/unidadcuatro/">Actividades Unidad 4</a> |
