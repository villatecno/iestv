# pi-school-tv  

Tv del instituto con Raspberry pi 3 enchufada por HDMI. 
Su función es fichar en Séneca por código QR o llavero RFID y mostrar imágenes en modo presentación.

![](https://www.kubii.es/7147-large_default/raspberry-pi-3-modelo-b-1-gb-kubii.jpg)

![](https://images-na.ssl-images-amazon.com/images/I/61Ry5l0ARoL._AC_SL1500_.jpg)

El lector RFID no necesita drivers ya que se configura como un teclado al conectarlo por usb.

+ Compatible con [Raspberry Pi OS](https://downloads.raspberrypi.org/raspios_armhf/images/raspios_armhf-2021-05-28/2021-05-07-raspios-buster-armhf.zip) (Legacy basado en debian buster). No descarges el más actual, utiliza solo la versión del enlace anterior.

### Instrucciones y recomendaciones de configuración del sistema: 

[Aquí](https://github.com/aosucas499/pischooltv/wiki/Preconfiguraci%C3%B3n-del-sistema)


## Temporizador y funciones:

1. Se enciende cada día con un **temporizador** en la pared que le da corriente por la mañana y se debe de apagar antes de que dicho temporizador apague el sistema. En nuestro caso se ha programado **el encendido a las 8:00 y el apagado a las 15:00**. En el reloj temporizador **se enchufa la Raspberry PI y también el televisor**.

![](https://images-na.ssl-images-amazon.com/images/I/41c3xcYQaFL.__AC_SY300_QL70_ML2_.jpg)


2. Cada mañana, al **arrancar el sistema**, abre el navegador Chromium en modo kiosko con la página del [control de presencia de Séneca.](https://seneca.juntadeandalucia.es/controldepresencia/). Tarda unos 40 segundos en iniciar, ya que durante los primeros 30 segundos, el sistema lanza un script que actualiza la hora y la fecha en el sistema. Todo esto es debido a que los dispositivos conectados por WIFI (Andared) a la red de Internet de los centros educativos de Andalucía no actualizan bien la hora. El inicio del navegador Chromium en el arranque del sistema no ocurre de forma temporizada, ocurriría de la misma manera si de forma accidental se encendiera la raspberry a otra hora distinta.

4. En nuestro centro las clases se inician a las 8:15, por lo cual hay que fichar antes. Pasado un tiempo prudencial de 7 minutos, a las **8:22** de la mañana, se abre un visualizador de imágenes con fotos del Instituto o avisos en forma de archivo de imagen. Lleva activado samba para compartir las imágenes de modo rápido y fácil desde un ordenador Windows (usando por ejemplo WinSCP https://winscp.net/eng/docs/lang:es) o un teléfono móvil. Igualmente se activará la presentación de imágenes (slideshow) 7 minutos después de cada momento de fichaje: **En total, se abrirá el visualizador de imágenes a las 8:22, las 9:22, las 10:22, las 11:22, las 11:52, las 12:52 y las 13:52.**

5. Por otra parte, unos 7 minutos antes de cada cambio de hora, se vuelve a abrir el navegador Chromium en modo kiosko, para el fichaje desde código QR o lector de proximidad RFID.**El navegador Chromium para fichar se activará a las 9:08, las 10:08, las 11:08, las 11:38, las 12:38, las 13:38 y las 14:38**. Como se ha dicho anteriormente, la primera vez que se abre por la mañana (que debía ser antes de las 8:15) no se hace en un momento exacto sino cuando el sistema arranca, que serán aproximadamente las 8:00 y depende del reloj temporizador.   

6. Finalmente, a las **14:57**, se apaga automáticamente la Raspberry Pi, para que se cierre bien el sistema, ya que a las **15:00** el temporizador de corriente corta la alimentación eléctrica, tanto de la Raspberry Pi como del televisor.

## Instalación

`git clone https://github.com/aosucas499/pischooltv`

`cd pischooltv`

`chmod +x pischooltv`

`./pischooltv`

## Envío de imágenes desde el teléfono móvil.

Se debe de usar una aplicación que comparta archivos entre el teléfono y la raspberry a través del protocolo SAMBA. 

Tutorial para compartir imágenes: 
[Aquí](https://github.com/aosucas499/pischooltv/wiki/Im%C3%A1genes-de-Android-a-la-Raspberry)

Si este proyecto te ayuda, puedes invitarme a un café.


If this project helps you,  you can give me a cup of coffee .


[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/donate?business=FUMT27MVTRTHJ&no_recurring=0&item_name=Proyectos+TIC+Andaluc%C3%ADa&currency_code=EUR)

