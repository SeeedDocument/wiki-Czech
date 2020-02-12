---
name: Grove - PIR Motion Sensor
category: Sensor
bzurl: https://www.seeedstudio.com/Grove-PIR-Motion-Sensor-p-802.html
oldwikiname: Grove - PIR Motion Sensor
prodimagename: Breakout_for_LinkIt_Smart_7688_v2.0_product_view_700.jpg
surveyurl: https://www.surveymonkey.com/r/grove-pir-motion-sensor
sku: 101020020
tags: io_3v3, io_5v, plat_duino, plat_pi
---

![](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/img/Grove_-_PIR_Motion_Sensor.jpg)

Toto čidlo detekuje pohyb člověka nebo větších zvířat. Jakmile se v blízkosti něco pohne, senzor nastaví výstup do stavu HIGH. Stačí jen připojit k Base Shieldu a naprogramovat.

<p style=":center"><a href="https://www.seeedstudio.com/Grove-PIR-Motion-Sensor-p-802.html" target="_blank"><img src="https://raw.githubusercontent.com/SeeedDocument/Seeed-WiKi/master/docs/images/get_one_now_small.png" width="210" height="41"  border=0 /></a></p>

## Vlastnosti

- Kompatibilní s rozhraním Grove
- Nastavitelná vzdálenost detekce
- Nastavitelná doba aktivace

!!!Tip
Více detailů o modulech Grove zjistíte v [popisu systému Grove](http://wiki.seeedstudio.com/Grove_System/)

## Specifikace

| Parametr                   | Hodnota / Rozsah |
| -------------------------- | ---------------- |
| Pracovní napětí            | 3V–5V            |
| Pracovní proud(VCC = 3V)   | 100uA            |
| Pracovní proud(VCC = 5V)   | 150uA            |
| Measuring Range            | 0.1 - 6m         |
| Default detecting distance | 3m               |
| Holding Time               | 1 - 25s          |
| Working Wave Length        | 7 - 14um         |
| Detecting Angle            | 120 degrees      |

## Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                               | BeagleBone                                                                                          | Wio                                                                                                 | LinkIt ONE                                                                                             |
| ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Začínáme

!!!Poznámka
Pokud se s Arduinem setkáváte poprvé, doporučujeme vám pročíst návod [Začínáme s Arduinem](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) dřív, než začnete.

### Pokusy s Arduinem

#### Hardware

- **Krok 1.** Připravte si tyto součástky:

| Seeeduino V4.2                                                                                                             | Grove - PIR Motion Sensor                                                                                                                        | Base Shield                                                                                                                |
| -------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/img/Grove%20-%20PIR%20Motion%20Sensor_s.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                            | [Koupit](https://www.seeedstudio.com/Grove-PIR-Motion-Sensor-p-802.html)                                                                         | [Koupit](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                           |

- **Krok 2.** Připojte Grove - PIR Motion Sensor k portu **D2** na Grove-Base Shieldu.

- **Krok 3.** Připojte Base Shield k Seeeduinu.

- **Krok 4.** Připojte Seeduino k PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/img/connect_arduino.jpg)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit Grove-PIR Motion Sensor k Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino   | Grove - PIR Motion Sensor |
| ----------- | ------------------------- |
| 5V          | Červený                   |
| GND         | Černý                     |
| Nepřipojeno | Bílý                      |
| D2          | Žlutý                     |

#### Software

- Zkopírujte následující kód do Arduino IDE, přeložte jej a nahrajte do Arduina. Pokud si nejste jisti, jak nahrát kód, podívejte se na stránku [Jak nahrát kód](http://wiki.seeedstudio.com/Upload_Code/).

```c
/*macro definitions of PIR motion sensor pin and LED pin*/
#define PIR_MOTION_SENSOR 2//Use pin 2 to receive the signal from the module


void setup()
{
    pinMode(PIR_MOTION_SENSOR, INPUT);
    Serial.begin(9600);

}

void loop()
{
    if(digitalRead(PIR_MOTION_SENSOR))//if it detects the moving people?
        Serial.println("Hi,people is coming");
    else
        Serial.println("Watching");

 delay(200);
}

```

!!!Poznámka
Vzdálenost detekce a čas, po který je výstup udržen ve stavu HIGH, lze nastavit přidáním dvou potenciometrů na desku. Detaily zjistíte ve schématu pro Eagle (níže). Rovněž jej můžete nastavit pomocí propojky tak, aby spouštěl i během aktivního stavu.

Uvidíte výsledek podobný tomuto:

![](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/img/result_arduino.png)

### Pokusy s Codecraftem

#### Hardware

**Krok 1.** Připojte Grove - PIR Motion Sensor k portu D2 na Grove-Base Shieldu

**Krok 2.** Připojte Base Shield k Seeeduinu / Arduinu.

**Krok 3.** Propojte Seeeduino/Arduino s PC pomocí kabelu USB.

#### Software

**Krok 1.** Spusťte [Codecraft](https://ide.chmakered.com/), přepněte se na prostředí pro Arduino a přidejte na plochu hlavní proceduru (Start).

!!!Poznámka
Pokud používáte Codecraft poprvé, podívejte se na [Průvodce světem Codecraftu a Arduina](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Krok 2.** Přetáhněte bloky tak, jak ukazuje následující obrázek, nebo otevřte cdc soubor, který si můžete stáhnout na konci této stránky.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove_PIR_Motion_Sensor/master/img/cc_PIR_Motion_Sensor.png)

Nahrajte hotový program do svého Arduina/Seeeduina.

!!!Povedlo se
Jakmile je nahrávání hotové, the LED will goes on when people is coming.

### Pokusy s Raspberry Pi (s Grove Base Hat)

#### Hardware

- **Krok 1**. Součástky, použité v tomto projektu:

| Raspberry pi                                                                                                   | Grove Base Hat for RasPi                                                                                                       | Grove - PIR Motion Sensor                                                                                                                        |
| -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/img/Grove%20-%20PIR%20Motion%20Sensor_s.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)                                              | [Koupit](https://www.seeedstudio.com/Grove-PIR-Motion-Sensor-p-802.html)                                                                         |

- **Krok 2**. Připojte Grove Base Hat k Raspberry Pi.
- **Krok 3**. Připojte PIR motion sensor k portu 12 na Base Hatu.
- **Krok 4**. Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/img/Motion_Hat.jpg)

!!! Poznámka
V kroku 3 můžete připojit the PIR motion sensor k **libovolnému GPIO portu**, ale ujistěte se, že jste změnili i číslo portu v kódu ukázky.

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
python grove_mini_pir_motion_sensor.py 12

```

Toto je kód v souboru grove_mini_pir_motion_sensor.py.

```python

import time
from grove.gpio import GPIO


class GroveMiniPIRMotionSensor(GPIO):
    def __init__(self, pin):
        super(GroveMiniPIRMotionSensor, self).__init__(pin, GPIO.IN)
        self._on_detect = None

    @property
    def on_detect(self):
        return self._on_detect

    @on_detect.setter
    def on_detect(self, callback):
        if not callable(callback):
            return

        if self.on_event is None:
            self.on_event = self._handle_event

        self._on_detect = callback

    def _handle_event(self, pin, value):
        if value:
            if callable(self._on_detect):
                self._on_detect()

Grove = GroveMiniPIRMotionSensor


def main():
    import sys

    if len(sys.argv) < 2:
        print('Usage: {} pin'.format(sys.argv[0]))
        sys.exit(1)

    pir = GroveMiniPIRMotionSensor(int(sys.argv[1]))

    def callback():
        print('Motion detected.')

    pir.on_detect = callback

    while True:
        time.sleep(1)


if __name__ == '__main__':
    main()

```

!!!Povedlo se
Pokud vše šlo tak, jak má, uvidíte výsledek podobný tomuto

```python

pi@raspberrypi:~/grove.py/grove $ python grove_mini_pir_motion_sensor.py 12
Motion detected.
Motion detected.
Motion detected.
^CTraceback (most recent call last):
  File "grove_mini_pir_motion_sensor.py", line 84, in <module>
    main()
  File "grove_mini_pir_motion_sensor.py", line 80, in main
    time.sleep(1)
KeyboardInterrupt

```

Program ukončíte stiskem ++ctrl+c++.

### Pokusy s Raspberry Pi (s modulem GrovePi_Plus)

#### Hardware

- **Krok 1.** Připravte si tyto součástky:

| Raspberry pi                                                                                                      | GrovePi_Plus                                                                                                            | Grove - PIR Motion Sensor                                                                                                                        |
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| ![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/Grovepi%2B.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/img/Grove%20-%20PIR%20Motion%20Sensor_s.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                          | [Koupit](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)                                                            | [Koupit](https://www.seeedstudio.com/Grove-PIR-Motion-Sensor-p-802.html)                                                                         |

- **Krok 2.** Připojte GrovePi_Plus k Raspberry Pi.

- **Krok 3.** Připojte sensor k portu **D8** na GrovePi_Plus.

- **Krok 4.** Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/img/connect_pi.jpg)

#### Software

- **Krok 1.** Nastavte si vývojové prostředí pomocí průvodce [nastavení software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/).

- **Krok 2.** Aktualizujte firmware pro GrovePi podle návodu [Updating the Firmware](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/updating-firmware/).

!!!Tip
V této wiki používáme cestu **~/GrovePi/** namísto **/home/pi/Desktop/GrovePi**. Ujistěte se, že v kroku 2 a 3 používáte stejné cesty.

!!!Poznámka
Doporučujeme provést aktualizaci firmware, některé senzory bez ní mohou vykazovat chybné výsledky.

- **Krok 3.** Stáhněte si zdrojový kód tím, že naklonujete knihovnu GrovePi.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

- **Krok 4.** Následujícími příkazy spustíte program pro monitorování pohybu

```
cd ~/GrovePi/Software/Python
sudo python grove_pir_motion_sensor.py
```

Toto je kód v souboru grove_pir_motion_sensor.py.

```python
import time
import grovepi

# Připojte Grove PIR Motion Sensor to digital port D8
# SIG,NC,VCC,GND
pir_sensor = 8

grovepi.pinMode(pir_sensor,"INPUT")

while True:
    try:
        # Sense motion, usually human, within the target range
        if grovepi.digitalRead(pir_sensor):
            print 'Motion Detected'
        else:
            print '-'

        # if your hold time is less than this, you might not see as many detections
        time.sleep(.2)

    except IOError:
        print "Error"
```

Uvidíte výsledek podobný tomuto:

```python
pi@raspberrypi:~/GrovePi/Software/Python $ sudo python grove_pir_motion_sensor.py

-
-
-
Motion Detected
Motion Detected
Motion Detected
Motion Detected
Motion Detected
Motion Detected
Motion Detected
Motion Detected
Motion Detected
Motion Detected
Motion Detected
-
-

```

## FAQ - Často kladené dotazy

**Ot. 1: Jak nastavit detekční vzdálenost?**

Odp. 1: Důležité jsou dva potenciometrické trimry. R2 slouží k nastavení detekční vzdálenosti (AMP koeficient, 2MΩ). R6 slouží k nastavení doby, po jakou je výstup udržován aktivní (časovací konstanta, 100KΩ).

Detekční vzdálenost můžete nastavit v rozsahu 6 metrů až několik centimetrů. Pokud nastavíte citlivost příliš vysokou, bude čidlo spínat jen prostým pohybem vzduchu, ani nikdo okolo něj nebude muset projít. Dobu trvání aktivace můžete nastavit v rozmezí od 25 sekund do 1 sekundy.

Pokud připojíte trimry R2 a R6, musíte odpájet rezistory R13 a R14.

!!!Poznámka
Při pájení můžete desku zničit, proto prosím zvažte, zda se do úpravy pustíte.

![](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/img/Resistor.png)

## Zdroje

- **[Eagle]** [Grove - PIR Motion Sensor Eagle File v1.2](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/res/Grove%20PIR%20Motion%20Sensor_v1_2.zip)
- **[PDF]** [Grove - PIR Motion Sensor v1.2 Schematics](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/resources/Grove_PIR_Sensor_v1.2.pdf)
- **[PDF]** [Grove - PIR Motion Sensor Eagle V1.2 PCB](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/res/Grove%20-%20PIR%20motion%20sensor%20v1.1b%20PCB.pdf)
- **[Knihovna]** [Github repository for PIR Motion Sensor](https://github.com/Seeed-Studio/PIR_Motion_Sensor)
- **[Datasheet]** [BISS0001 Datasheet](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/resources/Twig_-_BISS0001.pdf)
- **[Datasheet]** [Fresnel lens 8120 Datasheet](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/resources/Fresnel_lens_8120.pdf)
- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove_PIR_Motion_Sensor/master/res/Grove_PIR_Motion_Sensor_CDC_File.zip)

## Projekty

**Alarm proti zlodějům s PIR senzorem**: Článek popisuje jednoduchý poplašný systém proti zlodějům.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/pooja_baraskar/burglar-alarm-with-pir-motion-sensor-964c42/embed' width='350'></iframe>

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
