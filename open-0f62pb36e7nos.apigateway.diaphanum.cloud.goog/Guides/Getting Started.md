### Requisitos previos
El equipo de IronIA le habrá suministrado un **Id Afiliado** y una ***Contraseña Afiliado* para poder acceder al API.

### Usando el API
Url del servicio:
* https://open-api-dev-6dd675tf.ew.gateway.dev

Formato de las peticiones:
Todas las peticiones deben incluir la cabecera de autenticación básica que se construye de la siguiente manera:
* El identificador y la contraseña se combinan en una cadena "api_key:api_secret" usando el caracter dos puntos como "pegamento".
* La cadena resultante se codifica utilizando la variante RFC2045-MIME de Base64 (sin la limitación de 76 caracteres por línea).
* El método de autorización y un espacio, es decir, "Basic " se pone a continuación, antes de la cadena codificada.

Ejemplo:
'Authorization: Basic EHAxcEAkNzUtNmU3Yi00MGFiLTk1MmYtYzRjYzAxNGM1ZGYxOjVjaWpqNmttYzI5NjQxaGNmYTVzbG42bQ=='

Ejemplo de petición:
```
curl --location --request POST 'https://open-api-dev-6dd675tf.ew.gateway.dev/signup' \
--header 'Authorization: Basic EHAxcEAkNzUtNmU3Yi00MGFiLTk1LlYtYzRjYcAxNGM1ZGYxOjVjaWpqNmttYzI5NjQxaGNmYTVzbG42bQ==' \
--header 'Content-Type: application/json' \
--data-raw '{"user": "info@ironia.tech"}'
```
