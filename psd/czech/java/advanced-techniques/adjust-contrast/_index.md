---
date: 2026-07-27
description: Zjistěte, jak převést PSD na TIFF a provést úpravu kontrastu obrazu pomocí
  Aspose.PSD for Java, přední knihovny pro manipulaci s obrázky v Java.
keywords:
- convert psd to tiff
- java image processing
- improve image contrast
lastmod: 2026-07-27
linktitle: Převod PSD na TIFF a úprava kontrastu
og_description: Převod PSD na TIFF s úpravou kontrastu pomocí Aspose.PSD for Java.
  Tento průvodce ukazuje krok‑za‑krokem kód, tipy na výkon a možnosti exportu pro
  výstup TIFF ve vysoké kvalitě.
og_image_alt: 'Guide: Convert PSD to TIFF and adjust contrast using Aspose.PSD for
  Java'
og_title: Převod PSD na TIFF & úprava kontrastu – Aspose.PSD Java
schemas:
- author: Aspose
  dateModified: '2026-07-27'
  description: Learn how to convert PSD to TIFF and perform image contrast adjustment
    using Aspose.PSD for Java, a leading java image manipulation library.
  headline: Convert PSD to TIFF and Adjust Contrast with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: It changes the difference between the darkest and brightest pixels, making
      details pop.
    question: What does “adjust contrast” mean?
  - answer: Aspose.PSD for Java – a full‑featured image processing toolkit.
    question: Which library handles this?
  - answer: A **temporary Aspose license** works for testing; a full license is required
      for production.
    question: Do I need a license?
  - answer: Absolutely – we’ll use `TiffOptions` to export the processed image.
    question: Can I convert PSD to TIFF?
  - answer: For a typical 30 MB PSD the whole pipeline runs under one second on a
      modern CPU.
    question: How fast is the conversion?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image manipulation
- tiff export options
title: Převod PSD na TIFF a úprava kontrastu s Aspose.PSD for Java
url: /cs/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak převést PSD na TIFF a upravit kontrast pomocí Aspose.PSD pro Java

## Úvod

Pokud potřebujete **převést PSD na TIFF** a zároveň doladit vizuální kvalitu svých grafických souborů, jste na správném místě. V tomto tutoriálu projdeme kompletní workflow pomocí Aspose.PSD pro Java – robustní knihovny **java image manipulation**. Naučíte se, jak zvýšit **úpravu kontrastu obrazu**, kešovat velká rastrová data pro výkon a nakonec **uložit obrázek jako TIFF** pro následné zpracování. Pojďme na to!

## Rychlé odpovědi
- **Co znamená „adjust contrast“?** Mění rozdíl mezi nejtmavšími a nejjasnějšími pixely, čímž zvýrazňuje detaily.  
- **Která knihovna to řeší?** Aspose.PSD pro Java – plnohodnotná sada nástrojů pro zpracování obrázků.  
- **Potřebuji licenci?** **Dočasná licence Aspose** funguje pro testování; pro produkci je vyžadována plná licence.  
- **Mohu převést PSD na TIFF?** Ano – použijeme `TiffOptions` k exportu zpracovaného obrázku.  
- **Jak rychlý je převod?** Pro typický 30 MB PSD celý proces běží pod jednou sekundou na moderním procesoru.

## Co je úprava kontrastu obrazu?
Úprava kontrastu mění tonální rozsah obrázku, zesiluje rozdíl mezi světlými a tmavými oblastmi. To je zvláště užitečné, když obrázky po skenování vypadají ploché nebo při přípravě grafiky pro tisk. Funguje tak, že roztahuje nebo stlačuje histogram intenzity pixelů, čímž prohlubuje stíny a zesvětluje světla, což zvyšuje vnímanou hloubku a detail.

## Proč použít Aspose.PSD pro Java?
Aspose.PSD poskytuje vysoce výkonný, bohatý na funkce engine, který dokáže zpracovat **více než 50 rastrových a vektorových formátů**, pracovat se soubory až do 500 MB bez úplného načtení do paměti a exportovat do TIFF s přesnou kontrolou nad bits‑per‑sample a fotometrickou interpretací. Tyto kvantifikované schopnosti z něj činí špičkovou volbu pro podnikové image pipeline.

## Předpoklady

Než začnete, ujistěte se, že máte:

- Základní znalosti programování v Javě.  
- Nainstalovanou knihovnu Aspose.PSD pro Java. Můžete si ji stáhnout [zde](https://releases.aspose.com/psd/java/).

## Importovat balíčky

Přidejte potřebné importy do své Java třídy:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Krok 1: Načtení obrázku

Třída `Image` je vstupním bodem Aspose.PSD, který představuje libovolný podporovaný rastrový obrázek v paměti.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

Načteme zdrojový PSD soubor (`sample.psd`) do objektu `Image`, který slouží jako vstupní bod pro veškeré další zpracování.

## Krok 2: Přetypování na RasterImage a kešování dat

`RasterImage` poskytuje přímý přístup na úrovni pixelů a umožňuje kešování pro velké soubory.  
```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Přetypování na `RasterImage` nám dává přístup k operacím na úrovni pixelů. Kešování zlepšuje výkon, zejména u velkých souborů.

## Jak upravit kontrast obrázku

Metoda `adjustContrast` je jednoduché volání API, které mění kontrast obrázku o procentuální hodnotu.  
```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

Metoda `adjustContrast` přijímá celé číslo představující procentuální změnu. V tomto příkladu zvýšíme kontrast o **50 %**.

## Převod PSD na TIFF pomocí Aspose.PSD

`TiffOptions` vám umožňuje nastavit specifické parametry TIFF, jako jsou bity na vzorek, typ komprese a fotometrická interpretace.  
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

Zde konfigurujeme `TiffOptions` (bity na vzorek, fotometrická interpretace) a **uložíme obrázek jako TIFF**. Tento krok dokončuje workflow **převodu PSD na TIFF**.

## Časté problémy a řešení
- **Obrázek není kešován:** Vždy zavolejte `cacheData()` pro velké PSD, aby se předešlo `OutOfMemoryError`.  
- **Neočekávaný posun barev:** Ověřte, že `setPhotometric` odpovídá cílovému barevnému prostoru (RGB vs. CMYK).  
- **Soubor nenalezen:** Ujistěte se, že `dataDir` ukazuje na správnou složku a že název souboru je správně napsán.

## Často kladené otázky

### Q1: Je Aspose.PSD kompatibilní s různými formáty obrázků?
A1: Ano, Aspose.PSD podporuje **více než 50 vstupních a výstupních formátů**, včetně PSD, TIFF, PNG, JPEG, BMP a GIF, což vám poskytuje flexibilitu napříč projekty.

### Q2: Jak mohu získat dočasnou licenci pro Aspose.PSD?
A2: Dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).

### Q3: Kde najdu dokumentaci k Aspose.PSD?
A3: Dokumentace je k dispozici [zde](https://reference.aspose.com/psd/java/).

### Q4: Jaké možnosti podpory jsou k dispozici pro Aspose.PSD?
A4: Pro podporu navštivte [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q5: Mohu si zakoupit Aspose.PSD?
A5: Ano, Aspose.PSD můžete zakoupit [zde](https://purchase.aspose.com/buy).

## Závěr

Nyní víte **jak převést PSD na TIFF** a provést **úpravu kontrastu obrazu** pomocí Aspose.PSD pro Java. Tyto kroky vám poskytují jemnou kontrolu nad kvalitou obrázku při zachování čistého a udržovatelného kódu. Klidně experimentujte s dalšími metodami úprav, jako jsou `adjustBrightness` nebo `adjustGamma`, aby vyhovovaly vašim konkrétním potřebám.

---

**Poslední aktualizace:** 2026-07-27  
**Testováno s:** Aspose.PSD for Java 24.12  
**Autor:** Aspose

## Související tutoriály

- [Java Image Processing Tutorial – Úprava jasu obrázku pomocí Aspose.PSD pro Java](/psd/java/advanced-techniques/adjust-brightness/)
- [Jak upravit gama v Java Image Processing pomocí Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)
- [Převod PSD na rastrové formáty obrázků pomocí Aspose.PSD pro Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}