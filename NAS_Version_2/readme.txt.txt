Rasperry Pi 4 mit einer HDD als NAS mit openmediavault.
https://github.com/OpenMediaVault-Plugin-Developers/docs/blob/master/Getting_Started-OMV6.pdf

openmediavault is a complete network attached storage (NAS) solution based on Debian Linux.

The Raspberry PI OS Imager
From the additional choices provided, select Raspberry PI OS Lite 64bit

Raspberry PI OS Updates and Upgrades
Before installing OMV, update and upgrade Raspberry PI OS using the following commands, executed one at at time:

sudo apt-get update

sudo apt-get upgrade -y



Copy the following line complete (Ctrl+C) and paste it into PuTTY's SSH window, with a right mouse click. Then hit Enter.

wget -O - https://github.com/OpenMediaVault-Plugin-Developers/installScript/raw/master/install | sudo bash



Once the script is running, click out of the SSH window so the script will not be interrupted.
Do Not close PuTTY – that will terminate the root session. Minimizing PuTTY is OK, but it must be running.

Depending on several factors, running this script may take up to 30 minutes.

When the script is complete, the R-PI will automatically reboot.

First Time GUI Logon
After 3 to 5 minutes, OMV can be logged in using the same IP address that was used for the SSH client, entered in a web browser address bar. The web GUI user is admin and the default password is openmediavault

----- mein lt. GitHub

Installiert ein Raspbian - Image auf eine SD Karte

z.B. mit https://www.balena.io/etcher/ und https://www.raspberrypi.org/downloads/
oder Install Raspberry Pi OS using Raspberry Pi Imager
https://downloads.raspberrypi.org/imager/imager_latest.exe

Raspberry PI OS Lite 64bit
(Achtung!!! jetzt gibt es keinen Pi Benutzer mehr...)

Set Username and password will be checked, due to enabling SSH. pi is the default entry.
This user will be the administrative user for command line operations. The administrative username can be changed to the users preference but,
for the purposes of this document, the default username pi will be assumed.

  Warning
If the username is changed it CAN NOT be admin. admin is reserved for the OMV installation.

• Set Username and Password
Set the password. (It would be better to write the password down, than to forget it)


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

und wieder Neustarten... da ist alles bereit...

Die ganze Konfiguration kann jetzt über einen Webbrowser in euren lokalen Netz gemacht werden...

https://github.com/OpenMediaVault-Plugin-Developers/docs/blob/master/Getting_Started-OMV6.pdf
