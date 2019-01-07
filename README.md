# TP2 DEPAIRE Gabin B1B

## I. Exploration locale en solo

### 1.1 Affichage d'informations sur la pile TCP/IP locale

#### En CMD:

<img src="./TP2%20Screen/Ipconfigall%20-%2002.PNG">

**Nom, adresse MAC, adresse IP pour WIFI:**
* Carte réseau sans fil Wi-Fi
* 9C-B6-D0-09-AB-45
* 10.33.2.99

**Nom, adresse MAC, adresse IP pour Ethernet:**
* Carte Ethernet Ethernet
* 9C-B6-D0-09-AB-45
* J'en est pas

**Adresse de réseau:**
Calcule:
* 10.33.2.99 IP Base 10
* 0000.1010 0010.0001 0000.0010 0110.0011 IP
* 1111.1111 1111.1111 1111.1100 0000.0000 MASK
* 0000.1010 0010.0001 0000.0000 0000.0000 Adresse de Reseau
* 10.33.0.0 Adresse de Reaseau Base 10

**Adresse de broadcast:**
Calcule:
* 1111.1111 1111.1111 1111.1100 0000.0000 MASK
* 0000.1010 0010.0001 0000.0011 1111.1111 Brodcast
* 10.33.3.255 Brodcast Base 10

**Afficher la gateway:**
* 10.33.3.253 Parsserelle par défaut

#### En Graphique:

<img src="./TP2%20Screen/IPconfig%20Graph%20-03.PNG">


à quoi sert la gateway dans le réseau d'ingésup:
* Elle sert à relier un réseau Local (étudiant) au réseau mondial (Internet)

### 1.2 Modifications des informations

**A. Modification d'adresse IP**

<img src="./TP2%20Screen/ipconfig%20-%2004.PNG">

Calculez la première et la dernière IP du réseau:
* Première 10.33.0.0
* Dernière 10.33.3.256

**B. nmap**
<img src="./TP2%20Screen/Nmap%20-%2005.PNG">
<img src="./TP2%20Screen/Passerelle%20-%2007.PNG">
* Modifier l'IP: ça ne marche pas ! (Mais normalement soit doit marcher)
* Modifier la passerrelle: ça ne marche pas !

## II. Exploration Locale en duo
### Création d'un réseau / modification d'adresse IP

* Réseau /24:
<img src="./TP2%20Screen/Capture09.PNG">
<img src="./TP2%20Screen/Capture08.PNG">

* Réseau/20:

<img src="./TP2%20Screen/capture10.PNG">
<img src="./TP2%20Screen/capture11.PNG">

### Utilisation d'un des deux comme gateway

* Quand mon pc utilise la gateway pour avoir accès internet:
Ipconfig:
``` PS C:\Users\Florian> ipconfig

Configuration IP de Windows


Carte Ethernet Ethernet :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::70de:8f61:ddbb:d1fc%9
   Adresse IPv4. . . . . . . . . . . . . .: 192.168.137.20
   Masque de sous-réseau. . . . . . . . . : 255.255.255.0
   Passerelle par défaut. . . . . . . . . : 192.168.137.1

Carte réseau sans fil Connexion au réseau local* 3 :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte réseau sans fil Connexion au réseau local* 11 :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte réseau sans fil Wi-Fi :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . : auvence.co

Carte Ethernet Connexion réseau Bluetooth :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :


```
Curl Google:
```PS C:\Users\Florian> curl google.com


StatusCode        : 200
StatusDescription : OK
Content           : <!doctype html><html itemscope="" itemtype="http://schema.org/WebPage" lang="fr"><head><meta
                    content="text/html; charset=UTF-8" http-equiv="Content-Type"><meta
                    content="/images/branding/googleg/1x/goo...
RawContent        : HTTP/1.1 200 OK
                    X-XSS-Protection: 1; mode=block
                    X-Frame-Options: SAMEORIGIN
                    Cache-Control: private, max-age=0
                    Content-Type: text/html; charset=UTF-8
                    Date: Thu, 20 Dec 2018 10:16:41 GMT
                    Expires: ...
Forms             : {f}
Headers           : {[X-XSS-Protection, 1; mode=block], [X-Frame-Options, SAMEORIGIN], [Cache-Control, private,
                    max-age=0], [Content-Type, text/html; charset=UTF-8]...}
Images            : {@{innerHTML=; innerText=; outerHTML=<IMG id=hplogo onload=window.lol&amp;&amp;lol()
                    style="PADDING-BOTTOM: 14px; PADDING-TOP: 28px; PADDING-LEFT: 0px; PADDING-RIGHT: 0px" alt=Google
                    src="/images/branding/googlelogo/1x/googlelogo_white_background_color_272x92dp.png" width=272
                    height=92>; outerText=; tagName=IMG; id=hplogo; onload=window.lol&amp;&amp;lol();
                    style=PADDING-BOTTOM: 14px; PADDING-TOP: 28px; PADDING-LEFT: 0px; PADDING-RIGHT: 0px; alt=Google;
                    src=/images/branding/googlelogo/1x/googlelogo_white_background_color_272x92dp.png; width=272;
                    height=92}}
InputFields       : {@{innerHTML=; innerText=; outerHTML=<INPUT type=hidden value=fr name=hl>; outerText=;
                    tagName=INPUT; type=hidden; value=fr; name=hl}, @{innerHTML=; innerText=; outerHTML=<INPUT
                    type=hidden value=hp name=source>; outerText=; tagName=INPUT; type=hidden; value=hp; name=source},
                    @{innerHTML=; innerText=; outerHTML=<INPUT type=hidden name=biw>; outerText=; tagName=INPUT;
                    type=hidden; name=biw}, @{innerHTML=; innerText=; outerHTML=<INPUT type=hidden name=bih>;
                    outerText=; tagName=INPUT; type=hidden; name=bih}...}
Links             : {@{innerHTML=<SPAN class=gbtb2></SPAN><SPAN class=gbts>Recherche</SPAN>; innerText=Recherche;
                    outerHTML=<A onclick=gbar.logger.il(1,{t:1}); id=gb_1 class="gbzt gbz0l gbp1"
                    href="https://www.google.fr/webhp?tab=ww"><SPAN class=gbtb2></SPAN><SPAN
                    class=gbts>Recherche</SPAN></A>; outerText=Recherche; tagName=A; onclick=gbar.logger.il(1,{t:1});;
                    id=gb_1; class=gbzt gbz0l gbp1; href=https://www.google.fr/webhp?tab=ww}, @{innerHTML=<SPAN
                    class=gbtb2></SPAN><SPAN class=gbts>Images</SPAN>; innerText=Images; outerHTML=<A
                    onclick=gbar.logger.il(1,{t:2}); id=gb_2 class=gbzt
                    href="http://www.google.fr/imghp?hl=fr&amp;tab=wi"><SPAN class=gbtb2></SPAN><SPAN
                    class=gbts>Images</SPAN></A>; outerText=Images; tagName=A; onclick=gbar.logger.il(1,{t:2});;
                    id=gb_2; class=gbzt; href=http://www.google.fr/imghp?hl=fr&amp;tab=wi}, @{innerHTML=<SPAN
                    class=gbtb2></SPAN><SPAN class=gbts>Maps</SPAN>; innerText=Maps; outerHTML=<A
                    onclick=gbar.logger.il(1,{t:8}); id=gb_8 class=gbzt
                    href="http://maps.google.fr/maps?hl=fr&amp;tab=wl"><SPAN class=gbtb2></SPAN><SPAN
                    class=gbts>Maps</SPAN></A>; outerText=Maps; tagName=A; onclick=gbar.logger.il(1,{t:8});; id=gb_8;
                    class=gbzt; href=http://maps.google.fr/maps?hl=fr&amp;tab=wl}, @{innerHTML=<SPAN
                    class=gbtb2></SPAN><SPAN class=gbts>Play</SPAN>; innerText=Play; outerHTML=<A
                    onclick=gbar.logger.il(1,{t:78}); id=gb_78 class=gbzt
                    href="https://play.google.com/?hl=fr&amp;tab=w8"><SPAN class=gbtb2></SPAN><SPAN
                    class=gbts>Play</SPAN></A>; outerText=Play; tagName=A; onclick=gbar.logger.il(1,{t:78});;
                    id=gb_78; class=gbzt; href=https://play.google.com/?hl=fr&amp;tab=w8}...}
ParsedHtml        : mshtml.HTMLDocumentClass
RawContentLength  : 45839 
```
Quand mon collègue ce connecte à internet via mon pc:
* J'ai une version Insider de Windows je n'ai pas l'option "Ethernet"

<img src="./TP2%20Screen/capture12.PNG">

### Chat privé
Une fois sur le même réseau et avec le même port ça donne ça:
<img src="./TP2%20Screen/Capture13.PNG">

### Wirechark
Pendant un ping et un message:

<img src="./TP2%20Screen/capture14.PNG">

Voici les trames concernant les messages en question:

<img src="./TP2%20Screen/capture15.PNG">

Trier les trames avec "tcp.stream eq 0":

<img src="./TP2%20Screen/capture16.PNG">

### Firewall
Gestion des règles:

<img src="./TP2%20Screen/capture17.PNG">

Gestion IP:

<img src="./TP2%20Screen/capture18.PNG">

Gestion protocole:

<img src="./TP2%20Screen/capture19.PNG">

Nous avons essayé de nous Ping avec ceci mais ça ne marche pas !

## III. Manipulations d'autres outils/protocoles côté client
### 1. DHCP
 * Adresse IP du serveur DHCP du réseau WiFi: 10.33.3.254
 * Date d'expiration du bail DHCP:
 <img src="./TP2%20Screen/BailDHCP.PNG">
 * Nouvelle adresse IP (en ligne de commande):
<img src="./TP2%20Screen/1.PNG">
<img src="./TP2%20Screen/2.PNG">
<img src="./TP2%20Screen/3.PNG">

### 2. DNS
'''
ipconfig /all
Serveurs DNS. . .  . . . . . . . . . . : 10.33.10.20
                                       10.33.10.7
                                       8.8.8.8
'''
#### nslookup:
#### lookup:
* Pour  `google.com`
* Pour  `ynov.com`
* Résultats de ces commandes
#### reverse lookup_ :
* pour l'adresse  `78.78.21.21`
* pour l'adresse  `92.16.54.88`
* Résultats




<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4ODE3NjE0MTIsLTEyOTA5NTY5NDAsLT
M0OTI0MjYzMSwxMTcwMDA2ODQ4LC0xNzg3NjY5MzgxLDg3NTAy
ODE4NCwxMDI0NTQyLDE5OTQ2MTQxNDMsLTY5NDc4Nzc1OSwxMz
ExMTA1ODYwLDExMzk0NDA0NTUsMTg1MDgzMjY1LC0xOTM2OTIz
OTM5XX0=
-->
