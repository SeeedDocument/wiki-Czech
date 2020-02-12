---
name: Grove - Speaker
category: Actuator
bzurl: https://seeedstudio.com/Grove-Speaker-p-1445.html
oldwikiname: Grove_-_Speaker
prodimagename: Grove_Speaker_01.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/product/Grove Speaker.jpg
surveyurl: https://www.research.net/r/Grove-Speaker
sku: 107020001
tags: grove_digital, io_5v, plat_duino, plat_wio
---

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Speaker/master/img/Grove_Speaker_01.jpg)

Grove-Speaker je modul zvukového výstupu a zesilovače. Hlasitost si můžete upravit pomocí potenciometru, který je součástí modulu. Různé tóny získáte tím, že do modulu budete posílat různé frekvence signálu. Stačí připojit Arduino a snadno si vyrobit vlastní hudební nástroj!

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](http://www.seeedstudio.com/Grove-Speaker-p-1445.html)

## Vlastnosti

- Nastavitelná hlasitost
- Rozhraní Grove

!!!Tip
Více detailů o modulech Grove zjistíte v [popisu systému Grove](http://wiki.seeedstudio.com/Grove_System/)

## Specifikace

| Parametr          | Min | Typicky | Max | Jednotka |
| ----------------- | --- | ------- | --- | -------- |
| Napájecí napětí   | 4.0 | 5.0     | 5.5 | VDC      |
| Napěťové zesílení | -   | -       | 46  | db       |
| Šířka pásma       | -   | -       | 20  | KHz      |

## Podporované platformy

| Arduino                                                                                               | Raspberry Pi                                                                                                 | BeagleBone                                                                                          | Wio                                                                                               | LinkIt ONE                                                                                             |
| ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Pozor
Formulace "podporované platformy" je použita ve smyslu informace, že tato dvě zařízení jsou vzájemně propojitelná a mohou spolu pracovat. My poskytujeme ve většině případů pouze knihovny nebo příklady kódu pro platformu Arduino. Nemůžeme poskytovat ukázky a knihovny pro všechny možné mikrokontroléry a platformy. Uživatelé si pro takové případy musí napsat vlastní software.

## Začínáme

### Pokusy s Arduinem

Reproduktor dokáže vyluzovat nejrůznější zvuky, podobné například klaksonu auta, dveřnímu zvonku nebo houkačce. Různé zvukové efekty vytvoříte pomocí různých změn frekvence vstupního signálu.

Různé frekvence můžete vytvořit například Arduinem. Arduino generuje signál pomocí PWM nebo přímým zapisováním digitální úrovně a čekáním. Ukážeme si, jak vytvořit takový signál pomocí _delay()_, reproduktor bude přehrávat různé basové tóny.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Speaker/master/img/Tone.jpg)

```
/* na jakém pinu je připojený reproduktor? */
#define SPEAKER 3

int BassTab[]={1911,1702,1516,1431,1275,1136,1012};//tóny 1~7

void setup()
{
    pinInit();
}
void loop()
{
        /* přehrajeme tóny 1~7*/
    for(int note_index=0;note_index<7;note_index++)
    {
        sound(note_index);
        delay(500);
    }
}
void pinInit()
{
    pinMode(SPEAKER,OUTPUT);
    digitalWrite(SPEAKER,LOW);
}
void sound(uint8_t note_index)
{
    for(int i=0;i<100;i++)
    {
        digitalWrite(SPEAKER,HIGH);
        delayMicroseconds(BassTab[note_index]);
        digitalWrite(SPEAKER,LOW);
        delayMicroseconds(BassTab[note_index]);
    }
}
```

<div class="admonition note">
<p class="admonition-title">Poznámka</p>
Vlivem kapacity není možné tímto modulem generovat vysoké tóny, pouze hluboké.
</div>

### Pokusy s Codecraftem

#### Hardware

**Krok 1.** Připojte Grove - Speaker k portu D3 na Grove-Base Shieldu

**Krok 2.** Připojte Base Shield k Seeeduinu / Arduinu.

**Krok 3.** Propojte Seeeduino/Arduino s PC pomocí kabelu USB.

#### Software

**Krok 1.** Spusťte [Codecraft](https://ide.chmakered.com/), přepněte se na prostředí pro Arduino a přidejte na plochu hlavní proceduru (Start).

!!!Poznámka
Pokud používáte Codecraft poprvé, podívejte se na [Průvodce světem Codecraftu a Arduina](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Krok 2.** Přetáhněte bloky tak, jak ukazuje následující obrázek, nebo otevřte cdc soubor, který si můžete stáhnout na konci této stránky.

![](https://github.com/SeeedDocument/Grove-Speaker/raw/master/img/Speaker.png)

Nahrajte hotový program do svého Arduina/Seeeduina.

!!!Povedlo se
Jakmile je nahrávání hotové, uslyšíte, jak reproduktor přehrává stupnici.

## Zdroje

---

- [Grove - Speaker Eagle File](https://raw.githubusercontent.com/SeeedDocument/Grove-Speaker/master/res/Grove-Speaker_Eagle_File.zip)
- [How to generate different tone with MCU](https://raw.githubusercontent.com/SeeedDocument/Grove-Speaker/master/res/Tone.pdf)
- [Grove\_-_Speaker_v1.0_brd.pdf](https://raw.githubusercontent.com/SeeedDocument/Grove-Speaker/master/res/Grove-Speaker_v1.0_brd.pdf)
- [Grove\_-_Speaker_v1.0_sch.pdf](https://raw.githubusercontent.com/SeeedDocument/Grove-Speaker/master/res/Grove-Speaker_v1.0_sch.pdf)
- [LM386 Low Napětí Audio Power Amplifier Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Speaker/master/res/LM386_Low_Napětí_Audio_Power_Amplifier_Datasheet.pdf)
- [CodeCraft Code](https://github.com/SeeedDocument/Grove-Speaker/raw/master/res/Speaker.zip)

<!-- This Markdown file was created from http://www.seeedstudio.com/wiki/Grove_-_Speaker -->

## Technická podpora

Hlašte prosím jakékoli technické problémy na našem [fóru](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>
