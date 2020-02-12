---
name: Grove - Switch(P)
category: Sensor
bzurl: https://seeedstudio.com/Grove-Switch(P)-p-1252.html
oldwikiname: Grove_-_Switch(P)
prodimagename: GroveSwitchP_01.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/product/GroveSwitchP.jpg
surveyurl: https://www.research.net/r/Grove-Switch-P
sku: 101020004
tags: grove_digital, io_3v3, io_5v, plat_duino, plat_linkit, plat_pi, plat_bbg
---

![](https://github.com/SeeedDocument/Grove-Switch-P/raw/master/img/switch_p.jpg)

Tento přepínač (Grove – Switch(P)) je miniaturní posuvný přepínač SPDT, vhodný všude tam, kde je nutno něco trvale zapnout nebo vypnout. Je to spolehlivý přepínač se solidním zpracováním, který sami používáme v mnoha výrobcích. Měli byste jich mít několik vždy po ruce.

Mimochodem, co znamená to “P”? “P” znamená “panel mount”, tedy vhodné k montáži na panel přístroje zespodu.

<p style=":center"><a href="http://www.seeedstudio.com/Grove-Switch(P)-p-1252.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/get_one_now_small.png" width="200" height="38"  border=0 /></a></p>

## Verze

| Verze produktu       | Změny        | Datum vydání |
| -------------------- | ------------ | ------------ |
| Grove-Switch(P) V1.0 | První vydání | Jul 2012     |

## Vlastnosti

- Kompatibilní s rozhraním Grove
- Snadno použitelný
- Základní element Grove

!!!Tip
Více detailů o modulech Grove zjistíte v [popisu systému Grove](http://wiki.seeedstudio.com/Grove_System/)

## Specifikace

| Parametr         | Hodnota / Rozsah |
| ---------------- | ---------------- |
| Pracovní napětí  | 3.3/5V           |
| Životnost        | 10,000 cycles    |
| Síla k přepnutí  | 200 ± 50gf       |
| Pracovní teplota | -20℃ to +80℃     |
| Velikost         | 20mmX20mm        |

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

**Hardware**

- **Krok 1.** Připravte si tyto součástky:

| Seeeduino V4.2                                                                                                           | Base Shield                                                                                                           | Grove-Switch(P)                                                                                               | Grove - Purple LED (3mm)                                                            |
| ------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Switch-P/raw/master/img/SwitchP_s.jpg) | ![](https://github.com/SeeedDocument/Grove-Switch-P/raw/master/img/grove_led_s.jpg) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                          | [Koupit](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                      | [Koupit](<http://www.seeedstudio.com/Grove-Switch(P)-p-1252.html>)                                            | [Koupit](https://www.seeedstudio.com/Grove-Purple-LED-%283mm%29-p-1143.html)        |

- **Krok 2.** Připojte Grove-Switch(P) k portu **D2** port na Grove-Base Shieldu.
- **Krok 3.** Připojte Grove-LED k portu **D6** port na Grove-Base Shieldu.
- **Krok 4.** Připojte Base Shield k Seeeduinu.
- **Krok 5.** Připojte Seeduino k PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-Switch-P/raw/master/img/seeeduino_switch_led.jpg)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit Grove-Switch(P) and Grove - Purple LED (3mm) k Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino   | Grove-Switch(P) | Seeeduino   | Grove - Purple LED (3mm) |
| ----------- | --------------- | ----------- | ------------------------ |
| 5V          | Červený         | 5V          | Červený                  |
| GND         | Černý           | GND         | Černý                    |
| Nepřipojeno | Bílý            | Nepřipojeno | Bílý                     |
| D2          | Žlutý           | D6          | Žlutý                    |

**Software**

- **Krok 1.** Zkopírujte kód do Arduino IDE, přeložte a nahrajte do Arduina. Pokud si nejste jisti, jak nahrát kód, podívejte se na stránku [Jak nahrát kód](http://wiki.seeedstudio.com/Upload_Code/).

```
const int switchPin = 2;     // the number of the pushbutton pin
const int ledPin =  6;      // the number of the LED pin

int switchState = 0;         // variable for reading the pushbutton status

void setup() {
    // initialize the LED pin as an output:
    pinMode(ledPin, OUTPUT);
    // initialize the switch pin as an input:
    pinMode(switchPin, INPUT);
    Serial.begin(9600);
}

void loop(){
    // read the state of the switch value:
    switchState = digitalRead(switchPin);

    if (switchState == HIGH) {
        //turn LED on:
        digitalWrite(ledPin, HIGH);
        Serial.println("switch high!");
    }
    else {
        //turn LED off:
        digitalWrite(ledPin, LOW);
        Serial.println("switch low");
    }
}

```

- **Krok 2.** Přepínejte přepínač a sledujte, jak se chová LED a co se vypisuje na sériový monitor.

```
switch high!
switch low
switch high!
```

### Pokusy s Raspberry Pi (s Grove Base Hat)

#### Hardware

- **Krok 1**. Součástky, použité v tomto projektu:

| Raspberry pi                                                                                                   | Grove Base Hat for RasPi                                                                                                       | Grove - Switch P                                                                                              |
| -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Switch-P/raw/master/img/SwitchP_s.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)                                              | [Koupit](<http://www.seeedstudio.com/Grove-Switch(P)-p-1252.html>)                                            |

- **Krok 2**. Připojte Grove Base Hat k Raspberry Pi.
- **Krok 3**. Připojte Switch k portu 12 na Base Hatu.
- **Krok 4**. Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-Switch-P/raw/master/img/Switch_Hat.jpg)

!!! Poznámka
V kroku 3 můžete připojit přepínač k **libovolnému GPIO portu**, ale ujistěte se, že jste změnili i číslo portu v kódu ukázky.

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
python grove_switch.py 12

```

Toto je kód v souboru grove_switch.py.

```python


import time
from grove.gpio import GPIO


class GroveTiltSwitch(GPIO):
    def __init__(self, pin):
        super(GroveTiltSwitch, self).__init__(pin, GPIO.IN)

    @property
    def state(self):
        return super(GroveTiltSwitch, self).read()


Grove = GroveTiltSwitch


def main():
    import sys

    if len(sys.argv) < 2:
        print('Usage: {} pin'.format(sys.argv[0]))
        sys.exit(1)

    swicth = GroveTiltSwitch(int(sys.argv[1]))


    while True:
        if swicth.state is 1:
            print("on")
        else:
            print("off")
        time.sleep(1)


if __name__ == '__main__':
    main()


```

!!!Povedlo se
Pokud vše šlo tak, jak má, uvidíte výsledek podobný tomuto

```python

pi@raspberrypi:~/grove.py/grove $ python grove_switch.py 12
off
off
on
off
on
on
off
^CTraceback (most recent call last):
  File "grove_switch.py", line 70, in <module>
    main()
  File "grove_switch.py", line 66, in main
    time.sleep(1)
KeyboardInterrupt


```

Program ukončíte stiskem ++ctrl+c++.

### Pokusy s Raspberry Pi (s modulem GrovePi_Plus)

**Hardware**

- **Krok 1.** Připravte si tyto součástky:

| Raspberry pi                                                                                                   | GrovePi_Plus                                                                                                         | Grove-Switch(P)                                                                                               |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Switch-P/raw/master/img/SwitchP_s.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)                                                         | [Koupit](<http://www.seeedstudio.com/Grove-Switch(P)-p-1252.html>)                                            |

- **Krok 2.** Připojte GrovePi_Plus k Raspberry Pi.
- **Krok 3.** Připojte Grove-Switch(P) k portu **D3** na GrovePi_Plus.
- **Krok 4.** Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-Switch-P/raw/master/img/rpi_switch.jpg)

**Software**

- **Krok 1.** Nastavte si vývojové prostředí pomocí průvodce [nastavení software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/).
- **Krok 2.** Stáhněte si zdrojový kód tím, že naklonujete knihovnu GrovePi.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

- **Krok 3.** Spusťte následující příkazy.

```python
cd ~/GrovePi/Software/Python
python grove_switch.py
```

Toto je kód v souboru grove_switch.py.

```python
import time
import grovepi

# Připojte Grove Switch to digital port D3
# SIG,NC,VCC,GND
switch = 3

grovepi.pinMode(switch,"INPUT")

while True:
    try:
        print(grovepi.digitalRead(switch))
        time.sleep(.5)

    except IOError:
        print ("Error")
```

- **Krok 4.** We will see the switch status as below.

```python
pi@raspberrypi:~/GrovePi/Software/Python $ python grove_switch.py
1
1
0
0
0
```

## Zdroje

- **[Eagle&PDF]** [Grove-Switch(P) Schematic](https://github.com/SeeedDocument/Grove-Switch-P/raw/master/res/Grove-Switch-P-Eagle_File_v1.0.zip)

## Projekty

**Použití přepínače k ovládání relé**: Zjistíte, jak získat hodnotu přepínače. Navíc se dozvíte, jak použít relé ve funkci ovladače.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/sodaqmoja/using-a-switch-to-open-and-close-a-relay-3329ec/embed' width='350'></iframe>

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
