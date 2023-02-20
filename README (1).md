
# Investigacion acerca de MVC
Estilo de arquitectura de software que separa los datos de una aplicación, la interfaz de usuario, y la lógica de control en tres componentes distintos.
Se trata de un modelo muy maduro y que ha demostrado su validez a lo largo de los años en todo tipo de aplicaciones, y sobre multitud de lenguajes y plataformas de desarrollo.

El Modelo que contiene una representación de los datos que maneja el sistema, su lógica de negocio, y sus mecanismos de persistencia.

La Vista, o interfaz de usuario, que compone la información que se envía al cliente y los mecanismos interacción con éste.

El Controlador, que actúa como intermediario entre el Modelo y la Vista, gestionando el flujo de información entre ellos y las transformaciones para adaptar los datos a las necesidades de cada uno.

# Funcionalidades de la aplicacione
Tiene una fácil organización, puesto que solo cuenta con tres componentes.

Es un patrón que se puede adaptar a diferentes frameworks.

Se puede escalar fácilmente.

Facilita el trabajo en equipo.

# Definir la infraestructura para el almacenamiento y recuperación de datos
Modelo Vista Controlador (MVC) es un estilo de arquitectura de software que separa los datos de una aplicación, la interfaz de usuario, y la lógica de control en tres componentes distintos.

#Ejemplos 

**VISTA**

<html>
   <head>
      <title>LIBRERIA UAZON</title>
   </head>
   <body>
     <h1>Libros dados de alta en nuestra libreria</h1>
     <table border="1">
        <tr>
           <th>TITULO</th>
           <th>PRECIO</th>
        </tr>



**MODELO**

<?php
   $db = new PDO('mysql:host=localhost;dbname=uazon', 'comprador', 'proweb2013');
   $result = $db->query('SELECT titulo, precio FROM libros');
   while ($libro = $result->fetch()) {
?>
**VISTA**

<tr>
   <td><?php echo $libro['titulo']?></td>
   <td><?php echo number_format($libro['precio'],2)?></td>
</tr>
<?php
}
?>
</table>
</body>
</html>

**Controlador**
<?php
//La carpeta donde buscaremos los controladores
define ('CONTROLLERS_FOLDER', "controllers/");

//Si no se indica un controlador, este es el controlador que se usará
define ('DEFAULT_CONTROLLER', "libros");

 //Si no se indica una acción, esta acción es la que se usará
define ('DEFAULT_ACTION', "listar");

//Obtenemos el controlador.
//Si el usuario no lo introduce, seleccionamos el de por defecto.
$controller = DEFAULT_CONTROLLER;
if ( !empty ( $_GET[ 'controller' ] ) )
   $controller = $_GET [ 'controller' ];

$action = DEFAULT_ACTION;
// Obtenemos la acción seleccionada.
// Si el usuario no la introduce, seleccionamos la de por defecto.
if ( !empty ( $_GET [ 'action' ] ) )
    $action = $_GET [ 'action' ];

//Ya tenemos el controlador y la accion
//Formamos el nombre del fichero que contiene nuestro controlador
$controller = CONTROLLERS_FOLDER . $controller . '_controller.php';

//Si la variable ($controller) es un fichero lo requerimos
if ( is_file ( $controller ) )
   require_once ($controller)
else
   die ('El controlador no existe - 404 not found');

//Si la variable $action es una función la ejecutamos o detenemos el script
if ( is_callable ($action) )
   $action();
else
   die ('La accion no existe - 404 not found');
   


   
## 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://github.com/ZahiritaRuiz/Zahirita-MVC)

