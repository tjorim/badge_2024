download de [Arduino IDE van hun website](https://www.arduino.cc/en/software)

# Arduino IDE installatie
Om de Fri3d badge te gebruiken in de Arduino IDE moret je versie `2.0.17` van de ESP32 board package installeren. hieronder de instructies

## General Arduino IDE Setup
- In de Arduino IDE klik je op het `Tools` menu, selecteer `Boards` vervolgens `Boards Manager`. Installeer  **versie 2.0.17** van het ESP32 packet.
  - de reden dat we versie `2.0.17` adviseren is omdat ver `3.0.2` compilatie fouten geeft voor de ESP32S3 module.
- In het `Tools` menu, selecteer `Board` -> `esp32` -> `ESP32S3 Dev Module`

## Hoe uploaden in Arduino IDE
- Zet je badge aan
- Connecteer de badge via USB aan je computer
- In het `Tools` menu selecteer je `Port` en kies je degene die het mest lijkt op de badge uit de lijst.
- Klik op de Upload knop (rechts wijzenden groene pijl)