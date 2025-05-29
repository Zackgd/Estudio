Usar de manera incorrecta el `HttpClient` puede causar una cantidad de problemas nashe de rendimiento.

con la linea de código:
`var client = new HttpClient();`

Se crea un nuevo objeto HttpClient cada vez que necesitas hacer una llamada, lo que significa que abres un canal de comunicación nuevo cada vez que el código se ejecute.
Además es posible que no liberes correctamente la conexión al finalizar.

En lugar de eso se debería crear `HttpClientFactory`, que te permite reutilizar el cliente y configurarlo de manera centralizado. Así se implementa en un ejemplo 

`//recoger el IHttpClientFactory del contenedor de dependecias o inyectarlo en el constructor`
`var httpClientFactory = serviceProvider.GetRequiredService<IHttpClientFactory>();`
`var client = httpClientFactory.CreateClient();`

Utilizando `httpClientFactory` podrás crear clientes http configurados adecuadamente, que se reutilizan y se administran automáticamente por el framework.
