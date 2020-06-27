.. |BUILD| image:: /media/build.png
   :width: 50 px
.. |COLLECT| image:: /media/collect.png
   :width: 50 px
.. |AGGREGATE| image:: /media/aggregate.png
   :width: 50 px

.. _introduccion-label:

Introducción
============

.. admonition:: Conocimientos previos
   
   Este apartado requiere un conocimiento a nivel de usuario/a del sistema operativo Android, el más extendido para *smartphones* y tabletas, así como familiarizarse con el uso de navegadores de Internet.

¿Qué es Open Data Kit?
----------------------
   
La recolección de datos sobre el terreno es una tarea fundamental dentro de la acción humanitaria ya sea cuando se interviene en una emergencia o en un proyecto de desarrollo.

Tradicionalmente este trabajo se ha realizado rellenando a mano las encuestas y tabulándolas posteriormente.
Esta técnica es poco eficiente y son numerosas las posibles fuentes de error desde el momento de recoger la información hasta la publicación de los resultados.

Open Data Kit (ODK) es un conjunto de herramientas informáticas de **código abierto** que permiten sistematizar algunas de las tareas que intervienen en todo este proceso facilitando la creación e implementación de las encuestas a través de dispositivos móviles y el procesamiento de las mismas, sustituyendo el uso del papel, ahorrándonos horas de transcripción y, lo más importante, disminuyendo en buena medida posibles errores.
Todo esto contribuye a obtener la información necesaria en un tiempo menor y dar una respuesta más rápida y eficaz.

ODK comenzó como un proyecto de Google.org, en abril de 2008 y los desarrolladores principales son investigadores del Departamento de Ciencias Computacionales e Ingeniería de la **Universidad de Washington**.
En la actualidad está apoyada en una extensa comunidad distribuida en multitud de países que contribuye al crecimiento y mejora de esta herramienta.
`Open Data Kit <https://opendatakit.org/>`__ y el `Foro ODK <https://forum.getodk.org/>`__ permiten estar al tanto de todas las novedades y poder interactuar con la comunidad.
También están presentes en las redes sociales `Facebook <https://www.facebook.com/opendatakit>`__ y `Twitter <https://twitter.com/opendatakit>`__.

ODK nos permitirá hacer muchos tipos de formularios aplicados a diferentes áreas:

- Registro de actividades, beneficiarios/as, pacientes, vehículos, puntos de agua, letrinas, préstamo de material, etc.
- Encuestas de evaluación y de satisfacción, etc.
- Evaluaciones en terreno, líneas de base, etc.

Estos formularios pueden recoger también imágenes, audios, vídeos, geolocalización, etc., facilitando la evaluación y la visibilidad de las operaciones con un único dispositivo.

ODK y ODK-X
-----------

Una importante evolución de ODK ha dado lugar al denominado ODK-X.
Mientras que ODK se considera una herramienta robusta y simple para la realización de encuestas sencillas, compatible con otras herramientas muy utilizadas (Ona, Enketo, Kobo, ELMO) y con una amplia comunidad de usuarios/as; ODK-X es una herramienta concebida para **flujos de trabajo complejos** permitiendo saltar de un punto a otro de la encuesta, la sincronización de información con el servidor en ambas direcciones y, en definitiva, la **gestión de la información desde el propio dispositivo**.

Dada la larga trayectoria de las herramientas ODK y su gran rendimiento en la mayoría de los trabajos de recolección de información, esta web se centrará en la explicación de estas herramientas de uso más general.
En cualquier caso, Cruz Roja está explorando las capacidades de ODK-X y sus necesidades de infraestructura tecnológica para poder emplear también en el futuro las herramientas de ODK-X.

.. admonition:: Más información 

   Si quieres más información sobre ODK-X y explorar sus posibilidades puedes encontrarla en su apartado correspondiente en la web oficial de Open Data Kit: `ODK-X <https://docs.odk-x.org/>`__

Herramientas más utilizadas
---------------------------

Las herramientas ODK más utilizadas son:

* |BUILD| Build: para **crear un formulario** de recopilación de datos o una encuesta.
* |COLLECT| Collect: permite **registrar** datos en un dispositivo móvil y **enviarlos** a un servidor.
* |AGGREGATE| Aggregate: funciona como un **concentrador** de los datos recogidos y permite extraerlos y difundirlos en formatos útiles.

.. admonition:: ¿Sabías que? 

   Google Drive, el espacio de almacenamiento de Google en la nube, puede ser utilizado también como “servidor”, para obtener los formularios y recopilar la información. Es una opción más sencilla de implementar que Aggregate.

Comunicación entre herramientas
-------------------------------

Mientras que Build se comunica de forma **unidireccional** con Aggregate para enviarle los formularios en blanco, en cambio, la comunicación entre Collect y Aggregate es **bidireccional**: Collect obtiene los formularios en blanco del servidor y los envía una vez se hayan rellenado.

.. figure:: /media/comunicacion.jpg
   :align: center

Instalación de ODK Collect
--------------------------

A continuación vamos a realizar paso a paso la instalación de la aplicación ODK Collect en nuestro *smartphone*.

Una vez en nuestro dispositivo vamos a **“Play Store”** donde se pueden buscar e instalar las aplicaciones para nuestro dispositivo.

.. figure:: /media/googleplay.jpg
   :align: center

.. admonition:: Debes conocer

   Es necesario disponer de una cuenta de Gmail y configurarla adecuadamente para instalar cualquier aplicación de la Play Store.

Utilizando el cuadro superior de búsqueda, escribimos el nombre de la aplicación a instalar: ODK Collect.
Observaremos que según escribimos el nombre nos va sugiriendo resultados entre los que se encuentra el nombre de nuestra aplicación.
Una vez localizada la aplicación, le damos a “instalar”.

.. figure:: /media/googleplay_collect.jpg
   :align: center

.. admonition:: Recomendación 

   Cuando instales aplicaciones en tu dispositivo móvil conéctate a una red wifi para evitar un consumo innecesario de nuestra tarifa de datos.

Durante el proceso de instalación debemos aceptar que la aplicación acceda a determinados contenidos y herramientas de nuestro teléfono.
Finalmente nos ofrecerá la posibilidad de abrir la aplicación una vez está disponible en nuestro dispositivo.

.. figure:: /media/googleplay_collect2.jpg
   :align: center

Configuración de ODK Collect
----------------------------

A continuación, utilizando el acceso creado en nuestra pantalla, entramos en la aplicación Collect y vemos su pantalla principal.
Lo primero que vamos a hacer es comprobar la configuración de la aplicación.
Pulsa sobre el botón superior derecho (1) y selecciona “Cambiar la configuración” (2).
A continuación selecciona “Servidor - Usuario” (3).

.. figure:: /media/collect_conf.jpg
   :align: center

Inicialmente Collect está configurado para el acceso a un **servidor de prueba** de tipo “ODK Aggregate” cuya dirección URL es https://opendatakit.appspot.com y al que es posible el acceso de forma anónima, es decir, no hace falta ni usuario ni contraseña.
Deja la configuración tal como está y pulsa el botón “atrás” de tu *smartphone* hasta volver a la pantalla inicial de la aplicación.

.. figure:: /media/collect_default_conf.jpg
   :align: center

Obtención de un formulario en blanco
------------------------------------

Ahora estamos en disposición de descargar un formulario en blanco de entre aquellos que están en el servidor de pruebas.
En la pantalla principal pulsa en “obtener formulario en blanco” (1).

La aplicación valida en este momento que el servidor, usuario y contraseña introducidos anteriormente son correctos y ofrece una lista de los formularios disponibles.
Selecciona “All widgets” (2) y pulsa en “obtener los seleccionados” (3).

Se trata de un formulario demostrativo de los diferentes tipos de preguntas disponibles en ODK.
Aunque se encuentra en inglés nos puede dar una primera idea del tipo de información que se puede recopilar y de la potencialidad de esta herramienta.

Una vez descargado el formulario debes pulsar “De acuerdo” (4).

.. figure:: /media/collect_blank_form.jpg
   :align: center
   
Introducción de información en un formulario
--------------------------------------------

Volvemos a la pantalla principal y entramos en “Llenar Nuevo Formulario” (1). Seleccionamos el que nos acabamos de descargar (2) y entramos a las diferentes preguntas del mismo.

.. figure:: /media/collect_added_form.jpg
   :align: center

En esta primera pantalla no hay que rellenar nada, simplemente es de carácter **informativo** sobre el objetivo del formulario.
Observa que se ofrece un primer bloque (1) en negrita a modo de titular y un segundo bloque (2) mucho más extenso en cursiva.
Desliza la pantalla hacia arriba para ver la información que está oculta abajo por no caber en la pantalla.
Finalmente, desliza la pantalla hacia la izquierda para pasar al siguiente elemento del formulario.

.. figure:: /media/collect_note.jpg
   :align: center

El formulario nos ofrece ahora un elemento de tipo **texto**.
Se trata de una pregunta titulada :guilabel:`String widget` a rellenar con una palabra o conjunto de palabras en el espacio en blanco (1) usando para ello el teclado que se nos despliega en la parte inferior (2).
Escribe cualquier cosa y desliza la pantalla hacia la izquierda para pasar a la siguiente pregunta.
 
.. figure:: /media/collect_add_text.jpg
   :align: center

En la siguiente pantalla encontramos otra pregunta de tipo texto, aunque con aspecto numérico.
ODK permite jugar con diferentes apariencias para introducir la información.
Observa que bajo el enunciado de la pregunta que aparece en negrita :guilabel:`String number widget` (1) aparece en cursiva un pequeño texto aclaratorio sobre la pregunta (2).
Este es un recurso de ODK para facilitar el desarrollo y la comprensión de la encuesta.
Utilizando el teclado, introduce cualquier número.

.. figure:: /media/collect_add_number_options.jpg
   :align: center

.. admonition:: Presta atención

   Ya has comprobado que para **pasar de una pregunta a otra** basta con deslizar la pantalla hacia la izquierda. Comprueba que también es posible **retroceder a una pregunta anterior** deslizando la pantalla hacia la derecha.

A continuación, progresa a lo largo del formulario pasando diferentes preguntas hasta llegar a la relativa a :guilabel:`Ex printer widget`.
Habrás observado que ésta y las preguntas anteriores tenían un encabezado común denominado :guilabel:`Text widgets`.
Esto significa que las preguntas están integradas en un **grupo** lo que permite darles un tratamiento homogéneo dentro del formulario.

.. figure:: /media/collect_group.jpg
   :align: center

Pasa a la siguiente pregunta denominada :guilabel:`Integer widget` y que forma parte del grupo :guilabel:`Numerical widgets`.
En esta pregunta se nos pide introducir una respuesta de tipo **numérico**.
Introduce cualquier número y desliza la pantalla hacia la izquierda.

.. figure:: /media/collect_add_number.jpg
   :align: center

Observa las sucesivas preguntas situadas en el grupo :guilabel:`Numerical widgets` e interactúa con algunas de ellas, observando cómo reflejan la información introducida con el teclado.

El siguiente grupo de preguntas es el denominado :guilabel:`Range widgets` que permiten elegir determinados valores dentro de los **rangos** sugeridos.
Observa el ejemplo para :guilabel:`Range integer widget` y cómo puedes seleccionar el valor entero que desees en el rango situado entre 1 y 10.
Revisa los ejemplos posteriores hasta llegar al siguiente grupo.

.. figure:: /media/collect_add_range.jpg
   :align: center

El grupo :guilabel:`Image widgets` recoge ejemplos de preguntas relacionadas con la introducción de información de tipo **imagen** como pueden ser una foto, un dibujo o incluso una firma.
A continuación se recoge el ejemplo relativo al :guilabel:`Image widget` en la que puede registrarse la fotografía, tanto usando la cámara del teléfono como escogiéndola de la memoria de nuestro dispositivo.

.. figure:: /media/collect_photo.jpg
   :align: center

El siguiente grupo se llama :guilabel:`Media widgets` y permite integrar en la encuesta otras informaciones tipo **multimedia** como pueden ser códigos de barras, sonidos o vídeos, utilizando para ello elementos de nuestro dispositivo como la cámara de fotos, la grabadora de vídeo y la de sonido, o añadiendo ficheros ya disponibles en la memoria del *smartphone*.
Haz una prueba y graba un pequeño vídeo o audio y continúa hasta el siguiente grupo de preguntas.

El grupo :guilabel:`Date and time widgets` contiene elementos que nos permiten registrar información de tipo **fecha y hora** en diferentes formatos y calendarios según nuestras necesidades.
En el siguiente ejemplo se muestra el registro en una misma pantalla de la fecha y hora.

.. figure:: /media/collect_date_time.jpg
   :align: center

El siguiente grupo es el denominado :guilabel:`GPS widget` que nos permite registrar **coordenadas** utilizando el GPS de nuestro dispositivo y localizar el punto exacto de las observaciones, el camino que hayamos seguido o delimitar un área determinada.
A modo de ejemplo, en la pregunta :guilabel:`Geopoint widget` pulsa en :guilabel:`Buscar ubicación` (1).
Espera a que el GPS determine nuestra posición sobre el mapa.
También es posible seleccionar nuestra posición de forma manual marcando un punto sobre el mapa (2).
Una vez realizado le damos a la opción guardar (3) y veremos nuestras coordenadas geográficas en el formulario (4).

.. figure:: /media/collect_gps.jpg
   :align: center

.. admonition:: Debes conocer

   Para disponer de cobertura GPS es necesario estar en un lugar abierto: si estamos en campo abierto, en áreas de vegetación no muy densa. Para áreas urbanas, cerca de las ventanas de los edificios si estamos en el interior. 
   Activar la ubicación en tu *smartphone* no tiene costes, aunque sí incrementa el consumo de la batería.

En :guilabel:`Select one widgets` podemos encontrar las preguntas en las que sólo es posible **seleccionar una opción** de entre aquellas presentes en la lista facilitada.
Desliza la pantalla hacia la izquierda y repasa las múltiples posibilidades utilizando listas, imágenes, menús desplegables, combinación de listas e imágenes, etc.
En el siguiente ejemplo se muestra el :guilabel:`Grid select one widget` en el que se puede seleccionar la opción atendiendo a imágenes representativas de las mismas.
 
.. figure:: /media/collect_select_list.jpg
   :align: center

El grupo :guilabel:`Select Multi Widgets` agrupa diferentes modelos de preguntas que permiten **seleccionar varias opciones** como respuesta para una pregunta.
Observa el siguiente ejemplo denominado :guilabel:`Multi select widget` que es la versión más simple de todas las existentes.
Continúa avanzando por el formulario para ver otros modelos de preguntas de selección múltiple.

.. figure:: /media/collect_select_multiple.jpg
   :align: center

Llegando a los últimos tipos de pregunta se nos presenta la pregunta :guilabel:`Rank widget` que nos permite establecer un **orden de preferencia** entre las diferentes opciones que se plantean.
Una vez seleccionas :guilabel:`Ranking the items` (1) tienes que cambiar el orden de las respuestas (2), manteniendo ligeramente pulsadas las opciones y arrastrándolas posteriormente hacia el lugar deseado.

.. figure:: /media/collect_rank.jpg
   :align: center

El último tipo de pregunta que se nos muestra es el :guilabel:`Trigger widget` que permite **confirmar** que se ha cumplido (o no) determinadas condiciones en el desarrollo de la encuesta.
Marca la casilla de verificación y desliza la pantalla hacia la izquierda.

.. figure:: /media/collect_trigger.jpg
   :align: center

.. admonition:: Presta atención

   En el formulario que estamos recorriendo puedes dejar sin contestar las preguntas. Sin embargo, es posible obligar a dar respuesta a las preguntas para seguir adelante con la encuesta e incluso validar sobre la marcha la coherencia de las mismas.

Has llegado al final del formulario.
Selecciona “Guardar Formulario y Salir” para **terminar la encuesta** y volver a la pantalla principal de la aplicación.

.. figure:: /media/collect_form_save_exit.jpg
   :align: center
   
Envío de la información al servidor
-----------------------------------

La información está ahora almacenada en nuestro *smartphone*.
Es el momento de **enviarla al servidor** que reúne las encuestas que se hayan realizado desde diferentes dispositivos.

Volvemos a la pantalla principal de la aplicación Collect.
En ella podemos ver que tenemos la posibilidad de enviar o editar el formulario que acabamos de rellenar.
Le damos a “Enviar Formulario Finalizado”.

.. figure:: /media/collect_send_form.jpg
   :align: center

En la siguiente pantalla seleccionamos el formulario (1) y le damos a “Enviar seleccionados” (2).

.. figure:: /media/collect_send_form2.jpg
   :align: center

La aplicación nos informa del resultado del proceso de carga de nuestros datos en el servidor.
Pulsa en :guilabel:`De acuerdo` para cerrar la ventana.

.. figure:: /media/collect_send_form_results.jpg
   :align: center

En la pantalla principal podemos ver que ya tenemos un formulario en la sección de enviados.

.. figure:: /media/collect_send_form_results2.jpg
   :align: center

.. admonition:: Práctica

   Repite el proceso de :guilabel:`Llenar un nuevo formulario` y familiarízate con el manejo de Collect y con las diferentes tipos de preguntas que se pueden configurar.

Resumen y próximos pasos
^^^^^^^^^^^^^^^^^^^^^^^^

En este primer apartado hemos visto los aspectos más esenciales de Open Data Kit: en qué consiste, las diferentes herramientas que lo componen y sus relaciones.
Asimismo, hemos tenido una primera toma de contacto con la herramienta ODK Collect, instalando la aplicación en nuestro dispositivo y comprobando sus enormes potencialidades con un formulario de muestra.

Los siguientes apartados entrarán en detalle en las diferentes herramientas que se han enumerado de forma que seamos capaces de abarcar todo el proceso de recopilación y explotación de la información.
