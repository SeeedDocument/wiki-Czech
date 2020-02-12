---
name: Grove - Loudness Sensor
category: Sensor
bzurl: https://seeedstudio.com/Grove-Loudness-Sensor-p-1382.html
oldwikiname: Grove_-_Loudness_Sensor
prodimagename: LoudnessSensor.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/product/Loudness Sensor.jpg
surveyurl: https://www.research.net/r/Grove-Loudness_Sensor
sku: 101020063
tags: grove_analog, io_3v3, io_5v, plat_duino, plat_linkit, plat_bbg, plat_pi
---

![](https://github.com/SeeedDocument/Grove-Loudness_Sensor/raw/master/img/Loudness%20Sensor_new.jpg)

Grove - Loudness Sensor je navržen tak, aby zachycoval okolní zvuk. Pomocí zabudovaného mikrofonu a zesilovače LM2904 zachytává a filtruje vysoké frekvence zvuku, takže zůstane jen informace o celkové hlasitosti okolních zvuků. Tento signál pak zpracovává Arduino či jiný systém. Výstupní hodnota tak závisí na hlasitosti okolních zvuků. Zachycený signál prochází v modulu dvěma filtry, aby byl očištěný od rušivých výkyvů. Míra citlivosti se dá nastavit pomocí otočného potenciometru, který je rovněž součástí modulu.

<iframe width="800" height="450" src="https://www.youtube.com/embed/EhZ7uDvoALE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<p style=":center"><a href="http://www.seeedstudio.com/Grove-Loudness-Sensor-p-1382.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/get_one_now_small.png" width="200" height="38"  border=0 /></a></p>

## Verze

| Verze produktu              | Změny        | Datum vydání |
| --------------------------- | ------------ | ------------ |
| Grove-Loudness Sensor V0.9b | První vydání | Dec 2012     |

## Vlastnosti

- Kompatibilní s rozhraním Grove
- Snadno použitelný
- Základní element Grove

!!!Tip
Více detailů o modulech Grove zjistíte v [popisu systému Grove](http://wiki.seeedstudio.com/Grove_System/)

## Specifikace

| Parametr                 | Hodnota / Rozsah          |
| ------------------------ | ------------------------- |
| Napětí                   | 3.5~10 VDC                |
| Pracovní frekvence       | 50~2000 Hz                |
| Citlivost                | -48~66 dB                 |
| Odstup signálu od šumu   | >58 dB                    |
| Rozsah výstupních hodnot | Analogový signál (0-1023) |

## Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                               | BeagleBone                                                                                        | Wio                                                                                                 | LinkIt ONE                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Začínáme

!!!Poznámka
Pokud se s Arduinem setkáváte poprvé, doporučujeme vám pročíst návod [Začínáme s Arduinem](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) dřív, než začnete.

### Pokusy s Arduinem

**Hardware**

- **Krok 1.** Připravte si tyto součástky:

| Seeeduino V4.2                                                                                                           | Base Shield                                                                                                           | Grove-Loudness Sensor                                                                                                       |
| ------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Loudness_Sensor/raw/master/img/LoudnessSensor_s.jpg) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                          | [Koupit](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                      | [Koupit](http://www.seeedstudio.com/Grove-Loudness-Sensor-p-1382.html)                                                      |

- **Krok 2.** Připojte Grove-Loudness Sensor to **A0** port na Grove-Base Shieldu.
- **Krok 3.** Připojte Base Shield k Seeeduinu.
- **Krok 4.** Připojte Seeduino k PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-Loudness_Sensor/raw/master/img/seeeduino_loudness.jpg)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit Grove-Loudness Sensor k Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino   | Grove-Loudness Sensor |
| ----------- | --------------------- |
| 5V          | Červený               |
| GND         | Černý                 |
| Nepřipojeno | Bílý                  |
| A0          | Žlutý                 |

**Software**

- **Krok 1.** Zkopírujte kód do Arduino IDE, přeložte a nahrajte do Arduina. Pokud si nejste jisti, jak nahrát kód, podívejte se na stránku [Jak nahrát kód](http://wiki.seeedstudio.com/Upload_Code/).

```
int loudness;

void setup()
{
    Serial.begin(9600);
}

void loop()
{
    loudness = analogRead(0);
    Serial.println(loudness);
    delay(200);
}

```

- **Krok 2.** Otevřete Sériový plotter v Arduino IDE. Uvidíte výraznou změnu, pokud například fouknete na mikrofon.

![](https://github.com/SeeedDocument/Grove-Loudness_Sensor/raw/master/img/seeeduino_serial.png)

### Pokusy s Raspberry Pi (s Grove Base Hat)

#### Hardware

- **Krok 1**. Součástky, použité v tomto projektu:

| Raspberry pi                                                                                                   | Grove Base Hat for RasPi                                                                                                       | Grove - Loudness Sensor                                                                                                     |
| -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Loudness_Sensor/raw/master/img/LoudnessSensor_s.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)                                              | [Koupit](https://www.seeedstudio.com/Grove-Loudness-Sensor-p-1382.html)                                                     |

- **Krok 2**. Připojte Grove Base Hat k Raspberry Pi.
- **Krok 3**. Připojte Grove - Loudness Sensor k portu A0 na Base Hatu.
- **Krok 4**. Propojte Raspberry Pi s PC pomocí kabelu USB.
  ![](https://github.com/SeeedDocument/Grove-Loudness_Sensor/raw/master/img/withrpi_basehat.jpg)

#### Software

- **Krok 1**. Nastavte si vývojové prostředí pomocí průvodce [nastavení software](http://wiki.seeedstudio.com/Grove_Base_Hat_for_Raspberry_Pi/#installation).
- **Krok 2**. Stáhněte si zdrojový kód tím, že naklonujete knihovnu grove.py.

```
cd ~
git clone https://github.com/Seeed-Studio/grove.py

```

- **Krok 3.** Spusťte program pomocí následujících příkazů.

```
cd grove.py/grove
python grove_loudness_sensor.py 0
```

Toto je kód v souboru grove_water_sensor.py.

```python

import math
import sys
import time
from grove.adc import ADC


class GroveLoudnessSensor:

    def __init__(self, channel):
        self.channel = channel
        self.adc = ADC()

    @property
    def value(self):
        return self.adc.read(self.channel)

Grove = GroveLoudnessSensor


def main():
    if len(sys.argv) < 2:
        print('Usage: {} adc_channel'.format(sys.argv[0]))
        sys.exit(1)

    sensor = GroveLoudnessSensor(int(sys.argv[1]))

    print('Detecting loud...')
    while True:
        value = sensor.value
        if value > 10:
            print("Loud value {}, Loud Detected.".format(value))
            time.sleep(.5)

if __name__ == '__main__':
    main()


```

!!!Povedlo se
Pokud vše šlo tak, jak má, uvidíte výsledek podobný tomuto:

```python

pi@raspberrypi:~/grove.py/grove $ python grove_loudness_sensor.py 0
Detecting loud...
Loud value 15, Loud Detected.
Loud value 11, Loud Detected.
Loud value 250, Loud Detected.
Loud value 429, Loud Detected.
Loud value 203, Loud Detected.
Loud value 16, Loud Detected.
Loud value 11, Loud Detected.
^CTraceback (most recent call last):
  File "grove_loudness_sensor.py", line 68, in <module>
    main()
  File "grove_loudness_sensor.py", line 65, in main
    time.sleep(.5)
KeyboardInterrupt


```

Tento senzor můžete použít k měření úrovně hluku. Program ukončíte stiskem ++ctrl+c++.

!!!Poznámka
Možná jste si všimli, že analogové porty jsou na desce popsány jako **A1, A0**, i když v programu používáme jako parametry **0** a **1**, stejně jako u digitálních portů. Ujistěte se proto, že připojujete modul ke správným portům, jinak nebude zapojení fungovat.

### Pokusy s Raspberry Pi (s modulem GrovePi_Plus)

**Hardware**

- **Krok 1.** Připravte si tyto součástky:

| Raspberry pi                                                                                                   | GrovePi_Plus                                                                                                         | Grove-Loudness Sensor                                                                                                       |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Loudness_Sensor/raw/master/img/LoudnessSensor_s.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)                                                         | [Koupit](http://www.seeedstudio.com/Grove-Loudness-Sensor-p-1382.html)                                                      |

- **Krok 2.** Připojte GrovePi_Plus k Raspberry Pi.
- **Krok 3.** Připojte Grove-Loudness Sensor to **A0** na GrovePi_Plus.
- **Krok 4.** Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-Loudness_Sensor/raw/master/img/rpi_loudness.jpg)

**Software**

- **Krok 1.** Nastavte si vývojové prostředí pomocí průvodce [nastavení software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/).
- **Krok 2.** Stáhněte si zdrojový kód tím, že naklonujete knihovnu GrovePi.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

- **Krok 3.** Spusťte tento program.

```python
cd ~/GrovePi/Software/Python
python grove_loudness_sensor.py
```

Toto je kód v souboru grove_loudness_sensor.py.

```python
import time
import grovepi

# Připojte Grove Loudness Sensor to analog port A0
# SIG,NC,VCC,GND
loudness_sensor = 0

while True:
    try:
        # Read the sound level
        sensor_value = grovepi.analogRead(loudness_sensor)

        print("sensor_value = %d" %sensor_value)
        time.sleep(.5)

    except IOError:
        print ("Error")
```

- **Krok 4.** Uvidíte informace o hluku, podobné těm následujícím

```python
pi@raspberrypi:~/GrovePi/Software/Python $ python grove_loudness_sensor.py
sensor_value = 135
sensor_value = 23
sensor_value = 196
sensor_value = 258
sensor_value = 98
sensor_value = 131
```

## FAQ - Často kladené dotazy

- Ot.: Jaký je rozdíl mezi Grove-Loudness sensor a Grove - Sound Sensor?
  - Odp.: Grove-Loudness sensor obsahuje potenciometr k nastavení citlivosti.

## Zdroje

- **[Eagle&PDF]** [Grove - Loudness Sensor Schematic](https://github.com/SeeedDocument/Grove-Loudness_Sensor/raw/master/res/Grove%20-%20Loudness%20Sensor%20Eagle%20File_v0.9b.zip)
- **[Datasheet]** [LM2904DR Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Loudness_Sensor/master/res/LM2904DR.pdf)

## Projekty

**Monitor ovzduší na sluneční energii**: Open-source sada pro měření kvality ovzduší, úrovně hluku, vlhkosti a teploty.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/taifur/solar-powered-environmental-monitoring-kit-b1d03d/embed' width='350'></iframe>

**Šifra mistra Leonarda**: Tento projekt kombinuje elektroniku a řemeslo. Řemeslná část tvoří kostru díla a skládá se z 11 vrstev laserem zpracované dýhy.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/coding-with-da-vince/the-da-vinci-code-3b91a8/embed' width='350'></iframe>

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
