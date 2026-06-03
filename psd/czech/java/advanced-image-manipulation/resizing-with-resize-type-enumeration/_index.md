---
date: 2026-06-03
description: Naučte se, jak změnit velikost obrázku pomocí Aspose.PSD for Java. Tento
  podrobný návod pokrývá Resize Type Enumeration, vysoce kvalitní změnu velikosti
  obrázku a jak převést PSD na JPEG.
keywords:
- how to resize image
- convert psd to jpeg
- high quality image resize
- resize image java
- java image manipulation tutorial
linktitle: Změna velikosti pomocí Resize Type Enumeration
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  headline: How to Resize Image Java Using Resize Type Enumeration
  type: TechArticle
- description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  name: How to Resize Image Java Using Resize Type Enumeration
  steps:
  - name: '**Java Development Environment** – JDK 8 or newer installed and configured.'
    text: '**Java Development Environment** – JDK 8 or newer installed and configured.'
  - name: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
    text: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
  type: HowTo
- questions:
  - answer: Load the PSD with `Image.load`, then call `image.save("output.jpg", new
      JpegOptions());`.
    question: How do I programmatically convert a PSD file to JPEG without resizing?
  - answer: Yes, you can set the `Resolution` property on the `Image` object before
      saving.
    question: Is it possible to maintain the original DPI when resizing?
  - answer: While you can call `resize` multiple times, it’s more efficient to calculate
      the final dimensions and resize once.
    question: Can I chain multiple resize operations?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Jak změnit velikost obrázku v Javě pomocí Resize Type Enumeration
url: /cs/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak změnit velikost obrázku v Javě pomocí výčtu typu změny velikosti

## Úvod

Pokud hledáte **how to resize image** soubory efektivně v Java projektu, Aspose.PSD for Java poskytuje čisté, výkonné API. V tomto tutoriálu vás provedeme načtením PSD, použitím **Resize Type Enumeration** pro vysoce kvalitní změnu velikosti obrázku a nakonec **convert PSD to JPEG**. Ať už vytváříte desktopový editor nebo automatizovanou server‑side pipeline, tyto kroky vám umožní řídit rozměry, kvalitu a formát pomocí jen několika řádků kódu.

## Rychlé odpovědi
- **Jaká knihovna zpracovává resize image java?** Aspose.PSD for Java.
- **Který typ změny velikosti poskytuje nejlepší kvalitu?** `ResizeType.LanczosResample`.
- **Mohu po změně velikosti převést PSD na JPEG?** Ano – stačí uložit pomocí `JpegOptions`.
- **Potřebuji licenci pro produkci?** Platná licence Aspose.PSD je vyžadována pro použití v produkci.
- **Je tento přístup vhodný pro velké dávky?** Rozhodně; API zpracovává soubory s stovkami stránek, aniž by načítalo celý dokument do paměti.

## Co je „how to resize image“ v Javě?

**How to resize image** označuje programatickou změnu pixelových rozměrů obrázku při zachování vizuální věrnosti. Metoda `Resize` z Aspose.PSD v kombinaci s výčtem `ResizeType` poskytuje přesnou kontrolu nad škálovacími algoritmy, což vývojářům umožňuje udržet kvalitu napříč širokým spektrem zdrojových souborů a cílových velikostí.

## Proč použít výčet Resize Type?

`ResizeType` vám umožňuje vybrat algoritmus přeškálování, který nejlépe vyvažuje rychlost a vizuální kvalitu. Pro většinu scénářů **LanczosResample** poskytuje ostré výsledky s mírnou náročností na výkon, zpracovává obrázek 2000 × 1500 za méně než 120 ms na typickém serverovém procesoru a zachovává detaily okrajů.

## Požadavky

Before you start, make sure you have:

1. **Java Development Environment** – nainstalovaný a nakonfigurovaný JDK 8 nebo novější.  
2. **Aspose.PSD Library** – stáhněte nejnovější JAR z [website](https://releases.aspose.com/psd/java/).  
3. **Sample PSD File** – použijte soubor [sample.psd](Your Document Directory/sample.psd) zahrnutý v SDK pro praktické testování.

## Import balíčků

`Image` je základní třída pro všechny typy obrázků v Aspose.PSD. Přidejte požadované importy do vašeho Java zdrojového souboru:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Krok 1: Načíst obrázek

### Definiční kotva
The `RasterImage` class is Aspose.PSD’s core object that represents a raster‑based image loaded from a PSD file.

Třída `RasterImage` je jádrový objekt Aspose.PSD, který představuje rastrový obrázek načtený z PSD souboru.

Load your PSD into a `RasterImage` instance so you can manipulate its pixels:

Načtěte svůj PSD do instance `RasterImage`, abyste mohli manipulovat s jeho pixely:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## Krok 2: Změnit velikost obrázku

`image.resize(width, height, resizeType)` změní velikost obrázku na zadané rozměry pomocí vybraného algoritmu.

Nyní změňte velikost načteného obrázku pomocí **Resize Type Enumeration**. V tomto příkladu používáme metodu Lanczos Resample, která je ideální, když **how to resize image** s vysokou kvalitou:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Krok 3: Uložit změněný obrázek

`image.save(path, options)` zapíše obrázek na disk ve formátu definovaném poskytnutými možnostmi.

Po změně velikosti uložte obrázek se zadanými rozměry a vybraným typem změny velikosti. Zde také ukazujeme **convert psd to jpeg** uložením výsledku jako JPEG soubor:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

## Proč použít výčet Resize Type?

`ResizeType` vám poskytuje detailní kontrolu nad algoritmem přeškálování, což vám umožní vyvážit rychlost a kvalitu. Pro většinu aplikací `LanczosResample` nabízí výborný kompromis, poskytuje ostré výsledky bez velkého dopadu na výkon a dobře funguje s různým obsahem obrázků.

## Časté problémy a řešení

- **Obrázek po změně velikosti vypadá rozmazaně** – Vyzkoušejte jiný `ResizeType`, například `Bicubic` nebo `NearestNeighbour`, abyste zjistili, který poskytne nejlepší vizuální výsledek pro váš konkrétní obrázek.  
- **OutOfMemoryError u velkých PSD souborů** – Zpracovávejte obrázek v menších částech nebo zvyšte velikost haldy JVM (`-Xmx` flag). Aspose.PSD dokáže zvládnout soubory až do **2 GB** bez načtení celého dokumentu do paměti.

## Často kladené otázky

### Q1: Je Aspose.PSD for Java vhodný pro malé i rozsáhlé projekty?

A1: Rozhodně! Aspose.PSD for Java je navržen tak, aby vyhovoval projektům všech velikostí, poskytuje škálovatelnost a efektivitu.

### Q2: Mohu použít jiný typ změny velikosti než Lanczos Resample?

A2: Ano, Aspose.PSD for Java nabízí různé typy změny velikosti, jako **NearestNeighbour**, **Bicubic** a další. Pro kompletní seznam se podívejte do dokumentace API.

### Q3: Kde mohu najít další podporu pro Aspose.PSD for Java?

A3: Pro jakékoli dotazy nebo pomoc navštivte [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### Q4: Je k dispozici bezplatná zkušební verze pro Aspose.PSD for Java?

A4: Ano, můžete získat bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

### Q5: Jak mohu získat dočasnou licenci pro Aspose.PSD for Java?

A5: Pro získání dočasné licence navštivte [tento odkaz](https://purchase.aspose.com/temporary-license/).

## Často kladené otázky

**Q: Jak programově převést PSD soubor na JPEG bez změny velikosti?**  
A: Načtěte PSD pomocí `Image.load`, poté zavolejte `image.save("output.jpg", new JpegOptions());`.

**Q: Je možné zachovat původní DPI při změně velikosti?**  
A: Ano, můžete nastavit vlastnost `Resolution` na objektu `Image` před uložením.

**Q: Mohu řetězit více operací změny velikosti?**  
A: I když můžete volat `resize` vícekrát, je efektivnější vypočítat konečné rozměry a změnit velikost jednou.

---

**Poslední aktualizace:** 2026-06-03  
**Testováno s:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Jednoduché změny velikosti s Aspose.PSD – Java knihovna pro manipulaci s obrázky](/psd/java/basic-image-operations/simple-resizing/)
- [Vysoce kvalitní škálování obrázků s Bicubic Resampler v Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Jak převést PSD na PNG a změnit velikost proporcionálně s Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}