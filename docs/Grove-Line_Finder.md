---
name: Grove - Line Finder
category: Sensor
bzurl: https://www.seeedstudio.com/Grove-Line-Finder-v1.1-p-2712.html
oldwikiname: Grove - Line Finder
prodimagename: Grovelinefinder1.jpg
surveyurl: https://www.research.net/r/grove-line-finder
sku: 101020009
---

![](https://github.com/SeeedDocument/Grove_Line_Finder/raw/master/images/Grovelinefinder1.jpg)

Snímač čáry (Grove-Line finder) je navržen pro použití v robotech, které jezdí podle nakreslené čáry. Obsahuje zdroj infračerveného světla (LED) a snímač, citlivý na téže světlo (fototranzistor). Modul posílá digitální signál, takže robot snadno pozná, jestli správně sleduje černou čáru na bílém pozadí, případně bílou na černém pozadí.

[![](https://github.com/SeeedDocument/Grove_Line_Finder/raw/master/images/300px-Get_One_Now_Banner.png)](https://www.seeedstudio.com/Grove-Line-Finder-v1.1-p-2712.html)

## Verze

| Verze produktu         | Změny                  | Datum vydání |
| ---------------------- | ---------------------- | ------------ |
| Grove-Line Finder V1.0 | První vydání           | Jan 29 2010  |
| Grove-Line Finder V1.1 | Přidány testovací body | Dec 28 2015  |

## Specifikace

| Parametr             | Hodnota / Rozsah                                         |
| -------------------- | -------------------------------------------------------- |
| Napájecí napětí      | 5 V                                                      |
| Typ výstupu          | TTL (HIGH, pokud je pod snímačem černá, LOW, pokud bílá) |
| Konektor             | Čtyřpinový Grove                                         |
| Rozměr               | 20mm\*20mm                                               |
| ROHS                 | Ano                                                      |
| Fotoreflexivní dioda | RS-06WD                                                  |
| Komparátor           | MV358                                                    |

!!!Tip
Více detailů o modulech Grove zjistíte v [popisu systému Grove](http://wiki.seeedstudio.com/Grove_System/)

## Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                               | BeagleBone                                                                                          | Wio                                                                                                 | LinkIt ONE                                                                                             |
| ----------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Začínáme

### Pokusy s Arduinem

#### Hardware

- Krok 1: Připravte si tyto součástky:

| Seeeduino V4.2                                                                                                           | Base Shield                                                                                                           | Grove - Button                                                                                                       |
| ------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Line_Finder/raw/master/img/line_finder_s.jpg) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                          | [Koupit](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                      | [Koupit](https://www.seeedstudio.com/Grove-Line-Finder-v1.1-p-2712.html)                                             |

- Krok 2: Připojte Grove-line finder k portu D3 na Grove-Base Shieldu.
- Krok 3: Připojte Base Shield k Seeeduinu.
- Krok 4: Připojte Seeduino k PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove_Line_Finder/raw/master/img/seeeduino_line_finder.jpg)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit Grove-Line finder k Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino   | Grove-Line finder |
| ----------- | ----------------- |
| 5V          | Červený               |
| GND         | Černý             |
| Nepřipojeno | Bílý             |
| D3          | Žlutý            |

#### Software

- Krok 1: Zkopírujte kód do Arduino IDE, přeložte a nahrajte do Arduina.

```c
//------------------------------------------------------------
//Name: Line finder digital mode
//Function: detect black line or white line
//Parameter:   When digital signal is HIGH, black line
//             When digital signal is LOW, white line
//-------------------------------------------------------------
int signalPin =  3;    // connected to digital pin 3
void setup()   {
  pinMode(signalPin, INPUT); // initialize the digital pin as an output:
  Serial.begin(9600);  // initialize serial communications at 9600 bps:
}
// the loop() method runs over and over again,
// as long as the Arduino has power
void loop()
{
  if(HIGH == digitalRead(signalPin))
    Serial.println("black");
  else  Serial.println("white");  // display the color
  delay(1000);                  // wait for a second
}
```

- Krok 2: Otevřete sériový monitor v Arduino IDE. program vypisuje barvu povrchu pod snímačem.

```
white
white
white
black
black
black
black
black
```

### Pokusy s Codecraftem

#### Hardware

**Krok 1.** Připojte Grove - Line Finder k portu D3 na Grove-Base Shieldu

**Krok 2.** Připojte Base Shield k Seeeduinu / Arduinu.

**Krok 3.** Propojte Seeeduino/Arduino s PC pomocí kabelu USB.

#### Software

**Krok 1.** Spusťte [Codecraft](https://ide.chmakered.com/), přepněte se na prostředí pro Arduino a přidejte na plochu hlavní proceduru (Start).

!!!Poznámka
Pokud používáte Codecraft poprvé, podívejte se na [Průvodce světem Codecraftu a Arduina](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Krok 2.** Přetáhněte bloky tak, jak ukazuje následující obrázek, nebo otevřte cdc soubor, který si můžete stáhnout na konci této stránky.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove_Line_Finder/master/img/cc_Line_Finder.png)

Nahrajte hotový program do svého Arduina/Seeeduina.

!!!Povedlo se
Jakmile je nahrávání hotové, you will see line found or not in Serial Monitor.

### Pokusy s Raspberry Pi

#### Hardware

- Krok 1: Připravte si tyto součástky:

| Raspberry pi                                                                                                   | GrovePi_Plus                                                                                                         | Grove - Line Finder                                                                                                  |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove_Line_Finder/raw/master/img/line_finder_s.jpg) |
| [Koupit](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)                                       | [Koupit](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)                                                         | [Koupit](https://www.seeedstudio.com/Grove-Line-Finder-v1.1-p-2712.html)                                             |

- Krok 2: Připojte GrovePi_Plus k Raspberry Pi.
- Krok 3: Připojte Grove-Line Finder to D7 na GrovePi_Plus.
- Krok 4: Propojte Raspberry Pi s PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove_Line_Finder/raw/master/img/rasp_line_finder.jpg)

#### Software

- Krok 1: Nastavte si vývojové prostředí pomocí průvodce [nastavení software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/).
- Krok 2: Stáhněte si zdrojový kód tím, že naklonujete knihovnu GrovePi.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

- Krok 3: Spusťte následující příkazy.

```
cd ~/GrovePi/Software/Python
python grove_line_finder.py
```

Toto je kód v souboru grove_line_finder.py.

```python
import time
import grovepi

# Připojte Grove Line Finder to digital port D7
# SIG,NC,VCC,GND
line_finder = 7

grovepi.pinMode(line_finder,"INPUT")

while True:
    try:
        # Return HIGH when black line is detected, and LOW when white line is detected
        if grovepi.digitalRead(line_finder) == 1:
            print ("black line detected")
        else:
            print ("white line detected")

        time.sleep(.5)

    except IOError:
        print ("Error")
```

- Krok 4: Program vypisuje barvu povrchu pod snímačem.

```
pi@raspberrypi:~/GrovePi/Software/Python $ python grove_line_finder.py
black line detected
black line detected
white line detected
white line detected

```

## Zdroje

- **[Eagle&PDF]** [Grove-Line Finder Schematic V1.0](https://github.com/SeeedDocument/Grove_Line_Finder/raw/master/res/202000970_Grove%20-%20Line%20Finder%EF%BC%88CN%EF%BC%89%20v1.0.zip)
- **[Eagle&PDF]** [Grove-Line Finder Schematic V1.1](https://github.com/SeeedDocument/Grove_Line_Finder/raw/master/res/202000932_Grove%20-%20Line%20Finder%20v1.1.zip)
- **[Datasheet]** [LMV358.PDF](https://github.com/SeeedDocument/Grove_Line_Finder/raw/master/res/Lmv358.pdf)
- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove_Line_Finder/master/res/Grove_Line_Finder_CDC_File.zip)

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
