---
date: 2026-07-08
description: 'Tutoriál k Java knihovně pro úpravu obrázků: naučte se, jak oříznout
  obrázek v Javě pomocí Aspose.PSD for Java, změnit velikost, rozšířit plátno a převést
  PSD na JPEG.'
keywords:
- java image editing library
- java image processing tutorial
- how to crop image java
lastmod: 2026-07-08
linktitle: Rozšířit a oříznout obrázky
og_description: Tutoriál k Java knihovně pro úpravu obrázků ukazuje, jak během několika
  minut oříznout, rozšířit plátno a převést PSD na JPEG pomocí Aspose.PSD for Java.
og_image_alt: 'Guide: Crop and expand images in Java with Aspose.PSD'
og_title: Java knihovna pro úpravu obrázků – Oříznutí obrázku pomocí Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: 'Java image editing library tutorial: learn how to crop image java
    using Aspose.PSD for Java, resize, expand canvas, and convert PSD to JPEG.'
  headline: Java Image Editing Library – Crop Image with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles crop image java?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `JpegOptions` together with a cropping rectangle.
    question: Can I convert PSD to JPEG while cropping?
  - answer: Aspose.PSD supports Java 8 and newer versions.
    question: Is Java 8 supported?
  - answer: Typically under 10 minutes for a basic crop operation.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image editing
- Aspose.PSD
- image cropping
- PSD to JPEG
title: Java knihovna pro úpravu obrázků – Oříznutí obrázku pomocí Aspose.PSD
url: /cs/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java knihovna pro úpravu obrázků: Oříznutí obrázku v Javě s Aspose.PSD

## Úvod

V tomto tutoriálu se naučíte, jak použít **java image editing library**—konkrétně Aspose.PSD pro Java—k oříznutí, rozšíření a konverzi souborů PSD do JPEG. Ať už připravujete aktiva pro webový portál nebo automatizujete generování miniatur, níže uvedené kroky vám poskytnou opakovatelný, produkčně připravený workflow, který můžete integrovat do jakéhokoli projektu Java 8+.

## Rychlé odpovědi
- **What library handles crop image java?** Aspose.PSD for Java.  
- **Do I need a license for development?** A free trial works for testing; a commercial license is required for production.  
- **Can I convert PSD to JPEG while cropping?** Yes, using `JpegOptions` together with a cropping rectangle.  
- **Is Java 8 supported?** Aspose.PSD supports Java 8 and newer versions.  
- **How long does the implementation take?** Typically under 10 minutes for a basic crop operation.

## Co je „crop image java“?

Oříznutí obrázku v Javě znamená výběr obdélníkové oblasti ze zdrojového obrázku a zahazování všeho mimo tuto oblast. S Aspose.PSD vytvoříte `Rectangle`, který oblast definuje, aplikujete jej na `RasterImage` a poté výsledek uložíte v libovolném podporovaném formátu, například JPEG.

## Proč použít Aspose.PSD pro oříznutí obrázků v Javě?

Aspose.PSD poskytuje **java image editing library**, která nativně pracuje se soubory PSD, podporuje více než 100 funkcí vrstev a dokáže zpracovat obrázky až do rozměrů 10 000 × 10 000 pixelů při využití paměti pod 500 MB. Nabízí také vestavěnou konverzi do JPEG, PNG, BMP a dalších formátů, bez potřeby externích nástrojů. To dělá hromadné zpracování rychlým, spolehlivým a snadno udržovatelným.

## Předpoklady

1. **Java Development Kit (JDK)** – Java 8 nebo novější nainstalována.  
2. **Aspose.PSD for Java** – stáhněte knihovnu z oficiální stránky **[here](https://releases.aspose.com/psd/java/)**.  

> **Pro tip:** Přidejte Aspose.PSD JAR do classpath vašeho projektu nebo do Maven/Gradle závislostí, aby nedošlo k `ClassNotFoundException`.

## Import balíčků

Přidejte požadované importy do vašeho Java zdrojového souboru. Tyto třídy vám umožní načítání obrázků, manipulaci s rastry, definování obdélníků a nastavení exportu JPEG.

## Jak oříznout obrázek v Javě pomocí Aspose.PSD?

Načtěte zdrojový PSD pomocí `RasterImage`, definujte `Rectangle`, který popisuje oblast oříznutí (záporné souřadnice mohou rozšířit plátno), a nakonec výsledek uložte pomocí `JpegOptions`. Tento tříkrokový tok zvládá jak oříznutí, tak konverzi formátu v jednom průchodu, čímž eliminuje potřebu mezilehlých souborů.

## Krok 1: Nastavte adresář dokumentu

Určete složku, která obsahuje zdrojový PSD soubor. Nahraďte zástupný text skutečnou cestou na vašem počítači.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Krok 2: Zadejte cesty ke zdroji a cíli

Definujte, odkud se má PSD načíst a kam se má uložit oříznutý JPEG.

```java
String dataDir = "Your Document Directory";
```

## Krok 3: Načtěte a cachujte obrázek

`RasterImage` představuje rasterizovanou verzi souboru PSD v paměti.  
Načtěte PSD do objektu `RasterImage`. Cachování zlepšuje výkon při následných operacích, jako je oříznutí.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Krok 4: Vytvořte obdélník pro oříznutí

`Rectangle` definuje souřadnice X, Y a šířku/výšku ořezové oblasti.  
Vytvořte `Rectangle`, který popisuje oblast, kterou chcete zachovat. Souřadnice mohou být záporné, aby **rozšířily** plátno před oříznutím, což je užitečné pro přidání okraje kolem původního obrázku.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

> **Why use negative coordinates?**  
> Negative X/Y values shift the crop area left/up, effectively adding empty space (expanding) around the original content before the final crop.

> **Proč použít záporné souřadnice?**  
> Záporné hodnoty X/Y posunou ořezovou oblast doleva/nahoru, čímž efektivně přidají prázdný prostor (rozšíření) kolem původního obsahu před finálním oříznutím.

## Krok 5: Uložte oříznutý obrázek

`JpegOptions` určuje nastavení výstupu JPEG, jako je kvalita a komprese.  
Nakonec uložte výsledný obrázek pomocí `JpegOptions`. Tento krok také ukazuje **convert psd jpeg** při aplikaci ořezového obdélníku.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Result:** `jpeg_out.jpg` now contains a 300 × 300 pixel image that has been expanded by 200 px on each side and then cropped to the defined rectangle.

> **Výsledek:** `jpeg_out.jpg` nyní obsahuje obrázek o rozměrech 300 × 300 pixelů, který byl rozšířen o 200 px na každé straně a poté oříznut na definovaný obdélník.

Gratulujeme! Úspěšně jste provedli **java image cropping**, rozšířili plátno a převedli soubor PSD do JPEG—vše v několika stručných řádcích kódu.

## Běžné případy použití

- **Preparing assets for web** – ořízněte a změňte velikost snímků obrazovky nebo návrhů před nahráním.  
- **Generating thumbnails** – extrahujte konkrétní oblast z velkého PSD pro náhledové účely.  
- **Automated batch processing** – projděte složku se soubory PSD a aplikujte stejný ořezový obdélník na každý.

## Řešení problémů a tipy

| Problém | Navrhované řešení |
|-------|----------------|
| `OutOfMemoryError` při načítání velkých PSD souborů | Zavolejte `rasterImage.cacheData()` brzy a zvažte zvýšení velikosti haldy JVM (`-Xmx`). |
| Oříznutá oblast je mimo střed | Zkontrolujte posuny X/Y obdélníku; pamatujte, že záporné hodnoty rozšiřují plátno. |
| Výstupní JPEG vypadá rozmazaně | Upravte nastavení kvality v `JpegOptions` (např. `new JpegOptions { Quality = 90 }`). |

## Často kladené otázky

### Q1: Je Aspose.PSD kompatibilní s různými verzemi Javy?

A1: Ano, Aspose.PSD podporuje Java 8, 11, 17 a novější verze, což zajišťuje širokou kompatibilitu napříč vývojovými prostředími.

### Q2: Mohu použít Aspose.PSD pro komerční projekty?

A2: Rozhodně, Aspose.PSD poskytuje komerční licence pro vývojáře, což umožňuje jeho použití jak v osobních, tak komerčních aplikacích.

### Q3: Existují nějaká omezení podporovaných formátů souborů obrázků?

A3: Aspose.PSD podporuje více než 30 formátů obrázků, včetně PSD, JPEG, PNG, BMP, TIFF a dalších. Kompletní seznam najdete v [dokumentaci](https://reference.aspose.com/psd/java/).

### Q4: Jak mohu získat podporu pro dotazy související s Aspose.PSD?

A4: Navštivte [Aspose.PSD fórum](https://forum.aspose.com/c/psd/34), kde můžete získat pomoc od komunity nebo týmu podpory Aspose.

### Q5: Je k dispozici bezplatná zkušební verze?

A5: Ano, můžete si vyzkoušet Aspose.PSD s bezplatnou zkušební verzí. Stáhněte ji [here](https://releases.aspose.com/).

---

**Poslední aktualizace:** 2026-07-08  
**Testováno s:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

## Související tutoriály

- [Jednoduché změny velikosti s Aspose.PSD – Java knihovna pro manipulaci s obrázky](/psd/java/basic-image-operations/simple-resizing/)
- [Jak otočit obrázek o 270 stupňů s Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/rotate-image/)
- [Jak upravit gama v Java zpracování obrázků s Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}