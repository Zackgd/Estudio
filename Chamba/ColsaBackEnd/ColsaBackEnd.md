### Introducción:
Todo el sistema esta implementado en el lenguaje C# .net, utilizando MySQL para la base de datos

-----------------------------------------------------------------

### Funcionalidades Clave del Back
- __Carga y Validación de Configuraciones Personalizadas:__
	- Se usa `appSettings.json` para configurar la aplicación
	- Se leen los _secretos de entorno_ `Enviroment.GetEnvironmentVariable` como contraseñas y claves privadas.
	- Validación de existencias de configuraciones criticas 
- __Logging Avanzado con Nlog:__
	- Uso de [[Nlog]] con configuración externa `config/nlog.config`.
	- Se usa un método personalizado `CreateLogger<T>()` para crear loggers independientes por clase
	- Logging de red, IP local y estado del proceso.
- __Configuración Regional/Cultural__ 
	- Cambios en __CulturaInfo__ para definir punto decimal `.`: Se establece una configuración personalizada de la cultura o región para toda la aplicación modificando el separador decimal por punto, esto asegura que los formatos numéricos y monetarios utilicen esto independientemente de la configuración regional del sistema.
- [[Json Web Token (JWT)]]
	- Se configura autenticación y validación de tokens JWT con parámetros como:
		- `IssuerSigningKey`
		- `ValidIssuer`
		- `ValidAudience`
		- `ClockSkew`
- __Manejo de Errores Globales__
	- Captura de errores no manejados `UnhandledException`
	- Apagado forzoso del proceso si ocurren fallos críticos (`Kill()`)
- __Carga de Librerias Externas__
	- Se cargan dinámicamente configuraciones de [[MailFormats.dll]] y [[InformesTools.dll]]
- __Prevención de Instancias Duplicadas.__
	- Se verifica si el proceso ya esta corriendo usando ``Process.GetProcessesByName``: El código verifica si ya existe una instancia en ejecución del proceso utilizando el nombre del archivo ejecutable, este es útil para evitar múltiples instancias de la aplicación se ejecuten simultáneamente, lo cual podría causar conflictos
- __[[WebSockets]]__
	- Habilitación de [[WebSockets]] y configuración de `KeepAliveInterval`
- Archivos Estáticos en Carpeta Temporal
	- Se configura [[UseStaticFiles]] para exponer archivos bajo ``/temp``
- [[Hosted Services]] 
	- Se agregan varios servicios que corren en segundo plano:
		- `AlarmasServices`
		- ``MessageResponseService``
		- ``TokenService``
		- ``RecordatoriosService``
		- ``CheckServicioAduana``
		- ``ODTExcedidasService``
- [[Health Checks]]
	- Se expone un endpoint de [[Health Checks]] (`/Health/Index`)
	- Se implementa un `HealthCheckServices` personalizado
- [[CORS]]
	- Configuración distinta para __Development__ y __Producción__
	- Permite orígenes específicos en producción 
- [[Swagger]]
	- Documentación Swagger usando `NSwag`
- [[Middleware]] __Personalizado__
	- Se utiliza un [[Middleware]] propio: `AspNetCore.Middlewares.RequestMiddleware`
- __Configuración__ [[NHibernate]] 
	- Se configura NHibernate con `addNHibernateSutomConvencions`
	- Uso de convenciones personalizadas desde `HhibernateHelper`
- Serialización __JSON__
	- Se agregan convertidores personalizados como:
		- `StringTrimmerJsonConverter`
		- ``DateTimeProvider`` con formato `yyyy-MM-ddTHH:mm:ss`
- [[Controladores MVC ]]con Vistas
	- Uso de `AddControllerWithViews`
	- Inserción de un `CustomModelBinderProvider`




### __Patrones y Buenas Practicas__

- [[Singleton]]
- [[Factory Method]]
- [[Dependency Injection]]
- [[Middleware]]
- [[Hosted Services]]
- [[Configuration Binding]]
- [[Fail-Fast]]
- [[Cultura Invariante]]
- [[Modularización]]
