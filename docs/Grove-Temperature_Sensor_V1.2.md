---
name: Grove - Temperature Sensor V1.2
category: Sensor
bzurl: https://www.seeedstudio.com/Grove-Temperature-Sensor-p-774.html
oldwikiname: Grove - Temperature Sensor V1.2
prodimagename: Grove_Temperature_Sensor_View.jpg
surveyurl: https://www.surveymonkey.com/r/Grove-Temperature_Sensor_V1-2
sku: 101020015
tags: io_3v3, io_5v, plat_duino
---

<p style=":center"><img src="https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/img/Grove_Temperature_Sensor_View.jpg" ></p>

Snímač teploty (Grove - Temperature Sensor) používá takzvaný  [termistor](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/res/NCP18WF104F03RC.pdf) k měření teploty okolí. Elektrický odpor termistoru roste, když se teplota okolí zmenšuje. Díky známému vztahu mezi teplotou a odporem můžeme změřit teplotu okolního prostředí. Rozsah tohoto snímače je -40 až +125ºC a přesnost je ±1.5ºC

Poznámka: Tato stránka popisuje Grove - Temperature sensor V1.1 a vyšší, popis verze V1.0 naleznete zde: [Grove - Temperature Sensor](http://wiki.seeedstudio.com/Grove-Temperature_Sensor)

<p style=":center"><a href="https://www.seeedstudio.com/Grove-Temperature-Sensor-p-774.html" target="_blank"><img src="https://raw.githubusercontent.com/SeeedDocument/Seeed-WiKi/master/docs/images/get_one_now_small.png" width="210" height="41"  border=0 /></a></p>

## Specifikace

---

- Napětí: 3.3 ~ 5V
- Klidový odpor: 100 kΩ
- Přesnost: ±1%
- Provozní teplota: -40 ~ +125 ℃
- Teplotní konstanta B： 4250 ~ 4299K

!!!Tip
Více detailů o modulech Grove zjistíte v [popisu systému Grove](http://wiki.seeedstudio.com/Grove_System/)

## Podporované platformy

---

| Arduino                                                                                               | Raspberry Pi                                                                                               | BeagleBone                                                                                          | Wio                                                                                                 | LinkIt ONE                                                                                             |
| ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Začínáme

---

Jak použít Grove - Temperature Sensor V1.1/1.2 během několika kroků

!!!Poznámka
Pokud se s Arduinem setkáváte poprvé, doporučujeme vám pročíst návod [Začínáme s Arduinem](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) dřív, než začnete.

### Pokusy s Arduinem

#### Hardware

- **Krok 1.** Připravte si tyto součástky:

| Seeeduino V4.2                                                                                                             | Base Shield                                                                                                                | Grove - Temperature Sensor                                                                                                                              |
| -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/img/Grove_Temperature_Sensor_View_little.jpg) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                            | [Koupit](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                           | [Koupit](https://www.seeedstudio.com/Grove-Temperature-Sensor-p-774.html)                                                                               |

- **Krok 2.** Připojte Grove - Temperature Sensor k portu **A0** na Grove-Base Shieldu.

- **Krok 3.** Připojte Base Shield k Seeeduinu.

- **Krok 4.** Připojte Seeduino k PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/img/connect_Arduino.jpg)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit Grove_Ultrasonic_Ranger k Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino   | Grove - Temperature Sensor |
| ----------- | -------------------------- |
| 5V          | Červený                    |
| GND         | Černý                      |
| Nepřipojeno | Bílý                       |
| A0          | Žlutý                      |

#### Software

- **Krok 1.** Spusťte Arduino IDE a vytvořte nový projekt kliknutím na **File>New** (Soubor / Nový). Zkopírujte následující kód do editoru, uložte, přeložte a nahrajte.  Pokud si nejste jisti, jak nahrát kód, podívejte se na stránku [Jak nahrát kód](http://wiki.seeedstudio.com/Upload_Code/).

```
// Demo code for Grove - Temperature Sensor V1.1/1.2
// Loovee @ 2015-8-26

#include <math.h>

const int B = 4275;               // B value of the thermistor
const int R0 = 100000;            // R0 = 100k
const int pinTempSensor = A0;     // Grove - Temperature Sensor connect to A0

void setup()
{
    Serial.begin(9600);
}

void loop()
{
    int a = analogRead(pinTempSensor);

    float R = 1023.0/a-1.0;
    R = R0*R;

    float temperature = 1.0/(log(R/R0)/B+1/298.15)-273.15; // convert to temperature via datasheet

    Serial.print("temperature = ");
    Serial.println(temperature);

    delay(100);
}
```

**Krok 2.** Otevřete **Sériový Monitor** v Arduino IDE kliknutím na **Tool-> Serial Monitor**. Můžete použít klávesovou zkratku ++ctrl+shift+m++.

Uvidíte výsledek podobný tomuto:

![](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/img/Grove_Temperature_Sensor_result.jpg)

### Pokusy s Raspberry Pi (s Grove Base Hat)

#### Hardware

- **Krok 1**. Součástky, použité v tomto projektu:

| Raspberry pi                                                                                                   | Grove Base Hat for RasPi                                                                                                       | Grove - Temperature Sensor                                                                                                                              |
| -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/img/Grove_Temperature_Sensor_View_little.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)                                              | [Koupit](https://www.seeedstudio.com/Grove-Temperature-Sensor-p-774.html)                                                                               |

- **Krok 2**. Připojte Grove Base Hat k Raspberry Pi.
- **Krok 3**. Připojte temperature sensor k portu A0 na Base Hatu.
- **Krok 4**. Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/img/Temperature_Hat.jpg)

!!! Poznámka
V kroku 3 můžete připojit snímač teploty k **libovolnému analogovému portu**, ale nezapomeňte změnit příslušnou hodnotu v kódu.

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
python grove_temperature_sensor.py 0

```

Toto je kód v souboru grove_temperature_sensor.py.

```python

import sys
import time
from grove.factory import Factory


def main():
    from grove.helper import SlotHelper
    sh = SlotHelper(SlotHelper.ADC)
    pin = sh.argv2pin()

    sensor = Factory.getTemper("NTC-ADC", pin)

    print('Detecting temperature...')
    while True:
        print('{} Celsius'.format(sensor.temperature))
        time.sleep(1)


if __name__ == '__main__':
    main()

```

!!!Povedlo se
Pokud vše šlo tak, jak má, uvidíte výsledek podobný tomuto

```python

pi@raspberrypi:~/grove.py/grove $ python grove_temperature_sensor.py 0
Hat Name = 'Grove Base Hat RPi'
Detecting temperature...
24.7473402633 Celsius
24.7473402633 Celsius
24.7473402633 Celsius
24.7112751977 Celsius
24.7112751977 Celsius
^CTraceback (most recent call last):
  File "grove_temperature_sensor.py", line 53, in <module>
    main()
  File "grove_temperature_sensor.py", line 49, in main
    time.sleep(1)
KeyboardInterrupt

```

Program ukončíte stiskem ++ctrl+c++.

!!!Poznámka
Možná jste si všimli, že analogové porty jsou na desce popsány jako **A1, A0**, i když v programu používáme jako parametry **0** a **1**, stejně jako u digitálních portů. Ujistěte se proto, že připojujete modul ke správným portům, jinak nebude zapojení fungovat.


### Pokusy s Raspberry Pi (s modulem GrovePi_Plus)

#### Hardware

- **Krok 1.** Připravte si tyto součástky:

| Raspberry pi                                                                                                      | GrovePi_Plus                                                                                                            | Grove - Temperature Sensor                                                                                                                              |
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/Grovepi%2B.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/img/Grove_Temperature_Sensor_View_little.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                          | [Koupit](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)                                                            | [Koupit](https://www.seeedstudio.com/Grove-Temperature-Sensor-p-774.html)                                                                               |

- **Krok 2.** Připojte GrovePi_Plus k Raspberry Pi.

- **Krok 3.** Připojte Grove - Temperature Sensor ranger to **A0** na GrovePi_Plus.

- **Krok 4.** Připojte Raspberry to PC via USB cable.

![](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/img/connect_pi.jpg)

#### Software

- **Krok 1.** Nastavte si vývojové prostředí pomocí průvodce [nastavení software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/).

- **Krok 2.** Aktualizujte firmware pro GrovePi podle návodu [Updating the Firmware](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/updating-firmware/).


!!!Tip
V tomto návodu používáme cestu **~/GrovePi/** místo **/home/pi/Desktop/GrovePi**, ujistěte se, že v krocích 2 a 3 používáte stejnou.

!!!Poznámka
Doporučujeme provést aktualizaci firmware, některé senzory bez ní mohou vykazovat chybné výsledky.

- **Krok 3.** Stáhněte si zdrojový kód tím, že naklonujete knihovnu GrovePi.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

- **Krok 4.** Spusťte následující příkazy.

```
cd ~/GrovePi/Software/Python
sudo python grove_temperature_sensor.py
```

Toto je kód v souboru grove_temperature_sensor.py.

```python

# NOTE:
# 	The sensor uses a thermistor to detect ambient temperature.
# 	The resistance of a thermistor will increase when the ambient temperature decreases.
#
# 	There are 3 Revizes 1.0, 1.1 and 1.2, each using a different model thermistor.
# 	Each thermistor datasheet specifies a unique Nominal B-Constant which is used in the calculation forumla.
#
# 	The second argument in the grovepi.temp() method defines which board version you have connected.
# 	Defaults to '1.0'. eg.
# 		temp = grovepi.temp(sensor)        # B value = 3975
# 		temp = grovepi.temp(sensor,'1.1')  # B value = 4250
# 		temp = grovepi.temp(sensor,'1.2')  # B value = 4250

import time
import grovepi

# Připojte Grove Temperature Sensor to analog port A0
# SIG,NC,VCC,GND
sensor = 0

while True:
    try:
        temp = grovepi.temp(sensor,'1.2')
        print("temp =", temp)
        time.sleep(.5)

    except KeyboardInterrupt:
        break
    except IOError:
        print ("Error")

```

Uvidíte výsledek podobný tomuto:

```python

pi@raspberrypi:~/GrovePi/Software/Python $ sudo python grove_temperature_sensor.py

('temp =', 25.28652137917777)
('temp =', 25.28652137917777)
('temp =', 25.28652137917777)
('temp =', 25.28652137917777)
('temp =', 25.368489566400115)
('temp =', 25.61468397498203)
('temp =', 27.43501590142614)
('temp =', 27.85285590636829)
('temp =', 27.18509952680688)
('temp =', 26.852756540240193)

```

## Reference

---

Vysvětlení toho, jak funguje přepočet odporu na teplotu:

![](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/img/Grove_Temperature_Sensor_Basic_Characteristics.jpg)

## Zdroje

---

- **[Zip]** [Grove - Temperature Sensor v1.1 Eagle File](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/res/Grove_-_Temperature_sensor_v1.1.zip)
- **[PDF]** [Grove - Temperature Sensor v1.1.PDF](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/res/Grove_-_Temperature_sensor_v1.1.pdf)
- **[PDF]** [Temperature Sensor datasheet](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/res/NCP18WF104F03RC.pdf)

## Projekty

**Temperature sensor Grove module**:

<iframe width="560" height="315" src="https://www.youtube.com/embed/wjL7xOGqAqg" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/vI9pkmiK8EM" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
