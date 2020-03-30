Información
***********

Ventana principal
=================


En la ventana principal podremos elegir entre ir a controlar los productos y servicios o
sin embargo, los clientes.
Está estructurada con dos botones principales a los que se le añade un botón para la opción
de salida.
Dentro de esta está insertado dos ventanas, las cuales hacen invisible esta al selecionarlas:

Producto
--------
En esta clase, implementa una  ventana donde aparencen los servicios y productos, los cuales el usuario decide que hacer con ellos.
Implemento para ello un GtkTreeview para enseñar los productos actuales, tres botones para elegir qué hacer con el producto seleccionado;
Nuevo con la llamada a la clase nuevoser, Eliminar con la clase eliminaser e imprimir con el método imprimir() el cual utiliza la librería Reportlab.

nuevoser
""""""""
Es una clase en la que está formada por un dos entradas de texto y un botón para accionar
la inserción del producto

eliminaser
""""""""""
La misma que la de antes solo que cambiando el cursor para borrar el campo del valor que se ingrese
imprimir()
""""""""""
En esta clase se realiza una lectura de los datos de la base para poder listar todos los productos,
para que luego sean imprimidos a través de la librería de Reportlab.

Cliente
-------
Implemento otra ventana para controlar la gestion de clientes.
Esta ventana hace que aparezca un listado de clientes y unas acciones para hacer con ellos como son añadir, elminar y consultarlos.
En esta clase me valgo de un GtkTreeView para que aparezcan toda la lista de clientes actuales, un botón imprimir para imprimir y
un combobox para seleccionar la acción que desea el usuario realizar.

Imprimir
""""""""
Si se selecciona al botón imprimir, este pasara a un cursor que devuelve la lista de clientes de la base de datos para insertarlos
en el Pdf que genera a través de la librería Reportlab

Opciones
""""""""

Si el usuario selecciona el combobox, este enviará una señal para que aparezca la susodicha clase.
Recibe un parámetro String, del Comobobox para saber qué quiere realizar el usuario.
Dependiendo de esto tenemos:

ingresar()
++++++++++
Cambia el String y el cursor para añadir un cliente

consultar()
+++++++++++

Aprece un Treeview con el resulado de la busqueda de Clientes y un combobox para seleccionar cuál de ellos es el que buscas.

eliminar()
++++++++++
Cambia el String y el cursor para eliminar un cliente
