ODK Collect
===========

.. admonition:: Conocimientos previos

	Para la comprensión de este apartado es necesario conocer de forma básica qué es Open Data Kit y para qué sirven las diferentes herramientas que la componen. Aunque se irá paso a paso y con detalle, Collect es una aplicación que funciona en dispositivos con el sistema operativo Android por lo que debemos familiarizarnos con la instalación, configuración y uso de aplicaciones en este entorno.

¿Qué es ODK Collect?
--------------------

ODK Collect es la cara más visible del conjunto de herramientas que componen Open Data Kit ya que con ella es con la que interactúan la mayoría de usuarios y usuarias con el perfil de recolectores de información.
Esta herramienta, diseñada como aplicación para *smartphones*, **permite acceder a un conjunto de formularios, rellenarlos y enviarlos** de nuevo a la base de datos donde se centraliza la información.

Al ser una **herramienta gratuita** y funcionar en un dispositivo móvil de tan amplia difusión y bajo coste, ODK se hace accesible a un gran número de personas en todo el mundo.
Además, Collect permite utilizar las potencialidades de los *smartphones* para recopilar información, mediante el uso de ubicación por mapas o GPS, lectura de códigos de barras, pantalla táctil, captura y visualización de imágenes, audio y vídeo, etc., permitiendo **sistematizar la introducción de información** y utilizar información adicional aumentando la **calidad y seguridad** del siempre complicado proceso de recopilación de datos.

.. admonition:: Recuerda

	Para la instalación de ODK Collect en tu dispositivo Android debes acceder a *Google Play* y buscar la aplicación. Para más información sigue los pasos indicados en el apartado :ref:`introduccion-label`.

Menú principal
--------------

Esta es la primera pantalla que vemos cuando accedemos a la aplicación.
Ocupando la mayor parte de la pantalla, mediante grandes botones rectangulares, están **accesibles los formularios**, según el estado en que se encuentren.
Las opciones son las siguientes:

- **Rellenar** un nuevo formulario en blanco, seleccionando uno de la lista de los que nos hayamos descargado del servidor (1).
- Acceder a un formulario que hayamos guardado o dejado a medias y no enviado, para **modificarlo**. Una vez enviados los formularios no se pueden modificar (2).
- Seleccionar aquellos formularios rellenados que queramos **enviar** al servidor. Una vez enviados quedan guardados en el dispositivo pero no aparecen en la aplicación (3).
- Consultar los formularios **enviados** desde el dispositivo (4).
- Acceder al servidor y **descargar** al dispositivo aquellos **formularios** en blanco que se elijan (5).
- **Borrar** tanto formularios en blanco que hayamos descargado del servidor, como formularios que hayamos rellenado (6).

.. figure:: /media/menuprincipal.png
   :align: center
   :width: 280

Arriba a la derecha podemos acceder a **“Ajustes”**, a través de un símbolo formado por tres puntos alineados verticalmente.
Al pulsar sobre este icono (1) se abre un desplegable en el que, aparte del “Acerca de” que nos da acceso a recursos adicionales, tenemos dos elementos muy utilizados: “Cambiar la configuración” (2) y “Opciones de administrador”.

.. figure:: /media/cambiarconf.png
   :align: center
   :width: 600

Si en la pantalla principal entramos a “Llenar un nuevo formulario”, también tenemos el menú “Ajustes”. En caso de que el formulario esté diseñado en varios idiomas, nos dará la opción de “Cambiar el Idioma” y, como en el menú de “Ajustes” anterior, tendremos acceso a “Cambiar la configuración”:

.. figure:: /media/cambiarconf2.jpg
   :align: center

Cambiar la configuración
------------------------

Las opciones de “Cambiar la configuración” son de gran importancia ya que nos van a permitir **seleccionar el servidor** con el que trabajamos y **personalizar aspectos de apariencia y funcionamiento** de la aplicación de forma que ésta se adapte a nuestras necesidades.
Las opciones de configuración se dividen en cuatro grandes grupos que se enumeran a continuación:

- Servidor - Usuario (1), para configurar el servidor y los parámetros de acceso.
- Interfaz de usuario (2), donde se pueden personalizar opciones visuales de la aplicación, a destacar el idioma o tamaño del texto, además de otras opciones referentes a la navegación.
- Mapas (3), que contiene opciones exclusivas a cartografía.
- Manejo de formularios (4), con opciones sobre el envío, rellenado e importación.
- Metadatos del formulario (5), para indicar el identificador de usuario/a o del dispositivo.

.. figure:: /media/cambiarconf3.png
   :align: center
   :width: 280

A continuación entramos un poco más en detalle en cada una de estas opciones y repasamos sus principales funcionalidades.

Servidor
^^^^^^^^

Lo primero que hay que hacer es elegir el **tipo** de servidor al que vamos a conectarnos (1).
Lo más frecuente es que sea “ODK Aggregate” ya que es el tipo diseñado para ODK desde sus orígenes. 
Para conectarse a este tipo de servidor es necesario introducir la dirección web o **URL** del mismo (2) y un **usuario y contraseña** que tenga privilegios para la recolección de datos (3).

.. figure:: /media/collect_confserver.jpg
   :align: center

También se encuentra disponible un nuevo tipo de servidor que se basa en el uso de la unidad de almacenamiento virtual de Google en la nube, denominada **“Google Drive”**.
Para acceder a este tipo de servidor será necesario confirmar nuestros parámetros de acceso de Google y que hayamos creado la hoja de cálculo en la que se introducen las respuestas del formulario o tengamos permiso para su edición.

.. admonition:: Presta atención

	Los parámetros de acceso al servidor sobre el que se está trabajando deberán ser facilitados por alguien con permisos para administrar el sistema o por la persona responsable del proceso de recolección de datos. En próximas unidades se explicará cómo crear un servidor propio.

Interfaz de usuario
^^^^^^^^^^^^^^^^^^^

Permite personalizar aspectos de la interfaz de la aplicación.
Además del **idioma de la aplicación** (1) --no el del formulario-- y el tamaño del **texto** (2), destaca la posibilidad de elegir la **forma en que se pasa de una pantalla a otra** en los formularios (3), y la posibilidad de elegir una **imagen o logo** para que se visualice al iniciar la aplicación (4).

.. figure:: /media/confinterfazusuario.jpg
   :align: center

Mapas
^^^^^

En esta pantalla se pueden cambiar todas las opciones referentes a cartografía, tales como la fuente que se usará para mostrar los mapas --Google, OpenStreetMap, etc.-- (1); el estilo de mapa, en caso de que la fuente seleccionada disponga de varias opciones (2), y archivos de capas a elegir entre los presentes en el dispositivo, si los hubiera (3).

.. figure:: /media/mapas.png
   :align: center
   :width: 280

Manejo de formularios
^^^^^^^^^^^^^^^^^^^^^

Permite establecer opciones por defecto para que se realicen de acuerdo con el estado de los formularios ya sea a la hora del envío o del rellenado.

Respecto al envío, las opciones más relevantes son el :guilabel:`Envío Automático` (1), que permite **automatizar el envío** de los formularios una vez sean completados, ya sea usando una red de datos o wifi, y el :guilabel:`Eliminar después de enviar` (2) que permite **eliminar los formularios** de forma automática una vez se han enviado.

En relación al rellenado de formularios son importantes el **manejo de restricciones** (3) que configura el momento el que se aplican los controles y validaciones sobre la información introducida, y el **formato y tamaño de vídeos y fotos** que debe tenerse en cuenta, sobre todo, si hay condicionantes de cara a la transmisión de la información.

.. figure:: /media/gestionform.jpg
   :align: center

Metadatos del formulario
^^^^^^^^^^^^^^^^^^^^^^^^

Existe la posibilidad de introducir información identificativa del **usuario** y del **dispositivo** que pueden asociarse a cada una de los formularios que se realicen. 

.. figure:: /media/identidad.jpg
   :align: center

Algunos de estos campos son definidos por quien introduce los datos, tales como el nombre de usuario (1), número de teléfono (2) o la dirección de correo electrónico (3).
Otros vienen definidos por el dispositivo y no se pueden modificar (4): identificador del dispositivo y del suscriptor y el número de serie de la tarjeta SIM.

.. figure:: /media/identidad2.jpg
   :align: center

Este tipo de información, aunque no suele utilizarse, es de gran importancia en caso de errores ya que permite conocer de dónde viene la información, es decir, su **trazabilidad**.

Opciones de administrador
-------------------------

En opciones de administrador es donde realmente se va a poder configurar la aplicación a conveniencia.

Se pueden dar distintas situaciones a la hora de utilizar Collect. Por ejemplo, los dispositivos pueden ser propiedad de los/as encuestadores/as o se les puede haber prestado para la recolección de datos; o también pueden ser usuarios/as con diferentes niveles de conocimiento sobre ODK.
De esta forma, nos puede interesar o no **tener habilitados más o menos menús y opciones**; en los dispositivos se queda una copia de los formularios, en caso de pérdida en el servidor se podrían recuperar; pero si los dispositivos no pertenecen a Cruz Roja, puede que no nos interese que se queden datos sensibles guardados.

La pantalla de *Opciones de administrador* muestra las siguientes opciones: 

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

.. figure:: /media/opcionesadmin_password.jpg
   :align: center

.. admonition:: Práctica

	Entra en esta opción e introduce una contraseña que puedas recordar fácilmente. Luego, regresa a la pantalla principal y accede de nuevo a :guilabel:`Opciones de administrador`. Deberá solicitarte la contraseña. Para deshabilitar esta opción, selecciona de nuevo :guilabel:`Contraseña de administrador` y déjala en blanco.

- La posibilidad de crear o leer un **código QR** que permita exportar o importar la configuración de un dispositivo a otro. El código QR generado permite su lectura desde otro dispositivo a través de nuestra cámara de fotos, utilizando la opción :guilabel:`Escanear código de otro dispositivo`.

.. figure:: /media/opcionesadmin_codigoqr.jpg
   :align: center

- Las opciones que pueden verse en el **menú principal de ajustes** son las que se muestran en la siguiente imagen.

.. figure:: /media/opcionesprincipal.jpg
   :align: center

.. admonition:: Práctica

	Desmarca la opción :guilabel:`Enviar formulario finalizado` y observa cómo cambia la pantalla principal. Observa que, en caso de querer mantener este cambio, deberías activar también :guilabel:`Envío Automático` en :guilabel:`Cambiar de configuración` / :guilabel:`Manejo de formularios`, automatizando de esta forma el proceso.

- Las posibilidades de personalizar las opciones a las que los/las usuarios/as podrán acceder son innumerables, abarcando prácticamente todas las existentes en la aplicación. A continuación se muestra la lista de todas ellas tal como aparecen en el apartado :guilabel:`Ajustes de usuario`.

.. figure:: /media/opcionesusuario.jpg
   :align: center

.. admonition:: Práctica

	Desmarca alguna de las :guilabel:`Opciones de usuario` anteriores y observa que han desaparecido cuando vuelves a su apartado correspondiente.
 
- Las opciones que puede disponibles al rellenar formularios pueden configurarse en la siguiente pantalla. Destaca el acceso a :guilabel:`Cambiar la configuración` (1) y a :guilabel:`Cambiar el idioma` (2) entre los disponibles para el formulario.

.. figure:: /media/opcionesentryform.jpg
   :align: center

.. admonition:: Recuerda

	Al finalizar todas las pruebas vuelve a :guilabel:`Opciones de administrador` y dale a :guilabel:`Restablecer aplicación` para volver a dejar todos los valores por defecto.

Resumen y próximo pasos
^^^^^^^^^^^^^^^^^^^^^^^

En este apartado hemos recorrido las opciones de configuración de ODK Collect, que hacen de esta aplicación una potente herramienta para la recolección de información mediante dispositivos móviles, tanto para usuarios/as con conocimientos avanzados como para quienes disponen de menos experiencia en el manejo de *smartphones* o tabletas.
Collect permite personalizar muchos aspectos relevantes de la configuración y de la apariencia e incluso la posibilidad de replicarla rápidamente de unos dispositivos a otros. 
Una vez familiarizados con el manejo de Collect, en las siguientes unidades se entrará ya en la creación de nuestros propios formularios y su visualización a través de nuestros dispositivos. 
