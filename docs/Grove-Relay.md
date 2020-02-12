---
name: Grove - Relay
category: Actuator
bzurl: https://www.seeedstudio.com/Grove-Relay-p-769.html
oldwikiname:
prodimagename: Twig-Relay.jpg
surveyurl: https://www.surveymonkey.com/r/Grove_Relay
sku: 103020005
tags: io_3v3, io_5v, plat_duino, plat_linkit, plat_bbg, plat_pi,plat_wio
---

<p style=":center"><img src="https://raw.githubusercontent.com/SeeedDocument/Grove-Relay/master/img/Twig-Relay.jpg" /></p>

Relé je elektricky ovládaný spínač. Díky němu můžete spínat vysoké napětí i velké proudy relativně malým napětím, i pěti volty z mikrokontroléru. Za normálního stavu jsou jeho kontakty rozpojené. Na desce je integrovaná LED, která ukazuje, jestli je relé sepnuté.

<iframe width="800" height="450" src="https://www.youtube.com/embed/MwLEawbP0ZU" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<p style=":center"><a href="https://www.seeedstudio.com/Grove-Relay-p-769.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/300px-Get_One_Now_Banner-ragular.png" /></a></p>

## Verze

| Parametr                 | V1.1          | V1.2          |
| :----------------------- | :------------ | :------------ |
| Zahájení výroby          | 27th Jan 2013 | 9th June 2014 |
| Pracovní napětí          | 5V            | 3.3V~5V       |
| Pracovní proud           | 60mA          | 100mA         |
| Životnost                | 100,000 cyklů | 100,000 cyklů |
| Maximální spínané napětí | 250VAC/30VDC  | 250VAC/30VDC  |
| Maximální spínaný proud  | 5A            | 5A            |

!!!Tip
Více detailů o modulech Grove zjistíte v [popisu systému Grove](http://wiki.seeedstudio.com/Grove_System/)

## Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                               | BeagleBone                                                                                        | Wio                                                                                               | LinkIt ONE                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Začínáme

### Pokusy s Arduinem

!!!Poznámka
Pokud se s Arduinem setkáváte poprvé, doporučujeme vám pročíst návod [Začínáme s Arduinem](http://wiki.seeedstudio.com/_with_Arduino/) dřív, než začnete.

#### Potřebné součástky

| Seeeduino V4.2                                                                                                             | Base Shield                                                                                                                | Grove-Button **x2**                                                                                       | Grove-Relay                                                                             |
| -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Relay/raw/master/img/button_s.jpg) | ![](https://github.com/SeeedDocument/Grove-Relay/raw/master/img/Thumbnail.jpg)          |
| <a href="http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html" target="_blank">Koupit</a>                                 | <a href="https://www.seeedstudio.com/Base-Shield-V2-p-1378.html" target="_blank">Koupit</a>                                | <a href="https://www.seeedstudio.com/Grove-Button-p-766.html" target="_blank">Koupit</a>                  | <a href="https://www.seeedstudio.com/Grove-Relay-p-769.html" target="_blank">Koupit</a> |

!!!Poznámka
**1** Buďte opatrní při připojování USB kabelu, můžete poškodit konektor. Používejte datové kabely (se čtyřmi vodiči), ne napájecí (se dvěma vodiči). Pokud si nejste jisti, jaký USB kabel máte, můžete si [u nás koupit doporučený](https://www.seeedstudio.com/Micro-USB-Cable-48cm-p-1475.html)

**2** Všechny Grove moduly jsou prodávány s propojovacím kabelem Grove. Pokud jej ztratíte, můžete si [u nás koupit náhradní Grove kabel](https://www.seeedstudio.com/Grove-Universal-4-Pin-Buckled-20cm-Cable-%285-PCs-pack%29-p-936.html).

#### Hardware

- **Krok 1.** Připojte Grove-Relay k portu **D4** na Grove-Base Shieldu.

- **Krok 2.** Připojte Grove-Button#1 k portu **D2** na Grove-Base Shieldu. Poté připojte Grove-Button#2 k portu **D3** na Grove-Base Shieldu.

- **Krok 3.** Připojte Base Shield k Seeeduinu.

- **Krok 4.** Připojte Seeduino k PC pomocí kabelu USB.

![enter image description here](https://github.com/SeeedDocument/Grove-Relay/raw/master/img/button-relay.jpg)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit moduly k Seeduinu tak, jak je popsáno v následující tabulce:

| Grove-Relay | Arduino | Grove Cable |
| ----------- | ------- | ----------- |
| GND         | GND     | Černý       |
| VCC         | 5V      | Červený     |
| SIG         | D4      | Žlutý       |

| Grove-Button#1 | Arduino | Grove Cable |
| -------------- | ------- | ----------- |
| GND            | GND     | Černý       |
| VCC            | 5V      | Červený     |
| SIG            | D2      | Žlutý       |

| Grove-Button#2 | Arduino | Grove Cable |
| -------------- | ------- | ----------- |
| GND            | GND     | Černý       |
| VCC            | 5V      | Červený     |
| SIG            | D3      | Žlutý       |

#### Software

V následujícím příkladu si ukážeme, jak ovládat relé pomocí tlačítek. Jedním tlačítkem relé sepneme, druhým opět rozpojíme.

- **Krok 1.** Zkopírujte kód do Arduino IDE, přeložte a nahrajte do Arduina.

```
// Relay Control

void setup()
{
  pinMode(2, INPUT);
  pinMode(3, INPUT);
  pinMode(4, OUTPUT);
}

void loop()
{
  if (digitalRead(2)==HIGH)
  {
    digitalWrite(4, HIGH);
    delay(100);
  }
  if (digitalRead(3)==HIGH)
  {
    digitalWrite(4, LOW);
  }
}

```

- **Krok 2.** Nahrajte přeložený kód do Arduina. Pokud si nejste jisti, jak nahrát kód, podívejte se na stránku [Jak nahrát kód](http://wiki.seeedstudio.com/Upload_Code/).

Stiskem tlačítka 1 se relé sepne, stiskem tlačítka 2 vypne.

### Pokusy s Codecraftem

#### Hardware

**Krok 1.** Připojte Grove - Relay k portu D4 a dvě tlačítka Grove - Button k portům D2 a D3 na Grove-Base Shieldu

**Krok 2.** Připojte Base Shield k Seeeduinu / Arduinu.

**Krok 3.** Propojte Seeeduino/Arduino s PC pomocí kabelu USB.

#### Software

**Krok 1.** Spusťte [Codecraft](https://ide.chmakered.com/), přepněte se na prostředí pro Arduino a přidejte na plochu hlavní proceduru (Start).

!!!Poznámka
Pokud používáte Codecraft poprvé, podívejte se na [Průvodce světem Codecraftu a Arduina](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Krok 2.** Přetáhněte bloky tak, jak ukazuje následující obrázek, nebo otevřte cdc soubor, který si můžete stáhnout na konci této stránky.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove-Relay/master/img/cc_Relay.png)

Nahrajte hotový program do svého Arduina/Seeeduina.

!!!Povedlo se
Relé sepne stisknutím tlačítka, připojeného k portu D2, a vypne stisknutím tlačítka, připojeného k portu D3.

### Pokusy s Raspberry Pi (s Grove Base Hat)

#### Hardware

- **Krok 1**. Součástky, použité v tomto projektu:

| Raspberry pi                                                                                                   | Grove Base Hat for RasPi                                                                                                       | Grove - Relay                                                                                              |
| -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Relay/raw/master/img/Thumbnail.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)                                              | [Koupit](https://www.seeedstudio.com/Grove-Relay-p-769.html)                                               |

- **Krok 2**. Připojte Grove Base Hat k Raspberry Pi.
- **Krok 3**. Připojte Grove - Relay k portu 12 na Base Hatu.
- **Krok 4**. Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-Relay/raw/master/img/Relay_Hat.jpg)

!!! Poznámka
V kroku 3 můžete připojit the relay module k **libovolnému GPIO portu**, ale ujistěte se, že jste změnili i číslo portu v kódu ukázky.

#### Software

- **Krok 1**. Nastavte si vývojové prostředí pomocí průvodce [nastavení software](http://wiki.seeedstudio.com/Grove_Base_Hat_for_Raspberry_Pi/#installation).
- **Krok 2**. Stáhněte si zdrojový kód tím, že naklonujete knihovnu grove.py.

```
cd ~
git clone https://github.com/Seeed-Studio/grove.py

```

- **Krok 3**. Spusťte program pomocí následujících příkazů.

```
cd grove.py/grove
python grove_relay.py 12

```

Toto je kód v souboru grove_relay.py.

```python

from grove.gpio import GPIO


class GroveRelay(GPIO):
    def __init__(self, pin):
        super(GroveRelay, self).__init__(pin, GPIO.OUT)

    def on(self):
        self.write(1)

    def off(self):
        self.write(0)


Grove = GroveRelay


def main():
    import sys
    import time

    if len(sys.argv) < 2:
        print('Usage: {} pin'.format(sys.argv[0]))
        sys.exit(1)

    relay = GroveRelay(int(sys.argv[1]))

    while True:
        try:
            relay.on()
            time.sleep(1)
            relay.off()
            time.sleep(1)
        except KeyboardInterrupt:
            relay.off()
            print("exit")
            exit(1)

if __name__ == '__main__':
    main()



```

!!!Povedlo se
Pokud vše šlo tak, jak má, ullyšíte cvakání, jak relé spíná.

Program ukončíte stiskem ++ctrl+c++.

### Pokusy s Raspberry Pi (s modulem GrovePi_Plus)

#### Hardware

**Potřebné součástky**

| Raspberry pi                                                                                                      | GrovePi_Plus                                                                                                            | Grove-Button                                                                                              | Grove-Relay                                                                             |
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/Grovepi%2B.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Relay/raw/master/img/button_s.jpg) | ![](https://github.com/SeeedDocument/Grove-Relay/raw/master/img/Thumbnail.jpg)          |
| <a href="https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html" target="_blank">Koupit</a>               | <a href="https://www.seeedstudio.com/GrovePi%2B-p-2241.html" target="_blank">Koupit</a>                                 | <a href="https://www.seeedstudio.com/Grove-Button-p-766.html" target="_blank">Koupit</a>                  | <a href="https://www.seeedstudio.com/Grove-Relay-p-769.html" target="_blank">Koupit</a> |

- **Krok 1.** Připojte GrovePi_Plus k Raspberry Pi.

- **Krok 2.** Připojte Grove-Relay k portu **D4** na GrovePi_Plus.

- **Krok 3.** Připojte Grove-Button k portu **D3** na GrovePi_Plus.

- **Krok 4.** Připojte Raspberry to PC via USB cable.

![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Relay/master/img/GrovePiPlus_Grove_relay.jpeg)

#### Software

Pokud s GrovePi začínáte, postupujte krok po kroku a nejprve nainstalujte potřebný software. V případě, že již máte nainstalováno z předchozích pokusů, můžete kroky 1 a 2 přeskočit.

- **Krok 1.** Nastavte software pomocí následujících příkazů:

```
sudo curl -kL dexterindustries.com/update_grovepi | bash

```

```
sudo reboot
```

```
cd /home/pi/Desktop
```

```
git clone https://github.com/DexterInd/GrovePi.git
```

Podrobnější informace naleznete v případě potřeby v průvodci [nastavení software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/).

- **Krok 2.** Aktualizujte firmware pro GrovePi podle návodu [Updating the Firmware](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/updating-firmware/).

!!!Poznámka
Doporučujeme provést aktualizaci firmware, některé senzory bez ní mohou vykazovat chybné výsledky.

- **Krok 3.** Proveďte následující příkazy

```
cd /home/pi/Desktop/GrovePi/Software/Python/
sudo python grove_switch_relay.py
```

Pokud chcete vidět samotný program, použijte:

```
sudo nano grove_switch_relay.py

```

Zde je kód použitého programu:

```python
# Raspberry Pi + Grove Switch + Grove Relay

import time
import grovepi
# Připojte Grove Switch to digital port D3
# SIG,NC,VCC,GND

switch = 3
# Připojte Grove Relay to digital port D4
# SIG,NC,VCC,GND

relay = 4
grovepi.pinMode(switch,"INPUT")
grovepi.pinMode(relay,"OUTPUT")
while True:
    try:
        if grovepi.digitalRead(switch):
            grovepi.digitalWrite(relay,1)
        else:
            grovepi.digitalWrite(relay,0)
            time.sleep(.05)
    except KeyboardInterrupt:
        grovepi.digitalWrite(relay,0)
        break
    except IOError:
        print "Error"
```

### Pokusy s TI LaunchPad

Ovládání elektroniky přes relé.

![Relé a LaunchPad](https://raw.githubusercontent.com/SeeedDocument/Grove-Relay/master/img/Relay.jpg)

V tomto příkladu si ukážeme, jak použít Grove Realy k ovládání větší zátěže, třeba stolní lampičky. Třívoltový signál stačí k tomu, aby relé sepnulo napájecí napětí pro lampičku. **Při práci se síťovým napětím buďte opatrní!**

```
/*
Relay
The basic Energia example.
This example code is in the public domain.
*/

#define RELAY_PIN 39

// the setup routine runs once when you press reset:
void setup() {
         pinMode(RELAY_PIN, OUTPUT); // initialize the digital pin as an output.
}

// the loop routine runs over and over again forever:
void loop() {
         digitalWrite(RELAY_PIN, HIGH); // turn the relay on (HIGH is the voltage level)
         delay(1000);   // wait for a second
         digitalWrite(RELAY_PIN, LOW);   // turn the relay o by making the voltage LOW
         delay(1000);   // wait for a second
}
```

## Zdroje

- **[Eagle]** [Grove - Relay Schematic and PCB in Eagle format](https://raw.githubusercontent.com/SeeedDocument/Grove-Relay/master/res/Grove-Relay_Eagle_Files.zip)
- **[PDF]** [Grove - Relay PCB in PDF format](https://github.com/SeeedDocument/Grove-Relay/raw/master/res/Grove%20-%20Relay%20PCB.pdf)
- **[PDF]** [Grove - Relay Schematic in PDF format](https://github.com/SeeedDocument/Grove-Relay/raw/master/res/Grove%20-%20Relay%20Schematic.pdf)
- **[Datasheet]** [HLS8-T73 Series Relay Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Relay/master/res/Relay_Datasheet.pdf)
- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove-Relay/master/res/Grove_Relay_CDC_File.zip)

## Projekty

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;}
.tg .tg-yw4l{vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-031e"><iframe frameborder='0' height='327.5' scrolling='no' src='https://project.seeedstudio.com/sodaqmoja/using-a-switch-to-open-and-close-a-relay-3329ec/embed' width='350'></iframe></th>
    <th class="tg-031e"><iframe frameborder='0' height='327.5' scrolling='no' src='https://project.seeedstudio.com/rei-vilo/private-iot-with-blynk-on-local-server-619926/embed' width='350'></iframe></th>
    <th class="tg-yw4l"><iframe frameborder='0' height='327.5' scrolling='no' src='https://project.seeedstudio.com/josephroberts/resinified-office-lock-0ca2eb/embed' width='350'></iframe></th>
  </tr>
</table>

**Relay Grove module**:

<iframe width="560" height="315" src="https://www.youtube.com/embed/DnHqh_Rupb8" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/JOsjUOI9FU8" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
