---
date: 2026-05-19
description: Naučte se, jak převést PSD na JPEG a otočit obrázek o 270 stupňů pomocí
  Aspose.PSD pro Java. Tento průvodce ukazuje, jak otáčet soubory PSD, převracet obrázky
  a převádět PSD na JPEG.
keywords:
- convert psd to jpeg
- how to rotate psd
- flip image java
- rotate psd layer
- rotate image without photoshop
linktitle: Otočit obrázek o 270 stupňů
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  headline: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  name: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  steps:
  - name: Load the PSD File
    text: '`Image` is Aspose.PSD''s core class that represents a single PSD document
      in memory. Instantiating it reads only the header information, keeping memory
      usage low.'
  - name: Rotate the Image 270 Degrees
    text: '`rotateFlip` performs the specified rotation and optional flip on the image.
      `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise
      while leaving the image orientation unchanged. > **Pro tip:** If you also need
      to flip the image horizontally or vertically, choose a different `Ro'
  - name: Convert PSD to JPEG and Save
    text: '`JpegOptions` defines JPEG‑specific parameters such as compression quality.
      The `save` method writes the transformed image to disk in the desired format.
      The file `RotatedImage_out.jpg` now contains the original PSD content rotated
      270 degrees and saved as a JPEG.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other
      raster formats.
    question: Is Aspose.PSD compatible with different image formats?
  - answer: Absolutely! While `RotateFlipType` provides common angles, you can chain
      multiple calls or use transformation matrices for arbitrary angles.
    question: Can I apply custom rotations, not just predefined flips?
  - answer: Replace `JpegOptions` with `PngOptions` (or the appropriate options class)
      in the `save` method.
    question: How do I convert the rotated PSD to another format, such as PNG?
  - answer: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).
    question: Where can I find additional support or assistance?
  - answer: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Převod PSD na JPEG a otočení o 270° pomocí Aspose.PSD pro Java
url: /cs/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Převod PSD na JPEG a otočení obrázku o 270 stupňů pomocí Aspose.PSD pro Java

## Úvod

V tomto **Java tutoriálu pro zpracování obrázků** se naučíte, jak **převést PSD na JPEG** a zároveň otočit obrázek 270 stupňů pomocí Aspose.PSD pro Java. Ať už vytváříte dávkový zpracovatelský řetězec, webový editor nebo desktopovou utilitu, knihovna vám umožní manipulovat s vrstvami PSD bez Photoshopu. Také se podíváme na volitelné převracení a ukážeme kompletní tok od načtení souboru PSD až po uložení JPEG.

## Rychlé odpovědi
- **Jaká knihovna provádí otáčení?** Aspose.PSD for Java  
- **Jaký úhel otáčení příklad používá?** 270 stupňů  
- **Mohu také obrázek převrátit?** Ano – použijte možnosti `RotateFlipType` jako `Rotate90FlipX`  
- **Jak výsledek uložit?** V příkladu ukládáme jako JPEG pomocí `JpegOptions`  
- **Potřebuji licenci pro produkci?** Pro komerční použití je vyžadována platná licence Aspose.PSD  

## Co znamená „otočit obrázek o 270 stupňů“?

Otáčení obrázku o 270 stupňů znamená otočit obrázek o tři čtvrtiny úplného kruhu po směru hodinových ručiček (nebo o 90 stupňů proti směru hodinových ručiček). Tento orientační směr často obnovuje původní portrétní rozložení po předchozích transformacích a běžně se používá, když byly obrázky pořízeny v režimu na šířku, ale je potřeba je zobrazit na výšku. Výsledkem je správně orientovaný vizuál bez ztráty kvality.

## Proč použít Aspose.PSD pro tento úkol?

Aspose.PSD podporuje **více než 50 vstupních a výstupních formátů** – včetně PSD, JPEG, PNG, BMP, GIF a TIFF – a dokáže zpracovat soubory až do **2 GB** bez načítání celého dokumentu do paměti. API funguje na jakémkoli Java runtime (JDK 8+), nevyžaduje žádnou nativní instalaci Photoshopu a poskytuje jediný volání `rotateFlip`, které zvládne jak otáčení, tak převracení v jednom kroku.

## Předpoklady

Než začnete, ujistěte se, že máte:

- Nainstalovanou knihovnu **Aspose.PSD for Java**. Můžete si ji stáhnout a zobrazit úplnou referenci API [zde](https://reference.aspose.com/psd/java/).  
- Vývojové prostředí Java (JDK 8 nebo vyšší).  
- Vzorek souboru PSD, který chcete otočit. Aktualizujte proměnnou `sourceFile` v kódu na správnou cestu k vašemu souboru.

## Import balíčků

třídy `Image`, `RotateFlipType` a `JpegOptions` jsou vyžadovány pro načtení, transformaci a uložení souboru.  
`Image` je základní třída představující PSD dokument v paměti.  
`RotateFlipType` vyjmenovává podporované operace otáčení a převracení.  
`JpegOptions` konfiguruje nastavení výstupu JPEG, jako je kvalita.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Jak převést PSD na JPEG po otočení?

Nahrajte zdrojový PSD, aplikujte otáčení o 270 stupňů a okamžitě jej uložte jako JPEG. Tento tříkrokový proces běží za méně než sekundu pro typické 10‑MP obrázky na moderním CPU, což jej činí ideálním pro vysoce výkonné dávkové úlohy. Zpracováním pouze potřebných dat obrázku zůstává spotřeba paměti nízká a výsledný JPEG si zachovává vizuální věrnost při snížení velikosti souboru.

### Krok 1: Načtení souboru PSD

`Image` je základní třída Aspose.PSD, která v paměti představuje jediný PSD dokument. Jeho vytvoření načte pouze informace z hlavičky, což udržuje nízkou spotřebu paměti.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### Krok 2: Otočení obrázku o 270 stupňů

`rotateFlip` provádí zadané otáčení a volitelné převracení obrázku. `RotateFlipType.Rotate270FlipNone` otočí plátno o 270 stupňů po směru hodinových ručiček a zachová orientaci obrázku beze změny.

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Tip:** Pokud také potřebujete obrázek převrátit horizontálně nebo vertikálně, vyberte jiný `RotateFlipType`, například `Rotate90FlipX` nebo `Rotate180FlipY`.

### Krok 3: Převod PSD na JPEG a uložení

`JpegOptions` definuje parametry specifické pro JPEG, jako je kvalita komprese. Metoda `save` zapíše transformovaný obrázek na disk v požadovaném formátu.

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

Soubor `RotatedImage_out.jpg` nyní obsahuje původní obsah PSD otočený o 270 stupňů a uložený jako JPEG.

## Časté problémy a řešení

| Problém | Řešení |
|-------|----------|
| **Obrázek se zobrazuje vzhůru nohama** | Ověřte, že jste použili `Rotate270FlipNone`. Pro otáčení o 90 stupňů po směru hodinových ručiček použijte `Rotate90FlipNone`. |
| **Výstupní soubor je poškozen** | Ujistěte se, že cílová složka existuje a máte oprávnění k zápisu. |
| **Výjimka licence** | Nainstalujte dočasnou nebo trvalou licenci Aspose.PSD před načtením obrázku v produkci. |

## Často kladené otázky

**Q: Je Aspose.PSD kompatibilní s různými formáty obrázků?**  
A: Ano, Aspose.PSD podporuje PSD, JPEG, PNG, BMP, GIF, TIFF a mnoho dalších rastrových formátů.

**Q: Mohu použít vlastní otáčení, nejen předdefinované převrácení?**  
A: Rozhodně! Zatímco `RotateFlipType` poskytuje běžné úhly, můžete řetězit více volání nebo použít transformační matice pro libovolné úhly.

**Q: Jak převést otočený PSD do jiného formátu, například PNG?**  
A: V metodě `save` nahraďte `JpegOptions` třídou `PngOptions` (nebo příslušnou třídou možností).

**Q: Kde mohu najít další podporu nebo pomoc?**  
A: Pro komunitní pomoc navštivte [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Je k dispozici bezplatná zkušební verze?**  
A: Ano, můžete si vyzkoušet Aspose.PSD pomocí [bezplatné zkušební verze](https://releases.aspose.com/).

**Q: Jak získat dočasnou licenci?**  
A: Pokud potřebujete dočasnou licenci, můžete ji získat [zde](https://purchase.aspose.com/temporary-license/).

---

**Poslední aktualizace:** 2026-05-19  
**Testováno s:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Převod PSD na rastrové formáty obrázků pomocí Aspose.PSD pro Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Převod PSD na PNG a otočení vrstev v souborech PSD pomocí Java](/psd/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/)
- [Jak otočit obrázek v Java pomocí Aspose.PSD](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}