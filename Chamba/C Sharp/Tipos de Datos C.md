### Los tipos de Datos Fundamentales
- Tipos Integrales: Estos incluyen `int`,`long`,`short`,`byte`,`sbyte`,`uint`,`ulong` y `ushort`
	- Ejemplo: `int edad = 30;`
- Tipos de Punto Flotante: Estos incluyen `float` y `double` 
	- Ejemplo: `double precio = 19.99;`
- Tipo Decimal: El tipo `decimal` se utiliza para cálculos financieros donde la precisión es __critica.__ 
	- Ejemplo: `decimal salario = 50000.00m;`
- Tipo Booleano: El tipo `bool` puede contener dos valores: `true` o `false` 
	- Ejemplo: `bool esActivo = true;`
- Tipo Carácter: El tipo `char` representa un único carácter Unicode de 16 bits
	- Ejemplo: `char inicial = 'A';

### Tipos de Referencia.
_Los tipos de referencia almacenan referencias a sus datos_ (objetos) _y se almacenan en el montón. Los tipos de referencia comunes son:_ 
- __Cadena:__ Una secuencia de caracteres
	- Ejemplo: `string nombre = "Zacarias Garcia";`
- #__Arreglos (Array):__ Una colección de elementos del mismo tipo:
	- Ejemplo:
		- `int [] numeros = {1,2,3,4,5};`
		- bool resultado = ( 5 > 3 ) && ( 3 < 10 ); // Resultado es true
- __Clases:__ Tipos definidos por el usuario que pueden contener miembros de datos y métodos
	- Ejemplo: `class Persona {public string Nombre; public int Edad; }`
		- __Enumeradores:___ Un enum es una `clase` especial que representa un grupo de constantes (just read)
- __Interfaces:__ __Definen un contrato que las Clases pueden implementar__ 
	- Ejemplo: `interface IAnimal {void Hablar(); }`


### Conversión de Tipos.
La conversión de tipos es cuando se asigna un valor de un tipo de dato a otro tipo.

Existen dos tipos: 
- Explicita: Conversión de un tipo mas pequeño a un tamaño de tipo mas grande 
	- Ejemplo: ``char ``--> ``int ``--> ``long ``-->``float ``--> ``double``
- Implícita: Conversión de un tipo mas grande a un tipo de tamaño mas pequeño
	- Ejemplo: lo mismo que arriba pero al revés crack


#### Métodos de Conversión.

`int myInt = 10;`
`double myDouble = 5.25;`
`bool myBool = true;`

`Console.WriteLine(Convert.ToString(myInt)); // convert int to string Console.WriteLine(Convert.ToDouble(myInt)); // convert int to double Console.WriteLine(Convert.ToInt32(myDouble)); // convert double to int Console.WriteLine(Convert.ToString(myBool)); // convert bool to string`

#__Arreglos  
Los arreglos son indexados iniciando en cero (0)

##### Tipos de Arreglos:
###### Unidireccionales/ Unidireccionales
	Manejan una sola matriz, son chill de cojones.
	Ejemplo: 
		Declarar: int[] valores; Crear: valores = new int[100]; 
			int[] valores1 = new int[10] {0,1,2,3,4,5,6,7,8,9};
				 valores1[1] = 4; 

###### Multidimensionales
	Manejan de dos a infinita cantidad de matrices y elementos, un chino barbaro.
		Ejemplo:
		int[,] valores1;
		int[,] valores2 = new int[3,7];
		int[,] numeros = new int[3, 4] { {1, 2,3,4}, {9, 8,7,6}, {7, 6,2,5} };
			int[,,] valores1; //sin inicializar 
			int[,,] valores2 = new int[3,7,4]; 
			numeros[2,1] = 10; //Cambia el valor de indice 2,1 a 10
			Arreglos de Arreglos
			 int[][] matriz = new int[3][]; 
			 for (int i = 0; i < matriz.Length; i++) {
			  matriz[i] = new int[4]; 
			  } 
			  matriz[2][1] = 4;