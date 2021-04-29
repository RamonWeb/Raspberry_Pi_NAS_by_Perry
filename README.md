# Raspberry_Pi_NAS_by_Perry

https://www.thingiverse.com/thing:4841380

https://github.com/OpenMediaVault-Plugin-Developers/docs/blob/e58023ce7c76d4f83239065e8697e0894d6f94f1/Adden-B-Installing_OMV5_on_an%20R-PI.pdf



Installiert ein Raspbian - Image auf eine SD Karte

z.B. mit https://www.balena.io/etcher/ und https://www.raspberrypi.org/downloads/

Startet nun den Raspberry Pi neu, damit die gemachten Änderungen übernommen werden.

Update / Upgrade

Schließlich ist das System noch auf den aktuellen Stand zu bringen.

Stellt wieder die SSH-Verbindung zum Raspberry Pi:

ssh pi@raspberrypi.local

Verwendet für die Aktualisierung des Systems die integrierte Paketverwaltung. Mit den folgenden Befehlen wird dies erledigt:

sudo apt-get update && sudo apt-get upgrade -y 

sudo reboot



Software Installation ..OMV
wget -O – https://github.com/OpenMediaVault-Plugin-Developers/installScript/raw/master/install | sudo bash

