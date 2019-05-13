ODK Collect
===========

.. admonition:: Conocimientos previos

	Para la comprensión de este apartado es necesario conocer de forma básica qué es Open Data Kit y para qué sirven las diferentes herramientas que la componen. Aunque se irá paso a paso y con detalle, Collect es una aplicación que funciona en Smartphones con el sistema operativo Android por lo que debemos estar familiarizados con la instalación, configuración y uso de aplicaciones en este entorno.  

¿Qué es ODK Collect?
--------------------

ODK Collect es la cara más visible del conjunto de herramientas que componen Open Data Kit ya que con ella es con la que interactúan la mayoría de usuarios que suelen tener el perfil de recolectores de información. Esta herramienta, diseñada como aplicación para smartphones, **permite acceder a un conjunto de formularios, rellenarlos y enviarlos** de nuevo a la base de datos donde se centraliza la información.

Al ser una **herramienta gratuita** y funcionar en un dispositivo móvil de tan amplia difusión y bajo coste, ODK se hace accesible a un gran número de usuarios en todo el mundo. Además, Collect permite utilizar las potencialidades de los smartphone para recopilar información, mediante el uso de ubicación por mapas o GPS, lectura de códigos de barras, pantalla táctil, captura y visualización de imágenes, audio y vídeo, etc., permitiendo al usuario **sistematizar la introducción de información** y utilizar información adicional aumentando la **calidad y seguridad** del siempre complicado proceso de recopilación de datos.  

.. admonition:: Recuerda

	Para la instalación de odk Collect en tu dispositivo Android debes acceder a Google Play en tu dispositivo y buscar la aplicación. Para más información sigue los pasos indicados en el apartado anterior.
	
Menú principal
--------------

Este es el menú principal una vez accedemos a la aplicación. Ocupando la mayor parte de la pantalla, mediante grandes botones rectangulares, están **accesibles los formularios**, según el estado en que se encuentren. Las opciones son las siguientes:

- **Rellenar** un nuevo formulario en blanco, seleccionando uno de la lista de los que nos hayamos descargado del servidor (1).
- Acceder a un formulario que hayamos guardado o dejado a medias y no enviado, para **modificarlo**. Una vez enviados los formularios no se pueden modificar (2).
- Seleccionar aquellos formularios rellenados que queramos **enviar** al servidor. Una vez enviados quedan guardados en el dispositivo pero no aparecen en la aplicación (3).
- Consultar los formularios **enviados** desde el dispositivo (4).
- Acceder al servidor y **descargar** al dispositivo aquellos **formularios** en blanco que se elijan (5).
- **Borrar** tanto formularios en blanco que hayamos descargado del servidor, como formularios que hayamos rellenado (6).

.. figure:: /media/menuprincipal.jpg
   :align: center

Arriba a la derecha podemos acceder a **“Ajustes”**, a través de un símbolo formado por tres puntos alineados verticalmente. Al pulsar sobre éste icono se abre un desplegable en el que, aparte del “Acerca de” que nos da acceso a recursos adicionales, tenemos dos elementos muy utilizados: “cambiar la configuración” y “opciones de administrador”.

.. figure:: /media/cambiarconf.jpg
   :align: center

Si en la pantalla principal entramos a “Llenar un nuevo formulario”, también tenemos el menú “Ajustes”. En caso de que el formulario esté diseñado en varios idiomas, nos dará la opción de “Cambiar el Idioma” y, como en el menú de “Ajustes” anterior, tendremos acceso a “Cambiar la configuración”:

.. figure:: /media/cambiarconf2.jpg
   :align: center

Cambiar la configuración
------------------------

Las opciones de “Cambiar la configuración” son de gran importancia ya que nos van a permitir **seleccionar el servidor** con el que trabajamos y **personalizar aspectos de apariencia y funcionamiento** de la aplicación de forma que ésta se adapte a nuestras necesidades. Las opciones de configuración se dividen en cuatro grandes grupos que se enumeran a continuación: 

- Servidor y parámetros de acceso (1).
- Idioma, tamaño del texto y mapas (2).
- Envío, rellenado e importación (3).
- Id. De usuario y dispositivo (4).

.. figure:: /media/cambiarconf3.jpg
   :align: center

A continuación entramos un poco más en detalle en cada una de estas opciones y repasamos sus principales funcionalidades.

Configuración del servidor
--------------------------

Lo primero que hay que hacer es elegir el **tipo** de servidor al que vamos  conectarnos (1). Lo más frecuente es que sea “ODK Aggregate” ya que es el tipo diseñado para ODK desde sus orígenes. Para conectarse a este tipo de servidores es necesario introducir la dirección web o **URL** del mismo (2) y un **usuario y contraseña** que tenga privilegios para la recolección de datos (3).

.. figure:: /media/confserver.jpg
   :align: center

Recientemente se ha implementado un nuevo tipo de servidor que se basa en el uso de la unidad de almacenamiento virtual de Google en la nube, denominada **“Google Drive”**. Para acceder a este tipo de servidor será necesario confirmar nuestros parámetros de acceso de Google y que hayamos creado la hoja de cálculo en la que se introducen las respuestas del formulario o tengamos permiso para su edición. 

.. figure:: /media/confgdrive.jpg
   :align: center

.. admonition:: Presta atención

	Los parámetros de acceso al servidor sobre el que se está trabajando deberán ser facilitados por el administrador de sistema o por el responsable del proceso de recolección de datos. En próximas unidades se explicará cómo crear tu propio servidor. 

Configuración de la interfaz de usuario
---------------------------------------

Permite personalizar aspectos de la interfaz de la aplicación. Además del **idioma** y el tamaño del **texto** (1) destaca la posibilidad de elegir la **forma en que se pasa de una pantalla a otra** en los formularios (2) y la posibilidad de elegir una **imagen o logo** para que se visualice al iniciar la aplicación (3).

.. figure:: /media/confinterfezusuario.jpg
   :align: center

Configuración de la gestión de formulario
-----------------------------------------

Permite establecer opciones por defecto para que se realicen de acuerdo con el estado de los formularios ya sea a la hora del envío o del rellenado. Las opciones más relevantes son el "Auto Envío" (1), que permite **automatizar el envío** de los formularios una vez sean completados, ya sea usando una red de datos o wifi, y el "Eliminar después de enviar" (2) que permite **eliminar los formularios** de forma automática una vez se han enviado.

.. figure:: /media/gestionform.jpg
   :align: center

Configuración de la identidad de usuario y dispositivo
------------------------------------------------------

Existe la posibilidad de introducir información identificativa del **usuario** y del **dispositivo** que pueden asociarse a cada una de los formularios que se realicen. 

.. figure:: /media/identidad.jpg
   :align: center

Algunos de estas informaciones son definidas por el usuario como el nombre del usuario, número de teléfono o la dirección de correo electrónico. Otras vienen definidas por el dispositivo y no se pueden modificar: identificador del dispositivo y del suscriptor y el número de serie de la tarjeta SIM.

Este tipo de información, aunque no suele utilizarse, es de gran importancia en caso de errores ya que permite conocer de dónde viene la información, es decir, su **trazabilidad**.

Opciones de administrador
-------------------------

En opciones de administrador es donde realmente se va a poder configurar la aplicación según conveniencia.

Se pueden dar distintas situaciones a la hora de utilizar Collect, por ejemplo los dispositivos pueden ser propiedad de los encuestadores o se les puede haber prestado para la recolección de datos; o también pueden ser usuarios avanzados o básicos. De esta forma, nos puede interesar o no, **tener habilitados más o menos menús y opciones**; en los dispositivos se queda una copia de los formularios, en caso de pérdida en el servidor se podrían recuperar, pero si los dispositivos son de los voluntarios, puede que no nos interese que se queden datos sensibles guardados; etc.

La pantalla de opciones de administrador muestra las siguientes opciones: 

- Configuración de la aplicación (1).
- Establecer una contraseña para acceder a este menú de administrador (2).
- Importar / exportar configuración mediante código QR (3).
- Opciones de la pantalla de inicio (4).
- Configuración de usuario (5).
- Configuración de rellenado de formularios (6).

.. figure:: /media/opcionesadministrador.jpg
   :align: center

De entre las anteriores, las opciones más destacadas son las siguientes: 

- Crear una **contraseña de administrador**, para la configuración de los dispositivos y que nadie más pueda modificar la configuración una vez realizada. 

.. admonition:: Práctica

	Entra en esta opción e introduce una contraseña que puedas recordar fácilmente. Luego, regresa a la pantalla principal y accede de nuevo a opciones de administrador. Deberá solicitarte la contraseña. Para deshabilitar esta opción, selecciona de nuevo “contraseña de administrador” y déjala en blanco.

- La posibilidad de crear o leer un **código QR** que permita exportar o importar la configuración de un dispositivo a otro. 
- Las opciones que puede ver el usuario en el menú principal son las que se muestran en la siguiente imagen. 	

.. figure:: /media/opcionesprincipal.jpg
   :align: center

.. admonition:: Práctica

	Desmarca la opción “enviar formulario finalizado” y observa cómo cambia la pantalla principal. Observa que, en caso de querer mantener este cambio, deberías activar también “auto envío” en “opciones de configuración\gestión del formulario”, automatizando de esta forma el proceso.

- Las opciones que puede ver el usuario en el menú opciones de usuario pueden verse en la siguiente imagen.

.. figure:: /media/opcionesusuario.jpg
   :align: center

.. admonition:: Práctica

	Deselecciona alguna de las opciones anteriores y observa que deben desaparecer cuando vuelves a su apartado correspondiente en “Cambiar la configuración”.
 
- Las opciones que puede tener el usuario al rellenar formularios se ven en la siguiente imagen.

.. figure:: /media/opcionesentryform.jpg
   :align: center

.. admonition:: Recuerda

	Al finalizar todas las pruebas vuelve a “opciones de administrador” y dale a “resetear” para volver a dejar todos los valores por defecto.

.. admonition:: Resumen y próximo pasos

	En este apartado hemos recorrido las opciones de configuración Collect, que hacen de esta aplicación una potente herramienta para la recolección de información mediante dispositivos móviles, tanto para usuarios avanzados como para personas con menos habilidad en el manejo de smartphones o tabletas. Collect permite personalizar aspectos muy relevantes de la configuración y de la apariencia e incluso la posibilidad de replicarla de unos dispositivos a otros. 
	Una vez familiarizados con el manejo de Collect, en las siguientes unidades se entrará ya en la creación de nuestros propios formularios y su visualización a través de nuestros dispositivos. 
