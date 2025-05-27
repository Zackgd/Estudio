LINQ es el nombre que recibe el conjunto de tecnologías basadas en la integración de capacidades de consulta directamente en el lenguaje C#. 

### Introducción.
Una consulta es una expresión que recupera datos de un origen de datos. Los distintos orígenes de datos tienen diferentes lenguajes de consulta nativos, [[SQL]] para bases de datos relacionales y [[XQuery]] para [[XML]]. De esta forma los programadores, tienen que aprender un lenguaje de consultas nuevo para cada tipo de origen de datos. LINQ simplifica esto al ofrecer un modelo de lenguaje C# coherente para tipos de orígenes de datos y formatos.

### Partes de una Operación de Consulta.

**Todas las Operaciones de consulta LINQ constan de 3 acciones distintas:**

	1. Obtener el origen de datos.
	2. 2. Crear la consulta.
	3. Ejecutar la consulta.

#### Ejemplo
`// 1. Data source.`
 `int[] numbers = [ 0, 1, 2, 3, 4, 5, 6 ];`

`// 2. Query creation.`
`// numQuery is an IEnumerable<int>`
`var numQuery = from num in numbers`
               `where (num % 2) == 0`
               `select num;`

`// 3. Query execution.`
`foreach (int num in numQuery)`
`{`
    `Console.Write("{0,1} ", num);`
`}`

### Origen de Datos
Se debe utilizar [[IEnumerable T]] para utilizar las consultas LINQ, [[foreach]] es especialmente usado para [[IEnumerable T]]. Los tipos utilizados con este formato o una interfaz derivada se denominan *Tipos Consultables* 
Un Tipo Consultables no requiere ninguna modificación ni ningún tratamiento especial para actuar como origen de datos de LINQ.

### Consulta

La consulta especifica la información que se debe recuperar de los orígenes de Datos, opcionalmente, una consulta también especifica como se debe **ordenar**, **agrupar** y **dar forma a esa información** antes de devolverse. Las consultas se almacenan en una variable de consulta y se inicializa con una expresión de consulta. 
