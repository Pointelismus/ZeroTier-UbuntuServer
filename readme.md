-----------------------------------------
# ZeroTier VPN - Dev Server MEF Streaming
-----------------------------------------
**Dieses Repository ist eine kleinen Zusammenfassung von Coamnd und Informationen die Helfen können den ZeroTier VPN auf Linux bzw. Ubuntu Server zu Instalieren.**


### Instalation des ZeroTier VPN auf Ubuntu Server 22.04.3 LTS:

>	curl -s https://install.zerotier.com | sudo bash

*(Comandline von https://www.zerotier.com/ )*

#### Wenn bei den Folgenden Comands der Fehler "missing authentification token and authtoken.secret no found (or readable)" verwende "sudo zerotier-cli".

### ZeroTier addresse erfahren und status abfragen:

>	zerotier-cli status

*Bsp. Server antwort: "200 info 998765f00d 1.10.6 ONLINE"*

### ZeroTier Netzwerk beitreten:
**Eine ZeroTier Netzwerk ID besteht aus 16 Zeichen, dafür stehen die "#".**

>	zerotier-cli join ################

*Bsp. Server antwort: "200 join OK"*

### ZeroTier Netzwerk verlassen:

>	zerotier-cli leave ################

*Bsp. Server antwort: "200 leave OK"*

### Alle auf dem Server installierten ZeroTier Netzwerke anzeigen:

>	zerotier-cli listnetworks

*Bsp. Server antwort: "200 <nwid> <name> <mac> <status> <type> <dev> <ZT assinged ips>"*

### Ausgabe von Debug Informationen:

>	zerotier-cli dump

*Dieser Comand  erstellt eine Datei mit Inforamtionen über dein Gerät und ZeroTier. Manche darin erhaltene Informationen sollten Privat bleiben.*

**Weitere Inforamtionen findet man auf der [ZeroTier Knowledge Base](https://zerotier.atlassian.net/wiki/spaces/SD/overview?homepageId=163911) und auf [ZeroTier.com](https://www.zerotier.com/)**
