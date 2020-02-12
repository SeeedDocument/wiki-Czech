---
name: Grove - Water Sensor
category: Sensor
bzurl: https://www.seeedstudio.com/Grove-Water-Sensor-p-748.html
oldwikiname: Grove_-_Water_Sensor
prodimagename: Grove-Water_Sensor.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/101020018 1.jpg
surveyurl: https://www.research.net/r/Grove-Water_Sensor
sku: 101020018
tags: grove_digital, io_3v3, io_5v, plat_duino, plat_linkit, plat_pi, plat_bbg
---

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Water_Sensor/master/img/Grove-Water_Sensor_1.png)

Tento modul dokáže dát informaci o tom, zda je suchý, vlhký nebo kompletně ponořený ve vodě, a to na základě měření vodivosti. Vodivé dráhy mají připojený pull-up rezistor 1 MΩ, který udržuje hodnotu ve stavu HIGH. Dopadající kapky propojí snímací dráhu se zemí a naměřené napětí poklesne. Tento snímač můžete použít jako digitální, pro indikaci, jestli je suchý nebo mokrý, anebo jako analogový, kdy říká, kolik vody na něm je.

<p style=":center"><a href="https://www.seeedstudio.com/Grove-Water-Sensor-p-748.html" target="_blank"><img src="https://raw.githubusercontent.com/SeeedDocument/Seeed-WiKi/master/docs/images/get_one_now_small.png" width="210" height="41"  border=0 /></a></p>

## Verze

| Verze produktu          | Změny        | Datum vydání |
| ----------------------- | ------------ | ------------ |
| Grove-Water Sensor V1.1 | První vydání | July 2014    |

## Vlastnosti

- Kompatibilní s rozhraním Grove
- Nízký odběr
- Modul 2 x 2 cm
- Vysoká citlivost

## Použití

- Detektor deště
- Detektor úniku vody
- Upozornění na přeplnění nádrže

## Specifikace

<table border="1" cellspacing="0" width="80%">
<tr>
<th scope="col">
Parametr
</th>
<th scope="col">
Min
</th>
<th scope="col">
Typical
</th>
<th scope="col">
Max
</th>
<th scope="col">
Jednotka
</th>
</tr>
<tr align="center">
<th scope="row">
Pracovní napětí
</th>
<td>
4.75
</td>
<td>
5.0
</td>
<td>
5.25
</td>
<td>
V
</td>
</tr>
<tr align="center">
<th scope="row">
Proud
</th>
<td colspan="3">
&lt;20
</td>
<td>
mA
</td>
</tr>
<tr align="center">
<th scope="row">
Pracovní teplota
</th>
<td>
10
</td>
<td>
-
</td>
<td>
30
</td>
<td>
℃
</td>
</tr>
<tr align="center">
<th scope="row">
Pracovní vlhkost (nekondenzující)
</th>
<td>
10
</td>
<td>
-
</td>
<td>
90
</td>
<td>
 %
</td>
</tr>
</table>

!!!Tip
Více detailů o modulech Grove zjistíte v [popisu systému Grove](http://wiki.seeedstudio.com/Grove_System/)

## Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                               | BeagleBone                                                                                        | Wio                                                                                               | LinkIt ONE                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Začínáme

!!!Poznámka
Pokud se s Arduinem setkáváte poprvé, doporučujeme vám pročíst návod [Začínáme s Arduinem](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) dřív, než začnete.

### Pokusy s Arduinem

#### Hardware

Modul můžete připojit k některému z digitálních vstupů. Měříte hodnotu na výstupu SIG. Pokud je modul suchý, hodnota je HIGH, jakmile nějaká voda propojí vodivé lišty, výstup se změní na LOW.

- **Krok 1.** Připravte si tyto součástky:

| Seeeduino V4.2                                                                                                             | Base Shield                                                                                                                | Grove - Water Sensor                                                                                                                        |
| -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Water_Sensor/master/img/Grove-Water_Sensor_small.png) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                            | [Koupit](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                           | [Koupit](https://www.seeedstudio.com/Grove-Water-Sensor-p-748.html)                                                                         |

- **Krok 2.** Připojte modul k portu D2 na Grove-Base Shieldu.
- **Krok 3.** Připojte Base Shield k Seeeduinu.
- **Krok 4.** Připojte Seeduino k PC pomocí kabelu USB.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Water_Sensor/master/img/3.jpg)
!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit Grove_Water_Sensor k Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino   | Grove - Water Sensor |
| ----------- | -------------------- |
| 5V          | Červený              |
| GND         | Černý                |
| Nepřipojeno | Bílý                 |
| D2          | Žlutý                |

#### Software

- **Krok 1.** Zkopírujte kód do Arduino IDE, přeložte a nahrajte do Arduina. Pokud si nejste jisti, jak nahrát kód, podívejte se na stránku [Jak nahrát kód](http://wiki.seeedstudio.com/Upload_Code/).

```c
#define WATER_SENSOR 2

void setup()
{
  Serial.begin (9600);
  pinMode(WATER_SENSOR, INPUT);
}
void loop()
{
  Serial.println(digitalRead(WATER_SENSOR));
  delay(500);
}

```

- **Krok 2.** V sériovém terminálu uvidíte výstup, podobný tomuto.

```c
1
1
0
0
1
1
```

### Pokusy s Codecraftem

#### Hardware

**Krok 1.** Připojte Grove - Water Sensor k portu D2 na Grove-Base Shieldu

**Krok 2.** Připojte Base Shield k Seeeduinu / Arduinu.

**Krok 3.** Propojte Seeeduino/Arduino s PC pomocí kabelu USB.

#### Software

**Krok 1.** Spusťte [Codecraft](https://ide.chmakered.com/), přepněte se na prostředí pro Arduino a přidejte na plochu hlavní proceduru (Start).

!!!Poznámka
Pokud používáte Codecraft poprvé, podívejte se na [Průvodce světem Codecraftu a Arduina](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Krok 2.** Přetáhněte bloky tak, jak ukazuje následující obrázek, nebo otevřte cdc soubor, který si můžete stáhnout na konci této stránky.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove-Water_Sensor/master/img/cc_Water_Sensor.png)

Nahrajte hotový program do svého Arduina/Seeeduina.

!!!Povedlo se
Jakmile je nahrávání hotové, sériový monitor vám ukáže, jestli je na modulu přítomná voda, nebo není.

### Pokusy s Raspberry Pi (s Grove Base Hat)

#### Hardware

- **Krok 1**. Součástky, použité v tomto projektu:

| Raspberry pi                                                                                                   | Grove Base Hat for RasPi                                                                                                       | Grove - Water Sensor                                                                                                                        |
| -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Water_Sensor/master/img/Grove-Water_Sensor_small.png) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)                                              | [Koupit](https://www.seeedstudio.com/Grove-Water-Sensor-p-748.html)                                                                         |

- **Krok 2**. Připojte Grove Base Hat k Raspberry Pi.
- **Krok 3**. Připojte Grove - Water Sensor k portu A0 na Base Hatu.
- **Krok 4**. Propojte Raspberry Pi s PC pomocí kabelu USB.
  ![](https://github.com/SeeedDocument/Grove-Water_Sensor/raw/master/img/with_rpi_basehat.jpg)

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
python grove_water_sensor.py 0
```

Toto je kód v souboru grove_water_sensor.py.

```python

import math
import sys
import time
from grove.adc import ADC


class GroveWaterSensor:

    def __init__(self, channel):
        self.channel = channel
        self.adc = ADC()

    @property
    def value(self):
        return self.adc.read(self.channel)

Grove = GroveWaterSensor


def main():
    if len(sys.argv) < 2:
        print('Usage: {} adc_channel'.format(sys.argv[0]))
        sys.exit(1)

    sensor = GroveWaterSensor(int(sys.argv[1]))

    print('Detecting ...')
    while True:
        value = sensor.value
        if sensor.value > 800:
            print("{}, Detected Water.".format(value))
        else:
            print("{}, Dry.".format(value))

        time.sleep(.1)

if __name__ == '__main__':
    main()


```

!!!Povedlo se
Pokud vše šlo tak, jak má, uvidíte výsledek podobný tomuto

```python

pi@raspberrypi:~/grove.py/grove $ python grove_water_sensor.py 0
Detecting ...
612, Dry.
749, Detected Water.
829, Dry.
357, Dry.
98, Dry.
352, Dry.
517, Dry.
718, Detected Water.
868, Detected Water.
581, Dry.
90, Dry.
326, Dry.
451, Dry.
666, Dry.
867, Detected Water.
684, Dry.
100, Dry.
^CTraceback (most recent call last):
  File "grove_water_sensor.py", line 71, in <module>
    main()
  File "grove_water_sensor.py", line 62, in main
    value = sensor.value
  File "grove_water_sensor.py", line 48, in value
    return self.adc.read(self.channel)
  File "/usr/local/lib/python2.7/dist-packages/grove/adc.py", line 66, in read
    return self.read_register(addr)
  File "/usr/local/lib/python2.7/dist-packages/grove/adc.py", line 84, in read_register
    return self.bus.read_word_data(self.address, n)
  File "/home/pi/.local/lib/python2.7/site-packages/smbus2/smbus2.py", line 396, in read_word_data
    ioctl(self.fd, I2C_SMBUS, msg)
KeyboardInterrupt


```

Program detekuje přítomnost vody. Program ukončíte stiskem ++ctrl+c++.

!!!Poznámka
Možná jste si všimli, že analogové porty jsou na desce popsány jako **A1, A0**, i když v programu používáme jako parametry **0** a **1**, stejně jako u digitálních portů. Ujistěte se proto, že připojujete modul ke správným portům, jinak nebude zapojení fungovat.

### Pokusy s Raspberry Pi (s modulem GrovePi_Plus)

#### Hardware

- **Krok 1.** Připravte si tyto součástky:

| Raspberry pi                                                                                                   | GrovePi_Plus                                                                                                         | Grove - Water Sensor                                                                                                                        |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Water_Sensor/master/img/Grove-Water_Sensor_small.png) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)                                                         | [Koupit](https://www.seeedstudio.com/Grove-Water-Sensor-p-748.html)                                                                         |

- **Krok 2.** Připojte GrovePi_Plus k Raspberry Pi.
- **Krok 3.** Připojte Grove-Water Sensor k portu **D2** na GrovePi_Plus.
- **Krok 4.** Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Water_Sensor/master/img/7.jpg)

#### Software

- **Krok 1.** Nastavte si vývojové prostředí pomocí průvodce [nastavení software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/).
- **Krok 2.** Přesuňte se do adresáře s příklady:

```
cd yourpath/GrovePi/Software/Python/
```

- **Krok 3.** Zkopírujte následující kód

```
nano grove_water_sensor.py
```

```python
import time
import grovepi

# Připojte Grove Water Sensor to digital port D2
# SIG,NC,VCC,GND
water_sensor = 2

grovepi.pinMode(water_sensor,"INPUT")

while True:
    try:
        print grovepi.digitalRead(water_sensor)
        time.sleep(.5)

    except IOError:
        print "Error"
```

- **Krok 4.** Spusťte ukázkový program.

```
sudo python grove_water_sensor.py
```

- **Krok 5.** V sériovém terminálu uvidíte výstup, podobný tomuto.

```
1
1
0
0
1
```

## Zdroje

- **[Eagle]** [Grove Water Sensor Schematic](https://raw.githubusercontent.com/SeeedDocument/Grove-Water_Sensor/master/res/Water_sensor.zip)
- **[Knihovna]** [Demo code for Grove Water Sensor](https://github.com/Seeed-Studio/Grove_Water_Sensor)
- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove-Water_Sensor/master/res/Grove_Water_Sensor_CDC_File.zip)

<!-- This Markdown file was created from http://wiki.seeedstudio.com/Grove-Water_Sensor/ -->

## Projekt

**Smart Crops: Implementace Internetu věcí v zemědělství!**: Chceme chránit přírodu a proto navrhujeme a vytváříme technologie a monitorovací metody s pomocí Internetu věcí.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/gabogiraldo/smart-crops-implementing-iot-in-conventional-agriculture-3674a6/embed' width='350'></iframe>

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
