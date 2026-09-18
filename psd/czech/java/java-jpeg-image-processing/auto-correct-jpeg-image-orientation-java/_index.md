---
date: 2026-09-18
description: Naučte se, jak automaticky opravit orientaci JPEG v Javě pomocí Aspose.PSD.
  Vylepšete svůj workflow zpracování obrázků automatickým otáčením na základě EXIF.
keywords:
- auto correct jpeg orientation
- Aspose.PSD for Java
- Java image processing
lastmod: 2026-09-18
linktitle: Automatické opravení orientace JPEG obrázku v Javě
og_description: Naučte se, jak automaticky opravit orientaci JPEG v Javě pomocí Aspose.PSD.
  Tento průvodce ukazuje krok za krokem, jak detekovat EXIF data, automaticky otáčet
  obrázky a efektivně ukládat opravené soubory.
og_image_alt: Guide showing auto correction of JPEG orientation in Java with Aspose.PSD
og_title: Automatické opravení orientace JPEG v Javě s Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to auto correct JPEG orientation in Java using Aspose.PSD.
    Enhance your image processing workflow with automatic EXIF‑based rotation.
  headline: Auto correct JPEG image orientation in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java is a powerful library that allows Java developers
      to work with PSD, JPEG, and other image formats programmatically.
    question: What is Aspose.PSD for Java?
  - answer: You can download the library from the [Aspose PSD Java release page](https://releases.aspose.com/psd/java/).
    question: How can I download Aspose.PSD for Java?
  - answer: Yes, it supports various image manipulation tasks such as resizing, cropping,
      and adjusting orientation.
    question: Does Aspose.PSD for Java support image manipulation?
  - answer: Comprehensive documentation is available on the [Aspose.PSD for Java documentation
      site](https://reference.aspose.com/psd/java/).
    question: Where can I find documentation for Aspose.PSD for Java?
  - answer: Yes, you can get a free trial from the [Aspose free trial page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java for free?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- auto correct jpeg
- Aspose.PSD
- Java image processing
title: Automatické opravení orientace JPEG obrázku v Javě
url: /cs/java/java-jpeg-image-processing/auto-correct-jpeg-image-orientation-java/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Automatické opravení orientace JPEG obrázku v Javě

## Úvod
V dnešní digitální éře se manipulace a optimalizace obrázků programově stala klíčovým úkolem pro vývojáře napříč různými oblastmi. **Auto correct JPEG orientation** je běžnou požadavkem při práci s fotografiemi pořízenými na různých zařízeních. Aspose.PSD pro Java vám poskytuje robustní nástroje pro efektivní práci s PSD, JPEG a dalšími formáty obrázků. Tento tutoriál se zaměřuje na konkrétní úkol: automatické opravení orientace JPEG obrázku pomocí Aspose.PSD pro Java. Ať už vytváříte aplikaci pro úpravu fotografií, spravujete obrazové zdroje v CMS, nebo automatizujete pipeline pro zpracování obrázků, naučíte se, jak tuto funkci bez problémů integrovat.

## Rychlé odpovědi
- **Co dělá automatické opravení orientace JPEG?** Přečte data o rotaci z EXIF a otočí obrázek tak, aby byl zobrazen vzpřímeně na jakémkoli zařízení.  
- **Která knihovna provádí rotaci?** Aspose.PSD pro Java poskytuje vestavěnou podporu EXIF a automatickou rotaci.  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro hodnocení; pro produkční nasazení je vyžadována komerční licence.  
- **Lze tímto zpracovat velké dávky?** Ano – můžete procházet složky a zpracovat tisíce obrázků s minimální zátěží paměti.  
- **Jaké verze Javy jsou podporovány?** Aspose.PSD funguje s JDK 8 až 21.

## Co je automatické opravení orientace JPEG obrázku?
Automatické opravení orientace JPEG je automatické rozpoznání EXIF tagu „Orientation“ v obrázku a následná rotace bitmapy tak, aby se zobrazovala vzpřímeně bez ručního zásahu. Tento proces čte metadata vložená v souboru JPEG, určuje potřebnou rotaci nebo převrácení a aplikuje transformaci, aby vizuální reprezentace odpovídala záměru fotografa na všech platformách pro prohlížení.

## Proč použít Aspose.PSD pro automatické opravení orientace JPEG obrázku?
Aspose.PSD podporuje **více než 30 formátů obrázků** a může zpracovávat soubory až do **2 GB** bez načítání celého obrázku do paměti, což poskytuje až **5× vyšší** výkon oproti ruční rotaci pixel po pixelu na srovnatelném hardwaru. Knihovna také pracuje s vloženými zdroji, jako jsou JPEG náhledy uvnitř PSD souborů, a poskytuje vysoceúrovňová API, která abstrahují nízkoúrovňové zpracování EXIF, což usnadňuje a zpřehledňuje implementaci.

## Předpoklady
- Java Development Environment: Ujistěte se, že máte na svém systému nainstalovaný Java Development Kit (JDK).  
- Aspose.PSD for Java JAR: Stáhněte knihovnu Aspose.PSD pro Java ze [stránky vydání Aspose PSD Java](https://releases.aspose.com/psd/java/).  
- Integrated Development Environment (IDE): Použijte IntelliJ IDEA, Eclipse nebo jakékoli IDE dle vašeho výběru pro vývoj v Javě.  
- Basic Understanding of Java and Image Processing: Znalost programování v Javě a základních konceptů zpracování obrázků bude užitečná.

## Import balíčků
Před zahájením příkladu se ujistěte, že importujete potřebné balíčky z Aspose.PSD pro Java. Třída `Image` je základním typem pro načítání a ukládání obrázků, zatímco `JpegExifData` poskytuje přístup k EXIF metadatům a třídy zdrojů miniatur představují vložené JPEG náhledy.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Jak automaticky opravit orientaci JPEG pomocí Aspose.PSD v Javě?
Načtěte cílový PSD soubor, najděte vložený JPEG miniaturu, nechte Aspose.PSD přečíst jeho EXIF orientaci, aplikujte automatickou rotaci a nakonec uložte opravený obrázek. Tento postup vyžaduje jen několik volání metod a funguje pro jakýkoli JPEG obrázek vložený v PSD kontejneru, což jej činí vhodným jak pro zpracování jedné obrázku, tak pro dávkové scénáře.

## Krok 1: Načtení PSD obrázku
Třída `PsdImage` představuje PSD soubor a poskytuje přístup k jeho zdrojům, včetně vložených JPEG miniatur.  
Nejprve načtěte PSD obrázek, který obsahuje JPEG miniaturu, jejíž orientace vyžaduje opravu:

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
Nahraďte `"Your Document Directory"` skutečnou cestou k adresáři, kde se nachází váš PSD soubor.

## Krok 2: Procházení zdrojů obrázku
Dále procházejte zdroje obrázku, abyste našli zdroj JPEG miniatury. `ThumbnailResource` a `Thumbnail4Resource` představují různé verze vložených JPEG náhledů v rámci PSD souboru.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Find thumbnail resource. Typically they are in the Jpeg file format.
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Adjust thumbnail data.
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null && exifData.getThumbnail() != null) {
            // If there is a thumbnail stored, auto-rotate it.
            PsdImage jpegImage = (PsdImage) exifData.getThumbnail();
            if (jpegImage != null) {
                jpegImage.autoRotate();
            }
        }
    }
}
```

## Krok 3: Uložení obrázku
Na závěr uložte opravený obrázek po aplikaci automatické rotace:

```java
image.save();
```
Tento krok zajišťuje, že provedené změny v obrázku jsou uloženy.

## Časté problémy a řešení
- **EXIF tag not detected** – Ujistěte se, že JPEG miniatura skutečně obsahuje tag Orientation; některé fotoaparáty jej vynechávají.  
- **Memory errors on large files** – Použijte `PsdImage.load(..., LoadOptions)` s `LoadOptions.setLoadAllResources(false)`, aby byl odběr paměti nízký.  
- **Incorrect rotation direction** – Ověřte, že používáte nejnovější verzi Aspose.PSD; starší verze měly známou chybu u některých hodnot orientace.

## Často kladené otázky

**Q: Co je Aspose.PSD pro Java?**  
A: Aspose.PSD pro Java je výkonná knihovna, která umožňuje vývojářům v Javě programově pracovat s PSD, JPEG a dalšími formáty obrázků.

**Q: Jak mohu stáhnout Aspose.PSD pro Java?**  
A: Knihovnu můžete stáhnout ze [stránky vydání Aspose PSD Java](https://releases.aspose.com/psd/java/).

**Q: Podporuje Aspose.PSD pro Java manipulaci s obrázky?**  
A: Ano, podporuje různé úlohy manipulace s obrázky, jako je změna velikosti, ořezávání a úprava orientace.

**Q: Kde mohu najít dokumentaci k Aspose.PSD pro Java?**  
A: Kompletní dokumentace je k dispozici na [webu dokumentace Aspose.PSD pro Java](https://reference.aspose.com/psd/java/).

**Q: Můžu si Aspose.PSD pro Java vyzkoušet zdarma?**  
A: Ano, můžete získat bezplatnou zkušební verzi na [stránce Aspose free trial](https://releases.aspose.com/).

**Q: Je funkce automatické rotace thread‑safe?**  
A: Ano, každá instance `PsdImage` může být zpracována v samostatném vlákně bez konfliktů sdíleného stavu.

**Q: Jak zvládnu dávkové zpracování tisíců obrázků?**  
A: Procházejte adresář, načtěte každý PSD, aplikujte kroky automatické rotace a uložte; knihovna znovu používá buffery, aby udržela nízkou spotřebu paměti.

## Závěr
Závěrem, použití Aspose.PSD pro Java poskytuje výkonné řešení pro automatické opravení orientace JPEG obrázků v rámci PSD souborů. Dodržením kroků popsaných v tomto tutoriálu můžete vylepšit své workflow pro zpracování obrázků a zajistit, že obrázky budou zobrazovány správně na všech platformách a zařízeních.

---

**Poslední aktualizace:** 2026-09-18  
**Testováno s:** Aspose.PSD for Java 24.11  
**Autor:** Aspose

## Související tutoriály

- [Zpracování JPEG obrázků v Javě](/psd/java/java-jpeg-image-processing/)
- [Převod PSD na JPEG a otočení o 270° pomocí Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/rotate-image/)
- [Jak otočit obrázek o konkrétní úhel pomocí Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}