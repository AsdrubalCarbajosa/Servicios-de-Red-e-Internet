# Actividad 0.1 - HTTP Introduction
## ¿Quién, dónde y cuándo se crea el primer servidor web?
Tim-Berners-Lee creó el primer servidor web en Ginebra, Suiza en el año 1990.
## ¿Qué es pila de protocolos usados por http?
Es una colección de protocolos para redes de Computadores que son utilizados para definir, 
localizar, implementar y hacer que un Servicio Web interactúe con otro.
## ¿Componentes de una URL?

-Protocolo de red: Http, Https, mailto y ftp son los principales protocolos web que encabezan una URL, indicando a la máquina qué tipo de conexión debe realizar y cuál es el lenguaje específico que se hablará con la computadora o la red de computadoras que brindarán la información al usuario.

-Servicio: Www, www2, etc., se trata de los posibles servicios de soporte de información on-line, de los cuales la World Wide Web es la más popular.

-Dominio, tipo de dominio y país: Se trata del “nombre” de la empresa que brinda la información, o del proyecto o red o la computadora en donde se encuentran, es decir, el nombre específico de quien tiene lo que buscamos; además el tipo de servicio que presta: comercial (.com), educativo (.edu), etc., y el país al que pertenece: Argentina (.ar), Brasil (.br), Italia (.it), etc.

-Ruta y nombre del archivo: Las carpetas y directorios en los que se ubica el recurso específico dentro del computador servidor (que brinda la información).

## ¿Pasos en la recuperación de una página web mediante HTTP?
Las webs estáticas son básicamente paginas informativas que tienen sus secciones y contenido fijo. Obviamente se pueden actualizar pero no de una forma sencilla para el usuario que no tenga algún conocimiento de HTML. En las páginas web estáticas no se utilizan bases de datos ni se requiere programación. Este tipo de webs son mas económicas ya que el tiempo de programación es mucho menor que en las paginas dinámicas.

Las webs dinámicas son paginas en las que su contenido es fácilmente y frecuentemente modificado. Se construyen usando lenguajes de programación como PHP que permiten programar aplicaciones de todo tipo: blogs, foros, tiendas, etc. Requiere base de datos para almacenar la información.

## ¿Cómo usar telnet para acceder a un servidor web?
Lo primero es que sis estás en Windows debes activar Telnet. Para ello, nos vamos a Características de Windows y seleccionamos "Cliente Telnet" y aceptamos. Tras esto, puedes escribir telnet <nombre del dominio> o telnet <dirección IP> en el CMD para acceder remotamente a un equipo o servidor.

## Request. Métodos principales

-GET:
El método GET solicita una representación de un recurso específico. Las peticiones que usan el método GET sólo deben recuperar datos.

-HEAD:
El método HEAD pide una respuesta idéntica a la de una petición GET, pero sin el cuerpo de la respuesta.

-POST:
El método POST se utiliza para enviar una entidad a un recurso en específico, causando a menudo un cambio en el estado o efectos secundarios en el servidor.

-PUT:
El modo PUT reemplaza todas las representaciones actuales del recurso de destino con la carga útil de la petición.

-DELETE:
El método DELETE borra un recurso en específico.

-CONNECT:
El método CONNECT establece un túnel hacia el servidor identificado por el recurso.

-OPTIONS:
El método OPTIONS es utilizado para describir las opciones de comunicación para el recurso de destino.

-TRACE:
El método TRACE realiza una prueba de bucle de retorno de mensaje a lo largo de la ruta al recurso de destino.

-PATCH:
El método PATCH es utilizado para aplicar modificaciones parciales a un recurso.

## Response. Códigos

-200 OK:
La solicitud ha tenido éxito. El significado de un éxito varía dependiendo del método HTTP:

-201 Created:
La solicitud ha tenido éxito y se ha creado un nuevo recurso como resultado de ello. Ésta es típicamente la respuesta enviada después de una petición PUT.

-202 Accepted:
La solicitud se ha recibido, pero aún no se ha actuado. Es una petición "sin compromiso", lo que significa que no hay manera en HTTP que permite enviar una respuesta asíncrona que indique el resultado del procesamiento de la solicitud. Está pensado para los casos en que otro proceso o servidor maneja la solicitud, o para el procesamiento por lotes.

-203 Non-Authoritative Information:
La petición se ha completado con éxito, pero su contenido no se ha obtenido de la fuente originalmente solicitada, sino que se recoge de una copia local o de un tercero. Excepto esta condición, se debe preferir una respuesta de 200 OK en lugar de esta respuesta.

-403 Forbidden:
El cliente no posee los permisos necesarios para cierto contenido, por lo que el servidor está rechazando otorgar una respuesta apropiada.

-404 Not Found:
El servidor no pudo encontrar el contenido solicitado. Este código de respuesta es uno de los más famosos dada su alta ocurrencia en la web.

-405 Method Not Allowed:
El método solicitado es conocido por el servidor pero ha sido deshabilitado y no puede ser utilizado. Los dos métodos obligatorios, GET y HEAD, nunca deben ser deshabilitados y no deberían retornar este código de error.

## Content type. Tipos principales

El content type, también conocido como media type o MIME type (extensiones de correo de Internet multipropósito), es un recurso que se utiliza en la cabecera HTTP (header) y que le indica al cliente o navegador qué clase de archivo o medio le está enviando el servidor.

Existe un amplio número de media types que se pueden utilizar al configurar un content type. A continuación se muestran solamente algunos de los más comunes:

-application/pdf

-application/xml

-audio/ogg

-audio/mpeg

-image/apng

-image/jpeg (.jpg, .jpeg, .jfif, .pjpeg, .pjp)

-text/css

-text/html

-text/php

-text/xml

-video/mp4
