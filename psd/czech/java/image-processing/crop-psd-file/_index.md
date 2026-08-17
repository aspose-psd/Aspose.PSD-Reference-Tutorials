---
date: 2026-08-17
description: Naučte se, jak crop psd file java s Aspose.PSD for Java – rychlý, přesný
  způsob, jak trim Photoshop dokumenty ve vašich Java aplikacích.
keywords:
- crop psd file java
- aspose.psd java
- java image cropping
lastmod: 2026-08-17
linktitle: Crop PSD File
og_description: Crop psd file java using Aspose.PSD for Java. Tento průvodce vám ukazuje
  step‑by‑step, jak trim Photoshop soubory efektivně, s code‑free vysvětleními a best‑practice
  tipy.
og_image_alt: Guide showing how to crop a PSD file in Java using Aspose.PSD
og_title: Crop psd file java s Aspose.PSD – rychlé image cropping
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  headline: Crop psd file java using Aspose.PSD
  type: TechArticle
- description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  name: Crop psd file java using Aspose.PSD
  steps:
  - name: set document directory
    text: Replace “Your Document Directory” with the absolute or relative path that
      contains the PSD you want to process.
  - name: load PSD file
    text: The `RasterImage` class is Aspose.PSD’s entry point for raster‑based operations
      on a PSD file. Loading the file creates an in‑memory representation that you
      can manipulate.
  - name: define crop area
    text: '`Rectangle` defines the X and Y coordinates together with width and height
      of the region to keep. This class is part of the standard Java AWT package and
      is used by Aspose.PSD to specify cropping bounds.'
  - name: save cropped PSD
    text: After applying the crop, you can persist the result back to PSD format.
      The library writes only the cropped pixels, keeping the original color mode
      and bit depth.
  - name: save cropped image as PNG
    text: If you need a web‑friendly version, export the cropped raster to PNG. Aspose.PSD
      provides PNG save options that let you control compression level and interlacing.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles PSD cropping in Java?
  - answer: Two API calls after loading the image.
    question: How many lines of code are required for a basic crop?
  - answer: Yes, using the built‑in PNG save options.
    question: Can I export the cropped area as PNG?
  - answer: A commercial license is needed beyond the trial period.
    question: Is a license required for production use?
  - answer: Java 8 and later, including Java 11, 17, and 21.
    question: What Java versions are supported?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- crop psd
- aspose.psd
- java image processing
title: Crop psd file java pomocí Aspose.PSD
url: /cs/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Oříznutí souboru PSD v Javě pomocí Aspose.PSD

## Úvod

Pokud potřebujete programově ořezávat dokumenty Photoshopu, **crop psd file java** je běžný úkol pro vývojáře Javy pracující s grafickými pipeline, asset pipeline nebo automatizovanými designovými workflow. Aspose.PSD pro Javu poskytuje specializované API, které vám umožní definovat obdélník a extrahovat požadovanou oblast během několika řádků kódu. V tomto tutoriálu se dozvíte, proč je knihovna vytvořena pro vysoce výkonné ořezávání, jak nastavit své prostředí a přesné kroky k vytvoření výsledků ve formátech PSD i PNG.

## Rychlé odpovědi
- **Jaká knihovna provádí ořezávání PSD v Javě?** Aspose.PSD for Java.
- **Kolik řádků kódu je potřeba pro základní ořez?** Dvě volání API po načtení obrázku.
- **Mohu exportovat oříznutou oblast jako PNG?** Ano, pomocí vestavěných možností uložení PNG.
- **Je licence vyžadována pro produkční použití?** Komerční licence je potřeba po uplynutí zkušební doby.
- **Jaké verze Javy jsou podporovány?** Java 8 a novější, včetně Java 11, 17 a 21.

## Co je crop psd file java?

Crop psd file java označuje proces programového ořezání obdélníkové oblasti z dokumentu Photoshop (.psd) pomocí kódu v Javě. S Aspose.PSD můžete tuto operaci provést bez spouštění Photoshopu, což je ideální pro server‑side image pipeline.

## Proč použít Aspose.PSD pro Javu?

Aspose.PSD podporuje **30+ vstupních a výstupních formátů** a dokáže zpracovat soubory PSD až do **500 MB** bez načítání celého dokumentu do paměti, díky své streamovací architektuře. Knihovna zachovává vrstvy, masky a barevné profily, poskytuje oříznutý výsledek, který odpovídá nativnímu výstupu Photoshopu. Tento kvantifikovaný výkon vám umožní zpracovávat dávkové úlohy na běžném hardware s předvídatelnou spotřebou paměti.

## Požadavky

- **Java vývojové prostředí** – nainstalovaný a nakonfigurovaný JDK 8 nebo novější.
- **Aspose.PSD for Java** – stáhněte nejnovější JAR a dokumentaci [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).
- **Ukázkový soubor PSD** – umístěte soubor .psd do adresáře projektu, aby jej kód mohl najít.

## Jak oříznout soubor PSD v Javě?

Načtěte zdrojový soubor, definujte obdélník, který chcete zachovat, aplikujte ořez a nakonec uložte výsledek v požadovaných formátech. Celý pracovní postup vyžaduje pouze pět jednoduchých kroků, z nichž každý je ilustrován zástupcem, kam vložíte svůj vlastní kód.

### Krok 1: nastavení adresáře dokumentu

Nahraďte „Your Document Directory“ absolutní nebo relativní cestou, která obsahuje PSD, který chcete zpracovat.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

### Krok 2: načtení souboru PSD

Třída `RasterImage` je vstupním bodem Aspose.PSD pro raster‑založené operace na souboru PSD. Načtení souboru vytvoří v‑paměti reprezentaci, kterou můžete manipulovat.

```java
String dataDir = "Your Document Directory";
```

### Krok 3: definování oblasti ořezu

`Rectangle` určuje souřadnice X a Y spolu s šířkou a výškou oblasti, kterou chcete zachovat. Tato třída je součástí standardního balíčku Java AWT a používá ji Aspose.PSD k určení ořezových hranic.

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

### Krok 4: uložení oříznutého PSD

Po aplikaci ořezu můžete výsledek uložit zpět do formátu PSD. Knihovna zapíše pouze oříznuté pixely, zachovává původní barevný režim a bitovou hloubku.

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

### Krok 5: uložení oříznutého obrázku jako PNG

Pokud potřebujete verzi přátelskou pro web, exportujte oříznutý raster do PNG. Aspose.PSD poskytuje možnosti uložení PNG, které vám umožní řídit úroveň komprese a prokládání.

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

## Časté problémy a řešení

- **Nesprávné souřadnice obdélníku** – Ujistěte se, že hodnoty X/Y začínají na 0 pro levý horní roh; záporné hodnoty vyvolají `ArgumentException`.
- **Špičky paměti u velkých souborů** – Použijte možnost `loadOptions.setLoadOnlyVisibleLayers(true)`, abyste snížili paměťovou náročnost, když nepotřebujete skryté vrstvy.
- **Ztráta barevného profilu** – Zachovejte původní ICC profil voláním `image.getColorProfile()` před ořezem a přiřaďte jej zpět po operaci.

## Často kladené otázky

### Q1: mohu použít Aspose.PSD pro Javu k ořezávání obrázků v jiných formátech?

A1: Aspose.PSD primárně cílí na soubory PSD, ale také podporuje BMP, GIF, JPEG, PNG, TIFF a několik dalších rastrových formátů pro vstup i výstup.

### Q2: je Aspose.PSD pro Javu vhodný pro zpracování obrázků ve velkém měřítku?

A2: Ano. Streamovací architektura knihovny zpracovává více‑stovkové soubory PSD s paměťovou stopou pod 100 MB, což je ideální pro dávkové úlohy.

### Q3: existují nějaké licenční úvahy při používání Aspose.PSD pro Javu?

A3: Pro produkční nasazení je vyžadována komerční licence. Podrobnosti jsou k dispozici na [Aspose.PSD for Java purchase page](https://purchase.aspose.com/buy).

### Q4: jak mohu získat podporu pro problémy související s Aspose.PSD pro Javu?

A4: Navštivte [Aspose.PSD for Java forum](https://forum.aspose.com/c/psd/34), kde můžete klást otázky, sdílet úryvky kódu a získat pomoc od komunity a produktových inženýrů.

### Q5: mohu vyzkoušet Aspose.PSD pro Javu před zakoupením?

A5: Ano, plně funkční bezplatná zkušební verze je ke stažení na [Aspose.PSD free trial download](https://releases.aspose.com/).

{{< blocks/products/products-backtop-button >}}

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

## Související tutoriály

- [Oříznutí obrázku obdélníkem v Aspose.PSD pro Javu](/psd/java/image-editing/crop-image-by-rectangle/)
- [Oříznutí obrázku posuny v Aspose.PSD pro Javu](/psd/java/image-editing/crop-image-by-shifts/)
- [Jak otočit obrázek v Javě pomocí Aspose.PSD](/psd/java/advanced-image-manipulation/rotate-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}