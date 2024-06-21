---
title: Rozostření obrázku pomocí Aspose.PSD pro Javu
linktitle: Rozostření obrázku
second_title: Aspose.PSD Java API
description: Naučte se rozmazávat obrázky v Javě pomocí Aspose.PSD. Postupujte podle našeho podrobného průvodce pro profesionální výsledky.
type: docs
weight: 24
url: /cs/java/advanced-techniques/blur-image/
---
## Úvod

Ve světě vývoje v Javě je vylepšování a manipulace s obrázky běžným požadavkem. Pokud chcete do svých obrázků přidat efekt rozostření programově, Aspose.PSD for Java je mocný nástroj, který celý proces zjednodušuje. Tento výukový program vás provede kroky rozmazání obrázku pomocí Aspose.PSD a zajistí, že bez námahy dosáhnete profesionálních výsledků.

## Předpoklady

Než se pustíte do výukového programu, ujistěte se, že máte splněny následující předpoklady:

- Java Development Kit (JDK) nainstalovaný ve vašem systému.
-  Aspose.PSD pro knihovnu Java. Můžete si jej stáhnout[tady](https://releases.aspose.com/psd/java/).
- Základní znalost programování v Javě.

## Importujte balíčky

Začněte importováním potřebných balíčků do vašeho projektu Java. Patří mezi ně třídy Aspose.PSD pro zpracování obrazu.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussianBlurFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

Nyní si rozdělme proces rozmazání obrázku do několika kroků.

## Krok 1: Definujte cesty k souboru

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "BlurAnImage_out.gif";
```

## Krok 2: Načtěte obrázek

```java
// Načtěte existující obrázek do instance třídy RasterImage
Image image = Image.load(sourceFile);
```

## Krok 3: Převeďte na rastrový obrázek

```java
// Převeďte obrázek na rastrový obrázek
RasterImage rasterImage = (RasterImage)image;
```

## Krok 4: Použijte filtr rozostření

```java
//Předat Bounds[rectangle] obrázku a instance GaussianBlurFilterOptions do metody Filter
rasterImage.filter(rasterImage.getBounds(), new GaussianBlurFilterOptions(15, 15));
```

## Krok 5: Uložte výsledek

```java
// Uložte výsledky ve formátu GIF
rasterImage.save(destName, new GifOptions());
```

Pomocí těchto kroků jste úspěšně aplikovali efekt rozostření na váš obrázek pomocí Aspose.PSD for Java.

## Závěr

Aspose.PSD for Java zjednodušuje úlohy zpracování obrazu a usnadňuje vývojářům dosahovat profesionálních výsledků. Programové rozmazání obrázků je jen jedním příkladem výkonných funkcí, které tato knihovna poskytuje.

## FAQ

### Q1: Je Aspose.PSD for Java vhodný pro začínající vývojáře?

A1: Rozhodně! Aspose.PSD přichází s komplexní dokumentací, která má vést vývojáře všech úrovní dovedností.

### Q2: Mohu použít Aspose.PSD pro komerční projekty?

 A2: Ano, můžete. Návštěva[tady](https://purchase.aspose.com/buy) prozkoumat možnosti licencování.

### Q3: Je k dispozici bezplatná zkušební verze?

 A3: Ano, můžete získat bezplatnou zkušební verzi.[tady](https://releases.aspose.com/).

### Q4: Kde najdu podporu pro Aspose.PSD pro Java?

 A4: Navštivte[Fórum Aspose.PSD](https://forum.aspose.com/c/psd/34) pro jakékoli dotazy týkající se podpory.

### Q5: Jak získám dočasnou licenci pro Aspose.PSD?

 A5: Můžete získat dočasnou licenci.[tady](https://purchase.aspose.com/temporary-license/).