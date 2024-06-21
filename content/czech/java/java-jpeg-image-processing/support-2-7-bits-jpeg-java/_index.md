---
title: Podpora 2 a 7 bitů JPEG v Javě
linktitle: Podpora 2 a 7 bitů JPEG v Javě
second_title: Aspose.PSD Java API
description: Naučte se manipulovat se soubory PSD a ukládat je jako JPEG v Javě pomocí Aspose.PSD. Podrobný průvodce s příklady kódu. Ideální pro začátečníky i profíky.
type: docs
weight: 20
url: /cs/java/java-jpeg-image-processing/support-2-7-bits-jpeg-java/
---
## Úvod
Nazdárek! Jste připraveni ponořit se do světa zpracování obrazu pomocí Javy? Dnes prozkoumáme knihovnu Aspose.PSD for Java, výkonný nástroj, který vám umožňuje snadno manipulovat a transformovat soubory PSD. Konkrétně se podíváme na to, jak zacházet s 2 a 7 bitovými JPEGy. Tento tutoriál vás provede vším, co potřebujete vědět, od předpokladů až po podrobné pokyny krok za krokem. Takže se připoutejte a připravte se na zábavnou a poučnou jízdu!
## Předpoklady
Než začneme, ujistěte se, že máte vše, co potřebujete:
1. Java Development Kit (JDK): Ujistěte se, že máte nainstalovaný JDK 8 nebo vyšší.
2.  Aspose.PSD for Java Library: Můžete[stáhněte si jej zde](https://releases.aspose.com/psd/java/).
3. Integrované vývojové prostředí (IDE): Postačí jakékoli IDE kompatibilní s Java, jako je IntelliJ IDEA, Eclipse nebo NetBeans.
4. Ukázkový soubor PSD: Pro tento výukový program budete potřebovat ukázkový soubor PSD. Můžete použít svůj vlastní nebo najít online.
5. Základní znalost jazyka Java: Bude užitečné porozumět základní syntaxi Java a konceptům objektově orientovaného programování.
Dobře, ušpiníme si ruce!
## Importujte balíčky
Nejprve naimportujme potřebné balíčky. Abyste mohli začít, budete potřebovat knihovnu Aspose.PSD for Java. Ujistěte se, že jste knihovnu přidali do závislostí projektu. Jak na to:
```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.jpeg.JpegCompressionColorMode;
import com.aspose.psd.fileformats.jpeg.JpegCompressionMode;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
```
## Krok 1: Načtěte obrázek PSD
Prvním krokem na naší cestě je načtení obrázku PSD. Tady budeme pracovat se svou magií. Pojďme napsat kód pro načtení obrázku PSD:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "PsdImage.psd");
```
 V tomto kroku určujeme adresář, kde je umístěn náš soubor PSD, a načítáme soubor do a`PsdImage` objekt. Snadné, že?
## Krok 2: Nastavte možnosti JPEG
Nyní, když máme načtený náš obrázek, dalším krokem je nastavení možností JPEG. Zde definujeme, jak chceme uložit náš obrázek, včetně barevného režimu a typu komprese. Pojďme nakonfigurovat možnosti:
```java
JpegOptions options = new JpegOptions();
options.setColorType(JpegCompressionColorMode.Cmyk);
options.setCompressionType(JpegCompressionMode.JpegLs);
```
 Zde nastavujeme typ barvy na CMYK a typ komprese na JPEG LS. Tato nastavení můžete změnit podle svých potřeb. Chcete-li například použít YCCK místo CMYK, nahradili byste`JpegCompressionColorMode.Cmyk` s`JpegCompressionColorMode.Ycck`.
## Krok 3: Upravte počet bitů na kanál
Dále upravíme bity na kanál. Toto nastavení ovlivňuje kvalitu a velikost obrazu. Začneme se 2 bity na kanál:
```java
byte bpp = 2;
options.setBitsPerChannel(bpp);
```
 Nastavení`bpp` na 2 nám poskytuje obraz nižší kvality s menší velikostí souboru. S touto hodnotou můžete experimentovat a zjistit, jak ovlivní váš obrázek.
## Krok 4: Nastavte barevné profily
V tomto kroku nastavíme barevné profily. Pro jednoduchost použijeme výchozí profily:
```java
options.setRgbColorProfile(null);
options.setCmykColorProfile(null);
```
 Ponechání profilů jako`null`znamená, že budou použity výchozí profily. Pokud máte konkrétní barevné profily, které chcete použít, můžete je nastavit zde.
## Krok 5: Uložte obrázek
Nakonec uložíme obrázek s naším novým nastavením. Toto je okamžik pravdy! Zde je kód pro uložení obrázku:
```java
image.save(dataDir + "2_7BitsJPEG_output.jpg", options);
```
A to je vše! Úspěšně jste zpracovali obrázek PSD a uložili jej jako JPEG se zadanými nastaveními.
## Závěr
Gratulujeme! Právě jste se naučili, jak manipulovat se soubory PSD a ukládat je jako JPEG pomocí Aspose.PSD for Java. Tato výkonná knihovna nabízí širokou škálu funkcí, díky kterým je zpracování obrazu hračkou. Ať už pracujete na malém projektu nebo na rozsáhlé aplikaci, Aspose.PSD pro Java vám pomůže. Tak na co čekáš? Začněte experimentovat a uvidíte, jaké úžasné věci můžete vytvořit!
## FAQ
### Co je Aspose.PSD for Java?
Aspose.PSD for Java je výkonná knihovna, která vám umožňuje pracovat se soubory PSD v aplikacích Java. Nabízí širokou škálu funkcí pro manipulaci a transformaci obrazu.
### Jak nainstaluji Aspose.PSD pro Javu?
 Knihovnu si můžete stáhnout z[webová stránka](https://releases.aspose.com/psd/java/) a přidejte jej do závislostí projektu.
### Mohu používat vlastní barevné profily s Aspose.PSD pro Javu?
Ano, při konfiguraci možností JPEG můžete nastavit vlastní profily barev RGB a CMYK.
### Jaké jsou podporované formáty obrázků v Aspose.PSD pro Javu?
Aspose.PSD for Java podporuje různé formáty obrázků, včetně PSD, JPEG, PNG, BMP, TIFF a dalších.
### Je k dispozici bezplatná zkušební verze Aspose.PSD pro Javu?
 Ano, můžete si stáhnout a[zkušební verze zdarma](https://releases.aspose.com/) k otestování funkcí knihovny před nákupem.