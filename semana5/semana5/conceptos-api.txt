Conceptos API - Semana 5
=========================

¿Qué hace la ruta POST /reporte?
----------------------------------
La ruta POST /reporte recibe datos enviados por el usuario en el cuerpo
(body) de la solicitud HTTP. Específicamente, extrae el campo "mensaje"
del body usando req.body.mensaje, y luego responde con un objeto JSON
que contiene dos campos: "estado" (con el valor "Reporte recibido") y
"mensaje" (con el texto que envió el usuario).

A diferencia de las rutas GET, esta ruta no se puede probar simplemente
escribiendo la URL en el navegador, porque requiere que se envíen datos
en el cuerpo de la solicitud. Se debe usar una herramienta como
Postman, Thunder Client o código JavaScript (fetch/axios) para enviarle
datos con formato JSON, por ejemplo:
  { "mensaje": "Hay un daño en el acueducto del barrio norte" }

¿Para qué podría servir en una aplicación comunitaria?
-------------------------------------------------------
Esta ruta sería muy útil en una aplicación comunitaria para que los
vecinos puedan enviar reportes de problemas de su sector, como daños en
vías, cortes de agua, fallas en el alumbrado público o situaciones de
inseguridad. Cada reporte llegaría al servidor con el mensaje del
ciudadano, y desde allí podría almacenarse en una base de datos,
notificarse a las autoridades correspondientes o publicarse en un
tablero comunitario. Es la base de cualquier sistema de PQR
(Peticiones, Quejas y Reclamos) digital.
