# Sweet 4x4

## Kenmerken

De Sweet 4x4 macropad is nu in zijn derde iteratie. Dit keer gebruik je een [LANA TNY](https://phyx.be/LANA_TNY/) (of een ander [XIAO / QtPy compatibel bord](https://github.com/adafruit/awesome-qt-py)) als het hart van deze macropad. Je kunt kiezen voor 16 toetsen of 15 toetsen en een draaischakelaar.

![voltooide macropad](backlit.gif)

## Stapsgewijze montagegids

### Overzicht

Het pakket dat je hebt ontvangen bevat alles wat je nodig hebt om je eigen Sweet 4x4 te bouwen.

- 15 sockets
- 15 schakelaars
- 16 diodes
- 6 WS2812 LED's
- 2 condensatoren
- 1 [LANA TNY](https://phyx.be/LANA_TNY/)
- 1 roze printplaat
- Schroeven en afstandhouders `HOEVEEL?`

![onderdelen uitgespreid](overview.jpg)

### Sockets

Laten we beginnen met de laagste componenten, in dit geval de keysockets. Plaats de sockets in de gaten en soldeer de 2 SMD-pads aan de zijkanten vast. Doe dit 15 keer, tenzij je geen encoder wilt, dan kun je kiezen voor 16 sockets en toetsen. (Voor degenen die geen sockets willen, kun je ook je toetsen direct op de printplaat solderen.)

![SMD key sockets](sockets.jpg)

### Diodes

De 16 diodes moeten gebogen worden om goed op de printplaat te passen. De twee onderste hoeken zijn hiervoor ontworpen en speciaal bedoeld voor het buigen van deze onderdelen. Zodra alle diodes gebogen zijn, kun je beginnen met het solderen in de twee cirkels naast elkaar. De zwarte lijn op de diode (de kathode) moet naar buiten gericht zijn.

![voorgebogen diode](diode1.jpg)
![gebogen diode](diode2.jpg)
![diode solderen](diode3.jpg)

### LANA TNY

Je kunt de [LANA TNY](https://phyx.be/LANA_TNY/) module solderen met de meegeleverde doorvoerpennen OF je kunt het SMD solderen voor de laagste profieloplossing. Als je kiest voor de oppervlakmontage, kun je enkele pennen gebruiken om de module correct uit te lijnen voordat je het soldeert, zoals hieronder weergegeven.

![LANA solderen](lana.jpg)

### WS2812 LED's

Soldeer 6 WS2812 RGB-LED's aan de onderkant zoals aangegeven op de onderstaande afbeeldingen. Druk de LED's niet te ver naar beneden om schade aan de LED te voorkomen. Voorkom ook kortsluiting tussen de LED-pinnen en de SMD-sockets door de LED niet volledig naar de printplaat te buigen zoals weergegeven op de onderstaande afbeeldingen.

![oriëntatie van de WS2812 LED's](ws2812_1.jpg)
![LED's buigen](ws2812_2.jpg)

### Condensatoren

Om de totale hoogte van het toetsenbord te verminderen, moet je de condensator buigen voordat je hem soldeert.

![condensatoren](capacitors.jpg)

### Encoder

Als je een draaischakelaar wilt, plaats deze dan in de linkerbovenhoek van de toetsenmatrix en soldeer de 7 pinnen (5 kleinere en 2 grotere). De grotere pinnen, die voor mechanische sterkte worden gebruikt, kunnen veel soldeer nodig hebben om de gaten te vullen.

![encoder gemonteerd](encoder.jpg)

### Schakelaars

`PLAATS AFBEELDING MET DE PLEXI-PLAAT`

### Behuizing

Schroeven? Afstandhouders? Plexi?

### Keycaps

Klik de keycaps van jouw keuze erop.

![keycaps gemonteerd](keycaps.jpg)

## N-key rollover

Een toetsenbord met n-key rollover, of afgekort NKRO, heeft de mogelijkheid om elke toets afzonderlijk te scannen, in plaats van dat de pc dit doet. Hierdoor wordt elke ingedrukte toets geregistreerd, zelfs als je meerdere toetsen tegelijkertijd indrukt.

Soms zie je het "n" in n-key rollover vervangen door een getal. Dat getal vertelt je hoeveel toetsen je tegelijkertijd kunt indrukken terwijl het toetsenbord deze registreert. Bijvoorbeeld, als je toetsenbord 6-key rollover heeft, kun je zes toetsen tegelijk indrukken met succesvolle invoer. N-key rollover is vooral relevant/nuttig voor gaming toetsenborden.

Niet alle toetsenborden hebben n-key rollover, omdat het implementeren van deze functie bepaalde kosten en ontwerpuitdagingen met zich meebrengt.

Om n-key rollover op deze macropad mogelijk te maken, breek je de 2 bovenste hoeken af om de kortsluiting te verbreken en gebruik je de diodes.

## Firmware

`PLAATS INFO`
