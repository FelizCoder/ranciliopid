<<<<<<< HEAD
# Rancilio PID meets Clevercoffee

<div align="center">
<img src="https://img.shields.io/github/workflow/status/rancilio-pid/ranciliopid/Build/Alpha-3.0.0">
<img src="https://img.shields.io/github/last-commit/rancilio-pid/ranciliopid/Alpha-3.0.0"><br>
<a href='https://ko-fi.com/clevercoffee' target='_blank'><img height='35' style='border:0px;height:46px;' src='https://az743702.vo.msecnd.net/cdn/kofi3.png?v=0' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>
<br>
  <br>
  How to Video:<br>
  https://youtu.be/KZPjisOEcQ4

</div>

## Version
MASTER VERSION
Version 3.0.1  (07.06.2022)

## Hinweise
Unsere Projektwebseite findet ihr hier: [Clever Coffee Website](https://clevercoffee.de).

Wir empfehlen euch gerne unser Handbuch hier in Github zu erst anzuschauen,
hier geht es zum deutschen Handbuch: [Link](https://rancilio-pid.github.io/ranciliopid-handbook/)

Unseren Chat für die gemeinsame Zusammenarbeit und Fragen findet ihr hier: [Link](https://chat.rancilio-pid.de)

Anregungen zur Weiterentwicklung der Software werden von uns gerne aufgenommen. User-Input ist immer willkommen und bringt den PID weiter!
Ihr seid herzlich Willkommen uns gemeinsam bei der Mission zu besseren Espresso zu helfen. 

## Was nach einem Umbau möglich ist
 * **NEU** Eigene über den Node gehostet Webseite für die Einstellung der PID.
 * **NEU** Übergang vom Dampfmodus in den normalen Modus optimiert.
 * **NEU** MQTT (IoT) Support, um alle wichtigen Parameter zu manipulieren. 
 * Automatischer Kaltstart für das perfekte Erreichen der Soll-Temperatur innerhalb von 8 bis 12 Minuten (je nach Maschine) 
 * Integration einer Waagefunktion. Dokumentation im Handbuch steht noch aus. 
 * Steammodus mit Displayausgabe und eigenen PID Regler und Temperatur (in der App unter Expertenmodus) 
 * Integration von einem Füllstandssensor. 
 * Brüherkennung per Sensor bei OnlyPID. [mehr dazu](https://rancilio-pid.github.io/ranciliopid-handbook/de/customization/brueherkennung.html#konfiguration-der-erkennung).
 * Shottimer einstellbar, um die Bezugdauer zu sehen.
 * Aktuell 3 Displaydesgins für die Anzeige, Möglichkeit weitere Designs einfach einzubinden. 
 * Vertikales Template fürs Display 
 * Support für Siliva E Maschinen: Trigger mit definierbaren Intervall für ein Relais zum Überbrücken der Eco-Funktion
 * Regelung der Brühtemperatur mit einer Genauigkeit von bis zu +/- 0,1°
 * Steuerung der Brühzeit inkl. Pre-Infusion in der Ausbaustufe „Vollausbau“ möglich
 * Bedienung über eine Smartphone-App (iOS & Android) via Blynk (Blynk Server ist leider abgekündigt, unterstützen wir aber weiter)
 * Datenmonitoring über Grafana (webbasiert) 
 * Updates der PID-Software sind drahtlos über WLAN möglich
 * Unsere PID-Software ist OpenSource: für euch kostenfrei und auf persönliche Anforderungen anpassbar
 * Geringer Platzbedarf, passt problemlos in die meisten kleineren Espressomaschinen
 * Die serienmäßige Verkabelung der Maschine bleibt erhalten und wird nur erweitert. Die Maschine kann nach dem Umbau problemlos wieder zurückgerüstet werden.
 * Aktive User-Community im Projektchat mit schnellem Support
 * Support seit 4 Jahren mit kontinuerlichen Anpassungen

Anregungen zur Weiterentwicklung der Software werden von uns gerne aufgenommen. User-Input ist immer willkommen und bringt den PID weiter!
Ihr seid herzlich Willkommen uns gemeinsam bei der Mission zu besseren Espresso zu helfen. 

Vielen Dank an jeden einzelnen Unterstützer!

=======
# CleverCoffee
(formerly Rancilio PID)

<div align="center">
<img src="https://img.shields.io/github/actions/workflow/status/rancilio-pid/clevercoffee/main.yml?branch=master">
<img src="https://img.shields.io/github/last-commit/rancilio-pid/clevercoffee/master"><br>
<a href='https://ko-fi.com/clevercoffee' target='_blank'><img height='35' style='border:0px;height:46px;' src='https://az743702.vo.msecnd.net/cdn/kofi3.png?v=0' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>
</div>

# About

This project implements a PID controller for stable and accurate temperature control, originally for Rancilio Silvia espresso machines but also includes support for Gaggia and Quickmill machines. Others can easily be added or are already compatible.

Additional features include:

* shot timer
* pre-infusion (reduced initial pressure using a dimmer for the pump)
* brew by weight (using weight cells, no support for external scales yet)
* brew by time
* pressure monitoring

The hardware has a small footprint and can easily fit into most smaller espresso machines. The original wiring of the machine (mostly) remains and is only extended. The machine can be easily reversed to the orignal state after the conversion.

The project has been in active development and supported for 4 years with continuous improvements. Hundreds of machines have been converted to PID control already.

You can find our project website here: [Clever Coffee Website](https://clevercoffee.de).

This software is Open Source: free of charge for you and customizable to your personal needs.

We recommend you have a look at the manual before starting a build, you can find the german one [here](https://rancilio-pid.github.io/ranciliopid-handbook/). It is currently being reworked to include all the latest features. The english one is sadly still very outdated but will also be updated soon.

Our chat for collaboration and questions can be found[here](https://chat.rancilio-pid.de).

Video tutorial on how to flash the firmware (a little outdated but mostly still valid):<br>
https://youtu.be/KZPjisOEcQ4

## Version
Version 3.1.2 will be the last major version to support ESP8266, there will only be bug fixes for this platform.
All newer releases will only target the ESP32.

## What is possible after installation into your espresso machine?
 * Control of the brew temperature with an accuracy of up to +/- 0,1°.
 * Reaches the target temperature within 5 to 10 minutes after switching on (you should, however, wait a bit longer, e.g. 20 min depending on the machine to heat up the group head etc.)
 * Set PID parameters and monitor current temperature and heater output on a web page hosted on the ESP controller
 * Separate PID for steam mode with own parameters and target temperature (can be enabled in the web interface/MQTT or using the steam switch)
 * Automatically brew by set time (including pre-infusion with additional dimmer for the pump).
 * Automatically brew by weight when scale components are built in.
 * Allows brew switch detection (e.g. for the shot timer) by using an optocoupler module when deciding not to control the pump from the ESP ([details](https://rancilio-pid.github.io/ranciliopid-handbook/de/customization/brueherkennung.html#konfiguration-der-erkennung)).
* MQTT (IoT) support to monitor and manipulate all important parameters.
 * Extended data monitoring via Influxdb/Grafana.
 * Choose from multiple designs for the display (including vertical), possibility to integrate custom designs
 * Over-The-Air updates of the firmware (WiFi)

User feedback and suggestions for further development of the software are most welcome.
You are welcome to help us in our mission to make better espresso :)

Thanks to every single supporter!
>>>>>>> origin/master
