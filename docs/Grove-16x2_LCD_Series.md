---
name: Grove - 16 x 2 LCD
category: Display
bzurl:
oldwikiname:
prodimagename:
surveyurl:
sku: 104020111,104020112,104020113
tags:
---

![](https://github.com/SeeedDocument/Grove-16x2_LCD_Series/raw/master/img/main.jpg)

[Grove - LCD RGB Backlight](http://wiki.seeedstudio.com/Grove-LCD_RGB_Backlight/) je favoritem od té chvíle, co jsme jej představili. Na základě připomínek od uživatelů jsme připravili levnější varianty s jednobarevným podsvícením, jako jsou:

The Grove - 16 x 2 LCD (Modré písmo na žlutém pozadí)  
The Grove - 16 x 2 LCD (Černé písmo na červeném pozadí)  
The Grove - 16 x 2 LCD (Bílé písmo na modrém pozadí)

Tyto produkty jsou jinak téměř totožné jako Grove - LCD RGB Backlight, s výjimkou RGB podsvícení. Mají rovněž 16 znaků na řádek, 2 řádky textu a jasné podsvícení.

<p style=":center"><a href="https://www.seeedstudio.com/Grove-16-x-2-LCD-%28Black-on-Yellow%29-p-3198.html" target="_blank"><img src="https://github.com/SeeedDocument/Grove-16x2_LCD_Series/raw/master/img/Y1.png" height="48" width="300" /></a></p>
<p style=":center"><a href="https://www.seeedstudio.com/Grove-16-x-2-LCD-%28Black-on-Red%29-p-3197.html" target="_blank"><img src="https://github.com/SeeedDocument/Grove-16x2_LCD_Series/raw/master/img/R1.png" height="48" width="300" /></a></p>
<p style=":center"><a href="https://www.seeedstudio.com/Grove-16-x-2-LCD-%28White-on-Blue%29-p-3196.html" target="_blank"><img src="https://github.com/SeeedDocument/Grove-16x2_LCD_Series/raw/master/img/B1.png"  height="48" width="300" /></a></p>

## Vlastnosti

- Konstrukce displeje: 16 znaků x 2 řádky
- Technologie: STN (Žlutá a zelená)
- Integrovaný řadič
- Rozhraní pro sběrnici I2C
- Anglické a japonské znaky

## Specifikace

| Parametr           | Hodnota             |
| ------------------ | ------------------- |
| Pracovní napětí    | 3.3V / 5V           |
| Provozní teplota   | 0 to 50℃            |
| Skladovací teplota | -10 to 60℃          |
| Parametry řízení   | 1/16 duty, 1/5 bias |
| Rozhraní           | I^2^C               |
| Adresa I^2^C       | 0X3E                |

## Typické využití

- Zobrazení teploty
- Zobrazení času
- Projekty, které vyžadují jednoduchý displej

## Hardwarové parametry

### Rozměry

![](https://github.com/SeeedDocument/Grove-16x2_LCD_Series/raw/master/img/outline.jpg)

## Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                                 | BeagleBone                                                                                          | Wio                                                                                                 | LinkIt ONE                                                                                             |
| ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Začínáme

### Pokusy s Arduinem

#### Hardware

**Potřebné součástky**

| Seeeduino V4.2                                                                                                           | Base Shield                                                                                                           | Grove - 16 x 2 LCD                                                                                                     |
| ------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-16x2_LCD_Series/raw/master/img/perspective.jpg) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                          | [Koupit](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                      | [Koupit](https://www.seeedstudio.com/Grove-16-x-2-LCD-%28Black-on-Yellow%29-p-3198.html)                               |

!!!Poznámka

**1** Buďte opatrní při připojování USB kabelu, můžete poškodit konektor. Používejte datové kabely (se čtyřmi vodiči), ne napájecí (se dvěma vodiči). Pokud si nejste jisti, jaký USB kabel máte, můžete si [u nás koupit doporučený](https://www.seeedstudio.com/Micro-USB-Cable-48cm-p-1475.html)

**2** Všechny Grove moduly jsou prodávány s propojovacím kabelem Grove. Pokud jej ztratíte, můžete si [u nás koupit náhradní Grove kabel](https://www.seeedstudio.com/Grove-Universal-4-Pin-Buckled-20cm-Cable-%285-PCs-pack%29-p-936.html).

- **Krok 1.** Připojte Grove - 16 x 2 LCD k portu **I^2^C** na Grove-Base Shieldu.

- **Krok 2.** Připojte Base Shield k Seeeduinu.

- **Krok 3.** Připojte Seeduino k PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-16x2_LCD_Series/raw/master/img/connect.jpg)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit Grove - 16 x 2 LCD k
Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino  | Grove Cable | Grove - 16 x 2 LCD |
| ---------- | ----------- | ------------------ |
| GND        | Černý       | GND                |
| 5V or 3.3V | Červený         | VCC                |
| SDA        | Bílý       | SDA                |
| SCL        | Žlutý      | SCL                |

#### Software

!!!Poznámka
Pokud se s Arduinem setkáváte poprvé, doporučujeme vám pročíst návod [Začínáme s Arduinem](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) dřív, než začnete.

- **Krok 1.** Stáhněte si knihovnu [Grove-LCD RGB Backlight](https://github.com/Seeed-Studio/Grove_LCD_RGB_Backlight/archive/master.zip) z GitHubu.

!!!Tipy
Grove - 16 x 2 LCD používá stejné knihovny jako [Grove-LCD RGB Backlight](http://wiki.seeedstudio.com/Grove-LCD_RGB_Backlight/). Jediný rozdíl je, že Grove - 16 x 2 LCD nepodporuje příkazy pro řízení barvy podsvícení, jako **setRGB()**.

- **Krok 2.** S instalací knihovny pro Arduino vám pomůže návod [Jak instalovat knihovnu pro Arduino](http://wiki.seeedstudio.com/How_to_install_Arduino_Library).

- **Krok 3.** Restartujte Arduino IDE. Otevřete ukázkový příklad jedním z následujících postupů：

  1. Přímo v Arduino IDE jej vyberte pomocí menu: **File --> Examples --> Grove - LCD RGB Backlight --> HelloWorld**.
     ![](https://github.com/SeeedDocument/Grove-16x2_LCD_Series/raw/master/img/path_1.jpg)

  2. Otevřte jej z počítače kliknutím na **HelloWorld.ino**, který naleznete ve složce **XXXX\Arduino\libraries\Grove_LCD_RGB_Backlight-master\examples\HelloWorld**. **XXXX** je složka, ve které máte instalované Arduino IDE.
     ![](https://github.com/SeeedDocument/Grove-16x2_LCD_Series/raw/master/img/path_2.jpg)

  3. Můžete kliknout na ikonu ![](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/copy.jpg) v pravém horním rohu výpisu programu a zkopírovat následující kód do nového sketche v Arduinu IDE.

```C++
#include <Wire.h>
#include "rgb_lcd.h"

rgb_lcd lcd;

/*
const int colorR = 255;
const int colorG = 0;
const int colorB = 0;
*/

void setup()
{
    // Nastavíme počet řádků a znaků na řádek:
    lcd.begin(16, 2);

    //lcd.setRGB(colorR, colorG, colorB);

    // Print a message to the LCD.
    lcd.print("hello, world!");

    delay(1000);
}

void loop()
{
    //Nastavíme kurzor na sloupec 0, řádek 1
    // (pozn.: řádek 1 je druhý, protože číslování začíná od 0):
    lcd.setCursor(0, 1);
    // vypíšeme počet sekund od resetu:
    lcd.print(millis()/1000);

    delay(100);
}

/*********************************************************************************************************
  END FILE
*********************************************************************************************************/
```

!!!Pozor
1** Knihovna může být aktualizována. V takovém případě se může stát, že tento kód nebude s novou verzí knihovny kompatibilní, proto doporučujeme použití předchozích metod.  
 2** Protože má **Grove - 16 x 2 LCD** jednobarevné podsvícení, je zakomentovaný kód, který nastavuje RGB barvy. V kódu výše to jsou řádky 6 a 17.

- **Krok 4.** Nahrajte přeložený kód do Arduina. Pokud si nejste jisti, jak nahrát kód, podívejte se na stránku [Jak nahrát kód](http://wiki.seeedstudio.com/Upload_Code/).

!!!Povedlo se
Pokud vše proběhlo, jak má, uvidíte na displeji klasický nápis: hello world.

## Zdroje

- **[Zip]** [Grove-LCD RGB Backlight Library](https://github.com/Seeed-Studio/Grove_LCD_RGB_Backlight/archive/master.zip)

- **[PDF]** [JDH_1804_Datasheet](https://github.com/SeeedDocument/Grove-16x2_LCD_Series/raw/master/res/JDH_1804_Datasheet.pdf)

## Projekt

Podívejte se na ukázkové video tohoto produktu a na jednoduché příkaldy, které si můžete vyzkoušet.

<iframe width="560" height="315" src="https://www.youtube.com/embed/3slfeHKSSCw?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

**Vizualizace trasy s Mapami Google**：Používáme Wio LTE cat.1 pro monitorování GPS a dalších informací z vozu. U chladících vozů můžeme sledovat kromě GPS i teplotu a vlhkost. Můžete sledovat i jízdní kolo a spolu s pozicí monitorovat třeba srdeční frekvenci.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://project.seeedstudio.com/SeeedStudio/transportation-data-visualization-with-google-map-517ce4/embed' width='350'></iframe>

**Vizualizace znečištění ovzduší**：Problém znečištění ovzduší přitahuje stále větší pozornost. Tentokrát jsme zkusili monitorovat PM2.5 (polétavý prach) pomocí Wio LTE a nového laserového snímače PM2.5.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://project.seeedstudio.com/SeeedStudio/atmospheric-pollution-visualization-1940f4/embed' width='350'></iframe>

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/).

<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
