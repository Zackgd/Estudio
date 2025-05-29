El rendimiento de la aplicación decae significativamente cada vez que se quiere acceder a la base de datos en busca de actualizaciones o información que requiere tu sistema.
==La base de datos es una de las partes mas lentas del sistema.==

Una practica muy buena en estos casos en el uso de Caches
Una cache es una forma de almacenar datos en memoria para que no tengas que ir a buscarlos cada vez que los necesites.
Son difíciles de configurar que simplemente hacer otra consulta mas, a la larga es mas eficiente.

La próxima vez que estés escribiendo código que acceda constantemente a la base de datos para obtener información que cambia poco, detente un momento y piensa: “¿podría esto ser almacenado en una caché?” Tu aplicación y tus usuarios te lo agradecerán.