---
name: Grove - Flame Sensor
category: Sensor
bzurl: https://seeedstudio.com/Grove-Flame-Sensor-p-1450.html
oldwikiname: Grove_-_Flame_Sensor
prodimagename: Flame_Sensor_01.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/product/Flame Sensor.jpg
surveyurl: https://www.research.net/r/Grove-Flame_Sensor
sku: 101020049
tags: grove_digital, io_5v, plat_duino, plat_linkit
---

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Flame_Sensor/master/img/Flame_Sensor_01.jpg)

Detektor plamenů (Grove - Flame Sensor) můžete použít pro detekci ohně nebo jiných zdrojů světla s vlnovou délkou 760nm - 1100 nm. Používá snímač YG1006, což je rychlý a citlivý NPN křemíkový fototranzistor. Snímač není citlivý na viditelné světlo díky svému černému pouzdru. Když budete stavět hasicího robota, bude tento senzor jeho očima, které mu pomohou najít zdroj ohně.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](http://www.seeedstudio.com/Grove-Flame-Sensor-p-1450.html)

## Vlastnosti

- Kompatibilní s rozhraním Grove
- Vysoká optická citlivost
- Rychlá odezva
- Snadno použitelný
- Citlivost je nastavitelná

!!!Tip
Více detailů o modulech Grove zjistíte v [popisu systému Grove](http://wiki.seeedstudio.com/Grove_System/)

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
Napětí
</th>
<td>
4.75
</td>
<td>
5.0
</td>
<td>
5.30
</td>
<td>
VDC
</td>
</tr>
<tr align="center">
<th scope="row">
Proud
</th>
<td>
/
</td>
<td>
20
</td>
<td>
/
</td>
<td>
mA
</td>
</tr>
<tr align="center">
<th scope="row">
Rozsah detekovaných vlnových délek
</th>
<td>
760
</td>
<td>
940
</td>
<td>
1100
</td>
<td>
nm
</td>
</tr>
<tr align="center">
<th scope="row">
Vzdálenost detekce
</th>
<td>
0
</td>
<td>
~
</td>
<td>
1
</td>
<td>
m
</td>
</tr>
<tr align="center">
<th scope="row">
Reakční doba
</th>
<td colspan="3">
15
</td>
<td>
μS
</td>
</tr>
<tr align="center">
<th scope="row">
Provozní teplota
</th>
<td>
-25
</td>
<td>
~
</td>
<td>
85
</td>
<td>
℃
</td>
</tr>
</table>

## Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                               | BeagleBone                                                                                          | Wio                                                                                                 | LinkIt ONE                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Začínáme

Modul se používá hlavně k detekci infračerveného záření. Na výstupu dává digitální signál, který je v úrovni LOW, pokud je infračervené světlo detekováno, jinak bude HIGH. Citlivost je nastavitelná pomocí přesného potenciometru.

### Pokusy s Arduinem

#### Hardware

- **Krok 1.** Připravte si tyto součástky:

| Seeeduino V4.2                                                                                                           | Base Shield                                                                                                           | Grove-Flame_Sensor                                                                                                | Grove - Red LED                                                                                           |
| ------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Flame_Sensor/raw/master/img/45d_small.jpg) | ![enter image description](https://github.com/SeeedDocument/Grove-Red_LED/raw/master/img/Red%20LED_s.jpg) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                          | [Koupit](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                      | [Koupit](http://www.seeedstudio.com/Grove-Flame-Sensor-p-1450.html)                                               | [Koupit](https://www.seeedstudio.com/s/Grove-Red-LED-p-1142.html)                                         |

- **Krok 2.** Připojte Grove-Flame_Sensor k portu **D2** na Grove-Base Shieldu.
- **Krok 3.** Připojte Grove - Red LED k portu **D3** na Grove-Base Shieldu.
- **Krok 4.** Připojte Base Shield k Seeeduinu.
- **Krok 5.** Připojte Seeduino k PC pomocí kabelu USB.

<!--link-->

![with_ardu](https://github.com/SeeedDocument/Grove-Flame_Sensor/raw/master/img/with_ardu.jpg)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit this module k Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino   | Grove-Flame_Sensor |
| ----------- | ------------------ |
| 5V          | Červený            |
| GND         | Černý              |
| Nepřipojeno | Bílý               |
| D2          | Žlutý              |

| Seeeduino   | Grove - Red LED |
| ----------- | --------------- |
| 5V          | Červený         |
| GND         | Černý           |
| Nepřipojeno | Bílý            |
| D3          | Žlutý           |

#### Software

**Krok 1.** Zkopírujte následující kód do Arduino IDE, přeložte jej a nahrajte.

```c
    /******************************************************************************/

#define FLAME_SENSOR 2 //connect SENSOR to digital pin2
#define LED 3 //connect Grove - LED to pin3

void setup()
{
    pinsInit();
}
void loop()
{
    if(isFlameDetected())
    turnOnLED();
    else turnOffLED();
}
    /********************************/
void pinsInit()
{
    pinMode(FLAME_SENSOR, INPUT);
    pinMode(LED,OUTPUT);
    digitalWrite(LED,LOW);
}
void turnOnLED()
{
    digitalWrite(LED,HIGH);
}
void turnOffLED()
{
    digitalWrite(LED,LOW);
}
boolean isFlameDetected()
{
    if(digitalRead(FLAME_SENSOR))
    return false;
    else return true;
}
```

**Krok 2.** Jakmile snímač detekuje plameny, LED se rozsvítí.

### Pokusy s Codecraftem

#### Hardware

**Krok 1.** Připojte Grove - Flame Sensor k portu D2 a Grove - Red LED k portu D3 na Grove-Base Shieldu

**Krok 2.** Připojte Base Shield k Seeeduinu / Arduinu.

**Krok 3.** Propojte Seeeduino/Arduino s PC pomocí kabelu USB.

#### Software

**Krok 1.** Spusťte [Codecraft](https://ide.chmakered.com/), přepněte se na prostředí pro Arduino a přidejte na plochu hlavní proceduru (Start).

!!!Poznámka
Pokud používáte Codecraft poprvé, podívejte se na [Průvodce světem Codecraftu a Arduina](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Krok 2.** Přetáhněte bloky tak, jak ukazuje následující obrázek, nebo otevřte cdc soubor, který si můžete stáhnout na konci této stránky.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove-Flame_Sensor/master/img/cc_Flame_Sensor.png)

Nahrajte hotový program do svého Arduina/Seeeduina.

!!!Povedlo se
Jakmile je nahrávání hotové, LED se rozsvítí, když snímač detekuje plameny.

### Pokusy s Raspberry Pi

#### Hardware

- **Krok 1.** Připravte si tyto součástky:

| Raspberry pi                                                                                                   | GrovePi_Plus                                                                                                         | Grove-Flame_Sensor                                                                                                |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Flame_Sensor/raw/master/img/45d_small.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)                                                         | [Koupit](https://www.seeedstudio.com/Grove-Flame-Sensor-p-1450.html)                                              |

- **Krok 2.** Připojte GrovePi_Plus k Raspberry Pi.
- **Krok 3.** Připojte Grove-Flame_Sensor k portu **D2** na GrovePi_Plus.
- **Krok 4.** Propojte Raspberry Pi s PC pomocí kabelu USB.

![with_rpi](https://raw.githubusercontent.com/SeeedDocument/Grove-Flame_Sensor/master/img/with_rpi.jpg)

#### Software

- **Krok 1.** Nastavte si vývojové prostředí pomocí průvodce [nastavení software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/).
- **Krok 2.** Stáhněte si zdrojový kód tím, že naklonujete knihovnu GrovePi.

```bash
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

- **Krok 3.** Spusťte následující příkazy

```bash
cd ~/GrovePi/Software/Python
python grove_flame_sensor.py
```

Zde je zdrojový kód:

```Python
#!/usr/bin/env python
#
# GrovePi Example for using the Grove Flame Sensor (http://www.seeedstudio.com/wiki/Grove_-_Flame_Sensor)
#
# The GrovePi connects the Raspberry Pi and Grove sensors.  You can learn more about GrovePi here:  http://www.dexterindustries.com/GrovePi
#
# Have a question about this example?  Ask on the forums here:  http://forum.dexterindustries.com/c/grovepi
#
'''
## License
The MIT License (MIT)
GrovePi for the Raspberry Pi: an open source platform for connecting Grove Sensors to the Raspberry Pi.
Copyright (C) 2017  Dexter Industries
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:
The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
'''
import time
import grovepi

# Připojte Grove Flame Sensor to digital port D2
# SIG,NC,VCC,GND
flame_sensor = 2

grovepi.pinMode(flame_sensor,"INPUT")

while True:
    try:
        print(grovepi.digitalRead(flame_sensor))
        time.sleep(.5)

    except IOError:
        print ("Error")
```

## Reference

Snímač je citlivý na zdroj světla s vlnovou délkou v rozsahu 760nm - 1100 nm. Obrázek ukazuje spektrální citlivost.
![](https://raw.githubusercontent.com/SeeedDocument/Grove-Flame_Sensor/master/img/Spectral_Sensitive.jpg)

## Zdroje

- **[Eagle]** [Grove - Flame Sensor Eagle File](https://raw.githubusercontent.com/SeeedDocument/Grove-Flame_Sensor/master/res/Grove-Directional_Light_Sensor_Eagle_File.zip)
- **[Knihovna]** [Github repository for Grove_Flame_Sensor Library](https://github.com/Seeed-Studio/Grove_Flame_Sensor)
- **[Datasheet]** [LM293D datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Flame_Sensor/master/res/LM293D.pdf)
- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove-Flame_Sensor/master/res/Grove_Flame_Sensor_CDC_File.zip)

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
