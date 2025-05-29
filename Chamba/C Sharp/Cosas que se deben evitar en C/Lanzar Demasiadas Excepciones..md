En la vida no se puede escapar de la muerte, los cuernos y las excepciones de .NET

Lanzar excepciones es una practica común en C# y .NET para manejar errores, sin embargo su ejecución tiene un impacto negativo en el rendimiento de una aplicación.
`Cada excepción produce una sobrecarga significativa de la CPU y la memoria`

``Las excepciones son necesarias para manejar errores en la aplicación``
__Pero no para gestionar errores en el flujo de control normal de la aplicación__

	Ejemplo: Si se espera que una consulta a la base de datos devuelva un resultado
	 y en su lugar devuelve un valor nulo, lanzar una excepcion para informar de 
	 este error no es una buena practica

___En lugar de lanzar una excepción, se recomienda utilizar otro mecanismo para informar de esto, como devolver un resultado de error en la respuesta de la solicitud.___
___Esto no solo reduce la sobrecarga de excepción, sino que también hace que el código sea mas facil de leer y depurar___
