ODK Build
=========

.. admonition:: Conocimientos previos

	Para la comprensión de este apartado es necesario conocer de forma básica qué es Open Data Kit y cómo funciona la aplicación ODK Collect, tanto a nivel de configuración como de gestión y cumplimentación de formularios.
	
	Asimismo es necesario tener conocimientos básicos sobre la navegación y funcionamiento de aplicaciones web.

¿Qué es ODK Build?
------------------

Build es una herramienta que permite la creación de formularios de Open Data Kit.
Mediante una sencilla interfaz pueden diseñarse las diferentes preguntas y posibles respuestas así como añadir diferentes tipos de material audiovisual.

Originalmente estaba disponible como una herramienta en línea accesible a través de la url: https://build.getodk.org/ con las ventajas de su accesibilidad y disponibilidad de la información en cualquier lugar del mundo.
Más recientemente se ha creado una versión offline descargable desde el mismo sitio web, que permite superar las limitaciones derivadas de la dificultad de acceso a Internet en determinados lugares y circunstancias.

El objetivo de este apartado es familiarizarnos con sus funciones y características principales de forma que podamos generar nuestro primer formulario.

.. admonition:: Recuerda

	Aunque Build presenta limitaciones en el diseño de los formularios respecto a Microsoft Excel, es una herramienta muy efectiva para el diseño de formularios sencillos y, sobre todo, para todas las personas que se estén iniciando en el mundo de ODK.

.. admonition:: Recuerda

	Además de Build y Collect, la otra gran pieza de ODK es el servidor al que conectaremos para descargar los formularios en blanco y almacenar los ya completados. Ese servidor puede ser de tipo ODK Aggregate o de tipo Google Drive.

Tipos de datos
--------------

Antes de empezar a entender cómo funciona la herramienta, necesitamos entender los tipos de datos que vamos a poder elegir en los formularios.

¿Qué quiere decir esto?

En un formulario o encuesta, vamos a realizar una serie de preguntas.
Cada una de estas preguntas tendrá diferentes tipos de respuesta, es decir, a una determinada pregunta y según cómo esté descrita, la persona que grabe las respuestas tendrá que hacerlo con un texto, con un número, con una fecha, una fotografía, etc.
El formato en el que queremos que nos respondan, es el tipo de dato.

A continuación se muestra una tabla con los tipos de datos que nos vamos a encontrar, su descripción, y un ejemplo de pregunta cuya respuesta sería ese tipo de dato.

.. list-table::
   :header-rows: 1
   :widths: auto

   * - Tipo de Dato
     - Descripción de la Respuesta
     - Ejemplo de Pregunta
   * - Text
     - Se introduce un texto. Aparece el teclado con todos los caracteres
     - ¿Cómo te llamas?
   * - Numeric
     - Se introduce un número. Se puede elegir que la respuesta sea un número entero o decimal. Aparece el teclado de números
     - ¿Cuántos años tienes?
   * - Date/Time
     - Se introduce una fecha y/u hora en un formato de calendario o reloj, respectivamente. Se puede elegir que la respuesta sea una fecha completa, año, año y mes, y fecha completa y hora
     - ¿En qué año naciste?
   * - Time
     - Se introduce una hora en formato de reloj digital
     - ¿A qué hora es la distribución?
   * - Location
     - Se graban unas coordenadas geográficas. La respuesta puede ser un punto, una serie de puntos o un área. Se puede recoger con el GPS por defecto, señalándolo en el mapa o de forma manual
     - Registra tu posición actual
   * - Media
     - Se puede hacer o elegir una fotografía, un audio o un vídeo
     - Haz una foto de la instalación
   * - Barcode
     - Se escanea un código de barras o código QR. Es necesario tener un programa instalado en el dispositivo para este propósito
     - Escanea el código de barras de la tarjeta del beneficiario
   * - Choose One
     - Se puede elegir una sola opción de las posibilidades que nos den
     - Selecciona el género del o de la beneficiario/a: masculino, femenino, desconocido
   * - Select Multiple
     - Se puede elegir una o varias opciones de las posibilidades que nos den
     - Selecciona las necesidades más urgentes: agua, comida, refugio, dinero
   * - Metadata
     - Este tipo de dato no tiene una pregunta en el formulario, sino que envía al servidor con un valor por defecto
     - ID del dispositivo, hora de comienzo y/o final de la encuesta, fecha, nombre de usuario, ID del suscriptor, número de serie de la SIM, número de teléfono

.. admonition:: Práctica
	
	Piensa con detenimiento a qué tipo de dato corresponderían las respuestas a las siguientes preguntas:
	
	- La fecha de nacimiento
	- La foto de la persona beneficiaria
	- Indica qué días de la semana trabajas: L, M, MX, J, V, S, D
	- ¿Has recibido ayuda de Cruz Roja Española anteriormente? Sí, No
	- Indica tu altura.
	- Indica el número de voluntarios/as que han participado en la actividad.
	- Indica tu nivel de satisfacción con las jornadas: Muy satisfecho/a, Satisfecho/a, Poco satisfecho/a, Nada satisfecho/a
	- ¿En qué localidad se está llevando a cabo esta encuesta?
	- ¿De qué provincia procedes? Segovia, Toledo, Madrid, Ávila, Otros
	- ¿Cuántos miembros tiene la familia?

Crear una cuenta en Build
-------------------------

A continuación se va a ver cómo crear una cuenta en Build.
Para ello se requiere tener una conexión a Internet.

Internet Explorer impide algunas funcionalidades, por esta razón se recomienda utilizar uno de los siguientes navegadores de Internet:
    • Google Chrome (https://www.google.es/chrome/browser/desktop/) 
    • Firefox (https://www.mozilla.org/es-ES/firefox/new/) 

En el navegador vamos a la siguiente página: https://build.getodk.org/

Al entrar, nos sale la siguiente pantalla: si estamos registrados podemos introducir el usuario y la contraseña, pero la primera vez tendremos que hacer clic en :guilabel:`Dont’t yet have an account?`

.. figure:: /media/build_signin.jpg
   :align: center

Entonces habrá que proceder a rellenar los siguientes datos:

.. figure:: /media/build_signin2.jpg
   :align: center

Una vez finalizado, se hace clic en :guilabel:`Sign up`, y la cuenta ya está creada.

Panel principal
---------------

Este es el panel con el que nos encontramos al entrar en Build:

.. figure:: /media/build_panel.jpg
   :align: center

**Nombre del formulario**: permite renombrar un formulario. Si no se le da un nombre se guardará por defecto como :guilabel:`Untitled Form` y finalmente te puedes encontrar con varios con el mismo nombre. Para ello, hay que hacer clic en :guilabel:`rename` y una vez escrito el nuevo nombre, hacer clic en :guilabel:`done`:

.. figure:: /media/build_nombre.jpg
   :align: center

**Menús de Build**: proporciona varios menús donde poder gestionar el formulario:

- *File*: tiene los siguientes submenús:

	- New Form: crear un nuevo formulario.
    	- My Forms: da la opción de abrir un formulario guardado previamente dentro de la lista de formularios guardados.
    	- Save: guardar un formulario, es recomendable haberlo nombrado con anterioridad. Si no, te lo guarda sobre el formulario que estés. Por otro lado, es recomendable ir pulsando :guilabel:`Save` cuando se está haciendo un formulario nombrado previamente para no perder los cambios.
    	- Save Form As: permite guardar un formulario con el nombre que se desee.
    	- Save Form to File: permite descargarte el formulario en formato **.odkbuild**. Este archivo te permite poder enviarlo y abrirlo desde otra cuenta Build.
    	- Load Form from File: permite abrir en Build un archivo **.odkbuild**. Para ello tendrás que hacer clic en :guilabel:`Choose` (1) y elegir el archivo en la ubicación donde se encuentre, y hacer clic en :guilabel:`Load` (2). Recuerda haber guardado el formulario anterior si estuvieses trabajando en uno.

.. figure:: /media/build_loadform.jpg
   :align: center

    	- Upload Form to Aggregate: permite exportar el formulario en blanco que se ha creado, directamente a Aggregate. Se verá en el apartado :guilabel:`Exportar un formulario`.
    	- Export to XML: permite descargar el formulario en formato XML.
    	- Export to XLSForm: permite descargar el formulario con extensión **.xlsx** (Microsoft Excel), que posibilita hacer formularios más complejos y versátiles.

.. admonition:: Recuerda

	Build no guarda los cambios automáticamente. Es importante guardar los formularios que se vayan creando así como las modificaciones que se les haga. Sobre todo antes de abrir nuevos formularios o de cerrar la sesión. No obstante, Build suele mostrar mensajes como de advertencia como el siguiente:
	
	.. figure:: /media/build_aviso.jpg
		:align: center

- *Edit*: además de opciones comunes a otros programas de edición (:guilabel:`Cut`, :guilabel:`Copy`, :guilabel:`Paste`, :guilabel:`Undo` y :guilabel:`Redo`), este menú tiene la opción :guilabel:`Manage Translations`, la cual lleva a la ventana mostrada a continuación:

.. figure:: /media/build_manage_translations.jpg
   :align: center

En el desplegable que dice “Add a new language”, se escribe el nombre del idioma que quieres añadir.
Una vez escrito se hace clic en :guilabel:`Add Translation`:

.. figure:: /media/build_add_translation.jpg
   :align: center

Se pueden añadir tantos idiomas como se desee, así como eliminar el que no se quiera, haciendo clic en :guilabel:`remove`.
Cuando se ha finalizado se hace clic en :guilabel:`Done`.

.. figure:: /media/build_manage_translations_done.jpg
   :align: center

- *View*: en la primera parte, permite elegir en qué idioma se quieren ver las preguntas del formulario que se está haciendo, en caso de tener más de uno. La opción de :guilabel:`Collapse Questions` permite cambiar la visualización de las preguntas en Build (ver más o menos información en el Área Principal).
- *Help*: proporciona información sobre Build, su autora, enlaces para inspeccionar el código y reportar fallos que se encuentren en la herramienta.

**Área Principal**: es donde van a aparecer todas las preguntas que se vayan configurando en el formulario.

**Tipos de Datos**: cada vez que se quiera añadir una pregunta al formulario, hay que hacer clic en el tipo de dato que queremos obtener.

**Área de propiedades**: al añadir una pregunta o un tipo de dato, en el área de propiedades aparecerán una serie de elementos para configurar las preguntas.

Cómo crear un formulario
------------------------

Añadir preguntas a un formulario
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Para añadir preguntas a un formulario, únicamente hay que hacer clic sobre el tipo de dato que deseamos tener como respuesta de la pregunta que vamos a formular y configurar.

Por ejemplo, al hacer clic en :guilabel:`Text` (1), aparece la pregunta en el rectángulo del Área Principal (2) y, a la derecha en vertical, el Área de Propiedades (3) para esa pregunta: 

.. figure:: /media/build_add_question.jpg
   :align: center

Configuración de propiedades
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A continuación vamos a ver cómo se configuran y cuáles son las propiedades de una pregunta de tipo texto:

- Nombre del dato o variable (1): es el nombre que se guarda como referencia en la base de datos (BD). No puede tener espacios ni caracteres especiales. Será el nombre de la columna en la BD. Ej. nombre_del_entrevistado. Campo obligatorio.
- Texto del título (2): se define la pregunta que se quiere hacer y que se mostrará al usuario en el dispositivo móvil. Si se realiza el formulario en varios idiomas, habrá que incluir la pregunta o el texto en dichos idiomas en sus respectivos campos. Ej. Escriba el nombre del entrevistado. Campo obligatorio.
- Pista (3): ayuda adicional o aclaración para entender la pregunta que se muestra al usuario en el dispositivo móvil. Ej. Nombre y apellido. Campo recomendado.
- Valor por defecto (4): este texto será la respuesta por defecto a menos que el usuario la modifique. Ej. Juan Valdez. Rara vez utilizado.
- Solo lectura (5): el usuario no puede introducir datos, sólo leer lo que dice el texto o pregunta. Rara vez utilizado.
- Requerido (6): si se marca esta casilla, el usuario no puede pasar a la siguiente pregunta a menos que la pregunta actual sea respondida. Opcional.
- Longitud (7): el usuario no puede pasar a la siguiente pregunta a menos que la respuesta de la pregunta actual tenga una cantidad específica de caracteres:
	- Mínimo. La cantidad mínima de caracteres requerida.
	- Máximo. La cantidad máxima de caracteres aceptada.
	Ej. Mínimo 5, Máximo 10: la respuesta debe tener entre 6 y 9 caracteres. Si se seleccionan las opciones :guilabel:`incluyente` la respuesta debe tener entre 5 y 10 caracteres. Opcional.
- Texto inválido (8): mensaje que se muestra si no se cumple la longitud establecida anteriormente. A veces esta opción no funciona adecuadamente.

.. figure:: /media/build_properties_area.jpg
   :align: center

Posteriormente se ofrecen opciones avanzadas:

- Mostrar pregunta si (9): condición que debe cumplirse en una pregunta previa para que ésta se muestre.
- Condición (10): se impone una restricción o limitación al dato que se introduce.
- Cálculo (11): permite realizar un cálculo dentro del propio formulario basado en valores registrados en preguntas previas.

.. figure:: /media/build_properties_area_advanced.jpg
   :align: center

A continuación se muestra un ejemplo de cómo se muestra una pregunta en ODK Collect y en el servidor (ODK Aggregate o Google Drive), según la configuración en Build.
Observa con detenimiento cómo se refleja la variable (1), el texto del título (2) y la pista (3).

.. figure:: /media/build_question_example.jpg
   :align: center

Según los tipos de preguntas, hay algunas particularidades:

- Con algunos tipos de preguntas aparecerá una nueva propiedad, :guilabel:`Kind`, esto mostrará subtipos de formato en los que se pide introducir esa respuesta en el formulario en ODK Collect; se elige según conveniencia. En caso de no seleccionar ninguno aparecerá el que esté seleccionado por defecto:

.. list-table::
   :header-rows: 1
   :widths: auto

   * - Tipo de Dato
     - Opciones de Kind
     - Descripción
   * - Numeric
     - Integer / Decimal
     - **Integer**: sólo se puede introducir un número entero. **Decimal**: se puede introducir un número decimal o entero.
   * - Date/Time
     - Full Date / Year and Month / Year / Full Date and Time
     - **Full Date**: se pide introducir una fecha completa, es decir, día, mes y año. **Year and Month**: se pide introducir año y mes. **Year**: se pide introducir el año. **Full Date and Time**: se pide introducir fecha complete y una hora.
   * - Location 
     - Point / Path / Shape
     - **Point**: se pide que se introduzca la localización en un punto. **Path**: se pide que se introduzca varias localizaciones formando un camino. **Shape**: se pide que se introduzca varias localizaciones formando una forma cerrada.
   * - Media
     - Image / Audio / Video
     - **Image**: el formulario pide una imagen de archivo o nueva. **Audio**: el formulario pide un audio de archivo o nuevo. **Video**: el formulario pide un video de archivo o nuevo.
   * - Metadata
     - Device ID / Start Time / End Time / Today / Username / Suscriber ID / SIM Serial / Phone Number
     - **Device ID**: se graba automáticamente el ID del dispositivo. **Start Time**: se graba automáticamente la hora de comienzo de la encuesta. **End Time**: se graba automáticamente la hora de finalización de la encuesta. **Today**: se graba automáticamente el día. **Username**: se graba automáticamente el nombre del usuario del dispositivo. **Subscriber ID**: se graba automáticamente el ID del suscriptor. **SIM Serial**: se graba automáticamente el número de serie de la SIM. **Phone Number**: se graba automáticamente el número de teléfono. Estos datos se grabarán si están disponibles en el dispositivo. Puede que no todos se puedan; dependerá del dispositivo y de si se tiene SIM o no.

- En otras preguntas aparece una opción que es :guilabel:`Style`:

.. list-table::
   :header-rows: 1
   :widths: auto

   * - Tipo de Dato
     - Opciones de Style
     - Descripción
   * - Location 
     - Default (GPS) / Show Map (GPS) / Manual (No GPS)
     - **Default (GPS)**: al solicitar la localización en el formulario, toma los datos del sensor de GPS del dispositivo. **Show Map (GPS)**: al solicitar la localización se muestra el punto del GPS sobre el mapa. **Manual (No GPS)**: al solicitar la localización se muestra el punto del GPS sobre el mapa, pudiendo grabar ese punto u otro seleccionado manualmente sobre el mapa.
   * - Choose One & Select Multiple 
     - Default / Minimal (spinner) / Table / Horizontal Layout
     - **Default**: en el formulario aparecen todas las opciones. **Minimal (spinner)**: en el formulario las opciones aparecen en un desplegable. **Table**: no funciona correctamente. **Horizontal Layout**: se supone que las opciones aparecen de forma horizontal, pero no funciona correctamente.

- En el caso de :guilabel:`Choose One` o :guilabel:`Select Multiple` hay que añadir las opciones, y para ello hay dos formas posibles en el Área de Propiedades:

	- Haciendo clic en :guilabel:`Add Option` en el Área de Propiedades para configurar cada una de las opciones que quieras añadir.

	.. figure:: /media/build_add_option.jpg
   		:align: center


	- Haciendo clic en :guilabel:`bulk edit` en el Área de Propiedades y rellenar en cada línea las dos columnas para cada una de las opciones que se quiera añadir.

	.. figure:: /media/build_add_option2.jpg
   		:align: center

Para ambos casos:

- En el o los idiomas que se hayan elegido; :guilabel:`English` y/o :guilabel:`Spanish`, etc., se pone el texto de la opción como se quiere que aparezca en el formulario al leer la pregunta.
- El campo :guilabel:`Underlying Value` hace referencia a cómo queremos que se guarde esa opción en la base de datos de Aggregate. El texto que se introduzca no puede tener ni espacios ni caracteres especiales.

.. admonition:: Presta atención

	Es muy importante rellenar todos los campos que se generan según el número de opciones e idiomas que se añadan, incluido el :guilabel:`Underlying Value`. Si hay algún error o falta algún campo, se pondrá la pregunta en rojo indicando que hay un error. El texto que se introduzca en :guilabel:`Underlying Value` no puede tener ni espacios ni caracteres especiales, sí se pueden utilizar guiones bajos en lugar de espacios.

A continuación se muestra un ejemplo:

.. figure:: /media/build_add_option3.jpg
   :align: center

En caso de haber hecho clic en :guilabel:`bulk edit` se vería la siguiente pantalla con los datos incluidos:

.. figure:: /media/build_add_option4.jpg
   :align: center

A continuación podemos ver cómo queda reflejado en ODK Collect, Aggregate y Google Sheets.

.. figure:: /media/build_add_option5.jpg
   :align: center

Subir al servidor
-----------------

Una vez que tenemos el formulario finalizado, hay varias formas de subirlo al servidor:

Desde Build 
^^^^^^^^^^^

Permite subir el formulario en blanco que se ha creado, directamente al servidor Aggregate.
Para ello, hay que introducir la dirección o URL del servidor, el usuario y la contraseña correspondiente, y pulsar :guilabel:`Export`:

.. figure:: /media/build_upload.jpg
   :align: center

En caso de ser correcta la subida al servidor, aparece la siguiente pantalla o aviso en la parte inferior derecha de la pantalla:

.. figure:: /media/build_upload_success.jpg
   :align: center

En caso de haber algún error en los datos de conexión aparece el siguiente aviso:

.. figure:: /media/build_upload_error.jpg
   :align: center

Si es un error en el diseño del formulario el error es del tipo:

.. figure:: /media/build_upload_error2.jpg
   :align: center

.. admonition:: Presta atención

	En caso de que haya algún error de diseño, consulta el último apartado de esta sección: :guilabel:`Validar un Formulario`.

Desde Aggregate
^^^^^^^^^^^^^^^

Se necesita tener el formulario en blanco en el formato XML.

Para obtener el formulario en este formato, hay que ir al menú :guilabel:`File` de Build y hacer clic en :guilabel:`Export to XML`.
Esto permite descargar el formulario en formato XML al ordenador (generalmente a la carpeta :guilabel:`Descargas` o :guilabel:`Downloads`).

Google Drive
^^^^^^^^^^^^

También es posible utilizar Google Drive para alojar las diferentes respuestas al formulario en una hoja de cálculo, en formato Sheets de Google.
Este procedimiento, que comienza una vez exportamos el formulario a Excel, será descrito en el siguiente apartado.

.. admonition:: Práctica

	Observa la siguiente tabla y crea el formulario usando Build.
	
.. list-table::
   :header-rows: 1
   :widths: auto

   * - Tipo de Dato
     - Nombre del dato
     - Texto del título
     - Consejo
     - Requerido
     - Rango mín-máx
     - Opciones
   * - Texto
     - nombre
     - Nombre del entrevistado
     - Nombre y apellido
     - Sí
     - 
     - 
   * - Número
     - edad
     - Edad del entrevistado
     - 
     - 
     - 18 - 99
     - 
   * - Fecha
     - fecha
     - ¿Qué día es hoy?
     - 
     - 
     - 
     - 
   * - GPS
     - gps
     - Registra tus coordenadas GPS
     - 
     - 
     - 
     - 
   * - Multimedia
     - foto
     - Foto del entrevistado
     - Toma la foto en formato horizontal
     -
     -
     -
   * - Selección única
     - genero
     - Género del entrevistado
     - 
     - Sí
     - Masculino, femenino
     - 
   * - Selección múltiple
     - necesidades
     - Necesidades urgentes
     - Selecciona todas las que apliquen
     - 
     - 
     - Agua, comida, albergue
	
Grupos de preguntas
-------------------

En Build se pueden agrupar preguntas.
Esto significa que se pueden asociar preguntas bajo un mismo nombre.
Por ejemplo se puede crear un grupo que se llame :guilabel:`Datos Personales` y englobar ahí todas las preguntas que sean sobre los datos personales que se recogen de un/una beneficiario/a.
Además, las preguntas de un grupo, se pueden mostrar en una misma pantalla.
Para ello, en Build, hay que pulsar en :guilabel:`Group` en el panel de Tipo de datos:

.. figure:: /media/build_question_groups0.JPG
   :align: center

Aparece la siguiente pantalla y al igual que para las preguntas, hay que dar un nombre al grupo (1) (si no se pone, no aparece en el formulario y no podemos saber a qué hacen referencia esas preguntas), y un nombre para la base de datos (1).
Además, si se quiere que las preguntas aparezcan en la misma pantalla hay que hacer clic en la casilla :guilabel:`Display On One Screen` (2).
Si se quiere que el grupo de preguntas se repita tantas veces como se desee hay que hacer clic en :guilabel:`Looped` (2), aunque no se recomienda porque se crean Excels adicionales y su análisis es más complejo.

.. figure:: /media/build_question_groups1.JPG
   :align: center
  
A continuación, se arrastran las preguntas que se quieran dentro del recuadro verde para incluirlas preguntas dentro del grupo (1) y se hace clic en :guilabel:`Display On One Screen` (2):

.. figure:: /media/build_question_groups2.JPG
   :align: center

.. figure:: /media/build_question_groups3.JPG
   :align: center

Así es como se ve el grupo en ODK Collect (1) y lo que se obtiene en Aggregate (2):

.. figure:: /media/build_question_groups4.jpg
   :align: center

Como se puede ver en la imagen de Aggregate anterior, el nombre de las columnas de las preguntas que estén dentro de un grupo seguirán la siguiente estructura: 

:guilabel:`Nombre_del_grupo:nombre_pregunta`.

Como puede verse en la imagen inferior, en Google Drive se antepone, además, el nombre del formulario, cada elemento separado por un guión:

.. figure:: /media/build_question_groups5.jpg
   :align: center

.. admonition:: Práctica

	Modifica el formulario para que las preguntas se puedan ver en una única pantalla.
	En el siguiente apartado usaremos Google Drive para alojar el formulario en blanco y las respuestas.
 
Validar un formulario
---------------------

Generalmente, si un formulario contiene errores es por alguna de las siguientes razones:

- Hay espacios o caracteres especiales en el :guilabel:`Name` o :guilabel:`Data Name` de preguntas o grupos.
- No se ha añadido el :guilabel:`Caption Text` o el texto de alguna pregunta.
- No se han incluido por cada una de las opciones que se introduzcan todos los campos: :guilabel:`Underlying Value` y las opciones en los idiomas que se hayan seleccionado.

En caso de no tratarse de ninguna de estas opciones, se puede utilizar el programa ODK Validate para comprobar errores.
Para ello necesitamos:

- En Build, descarga el formulario en formato XML siguiendo las indicaciones que se han dado anteriormente.
- Asegúrate de tener Java actualizado en tu PC. Accede a https://java.com/es/download/ie_manual.jsp para verificar tu instalación.
- Descarga el programa Validate: https://github.com/opendatakit/validate/releases/latest

.. figure:: /media/build_validate_download.jpg
   :align: center
   
- Abre el programa :guilabel:`Validate` haciendo doble clic sobre el fichero .jar descargado. Haz clic en :guilabel:`Choose File…`.

.. figure:: /media/build_validate_choosefile.jpg
   :align: center

- A continuación selecciona el formulario en formato XML que nos hemos descargado previamente y se hace clic en :guilabel:`Abrir`:

.. figure:: /media/build_validate_open.jpg
   :align: center

La siguiente pantalla mostrará errores si los hubiese o nos dirá que el formulario es válido: 

.. figure:: /media/build_validate_results.jpg
   :align: center

Resumen y próximo pasos
^^^^^^^^^^^^^^^^^^^^^^^

En este apartado se ha explicado cómo hacer uso de Build para la creación y exportación de formularios ODK así como el procedimiento para exportarlos y subirlos al servidor.
También hemos visto cómo validar los formularios utilizando otra aplicación.
En los siguientes apartados se abordarán las diferentes modalidades de servidor y la forma en que podemos explotar la información.
