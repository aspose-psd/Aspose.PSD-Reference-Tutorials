---
date: 2026-09-28
description: Tutoriál zpracování obrázků v Javě ukazuje, jak upravit jas obrázku pomocí
  Aspose.PSD pro Javu. Postupujte podle kódu krok po kroku pro načtení, úpravu a uložení
  souborů PSD nebo TIFF.
keywords:
- java image processing
- aspose psd java
- java image manipulation
- adjust brightness java
lastmod: 2026-09-28
linktitle: Úprava jasu obrázku
og_description: Tutoriál zpracování obrázků v Javě ukazuje, jak upravit jas obrázku
  pomocí Aspose.PSD pro Javu. Postupujte podle kódu krok po kroku pro načtení, úpravu
  a uložení souborů PSD nebo TIFF.
og_image_alt: Guide to adjusting image brightness in Java using Aspose.PSD
og_title: 'Zpracování obrázků v Javě: úprava jasu pomocí Aspose.PSD'
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  headline: 'Java image processing: adjust brightness with Aspose.PSD'
  type: TechArticle
- description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  name: 'Java image processing: adjust brightness with Aspose.PSD'
  steps:
  - name: Load the image
    text: The `RasterImage` class represents a rasterized version of a PSD or TIFF
      file in memory. It provides direct pixel access for color‑correction operations.
      In this step, we load the target image and cast it to a `RasterImage` for further
      processing.
  - name: Adjust brightness
    text: '`adjustBrightness(int value)` changes the lightness of every pixel by the
      specified integer value. Positive numbers brighten the image; negative numbers
      darken it. The method processes the image in‑place, so no additional object
      creation is required. Here, we use the `adjustBrightness` method to mod'
  - name: Set TiffOptions
    text: '`TiffOptions` specifies the encoding parameters for TIFF output, such as
      bits per sample and photometric interpretation. It lets you control how the
      resulting file is encoded. Configure the `TiffOptions` for saving the adjusted
      image. Adjust the `bitsPerSample` and `photometric` properties based on '
  - name: Save the resultant image
    text: Calling `save` writes the processed raster data to a file using the previously
      defined options. The operation is atomic and guarantees that the output file
      is a valid TIFF image. Finally, save the modified image using the specified
      `TiffOptions`.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports JPEG, PNG, BMP, GIF, and many other
      raster formats in addition to PSD and TIFF.
    question: Can I adjust brightness in other image formats besides PSD?
  - answer: Wrap the processing code in a try‑catch block and catch `IOException`
      or `ImageProcessingException` to manage file‑access and raster‑operation errors.
    question: How can I handle errors during the image adjustment process?
  - answer: The method accepts integer values from –255 to +255; values outside this
      range are clamped to the nearest limit.
    question: Is there a limit to the range of brightness adjustment?
  - answer: Yes, a commercial license is required for production use. Purchase a license
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial projects?
  - answer: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose psd
- java image manipulation
title: 'Zpracování obrázků v Javě: úprava jasu pomocí Aspose.PSD'
url: /cs/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Upravit jas obrázku pomocí Aspose.PSD pro Java

## Úvod

V tomto **java image processing** tutoriálu se naučíte, jak upravit jas obrázku přímo z Java kódu. Úprava jasu je častý úkol pro grafické designéry, fotografy a všechny, kteří vytvářejí pipeline pro zpracování obrázků. V tomto **java image manipulation** průvodci projdeme kompletní workflow — načtení PSD/TIFF, aplikaci posunu jasu a uložení výsledku — pomocí knihovny Aspose.PSD pro Java.

## Rychlé odpovědi
- **Jaká knihovna zpracovává jas?** Aspose.PSD for Java.  
- **Která metoda mění jas?** `RasterImage.adjustBrightness()`.  
- **Mohu pracovat se soubory PSD a TIFF?** Ano, API podporuje oba formáty a více než 10 dalších typů obrázků.  
- **Potřebuji licenci pro produkci?** Komerční licence je vyžadována pro ne‑evaluaci použití.  
- **Jak dlouho trvá implementace?** Obvykle méně než 10 minut pro základní úpravu.

## Co je java image processing?

`Java image processing` označuje sadu technik, které vám umožňují programově číst, transformovat a zapisovat obrazová data pomocí Javy. Úprava jasu je jednou ze základních operací, která mění celkovou světlost každého pixelu, čímž tmavé oblasti zesvětluje nebo světlé oblasti ztmavuje.

## Proč používat Aspose.PSD pro Java?

Aspose.PSD pro Java poskytuje komplexní, čistě Java řešení, které podporuje širokou škálu rastrových a vektorových formátů, eliminuje nativní závislosti a nabízí vysoce výkonnou cache pro velké soubory. Jeho rozsáhlé API umožňuje vývojářům provádět složité korekce barev a úpravy založené na vrstvách s minimálním kódem, což ho činí ideálním jak pro jednoduché úpravy, tak pro pokročilé pipeline zpracování obrázků.

- **Podporuje více než 10 rastrových a vektorových formátů** – PSD, TIFF, JPEG, PNG, BMP, GIF a další.  
- **Čistá Java implementace** – bez nativních DLL nebo externích závislostí, takže funguje na jakémkoli JVM.  
- **Vysoce výkonná cache** – rastrová data mohou být uložena do cache, což umožňuje až 2× rychlejší opakované úpravy velkých souborů.  
- **Bohaté API** – více než 150 metod pro korekci barev, práci s vrstvami, masky a kompozici.

## Požadavky

Před ponořením se do tutoriálu se ujistěte, že máte následující požadavky:

- Aspose.PSD for Java knihovna: Stáhněte a nainstalujte knihovnu z [dokumentace Aspose.PSD pro Java](https://reference.aspose.com/psd/java/).  
- Java Development Kit (JDK) 8 nebo vyšší nainstalovaný na vašem počítači.  
- Vývojové prostředí (IDE) jako IntelliJ IDEA, Eclipse nebo VS Code.

## Import balíčků

Pro začátek importujte potřebné balíčky do svého Java projektu. V tomto příkladu použijeme následující:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Nyní si rozdělíme proces úpravy jasu obrázku do jednoduchých kroků:

## Jak upravit jas pomocí Aspose.PSD?

Načtěte zdrojový obrázek, aplikujte posun jasu, nakonfigurujte možnosti uložení a zapište výsledek na disk — vše ve čtyřech stručných krocích. Následující sekce poskytují jasný, krok‑za‑krokem průvodce, který můžete zkopírovat do svého projektu. Tento přístup zajišťuje, že každá operace je provedena efektivně a že finální obrázek si zachová původní kvalitu při požadované změně jasu.

### Krok 1: Načíst obrázek

Třída `RasterImage` představuje rasterizovanou verzi souboru PSD nebo TIFF v paměti. Poskytuje přímý přístup k pixelům pro operace korekce barev.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

V tomto kroku načteme cílový obrázek a přetypujeme jej na `RasterImage` pro další zpracování.

### Krok 2: Upravit jas

`adjustBrightness(int value)` mění světlost každého pixelu o zadanou celočíselnou hodnotu. Kladná čísla obrázek zesvětlí; záporná čísla jej ztmaví. Metoda zpracovává obrázek přímo v paměti, takže není potřeba vytvářet další objekty.

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Zde používáme metodu `adjustBrightness` k úpravě jasu obrázku. V tomto příkladu snižujeme jas o 50 jednotek, ale můžete tuto hodnotu přizpůsobit podle svých potřeb.

### Krok 3: Nastavit TiffOptions

`TiffOptions` určuje parametry kódování pro výstup TIFF, jako jsou bity na vzorek a fotometrická interpretace. Umožňuje vám kontrolovat, jak bude výsledný soubor kódován.

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Nakonfigurujte `TiffOptions` pro uložení upraveného obrázku. Přizpůsobte vlastnosti `bitsPerSample` a `photometric` podle konkrétních požadavků.

### Krok 4: Uložit výsledný obrázek

Volání `save` zapíše zpracovaná rasterová data do souboru pomocí dříve definovaných možností. Operace je atomická a zaručuje, že výstupní soubor je platný TIFF obrázek.

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Nakonec uložte upravený obrázek pomocí specifikovaných `TiffOptions`.

## Časté problémy a řešení

| Problém | Důvod | Řešení |
|-------|--------|----------|
| **`ClassCastException` při přetypování Image** | Soubor není rastrový obrázek (např. vektorový PSD). | Ověřte formát zdrojového souboru nebo použijte `image instanceof RasterImage` před přetypováním. |
| **Změna jasu nemá žádný efekt** | Obrázek nebyl před úpravou uložen do cache. | Zavolejte `rasterImage.cacheData()` jak je ukázáno v Kroku 1. |
| **Uložený soubor vypadá poškozeně** | Nesprávná konfigurace `TiffOptions`. | Ujistěte se, že `bitsPerSample` odpovídá hloubce zdrojového obrázku (obvykle 8‑bit na kanál). |

## Často kladené otázky

**Q: Mohu upravit jas i v jiných formátech obrázků než PSD?**  
A: Ano, Aspose.PSD pro Java podporuje JPEG, PNG, BMP, GIF a mnoho dalších rastrových formátů kromě PSD a TIFF.

**Q: Jak mohu ošetřit chyby během procesu úpravy obrázku?**  
A: Zabalte kód zpracování do bloku try‑catch a zachyťte `IOException` nebo `ImageProcessingException` pro správu chyb přístupu k souborům a rasterových operací.

**Q: Existuje limit rozsahu úpravy jasu?**  
A: Metoda přijímá celočíselné hodnoty od –255 do +255; hodnoty mimo tento rozsah jsou oříznuty na nejbližší limit.

**Q: Mohu používat Aspose.PSD pro Java v komerčních projektech?**  
A: Ano, pro produkční použití je vyžadována komerční licence. Zakupte licenci [zde](https://purchase.aspose.com/buy).

**Q: Je k dispozici bezplatná zkušební verze?**  
A: Ano, knihovnu můžete vyzkoušet zdarma z [zde](https://releases.aspose.com/).

**Q: Ovlivňuje metoda `adjustBrightness` viditelnost vrstev?**  
A: Metoda pracuje na rasterizovaném kompozitním obrázku, takže skryté vrstvy jsou během rasterizace ignorovány, což zachovává zamýšlený vizuální výsledek.

**Q: Mohu řetězit více úprav (např. kontrast, saturaci) dohromady?**  
A: Rozhodně. Po úpravě jasu můžete na stejném `RasterImage` volat `adjustContrast`, `adjustSaturation` nebo jiné metody korekce barev.

**Poslední aktualizace:** 2026-09-28  
**Testováno s:** Aspose.PSD for Java 24.12 (nejnovější v době psaní)  
**Autor:** Aspose

## Související tutoriály

- [Knihovna pro zpracování obrázků v Javě: Inverzní vrstva pomocí Aspose.PSD](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [Převést obrázek na odstíny šedi pomocí Aspose.PSD pro Java](/psd/java/advanced-techniques/grayscale-image/)
- [Jak otočit obrázek pod konkrétním úhlem pomocí Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}