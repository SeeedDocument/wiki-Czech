---
name: Grove-LED Button
category: Acator
bzurl:
oldwikiname:
prodimagename:
surveyurl:
sku: 111020044,111020045,111020046
tags: 2-链接
---

![](https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/main.jpg)

Svítivá tlačítka (The Grove - LED Button) jsou připravená ve třech verzích: Grove - Yellow LED Button, Grove - Blue LED Button a Grove - Red LED Button. Tlačítko vydrží alespoň 100.000 sepnutí. Díky zabudované LED jsou tato tlačítka ideální všude tam, kde je dobré u tlačítka zároveň ukázat jeho aktuální stav. Modul používá vysoce kvalitní tranzistory MOSFET(N) pro ovládání LED, aby byla zajištěna rychlá odezva a nízká spotřeba. Potřebujete nějaké opravdu cool tlačítka? Tady je máte!

<p style=":center"><a href="https://www.seeedstudio.com/Grove-Yellow-LED-Button-p-3101.html" target="_blank"><img src="https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/Y.png" height="48" width="300" /></a></p>
<p style=":center"><a href="https://www.seeedstudio.com/Grove-Blue-LED-Button-p-3104.html" target="_blank"><img src="https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/B.png" height="48" width="300" /></a></p>
<p style=":center"><a href="https://www.seeedstudio.com/Grove-Red-LED-Button-p-3096.html" target="_blank"><img src="https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/R.png"  height="48" width="300" /></a></p>

## Verze

| Verze produktu   | Změny        | Datum vydání |
| ---------------- | ------------ | ------------ |
| Grove-LED Button | První vydání | Jun 2018     |

## Verze

| Verze produktu   | Změny        | Datum vydání |
| ---------------- | ------------ | ------------ |
| Grove-LED Button | První vydání | Jun 2018     |

## Verze

| Verze produktu   | Změny        | Datum vydání |
| ---------------- | ------------ | ------------ |
| Grove-LED Button | První vydání | Jun 2018     |

## Vlastnosti

- Dlouhá životnost
- Snadno použitelný
- Grove Digital interface

## Specifikace

| Parametr              | Hodnota                  |
| --------------------- | ------------------------ |
| Pracovní napětí       | 3.3V/5V                  |
| Životnost bez zátěže  | 100 000 times            |
| Proud diodou LED      | 50mA                     |
| Odpor po stisknutí^1^ | <100mΩ                   |
| Odpor po uolnění^2^   | >100MΩ                   |
| Velikost              | D: 40mm Š: 20mm V: 13mm  |
| Hmotnost              | 4.3g                     |
| Rozměry balení        | D: 140mm Š: 90mm V: 10mm |
| Celková hmotnost      | 11g                      |

!!!Tipy
1,2- Pokud chcete měřit odpor, odpojte tlačítko od desky. Jinak odpor samotného modulu zkreslí výsledky měření.

## Hardwarové parametry

### Popis vývodů

![](https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/pin_map.jpg)

### Schéma

![](https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/schematic.jpg)

**SIG1** řídí LED. Normální hodnota je LOW, proto je MOSFET zavřený a LED nesvítí. Když přivedete na SIG1 hodnotu HIGHm MOSFET se otevře a LED rozsvítí.

**SIG2** je připojený na samotný spínač. Díky pull-up rezistoru je v klidu na SIG2 úroveň HIGH. Při stisku tlačítka se výstup **SIG2** přepne do LOW.

## Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                               | BeagleBone                                                                                        | Wio                                                                                               | LinkIt ONE                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

## Začínáme

!!!Tipy
V příkaldech používáme červenou variantu, ale ostatní fungujou stejně.

### Pokusy s Arduinem

#### Hardware

**Potřebné součástky**

| Seeeduino V4.2                                                                                                             | Base Shield                                                                                                                | Grove- Red LED Button                                                                                               |
| -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/IMG_0068a.jpg) |
| <a href="http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html" target="_blank">Koupit</a>                                 | <a href="https://www.seeedstudio.com/Base-Shield-V2-p-1378.html" target="_blank">Koupit</a>                                | <a href="https://www.seeedstudio.com/Grove-Red-LED-Button-p-3096.html" target="_blank">Koupit</a>                   |

- **Krok 1.** Grove- Red LED Button k portu **D3** na Grove-Base Shieldu.

- **Krok 2.** Připojte Base Shield k Seeeduinu.

- **Krok 3.** Připojte Seeduino k PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/red%20LED.jpg)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit Grove Button k
Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino | Grove- Red LED Button |
| --------- | --------------------- |
| 5V        | Červený               |
| GND       | Černý                 |
| SIG2      | Bílý                  |
| SIG1      | Žlutý                 |

#### Software

!!!Poznámka
Pokud se s Arduinem setkáváte poprvé, doporučujeme vám pročíst návod [Začínáme s Arduinem](http://wiki.seeedstudio.com/_with_Arduino/) dřív, než začnete.

- **Krok 1.** Zkopírujte následující kód do Arduino IDE, přeložte jej a nahrajte

```C++
#include "Arduino.h"

//1: toggle mode, 2: follow mode
#define LED_MODE   1

const int ledPin = 3;      // the number of the LED pin, D3
const int buttonPin = 4;    // the number of the pushbutton pin, D4
const boolean breathMode = true;  // if or not the led lights as breath mode when it's on

// Variables will change:
int ledState = LOW;         // the current state of the output pin
int ledFadeValue = 0;
int ledFadeStep = 5;
int ledFadeInterval = 20;   //milliseconds
int buttonState;             // the current reading from the input pin
int lastButtonState = HIGH;   // the previous reading from the input pin

unsigned long lastDebounceTime = 0;  // the last time the output pin was toggled
unsigned long debounceDelay = 50;    // the debounce time; increase if the output flickers
unsigned long lastLedFadeTime = 0;

void setup() {
  pinMode(buttonPin, INPUT);
  pinMode(ledPin, OUTPUT);
  digitalWrite(ledPin, ledState);
}

void loop() {
  int reading = digitalRead(buttonPin);

  // If the switch changed, due to noise or pressing:
  if (reading != lastButtonState) {
    // reset the debouncing timer
    lastDebounceTime = millis();
  }

  if ((millis() - lastDebounceTime) > debounceDelay) {
    // whatever the reading is at, it's been there for longer
    // than the debounce delay, so take it as the actual current state:

    // if the button state has changed:
    if (reading != buttonState) {
      buttonState = reading;

#if LED_MODE == 1
      if (buttonState == LOW) {  //button is pressed
          ledState = !ledState;
          ledFadeValue = 0;
          lastLedFadeTime = millis();
      }
#else
      if (buttonState == LOW) {  //button is pressed
        ledState = HIGH;
        ledFadeValue = 0;
        lastLedFadeTime = millis();
      } else {                   //button is released
        ledState = LOW;
      }
#endif
    }
  }

  // set the LED:
  if (breathMode && ledState != LOW) {
    if (millis() - lastLedFadeTime > ledFadeInterval) {
      lastLedFadeTime = millis();
      analogWrite(ledPin, ledFadeValue);
      ledFadeValue += ledFadeStep;
      if (ledFadeValue > 255){
        ledFadeValue = 255 - ledFadeStep;
        ledFadeStep = -ledFadeStep;
      } else if (ledFadeValue < 0) {
        ledFadeValue = 0;
        ledFadeStep = -ledFadeStep;
      }
    }
  } else {
    digitalWrite(ledPin, ledState);
  }

  lastButtonState = reading;
}

```

!!!Tip
V této ukázce jsme použili mód 1, kdy tlačítko pracuje jako přepínač. Můžete změnit na řádku 4 kód <mark>#define LED_MODE 1</mark> na <mark>#define LED_MODE 2</mark> a použít tlačítko jako opravdové tlačítko

- **Krok 2.** Nahrajte přeložený kód do Arduina. Pokud si nejste jisti, jak nahrát kód, podívejte se na stránku [Jak nahrát kód](http://wiki.seeedstudio.com/Upload_Code/).

- **Krok 3.** Now, try to press you button, you will see the LED light on with a fade on/fade off effect.

Výsledek by měl vypada takto:

<p style=":center"><img src="https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/result.gif"  /></p>

### Pokusy s Raspberry Pi

#### Hardware

- **Krok 1**. Součástky, použité v tomto projektu:

| Raspberry pi                                                                                                   | Grove Base Hat for RasPi                                                                                                       | Grove - Red LED Button                                                                                              |
| -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/IMG_0068a.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)                                              | [Koupit](https://www.seeedstudio.com/Grove-Red-LED-Button-p-3096.html)                                              |

- **Krok 2**. Připojte Grove Base Hat k Raspberry Pi.
- **Krok 3**. Připojte red LED button k portu D5 na Base Hatu.
- **Krok 4**. Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/LED_Hat.jpg)

!!! Poznámka
V kroku 3 můžete připojit the LED button k **libovolnému GPIO portu**, ale ujistěte se, že jste změnili i číslo portu v kódu ukázky.

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
python grove_ryb_led_button.py 5

```

Toto je kód v souboru grove_ryb_led_button.py.

```python

import time
from grove.button import Button
from grove.factory import Factory

class GroveLedButton(object):
    def __init__(self, pin):
        # High = light on
        self.__led = Factory.getOneLed("GPIO-HIGH", pin)
        # Low = pressed
        self.__btn = Factory.getButton("GPIO-LOW", pin + 1)
        self.__on_event = None
        self.__btn.on_event(self, GroveLedButton.__handle_event)

    @property
    def on_event(self):
        return self.__on_event

    @on_event.setter
    def on_event(self, callback):
        if not callable(callback):
            return
        self.__on_event = callback

    def __handle_event(self, evt):
        # print("event index:{} event:{} pressed:{}".format(evt['index'], evt['code'], evt['presesed']))
        if callable(self.__on_event):
            self.__on_event(evt['index'], evt['code'], evt['time'])
            return

        self.__led.brightness = self.__led.MAX_BRIGHT
        event = evt['code']
        if event & Button.EV_SINGLE_CLICK:
            self.__led.light(True)
            print("turn on  LED")
        elif event & Button.EV_DOUBLE_CLICK:
            self.__led.blink()
            print("blink    LED")
        elif event & Button.EV_LONG_PRESS:
            self.__led.light(False)
            print("turn off LED")


Grove = GroveLedButton

def main():
    from grove.helper import SlotHelper
    sh = SlotHelper(SlotHelper.GPIO)
    pin = sh.argv2pin()

    ledbtn = GroveLedButton(pin)

    # remove ''' pairs below to begin your experiment
    '''
    # define a customized event handle your self
    def cust_on_event(index, event, tm):
        print("event with code {}, time {}".format(event, tm))

    ledbtn.on_event = cust_on_event
    '''
    while True:
        time.sleep(1)


if __name__ == '__main__':
    main()


```

!!!Povedlo se
Pokud vše šlo tak, jak má, vaše LED se prvním stiskem rozsvítí, druhým zhasne. Pokud uděláte "dvojklik", LED zabliká.

```python

pi@raspberrypi:~/grove.py/grove $ python grove_ryb_led_button.py 5
Hat Name = 'Grove Base Hat RPi'
turn on  LED
turn on  LED
blink    LED
turn on  LED
turn off LED
^CTraceback (most recent call last):
  File "grove_ryb_led_button.py", line 101, in <module>
    main()
  File "grove_ryb_led_button.py", line 97, in main
    time.sleep(1)
KeyboardInterrupt

```

Program ukončíte stiskem ++ctrl+c++.

## Zdroje

- **[Zip]** [Grove-LED Button Eagle file](https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/res/Grove-Red_LED_Button.zip)

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/)..<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
