---
name: Grove - Temperature&Humidity Sensor
category: Sensor
bzurl: https://www.seeedstudio.com/Grove-Temp&Humi-Sensor-p-745.html
oldwikiname: Grove_-_Temperature&Humidity_Sensor
prodimagename: Grove-TempAndHumiSensor.jpg
bzprodimageurl: https://statics3.seeedstudio.com/images/101020011 1.jpg
surveyurl: https://www.research.net/r/Grove-TemperatureAndHumidity_Sensor
sku: 101020011
---

![](https://github.com/SeeedDocument/Grove-TemperatureAndHumidity_Sensor/raw/master/img/main.jpg)

Modul obsahuje kalibrovaný výstup pro teplotu a vlhkost. Kapacitní snímač měří relativní vlhkost vzduchu, teplota je měřena termistorem. Obvod je spolehlivý a dlouhodobě stabilní. Upozornění: tento senzor nepracuje při teplotách pod bodem mrazu.

<p style=":center"><a href="https://www.seeedstudio.com/Grove-Temperature-Humidity-Sensor-DHT1-p-745.html" target="_blank"><img src="https://raw.githubusercontent.com/SeeedDocument/Seeed-WiKi/master/docs/images/get_one_now_small.png" width="210" height="41"  border=0 /></a></p>

## Vlastnosti

---

- Měření teploty a relativní vlhkosti vzduchu
- Kalibrováno v celém teplotním rozsahu
- Digitální výstup
- Dlouhodobá stabilita
- Signál lze přenášet na velkou vzdálenost (>20m)
- Nízký odběr

!!!Tip
Více detailů o modulech Grove zjistíte v [popisu systému Grove](http://wiki.seeedstudio.com/Grove_System/)

## Použití

---

- Spotřební elektronika
- Měření počasí
- Regulace vlhkosti
- Klimatizace

## Specifikace

---

### Hlavní parametry

| Parametr | Min                    |
| -------- | ---------------------- |
| PCB Size | 2.0cm\*4.0cm           |
| Rozhraní | 2.0mm pitch pin header |
| Vývody   | SIG,VCC,GND,NC         |
| ROHS     | Ano                    |

## Elektrické vlastnosti

<table border="1">
<tr>
<th>
Parametr
</th>
<th>
Podmínky
</th>
<th>
Min
</th>
<th>
Norm
</th>
<th>
Max
</th>
<th>
Jednotka
</th>
</tr>
<tr align="center">
<td>
VCC
</td>
<td>
-
</td>
<td>
3.3
</td>
<td>
-
</td>
<td>
5
</td>
<td>
Volts
</td>
</tr>
<tr align="center">
<td>
Odběr při měření
</td>
<td>
-
</td>
<td>
1.3 
</td>
<td>
- 
</td>
<td>
2.1
</td>
<td>
mA
</td>
</tr>
<tr align="center">
<td>
Průměrný odběr
</td>
<td>
-
</td>
<td>
0.5
</td>
<td>
-
</td>
<td>
1.1
</td>
<td>
mA
</td>
</tr>
<tr align="center">
<td rowspan="2">
Rozsah měření
</td>
<td>
Vlhkost
</td>
<td>
20%
</td>
<td>
-
</td>
<td>
90%
</td>
<td>
RH
</td>
</tr>
<tr align="center">
<td>
Teplota
</td>
<td>
0
</td>
<td>
-
</td>
<td>
50
</td>
<td>
°C
</td>
</tr>
<tr align="center">
<td rowspan="2">
Přesnost
</td>
<td>
Vlhkost
</td>
<td>
-
</td>
<td>
-
</td>
<td>
±5%
</td>
<td>
RH
</td>
</tr>
<tr align="center">
<td>
Teplota
</td>
<td>
</td>
<td>
</td>
<td>
±2
</td>
<td>
°C
</td>
</tr>
<tr align="center">
<td rowspan="2">
 Citlivost
</td>
<td>
Vlhkost
</td>
<td>
</td>
<td>
-
</td>
<td>
1%
</td>
<td>
RH
</td>
</tr>
<tr align="center">
<td>
Teplota
</td>
<td>
</td>
<td>
</td>
<td>
1
</td>
<td>
°C
</td>
</tr>
<tr align="center">
<td rowspan="2">
Opakovatelnost
</td>
<td>
Vlhkost
</td>
<td>
</td>
<td>
</td>
<td>
±1%
</td>
<td>
RH
</td>
</tr>
<tr align="center">
<td>
Teplota
</td>
<td>
</td>
<td>
</td>
<td>
±1
</td>
<td>
°C
</td>
</tr>
<tr align="center">
<td>
Dlouhodobá stabilita
</td>
<td>
</td>
<td>
</td>
<td>
</td>
<td>
±1%
</td>
<td>
RH/rok
</td>
</tr>
<tr align="center">
<td>
Interval měření
</td>
<td>
</td>
<td>
</td>
<td>
2
</td>
<td>
</td>
<td>
s
</td>
</tr>
</table>

## Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                               | BeagleBone                                                                                          | Wio                                                                                               | LinkIt ONE                                                                                             |
| ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Poznámka
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

Getting Started

Když procesor pošle spouštěcí signál, snímač se probudí a aktivuje. Poté odpoví potvrzovacím signálem. Po něm pošle 40 bitů naměřených informací a začne cyklus měření. (Všimněte si, že poslaná data odpovídají předchozímu měření, nové měření začne až po jejich odeslání.) Jeden spouštěcí signál vrátí vždy jednu sadu 40 bitů informací. Pro komunikaci se používá jediný vodič.
Komunikační proces ukazuje obrázek:

![](https://raw.githubusercontent.com/SeeedDocument/Grove-TemperatureAndHumidity_Sensor/master/img/Twig-Temperature_Humidity.jpg)

Jedna komunikace zabere 5 ms. Jako první se posílá nejvyšší bit. Data se skládají z 16 bitů informace o vlhkosti, 16 bitů informace o teplotě a 8 bitů kontrolního součtu. Formát dat je:

    8 bitů celá část hodnoty vlhkosti + 8 bitůdesetinná část hodnoty vlhkosti
    + 8 bitů celá část teploty + 8 bitů desetinná část teploty
    +8 bitů kontrolního součtu.

!!!Poznámka
Pokud se s Arduinem setkáváte poprvé, doporučujeme vám pročíst návod [Začínáme s Arduinem](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) dřív, než začnete.

### Pokusy s Arduinem

#### Hardware

- **Krok 1.** Připravte si tyto součástky:

| Seeeduino V4.2                                                                                                             | Base Shield                                                                                                                | Temperature&Humidity Sensor                                                                                                   |
| -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-TemperatureAndHumidity_Sensor/raw/master/img/list.jpg) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                            | [Koupit](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                           | [Koupit](https://www.seeedstudio.com/Grove-Temp%26Humi-Sensor-p-745.html)                                                     |

- **Krok 2.** Připojte Grove - Temperature&Humidity Sensor k portu **D2** na Grove-Base Shieldu.

- **Krok 3.** Připojte Base Shield k Seeeduinu.

- **Krok 4.** Připojte Seeduino k PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-TemperatureAndHumidity_Sensor/raw/master/img/connect_arduino.jpg)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit Grove - Temperature and Humidity Sensor Pro k Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino   | Temperature&Humidity Sensor |
| ----------- | --------------------------- |
| 5V          | Červený                     |
| GND         | Černý                       |
| Nepřipojeno | Bílý                        |
| D2          | Žlutý                       |

#### Software

Ukázkový program měří teplotu a vlhkost vzduchu a údaje vypisuje na sériový monitor.

- **Krok 1.** Stáhněte si knihovnu [ Seeed DHT library](https://github.com/Seeed-Studio/Grove_Temperature_And_Humidity_Sensor) z GitHubu.

- **Krok 2.** S instalací knihovny pro Arduino vám pomůže návod [Jak instalovat knihovnu pro Arduino](http://wiki.seeedstudio.com/How_to_install_Arduino_Library).

- **Krok 3.** Restartujte Arduino IDE. Otevřte soubor “ DHTtester” následujícím postupem: **File --> Examples --> Grove_Humidity_Temperature_Sensor-master --> DHTtester**.

![](https://github.com/SeeedDocument/Grove-Temperature_and_Humidity_Sensor_Pro/raw/master/img/path.png)

!!!Poznámka
Snímač Grove - Temperature&Humidity Sensor a vylepšená verze [Grove-Temperature&Humidity Sensor pro](http://wiki.seeedstudio.com/Grove-Temperature_and_Humidity_Sensor_Pro/) používají tutéž knihovnu. Nezáleží na tom, jaký modul použijete, jen se ujistěte, že na začátku souboru správně nastavíte hodnotu konstanty DHTTYPE. Pro tento senzor je to DHT11. Specifikace typu snímače může v programu vypadat třeba takto:

```
#define DHTTYPE DHT11   // DHT 11
//#define DHTTYPE DHT22   // DHT 22  (AM2302)
//#define DHTTYPE DHT21   // DHT 21 (AM2301)
```

Přednastavený typ je `DHT 22`, takže budete muset změnit hodnotu na `DHT 11` ručně.

- **Krok 4.** Nahrajte přeložený kód do Arduina. Pokud si nejste jisti, jak nahrát kód, podívejte se na stránku [Jak nahrát kód](http://wiki.seeedstudio.com/Upload_Code/).

* **Krok 5.** Otevřte **Sériový monitor** v Arduino IDE kliknutím na **Tool-> Serial Monitor**, nebo použijte klávesovou zkratku ++ctrl+shift+m++. Pokud vše funguje jak má, na displeji uvidíte teplotu a vlhkost.

Uvidíte výsledek podobný tomuto:

![](https://github.com/SeeedDocument/Grove-TemperatureAndHumidity_Sensor/raw/master/img/result_ar.png)

### Pokusy s Codecraftem

#### Hardware

**Krok 1.** Připojte Grove - Temperature&Humidity Sensor k portu D2 a Base Shield.

**Krok 2.** Připojte Base Shield k Seeeduinu / Arduinu.

**Krok 3.** Propojte Seeeduino/Arduino s PC pomocí kabelu USB.

#### Software

**Krok 1.** Spusťte [Codecraft](https://ide.chmakered.com/), přepněte se na prostředí pro Arduino a přidejte na plochu hlavní proceduru (Start).

!!!Poznámka
Pokud používáte Codecraft poprvé, podívejte se na [Průvodce světem Codecraftu a Arduina](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Krok 2.** Přetáhněte bloky tak, jak ukazuje následující obrázek, nebo otevřte cdc soubor, který si můžete stáhnout na konci této stránky.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove-TemperatureAndHumidity_Sensor/master/img/cc_Temperature_Humidity.png)

Nahrajte hotový program do svého Arduina/Seeeduina.

!!!Povedlo se
Jakmile je nahrávání hotové, v Sériovém monitoru uvidíte teplotu a vlhkost.

### Pokusy s Raspberry Pi (s Grove Base Hat)

#### Hardware

- **Krok 1**. Součástky, použité v tomto projektu:

| Raspberry pi                                                                                                   | Grove Base Hat for RasPi                                                                                                       | Grove - Temp & Hum Sensor                                                                                                     |
| -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-TemperatureAndHumidity_Sensor/raw/master/img/list.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)                                              | [Koupit](https://www.seeedstudio.com/Grove-Temp%26Humi-Sensor-p-745.html)                                                     |

- **Krok 2**. Připojte Grove Base Hat k Raspberry Pi.
- **Krok 3**. Připojte temperature and humidity sensor to Port 12 of the Base Hat.
- **Krok 4**. Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-TemperatureAndHumidity_Sensor/raw/master/img/Temp_Hum_Hat.jpg)

!!! Poznámka
V kroku 3 můžete připojit tento snímač k **libovolnému GPIO portu**, ale ujistěte se, že jste změnili i číslo portu v kódu ukázky.

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
python grove_temperature_humidity_sensor.py 11 12

```

!!!Poznámka 1
Pro spuštění tohoto programu použijte příkaz +++python grove_temperature_humidity_sensor.py DHT type pin+++. U tohoto modulu je DHT typ 11 a pin 12. As for this module, DHT type is 11 and we connected temperature and humidity sensor to pin 12 in the above case.

!!!Poznámka 2

Snímač Grove - Temperature&Humidity Sensor a vylepšená verze [Grove-Temperature&Humidity Sensor pro](http://wiki.seeedstudio.com/Grove-Temperature_and_Humidity_Sensor_Pro/) používají tutéž knihovnu jménem 'grove_temperature_humidity_sensor.py'. Jediný rozdíl je v tom, že tento senzor má typ 11 a verze Pro má typ 22.

Toto je kód v souboru grove_temperature_humidity_sensor.py.

```python

import RPi.GPIO as GPIO
# from grove.helper import *
def set_max_priority(): pass
def set_default_priority(): pass
from time import sleep

GPIO.setmode(GPIO.BCM)
GPIO.setwarnings(False)

PULSES_CNT = 41

class DHT(object):
    DHT_TYPE = {
        'DHT11': '11',
        'DHT22': '22'
    }

    MAX_CNT = 320

    def __init__(self, dht_type, pin):
        self.pin = pin
        if dht_type != self.DHT_TYPE['DHT11'] and dht_type != self.DHT_TYPE['DHT22']:
            print('ERROR: Please use 11|22 as dht type.')
            exit(1)
        self._dht_type = '11'
        self.dht_type = dht_type
        GPIO.setup(self.pin, GPIO.OUT)

    @property
    def dht_type(self):
        return self._dht_type

    @dht_type.setter
    def dht_type(self, type):
        self._dht_type = type
        self._last_temp = 0.0
        self._last_humi = 0.0

    def _read(self):
        # Send Falling signal to trigger sensor output data
        # Wait for 20ms to collect 42 bytes data
        GPIO.setup(self.pin, GPIO.OUT)
        set_max_priority()

        GPIO.output(self.pin, 1)
        sleep(.2)

        GPIO.output(self.pin, 0)
        sleep(.018)

        GPIO.setup(self.pin, GPIO.IN)
        # a short delay needed
        for i in range(10):
            pass

        # pullup by host 20-40 us
        count = 0
        while GPIO.input(self.pin):
            count += 1
            if count > self.MAX_CNT:
                # print("pullup by host 20-40us failed")
                set_default_priority()
                return None, "pullup by host 20-40us failed"

        pulse_cnt = [0] * (2 * PULSES_CNT)
        fix_crc = False
        for i in range(0, PULSES_CNT * 2, 2):
            while not GPIO.input(self.pin):
                pulse_cnt[i] += 1
                if pulse_cnt[i] > self.MAX_CNT:
                    # print("pulldown by DHT timeout %d" % i)
                    set_default_priority()
                    return None, "pulldown by DHT timeout %d" % i

            while GPIO.input(self.pin):
                pulse_cnt[i + 1] += 1
                if pulse_cnt[i + 1] > self.MAX_CNT:
                    # print("pullup by DHT timeout %d" % (i + 1))
                    if i == (PULSES_CNT - 1) * 2:
                        # fix_crc = True
                        # break
                        pass
                    set_default_priority()
                    return None, "pullup by DHT timeout %d" % i

        # back to normal priority
        set_default_priority()

        total_cnt = 0
        for i in range(2, 2 * PULSES_CNT, 2):
            total_cnt += pulse_cnt[i]

        # Low level ( 50 us) average counter
        average_cnt = total_cnt / (PULSES_CNT - 1)
        # print("low level average loop = %d" % average_cnt)

        data = ''
        for i in range(3, 2 * PULSES_CNT, 2):
            if pulse_cnt[i] > average_cnt:
                data += '1'
            else:
                data += '0'

        data0 = int(data[ 0: 8], 2)
        data1 = int(data[ 8:16], 2)
        data2 = int(data[16:24], 2)
        data3 = int(data[24:32], 2)
        data4 = int(data[32:40], 2)

        if fix_crc and data4 != ((data0 + data1 + data2 + data3) & 0xFF):
            data4 = data4 ^ 0x01
            data = data[0: PULSES_CNT - 2] + ('1' if data4 & 0x01 else '0')

        if data4 == ((data0 + data1 + data2 + data3) & 0xFF):
            if self._dht_type == self.DHT_TYPE['DHT11']:
                humi = int(data0)
                temp = int(data2)
            elif self._dht_type == self.DHT_TYPE['DHT22']:
                humi = float(int(data[ 0:16], 2)*0.1)
                temp = float(int(data[17:32], 2)*0.2*(0.5-int(data[16], 2)))
        else:
            # print("checksum error!")
            return None, "checksum error!"

        return humi, temp

    def read(self, retries = 15):
        for i in range(retries):
            humi, temp = self._read()
            if not humi is None:
                break
        if humi is None:
            return self._last_humi, self._last_temp
        self._last_humi,self._last_temp = humi, temp
        return humi, temp

Grove = DHT


def main():
    import sys
    import time

    if len(sys.argv) < 3:
        print('Usage: {} dht_type pin'.format(sys.argv[0]))
        sys.exit(1)

    typ = sys.argv[1]
    sensor = DHT(typ, int(sys.argv[2]))

    while True:
        humi, temp = sensor.read()
        if not humi is None:
            print('DHT{0}, humidity {1:.1f}%, temperature {2:.1f}*'.format(sensor.dht_type, humi, temp))
        else:
            print('DHT{0}, humidity & temperature: {1}'.format(sensor.dht_type, temp))
        time.sleep(1)


if __name__ == '__main__':
    main()



```

!!!Povedlo se
Pokud vše šlo tak, jak má, uvidíte výsledek podobný tomuto

```python

pi@raspberrypi:~/grove.py/grove $ python grove_temperature_humidity_sensor.py 11 12
DHT11, humidity 31.0%, temperature 22.0*
DHT11, humidity 30.0%, temperature 23.0*
DHT11, humidity 29.0%, temperature 23.0*
^CTraceback (most recent call last):
  File "grove_temperature_humidity_sensor.py", line 192, in <module>
    main()
  File "grove_temperature_humidity_sensor.py", line 188, in main
    time.sleep(1)
KeyboardInterrupt


```

Program ukončíte stiskem ++ctrl+c++.

### Pokusy s Raspberry Pi (s modulem GrovePi_Plus)

#### Hardware

- **Krok 1.** Připravte si tyto součástky:

| Raspberry pi                                                                                                      | GrovePi_Plus                                                                                                            | Temperature&Humidity Sensor                                                                                                   |
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/Grovepi%2B.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-TemperatureAndHumidity_Sensor/raw/master/img/list.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                          | [Koupit](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)                                                            | [Koupit](https://www.seeedstudio.com/Grove-Temperature%26Humidity-Sensor-Pro-p-838.html)                                      |

- **Krok 2.** Připojte GrovePi_Plus k Raspberry Pi.

- **Krok 3.** Připojte Grove - Temperature&Humidity Sensor k portu **D4** na GrovePi_Plus.

- **Krok 4.** Připojte Raspberry to PC via USB cable.

![](https://github.com/SeeedDocument/Grove-TemperatureAndHumidity_Sensor/raw/master/img/connect_pi.jpg)

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

- **Krok 4.** Zkontrolujte kód.

```python

cd ~/GrovePi/Software/Python
sudo nano grove_dht_pro.py

```

Měl by vypadat takto:

```python
import grovepi
import math
# Připojte Grove Temperature & Humidity Sensor Pro to digital port D4
# This example uses the blue colored sensor.
# SIG,NC,VCC,GND
sensor = 4  # The Sensor goes on digital port 4.

# temp_humidity_sensor_type
# Grove Base Kit comes with the blue sensor.
blue = 0    # The Blue colored sensor.
white = 1   # The White colored sensor.

while True:
    try:
        # This example uses the blue colored sensor.
        # The first parameter is the port, the second parameter is the type of sensor.
        [temp,humidity] = grovepi.dht(sensor,blue)
        if math.isnan(temp) == False and math.isnan(humidity) == False:
            print("temp = %.02f C humidity =%.02f%%"%(temp, humidity))

    except IOError:
        print ("Error")

```

Stiskem ++ctrl+x++ ukončíte editor.

!!!Poznámka

Snímač Grove - Temperature&Humidity Sensor a vylepšená verze [Grove-Temperature&Humidity Sensor pro](http://wiki.seeedstudio.com/Grove-Temperature_and_Humidity_Sensor_Pro/) používají tutéž knihovnu jménem `grove_dht_pro.py`. Jediný rozdíl je v nastavení hodnot `[temp,humidity] = grovepi.dht(sensor,blue)`. Pro tento senzor používáme hodnotu
`blue`, pro verzi Pro hodnotu `white`. Výchozí hodnota je `blue`, takže nemusíte nic měnit.

- **Krok 5.** Spusťte následující příkazy.

```
sudo python grove_dht_pro.py
```

Uvidíte výsledek podobný tomuto:

```python

pi@raspberrypi:~/GrovePi/Software/Python $ sudo python grove_dht_pro.py
temp = 26.00 C humidity =40.00%
temp = 26.00 C humidity =40.00%
temp = 26.00 C humidity =40.00%
temp = 26.00 C humidity =40.00%
temp = 26.00 C humidity =40.00%
temp = 26.00 C humidity =40.00%
temp = 26.00 C humidity =40.00%
temp = 26.00 C humidity =40.00%
temp = 26.00 C humidity =40.00%
temp = 26.00 C humidity =40.00%
temp = 26.00 C humidity =40.00%
temp = 26.00 C humidity =40.00%

```

## Zdroje

- **[Zip]** [Temperature&Humidity Sensor eagle file](https://raw.githubusercontent.com/SeeedDocument/Grove-TemperatureAndHumidity_Sensor/master/res/Temperature_Humidity.zip)

- **[Zip]** [Temperature&Humidity Sensor Library](https://github.com/Seeed-Studio/Grove_Temperature_And_Humidity_Sensor)

- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove-TemperatureAndHumidity_Sensor/master/res/Grove_Temperature_and_Humidity_Sensor_CDC_File.zip)

## Projekty

**Správa toalet**: Využívejte sdílené toalety efektivně.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://project.seeedstudio.com/taifur/toilet-management-system-8e2786/embed' width='350'></iframe>

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
