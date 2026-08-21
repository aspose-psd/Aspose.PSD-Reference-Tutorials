---
date: 2026-06-28
description: Zjistěte, jak kombinovat obrázky v Java pomocí Aspose.PSD, sloučit dva
  obrázky do PSD canvas a během několika minut vytvořit layered file.
keywords:
- combine images java
- java graphics draw image
- merge images into psd
linktitle: Kombinovat obrázky
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to combine images java using Aspose.PSD, merge two pictures
    into a PSD canvas, and generate a layered file in just minutes.
  headline: Combine Images Java – Create PSD File by Merging Pictures with Aspose.PSD
  type: TechArticle
- description: Learn how to combine images java using Aspose.PSD, merge two pictures
    into a PSD canvas, and generate a layered file in just minutes.
  name: Combine Images Java – Create PSD File by Merging Pictures with Aspose.PSD
  steps:
  - name: Create PSD Options (prepare the file)
    text: '`PsdOptions` holds the configuration for the output PSD, such as compression
      level and color depth.'
  - name: Set the FileCreateSource (define where the PSD will be saved)
    text: '`FileCreateSource` tells Aspose where to write the generated file.'
  - name: Create Image Instance (initialize canvas size)
    text: The `Image` constructor creates a blank PSD canvas with the dimensions you
      specify.
  - name: Initialize Graphics and draw the first picture
    text: '`Graphics` provides drawing capabilities on the canvas. We clear the background
      to white and render the first source image on the left half.'
  - name: Draw the second picture (complete the combine)
    text: Now we place the second image on the right half of the same canvas, creating
      a second layer automatically.
  - name: Save the resulting PSD file
    text: Persist the combined canvas to disk. The resulting `combined.psd` contains
      two editable layers. Congratulations! You have successfully **combine images
      java** and generated a layered PSD file ready for further Photoshop editing.
  type: HowTo
- questions:
  - answer: Aspose.PSD natively reads and writes **15+ formats**, including PSD, PNG,
      JPEG, BMP, TIFF, GIF, and more, making it a versatile choice for image pipelines.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Yes. Each `drawImage` call creates a separate PSD layer, which you can
      later reposition, apply filters, or mask using Aspose.PSD’s extensive layer‑editing
      API.
    question: Can I perform additional edits after combining images?
  - answer: A valid license is required for production use. You can obtain one from
      the Aspose store; a free trial is available for evaluation.
    question: Do I need a commercial license for production?
  - answer: Simply repeat `graphics.drawImage(...)` with appropriate coordinates for
      each additional image. Each call adds a new layer.
    question: How do I add more than two pictures?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support, or consult the official documentation linked in the download page.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Kombinace obrázků v Java – Vytvoření souboru PSD sloučením obrázků pomocí Aspose.PSD
url: /cs/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kombinace obrázků Java – Vytvoření souboru PSD sloučením obrázků pomocí Aspose.PSD

## Úvod

Pokud potřebujete **combine images java** sloučením několika obrázků do jediného souboru kompatibilního s Photoshopem, Aspose.PSD pro Java proces značně usnadňuje. V tomto tutoriálu vás provedeme vytvořením PSD plátna o rozměrech 600 × 600 pixelů, vykreslením dvou zdrojových obrázků vedle sebe a uložením výsledku jako vrstveného souboru PSD. Na konci pochopíte, proč je tato technika cenná pro automatizované grafické pipeline a jak ji rozšířit na libovolný počet obrázků.

## Rychlé odpovědi
- **Jaká knihovna je nejlepší pro sloučení obrázků do PSD?** Aspose.PSD for Java.
- **Jak dlouho trvá základní sloučení?** Přibližně 10‑15 minut na napsání a spuštění kódu.
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze stačí pro hodnocení; pro produkční nasazení je vyžadována komerční licence.
- **Mohu přidat více než dva obrázky?** Rozhodně – stačí opakovat volání `drawImage` pro každou další vrstvu.
- **Které verze Javy jsou podporovány?** Java 8 a novější (až do Java 21).

## Co je combine images java?
*Combine images java* označuje programové sloučení více rastrových obrázků do jediného souboru pomocí Java API. Aspose.PSD poskytuje vysoce úrovňový, čistě Java způsob, jak to provést bez nativních závislostí na Photoshopu, což vám umožní automatizovat kompozici, zachovat vrstvy a vytvořit PSD kompatibilní s Photoshopem, který lze později upravovat v Photoshopu nebo jiných nástrojích podporujících PSD.

## Proč kombinovat obrázky pomocí Aspose.PSD?

Aspose.PSD podporuje **15+ formátů obrázků** (včetně PSD, PNG, JPEG, BMP, TIFF, GIF a dalších) a dokáže zpracovat **více‑stovkové dokumenty** bez načítání celého souboru do paměti díky své streamovací architektuře. Knihovna je **100 % spravovaná Java**, takže běží na jakémkoli OS, který podporuje JDK, a eliminuje problémy s nativními DLL.

## Požadavky

1. **Aspose.PSD Library** – stáhněte ji z [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit (JDK)** – vyžaduje se Java 8+; Java 11 nebo novější je doporučena pro lepší výkon.  
3. **Working Directory** – složka ve vašem počítači, která obsahuje zdrojové obrázky (`example1.png`, `example2.png`) a kam bude zapsán výstupní PSD (`combined.psd`).  
4. **License Purchase** – získejte komerční licenci [here](https://purchase.aspose.com/buy) pro produkční použití.  
5. **Other Aspose Releases** – prozkoumejte další produkty a aktualizace [here](https://releases.aspose.com/).

## Import balíčků

Příkazy `import` přinášejí do rozsahu nezbytné třídy Aspose.PSD.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdOptions;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.PsdImageLayer;
import com.aspose.psd.imageoptions.FileCreateSource;
import com.aspose.psd.graphics.Graphics;
import com.aspose.psd.Color;
```

## Jak kombinovat images java pomocí Aspose.PSD?

Načtěte prázdné plátno, vykreslete na něj každý obrázek a poté uložte výsledek jako soubor PSD – to je celý pracovní postup ve třech stručných krocích. API automaticky vytvoří samostatnou vrstvu pro každé volání `drawImage`, což vám později v Photoshopu poskytne plnou editovatelnost.

### Krok 1: Vytvoření PSD Options (příprava souboru)

`PsdOptions` obsahuje konfiguraci výstupního PSD, jako je úroveň komprese a barevná hloubka.

```java
PsdOptions psdOptions = new PsdOptions();
```

### Krok 2: Nastavení FileCreateSource (definice místa uložení PSD)

`FileCreateSource` říká Aspose, kam má zapisovat vygenerovaný soubor.

```java
psdOptions.setSource(new FileCreateSource(dataDir + "combined.psd", false));
```

### Krok 3: Vytvoření instance Image (inicializace velikosti plátna)

Konstruktor `Image` vytvoří prázdné PSD plátno s rozměry, které zadáte.

```java
Image image = new Image(psdOptions, 600, 600);
```

### Krok 4: Inicializace Graphics a vykreslení prvního obrázku

`Graphics` poskytuje kreslicí schopnosti na plátně. Vyčistíme pozadí na bílou a vykreslíme první zdrojový obrázek na levé polovině.

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(dataDir + "example1.png", new Rectangle(0, 0, 300, 600));
```

### Krok 5: Vykreslení druhého obrázku (dokončení sloučení)

Nyní umístíme druhý obrázek na pravou polovinu stejného plátna, čímž automaticky vytvoříme druhou vrstvu.

```java
graphics.drawImage(dataDir + "example2.png", new Rectangle(300, 0, 300, 600));
```

### Krok 6: Uložení výsledného souboru PSD

Uložte sloučené plátno na disk. Výsledný `combined.psd` obsahuje dvě editovatelné vrstvy.

```java
image.save();
```

Gratulujeme! Úspěšně jste **combine images java** a vygenerovali vrstvený soubor PSD připravený k dalším úpravám v Photoshopu.

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|-------|-------|-----|
| `File not found` při načítání zdrojových obrázků | Nesprávná cesta `dataDir` | Ověřte, že `dataDir` ukazuje na složku obsahující `example1.png` a `example2.png`. |
| Výstupní PSD je prázdný | `graphics.clear` voláno po vykreslení | Zavolejte `graphics.clear(Color.getWhite())` **před** jakýmkoli voláním `drawImage`. |
| Výjimka licence za běhu | Chybějící nebo vypršená licence Aspose.PSD | Aplikujte platnou licenci pomocí `License license = new License(); license.setLicense("Aspose.PSD.lic");` před jakýmkoli voláním API. |

## Často kladené otázky

**Q: Je Aspose.PSD kompatibilní se všemi formáty obrázků?**  
A: Aspose.PSD nativně čte a zapisuje **15+ formátů**, včetně PSD, PNG, JPEG, BMP, TIFF, GIF a dalších, což z něj činí univerzální volbu pro obrazové pipeline.

**Q: Mohu provádět další úpravy po sloučení obrázků?**  
A: Ano. Každé volání `drawImage` vytvoří samostatnou PSD vrstvu, kterou můžete později přesunout, aplikovat filtry nebo maskovat pomocí rozsáhlého API pro úpravu vrstev v Aspose.PSD.

**Q: Potřebuji komerční licenci pro produkci?**  
A: Platná licence je vyžadována pro produkční použití. Můžete ji získat v obchodě Aspose; pro hodnocení je k dispozici bezplatná zkušební verze.

**Q: Jak přidám více než dva obrázky?**  
A: Stačí opakovat `graphics.drawImage(...)` s vhodnými souřadnicemi pro každý další obrázek. Každé volání přidá novou vrstvu.

**Q: Kde mohu získat pomoc, pokud narazím na problémy?**  
A: Navštivte [Aspose.PSD fórum](https://forum.aspose.com/c/psd/34) pro podporu komunity nebo si prostudujte oficiální dokumentaci uvedenou na stránce ke stažení.

---

**Poslední aktualizace:** 2026-06-28  
**Testováno s:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Vytvořit obrázek nastavením cesty v Aspose.PSD pro Java](/psd/java/image-editing/create-image-by-setting-path/)
- [Vytvořit obrázek pomocí streamu v Aspose.PSD pro Java](/psd/java/image-editing/create-image-using-stream/)
- [Změna velikosti obrázku Java – Použití výčtu Resize Type v Aspose.PSD pro Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

```java
PsdOptions imageOptions = new PsdOptions();
```

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

```java
Image image = Image.create(imageOptions, 600, 600);
```

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

```java
image.save();
```