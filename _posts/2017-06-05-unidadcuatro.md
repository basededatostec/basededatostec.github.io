---
layout: post
title: Unidad 4
subtitle: Normalización de bases de datos
tags: [unidad cuatro, resumen, introducción, normalizado]
---
### 4.1 CONCEPTOS BÁSICOS

<p style="text-align: justify;">La normalización es el <b>proceso de organizar los datos</b>. Se incluye la creación de tablas y el establecimiento de relaciones entre ellas según reglas diseñadas tanto para proteger los datos como para hacer que la base de datos sea más <b>flexible</b>. 

<br><br>Los <b>datos redundantes</b> desperdician el espacio de disco y crean problemas de mantenimiento. Si hay que cambiar datos que existen en más de un lugar, se deben cambiar de la misma forma exactamente en todas sus ubicaciones. Un cambio en la dirección de un cliente es mucho más fácil de implementar si los datos sólo se almacenan en la <b>tabla Clientes</b> y no en algún otro lugar de la base de datos. 

<br><br>Uno de los parámetros que mide la calidad de una base de datos es la <b>forma normal</b> en la que se encuentra su diseño. Puede alcanzarse cumpliendo ciertas restricciones que impone cada forma normal al <b>conjunto de atributos</b> de un diseño. El proceso de obligar a los atributos de un diseño a cumplir ciertas formas normales se llama normalización.

<br><br>Las formas normales pretenden alcanzar dos objetivos:

<br><br><b>1.-</b> Almacenar en la base de datos cada hecho solo una vez, es decir, <b>evitar la redundancia</b> de datos. De esta manera se reduce el espacio de almacenamiento.

<br><br><b>2.-</b> Que los hechos distintos se <b>almacenen</b> en sitios distintos.</p>

__4.2 PRIMERA FORMA NORMAL__

<p style="text-align: justify;">Esta primera Forma Normal, nos lleva a no repetir datos en nuestras tablas. Si nuestra tabla de ventas repite una y otra vez, el nombre, el domicilio y otros datos del Cliente, es que no hemos aplicado esta Normalizaciòn. Si tenemos una tabla clientes, en la tabla ventas, solo debería figurar el código del cliente, para que el resto de los datos se puedan referenciar automaticamente.

<br><br>Lo mismo ocurriría en una tabla de detalle de ventas, si por cada producto vendido colocamos el detalle del producto, con su descripción , medidas, etc…Tendriamos un desaprovechamiento de espacio y recursos muy grande. Para ello, tendremos nuestra tabla maestra de Productos y con solo grabar el código de dicho producto en nuestra tabla de ventas, será suficiente.</p>
