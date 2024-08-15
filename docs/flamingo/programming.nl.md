# Programmeren van de LANA Module
Om de blaster (flamingo) te programmeren, kunt u gebruik maken van [Embeetle IDE](https://embeetle.com/) of [Mounriver Studio](http://www.mounriver.com/).

# Embeetle
Een beter alternatief is [Embeetle](https://embeetle.com/). Dit is een IDE van Belgische makelij. Dit is niet open source maar gebruikt wel een open toolchain bij het aanmaken van een nieuw project.

[LANA](https://phyx.be/LANA_TNY/) kan geprogrammeerd worden met [Embeetle](https://embeetle.com/) via de USB-aansluiting maar ook met de [WCH-Link debugger](https://www.wch-ic.com/products/WCH-Link.html), dit biedt extra debugopties.

De makers van [Embeetle](https://embeetle.com/) zijn ook zo vriendelijk geweest om het LANA-bord en zeer mooie documentatie toe te voegen (https://embeetle.com/#supported-hardware/wch/boards/lana-tny-01).

&nbsp;<br>
## STAP 1: Download Embeetle IDE
Download eerst Embeetle op [https://embeetle.com/downloads](https://embeetle.com/#embeetle-ide/download). U kunt het downloaden voor Windows of Linux.

<img src="https://github.com/user-attachments/assets/59498d20-e134-4101-98d4-90c1bf618ca1" width="400">

&nbsp;<br>
## STAP 2: Start het `lana-tny-01-blaster-2024` project
Als Belgisch bedrijf hebben we besloten het `lana-tny-01-blaster-2024` project voor onze Belgische vrienden op de Embeetle server te zetten! Start Embeetle en klik op 'CREATE PROJECT':

<img src="https://github.com/user-attachments/assets/8d881776-0d6e-4dac-a253-c3d7d610ed76" width="600">

Selecteer vervolgens `WCH` als de leverancier (dat is de leverancier van de microcontroller) en zoek naar het project `lana-tny-01-blaster-2024`:

<img src="https://github.com/user-attachments/assets/a00f00fb-5c35-4ee6-9703-bc0f17b03a32" width="600">

Klik nu op `CREATE` onderaan. Embeetle IDE zal automatisch het voorbeeldproject en alle benodigde tools downloaden. Vervolgens opent Embeetle het project:

<img src="https://github.com/user-attachments/assets/caac076a-4451-4286-8899-637ecab647cd">

&nbsp;<br>
## STAP 3: Flash de firmware
Klik nu op de `flash` knop bovenaan. U kunt nu de volgende fout ervaren:
<pre>
Failed to open USB device: Bus 001 Device 008: ID 4348:55e0
Error: Failed to open USB device on Windows
</pre>
Op Linux kunt u een ander probleem ervaren:
<pre>
Failed to open USB device: Bus 003 Device 010: ID 4348:55e0
Error: Failed to open USB device on Linux due to no enough permission
</pre>
Laten we dit oplossen.

&nbsp;<br>
## STAP 4a: Installeer Zadig (alleen Windows)
U moet [Zadig](https://zadig.akeo.ie/) installeren en de driver voor het USB-apparaat vervangen door de WinUSB-driver. Download eerst Zadig:

<img src="https://github.com/user-attachments/assets/d537fe6a-de71-48dd-9269-857ddcadfe81" width="600">

Open vervolgens Zadig en selecteer Opties -> Lijst met alle apparaten:

<img src="https://github.com/user-attachments/assets/7000ec9f-a97e-4c05-a57d-42b7e0265a69" width="600">

Selecteer USB Module uit de lijst van apparaten en kies WinUSB als de driver. Klik vervolgens op Driver vervangen:

<img src="https://github.com/user-attachments/assets/c5cb00ea-d307-4fd1-a668-03270ae98f34" width="600">

Wacht tot de installatie van de driver is voltooid:

<img src="https://github.com/user-attachments/assets/b55a5996-c4af-4f2c-ac66-8b4f59a05aed" width="600">

Succes:

<img src="https://github.com/user-attachments/assets/4afdf22e-804a-4845-92a7-93bcdd6be906" width="600">

Probeer het opnieuw in Embeetle IDE. Het zou nu moeten werken:
```
"C:/Users/krist/EMBEETLE IDE/embeetle/beetle_tools/windows/wchisp_0.2.2_64b/wchisp.exe" flash application.elf
14:57:06 [INFO] Chip: CH32V203G6U6[0x3619] (Code Flash: 32KiB)
14:57:06 [INFO] Chip UID: CD-AB-19-97-D0-BC-B6-FF
14:57:06 [INFO] BTVER(bootloader ver): 02.70
14:57:06 [INFO] Code Flash protected: false
14:57:06 [INFO] Current config registers: a55aff0000ff00ffffffffff00020700cdab1997d0bcb6ff
RDPR_USER: 0x00FF5AA5
  [7:0]   RDPR 0xA5 (0b10100101)
    `- Unprotected
  [16:16] IWDG_SW 0x1 (0b1)
    `- IWDG enabled by the software, and disabled by hardware
  [17:17] STOP_RST 0x1 (0b1)
    `- Disable
  [18:18] STANDBY_RST 0x1 (0b1)
    `- Disable, entering standby-mode without RST
  [23:22] SRAM_CODE_MODE 0x3 (0b11)
    `- CODE-228KB + RAM-32KB / CODE-160KB + RAM-32KB depending on the chip
DATA: 0xFF00FF00
  [7:0]   DATA0 0x0 (0b0)
  [23:16] DATA1 0x0 (0b0)
WRP: 0xFFFFFFFF
  `- Unprotected
14:57:06 [INFO] Read application.elf as ELF format
14:57:06 [INFO] Found loadable segment, physical address: 0x00000000, virtual address: 0x00000000, flags: 0x5
14:57:06 [INFO] Section names: [".init", ".vector", ".text"]
14:57:06 [INFO] Found loadable segment, physical address: 0x00000dbc, virtual address: 0x20000000, flags: 0x6
14:57:06 [INFO] Section names: [".data"]
14:57:06 [INFO] Firmware size: 4096
14:57:06 [INFO] Erasing...
14:57:06 [WARN] erase_code: set min number of erased sectors to 8
14:57:06 [INFO] Erased 8 code flash sectors
14:57:07 [INFO] Erase done
14:57:07 [INFO] Writing to code flash...
██████████████████████████████████████ 4096/409614:57:07 [INFO] Code flash 4096 bytes written
14:57:08 [INFO] Verifying...
██████████████████████████████████████ 4096/409614:57:08 [INFO] Verify OK
14:57:08 [INFO] Now reset device and skip any communication errors
14:57:08 [INFO] Device reset
```


## STAP 4b: Voeg het apparaat toe aan de plugdev groep (alleen Linux)
Op Linux moet je het apparaat toevoegen aan de plugdev groep. Je kunt de documentatie hier vinden:
https://embeetle.com/#supported-hardware/wch/boards/lana-tny-01 > 3.Installatie > 3.1 Firmware flashen via USB-C poort > Linux

Stuur me een WhatsApp-bericht als het niet werkt:
+32 496 90 75 44


## WCH Official Tools
[Mounriver](http://www.mounriver.com/) is een IDE gebaseerd op Eclipse, uitgebracht door de chipfabrikant WCH. Dit werkt op Windows en er is een versie voor Linux en mogelijk ook voor Mac, maar de laatste twee lopen wat achter. [Mounriver](http://www.mounriver.com/) geeft ook valse virusmeldingen op veel systemen en schendt de GPL-licentievoorwaarden van Eclipse.

## Opmerking specifiek voor de LANA module
Als je zelf aan de slag gaat met de blaster/LANA TNY dan moet je op 1 ding letten (onafhankelijk van de IDE) en dat is dat LANA geen externe klok heeft en de interne klok (HSI) moet gebruiken, dit staat ook zo in de standaard sketch van [Embeetle](https://embeetle.com/).
Als je per ongeluk je [LANA](https://phyx.be/LANA_TNY/) bordje "bricked" kan je die meestal unbricken via USB of door de power reset feature te gebruiken van de [WCHISPTool](https://www.wch-ic.com/downloads/WCHISPTool_Setup_exe.html).
