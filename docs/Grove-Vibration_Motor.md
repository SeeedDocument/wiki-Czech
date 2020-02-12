---
name: Grove - Vibration Motor
category: Actuator
bzurl: https://seeedstudio.com/Grove-Vibration-Motor-p-839.html
oldwikiname: Grove_-_Vibration_Motor
prodimagename: Gvib.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/product/gvib.jpg
surveyurl: https://www.research.net/r/Grove-Vibration_Motor
sku: 105020003
tags: grove_digital, io_3v3, io_5v, plat_duino, plat_linkit, plat_pi, plat_bbg
---

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Vibration_Motor/master/img/Gvib.jpg)

Miniaturní vibrační motorek, který lze použít jako mechanickou signalizaci. Když je vstup ve stavu HIGH, motorek vibruje stejně jako váš mobilní telefon v tichém režimu.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](http://www.seeedstudio.com/Grove-Vibration-Motor-p-839.html)

## Verze

| Revize | Popis                                        | Vydání        |
| ------ | -------------------------------------------- | ------------- |
| v0.9b  | První veřejné vydání                         | May 10, 2011  |
| v1.0   | Přímé připojení k I/O portům                 | Nov 5, 2011   |
| v1.2   | Přidán tranzistor pro zvýšení výkonu motorku | July 11, 2013 |

## Vlastnosti

- Kompatibilní s Grove
- Neslyšné
- Nízká spotřeba
- Vysoká spolehlivost

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
Typ
</th>
<th scope="col">
Max
</th>
</tr>
<tr align="center">
<th scope="row">
Pracovní napětí
</th>
<td>
3.0V
</td>
<td>
5.0V
</td>
<td>
5.5V
</td>
</tr>
<tr align="center">
<th scope="row">
Řízení
</th>
<td colspan="3" rowspan="1">
Logické úrovně
(HIGH = zapnutý motor, LOW = vypnutý motor.)
</td>
</tr>
<tr align="center">
<th scope="row">
Rychlost otáček
</th>
<td colspan="3" rowspan="1">
9000 rpm
</td>
</tr>
</table>

## Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                               | BeagleBone                                                                                        | Wio                                                                                                 | LinkIt ONE                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Začínáme

!!!Poznámka
Pokud se s Arduinem setkáváte poprvé, doporučujeme vám pročíst návod [Začínáme s Arduinem](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) dřív, než začnete.

### Pokusy s Arduinem

Rozvibrovat tento motor je stejně snadné, jako rozsvítit LED. Ukažme si to na jednoduchém příkladu.

#### Hardware

- **Krok 1.** Připravte si tyto součástky:

| Seeeduino V4.2                                                                                                             | Base Shield                                                                                                                | Grove - Vibration Motor                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Vibration_Motor/master/img/Gvib_small.jpg) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                            | [Koupit](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                           | [Koupit](http://www.seeedstudio.com/Grove-Vibration-Motor-p-839.html)                                                            |

- **Krok 2.** Připojte Grove - Vibration Motor k portu D2 na Grove-Base Shieldu.
- **Krok 3.** Připojte Base Shield k Seeeduinu.
- **Krok 4.** Připojte Seeduino k PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-Vibration_Motor/raw/master/img/vibration_motor.png)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit Grove - Vibration Motor k Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino   | Grove - Vibration Motor |
| ----------- | ----------------------- |
| 5V          | Červený                 |
| GND         | Černý                   |
| Nepřipojeno | Bílý                    |
| D2          | Žlutý                   |

#### Software

- **Krok 1.** Zkopírujte kód do Arduino IDE, přeložte a nahrajte do Arduina. Pokud si nejste jisti, jak nahrát kód, podívejte se na stránku [Jak nahrát kód](http://wiki.seeedstudio.com/Upload_Code/).

```c
int MoPin = 2;    // vibrator Grove connected to digital pin 9

void setup()  {
    pinMode( MoPin, OUTPUT );
}

void loop()  {

    digitalWrite(MoPin, HIGH);
    delay(1000);

    digitalWrite(MoPin, LOW);
    delay(1000);
}

```

- **Krok 2.** Zkuste si, jak motor vibruje!

### Pokusy s Codecraftem

#### Hardware

**Krok 1.** Připojte Grove - Vibration Motor k portu D2 na Grove-Base Shieldu

**Krok 2.** Připojte Base Shield k Seeeduinu / Arduinu.

**Krok 3.** Propojte Seeeduino/Arduino s PC pomocí kabelu USB.

#### Software

**Krok 1.** Spusťte [Codecraft](https://ide.chmakered.com/), přepněte se na prostředí pro Arduino a přidejte na plochu hlavní proceduru (Start).

!!!Poznámka
Pokud používáte Codecraft poprvé, podívejte se na [Průvodce světem Codecraftu a Arduina](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Krok 2.** Přetáhněte bloky tak, jak ukazuje následující obrázek, nebo otevřte cdc soubor, který si můžete stáhnout na konci této stránky.

![cc](https://github.com/SeeedDocument/Grove-Vibration_Motor/raw/master/img/cc_Vibration_Motor.png)

Nahrajte hotový program do svého Arduina/Seeeduina.

!!!Povedlo se
Jakmile je nahrávání hotové, ucítíte vibrace motorku.

### Pokusy s Raspberry Pi

#### Hardware

- **Krok 1.** Připravte si tyto součástky:

| Raspberry pi                                                                                                   | GrovePi_Plus                                                                                                         | Grove - Vibration Motor                                                                                                          |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Vibration_Motor/master/img/Gvib_small.jpg) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                | [Koupit](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                     | [Koupit](http://www.seeedstudio.com/Grove-Vibration-Motor-p-839.html)                                                            |

- **Krok 2.** Připojte GrovePi_Plus k Raspberry Pi.
- **Krok 3.** Připojte Grove - Vibration Motor k portu **D8** na GrovePi_Plus.
- **Krok 4.** Propojte Raspberry Pi s PC pomocí kabelu USB.

#### Software

- **Krok 1.** Přesuňte se do adresáře s příklady:

```
cd yourpath/GrovePi/Software/Python/
```

- **Krok 2.** Zkopírujte následující kód

```
nano grove_vibration_motor.py   # "Ctrl+x" to exit #
```

```python
import time
import grovepi

# Připojte Grove Vibration Motor to digital port D8
# SIG,NC,VCC,GND
vibration_motor = 8

grovepi.pinMode(vibration_motor,"OUTPUT")

while True:
    try:
        # Start vibrating for 1 second
        grovepi.digitalWrite(vibration_motor,1)
        print 'start'
        time.sleep(1)

        # Stop vibrating for 1 second, then repeat
        grovepi.digitalWrite(vibration_motor,0)
        print 'stop'
        time.sleep(1)

    except KeyboardInterrupt:
        grovepi.digitalWrite(vibration_motor,0)
        break
    except IOError:
        print "Error"
```

- **Krok 3.** Spusťte ukázkový program.

```
sudo python grove_vibration_motor.py
```

## Zdroje

- **[Eagle]** [Grove - Vibration Motor Schematic](https://raw.githubusercontent.com/SeeedDocument/Grove-Vibration_Motor/master/res/Grove-Vibration_Motor_Eagle_Files.zip)

- **[Datasheet]** [S9013 Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Vibration_Motor/master/res/S9013.pdf)

- **[Datasheet]** [ANDA-B1020 Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Vibration_Motor/master/res/ANDA-B1020_datasheet.pdf)

- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove_Vibration_Motor/master/resource/Grove_Vibration_Motor_CDC_File.zip)

<!-- This Markdown file was created from http://www.seeedstudio.com/wiki/Grove_-_Vibration_Motor -->

## Projekt

**Grove - Introduction in a Vibration Motor - only for adults**: Beginner-Example

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/ingo-lohs/grove-introduction-in-a-vibration-motor-only-for-adults-2acfc2/embed' width='350'></iframe>

Inspirovali jsme se hrou OVERWATCH a pro pobavení jsme si udělali dřevěný model laserové pistole!

Laserová pistole a Terč pro pistoli jsou založené na Arduinu s názvem Seeeduino Lotus. Laserový zdroj v laserové pistoli posílá pulsy na terč. Terč obsahuje tři světelné senzory, které hlídají, zda paprsek zasáhl cíl. Vypadá to velmi jednoduše, že? Pokud vás tento projekt zaujal, udělejte si jej také. Stojí za to strávit jeden den stavbou takové hračky pro sebe nebo pro vaše děti.

[![](https://raw.githubusercontent.com/SeeedDocument/Seeeduino_Lotus/master/img/gun.jpg)](http://www.instructables.com/id/DIY-a-Wooden-Laser-Gun-As-a-Xmas-Present-for-Your-/)

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
