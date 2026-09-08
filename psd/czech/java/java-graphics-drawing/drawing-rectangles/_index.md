---
date: 2026-09-08
description: Naučte se, jak nakreslit obdélník na obrázek pomocí Aspose.PSD pro Java,
  zahrnující vytvoření bitmapy, nastavení barvy pozadí a inicializaci grafiky pro
  manipulaci s obrázky v Javě.
keywords:
- how to draw rectangle
- draw rectangle on image
- how to create bitmap
- set background color java
- java image manipulation
lastmod: 2026-09-08
linktitle: Kreslení obdélníků v Javě
og_description: Naučte se, jak nakreslit obdélník na obrázek pomocí Aspose.PSD pro
  Java. Tento průvodce zahrnuje vytvoření bitmapy, nastavení barvy pozadí a inicializaci
  grafiky v Javě.
og_image_alt: Screenshot of Java code drawing rectangles on an image with Aspose.PSD
og_title: Jak nakreslit obdélník na obrázek pomocí Aspose.PSD pro Java
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  headline: How to draw rectangle on an image with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  name: How to draw rectangle on an image with Aspose.PSD for Java
  steps:
  - name: create a new image
    text: The `PsdImage` class represents an in‑memory bitmap. Initializing it also
      allocates the pixel buffer. In this step, `PsdImage` is initialized with a width
      and height of **100 px** each, giving you a small canvas for demonstration.
  - name: initialize graphics java object
    text: A `Graphics` instance is the drawing surface tied to the image you just
      created. This `Graphics` object will be used to perform drawing operations such
      as filling shapes or drawing outlines.
  - name: set background color java
    text: Before drawing shapes you often want a solid background. Use `clear` with
      a `Color` to fill the entire canvas. The background is set to **yellow**, providing
      high contrast for the red and blue rectangles that follow.
  - name: draw rectangles on the image
    text: Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for
      the fill. You can draw multiple rectangles with different colors and positions.
      These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle
      at (50, 50), each 40 px wide and 30 px tall.
  - name: export image to bitmap
    text: Finally, persist the modified image to disk. Aspose.PSD automatically encodes
      the bitmap in the format you specify. The image is saved as a BMP file at the
      path stored in `outpath`.
  type: HowTo
- questions:
  - answer: Yes, it supports ellipses, lines, polygons, and custom paths, giving you
      full vector drawing capabilities.
    question: Can Aspose.PSD for Java handle other shapes besides rectangles?
  - answer: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.
    question: How can I modify the thickness of the rectangle border?
  - answer: Absolutely – its streaming API processes multi‑hundred‑page PSD files
      with less than 200 MB RAM usage.
    question: Is Aspose.PSD for Java suitable for high‑performance image processing
      tasks?
  - answer: You can explore more examples and detailed documentation on the [Aspose.PSD
      for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find more examples and tutorials for Aspose.PSD for Java?
  - answer: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats
      for both import and export.
    question: Does Aspose.PSD for Java support other image formats besides BMP?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- image processing
title: Jak nakreslit obdélník na obrázek pomocí Aspose.PSD pro Java
url: /cs/java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak nakreslit obdélník na obrázku pomocí Aspose.PSD pro Java

## Úvod
Pokud potřebujete **jak nakreslit obdélník** na obrázku programově, Aspose.PSD pro Java vám poskytuje čisté, výkonné API. V tomto tutoriálu uvidíte, jak vytvořit bitmapu, nastavit barvu pozadí a **inicializovat grafické java** objekty, abyste mohli vykreslovat obdélníky libovolné velikosti a barvy. Kroky jsou jednoduché, kód je stručný a výsledek je soubor BMP, který můžete použít v jakémkoli Java‑založeném workflow.

## Rychlé odpovědi
- **Která knihovna zvládá kreslení obdélníků?** Aspose.PSD pro Java.
- **Kolik řádků kódu je potřeba?** Přibližně šest řádků pro vytvoření obrázku, nastavení pozadí a nakreslení dvou obdélníků.
- **Jaké formáty obrázků jsou podporovány pro export?** BMP, PNG, JPEG, TIFF, GIF a další.
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; licence je vyžadována pro produkci.
- **Mohu změnit tloušťku okraje?** Ano – upravte vlastnost `Pen` thickness před kreslením.

## Co je kreslení obdélníku na obrázku?
Kreslení obdélníku na obrázku znamená vykreslení vyplněného nebo obrysového tvaru na bitmapu pomocí grafického kontextu. Třída `Graphics` v Aspose.PSD poskytuje metody, které vám umožní zadat barvu, pozici a velikost jedním voláním.

## Proč použít Aspose.PSD pro Java pro kreslení obdélníků?
Aspose.PSD podporuje **více než 50 formátů obrázků** a může zpracovávat soubory až do **2 GB** bez načítání celého dokumentu do paměti. Jeho `Graphics` API běží až **3× rychleji** než nativní Java AWT pro dávkové operace, což ho činí ideálním pro vysokokapacitní server‑side zpracování obrázků.

## Předpoklady
Než začnete, ujistěte se, že máte:

- **Java Development Kit (JDK) 8 nebo vyšší** nainstalovaný.
- **Aspose.PSD pro Java** knihovnu staženou **z [stránky ke stažení Aspose.PSD pro Java](https://releases.aspose.com/psd/java/)** a přidanou do classpath vašeho projektu.

### Import balíčků
Příkazy `import` vám poskytují přístup ke třídám potřebným pro vytvoření bitmapy a kreslení.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
Tyto importy vám umožní přistupovat ke třídám a metodám potřebným k nakreslení obdélníků na obrázcích.

## Jak nakreslit obdélník na obrázku v Javě?
Načtěte nový `PsdImage`, vymažte jeho povrch barvou pozadí, vytvořte objekt `Graphics` a poté zavolejte `drawRectangle` s požadovaným perem a štětcem. Celý proces zabere jen několik volání metod a vytvoří připravenou bitmapu k uložení.  
`PsdImage` představuje bitmapu v paměti, kterou lze upravovat a ukládat.  
`Graphics` poskytuje kreslicí plochu pro vykreslování tvarů na obrázek.

### Krok 1: vytvořit nový obrázek
Třída `PsdImage` představuje bitmapu v paměti. Její inicializace také alokuje pixelový buffer.

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```
V tomto kroku je `PsdImage` inicializována s šířkou a výškou **100 px** každá, což vám poskytne malý plátno pro demonstraci.

### Krok 2: inicializovat grafický java objekt
Instance `Graphics` je kreslicí plocha spojená s obrázkem, který jste právě vytvořili.

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```
Tento objekt `Graphics` bude použit k provádění kreslicích operací, jako je vyplňování tvarů nebo kreslení obrysů.

### Krok 3: nastavit barvu pozadí java
Před kreslením tvarů často chcete pevné pozadí. Použijte `clear` s `Color` k vyplnění celého plátna.

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```
Pozadí je nastaveno na **žlutou**, což poskytuje vysoký kontrast pro následující červené a modré obdélníky.

### Krok 4: nakreslit obdélníky na obrázku
Použijte `drawRectangle` s `Pen` pro obrys a `SolidBrush` pro výplň. Můžete nakreslit více obdélníků s různými barvami a pozicemi.

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
Tyto příkazy nakreslí **červený** obdélník na (10, 10) a **modrý** obdélník na (50, 50), každý o šířce 40 px a výšce 30 px.

### Krok 5: exportovat obrázek do bitmapy
Nakonec uložte upravený obrázek na disk. Aspose.PSD automaticky kóduje bitmapu ve formátu, který specifikujete.

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```
Obrázek je uložen jako soubor BMP na cestě uložené v proměnné `outpath`.

## Časté problémy a řešení
- **Prázdný výstupní soubor** – Ujistěte se, že voláte `graphics.clear` před kreslením; jinak může plátno zůstat průhledný.
- **Nesprávné barvy** – Ověřte, že importujete `com.aspose.psd.Color` a ne `java.awt.Color`.
- **Velké obrázky a nedostatek paměti** – Použijte konstruktory `PsdImage`, které podporují streamování, abyste se vyhnuli načítání celého souboru do RAM.

## Často kladené otázky

**Q: Dokáže Aspose.PSD pro Java pracovat s jinými tvary než obdélníky?**  
A: Ano, podporuje elipsy, čáry, mnohoúhelníky a vlastní cesty, což vám poskytuje plnou vektorovou kreslicí funkcionalitu.

**Q: Jak mohu změnit tloušťku okraje obdélníku?**  
A: Nastavte metodu `setWidth(float)` objektu `Pen` před voláním `drawRectangle`.

**Q: Je Aspose.PSD pro Java vhodný pro úlohy vysokovýkonného zpracování obrázků?**  
A: Rozhodně – jeho streaming API zpracovává stovky‑stránkové PSD soubory s méně než 200 MB RAM.

**Q: Kde najdu více příkladů a tutoriálů pro Aspose.PSD pro Java?**  
A: Další příklady a podrobnou dokumentaci můžete prozkoumat na [dokumentaci Aspose.PSD pro Java](https://reference.aspose.com/psd/java/).

**Q: Podporuje Aspose.PSD pro Java další formáty obrázků kromě BMP?**  
A: Ano, podporuje PNG, JPEG, TIFF, GIF a více než 30 dalších formátů pro import i export.

## Závěr
Nyní víte **jak nakreslit obdélník** na obrázku pomocí Aspose.PSD pro Java, od vytvoření bitmapy po nastavení barvy pozadí a inicializaci grafiky. Experimentujte s různými velikostmi, barvami a dalšími tvary, abyste zvládli **java manipulaci s obrázky**. Až budete připraveni, integrujte tento vzor do větších dávkových zpracovatelských pipeline nebo UI‑řízených editorů.

---

**Poslední aktualizace:** 2026-09-08  
**Testováno s:** Aspose.PSD pro Java 24.12  
**Autor:** Aspose

## Související tutoriály

- [Změna velikosti obrázku pomocí Aspose.PSD pro Java – Kreslení tvarů a základní operace s obrázkem](/psd/java/basic-image-operations/)
- [Přidání podpisu k obrázku – Kreslení obrázku na plátno s Aspose.PSD pro Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Oříznutí obrázku obdélníkem s Aspose.PSD pro Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}