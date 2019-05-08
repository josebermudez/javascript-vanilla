---
layout: post
title: "Event Bubbling"
author: jbermudez
image: assets/images/bubbles-1836457_1280.jpg
---

En este modelo de flujo de eventos, el orden que se sigue es desde el elemento más específico hasta el elemento menos específico.

Bubbling en la vida real se puede comparar a una burbuja que va desde el fondo del vaso hasta la parte superior del vaso.

A nivel de una página web,
cuando se tiene un evento en un elemento la ejecución de el evento
va desde el elemento mas bajo hasta el elemento del top.

Ejemplo:

<iframe width="100%" height="300" src="//jsfiddle.net/jjbermudez/ny82ebtg/4/embedded/js,html,result/dark/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

En este ejemplo tenemos 3 elementos de tipo button y el comportamiento es el siguiente:

* Si presionamos en el elemento **"Child 1"** el texto **"child_1 click"** y **"parent click"** es desplegado en la consola, esto quiere decir que el evento del elemento padre tambien fué activado.
* Si presionamos en el elemento **"Child 2"** el texto **"parent click"** es desplegado en la consola, esto quiere decir que el evento del elemento fué activado a pesar que el elemento **"Child 2"** no tiene un evento asignado.

Esto puede ser útil en el desarrollo web cuando tenemos elementos que se agregan dinámicamente al DOM, por ejemplo:

<iframe width="100%" height="300" src="//jsfiddle.net/jjbermudez/7ag4kdwq/23/embedded/js,html,result/dark/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

En este ejemplo estamos agregando dinamicamente elementos al contenedor padre, cada elemento agregado puede ser presionado y
activa la function del evento **"click"** que esta asociado al elemento padre.