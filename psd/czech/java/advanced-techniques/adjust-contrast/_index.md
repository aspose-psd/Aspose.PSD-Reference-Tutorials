---
date: 2026-02-25
description: Naučte se, jak převést PSD na TIFF a upravit kontrast obrázku pomocí
  Aspose.PSD pro Javu, přední knihovny pro manipulaci s obrázky v Javě.
linktitle: Convert PSD to TIFF and Adjust Contrast
second_title: Aspose.PSD Java API
title: Jak převést PSD na TIFF a upravit kontrast pomocí Aspose.PSD pro Javu
url: /cs/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak převést PSD na TIFF a upravit kontrast pomocí Aspose.PSD pro Java

## Úvod

Pokud potřebujete **convert PSD to TIFF** a zároveň doladit vizuální kvalitu svých grafik, jste na správném místě. V tomto tutoriálu projdeme kompletní workflow pomocí Aspose.PSD pro Java – robustní knihovny pro **java image manipulation**. Naučíte se, jak zvýšit **image contrast adjustment**, kešovat velká rastrová data pro výkon a nakonec **save image as TIFF** pro následné zpracování. Pojďme na to!

## Rychlé odpovědi
- **What does “adjust contrast” mean?** Mění rozdíl mezi nejsvětlejšími a nejtmavšími pixely, čímž zvýrazní detaily.  
- **Which library handles this?** Aspose.PSD pro Java – kompletní sada nástrojů pro zpracování obrázků.  
- **Do I need a license?** Dočasná **temporary aspose license** funguje pro testování; pro produkci je vyžadována plná licence.  
- **Can I **convert PSD to TIFF**?** Určitě – použijeme `TiffOptions` k exportu zpracovaného obrázku.  
- **How long does the code take to run?** Obvykle méně než sekunda pro standardně velké PSD soubory na moderním hardware.

## Co je úprava kontrastu obrázku?

Úprava kontrastu mění tonální rozsah obrázku, zesiluje rozdíl mezi světlými a tmavými oblastmi. To je zvláště užitečné, když obrázky vypadají po skenování ploché nebo při přípravě grafik pro tisk.

## Proč použít Aspose.PSD pro Java?

- **Rich format support** – otevírejte, upravujte a **save image as TIFF**, PNG, JPEG a mnoho dalších.  
- **High performance** – kešování a optimalizace rastrových obrázků snižují paměťovou zátěž, což je klíčové pro velké PSD soubory.  
- **Straight‑forward API** – volání jedné metody jako `adjustContrast` činí kód čitelným a udržovatelným.  
- **Comprehensive java image manipulation** – komplexní schopnosti **java image manipulation**, které vyhovují jak jednoduchým skriptům, tak podnikovým aplikacím.

## Požadavky

Než se pustíte dál, ujistěte se, že máte:

- Základní znalosti programování v Java.  
- Nainstalovanou knihovnu Aspose.PSD pro Java. Můžete si ji stáhnout [zde](https://releases.aspose.com/psd/java/).

## Import balíčků

Přidejte potřebné importy do své Java třídy:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Krok 1: Načtení obrázku

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

Načteme zdrojový PSD soubor (`sample.psd`) do objektu `Image`, který slouží jako vstupní bod pro veškeré další zpracování.

## Krok 2: Přetypování na RasterImage a kešování dat

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Přetypování na `RasterImage` nám umožňuje přístup k operacím na úrovni pixelů. Kešování zlepšuje výkon, zejména u velkých souborů.

## Jak upravit kontrast obrázku

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

Metoda `adjustContrast` přijímá celé číslo představující procentuální změnu. V tomto příkladu zvýšíme kontrast o **50 %**.

## Převod PSD na TIFF pomocí Aspose.PSD

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Zde nastavíme `TiffOptions` (bity na vzorek, fotometrickou interpretaci) a **save image as TIFF**. Tento krok dokončuje workflow **convert PSD to TIFF**.

## Časté problémy a řešení
- **Image not cached:** Vždy zavolejte `cacheData()` pro velké PSD soubory, aby se předešlo `OutOfMemoryError`.  
- **Unexpected color shift:** Ověřte, že `setPhotometric` odpovídá cílovému barevnému prostoru (RGB vs. CMYK).  
- **File not found:** Ujistěte se, že `dataDir` ukazuje na správnou složku a že název souboru je napsán správně.

## Často kladené otázky

### Q1: Je Aspose.PSD kompatibilní s různými formáty obrázků?

A1: Ano, Aspose.PSD podporuje různé formáty obrázků, což poskytuje flexibilitu ve vašich projektech.

### Q2: Jak získat dočasnou licenci pro Aspose.PSD?

A2: Dočasnou licenci získáte [zde](https://purchase.aspose.com/temporary-license/).

### Q3: Kde najdu dokumentaci k Aspose.PSD?

A3: Dokumentace je k dispozici [zde](https://reference.aspose.com/psd/java/).

### Q4: Jaké možnosti podpory jsou k dispozici pro Aspose.PSD?

A4: Pro podporu navštivte [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q5: Můžu si zakoupit Aspose.PSD?

A5: Ano, Aspose.PSD si můžete koupit [zde](https://purchase.aspose.com/buy).

## Závěr

Nyní víte **how to convert PSD to TIFF** a jak provést **image contrast adjustment** pomocí Aspose.PSD pro Java. Tyto kroky vám poskytují detailní kontrolu nad kvalitou obrázku a zároveň udržují kód čistý a udržovatelný. Neváhejte experimentovat s dalšími metodami úprav, jako jsou `adjustBrightness` nebo `adjustGamma`, aby vyhovovaly vašim konkrétním potřebám.

---

**Last Updated:** 2026-02-25  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}