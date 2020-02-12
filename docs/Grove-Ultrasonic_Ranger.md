---
category: Sensor
bzurl: https://www.seeedstudio.com/Grove-Ultrasonic-Ranger-p-960.html
oldwikiname: Grove - Ultrasonic Ranger
prodimagename: 350px-Ultrasonic_Ranger.jpg
surveyurl: https://www.research.net/r/Grove-Ultrasonic-Ranger
sku: 101020010
tags: io_3v3, io_5v, plat_duino, plat_pi
---

![](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/Ultrasonic.jpg)

Ultrazvukový měřič vzdálenosti (Grove - Ultrasonic ranger) slouží k bezkontaktnímu měření vzdálenosti od překážky. Používá ultrazvuk o frekvenci 40 kHz. Když do měřiče pošleme signál, dlouhý alespoň 10 µS, spustí se měření, během níž modul vyšle osm ultrazvukových vln a snaží se zachytit ozvěnu, tedy zvuk, odražený od překážky. Po tu dobu drží svůj výstup v úrovni HIGH, jakmile signál dorazí, změní se na LOW. Délka pulsu odpovídá zpoždění zvuku, a to je přímo úměrné vzdálenosti od překážky. Vzorec pro výpočet je jednoduchý: Vzdálenost = délka pulsu x rychlost zvuku / 2. 

Tento modul používá signálový pin SIG jako vstup i výstup.

!!!Upozornění
Grove-Ultrasonic-Ranger připojujte a odpojujte pouze k vypnutému zařízení, jinak hrozí nebezpečí zničení. Měření musí probíhat v prostoru větším než 0,5 m^2^ a bez výrazných hran.

<p style=":center"><a href="https://www.seeedstudio.com/Grove-Ultrasonic-Ranger-p-960.html" target="_blank"><img src="https://raw.githubusercontent.com/SeeedDocument/Seeed-WiKi/master/docs/images/get_one_now_small.png" width="210" height="41"  border=0 /></a></p>

## Verze

| Verze produktu               | Změny                                                                                                                                     | Datum vydání |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ |
| Grove-Ultrasonic ranger V1.0 | První vydání                                                                                                                              | Mar 2012     |
| Grove-Ultrasonic ranger V2.0 | Zlepšení stability napájecího napětí následujícími kroky: 1. Přidán kondenzátor C14 2. Vyčištění návrhu 3. Kompatibilita s napájením 3.3V | July 2017    |

## Specifikace

| Parametr         | Hodnota / Rozsah   |
| :--------------- | :----------------- |
| Pracovní napětí  | 3.2~5.2V           |
| Pracovní proud   | 8mA                |
| Frekvence zvuku  | 40kHz              |
| Rozsah měření    | 2-350cm            |
| Rozlišení        | 1cm                |
| Výstup           | PWM                |
| Velikost         | 50mm X 25mm X 16mm |
| Hmotnost         | 13g                |
| Úhel měření      | 15°                |
| Pracovní teplota | -10~60 °C          |
| Spouštěcí signál | 10 µS TTL          |
| Výstup           | TTL                |

!!!Tip
Více detailů o modulech Grove zjistíte v [popisu systému Grove](http://wiki.seeedstudio.com/Grove_System/)

## Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                               | BeagleBone                                                                                          | Wio                                                                                               | LinkIt ONE                                                                                             |
| ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Začínáme

!!!Poznámka
Pokud se s Arduinem setkáváte poprvé, doporučujeme vám pročíst návod [Začínáme s Arduinem](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) dřív, než začnete.

### Pokusy s Arduinem

#### Hardware

- **Krok 1.** Připravte si tyto součástky:

| Seeeduino V4.2                                                                                                             | Base Shield                                                                                                                | Grove - Ultrasonic Ranger                                                                                                     |
| -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/Ultrasonic_small.jpg) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                            | [Koupit](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                           | [Koupit](https://www.seeedstudio.com/Grove-Ultrasonic-Ranger-p-960.html)                                                      |

- **Krok 2.** Připojte Ultrasonic Ranger k portu D7 na Grove-Base Shieldu.
- **Krok 3.** Připojte Base Shield k Seeeduinu.
- **Krok 4.** Připojte Seeduino k PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/arduino%20connection.jpg)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit Grove_Ultrasonic_Ranger k Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino   | Grove-Ultrasonic Ranger |
| ----------- | ----------------------- |
| 5V          | Červený                 |
| GND         | Černý                   |
| Nepřipojeno | Bílý                    |
| D7          | Žlutý                   |

#### Software

- **Krok 1.** Stáhněte si knihovnu [ UltrasonicRanger Library](https://github.com/Seeed-Studio/Grove_Ultrasonic_Ranger/archive/master.zip) z GitHubu.
- **Krok 2.** S instalací knihovny pro Arduino vám pomůže návod [Jak instalovat knihovnu pro Arduino](http://wiki.seeedstudio.com/How_to_install_Arduino_Library).
- **Krok 3.** Zkopírujte kód do Arduino IDE, přeložte a nahrajte do Arduina. Pokud si nejste jisti, jak nahrát kód, podívejte se na stránku [Jak nahrát kód](http://wiki.seeedstudio.com/Upload_Code/).

```
#include "Ultrasonic.h"

Ultrasonic ultrasonic(7);
void setup()
{
	Serial.begin(9600);
}
void loop()
{
	long RangeInInches;
	long RangeInCentimeters;

	Serial.println("The distance to obstacles in front is: ");
	RangeInInches = ultrasonic.MeasureInInches();
	Serial.print(RangeInInches);//0~157 inches
	Serial.println(" inch");
	delay(250);

	RangeInCentimeters = ultrasonic.MeasureInCentimeters(); // two measurements should keep an interval
	Serial.print(RangeInCentimeters);//0~400cm
	Serial.println(" cm");
	delay(250);
}
```

- **Krok 4.** V terminálu uvidíte naměřené vzdálenosti.

```
The distance to obstacles in front is:
2 inches
6 cm
The distance to obstacles in front is:
2 inches
6 cm
The distance to obstacles in front is:
2 inches
6 cm
```

### Pokusy s Codecraftem

#### Hardware

**Krok 1.** Připojte Grove - Ultrasonic Ranger k portu D7 na Grove-Base Shieldu

**Krok 2.** Připojte Base Shield k Seeeduinu / Arduinu.

**Krok 3.** Propojte Seeeduino/Arduino s PC pomocí kabelu USB.

#### Software

**Krok 1.** Spusťte [Codecraft](https://ide.chmakered.com/), přepněte se na prostředí pro Arduino a přidejte na plochu hlavní proceduru (Start).

!!!Poznámka
Pokud používáte Codecraft poprvé, podívejte se na [Průvodce světem Codecraftu a Arduina](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Krok 2.** Přetáhněte bloky tak, jak ukazuje následující obrázek, nebo otevřte cdc soubor, který si můžete stáhnout na konci této stránky.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove_Ultrasonic_Ranger/master/img/cc_Ultrasonic_Ranger.png)

Nahrajte hotový program do svého Arduina/Seeeduina.

!!!Povedlo se
Jakmile je nahrávání hotové, v terminálu uvidíte naměřené vzdálenosti.

### Pokusy s Raspberry Pi (s Grove Base Hat)

#### Hardware

- **Krok 1**. Součástky, použité v tomto projektu:

| Raspberry pi                                                                                                   | Grove Base Hat for RasPi                                                                                                       | Grove - Ultrasonic Ranger                                                                                                     |
| -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/Ultrasonic_small.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)                                              | [Koupit](https://www.seeedstudio.com/Grove-Ultrasonic-Ranger-p-960.html)                                                      |

- **Krok 2**. Připojte Grove Base Hat k Raspberry Pi.
- **Krok 3**. Připojte Grove - Ultrasonic Ranger k portu D5 of the Base Hat.
- **Krok 4**. Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/connect2.jpg)

!!! Poznámka
V kroku 3 můžete připojit the ultrasonic ranger k **libovolnému GPIO portu**, ale ujistěte se, že jste změnili i číslo portu v kódu ukázky.

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
python grove_ultrasonic_ranger.py 5 6

```

Toto je kód v souboru grove_ultrasonic_ranger.py.

```python

import sys
import time
from grove.gpio import GPIO

usleep = lambda x: time.sleep(x / 1000000.0)

_TIMEOUT1 = 1000
_TIMEOUT2 = 10000

class GroveUltrasonicRanger(object):
    def __init__(self, pin):
        self.dio =GPIO(pin)

    def _get_distance(self):
        self.dio.dir(GPIO.OUT)
        self.dio.write(0)
        usleep(2)
        self.dio.write(1)
        usleep(10)
        self.dio.write(0)

        self.dio.dir(GPIO.IN)

        t0 = time.time()
        count = 0
        while count < _TIMEOUT1:
            if self.dio.read():
                break
            count += 1
        if count >= _TIMEOUT1:
            return None

        t1 = time.time()
        count = 0
        while count < _TIMEOUT2:
            if not self.dio.read():
                break
            count += 1
        if count >= _TIMEOUT2:
            return None

        t2 = time.time()

        dt = int((t1 - t0) * 1000000)
        if dt > 530:
            return None

        distance = ((t2 - t1) * 1000000 / 29 / 2)    # cm

        return distance

    def get_distance(self):
        while True:
            dist = self._get_distance()
            if dist:
                return dist


Grove = GroveUltrasonicRanger


def main():
    if len(sys.argv) < 2:
        print('Usage: {} pin_number'.format(sys.argv[0]))
        sys.exit(1)

    sonar = GroveUltrasonicRanger(int(sys.argv[1]))

    print('Detecting distance...')
    while True:
        print('{} cm'.format(sonar.get_distance()))
        time.sleep(1)

if __name__ == '__main__':
    main()



```

!!!Povedlo se
Pokud vše šlo tak, jak má, uvidíte výsledek podobný tomuto

```python

pi@raspberrypi:~/grove.py/grove $ python grove_ultrasonic_ranger.py 5 6
Detecting distance...
121.757901948 cm
246.894770655 cm
2.60205104433 cm
0.205533257846 cm
0.657706425108 cm
247.433267791 cm
122.485489681 cm
^CTraceback (most recent call last):
  File "grove_ultrasonic_ranger.py", line 110, in <module>
    main()
  File "grove_ultrasonic_ranger.py", line 107, in main
    time.sleep(1)
KeyboardInterrupt


```

Program ukončíte stiskem ++ctrl+c++.

### Pokusy s Raspberry Pi (s modulem GrovePi_Plus)

#### Hardware

- **Krok 1.** Připravte si tyto součástky:

| Raspberry pi                                                                                                      | GrovePi_Plus                                                                                                            | Grove - Ultrasonic Ranger                                                                                                     |
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/Grovepi%2B.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/Ultrasonic_small.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                          | [Koupit](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)                                                            | [Koupit](https://www.seeedstudio.com/Grove-Ultrasonic-Ranger-p-960.html)                                                      |

- **Krok 2.** Připojte GrovePi_Plus k Raspberry Pi.
- **Krok 3.** Připojte Grove-Ultrasonic ranger k portu **D4** na GrovePi_Plus.
- **Krok 4.** Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/pi%20connection.jpg)

#### Software

- **Krok 1.** Nastavte si vývojové prostředí pomocí průvodce [nastavení software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/).
- **Krok 2.** Stáhněte si zdrojový kód tím, že naklonujete knihovnu GrovePi.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

- **Krok 3.** Spusťte následující příkazy.

```
cd ~/GrovePi/Software/Python
python grove_ultrasonic.py
```

Toto je kód v souboru grove_ultrasonic.py.

```python
# GrovePi + Grove Ultrasonic Ranger

from grovepi import *

# Připojte Grove Ultrasonic Ranger to digital port D4
# SIG,NC,VCC,GND

ultrasonic_ranger = 4

while True:
    try:
        # Read distance value from Ultrasonic
        print ultrasonicRead(ultrasonic_ranger)

    except TypeError:
        print "Error"
    except IOError:
        print "Error"
```

- **Krok 4.** V terminálu uvidíte naměřené vzdálenosti.

```
pi@raspberrypi:~/GrovePi/Software/Python $ python grove_ultrasonic.py
9
9
9
9
9
9
9
9
9
9
9

```

## FAQ - Často kladené dotazy

**Ot. 1: Jak modul funguje?**

- Odp. 1: Když do měřiče pošleme signál, dlouhý alespoň 10 µS, spustí se měření, během níž modul vyšle osm ultrazvukových vln a snaží se zachytit ozvěnu, tedy zvuk, odražený od překážky. Po tu dobu drží svůj výstup v úrovni HIGH, jakmile signál dorazí, změní se na LOW. Délka pulsu odpovídá zpoždění zvuku, a to je přímo úměrné vzdálenosti od překážky. Vzorec pro výpočet je jednoduchý: Vzdálenost = délka pulsu x rychlost zvuku / 2. 

**Ot. 2: Proč má tento modul, na rozdíl od jiných podobných, pouze jeden vývod a ne dva?**

- Odp. 2: Tento modul používá signálový pin SIG jako vstup i výstup.

**Ot. 3: Narazil jsem na technické problémy, kam se mám obrátit?**

- Odp. 3: Napište nám na techsupport@seeed.cc

**Ot. 4: Mohu připojit více těchto modulů k jednomu Arduinu?**

- Odp. 4: Ano, zde je ukázka připojení dvou snímačů, jednoho na D2, druhého na D3.

```c++
#include "Ultrasonic.h"

Ultrasonic ultrasonic1(2);
Ultrasonic ultrasonic2(3);
void setup()
{
    Serial.begin(9600);
}
void loop()
{
    long RangeInCentimeters1;
    long RangeInCentimeters2;

    RangeInCentimeters1 = ultrasonic1.MeasureInCentimeters(); // two measurements should keep an interval
    Serial.print(RangeInCentimeters1);//0~400cm
    Serial.println(" cm");

    RangeInCentimeters2 = ultrasonic2.MeasureInCentimeters(); // two measurements should keep an interval
    Serial.print(RangeInCentimeters2);//0~400cm
    Serial.println(" cm");

    delay(250);
}

```

## Zdroje

- **[PDF]** [Download Wiki PDF](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/res/Grove-Ultrasonic_Ranger_WiKi.pdf)
- **[PDF]** [Grove_Ultrasonic Ranger Schematic](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/res/Grove_Ultrasonic%20Ranger%20Schematic.pdf)
- **[PDF]** [Ceramic Ultrasonic Sensor NU40C16T/R-1](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/blob/master/res/NU40C16T-R-1.pdf)
- **[Knihovna]** [Grove_Ultrasonic Ranger library](https://github.com/Seeed-Studio/Grove_Ultrasonic_Ranger/archive/master.zip)
- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove_Ultrasonic_Ranger/master/res/Grove_Ultrasonic_Ranger_CDC_File.zip)
- **[Project]** [The Color Helix](https://community.seeedstudio.com/project_detail.html?id=138)
- **[Project]** [Indoor Lightning Cloud](https://community.seeedstudio.com/project_detail.html?id=182)
- **[Project]** [Automatic Water Level Controller](https://community.seeedstudio.com/project_detail.html?id=241)
- **[Example]** [Example_Measure_distance_and_led_display](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/res/Example_Measure_distance_and_led_display.zip)
- **[Example]** [Example_Measure_and_display_the_distance](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/res/Example_Measure_and_display_the_distance.zip)

## Projekt

**Osvětlení schodů v novém sídle Seeed**: V novém sídle jsme si proměnili schody v interaktivní instalaci. Zároveň tím sdělujeme návštěvám, že sem smí jen zaměstnanci.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/stairs-hackers/hacking-the-stairs-at-seeed-s-new-office-9ef30b/embed' width='350'></iframe>

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
