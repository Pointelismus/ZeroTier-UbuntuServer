# ZeroTier VPN - Dev Server MEF Streaming
-----------------------------------------
**Dieses Repository ist eine kleine Zusammenfassung von Befehlen und Informationen, die helfen können, ZeroTier VPN auf einem Linux bzw. Ubuntu Server zu installieren.**

### Installation des ZeroTier VPN auf Ubuntu Server 22.04.3 LTS:

> curl -s https://install.zerotier.com | sudo bash

*(Befehlszeile von https://www.zerotier.com/)*

#### Wenn bei den folgenden Befehlen der Fehler "missing authentication token and authtoken.secret not found (or readable)" auftritt, verwende "sudo zerotier-cli".

### ZeroTier-Adresse herausfinden und Status abfragen:

> zerotier-cli status

*Beispiel Serverantwort: "200 info 998765f00d 1.10.6 ONLINE"*

### ZeroTier Netzwerk beitreten:
**Eine ZeroTier Netzwerk-ID besteht aus 16 Zeichen, dafür stehen die "#".**

> zerotier-cli join ################

*Beispiel Serverantwort: "200 join OK"*

### ZeroTier Netzwerk verlassen:

> zerotier-cli leave ################

*Beispiel Serverantwort: "200 leave OK"*

### Alle auf dem Server installierten ZeroTier-Netzwerke anzeigen:

> zerotier-cli listnetworks

*Beispiel Serverantwort: "200 <nwid> <name> <mac> <status> <type> <dev> <ZT assigned ips>"*

### Ausgabe von Debug-Informationen:

> zerotier-cli dump

*Dieser Befehl erstellt eine Datei mit Informationen über dein Gerät und ZeroTier. Einige darin enthaltene Informationen sollten privat bleiben.*

**Weitere Informationen findest du in der [ZeroTier Knowledge Base](https://zerotier.atlassian.net/wiki/spaces/SD/overview?homepageId=163911) und auf [ZeroTier.com](https://www.zerotier.com/)**
