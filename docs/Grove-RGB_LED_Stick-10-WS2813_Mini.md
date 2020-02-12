---
name: Grove - RGB LED Stick (10 WS2813 Mini)
category: Sensor
bzurl:
oldwikiname:
prodimagename:
surveyurl:
sku: 104020131
tags:
---

![](https://github.com/SeeedDocument/Grove-RGB_LED_Stick-10-WS2813_Mini/raw/master/img/main.jpg)

Na tuto desku jsme umístili deset barevných RGB LED, a všechny můžete ovládat jediným signálem. Použili jsme diody WS2813 Mini, které jsou snadno ovladatelné a cenově přijatelné.
Výhodou je i to, že WS2813 dokážou předávat příkazy, i když se rozbijí, takže pokud si jednu LED poškodíte, budou ostatní fungovat dál.

S touto světelnou hůlkou můžete vytvořit nespočet světelných efektů a užít si spoustu zábavy.

<p style=":center"><a href="https://www.seeedstudio.com/Grove-RGB-LED-Stick-10-WS2813-Min-p-3226.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/300px-Get_One_Now_Banner-ragular.png" /></a></p>

## Verze

| Verze produktu                         | Změny        | Datum vydání |
| -------------------------------------- | ------------ | ------------ |
| Grove - RGB LED Stick (10 WS2813 Mini) | První vydání | Nov 2018     |

## Vlastnosti

- WS2813B IC, 3535 LED
- Inteligentní ochrana proti přepólování
- Každá LED dokáže nastavit jednotlivé barevné složky v 256 úrovních jasu, takže získáváme celkem “256x256x256=16777216” možných barev.
- Obnovovací frekvence je až 2 kHz.
- Komunikace přes sériové rozhraní po jediné lince.
- Dvojí vedení signálu zajišťuje funkčnost zbytku LED i v případě poruchy jedné či více LED.

### Odolnost proti poruchám

![](https://github.com/SeeedDocument/Outsourcing/raw/master/104020108/img/LED_RFBP.jpg)

Pokud nejsou poškozeny dvě LED bezprostředně vedle sebe, funguje přenos příkazů k ostatním LED bez problémů.

## Specifikace

| Parametr                     | Hodnota                   |
| ---------------------------- | ------------------------- |
| Pracovní napětí              | 3.3V / 5V                 |
| Provozní teplota             | -25℃ ~ +85℃               |
| Skladovací teplota           | -40℃ ~ +105℃              |
| Konstantní proud RGB kanálem | 16mA                      |
| Rozhraní                     | Digital                   |
| Velikost                     | D: 80mm Š: 10mm V: 10mm   |
| Hmotnost                     | 3.7g                      |
| Velikost balení              | D: 150mm Š: 100mm V: 25mm |
| Hmotnost včetně obalu        | 13g                       |

## Typické využití

- Vánoční dekorace
- Osvětlení
- Hračky

## Hardwarové parametry

### Zapojení vývodů

![](https://github.com/SeeedDocument/Grove-RGB_LED_Stick-10-WS2813_Mini/raw/master/img/pin_out.jpg)

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

| Seeeduino V4.2                                                                                                             | Base Shield                                                                                                                | Grove - RGB LED Stick (10 WS2813 Mini)                                                                                            |
| -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-RGB_LED_Stick-10-WS2813_Mini/raw/master/img/thumbnail.jpg) |
| <a href="http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html" target="_blank">Koupit</a>                                 | <a href="https://www.seeedstudio.com/Base-Shield-V2-p-1378.html" target="_blank">Koupit</a>                                | <a href="https://www.seeedstudio.com/Grove-RGB-LED-Stick-10-WS2813-Min-p-3226.html" target="_blank">Koupit</a>                    |

!!!Poznámka
**1** Buďte opatrní při připojování USB kabelu, můžete poškodit konektor. Používejte datové kabely (se čtyřmi vodiči), ne napájecí (se dvěma vodiči). Pokud si nejste jisti, jaký USB kabel máte, můžete si [u nás koupit doporučený](https://www.seeedstudio.com/Micro-USB-Cable-48cm-p-1475.html)

**2** Všechny Grove moduly jsou prodávány s propojovacím kabelem Grove. Pokud jej ztratíte, můžete si [u nás koupit náhradní Grove kabel](https://www.seeedstudio.com/Grove-Universal-4-Pin-Buckled-20cm-Cable-%285-PCs-pack%29-p-936.html).

!!!Důležité
**1**. Pokud používáte Arduino UNO, doporučujeme použít externí zdroj. RGB LED Stick může způsobit pokles napájecího napětí Arduina až o 100 mV. Pokud používáte Seeduino V4.2, není externí zdroj zapotřebí.

**2**. Nelze připojovat za provozu. Připojujte a odpojujte pouze při vypnutém Arduinu.

- **Krok 1.** Připojte Grove - RGB LED Stick (10 WS2813 Mini) k portu **D6** na Grove-Base Shieldu.

- **Krok 2.** Připojte Base Shield k Seeeduinu.

- **Krok 3.** Připojte Seeduino k PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-RGB_LED_Stick-10-WS2813_Mini/raw/master/img/connect.jpg)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit Grove Button k
Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino  | Grove Cable | Grove - RGB LED Stick (10 WS2813 Mini) |
| ---------- | ----------- | -------------------------------------- |
| GND        | Černý       | GND                                    |
| 5V or 3.3V | Červený     | VCC                                    |
| Nezapojeno | Bílý        | Nepřipojeno                            |
| D6         | Žlutý       | SIG                                    |

#### Software

!!!Poznámka
Pokud se s Arduinem setkáváte poprvé, doporučujeme vám pročíst návod [Začínáme s Arduinem](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) dřív, než začnete.

- **Krok 1.** Stáhněte si knihovnu [Led_Strip](https://github.com/Seeed-Studio/Seeed_Led_Strip) z GitHubu.

- **Krok 2.** S instalací knihovny pro Arduino vám pomůže návod [Jak instalovat knihovnu pro Arduino](http://wiki.seeedstudio.com/How_to_install_Arduino_Library).

- **Krok 3.** Restartujte Arduino IDE. Otevřete ukázkový příklad jedním z následujících postupů：

  1. Přímo v Arduino IDE jej vyberte pomocí menu: **File --> Examples --> Adafruit_Neopixel --> simple**.
     ![](https://github.com/SeeedDocument/Grove-RGB_LED_Stick-10-WS2813_Mini/raw/master/img/path1.jpg)

  2. Otevřte jej z počítače kliknutím na **simple.ino**, který naleznete ve složce **XXXX\Arduino\libraries\Seeed_Led_Strip-master\examples\simple**. **XXXX** je složka, ve které máte instalované Arduino IDE.
     ![](https://github.com/SeeedDocument/Grove-RGB_LED_Stick-10-WS2813_Mini/raw/master/img/path2.jpg)

  3. Můžete kliknout na ikonu ![](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/copy.jpg) v pravém horním rohu výpisu programu a zkopírovat následující kód do nového sketche v Arduinu IDE.

```C++
// NeoPixel Ring simple sketch (c) 2013 Shae Erisson
// released under the GPLv3 license to match the rest of the AdaFruit NeoPixel library

#include "Adafruit_NeoPixel.h"
#ifdef __AVR__
  #include <avr/power.h>
#endif

// Který pin je připojen k LED?
// On a Trinket or Gemma we suggest changing this to 1
#define PIN            6

// Kolik LED je zapojeno za sebou?
#define NUMPIXELS      10

// Když nastavujeme knihovnu, je důležité říct, kolik LED je za sebou a k jakému pinu jsou připojené.
// Pro starší typy LED je třeba nastavit třetí parametr - podrobnosti
// naleznete v dokumentaci.
Adafruit_NeoPixel pixels = Adafruit_NeoPixel(NUMPIXELS, PIN, NEO_GRB + NEO_KHZ800);

int delayval = 500; // Pauza půl sekundy

void setup() {
  // This is for Trinket 5V 16MHz, you can remove these three lines if you are not using a Trinket
#if defined (__AVR_ATtiny85__)
  if (F_CPU == 16000000) clock_prescale_set(clock_div_1);
#endif
  // End of trinket special code
  pixels.setBrightness(255);
  pixels.begin(); // Inicializace knihovny NeoPixel.
}

void loop() {

  // Při nastavování LED má první číslo 0, druhá 1 a tak dále až do počtu LED mínus 1.

  for(int i=0;i<NUMPIXELS;i++){

    // pixels.Color požaduje hodnoty RGB od 0,0,0 až po 255,255,255
    pixels.setPixelColor(i, pixels.Color(0,150,0)); // zelená, střední jas.

    pixels.show(); // Odešle nové hodnoty do LED

    delay(delayval); // Počkáme chvíli (v milisekundách).

  }
}
```

!!!Pozor
Knihovna může být aktualizována. V takovém případě se může stát, že tento kód nebude s novou verzí knihovny kompatibilní, proto doporučujeme použití předchozích metod.

- **Krok 4.** Nahrajte přeložený kód do Arduina. Pokud si nejste jisti, jak nahrát kód, podívejte se na stránku [Jak nahrát kód](http://wiki.seeedstudio.com/Upload_Code/).

!!!Povedlo se
Pokud vše proběhlo jak má, uvidíte blikající LED pásek:

![](https://github.com/SeeedDocument/Grove-RGB_LED_Stick-10-WS2813_Mini/raw/master/img/test20181210_162208.gif)

## Zdroje

- **[Zip]** [Grove - RGB LED Stick (10 WS2813 Mini) Eagle Files](<https://github.com/SeeedDocument/Grove-RGB_LED_Stick-10-WS2813_Mini/raw/master/res/Grove%20-%20RGB%20LED%20Stick%20(10-WS2813%20Mini).zip>)

- **[Zip]** [Led_Strip Library](https://github.com/Seeed-Studio/Seeed_Led_Strip/archive/master.zip)

- **[PDF]** [Datasheet WS2813-Mini](https://github.com/SeeedDocument/Grove-RGB_LED_Stick-10-WS2813_Mini/raw/master/res/WS2813-Mini.pdf)

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/).<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
