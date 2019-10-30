# TINY-DEVKIT-SIGFOX

## ESP8266 LOW POWER DEVKIT IMAGEN

![](https://github.com/markoAntonio1692/TINY-DEVKIT-SIGFOX/blob/master/imagenes/front.JPG)

![](https://github.com/markoAntonio1692/TINY-DEVKIT-SIGFOX/blob/master/imagenes/rear.JPG)


## Caracteristicas

- Diseño, simple y robusto para aplicaciones de bajo consumo de energia. 
- Incorpora Chip WISSOL WSSFM11R2DAT a bordo para conexiones a red Sigfox.
- Incorpora una antena Helicoidal para una optima cobertura, ademas incluye un conector UF-L para antenas externas.
- Ideal para aplicaciones con microcontroladores externos, Pic, Arduino, Arm, Freescale, Raspberry Pi. Deben contar con Puerto Serial RX,TX a 9600 baudios a niveles dde tension de 3.3V.
- Voltaje de Funcionamiento de 3.3V
- Puede ser alimentado directamente con 2 Baterias Alcalinas AA, AAA, C, D.
- Se Garantiza alta duracion de baterias.


## Caracteristicas Electricas

| Descripcion| Unidad                    |
| ------------- | ------------------------------ |
| Voltaje de Funcionamiento  |  3.3V    |  
| Voltaje  Maximo de Entrada  |  3.6 Voltios    | 
| Voltaje minimo de Entrada   | 2.7 Voltios     |
| Consumo corriente TX | 170mA      |
| Consumo corriente RX   | 32mA     |
| Consumo en modo Deep Sleep   | 2.5uA     |

## Descripcion de pines

| Pin| Descripcion                    |
| ------------- | ------------------------------ |
| G |  GND    |  
| Rx  |  Rx WSSFM11R2DAT    | 
| Tx   |  Tx WSSFM11R2DAT     |
| Rst   | Reset WSSFM11R2DAT    |
| +3V   | VIN, Voltaje de entrada [2.7 - 3.6]Voltios    |
| G   | GND     |



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




