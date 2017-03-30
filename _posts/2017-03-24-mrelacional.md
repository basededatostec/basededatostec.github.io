---
layout: post
title: Modelo Relacional (caso práctico)
subtitle: MODELO RELACIONAL DE UNA TIENDA
tags: [unidad tres, modelo, relacional]
---
<p style="text-align: justify;">
<br><br><b>ACTUALIZACIÓN 29 DE MARZO DEL 2107</b>

<br><br>Al entregar nuestro modelo surgieron algunas dudas:

<br><br>"Me queda una duda en la relación Producto-Pedido ya que indican que muchos Pedidos solo tienen un Producto, o que solo un producto puede estar en los pedidos, me gustaría que vieran si eso es en la realidad."

<br><br>La afirmación es errónea, así que corregimos nuestro modelo, la cardinalidad no era <b>1:N</b> es <b>N:1</b>, "un producto sólo puede ser suministrado por un proveedor, y un proveedor puede suministrar varios productos", por lo que el modelo queda corregido.</p>

Descarga el <b>primer modelo</b> dando clic en el siguiente [enlace](https://drive.google.com/uc?export=download&id=0B0tLjk4fF3eYT0E2bHBGVlZiNlE "clic para descargar la presentación") 

Descarga el modelo <b>corregido</b> dando clic [aquí](https://drive.google.com/uc?export=download&id=0B0tLjk4fF3eYOU5HaVZRU3ZTSWc "clic para descargar la presentación") 

O puedes dar clic para ver el modelo en el siguiente [enlace](https://basededatostec.github.io/img/ModeloERcorregido.png "clic para ver el modelo") 

#### CONCLUSIONES

<p style="text-align: justify;">Logramos conocer la importancia de las claves en las relaciones de las tablas que creamos con MySQL Workbench. Tomamos nuestras seis relaciones y evaluamos las reglas conocidas para realizar la propagación de la llave primaria si se trataba de una interrelación de uno a muchos o convertirla a una nueva relación si se trataba de una interrelación de muchos a muchos. Realizamos seis evaluaciones de las siguientes relaciones; Cliente-Pedido, Pedido-Producto, Pedido-Vendedor, Pedido-Factura, Factura-Detalle_Factura y Producto-Proveedor. Con esto comprobábamos con que interrelación estábamos trabajando y a donde propagar las llaves foráneas correspondientes, en nuestro modelo no se encontraron interrelaciones muchos a muchos. <br><br>Por último cabe señalar que el programa que usamos (MySQL Workbench) para llevar a cabo el trabajo tiene una interfaz excelente y su forma de uso es fácil y eficaz, un excelente programa que nos ahorro mucho trabajo.<br><br>REFERENCIAS<br><br>Vídeos en Linea<br><br>_Sandoval, Bani. (2015, Abril, 15). Bases de Datos - Introducción al Modelo-Relacional<br>Recuperado de https://www.youtube.com/watch?v=CPabJuf7KQE_</p>

__Bibliografía__
