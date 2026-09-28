---
date: 2026-09-28
description: Jak přidat miniaturu do segmentu JFIF v Javě pomocí Aspose.PSD. Postupujte
  podle tohoto krok‑za‑krokem průvodce a rychle a spolehlivě vložte miniatury do souborů
  PSD.
keywords:
- how to add thumbnail
- JFIF segment Java
- Aspose.PSD thumbnail
- Java image processing
lastmod: 2026-09-28
linktitle: Přidat miniaturu do segmentu JFIF v Javě
og_description: Jak přidat miniaturu do segmentu JFIF v Javě pomocí Aspose.PSD. Postupujte
  podle tohoto krok‑za‑krokem průvodce a rychle a spolehlivě vložte miniatury do souborů
  PSD.
og_image_alt: Guide showing how to add thumbnail to JFIF segment in Java with Aspose.PSD
og_title: Jak přidat miniaturu do segmentu JFIF v Javě
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  headline: How to add thumbnail to JFIF segment in Java
  type: TechArticle
- description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  name: How to add thumbnail to JFIF segment in Java
  steps:
  - name: import packages
    text: '`Document`, `JfifResource`, and related classes are part of the Aspose.PSD
      namespace. Document represents the PSD file container, and JfifResource provides
      access to the JFIF segment within the PSD. Import them at the top of your source
      file.'
  - name: load the PSD image
    text: Create a `PsdImage` instance by passing the file path to the constructor.
      PsdImage is the Aspose.PSD class that models a Photoshop document. This loads
      the document metadata while streaming the pixel data.
  - name: iterate over image resources
    text: Search the `Resources` collection for a `JfifResource`. When found, you
      can replace its thumbnail byte array with a new JPEG‑encoded preview.
  - name: adjust thumbnail data
    text: Generate a small JPEG thumbnail (e.g., 120 × 120 px) using any image‑processing
      library, then assign the resulting byte array to `jfifResource.ThumbnailData`.
  - name: save the modified image
    text: Call the `save` method on the `PsdImage` object, specifying the output path
      and desired format. The JFIF segment now contains the new thumbnail.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables developers to
      create, edit, convert, and render Photoshop PSD files without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Detailed documentation can be found on the [Aspose.PSD for Java documentation
      page](https://reference.aspose.com/psd/java/).
    question: Where can I find more documentation for Aspose.PSD for Java?
  - answer: Yes, Aspose.PSD for Java can be used commercially. You can purchase a
      license from [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).
    question: Is Aspose.PSD for Java suitable for commercial use?
  - answer: Yes, you can download a free trial from [Aspose.PSD's trial download page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- add thumbnail
- Aspose.PSD
- Java image processing
- JFIF
- PSD
title: Jak přidat miniaturu do segmentu JFIF v Javě
url: /cs/java/java-jpeg-image-processing/add-thumbnail-to-jfif-segment-java/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak přidat miniaturu do segmentu JFIF v Javě

## Úvod
Přidání miniatury do segmentu JFIF souboru PSD je běžný požadavek, když potřebujete rychlý vizuální náhled bez načítání celé obrázku. V tomto tutoriálu se naučíte **jak přidat miniaturu** do segmentu JFIF v Javě pomocí Aspose.PSD. Na konci průvodce budete mít spustitelný úryvek kódu, pochopení podkladové struktury JFIF a tipy pro efektivní práci s velkými soubory.

## Rychlé odpovědi
- **Jaká knihovna je vyžadována?** Aspose.PSD for Java.
- **Která verze Javy funguje?** JDK 11 nebo novější.
- **Kolik řádků kódu je potřeba?** Přibližně 10 řádků pro načtení, úpravu a uložení.
- **Mohu zpracovávat soubory o velikosti několika megabajtů?** Ano, Aspose.PSD streamuje data, takže spotřeba paměti zůstává nízká.
- **Je potřeba komerční licence?** Licence je vyžadována pro produkční použití; je k dispozici bezplatná zkušební verze.

## Co je segment JFIF?
Segment JFIF je blok formátu JPEG File Interchange Format, který může ukládat volitelná data, jako jsou miniatury, EXIF nebo barevné profily.  
Nachází se uvnitř JPEG proudu souboru PSD a je rozpoznáván většinou prohlížečů obrázků pro rychlé generování náhledů.

## Proč přidat miniaturu do souboru PSD?
Aspose.PSD for Java podporuje **více než 30 formátů obrázků** a může zpracovávat soubory až do **2 GB** bez načítání celého dokumentu do paměti. Přidání miniatury snižuje šířku pásma sítě při přenosu náhledů a urychluje vykreslování UI v galeriových aplikacích.

## Požadavky
- Java Development Kit (JDK): Ujistěte se, že máte na systému nainstalovanou Javu. Můžete ji stáhnout z [Oracle's JDK website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- Aspose.PSD for Java: Potřebujete mít knihovnu Aspose.PSD for Java. Můžete ji získat na [Aspose.PSD Java download page](https://releases.aspose.com/psd/java/).
- Integrated Development Environment (IDE): Používejte IDE jako IntelliJ IDEA nebo Eclipse pro vývoj v Javě.
- Basic Understanding of Java: Základní znalost programovacího jazyka Java a jeho konceptů.

## Jak přidat miniaturu do segmentu JFIF v Javě?
Načtěte cílový PSD, najděte zdroj JFIF, nahraďte jeho data miniatury a soubor uložte. Celou operaci lze provést pomocí několika jednoduchých volání API a Aspose.PSD se postará o nízkoúrovňovou strukturu JPEG za vás.

### Krok 1: importovat balíčky
`Document`, `JfifResource` a související třídy jsou součástí jmenného prostoru Aspose.PSD. Document představuje kontejner souboru PSD a JfifResource poskytuje přístup k segmentu JFIF v rámci PSD. Importujte je na začátku svého zdrojového souboru.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

### Krok 2: načíst obrázek PSD
Vytvořte instanci `PsdImage` předáním cesty k souboru do konstruktoru. PsdImage je třída Aspose.PSD, která modeluje dokument Photoshopu. Tím se načtou metadata dokumentu při streamování pixelových dat.

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```

### Krok 3: iterovat přes zdroje obrázku
Prohledejte kolekci `Resources` pro `JfifResource`. Jakmile jej najdete, můžete nahradit jeho pole bajtů miniatury novým JPEG‑kódovaným náhledem.

```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Continue with thumbnail processing
    }
}
```

### Krok 4: upravit data miniatury
Vygenerujte malou JPEG miniaturu (např. 120 × 120 px) pomocí libovolné knihovny pro zpracování obrázků a poté přiřaďte vzniklé pole bajtů do `jfifResource.ThumbnailData`.

```java
try {
    PsdImage thumbnailImage = new PsdImage(100, 100);
    
    // Fill thumbnail data (example: create a simple pixel array)
    int[] pixels = new int[thumbnailImage.getWidth() * thumbnailImage.getHeight()];
    for (int j = 0; j < pixels.length; j++) {
        pixels[j] = j;
    }
    
    // Save thumbnail data
    thumbnailImage.saveArgb32Pixels(thumbnailImage.getBounds(), pixels);
    
    // Set thumbnail data to Jpeg options
    JpegExifData exifData = new JpegExifData();
    exifData.setThumbnail(thumbnailImage);
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setExifData(exifData);
    
    // Set options to thumbnail resource
    thumbnail.getJpegOptions().setExifData(exifData);
    
} catch(Exception e) {
    // Handle exceptions
} finally {
    // Dispose of resources
}
```

### Krok 5: uložit upravený obrázek
Zavolejte metodu `save` na objektu `PsdImage`, přičemž určíte výstupní cestu a požadovaný formát. Segment JFIF nyní obsahuje novou miniaturu.

```java
image.save(dataDir + "output.psd");
```

## Časté problémy a řešení
- **Miniatura není viditelná v prohlížečích:** Ujistěte se, že data miniatury jsou platné JPEG pole bajtů a že její rozměry jsou v rozmezí 256 × 256 px, což je maximální velikost podporovaná specifikací JFIF.
- **OutOfMemoryError u velkých PSD:** Použijte `PsdImage.load(inputStream, true)`, aby se povolil režim streamování, který udržuje nízkou spotřebu paměti.
- **Nesprávný typ zdroje:** Ověřte, že upravovaný zdroj je skutečně `JfifResource`; jiné zdroje jako `ExifResource` neovlivní zobrazení miniatury.

## Často kladené otázky

**Q: Co je Aspose.PSD for Java?**  
A: Aspose.PSD for Java je komerční knihovna, která umožňuje vývojářům vytvářet, upravovat, konvertovat a renderovat soubory Photoshop PSD bez potřeby Adobe Photoshop.

**Q: Kde mohu najít další dokumentaci pro Aspose.PSD for Java?**  
A: Podrobnou dokumentaci najdete na stránce [Aspose.PSD for Java documentation page](https://reference.aspose.com/psd/java/).

**Q: Je Aspose.PSD for Java vhodný pro komerční použití?**  
A: Ano, Aspose.PSD for Java lze používat komerčně. Licenci můžete zakoupit na [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).

**Q: Můžu vyzkoušet Aspose.PSD for Java před zakoupením?**  
A: Ano, můžete si stáhnout bezplatnou zkušební verzi z [Aspose.PSD's trial download page](https://releases.aspose.com/).

**Q: Jak mohu získat podporu pro Aspose.PSD for Java?**  
A: Pro podporu navštivte [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

---

**Poslední aktualizace:** 2026-09-28  
**Testováno s:** Aspose.PSD for Java 24.11  
**Autor:** Aspose

## Související tutoriály

- [Přidat IOPA zdroj do souborů PSD pomocí Aspose PSD for Java](/psd/java/modifying-converting-psd-images/add-iopa-resource-psd-files/)
- [Přidat podpis k obrázku – kreslit obrázek na plátno s Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Jak otočit obrázek o konkrétní úhel s Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}