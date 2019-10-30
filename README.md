# TINY-DEVKIT-SIGFOX

# ESP8266-LOW-POWER-DEVKIT

## ESP8266 LOW POWER DEVKIT IMAGEN

![](https://github.com/markoAntonio1692/TINY-DEVKIT-SIGFOX/blob/master/imagenes/front.JPG)

![](https://github.com/markoAntonio1692/TINY-DEVKIT-SIGFOX/blob/master/imagenes/rear.JPG)


## Caracteristicas

- Diseñado para un ultrabajo consumo de energia.
- Chip ESP07 o ESP07S a bordo.
- Puede conectar una antena externa para tener mayor señal
- Ideal para aplicaciones con baterias de tipo Iones de Litio 1S y paneles solares
- Cuenta con un regulador de tension LDO TC1262 3.3V puede suministrar hasta 500mA.
- Incorpora un transistor mosfet canal N  en modo Drenador abierto (Drain open) conectado al Pin D8 (GPIO15), para activar o desativar circuitos con un maximo de corriente de 250mA.
- Boton de reset.
- Pin ADC para lecturas analogicas directamente con el chip esp8266 [0-1] voltios de rango.
- O tambien puede usar en Pin A0 donde puede ampliear el rango de lectura hasta los 6 Voltios.
- Jumper para cambiar de  modo programacion a modo normal y viceversa.
- Jumper en el pin D0 a GND para modo "Deep Sleep"
- Pin Header "SW" o Switch. puede agregar un interruptor externo, o puede solamente unirlos colocando un Jumper.
- Programable con Ide Arduino.
- Compatible con pines de placa "Nodemcu".


## Caracteristicas Electricas

| Voltaje Maximo VIN| 6.5 Voltios                    |
| ------------- | ------------------------------ |
| Voltaje Minimo  VIN |  3.5 Voltios    |  
| Voltaje  Salida  |  3.3 Voltios    | 
| Corriente minima en reposo   | 80uA     |
| Corriente maxima   | 500mA     |
| Lectura Analogica pin ADC   | 0-6 Voltios     |
| Lectrura analogica pin A0   | 0-1 Voltios     |

## Descripcion de pines

| Pin| Descripcion                    |
| ------------- | ------------------------------ |
| D0 |  GPIO16, Wake up deep Sleep    |  
| D1  |  GPIO5, SCL    | 
| D2   | GPIO4, SDA     |
| D3/PU   | GPIO0, pull_up, Flash mode     |
| D4/PU/LED   | GPIO4, pull_up, led interno esp     |
| D5   | GPIO14, SCLK     |
| D6   | GPIO12, MISO     |
| D7   | GPIO13, MOSI     |
| D8/DOP   | GPIO15, Drenador abierto (Drain open), CS     |
| TX   | GPIO1     |
| RX   | GPIO3    |
| ADC   | Lectrura analogica [0-1] Voltios    |
| A0   | Lectrura analogica [0-6] Voltios   |


# Cargar un Programa a ESP8266 DEVKIT LOW POWER
- Alimente a la placa ESP8266 DEVKIT LOW POWER por VIN.
- Coloque un Jumper entre los pin Heder "SW", o puede usar un switch externo si lo necesita.

![](https://github.com/markoAntonio1692/ESP8266-LOW-POWER-DEVKIT/blob/master/Imagenes/vin.JPG)
- Utilice un Conversor UBS A Serial TTL como FTDI, CH340, CP210x, etc. Conectelo de la forma correspondiente. 
- Cambie el Jumper a la posicion que se muestra en la imagen y reinicie a ESP8266 LOW POWER DEVKIT con el boton RST, esta accion pondra a la esp8266 en modo programacion
![](https://github.com/markoAntonio1692/ESP8266-LOW-POWER-DEVKIT/blob/master/Imagenes/serial.jpg)

- Conecte a su PC su Conversor UBS A Serial TTL, espere que sea reconocido por los drivers.
- Abra su ide Arduino.
- Selecciones un ejemplo.
- Selecciones su puerto COM que fue detectado.
- Seleciones la Placa Nodemcu 1.0 y Cargue!
 (Si no tiene instalado la placa esp8266 en Ide Arduino se recomienda usar los Siguientes pasos)
`<link>` : <https://www.luisllamas.es/programar-esp8266-con-el-ide-de-arduino/>

![](https://github.com/markoAntonio1692/ESP8266-LOW-POWER-DEVKIT/blob/master/Imagenes/arduinocom.jpg)

![](https://github.com/markoAntonio1692/ESP8266-LOW-POWER-DEVKIT/blob/master/Imagenes/arduino.jpg)

![](https://github.com/markoAntonio1692/ESP8266-LOW-POWER-DEVKIT/blob/master/Imagenes/arduinoprog.jpg)

- Una vez cargado el Sketch a su ESP8266 LOW POWER DEVKIT Cambie la posicion del Jumper a su estado inicial y nuevamente reinicie con el boton reset, el esp8266 arrancara con su el sketch cargado.

## Transitor Mosfet N en pin D8 (D8/DOP) 
-  Use este transistor para activar cargas de un maximo de 250 mA, con una salida de 1 logico o HIGH, enciende la carga, con 0 o LOW apaga a la carga.

![](https://github.com/markoAntonio1692/ESP8266-LOW-POWER-DEVKIT/blob/master/Imagenes/mosfet.jpg)




