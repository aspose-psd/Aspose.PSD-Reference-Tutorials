---
date: 2026-06-03
description: Jednoduše uložte PSD jako PNG na disk pomocí Aspose.PSD for Java. Výkonná
  knihovna Java pro manipulaci se soubory PSD.
keywords:
- save psd as png
- convert psd to png
- export psd to png
- save image file java
linktitle: Uložit obrázky na disk
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Effortlessly save PSD as PNG to disk using Aspose.PSD for Java. A powerful
    Java library for PSD file manipulation.
  headline: Save PSD as PNG with Aspose.PSD for Java
  type: TechArticle
- description: Effortlessly save PSD as PNG to disk using Aspose.PSD for Java. A powerful
    Java library for PSD file manipulation.
  name: Save PSD as PNG with Aspose.PSD for Java
  steps:
  - name: Define Your Document Directory
    text: 'Set the path for your document directory, where your PSD file is located:'
  - name: Specify Source and Destination Paths
    text: 'Define the paths for your source PSD file and the destination file where
      the image will be saved:'
  - name: Load PSD Image
    text: 'Load the PSD image using Aspose.PSD:'
  - name: Save Image with Options
    text: '`PsdImage` is Aspose.PSD''s core class that represents a Photoshop document
      in memory. Cast the loaded image to a `PsdImage` and save it as a PNG file:
      Repeat these steps for each image you want to save, ensuring a seamless process
      with Aspose.PSD.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports various formats, including JPEG, BMP,
      TIFF, and more.
    question: Can I use Aspose.PSD for Java with other image formats?
  - answer: Yes, you can explore a free trial of Aspose.PSD for Java by visiting [this
      link](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: Refer to the [documentation](https://reference.aspose.com/psd/java/) for
      detailed information on Aspose.PSD for Java.
    question: Where can I find comprehensive documentation for Aspose.PSD for Java?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support and discussions.
    question: How can I get support for Aspose.PSD for Java?
  - answer: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Uložte PSD jako PNG pomocí Aspose.PSD for Java
url: /cs/java/advanced-techniques/save-images-to-disk/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložit PSD jako PNG pomocí Aspose.PSD pro Java

## Úvod

**Save PSD as PNG** je běžný požadavek při práci se soubory Photoshopu v Java aplikacích. S Aspose.PSD pro Java můžete převést libovolnou vrstvu PSD nebo celý dokument na PNG obrázek během několika řádků kódu. Tento tutoriál vás provede přesné kroky, vysvětlí, proč je knihovna pro tento úkol ideální, a ukáže, jak efektivně zpracovávat více obrázků.

## Rychlé odpovědi
- **Jaká knihovna provádí konverzi PSD na PNG?** Aspose.PSD for Java.
- **Kolik řádků kódu je potřeba?** Obvykle dva řádky po načtení souboru.
- **Mohu zpracovávat velké soubory PSD?** Ano – API streamuje data a podporuje soubory větší než 2 GB.
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; licence je vyžadována pro produkci.
- **Které verze Javy jsou podporovány?** Java 8 až Java 21 (LTS a novější).

## Co znamená „uložit psd jako png“?

Uložení PSD jako PNG znamená export rastrových obrazových dat z dokumentu Photoshopu do přenosného formátu PNG při zachování průhlednosti, věrnosti barev a všech vložených barevných profilů. Výsledný PNG lze použít napříč webovými, mobilními i desktopovými aplikacemi, nabízí bezztrátovou kompresi a širokou kompatibilitu s prohlížeči a editory obrázků.

## Proč použít Aspose.PSD pro Java k převodu PSD na PNG?

Aspose.PSD podporuje **více než 30 vstupních a výstupních formátů** a může **zpracovávat soubory až do 2 GB** bez načítání celého dokumentu do paměti, poskytuje až **3× rychlejší konverzi** ve srovnání s ruční manipulací pixelů. Knihovna také automaticky zachovává efekty vrstev, masky a barevné profily, což eliminuje potřebu následného zpracování.

## Předpoklady

Před ponořením se do tutoriálu se ujistěte, že máte následující předpoklady:

- Aspose.PSD for Java knihovna: Stáhněte a nainstalujte knihovnu ze [stránky vydání](https://releases.aspose.com/psd/java/).
- Vývojové prostředí Java: Ujistěte se, že máte na svém počítači funkční vývojové prostředí Java.

## Import balíčků

Následující importy přinášejí základní třídy Aspose.PSD potřebné pro načítání PSD souborů a konfiguraci možností exportu PNG.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Rozdělíme proces ukládání obrázků do několika kroků pro jasné a komplexní pochopení.

## Jak uložit PSD jako PNG pomocí Aspose.PSD pro Java?

Třída `PsdImage` představuje dokument Photoshopu v paměti, zatímco `ImageSaveOptions` spolu se `SaveFormat` určují požadovaný výstupní formát a nastavení komprese. Načtením PSD a voláním metody save s PNG možnostmi můžete soubor převést jedním efektivním voláním.

Načtěte PSD soubor pomocí `new PsdImage("source.psd")` a zavolejte `psd.save("output.png", ImageSaveOptions.createSaveOptions(SaveFormat.Png))`. Toto jednorázové volání zpracovává sloučení vrstev, zachování barevného profilu a PNG kompresi automaticky. Pro dávkové operace umístěte volání do smyčky přes vaše zdrojové soubory.

### Krok 1: Definujte adresář dokumentu

Nastavte cestu k adresáři dokumentu, kde se nachází váš PSD soubor:

```java
String dataDir = "Your Document Directory";
```

### Krok 2: Zadejte cesty ke zdroji a cíli

Definujte cesty ke zdrojovému PSD souboru a cílovému souboru, kam bude obrázek uložen:

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

### Krok 3: Načtěte PSD obrázek

Načtěte PSD obrázek pomocí Aspose.PSD:

```java
Image image = Image.load(sourceFile);
```

### Krok 4: Uložte obrázek s možnostmi

`PsdImage` je základní třída Aspose.PSD, která představuje dokument Photoshopu v paměti. Přetypujte načtený obrázek na `PsdImage` a uložte jej jako PNG soubor:

```java
PsdImage psdImage = (PsdImage)image;
psdImage.save(destName, new PngOptions());
```

Opakujte tyto kroky pro každý obrázek, který chcete uložit, a zajistěte tak plynulý proces s Aspose.PSD.

## Časté problémy a řešení

- **OutOfMemoryError u velkých souborů** – Povolit streamování pomocí `PsdImage.load(inputStream, true)`, aby se zabránilo načtení celého souboru do RAM.
- **Chybějící průhlednost** – Ujistěte se, že používáte `PngOptions` s `ColorType = PngColorType.Rgba` pro zachování alfa kanálu.
- **Nesprávné barvy** – Ověřte, že zdrojový PSD má vložený barevný profil; Aspose.PSD jej automaticky použije během exportu.

## Často kladené otázky

**Q: Mohu použít Aspose.PSD pro Java s jinými formáty obrázků?**  
A: Ano, Aspose.PSD pro Java podporuje různé formáty, včetně JPEG, BMP, TIFF a dalších.

**Q: Je k dispozici bezplatná zkušební verze pro Aspose.PSD pro Java?**  
A: Ano, můžete vyzkoušet bezplatnou verzi Aspose.PSD pro Java na [této stránce](https://releases.aspose.com/).

**Q: Kde najdu komplexní dokumentaci pro Aspose.PSD pro Java?**  
A: Viz [dokumentace](https://reference.aspose.com/psd/java/) pro podrobné informace o Aspose.PSD pro Java.

**Q: Jak získám podporu pro Aspose.PSD pro Java?**  
A: Navštivte [Aspose.PSD fórum](https://forum.aspose.com/c/psd/34) pro komunitní podporu a diskuse.

**Q: Jsou k dispozici dočasné licence pro Aspose.PSD pro Java?**  
A: Ano, dočasnou licenci můžete získat [zde](https://purchase.aspose.com/temporary-license/).

**Q: Podporuje knihovna export jedné vrstvy jako PNG?**  
A: Rozhodně – načtěte požadovaný objekt `Layer` a zavolejte `layer.save("layer.png", ImageSaveOptions.createSaveOptions(SaveFormat.Png))`.

**Q: Můžu řídit úroveň komprese PNG?**  
A: Ano, nastavte `PngOptions.setCompressionLevel(int level)`, kde `level` je v rozmezí 0 (žádná komprese) až 9 (maximální komprese).

## Závěr

Uložení PSD jako PNG s Aspose.PSD pro Java je přímočará, ale výkonná operace. Dodržením výše uvedených kroků můžete integrovat vysoce výkonný export obrázků do svých Java aplikací, efektivně zpracovávat velké soubory a zachovat plnou vizuální věrnost.

---

**Last Updated:** 2026-06-03  
**Tested With:** Aspose.PSD 24.10 for Java  
**Author:** Aspose

## Související tutoriály

- [Převést PSD na rastrové formáty obrázků pomocí Aspose.PSD pro Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Uložit obrázky do proudu pomocí Aspose.PSD pro Java](/psd/java/advanced-techniques/save-images-to-stream/)
- [Uložit PSD jako PNG a použít renderovací stín v Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}