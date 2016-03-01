# eurobotics-hardware
Hardware del equipo Eurobotics Enginering para el desarrollo de robots participantes en Eurobot.

Contenído del repositorio HW de ARC Eurobotics Engineering
----------------------------------------------------------

Aclaraciones:

 - Cada carpeta del repositorio se corresponde con una tarjeta.

 - En el root de cada capeta se encuentra el proyecto de desarrollo de la tarjeta (Eagle, Orcad, Altium...). Si es una tarjeta comercial la documentación dada por el fabricante.

 - Por lo general, los archivos de cada proyecto se nombran como MMMMM_rXX, donde XX es la revisión y MMMMM el nombre de la tarjeta. La modificaciones sobre tarjetas fabricadas se documentan añadiendo al nombre del fichero de diseño el sufijo _NNNN_rYY, donde NNNN es el identificador de la modificacion y YY es el número revisión de la modificación. Por ejemplo: "mainboard_r15_eurobot2012_r1.pdf" es la modificación para eurobot 2012 con revisión 1 de la tarjeta mainboard correspondientes a la revisión 15 de los esquemas. 

 - Cada carpeta de una tarjeta desarrollada puede contener las siguientes subcarpetas:
   # bom: listado de materiales.
   # cam: ficheros de fabricación y versión en pdf de versiones de tarjetas fabricadas o de modificaciones en placa realizadas para una edición concreta de Eurobot.
	


A continuación se explican brevemente las tarjetas del repositorio:

dspic22_protoboard
------------------ 
Tarjeta prototipo basada en microcontrolador dspic33. Características: control motores (DC, Dunkermotoren, servo, AX12), comunicaciones (RS-232, BT, SPI, I2C), sensores (industriales, TTL, laser analógico y encoders en cuadratura), expansaor I2C de 16 E/S. Desarrollada para Eurobot 2010. Diseñada en Eagle (sólo esquematicos). Fabricada sobre tarjeta de prototipos. Es la tarjeta que se utilizó en el robot prototipo, llamado Dumybot, con el que se portó las librerías Aversive.

mainboard_v01
-------------
Tarjeta principal del robot. Compuesta por dos microcontroladores dspic33 comunicados por I2C, un maestro y un esclavo. El maestro está pensado para implementar la navegación motoriz y estrategia del robot, y el esclavo para controlar la mecánica del robot. 

Conectividad: 3 motores Dunkermotoren a 24V, 2 motores DC de 12V, 1 driver de solenoide, 1 Rele, 2 telémetros lásers, 5 servos standar, servos AX12, 3 encoders con salida en cuadratura, 7 sensores industriales a 12V, 1 RS-232, 2 Bluetooth. 

Desarrollada para el robot de Eurobot 2010. Dieño en Eagle (esquematicos y PCB). Tiene varios bugs documentados y solucionados en la versión 2.

mainboard_v02 
-------------
Segunda versión de la tarjeta principal de los robots. Tiene algunos bugs y mejoras documentadas. Desarrollada para Eurobot 2012 y utilizada en las ediciones posteriores.

mainboard_v03 
-------------
Tercera versión de la tarjeta principal de los robots desarrollada. PCB diseñado por Rubén Espino. Compuesta por un únicao un microcontrolador.

Conectividad: 3 motores DC de 12V, 4 servos standar, servos AX12, 2 encoders con salida en cuadratura, 1 encoder de único canal, 11 sensores industriales a 12V, 1 RS-232, 1 Bluetooth. 

Desarrollada para Eurobot 2014 y utilizada en las ediciones posteriores.

beaconboard_v01
--------------- 
Electrónica de la baliza desarrollada para Eurobot 2010 por Diego Salazar. Permite el control de 1 motor DC con encoder en cuadratura, la lectura de 2 sensores de tipo Keyence y de 2 sensores opticos de herradura. Permite la comunicación por Bluetooth. Tiene bugs resueltos en placa, pero no todos documentados. Diseño en Orcad (esquemas y PCB).

sensorboard
----------- 
Tarjeta de expansión E/S digital por I2C (32 E/S). Desarrollada para Eurobot 2010 y reutilizada en las siguientes ediciones.


swithboard
---------- 
Tarjeta de distribución de alimentación de los robots. Permite activar de forma independiente las diferentes alimentaciones: 24V, 12V y 5V. Desarrollada para Eurobot 2010 y reutilizada en las siguientes ediciones. Diseño en Eagle (esquemáticos y PCB).
m3_atx: fuente de alimentación mini ATX. Perminte un rango de alimentación variable y da salidas de +/-12V, 5V y 3.3V.  Se ha utilizado desde Eurobot 2010 para alimentar la electrónica del robot a partir de baterías. Es una tarjeta comercial.
