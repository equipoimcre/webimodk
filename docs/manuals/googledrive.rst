.. _inicio-google-drive:

Integración con Google Drive
============================

Presentación y objetivos
------------------------

La aplicación ODK Collect ofrece varias opciones para el destino de los datos una vez se han recogido.
La forma habitual es utilizar ODK Aggregate, ya sea alojado en Google App Engine, o en tu propio servidor.
La opción que se presenta en esta unidad es más sencilla y consiste, en primer lugar, en conectar con Google Drive para permitir que ODK Collect tome formularios de tu cuenta de Drive, para finalmente enviar los datos recogidos en los formularios directamente a un documento de Hojas de cálculo de Google.

Conocimientos previos y recursos
--------------------------------

Esta unidad requiere haber completado las unidades anteriores, es decir, conocer de forma básica qué es Open Data Kit, cómo funciona la aplicación ODK Collect y cómo se diseñan los formularios con Build.
Asimismo es necesario tener una cuenta de Google y configurarla en un dispositivo Android 1.6 o superior.

.. admonition:: Nota

	Puedes crear gratuitamente una cuenta de Google en https://accounts.google.com/signup

La fuente original para la elaboración de estos contenidos es `ODK Collect and Google Drive Integration to Store and Manage Your Data <https://www.google.com/earth/outreach/learn/odk-collect-and-google-drive-integration-to-store-and-manage-your-data/>`__.

.. _subir-google-drive:

1. Subir un formulario a Google Drive
-------------------------------------

En la sección de :ref:`inicio-odk-build` vimos cómo generar un formulario.
Posteriormente debes exportarlo a formato Microsoft Excel (opción :guilabel:`Export to XLSForm` en el menú :guilabel:`File`):

.. figure:: /media/drive_build1.png
   :align: center

Si utilizas la versión web de Build el fichero se alojará probablemente en la carpeta "Descargas".
Si utilizas la opción *offline* podrás elegir con precisión dónde almacenarlo.

.. admonition:: Recuerda

	Otra forma de crear formularios es directamente desde Excel utilizando XLSForm. Lo veremos en próximas unidades.

Una vez tenemos el formulario en formato *xlsx* debemos subirlo a Google Drive con pequeños retoques para su detección y uso por las herramientas ODK.
Accede a https://drive.google.com/ e introduce tu dirección de correo electrónico de GMail y contraseña.

.. figure:: /media/google_drive1.png
   :align: center

En Google Drive haz clic en :guilabel:`Nuevo` y crea una carpeta denominada "odk" en la que irás introduciendo toda la información relacionada con tu proyecto.

.. figure:: /media/google_drive2.png
   :align: center

Ahora vamos a añadir el fichero en formato *xlsx*.
Accede a la carpeta que acabas de crear en Google Drive y haz clic otra vez en :guilabel:`Nuevo`.

.. figure:: /media/google_drive3.png
   :align: center

Selecciona :guilabel:`Subir archivo`, busca la ruta donde almacenaste el fichero *xlsx* y pulsa :guilabel:`Abrir`.


.. figure:: /media/google_drive4.png
   :align: center

Haz doble clic sobre el fichero y ábrelo usando la aplicación Hojas de Cálculo de Google.
Una vez abierto, haz una copia del fichero renombrándolo (:guilabel:`Crear una copia` en el menú :guilabel:`Archivo`).

.. figure:: /media/google_drive5.png
   :align: center

Asegúrate de que el nombre del fichero no contiene espacios y está formado sólo por caracteres alfanuméricos o guiones.
Un ejemplo de nombre válido es "odk-form".

.. figure:: /media/google_drive6.png
   :align: center

Añade una pestaña nueva a la hoja de cálculo y cámbiale el nombre (haciendo doble clic sobre el nombre, por ejemplo, "resultados"), pero no rellenes nada más.
Recuerda que sólo se pueden utilizar caracteres alfanuméricos y guiones al cambiar el nombre de la pestaña.
La pestaña "resultados" debe estar situada a la izquierda de todas las demás.
Haz clic y arrástrala si es necesario.

.. figure:: /media/google_drive7.png
   :align: center

.. figure:: /media/google_drive8.png
   :align: center

A continuación, copia la URL de la nueva hoja vacía, es decir, la que te aparece en el navegador al visualizarla.

.. figure:: /media/google_drive9.png
   :align: center

Ve a la pestaña :guilabel:`settings` y pégala bajo la celda *submission_url*. Si no tienes esa celda en tu formulario escribe *submission_url* a continuación de los otros que ya estén de forma que quede como se ve a continuación:

.. figure:: /media/google_drive10.png
   :align: center

De esta forma definimos la ruta de destino para que los datos que envíen los/las usuarios/as del formulario vayan a la hoja de resultados.
Como los cambios en Hojas de Cálculo de Google son automáticos, puedes cerrar el fichero conservando los cambios realizados.

.. admonition:: Recomendación

	Para almacenar este fichero y otros que iremos creando, crea una carpeta en Google Drive con un nombre fácilmente reconocible; por ejemplo, *odk*.

.. _conceder-permisos:

2. Conceder permisos para el acceso de otros/as usuarios/as
-----------------------------------------------------------

Para que otros/as usuarios/as puedan descargar y rellenar el formulario con ODK Collect, debes darles permiso para acceder a la hoja de cálculo de Google Drive.
Puedes añadirles individualmente o conceder acceso a cualquiera mediante un enlace.
A continuación te indicamos cómo hacerlo.

Cómo dar permisos individualmente
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Para conceder accesos individuales, haz clic con el botón secundario del ratón sobre el fichero. Selecciona :guilabel:`Compartir`

.. figure:: /media/google_drive11.png
   :align: center

Añade los correos electrónicos de los/las usuarios/as (por ejemplo, de quienes se encargarán de recoger datos sobre el terreno) y asegúrate de que tengan permiso de edición (lápiz a la derecha del cuadro de texto).

.. figure:: /media/google_drive12.png
   :align: center

Una vez compartido aparecerá el siguiente icono al lado del nombre de fichero en la vista de lista de Google Drive:

.. figure:: /media/google_drive13.png
   :align: center

Cómo dar permisos mediante un enlace
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Puedes activar la función de compartir mediante enlace para que cualquiera que reciba el enlace pueda editar la hoja.
Esto resulta útil cuando quieres que los/las usuarios/as envíen datos de forma anónima a tu proyecto de ODK (p. ej., en un proyecto de *crowdsourcing*).
Para que cualquiera pueda enviar datos, haz clic en :guilabel:`Compartir` y, a continuación, en :guilabel:`Obtener enlace para compartir`. 

.. figure:: /media/google_drive14.png
   :align: center

Al obtener el enlace para compartir la opción por defecto es de lectura (puede ver el documento, pero no editarlo).
Haz clic sobre :guilabel:`Permisos` para modificarlo.

.. figure:: /media/google_drive15.png
   :align: center

Accede al desplegable con los tipos de permisos y hac clic sobre :guilabel:`Cualquier usuario con el enlace puede editar`.
Para finalizar haz clic sobre :guilabel:`Listo`.

.. figure:: /media/google_drive16.png
   :align: center

.. admonition:: Recomendación

	Si quieres controlar quién puede editar el formulario o las respuestas, puedes proteger la pestaña de respuestas y elegir quién tiene derechos de edición.

3. Transformar el fichero a formato xml
---------------------------------------

A continuación vamos a convertir el formulario a un archivo XML para que ODK Collect pueda mostrarlo en los dispositivos móviles.
Para ello debemos convertir nuestra hoja de cálculo a formato *xlsx*.

Abre el fichero en Hojas de Cálculo de Google y en el menú :guilabel:`Archivo` selecciona :guilabel:`Descargar como Microsoft Excel (.xlsx)`.

.. figure:: /media/google_drive17.png
   :align: center

El fichero quedará alojado por defecto en la carpeta :guilabel:`Descargas` (para sistemas Windows).

Una vez tenemos el fichero *xlsx*, para convertirlo a xml utilizaremos el conversor de ODK a XLSForm online en la url http://opendatakit.org/xiframe/

.. figure:: /media/drive_build2.png
   :align: center

Selecciona el archivo y haz clic en :guilabel:`Submit`.
Aparecerá el botón para descargar el formulario en xml.
Haz clic sobre el botón y el fichero se descargará.

.. admonition:: Recuerda

   También puedes convertir tu fichero *xlsx* en XML utilizando la herramienta XLSForm Offline, descargable en la url https://gum.co/xlsform-offline. Veremos el uso de esta herramienta en próximas unidades.

Finalmente, igual que hiciste con el fichero *xlsx* en el apartado :ref:`subir-google-drive`, sube el archivo XML a tu cuenta de Google Drive.
Seguidamente puedes compartirlo, tal como vimos en el apartado :ref:`conceder-permisos`, con quienes vayan a recoger datos y necesiten descargar el formulario en su dispositivo Android.
En este caso, el permiso facilitado puede ser sólo de lectura.

.. figure:: /media/google_drive18.png
   :align: center

.. admonition:: Presta atención

   Algunas funciones de ODK no son compatibles con Hojas de Cálculo de Google. Ten en cuenta lo siguiente a la hora de diseñar tu formulario:

   - Puedes agrupar preguntas, pero no se permiten repeticiones.
   - Está permitido usar hasta 254 variables (o preguntas del formulario que se muestran en ODK Collect).
   - Se admiten fotos, pero no audio ni vídeo. Las fotos se almacenarán en tu archivo de álbumes de Google Fotos de forma oculta y se vincularán desde Hojas de Cálculo de Google.
   - Las demás funciones, incluida la ubicación GPS, son compatibles.

4. Configuración de ODK Collect
-------------------------------

Abre la aplicación ODK Collect en tu dispositivo móvil y accede a la opción :guilabel:`Cambiar la configuración` accesible a través del menú (los tres puntos situados en la esquina superior derecha.

.. figure:: /media/google_collect1.png
   :align: center

En :guilabel:`Servidor-usuario`, haz clic en :guilabel:`Tipo` para cambiar la ruta de destino de los envíos de datos desde ODK Collect.
Selecciona el protocolo :guilabel:`Google Drive, Google Sheets`.

.. figure:: /media/google_collect2.png
   :align: center

A continuación, haz clic en :guilabel:`Cuenta de Google` y selecciona la que quieras utilizar con ODK Collect.

.. image:: /media/google_collect3.png
    :width: 49 %
.. image:: /media/google_collect4.png
    :width: 49 %

En esta cuenta se almacenarán tus formularios en Google Drive, así como la hoja de cálculo con todos tus datos y los datos enviados por otros usuarios de ODK.
Ya puedes volver al menú principal de tu aplicación Collect.

.. admonition:: Atención

   El dispositivo Android debe estar conectado a una cuenta de Google que pueda editar el formulario que has creado (se le hayan concedido permisos siguiendo los pasos indicados en :ref:`conceder-permisos`.

.. admonition::  Recuerda

   Asegúrate de tener actualizada tu aplicación ODK Collect con la última versión disponible en la Play Store de Google.
