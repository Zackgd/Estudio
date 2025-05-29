Es un paradigma de programación que utiliza "objetos" para representar datos y métodos para manipular esos datos.

Vamos por lo mas facilito: 
#ClasesYObjetos
#### Clases y Objetos.
Una clase en C# es un plano para crear objetos, también se lo puede ver como una plantilla o modelo del cual se crean los objetos, todo basado en la clase modelo de la cual parte
- Define propiedades (atributos)
- Define métodos (funciones)
	==Que tendrá el Objeto creado==


Un `Objeto` es una instancia de una clase, cuando creas un objeto, se instancia de una clase.

`public class Car 
	{ 
	// Propiedades 
	public string Make { get; set; } 
	public string Model { get; set; } 
	public int Year { get; set; } 
		// Método 
		public void DisplayInfo() { Console.WriteLine($"Coche: {Year} {Make} {Model}"); } }`

`// Creando un Objeto`
	`Car myCar = new Car();`
		``myCar.Make = "Toyota"; //se asignan los valores, en las propiedades establecidas por la clase
		``myCar.Model = "Corolla";``
		``myCar.Year = 2020;``
		``myCar.DisplayInfo();``


#Herencia
#### Herencia y Polimorfismo.

Es un $Mecanismo$ en C# que permite que una clase ==herede== las propiedades y métodos de otra clase, esto, con la finalidad de reutilizar código y establecer una jerarquía entre las clases.

| Jerarquia          | Descripcion                                                     |
| ------------------ | --------------------------------------------------------------- |
| **Clase Base**     | Clase de la cual otras clases van a heredar atributos o metodos |
| **Clase Derivada** | Clase que recibe los atributos o metodos de la clase Base       |
El ejemplo no hace falta, ya lo tengo clarito ==acccche==

#Polimorfismo
#### Polimorfismo.
Otro concepto masivo, que permite que los métodos heredados de otra clase actúen distinto en función de la necesidad de la clase derivada.

	Ejemplo (no entendi na de na): 
		public class Truck : Vehicle {
			public int LoadCapacity { get; set; }
			public override void DisplayInfo() {
				Console.WriteLine($"Camión: {Make} {Model}, 
					Capacidad de Carga: {LoadCapacity} toneladas"); } }
// Con polimorfismo aplicado nos queda:

`Vehicle myTruck = new Truck();`
``Vehicle myTruck = new Truck(); myTruck.Make = "Ford";
``myTruck.Model = "F-150";``
``((Truck)myTruck).LoadCapacity = 3;``
`myTruck.DisplayInfo(); // Salida: Camión: Ford F-150, Capacidad de Carga: 3 toneladas`
#Encapsulamiento
Es la agrupación de datos (atributos) y métodos (funciones) que operan sobre los datos en una sola unidad, o clase. Restringe el acceso directo a algunos de los componentes del objeto, lo que es un medio para prevenir interferencias no intencionadas y el uso indebido de los métodos y datos. 
En C#, la encapsulación se logra utilizando [[Modificadores de Acceso]]
#Abstracción
Es el concepto de ocultar la realidad compleja mientras se expone solo las partes necesarias
Ayuda a reducir la complejidad de la programación y aumenta la eficiencia.
En C#, la abstracción se puede lograr utilizando clases e [[Interfaces]]
