### Requisitos previos
El equipo de IronIA le habrá suministrado un **API key** y un **API secret** para poder acceder al API.

### Usando el API
Url del servicio:
* https://open-api-dev-6dd675tf.ew.gateway.dev

Formato de las peticiones:
Todas las peticiones deben incluir la cabecera de autenticación básica que se construye de la siguiente manera:
* Nombre de usuario y la contraseña se combinan en una cadena "api_key:api_secret".
* La cadena resultante se codifica utilizando la variante RFC2045-MIME de Base64, excepto que no limitado a 76 caracteres por línea.​
* El método de autorización y un espacio, es decir, "Basic " se pone a continuación, antes de que la cadena codificada.

Ejemplo:
'Authorization: Basic EHAxcEAkNzUtNmU3Yi00MGFiLTk1MmYtYzRjYzAxNGM1ZGYxOjVjaWpqNmttYzI5NjQxaGNmYTVzbG42bQ=='

La información de cada operación se transmitirá al servidor a través de variables en el cuerpo de la petición.

Ejemplo de petición:
```
curl --location --request POST 'https://open-api-dev-6dd675tf.ew.gateway.dev/signup' \
--header 'Authorization: Basic EHAxcEAkNzUtNmU3Yi00MGFiLTk1MmYtYzRjYzAxNGM1ZGYxOjVjaWpqNmttYzI5NjQxaGNmYTVzbG42bQ==' \
--header 'Content-Type: application/json' \
--data-raw '{"user": "monxela@gmail.com"}'
```
