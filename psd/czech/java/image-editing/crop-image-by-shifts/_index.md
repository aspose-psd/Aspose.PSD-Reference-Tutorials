---
date: 2026-07-03
description: Naučte se, jak oříznout obrázek v Javě pomocí Aspose.PSD pro Java. Tento
  podrobný návod na oříznutí obrázku krok za krokem zahrnuje načítání souborů PSD,
  nastavení hodnot posunu a uložení výsledku.
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: Oříznutí obrázku posunutím
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Oříznutí obrázku v Javě posunutím s Aspose.PSD
url: /cs/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Oříznutí obrázku v Javě posuny s Aspose.PSD

## Úvod

V Java zpracování obrázků je **crop image java** běžnou požadavkou pro přípravu grafiky, miniatur nebo UI aktiv. Aspose.PSD pro Java usnadňuje tento úkol tím, že poskytuje jednoduchou metodu `crop`, která funguje na jakémkoli podporovaném rastrovém formátu. V tomto tutoriálu se naučíte, jak načíst soubor PSD, definovat posuny vlevo‑vpravo‑nahoru‑dolů, aplikovat oříznutí a uložit výsledek — vše bez psaní vlastního kódu pro manipulaci s pixely.

## Rychlé odpovědi
- **Která knihovna provádí oříznutí?** Aspose.PSD for Java provides a built‑in `crop` method.  
- **Potřebuji licenci?** A temporary license works for evaluation; a full license is required for production.  
- **Podporované formáty?** Over 30 raster formats, including PSD, JPEG, PNG, BMP, and TIFF.  
- **Maximální velikost souboru?** Handles files up to 2 GB without loading the entire image into memory.  
- **Kolik řádků kódu?** Only five logical steps—load, cache, define shifts, crop, and save.

## Co je crop image java?
`crop image java` odkazuje na operaci oříznutí bitmapy v Java aplikaci. Pomocí Aspose.PSD je operace prováděna metodou `crop`, která přijímá hodnoty posunu pro každou stranu obrázku a vrací novou instanci obrázku.

## Proč použít Aspose.PSD pro oříznutí obrázku?
Aspose.PSD podporuje **30+** formátů obrázků a dokáže zpracovat více než stovky stránek PSD souborů při využití méně než 150 MB RAM díky své lazy‑loading architektuře. Knihovna také zaručuje pixel‑dokonalé výsledky, zachovává vrstvy, masky a barevné profily — něco, co mnoho obecných knihoven pro obrázky nemůže zaručit.

## Požadavky

### Java Development Kit (JDK)

Ujistěte se, že máte nainstalovanou nejnovější verzi JDK na svém systému. Můžete si ji stáhnout [zde](https://www.oracle.com/java/technologies/javase-downloads.html).

### Aspose.PSD pro Java knihovna

Nejprve musíte získat knihovnu Aspose.PSD pro Java. Navštivte [stránku ke stažení](https://releases.aspose.com/psd/java/) a stáhněte nejnovější verzi.

### Integrované vývojové prostředí (IDE)

Vyberte si své oblíbené Java IDE, například Eclipse nebo IntelliJ, pro plynulý vývoj.

## Jak oříznout obrázek v Javě?

Načtěte svůj zdrojový soubor, definujte posuny pixelů pro každou stranu a zavolejte metodu `crop` — celý tento postup lze zapsat v pěti stručných řádcích kódu. Operace `crop` vytvoří nový obrázek, který obsahuje pouze oblast, kterou jste určili, a původní soubor zůstane nedotčen.

### Krok 1: Načtení obrázku

`Image` je základní třída pro všechny typy obrázků v Aspose.PSD.  
`RasterImage` představuje rastrový obrázek a poskytuje možnosti oříznutí.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Krok 2: Uložení dat obrázku do mezipaměti

`cacheData()` načte data obrázku do paměti pro rychlejší zpracování.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### Krok 3: Definice hodnot posunu

Zadejte hodnoty posunu pro všechny čtyři strany obrázku (levá, horní, pravá, dolní) v pixelech.  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### Krok 4: Aplikace oříznutí

`crop(left, right, top, bottom)` ořízne obrázek podle zadaných posunů pixelů na každé straně.  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### Krok 5: Uložení výsledků

`JpegOptions` definuje nastavení JPEG kódování, jako je kvalita a barevný profil.  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

Gratuluji! Úspěšně jste ořízli obrázek pomocí Aspose.PSD pro Java.

## Časté problémy a řešení

- **Obrázek se nezměnil:** Ověřte, že hodnoty posunu jsou kladné a nepřekračují původní rozměry.  
- **OutOfMemoryError u velkých souborů:** Povolením cache, jak je ukázáno v kroku 2, přinutíte Aspose.PSD použít dočasný soubor místo udržování celého obrázku v RAM.  
- **Posun barev po oříznutí:** Zajistěte zachování barevného profilu voláním `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })`, pokud potřebujete přesnou věrnost barev.

## Často kladené otázky

**Q: Je Aspose.PSD kompatibilní se všemi formáty obrázků?**  
A: Ano, Aspose.PSD podporuje více než 30 rastrových formátů, včetně PSD, JPEG, PNG, BMP, TIFF a GIF, což zajišťuje širokou kompatibilitu.

**Q: Mohu na stejný obrázek aplikovat více oříznutí?**  
A: Ano. Po každém volání `crop` získáte nový objekt obrázku, který můžete podle potřeby znovu oříznout.

**Q: Existuje komunitní fórum pro podporu Aspose.PSD?**  
A: Ano, podporu a komunitu najdete na [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Jak mohu získat dočasnou licenci pro Aspose.PSD?**  
A: Navštivte [zde](https://purchase.aspose.com/temporary-license/) a získejte dočasnou licenci.

**Q: Existují ukázkové projekty představující funkce Aspose.PSD?**  
A: Prozkoumejte dokumentaci a příklady na [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).

---

**Poslední aktualizace:** 2026-07-03  
**Testováno s:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## Související tutoriály

- [Oříznutí obrázku obdélníkem v Aspose.PSD pro Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Oříznutí obrázku v Javě – Rozšíření a oříznutí obrázků s Aspose.PSD pro Java](/psd/java/image-editing/expand-and-crop-images/)
- [Změna velikosti obrázku v Javě – Použití výčtu Resize Type v Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}