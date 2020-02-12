---
name: Grove - Light Sensor
category: Sensor
bzurl: https://www.seeedstudio.com/Grove-Light-Sensor-(P)-v1.1-p-2693.html
oldwikiname: Grove_-_Light_Sensor
prodimagename: cover.jpg
sku: 101020173
tags: io_3v3, io_5v, plat_duino, plat_wio, plat_pi, plat_bbg, plat_linkit
---

![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/cover.jpg)

Tento snímač obsahuje fotorezistor – součástku, jejíž odpor je závislý na intenzitě světla. Čím vyšší intenzita světla, tím nižší odpor. Integrovaný operační zesilovač LM358 převádí odpor na napětí. Výsledkem je analogový signál, jehož napětí je tím vyšší, čím víc světla dopadá na čidlo.

Tento modul můžete například použít pro zapínání nočního osvětlení.

!!!Pozor
Světelný snímač ukazuje pouze orientační hodnotu osvětlení, neměří přesnou hodnotu v lumenech.

<p style=":center"><a href="https://www.seeedstudio.com/Grove-Light-Sensor-v1.2-p-2727.html" target="_blank"><img src="https://raw.githubusercontent.com/SeeedDocument/Seeed-WiKi/master/docs/images/get_one_now_small.png" width="210" height="41"  border=0 /></a></p>

## Verze

| Verze produktu               | Změny                                                                               | Datum vydání |
| ---------------------------- | ----------------------------------------------------------------------------------- | ------------ |
| Grove - Light Sensor 1.0     | První vydání                                                                        | Apr 28 2013  |
| Grove - Light Sensor(P)      | Přesunutí konektoru dozadu                                                          | May 15 2014  |
| Grove - Light Sensor(P) V1.1 | Změna fotorezistoru 5528 na model LS06-S u předchozí verze Grove - Light Sensor(P)  | Dec 31 2015  |
| Grove - Light Sensor 1.2     | Změna fotorezistoru 5528 na model LS06-S u předchozí verze Grove - Light Sensor 1.0 | Jan 20 2016  |

## Vlastnosti

- Analogový výstup
- Vysoká citlivost a spolehlivost
- Malé rozměry
- Široké spektrum citlivosti

!!!Tip
Více detailů o modulech Grove zjistíte v [popisu systému Grove](http://wiki.seeedstudio.com/Grove_System/)

### Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                               | BeagleBone                                                                                        | Wio                                                                                               | LinkIt ONE                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Specifikace

| Parametr                           | Hodnota  |
| ---------------------------------- | -------- |
| Pracovní napětí                    | 3~5V     |
| Pracovní proud                     | 0.5~3 mA |
| Rychlost reakce                    | 20-30 ms |
| Vlnová délka s nejvyšší citlivostí | 540 nm   |
| Hmotnost                           | 4 g      |

## Začínáme

### Pokusy s Arduinem

#### Hardware

- Krok 1: Připravte si tyto součástky:

| Seeeduino V4                                                                                                               | Base Shield                                                                                                                | Grove - Light Sensor                                                                                                   | Grove - LED Bar                                                                                                            |
| -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/img/light_sensor_s.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_3.jpg) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                            | [Koupit](http://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                            | [Koupit](https://www.seeedstudio.com/Grove-Light-Sensor-v1.2-p-2727.html)                                              | [Koupit](http://www.seeedstudio.com/Grove-LED-Bar-v2.0-p-2474.html)                                                        |

- Krok 2: Připojte Grove-Light Sensor k portu A0 na Grove-Base Shieldu.
- Krok 3: Připojte Grove-Led Bar k portu D2 na Grove-Base Shieldu.
- Krok 4: Připojte Base Shield k Seeeduinu.
- Krok 5: Připojte Seeduino k PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/img/seeeduino_light.jpg)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit Grove-Light Sensor k Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino   | Grove-Light Sensor |
| ----------- | ------------------ |
| 5V          | Červený            |
| GND         | Černý              |
| Nepřipojeno | Bílý               |
| A0          | Žlutý              |

| Seeeduino | Grove-Led Bar |
| --------- | ------------- |
| 5V        | Červený       |
| GND       | Černý         |
| D3        | Bílý          |
| D2        | Žlutý         |

#### Software

- Krok 1: Stáhněte si knihovnu [ Grove-LED Bar Library](https://github.com/Seeed-Studio/Grove_LED_Bar/archive/master.zip) z GitHubu.
- Krok 2: S instalací knihovny pro Arduino vám pomůže návod [Jak instalovat knihovnu pro Arduino](http://wiki.seeedstudio.com/How_to_install_Arduino_Library).
- Krok 3: Zkopírujte kód do Arduino IDE a nahrajte jej

```c

#include <Grove_LED_Bar.h>

Grove_LED_Bar bar(3, 2, 0);  // Clock pin, Data pin, Orientation

void setup()
{
  // nothing to initialize
  bar.begin();
  bar.setGreenToRed(true);
}

void loop()
{

  int value = analogRead(A0);
  value = map(value, 0, 800, 0, 10);

  bar.setLevel(value);
  delay(100);
}
```

- Krok 2: LED Bargraf ukazuje úroveň osvětlení

### Pokusy s Codecraftem

#### Hardware

**Krok 1.** Připojte Grove - Light Sensor k portu A0 na Grove-Base Shieldu

**Krok 2.** Připojte Base Shield k Seeeduinu / Arduinu.

**Krok 3.** Propojte Seeeduino/Arduino s PC pomocí kabelu USB.

#### Software

**Krok 1.** Spusťte [Codecraft](https://ide.chmakered.com/), přepněte se na prostředí pro Arduino a přidejte na plochu hlavní proceduru (Start).

!!!Poznámka
Pokud používáte Codecraft poprvé, podívejte se na [Průvodce světem Codecraftu a Arduina](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Krok 2.** Přetáhněte bloky tak, jak ukazuje následující obrázek, nebo otevřte cdc soubor, který si můžete stáhnout na konci této stránky.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/img/cc_Light_Sensor.png)

Nahrajte hotový program do svého Arduina/Seeeduina.

!!!Povedlo se
Jakmile je nahrávání hotové, uvidíte orientační intenzitu osvětlení v Sériovém monitoru.

### Pokusy s Raspberry Pi (s Grove Base Hat)

#### Hardware

- **Krok 1**. Součástky, použité v tomto projektu:

| Raspberry pi                                                                                                   | Grove Base Hat for RasPi                                                                                                       | Grove - Light Sensor                                                                                                   |
| -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/img/light_sensor_s.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)                                              | [Koupit](https://www.seeedstudio.com/Grove-Light-Sensor-v1.2-p-2727.html)                                              |

- **Krok 2**. Připojte Grove Base Hat k Raspberry Pi.
- **Krok 3**. Připojte light sensor k portu A0 na Base Hatu.
- **Krok 4**. Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/img/Light_Hat.jpg)

!!! Poznámka
V kroku 3 můžete připojit světelný snímač k **libovolnému analogovému portu**, ale nezapomeňte změnit příslušnou hodnotu v kódu.

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
python grove_light_sensor_v1_2.py 0

```

Toto je kód v souboru grove_light_sensor_v1_2.py.

```python

import math
import sys
import time
from grove.adc import ADC


class GroveLightSensor:

    def __init__(self, channel):
        self.channel = channel
        self.adc = ADC()

    @property
    def light(self):
        value = self.adc.read(self.channel)
        return value

Grove = GroveLightSensor


def main():
    if len(sys.argv) < 2:
        print('Usage: {} adc_channel'.format(sys.argv[0]))
        sys.exit(1)

    sensor = GroveLightSensor(int(sys.argv[1]))

    print('Detecting light...')
    while True:
        print('Light value: {0}'.format(sensor.light))
        time.sleep(1)

if __name__ == '__main__':
    main()

```

!!!Povedlo se
Pokud vše šlo tak, jak má, uvidíte výsledek podobný tomuto, s údaji, které odpovídají množství světla

```python

pi@raspberrypi:~/grove.py/grove $ python grove_light_sensor_v1_2.py 0
Detecting light...
Light value: 600
Light value: 448
Light value: 267
Light value: 311
Light value: 102
Light value: 82
Light value: 63
Light value: 54
Light value: 49
Light value: 45
Light value: 545
^CTraceback (most recent call last):
  File "grove_light_sensor_v1_2.py", line 67, in <module>
    main()
  File "grove_light_sensor_v1_2.py", line 64, in main
    time.sleep(1)
KeyboardInterrupt

```

Program ukončíte stiskem ++ctrl+c++.

!!!Poznámka
Možná jste si všimli, že analogové porty jsou na desce popsány jako **A1, A0**, i když v programu používáme jako parametry **0** a **1**, stejně jako u digitálních portů. Ujistěte se proto, že připojujete modul ke správným portům, jinak nebude zapojení fungovat.

### Pokusy s Raspberry Pi (s modulem GrovePi_Plus)

#### Hardware

- Krok 1: Připravte si tyto součástky:

| Raspberry pi                                                                                                   | GrovePi_Plus                                                                                                         | Grove - Light Sensor                                                                                                   | Grove - Red LED                                                                                                |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/img/light_sensor_s.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Red_LED/raw/master/img/Red%20LED_s.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)                                                         | [Koupit](https://www.seeedstudio.com/Grove-Light-Sensor-v1.2-p-2727.html)                                              | [Koupit](https://www.seeedstudio.com/s/Grove-Red-LED-p-1142.html)                                              |

- Krok 2: Připojte GrovePi_Plus k Raspberry Pi.
- Krok 3: Připojte Grove-light sensor k portu A0 na GrovePi_Plus.
- Krok 4: Připojte Grove-Red Led k portu D4 na GrovePi_Plus.
- Krok 5: Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/img/rasp_light.jpg)

#### Software

- Krok 1: Nastavte si vývojové prostředí pomocí průvodce [nastavení software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/).
- Krok 2: Stáhněte si zdrojový kód tím, že naklonujete knihovnu GrovePi.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

- Krok 3: Spusťte následující příkazy.

```
cd ~/GrovePi/Software/Python
python grove_light_sensor.py
```

Toto je kód v souboru grove_light_sensor.py.

```python
import time
import grovepi

# Připojte Grove Light Sensor to analog port A0
# SIG,NC,VCC,GND
light_sensor = 0

# Připojte LED to digital port D4
# SIG,NC,VCC,GND
led = 4

# Turn on LED once sensor exceeds threshold resistance
threshold = 10

grovepi.pinMode(light_sensor,"INPUT")
grovepi.pinMode(led,"OUTPUT")

while True:
    try:
        # Get sensor value
        sensor_value = grovepi.analogRead(light_sensor)

        # Calculate resistance of sensor in K
        resistance = (float)(1023 - sensor_value) * 10 / sensor_value

        if resistance > threshold:
            # Send HIGH to switch on LED
            grovepi.digitalWrite(led,1)
        else:
            # Send LOW to switch off LED
            grovepi.digitalWrite(led,0)

        print("sensor_value = %d resistance = %.2f" %(sensor_value,  resistance))
        time.sleep(.5)

    except IOError:
        print ("Error")
```

- Krok 4: LED se rozsvítí, když snímač světla zakryjete.

```
pi@raspberrypi:~/GrovePi/Software/Python $ python grove_light_sensor.py
sensor_value = 754 resistance = 3.57
sensor_value = 754 resistance = 3.57
sensor_value = 752 resistance = 3.60
sensor_value = 752 resistance = 3.60
sensor_value = 752 resistance = 3.60
sensor_value = 313 resistance = 22.68
sensor_value = 155 resistance = 56.00
sensor_value = 753 resistance = 3.59
```

## Zdroje

- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/res/Grove_Light_Sensor_CDC_File.zip)
- **[Eagle&PDF]** [Eagle File for Grove - Light Sensor V1.0](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/resources/Grove%20-%20Light%20Sensor.zip)
- **[Eagle&PDF]** [Eagle File for Grove - Light Sensor(P) V1.0](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/resources/Grove%20-%20Light%20Sensor%28P%29.zip)
- **[Eagle&PDF]** [Eagle File for Grove - Light Sensor(P) V1.1](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/resources/Grove%20-%20Light%20Sensor%28P%29%20v1.1.zip)
- **[Datasheet]** [LS06-MΦ5 Reference Information](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/res/LS06-M%CE%A65_datasheet.pdf)
- **[Datasheet]** [LM358.PDF](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/res/LM358.pdf)
- **[Další čtení]** Tajná schránka

![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/secret_box.png)

Použijeme snímač světla ke konstrukci tajné schránky. Ze všeho nejdřív budete potřebovat nějakou neprůsvitnou krabici s víkem - papírovou, dřevěnou, plastovou, zkrátka libovolnou. Do krabice dáme něco, co nechceme, aby ostatní viděli, jinak by to nebylo tajné. Když krabici někdo otevře, dostaneme o tom zprávu.

Jako řídicí modul jsme použili LinkIt ONE, což je deska, kompatibilní s Arduinem, ale vylepšená o některé funkce. Zde je seznam dílů:

- [LinkIt ONE](http://www.seeedstudio.com/LinkIt-ONE-p-2017.html)
- Grove - Light Sensor
- Grove - Base Shield
- Aktivní SIM karta

Připojíme snímač světla k protu A0 na Base Shieldu a do Arduino IDE zkopírujeme následující kód. Přeložíme a nahrajeme do LinkIt ONE. Jakmile někdo otevře krabici a na snímač dopadne světlo, program vám pošle SMS.

```c
// demo of Grove Starter kit for LinkIt ONE
// Secret box

#include <LGSM.h>

char num[20] = "13425171053";           // your number write here
char text[100] = "Warning: Your box had been opened!!";    // what do you want to send


const int pinLight = A0;                // light sensor connect to A0

bool isLightInBox()
{
    return (analogRead(pinLight)<50);   // when get data less than 50, means light sensor was in box
}

void setup()
{
    Serial.begin(115200);

    while(!isLightInBox());             // until put in box
    delay(2000);
}


void loop()
{
    if(!isLightInBox())                 // box is open
    {
        Serial.println("box had been opened");

        while(!LSMS.ready())
        {
            delay(1000);
        }

        Serial.println("SIM ready for work!");
        LSMS.beginSMS(num);
        LSMS.print(text);

        if(LSMS.endSMS())
        {
            Serial.println("SMS is sent");
        }
        else
        {
            Serial.println("SMS send fail");
        }

        while(!isLightInBox());             // until put in box
        delay(2000);
    }

    delay(10);
}
```

Have fun.

## Projekty

**Grove - Úvod ke snímači světla**:

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/ingo-lohs/grove-introduction-in-a-light-sensor-a55efd/embed' width='350'></iframe>

**Monitorovací krychle! Poznejte zemi se Sigfoxem**: Krychle se všemi podstatnými snímači, použitelná pro širokou škálu aplikací v zemědělství apod.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/dhairya-parikh/the-environment-cube-know-the-land-beneath-you-using-sigfox-952f29/embed' width='350'></iframe>

**Modul světelného snímače Grove**:

<iframe width="560" height="315" src="https://www.youtube.com/embed/ZvFswNYY2mU" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/GOROc2f5Xkg" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
