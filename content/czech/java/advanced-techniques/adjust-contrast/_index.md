---
title: Upravte kontrast obrázku pomocí Aspose.PSD pro Javu
linktitle: Upravte kontrast obrázku
second_title: Aspose.PSD Java API
description: Prozkoumejte svět úpravy kontrastu obrazu v Javě s Aspose.PSD. Postupujte podle našeho podrobného průvodce pro bezproblémovou manipulaci s obrázky.
type: docs
weight: 22
url: /cs/java/advanced-techniques/adjust-contrast/
---
## Úvod

oblasti zpracování obrazu pomocí Javy vyniká Aspose.PSD jako mocný nástroj. Mezi jeho nesčetnými funkcemi je běžným požadavkem úprava kontrastu obrazu. Tento tutoriál vás provede procesem úpravy kontrastu obrazu pomocí Aspose.PSD pro Java. Ať už jste zkušený vývojář nebo teprve začínáte, tato příručka vám pomůže zvládnout tento základní aspekt manipulace s obrázky.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

- Základní znalost programování v Javě.
-  Nainstalovaná knihovna Aspose.PSD for Java. Můžete si jej stáhnout[tady](https://releases.aspose.com/psd/java/).

## Importujte balíčky

Chcete-li začít, musíte do svého projektu Java importovat potřebné balíčky. Přidejte do kódu následující řádky:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Krok 1: Načtěte obrázek

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Načtěte existující obrázek do instance třídy RasterImage
Image image = Image.load(sourceFile);
```

 V tomto kroku načteme ukázkový obrázek ("sample.psd") pomocí`Image.load` metoda.

## Krok 2: Odeslání na rastrový obrázek a data do mezipaměti

```java
// Odeslání objektu obrázku do rastrového obrázku
RasterImage rasterImage = (RasterImage)image;

// Zkontrolujte, zda je RasterImage uložen v mezipaměti a pro lepší výkon uložte RasterImage do mezipaměti
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Zde jsme obsadili generikum`Image` namítat proti a`RasterImage` pro konkrétní zpracování. Ukládání obrazových dat do mezipaměti zlepšuje výkon.

## Krok 3: Upravte kontrast

```java
// Upravte kontrast
rasterImage.adjustContrast(50);
```

 The`adjustContrast`metoda se používá k úpravě kontrastu obrazu. V tomto příkladu se kontrast zvýší o 50 %.

## Krok 4: Vytvořte TiffOptions a uložte

```java
// Vytvořte instanci TiffOptions pro výsledný obrázek
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Uložte výsledný obrázek do formátu TIFF
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

 Tady jsme se postavili`TiffOptions` pro výstupní obraz s uvedením formátu a dalších vlastností. Konečný obrázek je poté uložen do souboru TIFF.

## Závěr

Gratulujeme! Úspěšně jste upravili kontrast obrázku pomocí Aspose.PSD pro Java. Tento tutoriál se zabýval základními kroky, od importu balíčků po uložení zpracovaného obrázku.

## FAQ

### Q1: Je Aspose.PSD kompatibilní s různými formáty obrázků?

Odpověď 1: Ano, Aspose.PSD podporuje různé formáty obrázků a poskytuje flexibilitu ve vašich projektech.

### Q2: Jak mohu získat dočasnou licenci pro Aspose.PSD?

 A2: Můžete získat dočasnou licenci.[tady](https://purchase.aspose.com/temporary-license/).

### Q3: Kde najdu dokumentaci Aspose.PSD?

A3: Dokumentace je k dispozici.[tady](https://reference.aspose.com/psd/java/).

### Q4: Jaké možnosti podpory jsou k dispozici pro Aspose.PSD?

 A4: Pro podporu navštivte[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q5: Mohu si zakoupit Aspose.PSD?

 A5: Ano, můžete si koupit Aspose.PSD[tady](https://purchase.aspose.com/buy).