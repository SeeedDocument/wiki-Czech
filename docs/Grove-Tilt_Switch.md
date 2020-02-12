---
name: Grove - Tilt Switch
category: Sensor
bzurl: https://seeedstudio.com/Grove-Tilt-Switch-p-771.html
oldwikiname: Grove_-_Tilt_Switch
prodimagename: Tilt1.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/product/gbtlt.jpg
surveyurl: https://www.research.net/r/Grove-Tilt_Switch
sku: 101020025
tags: grove_digital, io_3v3, io_5v, plat_duino, plat_pi, plat_bbg
---

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Tilt_Switch/master/img/Tilt1.jpg)

Modul Grove-Tilt Switch funguje podobně jako tlačítko a používá se jako digitální vstup. Uvnitř čidla je dvojice kovových kuliček, které propojují kontakty, když čidlo stojí svisle. Jakmile snímač nakloníte, kuličky se přestanou dotýkat a kontakt se přeruší. Výstup je připojen k vývodu SIG, vývod NC není použitý.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](https://www.seeedstudio.com/Grove-Tilt-Switch-p-771.html)

## Vlastnosti

- Kompatibilní s rozhraním Grove
- Snadno použitelný
- Jednoduchý modul

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
3
</td>
<td>
5.0
</td>
<td>
5.25
</td>
<td>
V
</td>
</tr>
<tr align="center">
<th scope="row">
Úhel pro spojení
</th>
<td colspan="3">
10° ~170°
</td>
<td>
-
</td>
</tr>
<tr align="center">
<th scope="row">
Úhel pro rozpojení
</th>
<td colspan="3">
190° ~350°
</td>
<td>
-
</td>
</tr>
<tr align="center">
<th scope="row">
Životnost
</th>
<td colspan="3">
100,000
</td>
<td>
Cykly
</td>
</tr>
</table>

## Podporované platformy------------

| Arduino                                                                                               | Raspberry Pi                                                                                               | BeagleBone                                                                                        | Wio                                                                                                 | LinkIt ONE                                                                                             |
| ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Začínáme

### Pokusy s Arduinem

Pin SIG modulu Grove - Tilt Switch je normálně v úrovni LOW. Když je snímač svisle, propojí se kovové kuličky uvnitř snímače a výstup SIG se přepne do stavu HIGH.

V následujícím příkladu si ukážeme, jak snadno pomocí snímače náklonu ovládat LED.

- Následující obrázek ukazuje, že snímač náklonu je připojen k portu 5 na Grove - Base Shieldu a tlačítko Grove-Button k portu 7. LED je připojena k portu 1. Hardwarové zapojení vypadá takto:

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Tilt_Switch/master/img/Digitalv1.0b.jpg)

- Zkopírujte následující kód do nového projektu v Arduino IDE.

```
void setup()
{
    pinMode(1, OUTPUT);
    pinMode(5, INPUT);
    pinMode(7, INPUT);
}

void loop()
{

    if (digitalRead(5)==HIGH)
    {
        digitalWrite(1, HIGH);
        delay(100);
        digitalWrite(1, LOW);
    }

    if (digitalRead(7)==HIGH)
    {
        digitalWrite(1, HIGH);
        delay(200);
        digitalWrite(1, LOW);
    }

}
```

- Nahrajte kód do Arduina.
- LED se rozsvítí, když stisknete tlačítko nebo nakloníte snímač náklonu. Zkuste si to!

### Pokusy s Codecraftem

#### Hardware

**Krok 1.** Připojte Grove - Tilt Switch k portu D5, pak připojte Grove - Button a Grove - Red LED k portům D7 a D2 na Grove-Base Shieldu

**Krok 2.** Připojte Base Shield k Seeeduinu / Arduinu.

**Krok 3.** Propojte Seeeduino/Arduino s PC pomocí kabelu USB.

#### Software

**Krok 1.** Spusťte [Codecraft](https://ide.chmakered.com/), přepněte se na prostředí pro Arduino a přidejte na plochu hlavní proceduru (Start).

!!!Poznámka
Pokud používáte Codecraft poprvé, podívejte se na [Průvodce světem Codecraftu a Arduina](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Krok 2.** Přetáhněte bloky tak, jak ukazuje následující obrázek, nebo otevřte cdc soubor, který si můžete stáhnout na konci této stránky.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove-Tilt_Switch/master/img/cc_Tilt_Switch.png)

Nahrajte hotový program do svého Arduina/Seeeduina.

!!!Povedlo se
Jakmile je nahrávání hotové, LED se rozsvítí, když stisknete tlačítko nebo nakloníte snímač náklonu.

### Pokusy s Raspberry Pi (s Grove Base Hat)

#### Hardware

- **Krok 1**. Součástky, použité v tomto projektu:

| Raspberry pi                                                                                                   | Grove Base Hat for RasPi                                                                                                       | Grove - Tilt Switch                                                                                              |
| -------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Tilt_Switch/raw/master/img/thumbnail.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)                                              | [Koupit](https://www.seeedstudio.com/Grove-Tilt-Switch-p-771.html)                                               |

- **Krok 2**. Připojte Grove Base Hat k Raspberry Pi.
- **Krok 3**. Připojte tilt switch k portu 12 na Base Hatu.
- **Krok 4**. Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-Tilt_Switch/raw/master/img/Tilt_Hat.jpg)

!!! Poznámka
V kroku 3 můžete připojit snímač náklonu k **libovolnému GPIO portu**, ale ujistěte se, že jste změnili i číslo portu v kódu ukázky.

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
python grove_tilt_switch.py 12

```

Toto je kód v souboru grove_tilt_switch.py.

```python

import time
from grove.gpio import GPIO


class GroveTiltSwitch(GPIO):
    def __init__(self, pin):
        super(GroveTiltSwitch, self).__init__(pin, GPIO.IN)
        self._on_trigger = None
        self._on_release = None

    @property
    def on_trigger(self):
        return self._on_trigger

    @on_trigger.setter
    def on_trigger(self, callback):
        if not callable(callback):
            return

        if self.on_event is None:
            self.on_event = self._handle_event

        self._on_trigger = callback

    @property
    def on_release(self):
        return self._on_release

    @on_release.setter
    def on_release(self, callback):
        if not callable(callback):
            return

        if self.on_event is None:
            self.on_event = self._handle_event

        self._on_release = callback

    def _handle_event(self, pin, value):

        if value:
            if callable(self._on_trigger):
                self._on_trigger()
        else:
            if callable(self._on_release):
                self._on_release()

Grove = GroveTiltSwitch


def main():
    import sys

    if len(sys.argv) < 2:
        print('Usage: {} pin'.format(sys.argv[0]))
        sys.exit(1)

    swicth = GroveTiltSwitch(int(sys.argv[1]))

    def on_trigger():
        print('Triggered')
    def on_release():
        print("Released.")

    swicth.on_trigger = on_trigger
    swicth.on_release = on_release

    while True:
        time.sleep(1)


if __name__ == '__main__':
    main()


```

!!!Povedlo se
Pokud vše šlo tak, jak má, uvidíte, jak systém reaguje na změnu pozice snímače.

```python

pi@raspberrypi:~/grove.py/grove $ python grove_tilt_switch.py 12
Triggered
Released.
Triggered
^CTraceback (most recent call last):
  File "grove_tilt_switch.py", line 106, in <module>
    main()
  File "grove_tilt_switch.py", line 102, in main
    time.sleep(1)
KeyboardInterrupt

```

Program ukončíte stiskem ++ctrl+c++.

### Pokusy s Raspberry Pi (s modulem GrovePi_Plus)

### Pokusy s Raspberry Pi

1. Připravte si Raspberry Pi a modul Grovepi nebo Grovepi+.

2. Nastavte si vývojové prostředí pomocí průvodce [nastavení software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/).

3. Připojení

- Zapojte Tilt_Switch pomocí kabelu Grove do konektoru D3 na grovepi.

  4.Přesuňte se do adresáře s příklady:

```
       cd yourpath/GrovePi/Software/Python/
```

- Zkopírujte následující kód

```
    nano grovepi_tilt_switch.py   # "Ctrl+x" to exit #
```

```
    import time
    import grovepi

    # Připojte Grove Tilt Switch to digital port D3
    # SIG,NC,VCC,GND
    tilt_switch = 3

    grovepi.pinMode(tilt_switch,"INPUT")

    while True:
        try:
            print grovepi.digitalRead(tilt_switch)
            time.sleep(.5)

        except IOError:
            print "Error"
```

5.Spusťte ukázkový program.

```
    sudo python grove_tilt_switch.py
```

6.Výsledek: Když nakloníte snímač, změní se načtená hodnota.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Tilt_Switch/master/img/Grovepi_tilt_Switch_00.png)

## Reference

Rozsah spínání je zobrazen na tomto schématu:

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Tilt_Switch/master/img/Tilt_Switch_Operate.jpg)

<div class="admonition note">
<p class="admonition-title">Poznámka</p>
Značka J1 na modulu označuje referenční pozici.
</div>

## Zdroje

- [Grove - Tilt Switch v1.0 Eagle File](https://raw.githubusercontent.com/SeeedDocument/Grove-Tilt_Switch/master/res/Grove-Tilt_Switch_v1.0_Source_File.zip)
- [Grove - Tilt Switch v1.1 PDF File](https://raw.githubusercontent.com/SeeedDocument/Grove-Tilt_Switch/master/res/Grove-Tilt_Switch_v1.1_PDF_File.pdf)
- [Grove - Tilt Switch v1.1 Eagle File](https://raw.githubusercontent.com/SeeedDocument/Grove-Tilt_Switch/master/res/Grove-Tilt_Switch_v1.1_Eagle_File.zip)
- [SW200D Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Tilt_Switch/master/res/SW200D_datasheet.pdf)
- [Codecraft CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove-Tilt_Switch/master/res/Grove_Tilt_Switch_CDC_File.zip)

<!-- This Markdown file was created from http://www.seeedstudio.com/wiki/Grove_-_Tilt_Switch -->

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
