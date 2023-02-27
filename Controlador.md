
# Controlador En MVC

Contiene el código necesario para responder a las acciones que se solicitan en la aplicación, como visualizar un elemento, realizar una compra, una búsqueda de información, etc.

En realidad es una capa que sirve de enlace entre las vistas y los modelos, respondiendo a los mecanismos que puedan requerirse para implementar las necesidades de nuestra aplicación. Sin embargo, su responsabilidad no es manipular directamente datos, ni mostrar ningún tipo de salida, sino servir de enlace entre los modelos y las vistas para implementar las diversas necesidades del desarrollo.

# Logica del negocio

La primera lógica es muy simple e incluye: verificación de si existe disponibilidad o capacidad para proveer el producto o servicio; reserva de disponibilidad o capacidad en caso posi- tivo; y generación de alguna solución o alternativa en caso negativo.




## Ejemplo

![App Screenshot](http://codingornot.com/wp-content/uploads/2017/10/mvc-modelo-vista-controlador.png)

El proceso general para implementar un controlador de lógica de negocios es:

Cree el ensamblado del controlador de lógica de negocios.

Registre el ensamblado en el distribuidor.

Implemente el ensamblado en el servidor en el que se ejecuta el Agente de mezcla. Para una suscripción de extracción, el agente se ejecuta en el suscriptor y, para una suscripción de inserción, se ejecuta en el distribuidor. Al usar la sincronización web, el agente se ejecuta en el servidor web.

Cree un artículo que use el controlador de lógica de negocios, o bien modifique un artículo existente para usar dicho controlador.
