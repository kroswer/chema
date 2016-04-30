
**Manual Técnico Sensor IR**
=


----------

El proyecto fue desarrollado para trabajar sobre una tarjeta Raspberry PI. Este manual tecnico describe su funcionamiento apropiado.

Integrantes: 

- Hugo Díaz 
- Luis Escamilla
- Gerardo Francia
- Gerardo Maldonado

**Overview**
-
Un sistema embebido (anglicismo de embedded) ) es un sistema de computación diseñado para realizar una o algunas pocas funciones dedicadas, frecuentemente en un sistema de computación en tiempo real. 

La finalidad de nuestro proyecto es tener un sistema funcionando continuamente, que nos sirva como alarma en caso de que el sensor se active y lo alerte mediante un mensaje de Twitter para que cualquiera lo pueda ver. 
**Estructura**
-
------------
**Software**

El script fue escrito utilizando como lenguaje a Python. Es importante recalcar que se utilizo la libreria 		*RPi.GPIO* para poder utilizar los puertos dentro del script. 

Para poder mantener el código como un ***demonio***, se siguieron los siguientes pasos. 

- 1
- 2
- 3

Utiliza a su vez la API de Twitter para Python, para poder enviar información al exterior y poder ser visualizada desde cualquier parte, por multiples usuarios. 

**Hardware**

Comenzamos con el sensor IR, el cual nos devuelve una una señal analogica que varia dependiendo de que tan cerca se encuentre el receptor del emisor. 

Para poder implementar este proyecto se necesitó utilizar un ADC ya que las tarjetas RPi no cuentan con uno integrado. Se eligió un ADC MCP3008 de 8 canales con 10 bits de resolución, el cual le transmite la información mediante SPI a la tarjeta. 
 
 La RPi debe tener conexión a internet, ya sea alambrica o inalambrica, para poder enviar la información a la API de Twitter.
 
 ![Esquematico](https://github.com/cerelacrox/bichoIR/blob/master/SensorIR_Esquematico.PNG?raw=true)

**Funcionalidad**
-
-------
**Operacion**
El sistema, una vez con el servicio para el demonio, al energizar el sistema siempre estará funcionando y si el sensor se activa, mandara un tuit a la cuenta @bichoirdiplo alarmando que el sensor fue activado.
**Glosario**
-

**Sensor IR**: Es un dispositivo optoelectrónico capaz de medir la radiación electromagnética infrarroja

**Esquemático**: Es un diagrama con las conexiones realizadas con el hardware.

**Demonio**: Programa residente que se ejecuta en segundo plano, puede cargarse automáticamente al iniciar el sistema.

**SPI**:  *Serial Peripheral Interface* es un estándar de transferencia de información de forma síncrona.  

**API**:  *Application Programming Interface* es el conjunto de subrutinas, funciones y procedimientos que ofrece cierta biblioteca para ser utilizado por otro software como una capa de abstracción.

**RPi**: Abreviatura de Raspberry Pi.

**ADC**: *Analog-to-digital converter* es un dispositivo que convierte una señal continua fisica un numero digital cuantizable. 

