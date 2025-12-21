---
date: 2025-12-21
description: Naučte se, jak upravit kontrast obrázků pomocí Aspose.PSD pro Javu, přední
  knihovny pro manipulaci s obrázky v Javě, a efektivně převádět PSD do TIFF.
linktitle: Adjust Contrast of an Image
second_title: Aspose.PSD Java API
title: Jak upravit kontrast obrázku pomocí Aspose.PSD pro Javu
url: /cs/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak upravit kontrast obrázku pomocí Aspose.PSD pro Java

## Úvod

Pokud hledáte **jak upravit kontrast** ve svých Java projektech, jste na správném místě. Aspose.PSD pro Java je výkonná **java image manipulation library**, která vám umožní jemně doladit vlastnosti obrázku, jako je kontrast, jas a další. V tomto tutoriálu projdeme přesné kroky, jak zvýšit kontrast PSD souboru a následně **převést PSD na TIFF** pro další workflow.

## Rychlé odpovědi
- **Co znamená „upravit kontrast“?** Změní rozdíl mezi nejtmavšími a nejjasnějšími pixely, čímž zvýrazní detaily.
- **Která knihovna to provádí?** Aspose.PSD pro Java – kompletní nástroj pro zpracování obrázků.
- **Potřebuji licenci?** Dočasná licence stačí pro testování; plná licence je vyžadována pro produkci.
- **Mohu výsledek uložit jako TIFF?** Ano, použijeme `TiffOptions` pro export zpracovaného obrázku.
- **Jak dlouho kód běží?** Obvykle pod jednou sekundou pro standardní PSD soubory.

## Co je úprava kontrastu?
Úprava kontrastu mění tonální rozsah obrázku, zesiluje rozdíl mezi světlými a tmavými oblastmi. To je zvláště užitečné, když obrázky po skenování vypadají ploché nebo při přípravě grafiky pro tisk.

## Proč použít Aspose.PSD pro Java?
- **Bohatá podpora formátů** – otevírejte, upravujte a ukládejte PSD, TIFF, PNG, JPEG a mnoho dalších.
- **Vysoký výkon** – kešování a optimalizace rastrových obrázků snižují paměťovou zátěž.
- **Jednoduché API** – jednorázové volání metod jako `adjustContrast` zvyšuje čitelnost kódu.

## Předpoklady

Než se pustíte do práce, ujistěte se, že máte:

- Základní znalosti programování v Javě.
- Nainstalovanou knihovnu Aspose.PSD pro Java. Stáhnout ji můžete [zde](https://releases.aspose.com/psd/java/).

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

Načteme zdrojový PSD soubor (`sample.psd`) do objektu `Image`, který slouží jako výchozí bod pro veškeré další zpracování.

## Krok 2: Přetypování na RasterImage a kešování dat

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Přetypování na `RasterImage` nám poskytuje přístup k operacím na úrovni pixelů. Kešování zlepšuje výkon, zejména u velkých souborů.

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

Zde nakonfigurujeme `TiffOptions` (bits per sample, photometric interpretation) a zapíšeme kontrastně vylepšený obrázek do TIFF souboru.

## Časté problémy a řešení
- **Obrázek není kešován:** Vždy zavolejte `cacheData()` pro velké PSD soubory, aby se předešlo `OutOfMemoryError`.
- **Neočekávaný posun barev:** Ověřte, že `setPhotometric` odpovídá cílovému barevnému prostoru (RGB vs. CMYK).
- **Soubor nenalezen:** Ujistěte se, že `dataDir` ukazuje na správnou složku a že název souboru je napsán správně.

## Často kladené otázky

### Q1: Je Aspose.PSD kompatibilní s různými formáty obrázků?

A1: Ano, Aspose.PSD podporuje různé formáty obrázků, což poskytuje flexibilitu ve vašich projektech.

### Q2: Jak mohu získat dočasnou licenci pro Aspose.PSD?

A2: Dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).

### Q3: Kde najdu dokumentaci k Aspose.PSD?

A3: Dokumentace je k dispozici [zde](https://reference.aspose.com/psd/java/).

### Q4: Jaké možnosti podpory jsou k dispozici pro Aspose.PSD?

A4: Pro podporu navštivte [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q5: Mohu si zakoupit Aspose.PSD?

A5: Ano, Aspose.PSD můžete koupit [zde](https://purchase.aspose.com/buy).

## Závěr

Nyní víte **jak upravit kontrast** PSD obrázku pomocí Aspose.PSD pro Java a jak **převést PSD na TIFF** pro další zpracování. Tyto kroky vám poskytují detailní kontrolu nad kvalitou obrazu při zachování čistého a udržovatelného kódu. Nebojte se experimentovat s dalšími metodami úpravy obrázku, jako je `adjustBrightness` nebo `adjustGamma`, aby vyhovovaly vašim konkrétním potřebám.

---

**Poslední aktualizace:** 2025-12-21  
**Testováno s:** Aspose.PSD pro Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}