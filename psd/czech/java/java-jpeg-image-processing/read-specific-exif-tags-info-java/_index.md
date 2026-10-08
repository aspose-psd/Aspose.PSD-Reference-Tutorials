---
date: 2026-10-08
description: Naučte se, jak číst EXIF tagy v Javě pomocí Aspose.PSD pro Java (asp)
  s naším krok‑za‑krokem návodem a zvyšte své schopnosti zpracování obrázků.
keywords:
- read exif tags java
- java exif tag extraction
- java image metadata extraction
lastmod: 2026-10-08
linktitle: Číst konkrétní informace o EXIF tagách v Javě
og_description: 'Čtení EXIF tagů: vývojáři Java mohou rychle získat metadata obrázků
  pomocí Aspose.PSD. Tento průvodce vás provede načtením PSD, vyhledáním miniatur
  a výpisem klíčových EXIF polí, jako jsou WhiteBalance a ISO speed.'
og_image_alt: Guide showing how to read EXIF tags from PSD files in Java using Aspose.PSD
og_title: Jak číst EXIF tagy v Javě s Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-08'
  description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  headline: How to read EXIF tags in Java with Aspose.PSD
  type: TechArticle
- description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  name: How to read EXIF tags in Java with Aspose.PSD
  steps:
  - name: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
    text: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
  - name: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
    text: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
  - name: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
    text: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
  type: HowTo
- questions:
  - answer: Aspose.PSD (asp)
    question: What library reads EXIF data from PSD in Java?
  - answer: WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength,
      and more.
    question: Which tags can be extracted?
  - answer: Yes, a commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: The same API supports PNG, JPEG, TIFF via Java image metadata extraction.
    question: Can I use this with other image formats?
  - answer: About 10‑15 minutes for a basic read‑only scenario.
    question: How long does implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- read exif tags java
- Aspose.PSD
- java image metadata extraction
- EXIF extraction
- PSD processing
title: Jak číst EXIF tagy v Javě s Aspose.PSD
url: /cs/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přečtěte si informace o konkrétních EXIF značkách v Javě s Aspose (asp)

## Úvod
Pokud potřebujete **číst EXIF značky v Javě**, Aspose.PSD (asp) nabízí čisté, čistě‑Java API, které funguje bez Photoshopu. V tomto tutoriálu se naučíte, jak extrahovat EXIF data z PSD obrázku, vybrat pouze značky, které vás zajímají, a vytisknout je do konzole. Pokryjeme vše od nastavení vývojového prostředí až po získání metadat, jako jsou WhiteBalance, ISO rychlost a ohnisková vzdálenost. Pojďme na to!

## Rychlé odpovědi
- **Jaká knihovna čte EXIF data z PSD v Javě?** Aspose.PSD (asp)  
- **Které značky lze extrahovat?** WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength a další.  
- **Potřebuji licenci pro produkci?** Ano, je vyžadována komerční licence; je k dispozici bezplatná zkušební verze.  
- **Mohu to použít s jinými formáty obrázků?** Stejné API podporuje PNG, JPEG, TIFF prostřednictvím Java extrakce metadat obrázku.  
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní scénář jen pro čtení.

## Co je asp (Aspose.PSD pro Javu)?
Aspose.PSD pro Javu je čistě‑Java knihovna, která vývojářům umožňuje pracovat se soubory Adobe Photoshop (PSD, PSB) bez instalace Photoshopu. Poskytuje programový přístup k vrstvám, zdrojům a metadatům — včetně EXIF značek — což ji činí ideální pro úkoly **java image metadata extraction**.

## Proč použít Aspose.PSD (asp) pro extrakci EXIF?
Můžete extrahovat EXIF značky v Javě pouhými dvěma voláními metod a knihovna zpracovává soubory až do 2 GB, aniž by načítala celý dokument do paměti. Podporuje **30+ formátů obrázků** a zachovává přesná nastavení fotoaparátu, což vám poskytuje deterministické výsledky napříč Windows, Linux a macOS prostředími.

## Prerequisites
Než se ponoříme do kódu, budete potřebovat následující:

1. **Java Development Kit (JDK):** Ujistěte se, že máte JDK nainstalovaný na svém počítači. Můžete jej stáhnout z [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java:** Stáhněte knihovnu ze [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
3. **Integrated Development Environment (IDE):** IDE jako IntelliJ IDEA, Eclipse nebo NetBeans vám usnadní psaní kódu.  
4. **PSD file:** PSD soubor s EXIF daty. Můžete použít ukázkový soubor poskytnutý v tomto tutoriálu nebo jakýkoli jiný PSD soubor s EXIF značkami.

## Importovat balíčky
Importujte požadované třídy Aspose.PSD, jako jsou Image, PsdImage, ThumbnailResource a JpegExifData, pro práci s PSD soubory.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Krok 1: načíst PSD obrázek
`Image.load()` načte soubor a vrátí objekt Image představující data obrázku.  
`PsdImage` je třída Aspose.PSD, která poskytuje funkce specifické pro PSD.  
Metoda `Image.load()` načte libovolný podporovaný soubor obrázku do paměti a vrátí obecný objekt `Image`, který můžete přetypovat na typ specifický pro PSD.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```

V tomto kroku načteme PSD soubor pomocí metody `Image.load()`. Třída `PsdImage` slouží k reprezentaci PSD obrázku a načtený obrázek přetypujeme na tuto třídu, abychom získali přístup k funkcím specifickým pro PSD.

## Krok 2: iterovat přes zdroje obrázku
`PsdImage.getResources()` vrací kolekci vložených zdrojů, jako jsou náhledy a EXIF data.  
Volání `PsdImage.getResources()` vrací kolekci všech vložených zdrojů. Iterací přes tuto kolekci můžete najít náhledové zdroje, které obsahují EXIF metadata.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Further processing will be done here
    }
}
```

Procházíme zdroje obrázku pomocí smyčky `for`. Cílem je identifikovat zdroje, které jsou instancemi `ThumbnailResource` nebo `Thumbnail4Resource`, protože právě tyto typy obsahují EXIF data.

## Krok 3: extrahovat EXIF data
`ThumbnailResource.getJpegOptions()` poskytuje přístup k JPEG možnostem včetně EXIF metadat.  
`JpegExifData` obsahuje jednotlivé hodnoty EXIF značek.  
Metoda `ThumbnailResource.getJpegOptions()` poskytuje přístup k objektu `JpegExifData`, který obsahuje jednotlivé EXIF značky jako WhiteBalance, ISOSpeed a FocalLength.  
```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
    if (exif != null) {
        System.out.println("Exif WhiteBalance: " + exif.getWhiteBalance());
        System.out.println("Exif PixelXDimension: " + exif.getPixelXDimension());
        System.out.println("Exif PixelYDimension: " + exif.getPixelYDimension());
        System.out.println("Exif ISOSpeed: " + exif.getISOSpeed());
        System.out.println("Exif FocalLength: " + exif.getFocalLength());
    }
}
```

Používáme podmínku `if` k ověření, zda je zdroj instancí `ThumbnailResource`. Pokud ano, přetypujeme jej a získáme jeho `JpegOptions` pro přístup k `ExifData`. Nakonec vytiskneme různé EXIF značky, jako jsou WhiteBalance, rozměry pixelů, ISOSpeed a FocalLength.

## Časté problémy a tipy
- **Null EXIF data:** Některé PSD soubory nemusí obsahovat náhledový zdroj s EXIF informacemi. Vždy před přístupem k hodnotám značek zkontrolujte, zda není `null`.  
- **Chyby cest k souborům:** Používejte absolutní cesty nebo se ujistěte, že pracovní adresář ukazuje na složku obsahující váš PSD soubor.  
- **Omezení licence:** Bezplatná zkušební verze omezuje počet stránek, které můžete zpracovat; pro neomezené použití upgradujte na plnou licenci.

## Často kladené otázky
### Co jsou EXIF data?
EXIF (Exchangeable Image File Format) data jsou metadata vložená do souborů obrázků, která obsahují informace jako nastavení fotoaparátu, datum a čas, a rozměry obrázku.

### Mohu upravovat EXIF data pomocí Aspose.PSD?
Ano, Aspose.PSD vám umožňuje číst i upravovat EXIF data. Můžete aktualizovat značky a uložit změny zpět do souboru obrázku.

### Je Aspose.PSD pro Javu zdarma?
Aspose.PSD nabízí bezplatnou zkušební verzi, kterou si můžete stáhnout ze [Aspose.PSD official releases page](https://releases.aspose.com/). Pro plné funkce je nutné zakoupit licenci.

### Jaké další formáty Aspose.PSD podporuje?
Aspose.PSD podporuje různé formáty Adobe Photoshop, včetně PSD, PSB a dalších. Poskytuje také možnosti konverze těchto formátů do PNG, JPEG, TIFF atd.

### Jak získám podporu pro Aspose.PSD?
Podporu můžete získat prostřednictvím Aspose.PSD [forum](https://forum.aspose.com/c/psd/34).

### Jak to pomáhá s **java image metadata extraction**?
Použitím objektu `JpegExifData` můžete programově získat jakoukoli EXIF značku, kterou potřebujete, což tvoří solidní základ pro širší úlohy extrakce metadat napříč různými formáty obrázků.

---

**Poslední aktualizace:** 2026-10-08  
**Testováno s:** Aspose.PSD for Java 24.11 (nejnovější v době psaní)  
**Autor:** Aspose

## Související tutoriály

- [Číst a upravovat JPEG Exif značky Java](/psd/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/)
- [Java JPEG zpracování obrázků](/psd/java/java-jpeg-image-processing/)
- [Jak otočit obrázek pod konkrétním úhlem s Aspose.PSD pro Javu](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}