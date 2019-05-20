Build
=====

.. admonition:: Conocimientos previos

	Para la comprensión de este apartado es necesario conocer de forma básica qué es Open Data Kit y cómo funciona la aplicación Collect, tanto a nivel de configuración como de gestión y cumplimentación de formularios. 
	Asimismo es necesario tener conocimientos básicos sobre la navegación y funcionamiento de aplicaciones web.  

¿Qué es ODK Build?
------------------

Build es una herramienta que permite la creación de formularios de Open Data Kit.  Mediante un sencillo interface pueden diseñarse las diferentes preguntas y posibles respuestas así como añadir diferentes tipos de material audiovisual. 

Originalmente estaba disponible como una herramienta en línea accesible a través de la url: http://build.opendatakit.org/ con las ventajas de su accesibilidad y disponibilidad de la información en cualquier lugar del mundo. Más recientemente se ha creado una versión offline descargable desde el mismo sitio web, que permite superar las limitaciones derivadas de la dificultad de acceso a Internet en determinados lugares y circunstancias.

El objetivo de este apartado es familiarizarnos con sus funciones y características principales de forma que podamos generar nuestro primer formulario.

.. admonition:: Recuerda

	Aunque Build presenta limitaciones en el diseño de los formularios respecto a Excel, es una herramienta muy efectiva para el diseño de formularios sencillos y, sobre todo, para todas las personas que se estén iniciando en el mundo de ODK. 

.. admonition:: Recuerda

	Además de Build y Collect, la otra gran pieza de ODK es el servidor al que conectaremos para descargar los formularios en blanco y almacenar los ya completados. Ese servidor puede ser de tipo Aggregate o de tipo Google Drive.

Tipos de datos
--------------

Antes de empezar a entender cómo funciona la herramienta, necesitamos entender los tipos de datos que vamos a poder elegir en los formularios.

¿Qué quiere decir esto?

En un formulario o encuesta, vamos a realizar una serie de preguntas. Cada una de estas preguntas tendrá diferentes tipos de respuesta, es decir, a una determinada pregunta y según cómo esté descrita, la persona que grabe las respuestas tendrá que hacerlo con un texto, con un número, con una fecha, una fotografía, etc. El formato en el que queremos que nos respondan, es el tipo de dato.

A continuación se muestra una tabla con los tipos de datos que nos vamos a encontrar, su descripción, y un ejemplo de pregunta cuya respuesta sería ese tipo de dato.

.. tabularcolumns:: |>{\centering\arraybackslash}\X{1}{3}|>{\centering\arraybackslash}\X{2}{3}|>{\centering\arraybackslash}\X{3}{3}|

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
     - Se introduce una fecha y/u hora en un formato de calendario y/o reloj. Se puede elegir que la respuesta sea una fecha completa, año, año y mes y fecha completa y hora
     - ¿En qué año naciste?
   * - Time
     - Se introduce una hora en formato de reloj digital
     - ¿A qué hora es la distribución?
   * - Location
     - Se graban unas coordenadas geográficas. La respuesta puede ser un punto, una serie de puntos o una forma. Se puede recoger con el GPS por defecto, señalándolo en el mapa o de forma manual
     - Registra tu posición actual
   * - Media
     - Se puede hacer o elegir una fotografía, un audio o un video
     - Haz una foto de la instalación
   * - Barcode
     - Se escanea un código de barras o código QR. Es necesario tener un programa instalado en el dispositivo para este propósito
     - Escanea el código de barras de la tarjeta del beneficiario
   * - Choose One
     - Se puede elegir una opción de las posibilidades que nos den
     - Selecciona el género del o de la beneficiario/a: masculino, femenino, desconocido
   * - Select Multiple
     - Se puede elegir una o varias opciones de las posibilidades que nos den
     - Selecciona las necesidades más urgentes: agua, comida, refugio, dinero
   * - Metadata
     - Este tipo de dato no tiene una pregunta en el formulario, si no que se graba por defecto
     - ID del dispositivo, hora de comienzo y/o final de la encuesta, fecha, nombre de usuario, ID del suscriptor, número de serie de la SIM, número de teléfono

.. admonition:: Práctica

	Piensa con detenimiento a qué tipo de dato corresponderían las respuestas a las siguientes preguntas:
	- La fecha de nacimiento.
	- La foto de la persona beneficiaria
	- Indica que días de la semana trabajas: L, M, MX, J, V, S, D
	- ¿Has recibido ayuda de Cruz Roja Española anteriormente?: Si, No
	- Indica tu altura. 
	- Indica el número de voluntarios/as que han participado en la actividad.
	- Indica tu nivel de satisfacción con las jornadas: Muysatisfecho/a, Satisfecho/a, Poco Satisfecho/a, Nada Satisfecho/a
	- ¿En qué localidad se está llevando a cabo esta encuesta?
	- ¿De qué provincia procedes? Segovia, Toledo, Madrid, Ávila, Otros
	- ¿Cuántos miembros tiene la familia? 

Crear una cuenta en Build
-------------------------

A continuación se va a ver cómo crear una cuenta en Build. Para ello se requiere tener una conexión a Internet.

Internet Explorer limita algunas funcionalidades, por esta razón se recomienda utilizar uno de los siguientes navegadores de Internet:
    • Google Chrome (https://www.google.es/chrome/browser/desktop/) 
    • Firefox (https://www.mozilla.org/es-ES/firefox/new/) 

En el navegador vamos a la siguiente página: http://build.opendatakit.org/

Al entrar, nos sale la siguiente pantalla: si estamos registrados podemos introducir el usuario y la contraseña, pero la primera vez tendremos que hacer clic en “Dont’t yet have an account?”:

.. figure:: /media/build1.jpg
   :align: center

Entonces habrá que proceder a rellenar los siguientes datos:

.. figure:: /media/build1.jpg
   :align: center

Una vez finalizado, se hace clic en “Sign up”. Y la cuenta ya está creada.

Panel principal
---------------

Este es el panel con el que nos encontramos al entrar en Build:

.. figure:: /media/build1.jpg
   :align: center

Nombre del formulario: permite renombrar un formulario. Si no se le da un nombre se guardará por defecto como “Untitled Form” y finalmente te puedes encontrar con varios con el mismo nombre. Para ello, hay que hacer clic en “rename” y una vez escrito el nuevo nombre, hacer clic en “done”:

.. figure:: /media/build1.jpg
   :align: center

Menús de Build: proporciona varios menús donde poder gestionar el formulario:
- File: tiene los siguientes submenús:
	- New Form: crear un nuevo formulario.
    - Open Form: da la opción de abrir un formulario guardado previamente dentro de la lista de formularios guardados.
    - Save: guardar un formulario, es recomendable haberlo nombrado con anterioridad. Si no, te lo guarda sobre el formulario que estés. Por otro lado, es recomendable ir pulsando “Save” cuando se está haciendo un formulario nombrado previamente para no perder los cambios.
    - Save Form As: permite guardar un formulario con el nombre que se desee.
    - Save Form to File: permite descargarte el formulario en formato “.odkbuild”. Este archivo te permite poder enviarlo y abrirlo desde otra cuenta Build. Los documentos que se descargan al ordenador desde Build suelen guardarse en la carpeta “Descargas” o “Downloads”.
    - Load Form from File: permite abrir en Build un archivo “.odkbuild”. Para ello tendrás que hacer clic en “Choose” y elegir el archivo en la ubicación donde se encuentre, y hacer clic en “Load”. Recuerda haber guardado el formulario anterior si estuvieses trabajando en uno; Build no guarda los cambios automáticamente:

.. figure:: /media/build1.jpg
   :align: center

    - Upload Form to Aggregate: permite exportar el formulario en blanco que se ha creado, directamente a Aggregate. Se verá en el apartado “Exportar un formulario”.
    - Export to XML: permite descargar el formulario en formato “.XML”.
    - Export to XLSForm: permite descargar el formulario en formato Excel, que posibilita hacer formularios más complejos y versátiles con más funcionalidades.

.. admonition:: Recuerda

	Build no guarda los cambios automáticamente. Es importante guardar los formularios que se vayan creando así como las modificaciones que se les haga. Sobre todo antes de abrir nuevos formularios o de cerrar la sesión. No obstante, Build suele dar algunos mensajes para avisar:
	.. figure:: /media/build1.jpg
		:align: center

- Edit: principalmente tiene el menú de “Manage Translations” que te permite añadir nuevos idiomas, es decir, que puedas crear el formulario en varios idiomas. Cuando haces clic sobre esa opción, aparece la siguiente ventana. En el desplegable que dice “Add a new language”, se elige el idioma que quieres añadir:

.. figure:: /media/build1.jpg
   :align: center

Una vez elegido se hace clic en “Add Translation”:

.. figure:: /media/build1.jpg
   :align: center

Se pueden añadir tantos idiomas como se desee, así como eliminar el que no se quiera, haciendo clic en “remove”. Cuando se ha finalizado se hace clic en “Done”.

- View: en la primera parte, permite elegir en qué idioma se quieren ver las preguntas del formulario que se está haciendo, en caso de tener más de uno. La opción de “Collapse Controls” permite cambiar la visualización de las preguntas en Build (ver más o menos información en el Área Principal). 
- Help: proporciona información sobre Build y enlaces para descargarse el código y reportar fallos que se encuentren en la herramienta. 

Área Principal: es donde van a aparecer todas las preguntas que se vayan configurando en el formulario.

Tipos de Datos: cada vez que se quiera añadir una pregunta al formulario, hay que hacer clic en el tipo de dato que queremos obtener. 

Área de propiedades: al añadir una pregunta o un tipo de dato, en el área de propiedades aparecerán una serie de elementos para configurar las preguntas. 

Cómo crear un formulario
------------------------

Añadir preguntas a un formulario
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Para añadir preguntas a un formulario, únicamente hay que hacer clic sobre el tipo de dato que deseamos tener como respuesta de la pregunta que vamos a formular y configurar.

Ejemplo, al hacer clic en “Text”, aparece la pregunta en el rectángulo del Área Principal y, a la derecha en vertical, el Área de Propiedades para esa pregunta: 

.. figure:: /media/build1.jpg
   :align: center

Configuración de propiedades
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A continuación vamos a ver cómo se configuran y cuáles son las propiedades de las preguntas:

.. figure:: /media/build1.jpg
   :align: center

- Nombre del dato o variable: es el nombre que se guarda como referencia en la base de datos (BD). No puede tener espacios ni caracteres especiales. Será el nombre de la columna en la BD. Ej. nombre_del_entrevistado. Campo obligatorio.
- Texto del título: se define la pregunta que se quiere hacer y que se mostrará al usuario en el dispositivo móvil. Si se realiza el formulario en varios idiomas, habrá que incluir la pregunta o el texto en dichos idiomas en sus respectivos campos. Ej. Escriba el nombre del entrevistado. Campo obligatorio.
- Pista: ayuda adicional o aclaración para entender la pregunta que se muestra al usuario en el dispositivo móvil. Ej. Nombre y apellido. Campo recomendado.
- Valor por defecto: este texto será la respuesta por defecto a menos que el usuario la modifique. Ej. Juan Valdez. Rara vez utilizado.
- Solo lectura: el usuario no puede introducir datos, sólo leer lo que dice el texto o pregunta. Rara vez utilizado.
- Requerido: si se marca esta casilla, el usuario no puede pasar a la siguiente pregunta a menos que la pregunta actual sea respondida. Opcional.
- Longitud: el usuario no puede pasar a la siguiente pregunta a menos que la respuesta de la pregunta actual tenga una cantidad específica de caracteres:
	- Mínimo. La cantidad mínima de caracteres requerida.
	- Máximo. La cantidad máxima de caracteres aceptada.
	Ej. Mínimo 5, Máximo 10: la respuesta debe tener entre 6 y 9 caracteres. Si se seleccionan las opciones “incluyente” la respuesta debe tener entre 5 y 10 caracteres. Opcional.
- Texto inválido: mensaje que se muestra si no se cumple la longitud establecida anteriormente. A veces esta opción no funciona adecuadamente.

A continuación se muestra un ejemplo de cómo se muestra una pregunta, en ODK Collect y en el servidor (Aggregate o Google Drive), según la configuración en Build:

.. figure:: /media/build1.jpg
   :align: center

Según los tipos de preguntas, hay algunas particularidades:

- Con algunos tipos de preguntas aparecerá una nueva propiedad, “Kind”, esto mostrará subtipos de formato en los que se pide introducir esa respuesta en el formulario en ODK Collect; se elige según conveniencia. En caso de no seleccionar ninguno aparecerá el que esté seleccionado por defecto:

.. tabularcolumns:: |p{1cm}|p{7cm}|

.. csv-table:: Propiedad kind
   :file: /media/tipokind.csv
   :header-rows: 1
   :class: longtable
   :widths: 1 1

- En otras preguntas aparece una opción que es “Style”:

.. tabularcolumns:: |p{1cm}|p{7cm}|

.. csv-table:: Propiedad Style
   :file: /media/tipostyle.csv
   :header-rows: 1
   :class: longtable
   :widths: 1 1
 
- En el caso de “Choose One” o “Select Multiple” hay que añadir las opciones, y para ello hay dos formas posibles en el Área de Propiedades:

	- Haciendo clic en “Add Option” en el Área de Propiedades para configurar cada una de las opciones que quieras añadir.

.. figure:: /media/build1.jpg
   :align: center

	- Haciendo clic en “bulk edit” en el Área de Propiedades y rellenar en cada línea las dos columnas para cada una de las opciones que se quiera añadir.

.. figure:: /media/build1.jpg
   :align: center

Para ambos casos:

- En el o los idiomas que se hayan elegido; “English” y/o “Spanish”, etc., se pone el texto de la opción como se quiere que aparezca en el formulario al leer la pregunta.
- El campo “Underlying Value” hace referencia a cómo queremos que se guarde esa opción en la base de datos de Aggregate. El texto que se introduzca no puede tener ni espacios ni caracteres especiales. 

.. admonition:: Presta atención

	Es muy importante rellenar todos los campos que se generan según el número de opciones e idiomas que se añadan, incluido el “Underlying Value”. Si hay algún error o falta algún campo, se pondrá la pregunta en rojo indicando que hay un error. El texto que se introduzca en “Underlying Value” no puede tener ni espacios ni caracteres especiales, sí se pueden utilizar guiones bajos en lugar de espacios.

A continuación se muestra un ejemplo:

.. figure:: /media/build1.jpg
   :align: center

En caso de haber hecho clic en “bulk edit” se vería la siguiente pantalla con los datos incluidos:

.. figure:: /media/build1.jpg
   :align: center

A continuación podemos ver cómo queda reflejado en ODK Collect, Aggregate y Google Sheets.

.. figure:: /media/build1.jpg
   :align: center

Exportar un formulario
----------------------

Una vez que tenemos el formulario finalizado, hay varias formas para exportar el formulario o subirlo al servidor:

Desde Build 
^^^^^^^^^^^

Permite exportar el formulario en blanco que se ha creado, directamente al servidor Aggregate. Para ello, hay que introducir la dirección o URL del servidor, el usuario y la contraseña correspondiente y pulsar “Export”:

.. figure:: /media/build1.jpg
   :align: center

En caso de ser correcta la subida al servidor, aparece la siguiente pantalla o aviso en la parte inferior derecha de la pantalla:

.. figure:: /media/build1.jpg
   :align: center

En caso de haber algún error en el formulario, aparece el siguiente aviso:

.. figure:: /media/build1.jpg
   :align: center

.. admonition:: Presta atención

	En caso de que haya algún error, ver el último apartado de este documento: “Validar un Formulario”.

Desde Aggregate
^^^^^^^^^^^^^^^

Se necesita tener el formulario en blanco en el formato “.XML”.

Para obtener el formulario en este formato, hay que ir al menú “File” de Build y hacer clic en “Export to XML”. Esto permite descargar el formulario en formato “.XML” al ordenador (generalmente a la carpeta “Descargas” o “Downloads”).

Google Drive
^^^^^^^^^^^^

También es posible utilizar Google Drive para alojar las diferentes respuestas al formulario en una hoja de cálculo, en formato  Sheets de Google. Este procedimiento, que comienza una vez exportamos el formulario a Excel, será descrito en el siguiente apartado.

.. admonition:: Práctica

	Observa la siguiente tabla y crea el formulario usando Build.

	.. tabularcolumns:: |p{1cm}|p{7cm}|

	.. csv-table:: Preguntas
		:file: /media/practicaform.csv
		:header-rows: 1
		:class: longtable
		:widths: 1 1

Grupos de preguntas
-------------------

En Build se pueden agrupar preguntas. Esto significa que se pueden asociar preguntas bajo un mismo nombre. Por ejemplo se puede crear un grupo que se llame “Datos Personales” y englobar ahí todas las preguntas que sean sobre los datos personales que se recogen de un/una beneficiario/a. Además, las preguntas de un grupo, se pueden mostrar en una misma pantalla. Para ello, en Build, hay que pulsar en el panel de Tipo de datos en “Group”:

.. figure:: /media/build1.jpg
   :align: center

Aparece la siguiente pantalla y al igual que para las preguntas, hay que dar un nombre al grupo, si no se pone, no aparece en el formulario y podemos no saber a qué hacen referencia esas preguntas, y un nombre para la base de datos, además si se quiere que las preguntas aparezcan en la misma pantalla hay que hacer clic en la casilla “Display On One Screen”. Si se quiere que el grupo de preguntas se repita tantas veces como se desee hay que hacer clic en “Looped”, aunque no se recomienda porque se crean Excels adicionales y su análisis es más complejo.

.. figure:: /media/build1.jpg
   :align: center
  
A continuación, se arrastran las preguntas que se quieran dentro del recuadro verde para incluirlas preguntas dentro del grupo y se hace clic en “Display On One Screen”:

.. figure:: /media/build1.jpg
   :align: center

.. figure:: /media/build1.jpg
   :align: center

Así es como se ve en ODK Collect y lo que se obtiene en Aggregate y Google Drive:

.. figure:: /media/build1.jpg
   :align: center

Como se puede ver en la imagen de Aggregate anterior, en la base de datos, el nombre de las columnas de las preguntas que estén dentro de un grupo, seguirán la siguiente estructura: “Nombre_del_grupo:nombre_pregunta”. En Google Drive se antepone, además, el nombre del formulario, cada elemento separado por un guión:

.. figure:: /media/build1.jpg
   :align: center

.. admonition:: Práctica

	Modifica el formulario para que las preguntas se puedan ver en una única pantalla. 
	En el siguiente apartado usaremos Google Drive para alojar el formulario en blanco y las respuestas.
 
Validar un formulario
---------------------

Generalmente, si un formulario contiene errores es por alguna de las siguientes razones:

- Hay espacios o caracteres especiales en el “Name” o “Data Name” de preguntas o grupos. 
- No se ha añadido el “Caption Text” o el texto de alguna pregunta.
- No se han incluido por cada una de las opciones que se introduzcan todos los campos: “Underlying Value” y las opciones en los idiomas que se hayan seleccionado.

En caso de no tratarse de ninguna de estas opciones, se puede utilizar el programa Validate para comprobar errores. Para ello necesitamos:

- Descargar el programa Validate: https://opendatakit.org/downloads/download-info/odk-validate-2/
- Tener Java actualizado y eliminar las versiones anteriores, si se tuvieran: https://java.com/es/download/ie_manual.jsp
- Descargar el formulario en XML.

Se abre el programa y se hace clic en “Choose File…”:

A continuación se selecciona el formulario en formato XML que nos hemos descargado previamente y se hace clic en “Open”:

.. figure:: /media/build1.jpg
   :align: center

La siguiente pantalla mostrará errores si los hubiese o nos dirá que el formulario es válido: 

.. figure:: /media/build1.jpg
   :align: center

.. admonition:: Resumen y próximo pasos

	En este apartado hemos explicado cómo hacer uso de Build para la creación y exportación de formularios ODK así como el procedimiento para exportarlos y subirlos al servidor. También hemos visto como validar los formularios utilizando otra aplicación. En los siguientes apartados se abordarán las diferentes modalidades de servidor y la forma en que podemos explotar la información.
