---
name: Grove - Red LED
category: Display
bzurl: https://www.seeedstudio.com/Grove-Red-LED-p-1142.html
oldwikiname: Grove - Red LED
prodimagename: Grove-LED_Photo.jpg
surveyurl: https://www.research.net/r/Grove_Red_LedLED
sku: 104030005
---

![](https://github.com/SeeedDocument/Raspi_wiki/raw/master/img/red_led.jpg)

Modul s červenou LED (Grove - Red LED) je podobný ostatním modulům Grove - LED module, které obsahují svítivou diodu jako zdroj světla. Tento modul obsahuje navíc i potenciometr, kterým lze nastavit intenzitu svitu a spotřebu. Modul má i montážní otvory, takže je možné jej připevnit na základní desku vašeho prototypu. Tento modul můžete použít třeba k indikaci toho, že je zařízení zapnuté.

<p style=":center"><a href="https://www.seeedstudio.com/Grove-Red-LED-p-1142.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/300px-Get_One_Now_Banner-ragular.png" /></a></p>

## Verze

| Verze produktu | Změny        | Datum vydání |
| -------------- | ------------ | ------------ |
| Grove-LED_v1.3 | První vydání | Mar 15 2016  |

## Vlastnosti

- Poskytuje zdroj světla pro vaši konstrukci
- LED je umístěna v patici, takže ji můžete snadno vyměnit a použít jinou barvu světla
- Díky integrovanému potenciometru můžete ovládat jas světla a používat tento modul v širokém rozsahu napájecího napětí

## Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                               | BeagleBone                                                                                        | Wio                                                                                               | LinkIt ONE                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Začínáme

### Pokusy s Arduinem

#### Hardware

- Krok 1: Připravte si tyto součástky:

| Seeeduino V4.2                                                                                                           | Base Shield                                                                                                           | Grove - Red LED                                                                                                |
| ------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Red_LED/raw/master/img/Red%20LED_s.jpg) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                          | [Koupit](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                      | [Koupit](https://www.seeedstudio.com/s/Grove-Red-LED-p-1142.html)                                              |

- Krok 2: Připojte Grove-Red LED k portu D2 na Grove-Base Shieldu.
- Krok 3: Připojte Base Shield k Seeeduinu.
- Krok 4: Připojte Seeduino k PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-Red_LED/raw/master/img/seeedstudio_red_led.jpg)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit Grove-Red_Led k Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino   | Grove-Red Led |
| ----------- | ------------- |
| 5V          | Červený       |
| GND         | Černý         |
| Nepřipojeno | Bílý          |
| D2          | Žlutý         |

#### Software

- **Krok 1**. Zkopírujte kód do Arduino IDE, přeložte a nahrajte do Arduina.

```
void setup() {
  // initialize digital pin2  as an output.
  pinMode(2, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(2, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);                       // wait for a second
  digitalWrite(2, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);                       // wait for a second
}
```

- **Krok 2**. LED se bude rozsvěcet a zhasínat

### Pokusy s Codecraftem

#### Hardware

**Krok 1.** Připojte Grove - Red LED k portu D2 na Grove-Base Shieldu

**Krok 2.** Připojte Base Shield k Seeeduinu / Arduinu.

**Krok 3.** Propojte Seeeduino/Arduino s PC pomocí kabelu USB.

#### Software

**Krok 1.** Spusťte [Codecraft](https://ide.chmakered.com/), přepněte se na prostředí pro Arduino a přidejte na plochu hlavní proceduru (Start).

!!!Poznámka
Pokud používáte Codecraft poprvé, podívejte se na [Průvodce světem Codecraftu a Arduina](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Krok 2.** Přetáhněte bloky tak, jak ukazuje následující obrázek, nebo otevřte cdc soubor, který si můžete stáhnout na konci této stránky.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove-Red_LED/master/img/cc_LED.png)

Nahrajte hotový program do svého Arduina/Seeeduina.

!!!Povedlo se
Jakmile je nahrávání hotové, začne LED blikat.

### Pokusy s Raspberry Pi (s Grove Base Hat)

#### Hardware

- **Krok 1**. Součástky, použité v tomto projektu:

| Raspberry pi                                                                                                   | Grove Base Hat for RasPi                                                                                                       | Grove - Red LED                                                                                                |
| -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Red_LED/raw/master/img/Red%20LED_s.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)                                              | [Koupit](https://www.seeedstudio.com/s/Grove-Red-LED-p-1142.html)                                              |

- **Krok 2**. Připojte Grove Base Hat k Raspberry Pi.
- **Krok 3**. Připojte Red LED k portu 12 na Base Hatu.
- **Krok 4**. Propojte Raspberry Pi s PC pomocí kabelu USB.
  ![](https://github.com/SeeedDocument/Grove-Red_LED/raw/master/img/BaseHat_LED.jpg)
  !!!Poznámka
  V kroku 3 můžete připojit the Red LED k **libovolnému GPIO portu**, ale ujistěte se, že jste změnili i číslo portu v kódu ukázky.

#### Software

- **Krok 1**. Nastavte si vývojové prostředí pomocí průvodce [nastavení software](http://wiki.seeedstudio.com/Grove_Base_Hat_for_Raspberry_Pi/#installation).
- **Krok 2**. Stáhněte si zdrojový kód tím, že naklonujete knihovnu grove.py.

```
cd ~
git clone https://github.com/Seeed-Studio/grove.py

```

- **Krok 3**. Spusťte program pomocí následujících příkazů.

```
cd yourpath/grove.py/grove
python grove_led.py 12
```

Pokud jste modul připojili k jinému portu Base Hatu, spusťte program se správným číslem portu.

```
python grove_led.py číslo_portu
```

Toto je kód v souboru grove_led.py.

```python

from grove.gpio import GPIO


class GroveLed(GPIO):
    def __init__(self, pin):
        super(GroveLed, self).__init__(pin, GPIO.OUT)

    def on(self):
        self.write(1)

    def off(self):
        self.write(0)


Grove = GroveLed


def main():
    import sys
    import time

    if len(sys.argv) < 2:
        print('Usage: {} pin'.format(sys.argv[0]))
        sys.exit(1)

    led = GroveLed(int(sys.argv[1]))

    while True:
        led.on()
        time.sleep(1)
        led.off()
        time.sleep(1)


if __name__ == '__main__':
    main()


```

!!!Povedlo se
Pokud vše šlo tak, jak má, you will be able to see the led on and off.

!!!Pozor
V některých případech je potřeba zadat číslo portu jako parametr při spuštění programu. Tady to je kupříkladu `python grove_led.py 12`, **12** je číslo portu, k němuž jste LED připojili.

### Pokusy s Raspberry Pi (s modulem GrovePi_Plus)

#### Hardware

- Krok 1: Připravte si tyto součástky:

| Raspberry pi                                                                                                   | GrovePi_Plus                                                                                                         | Grove - Red Led                                                                                                |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Red_LED/raw/master/img/Red%20LED_s.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)                                                         | [Koupit](https://www.seeedstudio.com/s/Grove-Red-LED-p-1142.html)                                              |

- Krok 2: Připojte GrovePi_Plus k Raspberry Pi.
- Krok 3: Připojte Grove-Red Led to D4 na GrovePi_Plus.
- Krok 4: Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-Red_LED/raw/master/img/rasp_red_led.jpg)

#### Software

- **Krok 1**. Nastavte si vývojové prostředí pomocí průvodce [nastavení software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/).
- **Krok 2**. Stáhněte si zdrojový kód tím, že naklonujete knihovnu GrovePi.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

- **Krok 3**. Spusťte následující příkazy.

```
cd ~/GrovePi/Software/Python
python grove_led_blink.py
```

Toto je kód v souboru grove_led_blink.py.

```python

import time
from grovepi import *

# Připojte Grove LED to digital port D4
led = 4

pinMode(led,"OUTPUT")
time.sleep(1)

print ("This example will blink a Grove LED connected to the GrovePi+ on the port labeled D4. If you're having trouble seeing the LED blink, be sure to check the LED connection and the port number. You may also try reversing the direction of the LED on the sensor.")
print (" ")
print ("Připojte LED to the port labele D4!" )

while True:
    try:
        #Blink the LED
        digitalWrite(led,1)		# Send HIGH to switch on LED
        print ("LED ON!")
        time.sleep(1)

        digitalWrite(led,0)		# Send LOW to switch off LED
        print ("LED OFF!")
        time.sleep(1)

    except KeyboardInterrupt:	# Turn LED off before stopping
        digitalWrite(led,0)
        break
    except IOError:				# Print "Error" if communication error encountered
        print ("Error")

```

- **Krok 4**. Připojená LED začne blikat.

```
pi@raspberrypi:~/GrovePi/Software/Python $ python grove_led_blink.py
This example will blink a Grove LED connected to the GrovePi+ on the port labeled D4.
If you're having trouble seeing the LED blink, be sure to check the LED connection and the port number.
You may also try reversing the direction of the LED on the sensor.

Připojte LED to the port labele D4!
LED ON!
LED OFF!
LED ON!
LED OFF!
```

## Zdroje

- **[PDF]** [Grove-Red LED Schematic](https://github.com/SeeedDocument/Grove-Red_LED/raw/master/res/Grove-LED_v1.3.pdf)
- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove-Red_LED/master/res/Grove_Red_LED_CDC_File.zip)

## Projekty

**Jak pomocí Grove Buttonu ovládat Grove LED**: Ukázka propojení modulů Grove Button a Grove LED.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/user50338573/using-grove-button-to-control-grove-led-96d00b/embed' width='350'></iframe>

**Moduly Grove Button a LED**:

<iframe width="560" height="315" src="https://www.youtube.com/embed/RCtsxwx4OaA" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/78lVn_-oYaY" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/).

<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
