---
title: Upravte jas obrázku pomocí Aspose.PSD pro Java
linktitle: Upravte jas obrázku
second_title: Aspose.PSD Java API
description: Vylepšete jas obrazu v Javě pomocí Aspose.PSD. Podrobný průvodce programovým nastavením jasu obrazu.
type: docs
weight: 21
url: /cs/java/advanced-techniques/adjust-brightness/
---
## Zavedení

Vylepšení obrázků je běžným požadavkem v grafickém designu a digitální fotografii. Aspose.PSD for Java poskytuje výkonné řešení pro programovou úpravu jasu obrazu. V tomto tutoriálu krok za krokem prozkoumáme, jak využít knihovnu Aspose.PSD for Java k úpravě jasu obrázku.

## Předpoklady

Než se ponoříte do výukového programu, ujistěte se, že máte následující předpoklady:

-  Aspose.PSD for Java Library: Stáhněte a nainstalujte knihovnu z[Aspose.PSD pro dokumentaci Java](https://reference.aspose.com/psd/java/).

## Importujte balíčky

Chcete-li začít, importujte potřebné balíčky do svého projektu Java. V tomto příkladu použijeme následující:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Nyní si rozeberme proces úpravy jasu obrázku do jednoduchých kroků:

## Krok 1: Načtěte obrázek

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Načtěte existující obrázek do instance třídy RasterImage
Image image = Image.load(sourceFile);
// Odeslání objektu obrázku do rastrového obrázku
RasterImage rasterImage = (RasterImage) image;

// Zkontrolujte, zda je RasterImage uložen v mezipaměti a pro lepší výkon uložte RasterImage do mezipaměti
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 V tomto kroku načteme cílový obrázek a přeneseme jej do a`RasterImage` pro další zpracování.

## Krok 2: Upravte jas

```java
// Upravte jas
rasterImage.adjustBrightness(-50);
```

 Zde používáme`adjustBrightness`způsob úpravy jasu obrazu. V tomto příkladu snížíme jas o 50 jednotek, ale tuto hodnotu můžete upravit podle svých požadavků.

## Krok 3: Nastavte TiffOptions

```java
int[] ushort = {8, 8, 8};
// Vytvořte instanci TiffOptions pro výsledný obrázek
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

 Nakonfigurujte`TiffOptions` pro uložení upraveného snímku. Upravte`bitsPerSample` a`photometric` vlastnosti na základě vašich konkrétních potřeb.

## Krok 4: Uložte výsledný obrázek

```java
// Uložte výsledný obrázek
rasterImage.save(destName, tiffOptions);
```

 Nakonec upravený obrázek uložte pomocí zadaného`TiffOptions`.

## Závěr

Programové nastavení jasu obrazu je s Aspose.PSD pro Java snadné. Tento výukový program poskytuje komplexního průvodce implementací této funkce ve vašich aplikacích Java.

## FAQ

### Q1: Mohu upravit jas v jiných formátech obrázků kromě PSD?

Odpověď 1: Ano, Aspose.PSD for Java podporuje různé formáty obrázků, jako jsou JPEG, PNG a TIFF.

### Q2: Jak mohu řešit chyby během procesu úpravy obrazu?

A2: Zpracování chyb můžete implementovat pomocí bloků try-catch ke správě výjimek, které mohou nastat.

### Q3: Existuje omezení rozsahu nastavení jasu?

Odpověď 3: Rozsah úprav závisí na obsahu a formátu obrázku, ale Aspose.PSD poskytuje flexibilitu v přizpůsobení.

### Q4: Mohu použít Aspose.PSD pro Java v komerčních projektech?

 A4: Ano, Aspose.PSD for Java je komerční knihovna a můžete získat licenci od[zde](https://purchase.aspose.com/buy).

### Q5: Je k dispozici bezplatná zkušební verze pro Aspose.PSD pro Java?

 A5: Ano, můžete prozkoumat knihovnu pomocí bezplatné zkušební verze od[zde](https://releases.aspose.com/).