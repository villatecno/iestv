# pi-school-tv  

Tv del colegio con Raspberry pi 3 enchufada por HDMI. 
Su función es fichar en Séneca por código QR o llavero RFID y mostrar imágenes en modo presentación.

![](https://www.kubii.es/7147-large_default/raspberry-pi-3-modelo-b-1-gb-kubii.jpg)

Lleva instalado Raspberry Pi OS (debian buster) 

Se enciende cada día con un temporizador en la pared que le da corriente por la mañana y se debe de apagar antes de que dicho temporizador apague el sistema.

![](https://images-na.ssl-images-amazon.com/images/I/41c3xcYQaFL.__AC_SY300_QL70_ML2_.jpg)

Al encender debe de abrir el navegador Chromium en modo kiosko con la página del [control de presencia de Séneca](https://seneca.juntadeandalucia.es/controldepresencia/) y a las 9:20 de la mañana debe de abrirse un visualizador de imágenes con las fotos del cole. Debe de llevar activado samba para compartir las imágenes de modo rápido y fácil desde un móvil.

A las 13:50 debe de abrirse el navegador Chromium en modo kiosko nuevamente para el fichaje desde código QR o lector de proximidad RFID. 

El sistema debe de apagarse a las 14:15 para que se cierre bien el sistema ya que a las 14:30 el temporizador de corriente se apaga.

# Instalación

`git clone https://github.com/aosucas499/pischooltv`

`cd pischooltv`

`./pischooltv`

