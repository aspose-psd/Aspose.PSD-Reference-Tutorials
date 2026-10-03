---
date: 2026-10-03
description: Naučte se, jak v Javě extrahovat miniaturu z PSD pomocí Aspose.PSD. Tento
  krok‑za‑krokem průvodce zahrnuje nastavení, ukázky kódu a uložení miniatury jako
  JPEG obrázku.
keywords:
- extract thumbnail from psd
- java aspose psd
- psd thumbnail extraction
lastmod: 2026-10-03
linktitle: Extrahovat miniaturu z PSD v Javě
og_description: Naučte se, jak v Javě extrahovat miniaturu z PSD s Aspose.PSD. Tento
  průvodce vás provede nastavením, načtením souboru, extrakcí miniatury a uložením
  jako JPEG obrázku.
og_image_alt: Screenshot showing Java code extracting a thumbnail from a PSD file
  using Aspose.PSD
og_title: Extrahovat miniaturu z PSD v Javě pomocí Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to extract thumbnail from PSD in Java using Aspose.PSD. This
    step‑by‑step guide covers setup, code snippets, and saving the thumbnail as a
    JPEG image.
  headline: Extract thumbnail from PSD in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is a Java library that enables programmatic creation, manipulation,
      and conversion of PSD and other raster image formats without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD?
  - answer: You can refer to the [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references and examples.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library’s capabilities.
    question: Can I try Aspose.PSD for free before purchasing?
  - answer: Temporary licenses are available from the [temporary license](https://purchase.aspose.com/temporary-license/)
      page.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Yes, Aspose.PSD can be used in both personal and commercial projects under
      its licensing terms.
    question: Is Aspose.PSD suitable for commercial use?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose.psd
- thumbnail extraction
title: Extrahovat miniaturu z PSD v Javě
url: /cs/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Extrahovat miniaturu z PSD v Javě

## Úvod
Extrahování miniatury ze souboru PSD vám umožní rychle vytvořit náhledy, aniž byste museli načítat obrázek v plném rozlišení. V Javě to usnadňuje a zrychluje knihovna Aspose.PSD. V tomto tutoriálu se naučíte, jak nastavit knihovnu, najít zdroj miniatury a uložit jej jako soubor JPEG – vše pomocí několika řádků kódu.

## Rychlé odpovědi
- **Která knihovna zpracovává miniatury PSD?** Aspose.PSD for Java.  
- **Kolik řádků kódu je potřeba?** Přibližně pět řádků pro načtení, extrakci a uložení.  
- **Mohu extrahovat miniatury z velkých souborů PSD?** Ano, Aspose.PSD zpracovává soubory až do 500 MB bez načítání celé paměti.  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro hodnocení; licence je vyžadována pro produkci.  
- **Jaké výstupní formáty jsou podporovány?** Extrahovaná miniatura může být uložena jako JPEG, PNG nebo BMP.

## Co je extrahování miniatury z PSD?
Extrahování miniatury z PSD je proces čtení malé náhledové obrázku vloženého uvnitř dokumentu Photoshop (PSD). Tento náhled je uložen jako zdroj a může být uložen samostatně pro katalogizaci nebo zobrazovací účely. Miniatura je typicky nízké rozlišení, které aplikace používají k rychlému vizuálnímu shrnutí bez načítání obrázku v plné velikosti.

## Proč použít Aspose.PSD pro tento úkol?
Aspose.PSD podporuje **více než 30 formátů obrázků** a dokáže zpracovat soubory PSD až do **500 MB**, přičemž udržuje nízkou spotřebu paměti, protože čte zdroje na vyžádání. API také poskytuje robustní zpracování chyb, takže můžete spolehlivě extrahovat miniatury i z poškozených souborů.

## Požadavky
- Nainstalovaný Java Development Kit (JDK).  
- Aspose.PSD for Java knihovna stažená z [Aspose.PSD for Java download](https://releases.aspose.com/psd/java/).  
- Základní znalost syntaxe Javy a nastavení projektu.

## Jak extrahovat miniaturu ze souboru PSD v Javě?
Načtěte soubor PSD pomocí `PsdImage`, najděte `ThumbnailResource` a uložte jeho data jako JPEG. Aspose.PSD abstrahuje nízkoúrovňové parsování, takže stačí zavolat `getResources()` a následně `save()` na extrahovaném obrázku. Tento přístup funguje pro jakýkoli PSD, který obsahuje miniaturu, bez ohledu na velikost souboru.

## Importovat balíčky
`Image` je základní třída pro načítání obrázků. `PsdImage` představuje dokument PSD. `ThumbnailResource` a `Thumbnail4Resource` představují zdroje miniatur. `JpegOptions` určuje možnosti uložení JPEG.

```text
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
```

## Krok 1: načíst soubor PSD
Nejprve vytvořte instanci `PsdImage`, která ukazuje na váš soubor PSD. Konstruktor načte pouze hlavičku a potřebné zdroje, čímž minimalizuje využití paměti.

```text
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
```

Nahraďte `"Your_Document_Directory/"` cestou ke složce, kde se nachází váš soubor PSD, a `"your_file.psd"` názvem vašeho souboru PSD.

## Krok 2: iterovat přes zdroje obrázku
Aspose.PSD ukládá miniatury jako objekty `ThumbnailResource` uvnitř kolekce zdrojů obrázku. Projděte kolekci, zkontrolujte typ zdroje a zachyťte první nalezenou miniaturu.

```text
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```
```

## Krok 3: uložit extrahovanou miniaturu
Jakmile máte obrázek miniatury, zavolejte jeho metodu `save`, aby se zapsal na disk. Můžete zvolit JPEG, PNG nebo BMP; JPEG je nejčastěji používaný pro webové náhledy.

## Krok 4: zpracování různých typů miniatur
Pokud PSD obsahuje více variant miniatur, například `Thumbnail4Resource`, rozšiřte logiku iterace tak, aby kontrolovala každý typ. API poskytuje samostatné třídy pro každý zdroj, což vám umožní vybrat požadované rozlišení.

## Časté problémy a řešení
- **Žádná miniatura nenalezena:** Ne všechny soubory PSD obsahují náhled. Ověřte zdrojový soubor v panelu Photoshopu „File → File Info“.  
- **Chyba nepodporovaného formátu:** Ujistěte se, že používáte nejnovější verzi Aspose.PSD; starší verze mohou postrádat nové typy zdrojů miniatur.  
- **Nedostatek paměti u velkých souborů:** Použijte `PsdImage.load(..., LoadOptions)` s `LoadOptions.setLoadResourcesOnly(true)`, abyste se vyhnuli načítání celých dat obrázku, když potřebujete jen miniaturu.

## Často kladené otázky

**Q: Co je Aspose.PSD?**  
A: Aspose.PSD je Java knihovna, která umožňuje programově vytvářet, upravovat a konvertovat soubory PSD a další rastrové formáty obrázků bez nutnosti Adobe Photoshopu.

**Q: Kde mohu najít více dokumentace k Aspose.PSD pro Java?**  
A: Podrobné reference API a příklady najdete v [documentation](https://reference.aspose.com/psd/java/).

**Q: Mohu vyzkoušet Aspose.PSD zdarma před zakoupením?**  
A: Ano, můžete si stáhnout [free trial](https://releases.aspose.com/) a vyzkoušet si možnosti knihovny.

**Q: Jak získat dočasnou licenci pro Aspose.PSD?**  
A: Dočasné licence jsou k dispozici na stránce [temporary license](https://purchase.aspose.com/temporary-license/).

**Q: Je Aspose.PSD vhodný pro komerční použití?**  
A: Ano, Aspose.PSD může být používán jak v osobních, tak v komerčních projektech podle licenčních podmínek.

---

**Poslední aktualizace:** 2026-10-03  
**Testováno s:** Aspose.PSD for Java 24.12  
**Autor:** Aspose

## Související tutoriály

- [Jak převést PSD na rastrové formáty obrázků s Aspose.PSD pro Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Uložit PSD jako JPEG a podpora RGB barev s Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [Změna velikosti obrázku s Aspose.PSD pro Java – kreslení tvarů a základní operace s obrázkem](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}