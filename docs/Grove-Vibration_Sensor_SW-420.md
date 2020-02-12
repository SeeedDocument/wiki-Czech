---
name: Grove - Vibration Sensor (SW-420)
category: Sensor
bzurl:
oldwikiname:
prodimagename:
surveyurl:
sku: 101020586
tags:
---

![](https://github.com/SeeedDocument/Grove-Vibration_Sensor-SW-420/raw/master/img/main.jpg)

Snímač otřesů (Grove - Vibration Sensor) s obvodem SW-420 je citlivý všesměrový detektor vibrací. Pokud je model v klidu, je výstup v úrovni HIGH. Při pohybu nebo otřesech se výstup přepne do stavu LOW. U modulu můžete nastavit citlivost detekce.

Tímto modulem můžete detekovat otřesy, popřípadě pohyb.

<p style=":center"><a href="https://www.seeedstudio.com/Grove-Vibration-Sensor-%28SW-420%29-p-3158.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/300px-Get_One_Now_Banner-ragular.png" /></a></p>

## Verze

| Verze produktu                    | Změny        | Datum vydání |
| --------------------------------- | ------------ | ------------ |
| Grove - Vibration Sensor (SW-420) | První vydání | Sep 2018     |

## Vlastnosti

- Všesměrový
- Vysoce citlivý
- Reaguje na otřesy nebo na pohyb
- Voděodolný
- Odolný proti stlačení

## Specifikace

| Parametr              | Hodnota                  |
| --------------------- | ------------------------ |
| Pracovní napětí       | 3.3V / 5V                |
| Rozhraní              | Digitální                |
| Velikost              | D: 40mm Š: 20mm V: 10mm  |
| Hmotnost              | 4.3g                     |
| Velikost balení       | D: 140mm Š: 85mm V: 10mm |
| Hmotnost včetně obalu | 10g                      |

## Použití

- Poplašné zařízení proti odcizení do auta, kola, motocyklu...
- Ovládání her
- Detekce otřesů

## Hardwarové parametry

### Popis vývodů

![](https://github.com/SeeedDocument/Grove-Vibration_Sensor-SW-420/raw/master/img/pin_map.jpg)

1. SIG: Výstupní signál Vout
2. NC: Není zapojeno
3. VCC: Napájecí napětí, 5 nebo 3,3 V
4. GND: Zem. Připojte k systémové zemi
5. Trimr: Pomocí šroubováku můžete tento trimr otočit a nastavit tak citlivost snímače
6. GND: Zem pro potenciometr
7. Vsen: Rozhodovací úroveň napětí. Čím nižší, tím vyšší citlivost
8. VCC: VCC pro potenciometr
9. SW-420: Snímací obvod

### Schéma

![](https://github.com/SeeedDocument/Grove-Vibration_Sensor-SW-420/raw/master/img/Schematic.jpg)

Nejdůležitější část je spínač **SW1** vlevo dole. To je ve skutečnosti samotný snímač vibrací **SW-420**. Když je v klidu, je sepnutý a propojuje vstup 2 komparátoru **U1A** se zemí (**GND**).

Potenciometr **VR1** přivádí řídicí napětí (**Pin2**) na vstup **Pin3** komparátoru **U1A**

Obvod **U1A** je [komparátor](https://en.wikipedia.org/wiki/Comparator). Pro komparátory platí, že,

$$
V_{out} =
\begin{cases}
High,  & \mbox{if }V_+ > V_-  \\
Low,  & \mbox{if }V_+ < V_-
\end{cases}
$$

**V+** je připojeno na **Pin3**, **V-** je připojeno na **Pin2**, **V<sub>out</sub>** je připojeno na **Pin1**.

Hodnotu **V+** můžete nastavit potenciometrem, například na hodnotu $VCC/2$.

Hodnota **V-** závisí na stavu **SW1(SW-420)**:

- Pokud je modul v klidu, je **SW1** sepnutý, Pin2 obvodu **U1A** je tak spojen se zemí. Bude tedy platit, že:

$$
\left. \begin{array}{l}  & V- = 0V \\ & V+ = VCC/2 \end{array} \right\}  V_{out} = High
$$

- Jakmile se snímač začne otřásat nebo naklánět, rozpojí se **SW1** a napětí na **V-** bude vytaženo k **VCC** přes rezistor **R1**. Jakmile bude **V-** vyšší než VCC/2, tak komparátor zareaguje:

$$
\left. \begin{array}{l}  & V- > VCC/2 \\ & V+ = VCC/2 \end{array} \right\}  V_{out} = Low
$$

Nastavením **V+** můžete nastavit citlivost, jen pamatujte: čím nižší napětí na **V+**, tím vyšší citlivost.

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

| Seeeduino V4.2                                                                                                             | Base Shield                                                                                                                | Grove - Vibration Sensor                                                                                                     | Grove - Buzzer                                                                           |
| -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg) | ![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Vibration_Sensor-SW-420/raw/master/img/thumbnail.jpg) | ![](https://github.com/SeeedDocument/Grove_Buzzer/raw/master/img/buzzer_s.jpg)           |
| <a href="http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html" target="_blank">Koupit</a>                                 | <a href="https://www.seeedstudio.com/Base-Shield-V2-p-1378.html" target="_blank">Koupit</a>                                | <a href="https://www.seeedstudio.com/Grove-Vibration-Sensor-%28SW-420%29-p-3158.html" target="_blank">Koupit</a>             | <a href="https://www.seeedstudio.com/Grove-Buzzer-p-768.html" target="_blank">Koupit</a> |

!!!Poznámka
**1** Buďte opatrní při připojování USB kabelu, můžete poškodit konektor. Používejte datové kabely (se čtyřmi vodiči), ne napájecí (se dvěma vodiči). Pokud si nejste jisti, jaký USB kabel máte, můžete si [u nás koupit doporučený](https://www.seeedstudio.com/Micro-USB-Cable-48cm-p-1475.html)

**2** Všechny Grove moduly jsou prodávány s propojovacím kabelem Grove. Pokud jej ztratíte, můžete si [u nás koupit náhradní Grove kabel](https://www.seeedstudio.com/Grove-Universal-4-Pin-Buckled-20cm-Cable-%285-PCs-pack%29-p-936.html).

- **Krok 1.** Připojte Grove - Vibration Sensor (SW-420) to the **D2** port of the Base Shield.

- **Krok 2.** Připojte Grove - Buzzer to the **D3** port of the Base Shield.

- **Krok 3.** Připojte Base Shield k Seeeduinu.

- **Krok 4.** Připojte Seeduino k PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-Vibration_Sensor-SW-420/raw/master/img/connect.JPG)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit Grove Button k
Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino   | Grove - Vibration Sensor |
| ----------- | ------------------------ |
| 5V          | Červený                  |
| GND         | Černý                    |
| Nepřipojeno | Bílý                     |
| D2          | Žlutý                    |

| Seeeduino   | Grove - Buzzer |
| ----------- | -------------- |
| 5V          | Červený        |
| GND         | Černý          |
| Nepřipojeno | Bílý           |
| D3          | Žlutý          |

#### Software

!!!Poznámka
Pokud se s Arduinem setkáváte poprvé, doporučujeme vám pročíst návod [Začínáme s Arduinem](http://wiki.seeedstudio.com/_with_Arduino/) dřív, než začnete.

- **Krok 1.** Spusťte Arduino IDE a otevřte nový projekt.

- **Krok 2.** Můžete kliknout na ikonu ![](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/copy.jpg) v pravém horním rohu výpisu programu a zkopírovat následující kód do nového sketche v Arduinu IDE.

```C++
// constants won't change. They're used here to set pin numbers:
const int buttonPin = 2;     // the number of the pushbutton pin
const int buzzer =  3;      // the number of the buzzer pin

// variables will change:
int buttonState = 0;         // variable for reading the pushbutton status

void setup() {
  // initialize the LED pin as an output:
  pinMode(buzzer, OUTPUT);
  // initialize the pushbutton pin as an input:
  pinMode(buttonPin, INPUT);
}

void loop() {
  // read the state of the pushbutton value:
  buttonState = digitalRead(buttonPin);

  // check if the pushbutton is pressed. If it is, the buttonState is HIGH:
  if (buttonState == HIGH) {
    // turn LED on:
    digitalWrite(buzzer, LOW);
  } else {
    // turn LED off:
    digitalWrite(buzzer, HIGH);
  }
}
```

- **Krok 3.** Nahrajte přeložený kód do Arduina. Pokud si nejste jisti, jak nahrát kód, podívejte se na stránku [Jak nahrát kód](http://wiki.seeedstudio.com/Upload_Code/).

!!!Povedlo se
Pokud vše proběhlo jak má, bzučák se spustí pokaždé, když snímačem zatřesete nebo pohnete.

### Pokusy s Codecraftem

#### Hardware

**Krok 1.** Připojte Grove - Vibration Sensor k portu D2 a Grove - Buzzer k portu D3 na Grove-Base Shieldu

**Krok 2.** Připojte Base Shield k Seeeduinu / Arduinu.

**Krok 3.** Propojte Seeeduino/Arduino s PC pomocí kabelu USB.

#### Software

**Krok 1.** Spusťte [Codecraft](https://ide.chmakered.com/), přepněte se na prostředí pro Arduino a přidejte na plochu hlavní proceduru (Start).

!!!Poznámka
Pokud používáte Codecraft poprvé, podívejte se na [Průvodce světem Codecraftu a Arduina](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Krok 2.** Přetáhněte bloky tak, jak ukazuje následující obrázek, nebo otevřte cdc soubor, který si můžete stáhnout na konci této stránky.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove-Vibration_Sensor-SW-420/master/img/cc_Vibration_Sensor.png)

Nahrajte hotový program do svého Arduina/Seeeduina.

!!!Povedlo se
Jakmile je nahrávání hotové, bzučák oznámí, že se senzor pohnul nebo zaznamenal otřes.

## Zdroje

- **[Zip]** [Grove - Vibration Sensor (SW-420) eagle files](<https://github.com/SeeedDocument/Grove-Vibration_Sensor-SW-420/raw/master/res/Grove%20-%20Vibration%20Sensor%20(SW-420)%20v1.1.zip>)
- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove-Vibration_Sensor-SW-420/master/res/Grove_Vibration_Sensor_CDC_File.zip)

## Projekt

Podívejte se na ukázkové video tohoto produktu a na jednoduché příkaldy, které si můžete vyzkoušet.

<iframe width="560" height="315" src="https://www.youtube.com/embed/oFmvKxoZIuw?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/)..<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
