---
title: Přidejte vodoznak do souborů PSD pomocí Aspose.PSD pro Java
linktitle: Přidejte vodoznak do souborů PSD pomocí Aspose.PSD pro Java
second_title: Aspose.PSD Java API
description: Naučte se, jak přidat vodoznak do souborů PSD bez námahy pomocí Aspose.PSD pro Java. Chraňte své snímky pomocí jednoduchého průvodce krok za krokem.
weight: 18
url: /cs/java/modifying-converting-psd-images/add-watermark-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidejte vodoznak do souborů PSD pomocí Aspose.PSD pro Java

## Zavedení
Vodoznaky jsou nenápadným, ale účinným způsobem, jak chránit obrázky a komunikovat vlastnictví. Ať už jste fotograf předvádějící své portfolio nebo designér prezentující svou nejnovější práci, přidání vodoznaku může být zásadní pro udržení identity vaší značky. V tomto tutoriálu se ponoříme do toho, jak bez námahy přidat vodoznaky do souborů PSD pomocí Aspose.PSD pro Java. Takže si dejte šálek kávy, udělejte si pohodlí a můžeme začít!
## Předpoklady
Než se ponoříte do kódu, je nezbytné se ujistit, že máte potřebné nástroje a balíčky pro úspěšnou implementaci vodoznaku do vašich souborů PSD. Zde je to, co potřebujete připravit:
1. Java Development Kit (JDK): Ujistěte se, že máte na svém počítači nainstalovaný JDK. Může být také nutné nakonfigurovat proměnnou PATH.
2. Aspose.PSD for Java Library: Toto je srdce naší vodoznakové aplikace. Knihovnu si musíte stáhnout z[Aspose webové stránky](https://releases.aspose.com/psd/java/).
3. IDE: Postačí jakékoli Java IDE podle vašeho výběru. Ať už je to Eclipse, IntelliJ IDEA nebo dokonce jednoduchý textový editor, můžete si vybrat.
4.  Soubor PSD: Mějte po ruce soubor PSD. Můžete si jej vytvořit nebo najít vzorek online. Budeme to označovat jako`layers.psd`.
5. Základní znalosti jazyka Java: Dobré porozumění základům jazyka Java vám pomůže postupovat dál.
## Importujte balíčky
Nyní, když jste vše nastavili, pojďme importovat potřebné balíčky. Importy v Javě vám umožňují přinášet třídy a funkce z různých knihoven, čímž je váš kód efektivnější. Níže je to, co budete potřebovat:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```
## Krok 1: Nastavte svůj adresář
Nejprve musíme nastavit cestu, kde se nachází váš soubor PSD. To je zásadní, protože Java potřebuje vědět, kde najde vaše soubory. 
```java
String dataDir = "Your Document Directory";
```
 Nahradit`Your Document Directory` s vaším skutečným adresářem, kde se nachází váš soubor PSD.
## Krok 2: Načtěte soubor PSD
 Dále načteme soubor PSD a přeneseme jej do a`PsdImage`Tento krok převede soubor do formátu, se kterým můžeme manipulovat.
```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```
 Co tento řádek dělá, je vzít váš stávající soubor PSD a načíst jej do paměti jako a`PsdImage`. Představte si to, jako byste otevřeli knihu, abyste do ní mohli začít psát.
## Krok 3: Vytvořte grafický objekt
 S načteným souborem PSD musíme vytvořit soubor a`Graphics` objekt. To nám umožňuje provádět operace kreslení, v podstatě jako získání štětce pro přidání barvy na vaše plátno.
```java
Graphics graphics = new Graphics(psdImage);
```
## Krok 4: Definujte písmo pro váš vodoznak
Nyní je čas vybrat si, jak bude váš vodoznak vypadat. Budeme používat Arial s velikostí písma 20. Zde můžete předvést svůj styl!
```java
Font font = new Font("Arial", 20.0f);
```
## Krok 5: Vytvořte pevný štětec pro vodoznaky
Pevný štětec je to, co dává vodoznaku jeho barvu a neprůhlednost. Chceme, aby byl nápadný, ale ne ohromující, takže nastavme jeho alfa blízkou 0 pro částečně průhledný vzhled.
```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```
 Zde,`Color.fromArgb(50, 128, 128, 128)` vytváří šedou barvu s 50% krytím. Je to jako mrak jemně stínící jinak zářivou oblohu.
## Krok 6: Nastavte zarovnání řetězců pro váš vodoznak
Abychom zajistili, že se vodoznak zobrazí přímo ve středu obrázku, nastavíme možnosti zarovnání řetězců. Tento krok je především o přesnosti!
```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
sf.setLineAlignment(StringAlignment.Center);
```
## Krok 7: Nakreslete vodoznak
Nyní se dostáváme k vzrušující části! S naším grafickým kontextem je čas nakreslit vodoznak do obrázku.
```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, 0, psdImage.getWidth(), psdImage.getHeight()), sf);
```
 Tady, vyměňte`"Some watermark text"` s požadovaným textem vodoznaku. Tento krok je jako namalovat svůj podpis na mistrovské dílo!
## Krok 8: Exportujte obrázek do formátu PNG
Nyní, když je naše kresba připravena, musíme ji uložit do nového formátu souboru, v tomto případě PNG. 
```java
psdImage.save(dataDir + "AddWatermark_output.png", new PngOptions());
```
Spuštěním tohoto řádku efektivně zvěčňujete svou práci v novém formátu a zachováte vodoznak pro svět!
## Závěr
tady to máte! Úspěšně jste přidali vodoznak do svého souboru PSD pomocí Aspose.PSD for Java. Tento proces nejen zabezpečuje váš obsah, ale také zvyšuje viditelnost vaší značky. Pamatujte, že kroky, které jste podnikli, jsou pouze výchozím bodem. Nebojte se být kreativní – experimentujte s různými fonty, styly a barvami! Chraňte svou práci a prezentujte svou značku s hrdostí. 
## FAQ
### Mohu upravit text vodoznaku?
 Absolutně! Stačí nahradit text v`drawString` metodou s požadovaným vodoznakem.
### Co když chci jiný font?
 Písmo můžete snadno změnit výběrem jiného v`Font` konkretizace.
### Existuje způsob, jak upravit neprůhlednost?
 Ano! Změňte hodnotu alfa v`Color.fromArgb()` změnit neprůhlednost vodoznaku.
### Mohu použít jiné formáty obrázků?
 Ano, můžete ukládat v různých formátech, jako je JPEG nebo BMP. Stačí vyměnit`PngOptions()` s požadovanými možnostmi.
### Kde najdu další pomoc?
 Pro podrobné dotazy můžete navštívit[Aspose fóra](https://forum.aspose.com/c/psd/34) nebo zkontrolovat jejich[dokumentace](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
