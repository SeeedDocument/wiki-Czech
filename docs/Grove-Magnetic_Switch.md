---
name: Grove - Magnetic Switch
category: Sensor
bzurl: https://seeedstudio.com/Grove-Magnetic-Switch-p-744.html
oldwikiname: Grove_-_Magnetic_Switch
prodimagename: Magnetic_Switch.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/101020038 1.jpg
surveyurl: https://www.research.net/r/Grove-Magnetic_Switch
sku: 101020038
tags: grove_digital, io_3v3, io_5v, plat_duino, plat_pi, plat_bbg, plat_wio
---

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/img/45d.jpg)

Toto je modul magnetického spínače (jazýčkové relé), kompatibilní s rozhraním Grove. Používá jazýčkový kontakt CT10. CT10 je jednopólový spínač, který je v klidu rozpojený. Spíná se magnetickým polem, které můžete vytvořit permanentním magnetem, elektromagnetem či jejich kombinací. Magnetický spínač je skvělý pomocník při návrhu obvodů, které se mají zapínat či vypínat při přiblížení.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](http://www.seeedstudio.com/Grove-Magnetic-Switch-p-744.html)

## Vlastnosti

- Kompatibilní s rozhraním Grove
- Modul 2 x 2 cm
- Minimum dalších součástek
- Až do výkonu 10W
- Odolné pouzdro

!!!Tip
Více detailů o modulech Grove zjistíte v [popisu systému Grove](http://wiki.seeedstudio.com/Grove_System/)

## Můžete použít pro

- Snímač přiblížení
- Snímač zabezpečovacího systému
- Snímání hladiny
- Indikátor proudění
- Počítadlo pulsů

## Specifikace

<table border="1">
<tr>
<th scope="col">
Parametr
</th>
<th scope="col">
Min
</th>
<th scope="col">
Norm
</th>
<th scope="col">
Max
</th>
<th scope="col">
Jednotka
</th>
</tr>
<tr align="center">
<td>
Pracovní napětí
</td>
<td>
4.75
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
<td>
Spínaný výkon
</td>
<td colspan="3">
10
</td>
<td>
W
</td>
</tr>
<tr align="center">
<td>
Maximální spínané napětí AC,RMS
</td>
<td colspan="3">
&lt; 140
</td>
<td>
V
</td>
</tr>
<tr align="center">
<td>
Spínaný stejnosměrný proud
</td>
<td colspan="3">
&lt; 500
</td>
<td>
mA
</td>
</tr>
<tr align="center">
<td>
Stejnosměrná proudová zátěž v sepnutém stavu
</td>
<td colspan="3">
&lt; 0.5
</td>
<td>
A
</td>
</tr>
<tr align="center">
<td>
Odpor v sepnutém stavu
</td>
<td colspan="3">
&lt;200
</td>
<td>
mΩ
</td>
</tr>
<tr align="center">
<td>
Odpor v rozpojeném stavu
</td>
<td colspan="3">
&gt;10<sup>6</sup>
</td>
<td>
MΩ
</td>
</tr>
<tr align="center">
<td>
Provozní teplota
</td>
<td>
-40
</td>
<td>
-
</td>
<td>
125
</td>
<td>
℃
</td>
</tr>
<tr align="center">
<td>
Pracovní rozsah
</td>
<td>
10
</td>
<td>
-
</td>
<td>
40
</td>
<td>
AT
</td>
</tr>
</table>

!!!Tip
Více detailů o modulech Grove zjistíte v [popisu systému Grove](http://wiki.seeedstudio.com/Grove_System/)

## Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                               | BeagleBone                                                                                        | Wio                                                                                               | LinkIt ONE                                                                                             |
| ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Začínáme

!!!Poznámka
Pokud se s Arduinem setkáváte poprvé, doporučujeme vám pročíst návod [Začínáme s Arduinem](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) dřív, než začnete.

### Pokusy s Arduinem

#### Ukázka

Pin SIG je za normálních okolností v úrovni LOW. Jakmile se přiblíží magnet, jazýčkový kontakt sepne a pin SIG bude v úrovni HIGH.

#### Hardware

- **Krok 1.** Připravte si tyto součástky:

| Seeeduino V4.2                                                                                                             | Base Shield                                                                                                                | Grove - Magnetic Switch                                                                                                         |
| -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/img/45d_small.jpg) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                            | [Koupit](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                           | [Koupit](http://www.seeedstudio.com/Grove-Magnetic-Switch-p-744.html)                                                           |

- **Krok 2.** Připojte Grove - Magnetic Switch k portu **D2** na Grove-Base Shieldu.
- **Krok 3.** Připojte Base Shield k Seeeduinu.
- **Krok 4.** Připojte Seeduino k PC pomocí kabelu USB.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/img/with_ardu.jpg)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit Grove Button k
Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino   | Grove-Magnetic_Switch |
| ----------- | --------------------- |
| 5V          | Červený                   |
| GND         | Černý                 |
| Nepřipojeno | Bílý                 |
| D2          | Žlutý                |

#### Software

- **Krok 1.** Zkopírujte kód do Arduino IDE, přeložte a nahrajte do Arduina. Pokud si nejste jisti, jak nahrát kód, podívejte se na stránku [Jak nahrát kód](http://wiki.seeedstudio.com/Upload_Code/).

```c
/*******************************************************************************/

/* Kde je připojený spínač? */
#define MAGNETIC_SWITCH 2
//Vývod, k němuž je připojená LED
#define LED 13

void setup()
{
    pinsInit();
}

void loop()
{
    if(isNearMagnet()) //je poblíž snímače magnet?
    {
        turnOnLED();
    }
    else
    {
        turnOffLED();
    }
}
void pinsInit()
{
    pinMode(MAGNETIC_SWITCH, INPUT);
    pinMode(LED,OUTPUT);
}

/* Pokud je poblíž snímače magnet, vrátí true, jinak false */
boolean isNearMagnet()
{
    int sensorValue = digitalRead(MAGNETIC_SWITCH);
    if(sensorValue == HIGH) //je načtená hodnota HIGH?
    {
        return true; //ano, vrátíme true
    }
    else
    {
        return false; //ne, vrátíme false
    }
}
void turnOnLED()
{
    digitalWrite(LED,HIGH);
}
void turnOffLED()
{
    digitalWrite(LED,LOW);
}
```

- **Krok 2.** LED se rozsvítí, když přiblížíte magnet ke snímači. Zkuste si to!

### Pokusy s Codecraftem

#### Hardware

**Krok 1.** Připojte Grove - Magnetic Switch k portu D2 na Grove-Base Shieldu

**Krok 2.** Připojte Base Shield k Seeeduinu / Arduinu.

**Krok 3.** Propojte Seeeduino/Arduino s PC pomocí kabelu USB.

#### Software

**Krok 1.** Spusťte [Codecraft](https://ide.chmakered.com/), přepněte se na prostředí pro Arduino a přidejte na plochu hlavní proceduru (Start).

!!!Poznámka
Pokud používáte Codecraft poprvé, podívejte se na [Průvodce světem Codecraftu a Arduina](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Krok 2.** Přetáhněte bloky tak, jak ukazuje následující obrázek, nebo otevřte cdc soubor, který si můžete stáhnout na konci této stránky.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/img/cc_Magnetic_Switch.png)

Nahrajte hotový program do svého Arduina/Seeeduina.

!!!Povedlo se
Jakmile je nahrávání hotové, přiblížte magnet ke snímači a uvidíte, jak se LED na Arduinu rozsvítí.

### Pokusy s Raspberry Pi

#### Hardware

- **Krok 1.** Připravte si tyto součástky:

| Raspberry pi                                                                                                   | GrovePi_Plus                                                                                                         | Grove - Magnetic Switch                                                                                                         |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/img/45d_small.jpg) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                | [Koupit](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                     | [Koupit](http://www.seeedstudio.com/Grove-Magnetic-Switch-p-744.html)                                                           |

- **Krok 2.** Připojte GrovePi_Plus k Raspberry Pi.
- **Krok 3.** Připojte Grove-Magnetic-Switch ranger k portu **D2** na GrovePi_Plus.
- **Krok 4.** Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/img/with_rpi.jpg)

#### Software

- **Krok 1.** Nastavte si vývojové prostředí pomocí průvodce [nastavení software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/).

- **Krok 2.** Přesuňte se do adresáře s příklady:

```
cd yourpath/GrovePi/Software/Python/
```

- **Krok 3.** Zkopírujte následující kód (stejný kód lze použít i pro detektor náklonu)

```
nano grovepi_tilt_switch.py   # "Ctrl+x" to exit #
```

```py
import time
import grovepi

# Připojte Grove Tilt Switch to digital port D2
# SIG,NC,VCC,GND
tilt_switch = 2

grovepi.pinMode(tilt_switch,"INPUT")

while True:
    try:
        print grovepi.digitalRead(tilt_switch)
        time.sleep(.5)

    except IOError:
        print "Error"
```

- **Krok 4.** Spusťte ukázkový program.

```
sudo python grovepi_tilt_switch.py
```

- **Krok 5.** Výsledek

Když přiblížíte magnet ke snímači, změní se hodnota, načtená z vývodu SIG na 1.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/img/Grovepi_tilt_Switch_00.png)

## Zdroje

- **[Eagle]** [Grove-Magnetic Switch v0.9 Schematic](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/res/Magnetic_Switch.zip)

- **[Eagle]** [Grove-Magnetic Switch v1.3 Schematic](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/res/Grove-Magnetic_Switch_v1.3_Eagle_File.zip)

- **[PDF]** [Grove-Magnetic Switch v1.3 PDF File](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/res/Grove-Magnetic_Switch_v1.3_PDF_File.pdf)

- **[Datasheet]** [CT10 Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/res/CT10.pdf)

- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/res/Grove_Magnetic_Switch_CDC_File.zip)

<!-- This Markdown file was created from http://www.seeedstudio.com/wiki/Grove_-_Magnetic_Switch -->

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
