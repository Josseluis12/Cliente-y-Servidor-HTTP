# Descripción del Programa

Este programa consiste en un servidor HTTP que gestiona solicitudes en dos contextos diferentes: "/saludar" y "/calculadora". 

## Contexto "/saludar"

En el contexto "/saludar", el servidor responde a las solicitudes generando saludos personalizados. Para ello, espera recibir dos parámetros en la URL: "nombre" y "apellido". Si la solicitud contiene estos parámetros, el servidor responde con un saludo que incluye el nombre y el apellido proporcionados. Si los parámetros no están presentes o están mal formados, el servidor responde con un mensaje genérico de saludo.

La lógica para manejar estas solicitudes se encuentra en la clase `ManejadorSaludos`, que implementa la interfaz `HttpHandler`.

## Contexto "/calculadora"

En el contexto "/calculadora", el servidor realiza operaciones aritméticas básicas utilizando los parámetros de la solicitud. Espera recibir tres parámetros en la URL: "op1", "op2" y "ope" (representando el primer operando, el segundo operando y la operación a realizar, respectivamente). Si la solicitud cumple con estos requisitos, el servidor realiza la operación especificada y devuelve el resultado. Si los parámetros son incorrectos o faltan, el servidor responde con un mensaje de error.

La lógica para manejar estas solicitudes se encuentra en la clase `HttpHandlerCalculadora`, que también implementa la interfaz `HttpHandler`.

## Paquetes y Clases

El programa está estructurado en varios paquetes y clases:

- **Paquete `cliente`**: Contiene la clase `ClienteHTTP`, que se encarga de realizar solicitudes HTTP a un servidor.
- **Paquete `servidor1`**: Contiene las clases `ManejadorSaludos` y `ServicioHttpBase`, responsables de manejar las solicitudes en los contextos "/saludar" y "/servicio", respectivamente.
- **Paquete `servidor2`**: Contiene las clases `HttpHandlerCalculadora` y `ServidorHttp`, encargadas de manejar las solicitudes en el contexto "/calculadora" y de iniciar el servidor HTTP, respectivamente.
- **Paquete `utilidades`**: Contiene la clase `Herramientas`, que proporciona métodos útiles para diversas tareas, como obtener la fecha y hora actuales.

Cada clase cumple un rol específico en el funcionamiento del servidor y sigue los principios de diseño y separación de responsabilidades para mantener el código organizado y fácil de mantener.

