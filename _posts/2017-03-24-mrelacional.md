---
layout: post
title: Modelo Relacional
subtitle: (caso práctico) TIENDA DE APARATOS ELECTRÓNICOS
tags: [unidad tres, modelo, relacional]
---

<p style="text-align: justify;">En esta tarea construimos el <b>Modelo Relacional</b> que se construyo con la herramienta <b>WorkBench</b>, partiendo del Esquema de nuestra tarea anterior.</p>

__ACTUALIZACIÓN 29 DE MARZO DEL 2107__
<p style="text-align: justify;">Al entregar nuestro modelo surgieron algunas dudas:

<br><br>"Me queda una duda en la relación <b>Producto-Pedido</b> ya que indican que muchos Pedidos solo tienen un Producto, o que solo un producto puede estar en los pedidos, me gustaría que vieran si eso es en la realidad."

<br><br>Así es, esto es realidad. Omitimos redactar las reglas de envío de la tienda de aparatos electrónicos. Que estipulan que un envío sólo puede contener <b>un sólo producto</b> o articulo, en este caso un aparato electrónico. Por lo que la relación <b>Pedido-Producto</b>, con una cardinalidad de <b>N:1</b> indica que <b>muchos pedidos se conforman de un sólo producto</b> y que sólo <b>un producto puede estar en los pedidos</b>. A continuación les presentamos las seis relaciones y lo que indica cada una de ellas.</p>

| <img src="https://basededatostec.github.io/img/spacce.png" width="358"> __RELACIONES__ |  | 
| :-------: | :------ | 
| <img src="https://basededatostec.github.io/img/22relacion.png" width="298">   | Un cliente puede realizar varios pedidos, mientras que un pedido sólo puede ser enviado a un sólo cliente.       | 
| <img width="298" src="https://basededatostec.github.io/img/24relacion.gif">   | Muchos pedidos se conforman de un sólo producto y sólo un producto puede estar en los pedidos.       | 
| <img width="298" src="https://basededatostec.github.io/img/27relacion.png">   | Un vendedor puede atender varios pedidos y un pedido sólo puede ser atendido por un vendedor.       | 
| <img width="298" src="https://basededatostec.github.io/img/30relacion.gif">   | Un cliente puede obtener varias facturas, pero sólo una factura puede pertenecer a un cliente.    | 
| <img width="298" src="https://basededatostec.github.io/img/21relacion.png">   | Una factura puede contener varios detalles, mientras que un detalle solo puede pertenecer a una factura.       | 
| <img width="298" src="https://basededatostec.github.io/img/26relacion.gif">   | Un proveedor puede suministrar varios productos y un producto sólo puede ser suministrado por un proveedor.       | 

Por lo que nuestro modelo relacional es el siguiente.

<img src="https://basededatostec.github.io/img/29modelo.png">

Descarga este modelo dando clic en el siguiente [enlace](https://drive.google.com/uc?export=download&id=0B0tLjk4fF3eYa2RHUzltVEtMUDQ "clic para descargar el modelo")  

#### CONCLUSIONES

<p style="text-align: justify;">Logramos conocer la importancia de las claves en las relaciones de las tablas que creamos con <b>MySQL Workbench</b>. Tomamos nuestras relaciones y evaluamos las reglas conocidas para realizar la propagación de la <b>llave primaria</b> si se trataba de una interrelación de <b>uno a muchos</b> o convertirla a una nueva relación si se trataba de una interrelación de <b>muchos a muchos</b>. Realizamos seis evaluaciones; <b>Cliente-Pedido, Pedido-Producto, Vendedor-Pedido, Pedido-Facturas, Facturas-Detalles_Factura</b> y <b>Proveedor-Producto</b>. Con esto comprobábamos con que interrelación estábamos trabajando y a donde propagar las <b>llaves foráneas</b>, en nuestro modelo no se encontraron interrelaciones muchos a muchos. <br><br>Por último cabe señalar que el programa que usamos (<b>MySQL Workbench</b>) para llevar a cabo el trabajo tiene una interfaz excelente y su forma de uso es fácil y eficaz, un excelente programa que nos ahorro mucho trabajo.</p>__REFERENCIAS__<br><br>__Vídeos en Linea__<br><br>_Sandoval, Bani. (2015, Abril, 15). Bases de Datos - Introducción al Modelo-Relacional<br>Recuperado de https://www.youtube.com/watch?v=CPabJuf7KQE_
