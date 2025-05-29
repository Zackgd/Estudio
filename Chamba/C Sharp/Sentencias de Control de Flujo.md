Las sentencias de control de flujo te permiten dictar el orden en que se ejecutan las sentencias en tu programa. C# proporciona varios tipos de sentencias de control de flujo:
#SentenciasCondicionales
### Sentencias Condicionales.
Las sentencias condicionales ejecutan diferentes bloques de código según _Ciertas Condiciones_

__Sentencias IF:__
`Las sentencias if ejecuta un bloque de codigo si una condicion especificada es verdadera:`
	`if (edad >= 18) {Console.WriteLine("Adulto");}`

__Sentencias IF-ELSE__
La sentencia `if-else` te permite ejecutar un bloque de código si la condición es verdadera y otro bloque si es falsa:

`if (edad >= 18){ Console.WriteLine("Adulto"); } else { Console.WriteLine("Menor");}`

__Sentencia Switch__
La sentencia `Switch` es una forma mas limpia de manejar múltiples condiciones:
`switch (dia)
	{ case 1: Console.WriteLine("Lunes"); break; 
		case 2: Console.WriteLine("Martes"); break;
			 default: Console.WriteLine("Otro"); }`


#SentenciasBucle

#### Sentencias de Bucle
Las sentencias de este tipo te permiten ejecutar un bloque de código múltiples veces:

##### ___Bucle FOR___
Se utiliza cuando se conoce el numero de iteraciones.

``for (int i = 0; i < 10; i++) { Console.WriteLine(i); }``

##### ___Bucle While___
Continua ejecutándose mientras una condición especifica sea verdadera
`int i = 0; while (i > 10) {Console.WriteLine(i); i++}`

##### ___Bucle $Do-While$___
``Es similar al bucle while pero garantiza que el bloque de código se ejecute al menos una vez:``
`int i = 0; do {Console.WriteLine(i); i++ } while (i > 10);`

##### ___Bucle___ $FOREACH$
El ``foreach`` se utiliza para iterar colecciones, como arreglos o listas


