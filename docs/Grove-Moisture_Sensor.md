---
name: Grove - Moisture Sensor
category: Sensor
bzurl: https://www.seeedstudio.com/Grove-Moisture-Sensor-p-955.html
oldwikiname: Grove - Moisture Sensor
prodimagename: Moisture_sensor_.jpg
surveyurl: https://www.research.net/r/grove-moisture-sensor
sku: 101020008
---

![](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/images/Moisture_sensor_.jpg)

Měřič vlhkosti slouží buď k měření vlhkosti půdy, nebo například pro detekci zaplavení. Může kontrolovat, jestli květiny nepotřebují zalít, a případně spustit automatickou zálivku bez lidského zásahu. Snímač se dá použít velmi snadno, stačí jej jen zapíchnout do zeminy a číst hodnoty. Můžete si tak postavit jednoduché zařízení, kterým vaše rostliny pošlou zprávu "mám žízeň, zalij mě, prosím!"

<p style=":center"><a href="https://www.seeedstudio.com/Grove-Moisture-Sensor-p-955.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/get_one_now_small.png" width="200" height="38"  border=0 /></a></p>

## Verze

| Verze produktu               | Změny        | Datum vydání |
| ---------------------------- | ------------ | ------------ |
| Grove - Moisture Sensor V1.4 | První vydání | June 2014    |

## Vlastnosti

- Snímač půdní vlhkosti, založený na měření vodivosti zeminy
- Snadno použitelný
- 2.0 cm X 6.0 cm

!!!Tip
Více detailů o modulech Grove zjistíte v [popisu systému Grove](http://wiki.seeedstudio.com/Grove_System/)

## Specifikace

| Parametr         | Condition                        | Min                 | Typical | Max               | Jednotka |
| ---------------- | -------------------------------- | ------------------- | ------- | ----------------- | -------- |
| Napětí           | -                                | 3.3                 | -       | 5                 | V        |
| Proud            | -                                | 0                   | -       | 35                | mA       |
| Výstupní hodnota | Suchá půda<br>Vlhká půda<br>Voda | 0<br>300<br>700<br> | -       | 300<br>700<br>950 | -        |

## Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                               | BeagleBone                                                                                          | Wio                                                                                                 | LinkIt ONE                                                                                             |
| ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Můžete použít pro

- Chytrou zahradu
- Snímání vlhkosti

## Začínáme

!!!Poznámka
Pokud se s Arduinem setkáváte poprvé, doporučujeme vám pročíst návod [Začínáme s Arduinem](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) dřív, než začnete.

### Pokusy s Arduinem

**Hardware**

- **Krok 1.** Připravte si tyto součástky:

| Seeeduino V4.2                                                                                                           | Base Shield                                                                                                           | Grove-Moisture Sensor                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/img/Moisture_sensor_S.jpg) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                          | [Koupit](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                      | [Koupit](https://www.seeedstudio.com/Grove-Moisture-Sensor-p-955.html)                                                       |

- **Krok 2.** Připojte Grove-Moisture Sensor k portu A0 na Grove-Base Shieldu.
- **Krok 3.** Připojte Base Shield k Seeeduinu.
- **Krok 4.** Připojte Seeduino k PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/img/Seeeduino_moisture.jpg)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit Grove-Moisture Sensor k Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino   | Grove-Moisture Sensor |
| ----------- | --------------------- |
| 5V          | Červený               |
| GND         | Černý                 |
| Nepřipojeno | Bílý                  |
| A0          | Žlutý                 |

**Software**

- **Krok 1.** Zkopírujte kód do Arduino IDE, přeložte a nahrajte do Arduina. Pokud si nejste jisti, jak nahrát kód, podívejte se na stránku [Jak nahrát kód](http://wiki.seeedstudio.com/Upload_Code/).

```c++
int sensorPin = A0;
int sensorValue = 0;

void setup() {
    Serial.begin(9600);
}
void loop() {
    // read the value from the sensor:
    sensorValue = analogRead(sensorPin);
    Serial.print("Moisture = " );
    Serial.println(sensorValue);
    delay(1000);
}
```

- **Krok 2.** V terminálu uvidíte údaje o vlhkosti.

```
Moisture = 0
Moisture = 31
Moisture = 48
Moisture = 139
Moisture = 155
Moisture = 124
Moisture = 236
Moisture = 218
Moisture = 215
Moisture = 221
```

### Pokusy s Codecraftem

#### Hardware

**Krok 1.** Připojte Grove - Moisture Sensor k portu A0 na Grove-Base Shieldu

**Krok 2.** Připojte Base Shield k Seeeduinu / Arduinu.

**Krok 3.** Propojte Seeeduino/Arduino s PC pomocí kabelu USB.

#### Software

**Krok 1.** Spusťte [Codecraft](https://ide.chmakered.com/), přepněte se na prostředí pro Arduino a přidejte na plochu hlavní proceduru (Start).

!!!Poznámka
Pokud používáte Codecraft poprvé, podívejte se na [Průvodce světem Codecraftu a Arduina](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Krok 2.** Přetáhněte bloky tak, jak ukazuje následující obrázek, nebo otevřte cdc soubor, který si můžete stáhnout na konci této stránky.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove_Moisture_Sensor/master/img/cc_Moisture_Sensor.png)

Nahrajte hotový program do svého Arduina/Seeeduina.

!!!Povedlo se
Jakmile je nahrávání hotové, v terminálu uvidíte údaje o vlhkosti.

### Pokusy s Raspberry Pi (s Grove Base Hat)

#### Hardware

- **Krok 1**. Součástky, použité v tomto projektu:

| Raspberry pi                                                                                                   | Grove Base Hat for RasPi                                                                                                       | Grove - Moisture Sensor                                                                                                      |
| -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/img/Moisture_sensor_S.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)                                              | [Koupit](https://www.seeedstudio.com/Grove-Moisture-Sensor-p-955.html)                                                       |

- **Krok 2**. Připojte Grove Base Hat k Raspberry Pi.
- **Krok 3**. Připojte Grove - Moisture Sensor to the A0 port of the Base Hat.
- **Krok 4**. Propojte Raspberry Pi s PC pomocí kabelu USB.
  ![](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/images/with_hat.jpg)

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
python grove_moisture_sensor.py 0
```

Toto je kód v souboru grove_moisture_sensor.py.

```python
#!/usr/bin/env python
# -*- coding: utf-8 -*-
#
# The MIT License (MIT)
#
# Grove Base Hat for the Raspberry Pi, used to connect grove sensors.
# Copyright (C) 2018  Seeed Technology Co.,Ltd.
'''
This is the code for
    - Grove - Moisture Sensor <https://www.seeedstudio.com/Grove-Moisture-Sensor-p-955.html>`_

Examples:

    .. code-block:: python

        import time
        from grove.grove_moisture_sensor import GroveMoistureSensor

        # connect to alalog pin 2(slot A2)
        PIN = 2

        sensor = GroveMoistureSensor(PIN)

        print('Detecting moisture...')
        while True:
            m = sensor.moisture
            if 0 <= m and m < 300:
                result = 'Dry'
            elif 300 <= m and m < 600:
                result = 'Moist'
            else:
                result = 'Wet'
            print('Moisture value: {0}, {1}'.format(m, result))
            time.sleep(1)
'''
import math
import sys
import time
from grove.adc import ADC

__all__ = ["GroveMoistureSensor"]

class GroveMoistureSensor:
    '''
    Grove Moisture Sensor class

    Args:
        pin(int): number of analog pin/channel the sensor connected.
    '''
    def __init__(self, channel):
        self.channel = channel
        self.adc = ADC()

    @property
    def moisture(self):
        '''
        Get the moisture strength value/voltage

        Returns:
            (int): voltage, in mV
        '''
        value = self.adc.read_voltage(self.channel)
        return value

Grove = GroveMoistureSensor


def main():
    from grove.helper import SlotHelper
    sh = SlotHelper(SlotHelper.ADC)
    pin = sh.argv2pin()

    sensor = GroveMoistureSensor(pin)

    print('Detecting moisture...')
    while True:
        m = sensor.moisture
        if 0 <= m and m < 300:
            result = 'Dry'
        elif 300 <= m and m < 600:
            result = 'Moist'
        else:
            result = 'Wet'
        print('Moisture value: {0}, {1}'.format(m, result))
        time.sleep(1)

if __name__ == '__main__':
    main()
```

!!!Povedlo se
Pokud vše šlo tak, jak má, uvidíte výsledek podobný tomuto:

```python

pi@raspberrypi:~/grove.py/grove $ python grove_moisture_sensor.py 0
Detecting moisture...
Moisture value: 0, Dry
Moisture value: 1, Dry
Moisture value: 25, Dry
Moisture value: 3, Dry
Moisture value: 0, Dry
Moisture value: 0, Dry
Moisture value: 0, Dry
Moisture value: 0, Dry
Moisture value: 0, Dry
Moisture value: 1, Dry
^CTraceback (most recent call last):
  File "grove_moisture_sensor.py", line 74, in <module>
    main()
  File "grove_moisture_sensor.py", line 71, in main
    time.sleep(1)
KeyboardInterrupt


```

Program ukončíte stiskem ++ctrl+c++.

!!!Poznámka
Možná jste si všimli, že analogové porty jsou na desce popsány jako **A1, A0**, i když v programu používáme jako parametry **0** a **1**, stejně jako u digitálních portů. Ujistěte se proto, že připojujete modul ke správným portům, jinak nebude zapojení fungovat.

### Pokusy s Raspberry Pi (s modulem GrovePi_Plus)

**Hardware**

- **Krok 1.** Připravte si tyto součástky:

| Raspberry pi                                                                                                   | GrovePi_Plus                                                                                                         | Grove-Moisture Sensor                                                                                                        |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/img/Moisture_sensor_S.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)                                                         | [Koupit](https://www.seeedstudio.com/Grove-Moisture-Sensor-p-955.html)                                                       |

- **Krok 2.** Připojte GrovePi_Plus k Raspberry Pi.
- **Krok 3.** Připojte Grove-Moisture Sensor to **A0** na GrovePi_Plus.
- **Krok 4.** Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/img/rpi_moisture.jpg)

**Software**

- **Krok 1.** Nastavte si vývojové prostředí pomocí průvodce [nastavení software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/).
- **Krok 2.** Stáhněte si zdrojový kód tím, že naklonujete knihovnu GrovePi.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

- **Krok 3.** Spusťte následující příkazy.

```
cd ~/GrovePi/Software/Python
python grove_moisture_sensor.py
```

Toto je kód v souboru grove_moisture_sensor.py.

```python
# 	Here are suggested sensor values:
# 		Min  Typ  Max  Condition
# 		0    0    0    sensor in open air
# 		0    20   300  sensor in dry soil
# 		300  580  700  sensor in humid soil
# 		700  940  950  sensor in water


import time
import grovepi

# Připojte Grove Moisture Sensor to analog port A0
# SIG,NC,VCC,GND
sensor = 0

while True:
    try:
        print(grovepi.analogRead(sensor))
        time.sleep(.5)

    except KeyboardInterrupt:
        break
    except IOError:
        print ("Error")
```

- **Krok 4.** V terminálu uvidíte hodnoty vlhkosti.

```
pi@raspberrypi:~/GrovePi/Software/Python $ python grove_moisture_sensor.py
0
90
130
150
160
218
238
```

### Pokusy s TI LaunchPad

**Hardware**

Tento příklad ukazuje, jak snadno měřit vlhkost zeminy v květináči. Snímač vlhkosti snímá aktuání hodnoty a program je zobrazuje na displeji, takže prostým pohledem vidíte, zda je potřeba zalít.

![](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/images/Moisture.jpg)

**Software**

```c
/*
  Moisture-Sensor
  The following sketch demonstrates a simple application of sensing
  the moisture of the soil. You can know whether a plant needs water
  or not by observing the results that the sensor outputs.
  The circuit:
    * Moisture-Sensor attached to pin 24 (J6 plug on Grove Base BoosterPack)
    * one side pin (either one) to ground
    * the other side pin to +VCC
    * LED anode (long leg) attached to RED_LED
    * LED cathode (short leg) attached to ground
  - NOTE:
    This example code is in the public domain.
    http://seeedstudio.com/wiki/Grove_-_Moisture_Sensor
*/
#include "TM1637.h"
/* Macro Define */
#define CLK 39              /* 4-digital display clock pin */
#define DIO 38              /* 4-digiral display data pin */
#define BLINK_LED RED_LED   /* blink led */
#define MOISTURE_PIN 24     /* pin of moisture sensor */
#define THRESHOLD_VALUE 300 /* threshold for watering the flowers */
#define ON HIGH             /* led on */
#define OFF LOW             /* led off */
#define _handle_led(x) digitalWrite(BLINK_LED, x) /* handle led */

/* Global Varibles */
TM1637 tm1637(CLK, DIO);    /* 4-digital display object */
int analog_value = 0;       /* varible to store the value coming from rotary angle
sensor */
int8_t bits[4] = {0};       /* array to store the single bits of the value */
/* the setup() method runs once, when the sketch starts */
void setup() {
/* Initialize 4-digital display */
    tm1637.init();
    tm1637.set(BRIGHT_TYPICAL);
/* declare the red_led pin as an OUTPUT */
    pinMode(BLINK_LED, OUTPUT);
}
/* the loop() method runs over and over again */
void loop() {
    analog_value = analogRead(MOISTURE_PIN); /* read the value from the sensor */
/* if the value is smaller than threshold, turn on led */
    if(analog_value < THRESHOLD_VALUE) {
        _handle_led(ON);
    } else {
        _handle_led(OFF);
    }
    memset(bits, 0, 4); /* reset array when we use it */
    for(int i = 3; i >= 0; i--) {
/* get single bits of the analog value */
        bits[i] = analog_value % 10;
        analog_value = analog_value / 10;
        tm1637.display(i, bits[i]); /* display by 4-digital display */
    }
    delay(200);
}
```

## FAQ - Často kladené dotazy

**Ot. 1: Co je hodnota na výstupu? Volty, nebo co?**

Odp. 1: Výstup jsou volty. Když použijete funkci analogRead(), bude referenční napětí, tedy většinou 5V, poděleno hodnotou 1024. Načtená hodnota = Vout \* 1024/5. Čím vyšší číslo, tím vyšší vlhkost.

## Zdroje

- [**Eagle&PDF**][grove - moisture sensor v1.4 schematic](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/resources/Grove%20-%20Moisture%20Sensor%20v1.4.zip)
- [**Codecraft**][cdc file](https://raw.githubusercontent.com/SeeedDocument/Grove_Moisture_Sensor/master/res/Grove_Moisture_Sensor_CDC_File.zip)

## Projekty

**Monitorování rostlin pomocí AWS IoT**: Pokud jedete na dovolenou, tento jednoduchý projekt vám bude sledovat teplotu a vlhkost půdy v květináči a zaznamenávat vše pomocí dweet.io a AWS IoT.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/carmelito/plant-monitoring-system-using-aws-iot-6cb054/embed' width='350'></iframe>

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
