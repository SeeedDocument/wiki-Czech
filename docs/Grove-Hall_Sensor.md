---
name: Grove - Hall Sensor
category: Sensor
bzurl: https://seeedstudio.com/Grove-Hall-Sensor-p-965.html
oldwikiname: Grove_-_Hall_Sensor
prodimagename: Grove-Hall_Sensor_New.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/product/hall sensor.jpg
surveyurl: https://www.research.net/r/Grove-Hall_Sensor
sku: 101020046
tags: grove_digital, io_5v, plat_duino, plat_linkit
---

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Hall_Sensor/master/img/Grove-Hall_Sensor_New.jpg)

Hallův senzor je založen na Hallově jevu, při kterém vzniká elektrické napětí příčně k vodiči, kterým protéká proud, odchylovaný magnetickým polem. Výstup tohoto modulu je v úrovni LOW (aktivní), když intenzita magnetického pole, kolmé na snímač, překročí danou mez. Jakmile se magnetické pole zmenší či zmizí, výstup se přepne do HIGH (neaktivní). Snímač lze použít k měření otáček.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](http://www.seeedstudio.com/depot/grove-hall-sensor-p-965.html)

## Verze

| Revize                    | Descriptions           | Release    |
| ------------------------- | ---------------------- | ---------- |
| Grove - Hall Sensor v0.9b | První vydání public release | 3,Oct,2011 |

## Vlastnosti

- Rozhraní kompatibilní s Grove
- Přechodový čas 400ns při změně stavu.
- Spojitý signál na výstupu
- Ochrana proti přepólování

!!!Tip
Více detailů o modulech Grove zjistíte v [popisu systému Grove](http://wiki.seeedstudio.com/Grove_System/)

## Specifikace

| Parametr         | Min | Typical | Max | Jednotka |
| ---------------- | --- | ------- | --- | -------- |
| Napájecí napětí  | 3.8 | 5.0     | 24  | V        |
| Napájecí proud   | 4.1 | -       | 24  | mA       |
| Provozní teplota | -40 | -       | 85  | ºC       |

## Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                                 | BeagleBone                                                                                          | Wio                                                                                                 | LinkIt ONE                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Můžete použít pro

- Otáčkoměr.
- Řízení stejnosměrných motorů.

## Začínáme

!!!Poznámka
Pokud se s Arduinem setkáváte poprvé, doporučujeme vám pročíst návod [Začínáme s Arduinem](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) dřív, než začnete.

### Pokusy s Arduinem

#### Ukázka

Hallův senzor používáme jako zdroj vnějšího přerušení pro Arduino / Seeeduino. V tomto příkladu používáme přerušení 0, které je vyvedeno na pinu 2. Pokud chcete změnit vstup pro přerušení, podívejte se na popis funkce [attachInterrupt()](http://www.arduino.cc/en/Reference/AttachInterrupt).

#### Hardware

- **Krok 1.** Připravte si tyto součástky:

| Seeeduino V4.2                                                                                                             | Base Shield                                                                                                                | Grove - Hall Sensor                                                                                                                              |
| -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Hall_Sensor/master/img/Grove-Hall_Sensor_New%20_small.jpg) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                            | [Koupit](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                           | [Koupit](http://www.seeedstudio.com/depot/grove-hall-sensor-p-965.html)                                                                          |

- **Krok 2.** Připojte Grove - Hall Sensor k portu D2 na Grove-Base Shieldu.
- **Krok 3.** Připojte Base Shield k Seeeduinu.
- **Krok 4.** Připojte Seeduino k PC pomocí kabelu USB.

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit Grove - Hall Sensor k Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino   | Grove - Hall Sensor |
| ----------- | ------------------- |
| 5V          | Červený                 |
| GND         | Černý               |
| Nepřipojeno | Bílý               |
| D2          | Žlutý              |

#### Software

- **Krok 1.** Stáhněte si knihovnu [Hall Sensor Code](https://raw.githubusercontent.com/SeeedDocument/Grove-Hall_Sensor/master/res/Grove-Hall_Sensor_Demo_Code.zip)

- **Krok 2.** Otevřete některý z ukázkových příkladů, např. **MagnetControlLED**

* **Krok 3.** Zkopírujte kód do Arduino IDE, přeložte a nahrajte do Arduina. Pokud si nejste jisti, jak nahrát kód, podívejte se na stránku [Jak nahrát kód](http://wiki.seeedstudio.com/Upload_Code/).

```c
/****************************************************************************/
//	Function: When a magnet whose south pole is facing up is approaching to
//			  the onboard sensor, the LED will be turned on.Otherwise, the
//			  LED will be turned off.
//	Hardware: Grove - Hall Sensor, Grove - LED
//	Arduino IDE: Arduino-1.0
//	Author:	 FrankieChu
//	Date: 	 Jan 20,2013
//	Version: v1.0
//	by www.seeedstudio.com
//
//  This library is free software; you can redistribute it and/or
//  modify it under the terms of the GNU Lesser General Public
//  License as published by the Free Software Foundation; either
//  version 2.1 of the License, or (at your option) any later version.
//
//  This library is distributed in the hope that it will be useful,
//  but WITHOUT ANY WARRANTY; without even the implied warranty of
//  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
//  Lesser General Public License for more details.
//
//  You should have received a copy of the GNU Lesser General Public
//  License along with this library; if not, write to the Free Software
//  Foundation, Inc., 51 Franklin St, Fifth Floor, Boston, MA 02110-1301 USA
//
/*macro definitions of magnetic pin and LED pin*/
#define HALL_SENSOR 2
#define LED	4//the Grove - LED is connected to D4 of Arduino

void setup()
{
 	pinsInit();
}

void loop()
{
	if(isNearMagnet())//if the hall sensor is near the magnet?
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
	pinMode(HALL_SENSOR, INPUT);
	pinMode(LED,OUTPUT);
}

/*If the hall sensor is near the magnet whose south pole is facing up, */
/*it will return ture, otherwise it will return false.				*/
boolean isNearMagnet()
{
	int sensorValue = digitalRead(HALL_SENSOR);
	if(sensorValue == LOW)//if the sensor value is LOW?
	{
		return true;//yes,return ture
	}
	else
	{
		return false;//no,return false
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

- **Krok 4.** Když přiblížíte magnet jižním pólem k snímači, LED se rozsvítí. Po oddálení LED opět zhasne.

### Pokusy s Codecraftem

#### Hardware

**Krok 1.** Připojte Grove - Hall Sensor k portu D2 a Grove - Red LED k portu D4 na Grove-Base Shieldu

**Krok 2.** Připojte Base Shield k Seeeduinu / Arduinu.

**Krok 3.** Propojte Seeeduino/Arduino s PC pomocí kabelu USB.

#### Software

**Krok 1.** Spusťte [Codecraft](https://ide.chmakered.com/), přepněte se na prostředí pro Arduino a přidejte na plochu hlavní proceduru (Start).

!!!Poznámka
Pokud používáte Codecraft poprvé, podívejte se na [Průvodce světem Codecraftu a Arduina](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Krok 2.** Přetáhněte bloky tak, jak ukazuje následující obrázek, nebo otevřte cdc soubor, který si můžete stáhnout na konci této stránky.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove-Hall_Sensor/master/img/cc_Hall_Sensor.png)

Nahrajte hotový program do svého Arduina/Seeeduina.

!!!Povedlo se
Jakmile je nahrávání hotové, LED bude reagovat na přiblížení a oddálení magnetu.

## Zdroje

- **[Eagle]** [Grove-Hall Sensor Schematic](https://raw.githubusercontent.com/SeeedDocument/Grove-Hall_Sensor/master/res/Twig_Hall_Sensor_v0.9b.zip)

- **[Demo]** [Hall Sensor Demo Code](https://raw.githubusercontent.com/SeeedDocument/Grove-Hall_Sensor/master/res/Grove-Hall_Sensor_Demo_Code.zip)

- **[Datasheet]** [A1101 datasheet](http://www.allegromicro.com/en/Products/Part_Numbers/1101/1101.pdf)

- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove-Hall_Sensor/master/res/Grove_Hall_Sensor_CDC_File.zip)

<!-- This Markdown file was created from http://www.seeedstudio.com/wiki/Grove_-_Hall_Sensor -->

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
