---
name: Grove - Button
category: Sensor
bzurl: https://www.seeedstudio.com/Grove-Button-p-766.html
oldwikiname: Grove - Button
prodimagename: Button.jpg
surveyurl: https://www.surveymonkey.com/r/grove-button
sku: 101020003
---

![](https://github.com/SeeedDocument/Grove_Button/raw/master/img/Button.jpg)

Grove - Button je jednopolohové tlačítko. “Jednopolohové” znamená, že po uvolnění stisku se tlačítko vrátí do výchozí polohy. Tlačítko vrací signál HIGH, když je stisknuté, a signál LOW, když je uvolněné. Nápis Sig na plošném spoji označuje signál, nápis NC znamená nepoužitý vývod. Existují dvě verze tohoto modulu, jak je vidět na fotografiích. Jediný rozdíl mezi nimi je v orientaci konektoru.

[![](https://github.com/SeeedDocument/Grove_Button/raw/master/image/300px-Get_One_Now_Banner.png)](https://www.seeedstudio.com/Grove-Button-p-766.html)

## Verze

| Verze produktu | Změny        | Vydáno dne         |
| -------------- | ------------ | ------------------ |
| Grove-Button   | První vydání | 25. listopadu 2010 |

## Vlastnosti

- Snadno použitelé tlačítko
- Využívá standardní 4pinové kabely Grove

!!!Tip
Více detailů o modulech Grove zjistíte v [popisu systému Grove](http://wiki.seeedstudio.com/Grove_System/)

## Specifikace

| Parametr         | Hodnota/Rozsah |
| ---------------- | -------------- |
| Napájecí napětí  | 3.3/5V         |
| Životnost        | 200,000 cycles |
| Pracovní síla    | 100 ± 50gf     |
| Provozní teplota | -25℃ to +70℃   |
| Rozměry          | 20mm x 20mm    |

## Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                               | BeagleBone                                                                                        | Wio                                                                                               | LinkIt ONE                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Začínáme

### Pokusy s Arduinem

#### Hardware

- Krok 1. Připravte si tyto součástky:

| Seeeduino V4.2                                                                                                           | Base Shield                                                                                                           | Grove - Button                                                                                             |
| ------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Button/raw/master/img/button_s.jpg) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                          | [Koupit](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                      | [Koupit](https://www.seeedstudio.com/Grove-Button-p-766.html)                                              |

- Krok 2. Připojte Grove-Button k portu D2 na Base Shieldu.
- Krok 3. Připojte Base Shield k Seeeduinu.
- Krok 4. Připojte Seeduino k PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove_Button/raw/master/img/seeeduino_button.jpg)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit Grove Button k
Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino   | Grove-Button |
| ----------- | ------------ |
| 5V          | Červený      |
| GND         | Černý        |
| Nepřipojeno | Bílý         |
| D2          | Žlutý        |

#### Software

- Krok 1. Zkopírujte následující kód do Arduino IDE, přeložte jej a nahrajte

```c
const int buttonPin = 2;     // číslo pinu, kde je připojené tlačítko
const int ledPin =  13;      // číslo pinu, kde je připojená LED

// variables will change:
int buttonState = 0;         // proměnná, do níž se čte stav tlačítka

void setup() {
    // inicializujeme pin s LED jako výstupní:
    pinMode(ledPin, OUTPUT);
    // inicializujeme pin s tlačítkem jako vstupní:
    pinMode(buttonPin, INPUT);
}

void loop(){
    // čteme stav tlačítka:
    buttonState = digitalRead(buttonPin);

    // Zkontrolujeme, jestli je tlačítko stisknuté
    // pokud je, bude buttonState mít hodnotu HIGH:
    if (buttonState == HIGH) {
        // zapneme LED:
        digitalWrite(ledPin, HIGH);
    }
    else {
        // vypneme LED:
        digitalWrite(ledPin, LOW);
    }
}
```

- Krok 2. Zkuste mačkat tlačítko a sledujte LED na vývojovém kitu.

### Pokusy s Codecraftem

#### Hardware

**Krok 1.** Připojte Grove - Button k portu D2 na Base Shieldu.

**Krok 2.** Připojte Base Shield k Seeeduinu / Arduinu.

**Krok 3.** Propojte Seeeduino/Arduino s PC pomocí kabelu USB.

#### Software

**Krok 1.** Spusťte [Codecraft](https://ide.chmakered.com/), přepněte se na prostředí pro Arduino a přidejte na plochu hlavní proceduru (Start).

!!!Poznámka
Pokud používáte Codecraft poprvé, podívejte se na [Průvodce světem Codecraftu a Arduina](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Krok 2.** Přetáhněte bloky tak, jak ukazuje následující obrázek, nebo otevřte cdc soubor, který si můžete stáhnout na konci této stránky.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove_Button/master/img/cc_Button.png)

Nahrajte hotový program do svého Arduina/Seeeduina.

!!!Povedlo se
Jakmile je nahrávání hotové, začne blikat LED na Arduinu/Seeeduinu podle toho, jak budete mačkat tlačítko.

### Pokusy s Raspberry Pi (s Grove Base Hat)

#### Hardware

- **Krok 1**. Připravte si tyto součástky:

| Raspberry Pi                                                                                                   | Grove Base Hat for RasPi                                                                                                       | Grove - Button                                                                                             |
| -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Button/raw/master/img/button_s.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)                                              | [Koupit](https://www.seeedstudio.com/Grove-Button-p-766.html)                                              |

- **Krok 2**. Připojte Grove Base Hat k Raspberry Pi.
- **Krok 3**. Připojte Grove - Button k PWM portu (port 12) na Base Hatu.
- **Krok 4**. Propojte Raspberry Pi s PC pomocí kabelu USB.
  ![](https://github.com/SeeedDocument/Grove_Button/raw/master/img/with_hat.jpg)

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
python grove_button.py 12
```

Pokud připojíte červenou LED k jinému portu na Base Hatu, musíte použít místo **python grove_led.py 12** následující příkaz:

```
python grove_button.py portnumber
```

Toto je kód v souboru grove_button.py:

```python

import time
from grove.button import Button
from grove.factory import Factory


class GroveButton(object):
    def __init__(self, pin):
        # High = pressed
        self.__btn = Factory.getButton("GPIO-HIGH", pin)
        self.__last_time = time.time()
        self.__on_press = None
        self.__on_release = None
        self.__btn.on_event(self, GroveButton.__handle_event)

    @property
    def on_press(self):
        return self.__on_press

    @on_press.setter
    def on_press(self, callback):
        if not callable(callback):
            return
        self.__on_press = callback

    @property
    def on_release(self):
        return self.__on_release

    @on_release.setter
    def on_release(self, callback):
        if not callable(callback):
            return
        self.__on_release = callback

    def __handle_event(self, evt):
        dt, self.__last_time = evt["time"] - self.__last_time, evt["time"]
        # print("event index:{} event:{} pressed:{}".format(evt["index"], evt["code"], evt["pressed"]))
        if evt["code"] == Button.EV_LEVEL_CHANGED:
            if evt["pressed"]:
                if callable(self.__on_press):
                    self.__on_press(dt)
            else:
                if callable(self.__on_release):
                    self.__on_release(dt)


Grove = GroveButton

def main():
    from grove.helper import SlotHelper
    sh = SlotHelper(SlotHelper.GPIO)
    pin = sh.argv2pin()

    button = GroveButton(pin)

    def on_press(t):
        print('Button is pressed')
    def on_release(t):
        print("Button is released, pressed for {0} seconds".format(round(t,6)))

    button.on_press = on_press
    button.on_release = on_release

    while True:
        time.sleep(1)


if __name__ == '__main__':
    main()


```

!!!Povedlo se
Pokud vše šlo tak, jak má, uvidíte zhruba něco takového:

```python

pi@raspberrypi:~/grove.py/grove $ python grove_button.py 12
Hat Name = 'Grove Base Hat RPi'
Button is pressed
Button is pressed
Button is pressed
Button is pressed
Button is pressed
Button is pressed
Button is released, pressed for 0.002685 seconds
Button is pressed
Button is released, pressed for 0.219019 seconds
Button is pressed
Button is released, pressed for 0.001372 seconds
Button is pressed
Button is pressed
Button is released, pressed for 0.043143 seconds
Button is pressed
Button is released, pressed for 1.083292 seconds
^CTraceback (most recent call last):
  File "grove_button.py", line 103, in <module>
    main()
  File "grove_button.py", line 99, in main
    time.sleep(1)
KeyboardInterrupt


```

Pomocí **ctrl+c** ukončíte běh programu.

### Pokusy s Raspberry Pi (s modulem GrovePi_Plus)

#### Hardware

- Krok 1. Připravte si tyto součástky:

| Raspberry Pi                                                                                                   | GrovePi_Plus                                                                                                         | Grove - Button                                                                                             |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Button/raw/master/img/button_s.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)                                                         | [Koupit](https://www.seeedstudio.com/Grove-Button-p-766.html)                                              |

- Krok 2. Připojte GrovePi_Plus k Raspberry Pi.
- Krok 3. Připojte Grove-Button k portu D3 na GrovePi_Plus.
- Krok 4. Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove_Button/raw/master/img/rasp_button.jpg)

#### Software

- Krok 1. Nastavte si vývojové prostředí pomocí průvodce [nastavení software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/).
- Krok 2. Stáhněte si zdrojový kód tím, že naklonujete knihovnu GrovePi.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

- Krok 3. Proveďte tyto příkazy:

```
cd ~/GrovePi/Software/Python
python grove_button.py
```

Toto obsahuje soubor grove_button.py:

```python
import time
import grovepi

# Připojte Grove Button to digital port D3
# SIG,NC,VCC,GND
button = 3

grovepi.pinMode(button,"INPUT")

while True:
    try:
        print(grovepi.digitalRead(button))
        time.sleep(.5)

    except IOError:
        print ("Error")
```

- Krok 4. Zkuste mačkat tlačítko Grove Button.

```
pi@raspberrypi:~/GrovePi/Software/Python $ python grove_button.py
0
1
1
1
1
0
0
```

## Zdroje

- **[Eagle&PDF]** [Grove-Button Eagle Files](https://github.com/SeeedDocument/Grove_Button/raw/master/resources/Grove_-_Button_v1.0_Source_File.zip)

- **[Další čtení]** [Laserová pistole ze dřeva](http://www.instructables.com/id/DIY-a-Wooden-Laser-Gun-As-a-Xmas-Present-for-Your-/)

- **[Codecraft]** [Uvedený příklad ve formátu CDC](https://raw.githubusercontent.com/SeeedDocument/Grove_Button/master/res/Grove_Button_CDC_File.zip)

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Button/master/img/gun.jpg)

Inspirovali jsme se hrou OVERWATCH a pro pobavení jsme si udělali dřevěný model laserové pistole!

Laserová pistole a Terč pro pistoli jsou založené na Arduinu s názvem Seeeduino Lotus. Laserový zdroj v laserové pistoli posílá pulsy na terč. Terč obsahuje tři světelné senzory, které hlídají, zda paprsek zasáhl cíl. Vypadá to velmi jednoduše, že? Pokud vás tento projekt zaujal, udělejte si jej také. Stojí za to strávit jeden den stavbou takové hračky pro sebe nebo pro vaše děti.

## Projekty

**Grove - Úvod do tlačítek a světelných pásků**: Příklad pro začátečníky - vsadím se, že se budete usmívat, až si tento projekt postavíte. Pošlete nám selfie!

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/ingo-lohs/grove-introduction-in-a-button-led-string-light-f7e4d6/embed' width='350'></iframe>

**Jak pomocí Grove Buttonu ovládat Grove LED**: Ukázka propojení modulů Grove Button a Grove LED.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/user50338573/using-grove-button-to-control-grove-led-96d00b/embed' width='350'></iframe>

**Moduly Grove Button a LED**:

<iframe width="560" height="315" src="https://www.youtube.com/embed/RCtsxwx4OaA" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/78lVn_-oYaY" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
