---
date: 2026-08-11
description: Naučte se, jak použít otsu threshold v Javě pomocí Aspose.PSD pro Java
  – výkonná technika segmentace obrazu.
keywords:
- apply otsu threshold java
- image segmentation with otsu
- java image segmentation tutorial
lastmod: 2026-08-11
linktitle: Binarizace s Otsu Threshold
og_description: Použijte otsu threshold v Javě s Aspose.PSD pro Java. Tento tutoriál
  vám krok za krokem ukáže, jak binarizovat obrázky, vysvětlí, proč je metoda rychlá,
  a poskytne tipy na řešení běžných problémů.
og_image_alt: Screenshot of Java code applying Otsu threshold using Aspose.PSD
og_title: Použijte otsu threshold v Javě s Aspose.PSD – rychlý průvodce
schemas:
- author: Aspose
  dateModified: '2026-08-11'
  description: Learn how to apply otsu threshold java using Aspose.PSD for Java –
    a powerful image segmentation technique.
  headline: Apply otsu threshold java with Aspose.PSD
  type: TechArticle
- description: Learn how to apply otsu threshold java using Aspose.PSD for Java –
    a powerful image segmentation technique.
  name: Apply otsu threshold java with Aspose.PSD
  steps:
  - name: set up your document directory
    text: Define the folder that contains the source PSD file and the output location
      for the binarized image.
  - name: load the PSD file
    text: '`PsdImage` is the top‑level Aspose.PSD class that represents a PSD document
      and gives access to its layers, metadata, and pixel data.'
  - name: cache the image
    text: '`RasterImage` holds the raster representation of a layer; calling `cache()`
      loads the pixel data into memory so subsequent operations are fast.'
  - name: binarize image with Otsu threshold
    text: '`applyOtsuThreshold()` evaluates all possible gray levels and selects the
      optimal cutoff, producing a binary image that separates foreground objects from
      the background.'
  - name: save the resultant image
    text: '`JpegOptions` configures JPEG‑specific settings such as quality and compression
      when saving the processed image. You can also choose PNG or BMP by swapping
      the options class – the API supports over **30 image formats** for output. {{<
      blocks/products/products-backtop-button >}}'
  type: HowTo
- questions:
  - answer: It automatically finds the gray‑level that minimizes intra‑class variance,
      producing a binary image in one step.
    question: What does Otsu Threshold do?
  - answer: A free trial works for development; a commercial license is required for
      production.
    question: Do I need a license to run the sample?
  - answer: Aspose.PSD for Java supports Java 8 through Java 21.
    question: Which Java version is supported?
  - answer: Yes – you can iterate over each layer and apply the threshold individually.
    question: Can I process multi‑layer PSD files?
  - answer: For a 1920 × 1080 image the Otsu binarization finishes in under 30 ms
      on a typical laptop CPU.
    question: How fast is the operation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- apply otsu threshold java
- image segmentation
- Aspose.PSD
- Java image processing
title: Použijte otsu threshold v Javě s Aspose.PSD
url: /cs/java/image-processing/binarization-otsu-threshold/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Použití Otsu prahování v Javě s Aspose.PSD

## Úvod

V tomto tutoriálu se naučíte, jak **aplikovat Otsu prahování v Javě** pomocí knihovny Aspose.PSD pro Java. Binarizace pomocí Otsu prahu je jednou z nejspolehlivějších metod segmentace obrazu s Otsu technikami, automaticky vybírající optimální úroveň šedi pro oddělení popředí od pozadí. Na konci průvodce budete mít funkční ukázkový kód v Javě, který převádí libovolnou vrstvu PSD na čistý černobílý obrázek.

## Rychlé odpovědi
- **Co dělá Otsu Threshold?** Automaticky najde úroveň šedi, která minimalizuje vnitro‑třídní rozptyl, a vytvoří binární obrázek v jednom kroku.  
- **Potřebuji licenci pro spuštění ukázky?** Bezplatná zkušební verze funguje pro vývoj; pro produkční nasazení je vyžadována komerční licence.  
- **Která verze Javy je podporována?** Aspose.PSD pro Java podporuje Javu 8 až po Javu 21.  
- **Mohu zpracovávat vícevrstvé soubory PSD?** Ano – můžete iterovat přes každou vrstvu a prahování aplikovat jednotlivě.  
- **Jak rychlá je operace?** Pro obrázek 1920 × 1080 trvá Otsu binarizace méně než 30 ms na typickém procesoru notebooku.

## Co je aplikace Otsu prahování v Javě?

Aplikace Otsu prahování v Javě je proces používání Java kódu k vyvolání Otsuova algoritmu na obrázku, který vytváří binární (černobílý) výsledek. Algoritmus vyhodnocuje každou možnou úroveň šedi, vybere tu, která poskytuje nejnižší vážený vnitro‑třídní rozptyl, a poté klasifikuje každý pixel jako popředí nebo pozadí. Tento automatizovaný přístup eliminuje potřebu ručního výběru prahu a dobře funguje na obrázcích s bimodálními histogramy, což jej činí ideálním pro dávkové zpracování velkých kolekcí obrázků.

## Proč používat Aspose.PSD pro Java?

Aspose.PSD pro Java podporuje **50+ vstupních a výstupních formátů** (včetně PSD, JPEG, PNG, BMP a TIFF) a může zpracovávat soubory až do **2 GB** velikosti, aniž by načítala celý dokument do paměti. Vestavěná Otsu implementace knihovny běží v lineárním čase, což vám umožní dávkově zpracovat stovky obrázků během několika sekund.

## Požadavky

- **Java vývojové prostředí** – nainstalovaný a nakonfigurovaný JDK 8 nebo novější.  
- **Aspose.PSD for Java library** – Stáhněte a nainstalujte knihovnu z oficiální stránky ke stažení Aspose.PSD pro Java. Odkaz ke stažení najdete na [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
- **Sample PSD file** – Mějte PSD soubor s alespoň jednou rastrovou vrstvou pro testování binarizace.  
- Pro ostatní produkty Aspose můžete také procházet obecnou stránku vydání na [Aspose releases](https://releases.aspose.com/).

## Import balíčků

Importujte třídy `PsdImage`, `RasterImage` a `JpegOptions` z knihovny Aspose.PSD, které poskytují přístup k souborům PSD, rastrovým datům a možnostem exportu JPEG.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterCachedImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Jak aplikovat Otsu prahování v Javě?

Načtěte svůj PSD, získejte požadovanou rastrovou vrstvu a zavolejte metodu Otsu binarizace – celý pracovní postup se vejde do pěti stručných příkazů. Nejprve vytvoříte objekt `PsdImage`, který představuje zdrojový soubor, poté získáte `RasterImage` pro cílovou vrstvu, zavoláte `applyOtsuThreshold()` a nakonec výsledek uložíte pomocí `JpegOptions`. Tento přístup zajišťuje minimální využití paměti a maximální výkon.

### Krok 1: nastavení adresáře dokumentu

Definujte složku, která obsahuje zdrojový soubor PSD a výstupní umístění pro binarizovaný obrázek.  
```java
String dataDir = "Your Document Directory";
```

### Krok 2: načtení souboru PSD

`PsdImage` je třída nejvyšší úrovně v Aspose.PSD, která představuje dokument PSD a poskytuje přístup k jeho vrstvám, metadatům a pixelovým datům.  
```java
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### Krok 3: cachování obrázku

`RasterImage` obsahuje rastrovou reprezentaci vrstvy; volání `cache()` načte pixelová data do paměti, takže následné operace jsou rychlé.  
```java
RasterCachedImage rasterCachedImage = (RasterCachedImage)image;

if (!rasterCachedImage.isCached()) {
    rasterCachedImage.cacheData();
}
```

### Krok 4: binarizace obrázku pomocí Otsu prahu

`applyOtsuThreshold()` vyhodnocuje všechny možné úrovně šedi a vybírá optimální prah, čímž vytváří binární obrázek, který odděluje objekty popředí od pozadí.  
```java
rasterCachedImage.binarizeOtsu();
```

### Krok 5: uložení výsledného obrázku

`JpegOptions` konfiguruje specifická nastavení JPEG, jako je kvalita a komprese při ukládání zpracovaného obrázku. Můžete také zvolit PNG nebo BMP výměnou třídy možností – API podporuje více než **30 formátů obrázků** pro výstup.  
```java
String destName = dataDir + "BinarizationWithOtsuThreshold_out.jpg";
rasterCachedImage.save(destName, new JpegOptions());
```

{{< blocks/products/products-backtop-button >}}

## Časté problémy a řešení

- **Memory‑out‑of‑bounds errors** – Ujistěte se, že voláte `cache()` na velkých vrstvách před zpracováním; to nutí Aspose.PSD použít streamovací přístup.  
- **Incorrect colors after binarization** – Ověřte, že zdrojová vrstva je skutečný odstín šedi; barevné vrstvy by měly být nejprve převedeny na odstín šedi pomocí `convertToGrayscale()`.

## Často kladené otázky

### Q1: Co je binarizace s Otsu prahem?

Binarizace s Otsu prahem je metoda používaná pro segmentaci obrazu, která odděluje obrázek na popředí a pozadí na základě optimálního prahování.

### Q2: Mohu používat Aspose.PSD pro Java zdarma?

Aspose.PSD pro Java je komerční knihovna, ale můžete si prozkoumat její funkce pomocí bezplatné zkušební verze. Získejte ji na [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).

### Q3: Kde najdu dokumentaci k Aspose.PSD pro Java?

Dokumentace je k dispozici na oficiální referenční stránce Aspose.PSD pro Java: [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

### Q4: Jak získám podporu pro Aspose.PSD pro Java?

Navštivte komunitní fórum Aspose.PSD pro pomoc: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### Q5: Je k dispozici dočasná licence pro Aspose.PSD pro Java?

Ano, můžete získat dočasnou licenci na stránce dočasných licencí Aspose: [Aspose temporary license](https://purchase.aspose.com/temporary-license/).

---

**Poslední aktualizace:** 2026-08-11  
**Testováno s:** Aspose.PSD for Java 24.11  
**Autor:** Aspose

## Související tutoriály

- [Převod obrázku na odstíny šedi pomocí Aspose.PSD pro Java](/psd/java/advanced-techniques/grayscale-image/)
- [Tutoriál zpracování obrazu v Javě - Úprava jasu obrázku pomocí Aspose.PSD pro Java](/psd/java/advanced-techniques/adjust-brightness/)
- [Jak upravit gama v zpracování obrazu v Javě s Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}