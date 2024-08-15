# Programming the LANA Module
Om de blaster (flamingo) te programmeren kan je [Mounriver Studio](http://www.mounriver.com/) of [Embeetle](https://embeetle.com/) gebruiken. 

## Standaard WCH IDE 
De eerste (Mounriver) is een IDE op basis van Eclipse gereleased door de chipmaker WCH. Deze werkt op Windows en er is een versie voor Linux en mogelijks ook voor Mac, maar de laatste 2 lopen wat achter. [Mounriver](http://www.mounriver.com/) geeft op veel systemen ook valse meldingen van virussen en schendt de GPL licentie voorwaarden van Eclipse.

## Embeetle
Een mooier alternatief is [Embeetle].(https://embeetle.com/) Dit is een IDE van Belgische makelij. Deze is niet open source maar produceert wel een open toolchain bij het maken van een nieuw project.
[LANA](https://phyx.be/LANA_TNY/) kan je met [Embeetle](https://embeetle.com/) programmeren via de USB connector maar ook met de [WCH-Link debugger](https://www.wch-ic.com/products/WCH-Link.html), deze geeft extra debugging opties.
De makers van [Embeetle](https://embeetle.com/) zijn ook zo lief geweest om voor het [LANA bordje heel knappe documentatie toe te voegen](https://embeetle.com/#supported-hardware/wch/boards/lana-tny-01).


## Opmerking specifiek voor de LANA module
Als je zelf aan de slag gaat met de blaster/LANA TNY dan moet je op 1 ding letten (onafhankelijk van de IDE) en dat is dat LANA geen externe klok heeft en de interne klok (HSI) moet gebruiken, dit staat ook zo in de standaard sketch van [Embeetle](https://embeetle.com/).
Als je per ongeluk je [LANA](https://phyx.be/LANA_TNY/) bordje "bricked" kan je die meestal unbricken via USB of door de power reset feature te gebruiken van de [WCHISPTool](https://www.wch-ic.com/downloads/WCHISPTool_Setup_exe.html).
