---
layout: post
title: Modelo Relacional
subtitle: (caso práctico) TIENDA DE APARATOS ELECTRÓNICOS
tags: [unidad tres, modelo, relacional]
---
__ACTUALIZACIÓN 29 DE MARZO DEL 2107__
<p style="text-align: justify;">Al entregar nuestro modelo surgieron algunas dudas:

<br><br>"Me queda una duda en la relación <b>Producto-Pedido</b> ya que indican que muchos Pedidos solo tienen un Producto, o que solo un producto puede estar en los pedidos, me gustaría que vieran si eso es en la realidad."

<br><br>Podemos señalar que no existen relaciones <b>Producto-Pedido</b> en nuestro modelo, existe la relacion <b>Pedido-producto</b>, el cual inidica que un pedido puede conformar varios productos y un producto puede ser conformado en varios pedidos. A continuacion les presentamos las seis relaciones y lo que inidica cada uno de acuerdo al modelo que presentamos.</p>

Descarga el <b>primer modelo</b> dando clic en el siguiente [enlace](https://drive.google.com/uc?export=download&id=0B0tLjk4fF3eYT0E2bHBGVlZiNlE "clic para descargar la presentación") 

Descarga el modelo <b>corregido</b> dando clic [aquí](https://drive.google.com/uc?export=download&id=0B0tLjk4fF3eYOU5HaVZRU3ZTSWc "clic para descargar la presentación") 

O puedes dar clic para ver el modelo en el siguiente [enlace](https://basededatostec.github.io/img/ModeloERcorregido.png "clic para ver el modelo") 

#### CONCLUSIONES

<p style="text-align: justify;">Logramos conocer la importancia de las claves en las relaciones de las tablas que creamos con <b>MySQL Workbench</b>. Tomamos nuestras relaciones y evaluamos las reglas conocidas para realizar la propagación de la <b>llave primaria</b> si se trataba de una interrelación de <b>uno a muchos</b> o convertirla a una nueva relación si se trataba de una interrelación de <b>muchos a muchos</b>. Realizamos seis evaluaciones; <b>Cliente-Pedido, Pedido-Producto, Pedido-Vendedor, Pedido-Factura, Factura-Detalle_Factura</b> y <b>Producto-Proveedor</b>. Con esto comprobábamos con que interrelación estábamos trabajando y a donde propagar las <b>llaves foráneas</b>, en nuestro modelo no se encontraron interrelaciones muchos a muchos. <br><br>Por último cabe señalar que el programa que usamos (MySQL Workbench) para llevar a cabo el trabajo tiene una interfaz excelente y su forma de uso es fácil y eficaz, un excelente programa que nos ahorro mucho trabajo.</p>__REFERENCIAS__<br><br>__Vídeos en Linea__<br><br>_Sandoval, Bani. (2015, Abril, 15). Bases de Datos - Introducción al Modelo-Relacional<br>Recuperado de https://www.youtube.com/watch?v=CPabJuf7KQE_