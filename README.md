# TP2 Depaire Gabin B1B

## 1 Exploration locale en solo

### 1.1 Affichage d'informations sur la pile TCP/IP locale

 **En invite de commande**. Avec la commande **ifconfig** nous avons recupéré ( pour le WIFI et pour le réseau Ethernet ) :
 * le nom du réseau
 * l'adresse IP 
 * ainsi que l'adresse MAC.
 
 <img src="https://github.com/wewlr17/TP2-reseau/blob/master/tp%20iot/ip%20wifi.PNG">
 IMAGE IP ETHERNET

### 1.2 Modification des informations

Calcule de l'adresse IP, du masque de sous réseau, l'adresse broadcast, gateway et de l'adresse réseau en binaire et en base 10 :
* 10.33.3.55 /22 **ip** en Base 10
* 00001010 00100001 00000011 00110111 **ip** en base 2
* **masque** 255.255.252.0 
* 11111111 11111111 11111100 00000000 **masque** en base 2
* **Réseau**	00001010 00100001 00000000 00000000	base 2
* **Réseau** 10.33.0.0	base 10
* **Broadcast** 00001010 00100001 00000011 11111111
* **Broadcast** 10 33 3 255
* **Gateway** 10.33.3.252

> Nous avons du allez dans les paramètres windows,
> ensuite dans réseau et internet, en bas de la fenetre cliquez sur **Afficher vos propriétés réseau**
> > Le gateway dans le réseau ingésup est utilisé pour avoir accés a un internet

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE3OTk0MTgzMDddfQ==
-->
