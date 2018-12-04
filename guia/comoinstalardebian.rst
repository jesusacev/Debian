Como instalar debian 9 desde cero para un server
=====================================

Lo primero que nos mostrará será un menú que nos indica como queremos realizar la instalación. En este caso elegiremos la gráfica, mediante la opción "Graphical Install"


.. image:: ../imagenes/Instalacion_Debian_9/013.png


Luego elegiremos el idioma con que queremos que se realice la instalación, en nuestro caso español:


.. image:: ../imagenes/Instalacion_Debian_9/014.png


Seguidamente nuestra ubicación para que se defina la zona horaria:


.. image:: ../imagenes/Instalacion_Debian_9/015.png


Se configura el teclado dependiendo del tipo que tengamos:


.. image:: ../imagenes/Instalacion_Debian_9/016.png


Se empiezan a cargar componentes:


.. image:: ../imagenes/Instalacion_Debian_9/017.png


Le damos el nombre a nuestro servidor:


.. image:: ../imagenes/Instalacion_Debian_9/018.png


Le damos el nombre del dominio:


.. image:: ../imagenes/Instalacion_Debian_9/019.png


Le asignamos la contraseña al usuario root:


.. image:: ../imagenes/Instalacion_Debian_9/020.png


Luego se crea una cuenta de usuario alternativa a la de root, para ser usada en tareas que no sean administrativas. Se coloca el nombre completo para el usuario:


.. image:: ../imagenes/Instalacion_Debian_9/021.png


Se asigna el nombre de usuario para la cuenta:


.. image:: ../imagenes/Instalacion_Debian_9/022.png


Se le asigna la contraseña a la nueva cuenta:


.. image:: ../imagenes/Instalacion_Debian_9/023.png


Se empiezan a cargar nuevas configuraciones, incluida la configuración del reloj:


.. image:: ../imagenes/Instalacion_Debian_9/024.png


Pasamos a la parte de particionado de discos, en este caso elegimos manual para entener bien como se realiza dicho particionado:


.. image:: ../imagenes/Instalacion_Debian_9/025.png


Seleccionamos el disco que tenemos:


.. image:: ../imagenes/Instalacion_Debian_9/026.png


Luego nos preguntará si queremos crear una tabla de particiones vacía en este dispositivo, y le decimos que sí. Si llegara a haber otras particiones ya configuradas, serán eliminadas:

.. image:: ../imagenes/Instalacion_Debian_9/027.png


Seleccionamos todo el espacio libre:


.. image:: ../imagenes/Instalacion_Debian_9/028.png


Creamos una partición nueva:


.. image:: ../imagenes/Instalacion_Debian_9/029.png


En los server debemos respetar la premisa de que la partición var sea la que tenga mayor espacio, y la swap dependerá de la ram. Sí la ram está entre 1 y 2 GB, la swap sera 1,5 veces la ram; y si esta entre 2 a 8 GB, la memoria de intercambio debe ser igual a la ram. Es recomendable asignar los espacios, antes de empezar el particionado.


Asignamos el espacio que le daremos a la partición. Este puede ser especificado en número o en porcentaje:


.. image:: ../imagenes/Instalacion_Debian_9/030.png


Como es la partición / la que estamos creando le decimos que sea primaria:


.. image:: ../imagenes/Instalacion_Debian_9/031.png


Le decimos que la nueva partición se cree al principio:


.. image:: ../imagenes/Instalacion_Debian_9/032.png


Le colocamos la marca de arranque activada:


.. image:: ../imagenes/Instalacion_Debian_9/033.png



Y le decimos que se ha terminado de definir la partición:


.. image:: ../imagenes/Instalacion_Debian_9/034.png


Volvemos a seleccionar el espacio libre:


.. image:: ../imagenes/Instalacion_Debian_9/035.png



Creamos otra partición que en este caso será para /home:


.. image:: ../imagenes/Instalacion_Debian_9/036.png


Le asignamos la cantidad que queremos que ocupe del disco. Como es un server, /home no debe tener tanto espacio, a diferencia de cuando se realiza la instalación para un desktop:


.. image:: ../imagenes/Instalacion_Debian_9/037.png


Le decimos que sea una partición lógica:


.. image:: ../imagenes/Instalacion_Debian_9/038.png


Que la partición se cree al principio:


.. image:: ../imagenes/Instalacion_Debian_9/039.png


Y luego le damos a la opción de se ha terminado de definir la partición:


.. image:: ../imagenes/Instalacion_Debian_9/040.png


Y así crearemos todas las particiones que necesitemos y el área de intercambio:


.. image:: ../imagenes/Instalacion_Debian_9/059.png


Creamos la partición para la swap:


.. image:: ../imagenes/Instalacion_Debian_9/060.png


le asignamos el espacio:


.. image:: ../imagenes/Instalacion_Debian_9/061.png


Le decimos que sea lógica:


.. image:: ../imagenes/Instalacion_Debian_9/062.png


En la opción utilizar como, le decimos que sea área de intercambio:


.. image:: ../imagenes/Instalacion_Debian_9/063.png

.. image:: ../imagenes/Instalacion_Debian_9/064.png

.. image:: ../imagenes/Instalacion_Debian_9/065.png


Y así finalmente queda nuestro particionado:


.. image:: ../imagenes/Instalacion_Debian_9/066.png


Seleccionamos la opción de finalizar el particionado y escribir los cambios en el disco:


.. image:: ../imagenes/Instalacion_Debian_9/067.png


Le decimos que sí a la pregunta de si deseamos escribir los cambios en los discos:


.. image:: ../imagenes/Instalacion_Debian_9/068.png


Luego nos pregunta que si deseamos analizar otro cd o dvd. En nuestro caso no, ya que estamos instalando una sola ISO:


.. image:: ../imagenes/Instalacion_Debian_9/070.png


Seguidamente nos pregunta si deseamos utilizar una réplica de red. Le decimos que no, ya que queremos instalar solo los paquetes que contiene la ISO:


.. image:: ../imagenes/Instalacion_Debian_9/071.png


Se cargan configuraciones del gestor de paquetes, incluidas las de apt:


.. image:: ../imagenes/Instalacion_Debian_9/072.png


Luego nos pregunta si queremos participar en una encuesta sobre el uso de paquetes, y en nuestro caso le decimos que no:


.. image:: ../imagenes/Instalacion_Debian_9/073.png


Seleccionamos los programas a instalar. En este caso unicamente las utilidades estandar del sistema, ya que luego instalaremos lo que necesitemos a traves de los repositorios de Debian:


.. image:: ../imagenes/Instalacion_Debian_9/074.png


Comienza la instalación de los programas seleccionados:


.. image:: ../imagenes/Instalacion_Debian_9/075.png


Luego nos pregunta si deseamos instalar el cargador de arranque GRUB y le decimos que sí:


.. image:: ../imagenes/Instalacion_Debian_9/076.png


Seleccionamos el disco a donde será instalado:


.. image:: ../imagenes/Instalacion_Debian_9/077.png


Se instalar el cargador de arranque GRUB:


.. image:: ../imagenes/Instalacion_Debian_9/078.png


¡FELICITACIONES! has instalado debian 9 de manera satisfactoria:


.. image:: ../imagenes/Instalacion_Debian_9/079.png


Finalmente te solicitará el login para poder acceder al servidor:


.. image:: ../imagenes/Instalacion_Debian_9/080.png


