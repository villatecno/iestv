# pi-school-tv  

Tv del colegio con Raspberry pi 3 enchufada por HDMI. 
Su función es fichar en Séneca por código QR o llavero RFID y mostrar imágenes en modo presentación.

![](https://www.kubii.es/7147-large_default/raspberry-pi-3-modelo-b-1-gb-kubii.jpg)

![](https://images-na.ssl-images-amazon.com/images/I/61Ry5l0ARoL._AC_SL1500_.jpg)

El lector RFID no necesita drivers ya que se configura como un teclado al conectarlo por usb.

Lleva instalado [Raspberry Pi OS](https://www.raspberrypi.org/software/operating-systems/#raspberry-pi-os-32-bit) (debian buster) 

### Instrucciones y recomendaciones de configuración del sistema: 

[Aquí](https://github.com/aosucas499/pischooltv/wiki/Preconfiguraci%C3%B3n-del-sistema)


## Temporizador y funciones:

1. Se enciende cada día con un **temporizador** en la pared que le da corriente por la mañana y se debe de apagar antes de que dicho temporizador apague el sistema.

![](https://images-na.ssl-images-amazon.com/images/I/41c3xcYQaFL.__AC_SY300_QL70_ML2_.jpg)


2. Cada mañana, al **arrancar el sistema**, abre el navegador Chromium en modo kiosko con la página del [control de presencia de Séneca.](https://seneca.juntadeandalucia.es/controldepresencia/). Tarda unos 40 segundos en iniciar, ya que durante los primeros 30 segundos, el sistema lanza un script que actualiza la hora y la fecha en el sistema. Todo esto es debido a que los dispositivos conectados por WIFI (Andared) a la red de Internet de los centros educativos de Andalucía no actualizan bien la hora.

3. A las **9:20** de la mañana, abre un visualizador de imágenes con las fotos del cole. Lleva activado samba para compartir las imágenes de modo rápido y fácil desde un teléfono móvil.

4. A las **13:50**, abre el navegador Chromium en modo kiosko nuevamente, para el fichaje desde código QR o lector de proximidad RFID. 

5. A las **14:15**, se apaga automáticamente la Raspberry Pi, para que se cierre bien el sistema, ya que a las **14:30** el temporizador de corriente corta la alimentación eléctrica.

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

