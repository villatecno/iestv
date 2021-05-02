# pi-school-tv  

Tv del colegio con Raspberry pi 3 enchufada por HDMI. 
Su función es fichar en Séneca por código QR o llavero RFID y mostrar imágenes en modo presentación.

![](https://www.kubii.es/7147-large_default/raspberry-pi-3-modelo-b-1-gb-kubii.jpg)

![](https://images-na.ssl-images-amazon.com/images/I/61Ry5l0ARoL._AC_SL1500_.jpg)

Lleva instalado [Raspberry Pi OS](https://www.raspberrypi.org/software/operating-systems/#raspberry-pi-os-32-bit) (debian buster) 

## Temporizador y funciones:

1. Se enciende cada día con un **temporizador** en la pared que le da corriente por la mañana y se debe de apagar antes de que dicho temporizador apague el sistema.

2. Cada mañana, al **arrancar el sistema**, abre el navegador Chromium en modo kiosko con la página del [control de presencia de Séneca.](https://seneca.juntadeandalucia.es/controldepresencia/) 

3. A las **9:20** de la mañana, abre un visualizador de imágenes con las fotos del cole. Lleva activado samba para compartir las imágenes de modo rápido y fácil desde un teléfono móvil.

4. A las **13:50**, abre el navegador Chromium en modo kiosko nuevamente, para el fichaje desde código QR o lector de proximidad RFID. 

5. A las **14:15**, se apaga automáticamente la Raspberry Pi, para que se cierre bien el sistema, ya que a las **14:30** el temporizador de corriente corta la alimentación eléctrica.

## Instalación

`git clone https://github.com/aosucas499/pischooltv`

`cd pischooltv`

`./pischooltv`

