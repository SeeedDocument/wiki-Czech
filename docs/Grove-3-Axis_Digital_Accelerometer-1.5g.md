---
name: Grove - 3-Axis Digital Accelerometer(±1.5g)
category: Sensor
bzurl: https://seeedstudio.com/Grove-3-Axis-Digital-Accelerometer(±1.5g)-p-765.html
oldwikiname: Grove_-_3-Axis_Digital_Accelerometer(±1.5g)
prodimagename: 3_aix_acc.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/101020039 1.jpg
surveyurl: https://www.research.net/r/Grove-3-Axis_Digital_Accelerometer-1_5g
sku: 101020039
tags: grove_i2c, io_3v3, io_5v, plat_duino, plat_linkit, plat_wio
---

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><div class="center">
<div class="floatnone">
<img src="https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/img/3_aix_acc.jpg" />
</div>
</div></td>
<td><div class="center">
<div class="floatnone">
<img src="https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/img/Grove-3-Axis_v1.3.jpg" />
</div>
</div></td>
</tr>
<tr class="even">
<td><div style=": center">
Grove - 3-Axis Digital Accelerometer v1.2
</div></td>
<td><div style=": center">
Grove - 3-Axis Digital Accelerometer v1.2b
</div></td>
</tr>
</tbody>
</table>

3-Axis Digital Accelerometer (tříosý digitální akcelerometr) je klíčová součástka pro projekty, které zahrnují detekci orientace zařízení, pohybu či gest. Tento měřič zrychlení (do velikosti ±1.5g) je založen na úsporném čipu MMA7660FC od Freescale. Snímač vydrží krátkodobé přetížení až 10,000g a má nastavitelný počet měření za sekundu. Běžné aplikace nepotřebují příliš velký rozsah měření, a tak je tento modul ideální volba, protože je odolný, levný a má malou spotřebu energie.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](<http://www.seeedstudio.com/Grove-3-Axis-Digital-Accelerometer(%C2%B11.5g)-p-765.html>)

## Specifikace

- Pracovní napětí: 3.0 - 5.5V
- Odběr v neaktivním stavu: 0.4μA
- Odběr ve stavu připravenosti: 2μA
- Odběr při měření: 47 μA při 1 ODR
- Rozsah měření: ±1.5g
- Citlivost: 21LSB/g
- Knihovna kompatibilní se Suli

!!!Tip
Více detailů o modulech Grove zjistíte v [popisu systému Grove](http://wiki.seeedstudio.com/Grove_System/)

## Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                                 | BeagleBone                                                                                          | Wio                                                                                               | LinkIt ONE                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Ukázka s [Arduinem](/Arduino "Arduino")

Ukážeme si, jak z tohoto snímače získat surová naměřená data a hodnotu zrychlení (v "g").

Připojte modul k portu I^2^C na Grove - Base Shield příslušným kabelem.

<div class="admonition note">
<p class="admonition-title">Poznámka</p>
Pokud chcete použít funkci přerušení (Interrupt) na tomto modulu, musíte propojit pájecí bod INT, který jsme připravili, se vstupem Arduina, který může vyvolat přerušení.
</div>

![](https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/img/Digital_Accelerometer_Sensor_Connector1.5g.jpg)

Nainstalujte knihovnu, kterou jsme připravili v sekci Zdroje ([Resources](/Grove-3-Axis_Digital_Accelerometer-1.5g#resources)).

Otevřte soubor pomocí menu: File -> Example ->DigitalAccelerometer_MMA7660FC ->MMA7660FC_Demo.

V této ukázce jsou data posílána ze senzoru do Seeeduina po sběrnici I^2^C a Seeeduino je vypisuje v sériovém monitoru.
Otevřete jej a sledujte výstupní hodnoty.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/img/Grove-3-Axis_Digital_Accelerometer-1.5g-.jpg)

Výstup obsahuje dva typy dat: surová naměřená data a informaci o zrychlení, přepočtenou na jednotky "g".

### Pokusy s Raspberry Pi

1. Připravte si Raspberry Pi a modul Grovepi nebo Grovepi+.

2. Nastavte si vývojové prostředí pomocí průvodce [nastavení software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/).

3. Připojení

- Připojte snímač ke GrovePi portu i2c-x(1~3) příslušným kabelem.

  4.Přesuňte se do adresáře s příklady:

         cd yourpath/GrovePi/Software/Python/

- Zkopírujte následující kód

```
    nano grove_i2c_accelerometer.py   # "Ctrl+x" to exit #
```

```
    import time
    import grovepi

    # Připojte Grove Accelerometer (+/- 1.5g) to any I2C port eg. I2C-1
    # Can be found at I2C address 0x4c
    # SCL,SDA,VCC,GND

    while True:
        try:
            print grovepi.acc_xyz()
            time.sleep(.5)

        except IOError:
            print "Error"
```

5.Spusťte ukázkový program.

```
    sudo python grove_i2c_accelerometer.py
```

## Reference

Na ilustracích níže je ukázán fyzikální význam měřených hodnot.

První obrázek ukazuje význam os a kladný / záporný směr:
![](https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/img/MMA7660_Direction.jpg)

Druhý obrázek ukazuje některé příklady:

![](https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/img/Sensing_Direction_1.jpg)

## Zdroje

- [Datasheet of MMA7660FC](https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/res/MMA7660FC.pdf)
- [Grove - 3-Axis Digital Accelerometer Eagle File](https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/res/Grove-3-Axis_Digital_Accelerometer-1.5g-Eagle_File.zip)
- [github repository for 3-Axis Digital Accelerometer(±1.5g)](https://github.com/Seeed-Studio/Accelerometer_MMA7660)

## Projekt

**Pohybem aktivovaný blikač pro běžce** Přenosný blikač reaguje na otřesy při pohybu. Navíc s ventilátorem a alarmem.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/chuartdo/tilt-activated-spinning-fan-light-stick-e05cec/embed' width='350'></iframe>

**Rádiem řízená plachetnice**
Tuto plachetnici ovládáte přes internet. Pomocí GSM modulu posílá v reálném čase informace ze senzorů (GPS, gyroskop, akcelerometr a kompas) a přijímá pokyny pro servo.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/anemoi/lean-green-rc-sailing-machine-2cdde5/embed' width='350'></iframe>

<!-- This Markdown file was created from http://www.seeedstudio.com/wiki/Grove_-_3-Axis_Digital_Accelerometer(±1.5g) -->

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
