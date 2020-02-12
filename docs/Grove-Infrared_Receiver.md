---
name: Grove - Infrared Receiver
category: Sensor
bzurl: https://seeedstudio.com/Grove-Infrared-Receiver-p-994.html
oldwikiname: Grove_-_Infrared_Receiver
prodimagename: Grove-Infrared_Receiver.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/101020016 1.jpg
surveyurl: https://www.research.net/r/Grove-Infrared_Receiver
sku: 101020016
tags: grove_digital, io_3v3, io_5v, plat_duino
---

![](https://github.com/SeeedDocument/Grove-Infrared_Receiver/raw/master/img/Grove-Infrared_Receiver.jpg)

Infračervený přijímač (Infrared Receiver) se používá k přijímání infračerveného světla, například z dálkového ovládání. Snímací prvek (IR detektor) je citlivý na infračervené světlo, vysílané Infračerveným vysílačem (Infrared Emitter). Detektor má zabudovaný demodulátor, který demoduluje signál, vysílaný na používané frekvenci 38 kHz. Přijímač má dosah až 10 metrů, na větší vzdálenost není přenos zajištěn. Často se používá v páru s modulem vysílače [Grove - Infrared Emitter](http://wiki.seeedstudio.com/Grove-Infrared_Emitter).

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](http://www.seeedstudio.com/Grove-Infrared-Receiver-p-994.html)

## Verze

| Verze produktu                 | Změny              | Datum vydání |
| ------------------------------ | ------------------ | ------------ |
| Grove - Infrared Receiver v1.0 | První vydání       | Nov. 01 2015 |
| Grove - Infrared Receiver v1.1 | Změna popisu desky | Jul. 24 2016 |

## Specifikace

- Napětí: 3.3-5V
- Vzdálenost: 10m

!!!Tip
Více detailů o modulech Grove zjistíte v [popisu systému Grove](http://wiki.seeedstudio.com/Grove_System/)

## Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                                 | BeagleBone                                                                                          | Wio                                                                                               | LinkIt ONE                                                                                             |
| ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Začínáme

Grove - Infrared Emitter vysílá data a Grove - Infrared Receiver je opět přijímá.

### Pokusy s Arduinem

!!!Poznámka
Pokud se s Arduinem setkáváte poprvé, doporučujeme vám pročíst návod [Začínáme s Arduinem](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) dřív, než začnete.

#### Hardware

- **Krok 1.** Připravte si tyto součástky:

| Seeeduino V4.2                                                                                                        | Base Shield                                                                                                            | Grove - Infrared Emitter                                                                                              | Grove - Infrared Receiver                                                                                           |
| --------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduinoX2.png) | ![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/baseshiledX2.png) | ![enter image description here](https://github.com/SeeedDocument/Grove-Infrared_Emitter/raw/master/img/thumbnail.jpg) | ![enter image description here](https://github.com/SeeedDocument/Grove-Infrared_Receiver/raw/master/img/little.jpg) |
| [Koupit](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)                                                       | [Koupit](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)                                                       | [Koupit](https://www.seeedstudio.com/Grove-Infrared-Emitter-p-993.html)                                               | [Koupit](https://www.seeedstudio.com/Grove-Infrared-Receiver-p-994.html)                                            |

- **Krok 2.** Připojte Grove - Infrared Emitter k portu **D3** na jednom Grove-Base Shieldu.
- **Krok 3.** Připojte Grove - Infrared Receiver k portu **D2** na druhém Grove-Base Shieldu.

- **Krok 4.** Připojte Base Shield k Seeeduinu.

- **Krok 5.** Připojte Seeduino k PC pomocí kabelu USB.

![](https://github.com/SeeedDocument/Grove-Infrared_Emitter/raw/master/img/connect.jpg)

!!!Poznámka
Pokud nemáte Grove Base Shield, můžete připojit this module k Seeduinu tak, jak je popsáno v následující tabulce:

| Seeeduino   | Grove - Infrared Emitter |
| ----------- | ------------------------ |
| 5V          | Červený                  |
| GND         | Černý                    |
| Nepřipojeno | Bílý                     |
| D3          | Žlutý                    |

| Seeeduino   | Grove - Infrared Receiver |
| ----------- | ------------------------- |
| 5V          | Červený                   |
| GND         | Černý                     |
| Nepřipojeno | Bílý                      |
| D2          | Žlutý                     |

#### Software

- **Krok 1.** Stáhněte si knihovnu [IRSendRev-master library](https://github.com/Seeed-Studio/IRSendRev) z GitHubu.

- **Krok 2.** S instalací knihovny pro Arduino vám pomůže návod [Jak instalovat knihovnu pro Arduino](http://wiki.seeedstudio.com/How_to_install_Arduino_Library).

- **Krok 3.** Restartujte Arduino IDE. Otevřte soubor `recv` následujícím postupem: **File->Examples->Grove - Infrared Receiver And Emitter->recv**.

![](https://github.com/SeeedDocument/Grove-Infrared_Receiver/raw/master/img/path.png)

Můžete také otevřít nový projekt v Arduino IDE a zkopírovat do něj níže uvedený kód.

```c++

#include <IRSendRev.h>

#define BIT_LEN         0
#define BIT_START_H     1
#define BIT_START_L     2
#define BIT_DATA_H      3
#define BIT_DATA_L      4
#define BIT_DATA_LEN    5
#define BIT_DATA        6

const int pinRecv = 2;              // ir receiver connect to D2

void setup()
{
    Serial.begin(115200);
    IR.Init(pinRecv);
    Serial.println("init over");
}

unsigned char dta[20];

void loop()
{
    if(IR.IsDta())                  // get IR data
    {
        IR.Recv(dta);               // receive data to dta

        Serial.println("+------------------------------------------------------+");
		Serial.print("LEN = ");
        Serial.println(dta[BIT_LEN]);
        Serial.print("START_H: ");
        Serial.print(dta[BIT_START_H]);
        Serial.print("\tSTART_L: ");
        Serial.println(dta[BIT_START_L]);

        Serial.print("DATA_H: ");
        Serial.print(dta[BIT_DATA_H]);
        Serial.print("\tDATA_L: ");
        Serial.println(dta[BIT_DATA_L]);

        Serial.print("\r\nDATA_LEN = ");
        Serial.println(dta[BIT_DATA_LEN]);

		Serial.print("DATA: ");
        for(int i=0; i<dta[BIT_DATA_LEN]; i++)
        {
            Serial.print("0x");
            Serial.print(dta[i+BIT_DATA], HEX);
            Serial.print("\t");
        }
        Serial.println();

		Serial.print("DATA: ");
        for(int i=0; i<dta[BIT_DATA_LEN]; i++)
        {
            Serial.print(dta[i+BIT_DATA], DEC);
            Serial.print("\t");
        }
        Serial.println();
        Serial.println("+------------------------------------------------------+\r\n\r\n");
    }
}

```

- **Krok 4.** Nahrajte kód `recv` do Seeeduina, k němuž je připojen Grove - Infrared Receiver. Pokud si nejste jisti, jak nahrát kód, podívejte se na stránku [Jak nahrát kód](http://wiki.seeedstudio.com/Upload_Code/).

- **Krok 5.** Otevřte soubor `send` následujícím postupem: **File->Examples->Grove - Infrared Receiver And Emitter->send**.

Můžete také otevřít nový projekt v Arduino IDE a zkopírovat do něj níže uvedený kód.

```
#include <IRSendRev.h>

#define BIT_LEN         0
#define BIT_START_H     1
#define BIT_START_L     2
#define BIT_DATA_H      3
#define BIT_DATA_L      4
#define BIT_DATA_LEN    5
#define BIT_DATA        6

const int ir_freq = 38;                 // 38k

unsigned char dtaSend[20];

void dtaInit()
{
    dtaSend[BIT_LEN]        = 11;			// all data that needs to be sent
    dtaSend[BIT_START_H]    = 179;			// the logic high duration of "Start"
    dtaSend[BIT_START_L]    = 90;			// the logic low duration of "Start"
    dtaSend[BIT_DATA_H]     = 11;			// the logic "long" duration in the communication
    dtaSend[BIT_DATA_L]     = 33;			// the logic "short" duration in the communication

    dtaSend[BIT_DATA_LEN]   = 6;			// Number of data which will sent. If the number is other, you should increase or reduce dtaSend[BIT_DATA+x].

    dtaSend[BIT_DATA+0]     = 128;			// data that will sent
    dtaSend[BIT_DATA+1]     = 127;
    dtaSend[BIT_DATA+2]     = 192;
    dtaSend[BIT_DATA+3]     = 63;
	dtaSend[BIT_DATA+4]     = 192;
    dtaSend[BIT_DATA+5]     = 63;
}

void setup()
{
    dtaInit();
}

void loop()
{
    IR.Send(dtaSend, 38);

    delay(2000);
}


```

- **Krok 6.** Nahrajte kód `send` do Seeeduina, k němuž je připojen Grove - Infrared Emitter.

* **Krok 7.** Otevřete **Sériový Monitor** v Arduino IDE kliknutím na **Tool-> Serial Monitor**. Můžete použít klávesovou zkratku ++ctrl+shift+m++.

Pokud vše proběhlo jak má, uvidíte něco takového:

![](https://github.com/SeeedDocument/Grove-Infrared_Emitter/raw/master/img/results.png)

## Zdroje

- **[Zip]** [Grove - Infrared Receiver eagle files](https://raw.githubusercontent.com/SeeedDocument/Grove-Infrared_Receiver/master/res/Grove-Infrared_Receiver_eagle_files.zip)
- **[Lib]** [IR Send and Receiver Library](https://github.com/Seeed-Studio/IRSendRev)
- **[Lib]** [IR Receive Library for LinkIt ONE](https://github.com/Seeed-Studio/IR_Recv_LinkIt_ONE)
- **[Pdf]** [TSOP282 Datasheet](http://www.vishay.com/docs/82491/tsop382.pdf)

## Projekty

**Infračervená komunikace mezi LaunchPady**: Pomocí infračervených modulů Grove můžete vysílat text z jednoho LaunchPadu do druhého!

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/ctroberts/ir-launchpad-to-launchpad-communication-0dd109/embed' width='350'></iframe>

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
