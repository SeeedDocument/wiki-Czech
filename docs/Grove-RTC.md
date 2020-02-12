---
name: Grove - RTC
category: Sensor
bzurl: https://seeedstudio.com/Grove-RTC-p-758.html
oldwikiname: Grove_-_RTC
prodimagename: Grove-RTC.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/101020013 1.jpg
surveyurl: https://www.research.net/r/Grove-RTC
sku: 101020013
tags: grove_i2c, io_3v3, io_5v, plat_duino, plat_pi
---

![](https://github.com/SeeedDocument/Grove-RTC/raw/master/img/45d.jpg)

Hodiny reálného času jsou založené na hodinovém obvodu DS1307, který komunikuje přes sběrnici I2C. Modul umožňuje připojení lithiové baterie (CR1225). Obvod udržuje informace o datu a času. Poskytuje údaje o sekundách, minutách, hodinách, dnu, měsíci, roku a pořadovém dnu v týdnu. Obvod správně počítá dny i v měsících s méně než 31 dny a má korekci přestupných roků. Obvod pracuje buď ve 24hodinovém režimu, nebo ve 12hodinovém s indikací AM/PM. Datum je platný až do roku 2100. S připojenou baterií dokáže obvod udržovat informaci o přesném času i když je napájení vypnuté. Bez této baterie se při vypnutí napájení obvod vynuluje.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](https://www.seeedstudio.com/Grove-RTC-p-758.html)

<div class="admonition note">
<p class="admonition-title">Poznámka</p>
Baterie není součástí balení.
</div>

## Specifikace

- Velikost: 2.0cm\*4.0cm
- Rozhraní: 2.0mm konektor
- Vývody: SCL,SDA,VCC,GND
- ROHS: Ano
- Napájecí napětí：3.3~5.5V
- Úroveň HIGH ：2.2~VCC+0.3 V
- Úroveň LOW ：-0.3~+0.8 V
- Napětí baterie：2.0~3.5 V

!!!Tip
Více detailů o modulech Grove zjistíte v [popisu systému Grove](http://wiki.seeedstudio.com/Grove_System/)

## Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                               | BeagleBone                                                                                          | Wio                                                                                                 | LinkIt ONE                                                                                             |
| ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Začínáme

### Pokusy s Arduinem

#### Hardware

- **Krok 1.** Připravte si tyto součástky:

| Seeeduino V4.2                                                                                                           | Base Shield                                                                                                           | Grove-RTC                                                                                                |
| ------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-RTC/raw/master/img/45d_small.jpg) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                          | [Koupit](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                      | [Koupit](https://www.seeedstudio.com/Grove-RTC-p-758.html)                                               |

- **Krok 2.** Připojte Grove-RTC k portu **I2C** na Grove-Base Shieldu.
- **Krok 3.** Připojte Base Shield k Seeeduinu.
- **Krok 4.** Připojte Seeduino k PC pomocí kabelu USB.

<div class="admonition note">
<p class="admonition-title">Poznámka</p>
S připojenou baterií dokáže obvod udržovat informaci o přesném času i když je napájení vypnuté. Bez této baterie se při vypnutí napájení obvod vynuluje. Připojte vždy baterii, bez ní se může stát, že obvod nebude fungovat správně.
</div>

![](https://github.com/SeeedDocument/Grove-RTC/raw/master/img/arduino_connection.jpg)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit Grove-LED Bar k Seeduinu tak, jak je popsáno v následující tabulce.

| Seeeduino_v4 | Grove-RTC |
| ------------ | --------- |
| 5V           | VCC       |
| GND          | GND       |
| SDA          | SDA       |
| SCL          | SCL       |

#### Software

**Krok 1.** Stáhněte si knihovnu [RTC Library](https://github.com/Seeed-Studio/RTC_DS1307/archive/master.zip).

**Krok 2.** S instalací knihovny pro Arduino vám pomůže návod [Jak instalovat knihovnu pro Arduino](http://wiki.seeedstudio.com/How_to_install_Arduino_Library).

**Krok 3.** Vytvořte nový projekt v Arduinu IDE a vložte níže uvedený kód, nebo otevřte přímo ukázkový program pomocí: **File -> Example ->RTC->SetTimeAndDisplay**.

![](https://github.com/SeeedDocument/Grove-RTC/raw/master/img/library%20example.jpg)

```c++
#include <Wire.h>
#include "DS1307.h"

DS1307 clock;//define a object of DS1307 class
void setup()
{
    Serial.begin(9600);
    clock.begin();
    clock.fillByYMD(2013,1,19);//Jan 19,2013
    clock.fillByHMS(15,28,30);//15:28 30"
    clock.fillDayOfWeek(SAT);//Saturday
    clock.setTime();//write time to the RTC chip
}
void loop()
{
    printTime();
}
    /*Function: Display time on the serial monitor*/
void printTime()
{
    clock.getTime();
    Serial.print(clock.hour, DEC);
    Serial.print(":");
    Serial.print(clock.minute, DEC);
    Serial.print(":");
    Serial.print(clock.second, DEC);
    Serial.print("  ");
    Serial.print(clock.month, DEC);
    Serial.print("/");
    Serial.print(clock.dayOfMonth, DEC);
    Serial.print("/");
    Serial.print(clock.year+2000, DEC);
    Serial.print(" ");
    Serial.print(clock.dayOfMonth);
    Serial.print("*");
    switch (clock.dayOfWeek)// Friendly printout the weekday
    {
        case MON:
        Serial.print("MON");
        break;
        case TUE:
        Serial.print("TUE");
        break;
        case WED:
        Serial.print("WED");
        break;
        case THU:
        Serial.print("THU");
        break;
        case FRI:
        Serial.print("FRI");
        break;
        case SAT:
        Serial.print("SAT");
        break;
        case SUN:
        Serial.print("SUN");
        break;
    }
    Serial.println(" ");
}
```

**Krok 4.** Nastavte správný čas. Změňte uvedené parametry na aktuální čas. Dávejte pozor na pořadí argumentů.

```c
clock.fillByYMD(2013,1,19);//Jan 19,2013
clock.fillByHMS(15,28,30);//15:28 30"
clock.fillDayOfWeek(SAT);//Saturday
```

**Krok 5.** Nahrajte kód a sledujte v Sériovém monitoru, jaká data modul poskytuje
![](https://github.com/SeeedDocument/Grove-RTC/raw/master/img/arduino%20result.png)

### Pokusy s Raspberry Pi

#### Hardware

- **Krok 1.** Připravte si tyto součástky:

| Raspberry pi                                                                                                   | GrovePi_Plus                                                                                                         | Grove-RTC                                                                                                |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-RTC/raw/master/img/45d_small.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)                                                         | [Koupit](https://www.seeedstudio.com/Grove-RTC-p-758.html)                                               |

- **Krok 2.** Připojte GrovePi_Plus k Raspberry Pi.
- **Krok 3.** Připojte Grove-RTC to **I2C** na GrovePi_Plus.
- **Krok 4.** Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-RTC/raw/master/img/rasp_connection.jpg)

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
python grove_i2c_rtc.py
```

Toto je zdrojový kód:

```Python
#!/usr/bin/env python
#
# GrovePi Example for using the Grove I2C RTC (http://www.seeedstudio.com/wiki/Grove_-_RTC)
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

# Připojte Grove Real Time Clock to any I2C port eg. I2C-1
# Can be found at I2C address 0x68
# SCL,SDA,VCC,GND

while True:
    try:
        print(grovepi.rtc_getTime())
        time.sleep(.5)

    except IOError:
        print ("Error")
```

- **Krok 4.** Výsledek bude vypadat nějak takto

![](https://github.com/SeeedDocument/Grove-RTC/raw/master/img/rpi_display.jpg)

**Demo 2: Grove_rtc**

Tento kód vypíše informace o čase v čitelnější podobě. Vytvořte soubor grove_rtc.py a vložte do něj toto.

```python
    '''
     * Grove-RTC.py
     * Demo for Raspberry Pi
     *
     * Copyright (c) 2014 seeed technology inc.
     * Website    : community.seeedstudio.com/
     * Author     : Lambor
     * Create Time: Nov 2014
     * Change Log :
     *
     * The MIT License (MIT)
     *
     * Permission is hereby granted, free of charge, to any person obtaining a copy
     * of this software and associated documentation files (the "Software"), to deal
     * in the Software without restriction, including without limitation the rights
     * to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
     * copies of the Software, and to permit persons to whom the Software is
     * furnished to do so, subject to the following conditions:
     *
     * The above copyright notice and this permission notice shall be included in
     * all copies or substantial portions of the Software.
     *
     * THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
     * IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
     * FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
     * AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
     * LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
     * OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
     * THE SOFTWARE.
     '''

    #!/usr/bin/python
import time
import smbus


    bus = smbus.SMBus(1)    # 0 = /dev/i2c-0 (port I2C0), 1 = /dev/i2c-1 (port I2C1)

class DS1307():
        def __init__(self):
            self.MON = 1
            self.TUE = 2
            self.WED = 3
            self.THU = 4
            self.FRI = 5
            self.SAT = 6
            self.SUN = 7
            self.DS1307_I2C_ADDRESS = 0x68

            print 'begin'

        def decToBcd(self, val):
            return ( (val/10*16) + (val%10) )

        def bcdToDec(self,  val):
            return ( (val/16*10) + (val%16) )

        def begin(self, news):
            print news

        def startClock(self):
            bus.write_byte(self.DS1307_I2C_ADDRESS, 0x00)
            self.second = bus.read_byte(self.DS1307_I2C_ADDRESS) & 0x7f
            bus.write_byte_data(self.DS1307_I2C_ADDRESS, 0x00, self.second)

            print 'startClock..'

        def stopClock(self):
            bus.write_byte(self.DS1307_I2C_ADDRESS, 0x00)
            self.second = bus.read_byte(self.DS1307_I2C_ADDRESS) | 0x80
            bus.write_byte_data(self.DS1307_I2C_ADDRESS, 0x00, self.second)

            print 'stopClock..'

        def setTime(self):
            data = [self.decToBcd(self.second), self.decToBcd(self.minute), \
                    self.decToBcd(self.hour), self.decToBcd(self.dayOfWeek), \
                    self.decToBcd(self.dayOfMonth), self.decToBcd(self.month), \
                    self.decToBcd(self.year)]

            bus.write_byte(self.DS1307_I2C_ADDRESS, 0x00)
            bus.write_i2c_block_data(self.DS1307_I2C_ADDRESS,0x00,data)

            print 'setTime..'

        def getTime(self):
            bus.write_byte(self.DS1307_I2C_ADDRESS, 0x00)
            data = bus.read_i2c_block_data(self.DS1307_I2C_ADDRESS,0x00)
            #A few of these need masks because certain bits are control bits
            self.second = self.bcdToDec(data[0] & 0x7f)
            self.minute = self.bcdToDec(data[1])
            self.hour = self.bcdToDec(data[2] & 0x3f)  #Need to change this if 12 hour am/pm
            self.dayOfWeek = self.bcdToDec(data[3])
            self.dayOfMonth = self.bcdToDec(data[4])
            self.month = self.bcdToDec(data[5])
            self.year = self.bcdToDec(data[6])

            print 'getTime..'

        def fillByHMS(self, _hour,  _minute,  _second):
            self.hour = _hour
            self.minute = _minute
            self.second = _second

            print 'fillByHMS..'

        def fillByYMD(self, _year,  _month,  _day):
            self.year = _year - 2000
            self.month = _month;
            self.dayOfMonth = _day

            print 'fillByYMD..'

        def fillDayOfWeek(self,  _dow):
            self.dayOfWeek = _dow

            print 'fillDayOfWeek..'

    if __name__ == "__main__":
        clock = DS1307()
        clock.fillByYMD(2015,3,5)
        clock.fillByHMS(12,42,30)
        clock.fillDayOfWeek(clock.THU)
        clock.setTime()
        while True:
            clock.getTime()
            print clock.hour, ":", clock.minute, ":", \
                    clock.second, " ", clock.dayOfMonth, "/", \
                    clock.month, "/", clock.year,"  ", "weekday", \
                    ":", clock.dayOfWeek
            time.sleep(1)
```

Spusťte následující příkazy

```bash
    sudo python grove_rtc.py
```

Výsledek je zde:

![](https://github.com/SeeedDocument/Grove-RTC/raw/master/img/rpi_display2.jpg)

## Zdroje

- **[Eagle]** [Grove-RTC in Eagle format](https://raw.githubusercontent.com/SeeedDocument/Grove-RTC/master/res/Real_Time_Clock.zip)
- **[PDF]** [Grove-RTC Schematic in PDF format](https://github.com/SeeedDocument/Grove-RTC/raw/master/res/Grove%20-%20RTC%20v1.1%20Sch.pdf)
- **[PDF]** [Grove-RTC PCB in PDF format](https://github.com/SeeedDocument/Grove-RTC/raw/master/res/Grove%20-%20RTC%20v1.1%20PCB.pdf)
- **[Knihovna]**[Github repository for RTC](https://github.com/Seeed-Studio/RTC_DS1307/archive/master.zip)
- **[Datasheet]** [DS1307 Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-RTC/master/res/DS1307.pdf)

## Projekty

**Hodiny reálného času s Arduinem**: Chcete si postavit zařízení, které bude fungovat podle rozvrhu? Použijte hodiny reálného času!

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/robotgeek-projects-team/using-a-real-time-clock-with-arduino-6b3896/embed' width='350'></iframe>

**Barevné hodiny**: Hodiny, které ukazují čas a reagují na váš příchod

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/zou-wei/colorful-clock-4cea6b/embed' width='350'></iframe>

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
