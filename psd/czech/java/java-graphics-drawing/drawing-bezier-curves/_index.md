---
date: 2026-09-08
description: Naučte se, jak kreslit bezier curves v Java pomocí Aspose.PSD for Java.
  Postupujte podle step‑by‑step instrukcí, prerequisites a code‑free příkladů.
keywords:
- how to draw bezier
- how to use pen
- bezier curve example java
- java graphics draw curve
lastmod: 2026-09-08
linktitle: Kreslení Bezier Curves v Java
og_description: Jak kreslit bezier curves v Java pomocí Aspose.PSD. Tento průvodce
  zahrnuje prerequisites, step‑by‑step kreslení a tipy pro high‑resolution images.
og_image_alt: Screenshot of a Java application rendering a Bezier curve with Aspose.PSD
og_title: Jak kreslit bezier curves v Javě s Aspose.PSD library
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw bezier curves in Java using Aspose.PSD for Java.
    Follow step‑by‑step instructions, prerequisites, and code‑free examples.
  headline: How to draw bezier curves in Java with Aspose.PSD library
  type: TechArticle
- description: Learn how to draw bezier curves in Java using Aspose.PSD for Java.
    Follow step‑by‑step instructions, prerequisites, and code‑free examples.
  name: How to draw bezier curves in Java with Aspose.PSD library
  steps:
  - name: create an image instance
    text: 'The `PsdImage` class is Aspose.PSD''s top‑level object that represents
      a single PSD file in memory. First, you need to create an instance of the `PsdImage`
      class, which represents a PSD image in memory. Explanation: - `PsdImage` is
      instantiated with width and height parameters (100 × 100 pixels in th'
  - name: initialize graphics context
    text: 'The `Graphics` class provides drawing capabilities on a `PsdImage`. Next,
      initialize an instance of the `Graphics` class to perform drawing operations
      on the image. Explanation: - `Graphics` object is initialized with the `image`
      instance, allowing drawing operations.'
  - name: clear the graphics surface
    text: 'The `clear()` method sets the background colour of the graphics surface.
      Clear the graphics surface using a specific background colour, here `Color.getYellow()`.
      Explanation: - `clear()` method sets the background colour of the graphics surface.'
  - name: initialize pen for drawing
    text: 'The `Pen` object defines stroke attributes such as colour and width. Set
      up a `Pen` object with properties like colour and width to define how the curve
      will be drawn. Explanation: - `Pen` is initialized with black colour and 3‑pixel
      width.'
  - name: define bezier curve parameters
    text: 'Control points determine the curvature. Specify the control points and
      end points for the Bezier curve. Explanation: - `startX`, `startY`: Starting
      point of the curve. - `controlX1`, `controlY1`: First control point. - `controlX2`,
      `controlY2`: Second control point. - `endX`, `endY`: Ending point of'
  - name: draw the bezier curve
    text: 'The `drawBezier()` method renders the curve using the supplied `Pen` and
      points. Use the `drawBezier()` method to draw the Bezier curve onto the image
      using the previously defined `Pen` and control points. Explanation: - `drawBezier()`
      method draws the curve with specified parameters using the `blac'
  - name: save the image
    text: Saving the image persists the drawing to disk. Save the drawn image to a
      BMP file format.
  type: HowTo
- questions:
  - answer: Yes, repeat the `drawBezier()` call inside a loop, updating the control
      points for each curve.
    question: Can I draw multiple Bezier curves in the same image?
  - answer: Modify the `Pen` object's colour property (`Color.getBlack()` in the example)
      before invoking `drawBezier()`.
    question: How can I change the colour of the Bezier curve?
  - answer: Yes, Aspose.PSD for Java supports high‑resolution images with efficient
      memory management, handling files larger than 500 MB without loading the entire
      file into memory.
    question: Is Aspose.PSD for Java suitable for high‑resolution images?
  - answer: Yes, Aspose.PSD for Java supports exporting to PNG, JPEG, TIFF, and many
      other raster formats.
    question: Can I export the image to formats other than BMP?
  - answer: Visit the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides and code samples.
    question: Where can I find more examples and documentation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- drawing bezier
- Aspose.PSD
- Java graphics
- curve drawing
title: Jak kreslit bezier curves v Javě s Aspose.PSD library
url: /cs/java/java-graphics-drawing/drawing-bezier-curves/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak kreslit Bezierovy křivky v Javě s knihovnou Aspose.PSD

## Úvod
Pokud potřebujete vědět **jak kreslit Bezier** tvary v desktopové nebo serverové aplikaci v Javě, Aspose.PSD pro Javu vám poskytuje čisté, paměťově úsporné API. V tomto tutoriálu uvidíte přesné kroky k vytvoření PSD plátna, nastavení kreslicího pera, definování řídicích bodů a vykreslení hladké Bezierovy křivky — vše bez psaní jakéhokoli nízkoúrovňového kódu pro manipulaci s pixely.

## Rychlé odpovědi
- **Která knihovna provádí kreslení?** Aspose.PSD for Java.
- **Kolik řádků kódu je potřeba?** About ten concise statements.
- **Mohu změnit barvu křivky?** Yes, by adjusting the `Pen` colour property.
- **Je podporován výstup ve vysokém rozlišení?** Yes, up to 500 MB files without full memory load.
- **Potřebuji komerční licenci?** A free trial works for development; a license is required for production.

## Co je Bezierova křivka?
Bezierova křivka je matematicky definovaná hladká čára řízená dvěma nebo více body. Je široce používána ve vektorové grafice, animaci a návrhu uživatelského rozhraní k vytváření elegantních, škálovatelných tvarů. Tvar křivky je určen počátečním bodem, koncovým bodem a jedním nebo více řídicími body, které ovlivňují zakřivení, což umožňuje návrhářům modelovat složité cesty pomocí jednoduchých parametrů.

## Proč použít Aspose.PSD pro kreslení Bezierových křivek?
Aspose.PSD podporuje **30+ formátů obrázků** a dokáže zpracovat **více‑stovkové PSD soubory** bez načítání celého dokumentu do RAM. Metoda `drawBezier()` knihovny automaticky zvládá anti‑aliasing a správu barev, což poskytuje pixel‑dokonalé výsledky za méně než sekundu pro typické plátna 100 × 100.

## Požadavky
Než začnete, ujistěte se, že máte následující požadavky:
1. **Java Development Kit (JDK)** – jakákoli aktuální verze (8 nebo novější) nainstalovaná a nakonfigurovaná.
2. **Aspose.PSD for Java JAR** – stáhněte knihovnu Aspose.PSD pro Javu z [Aspose.PSD Java download](https://releases.aspose.com/psd/java/) a přidejte ji do classpath vašeho projektu.
3. **Integrated Development Environment (IDE)** – například Eclipse, IntelliJ IDEA nebo NetBeans, nastavené s JDK.

## Import balíčků
Následující importy přinášejí třídy Aspose.PSD potřebné pro tvorbu obrázků a kreslení.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Jak kreslit Bezierovy křivky v Javě?
Načtěte prázdný `PsdImage`, vytvořte objekt `Graphics`, nakonfigurujte `Pen`, definujte počáteční, řídicí a koncové body, zavolejte `drawBezier()` a nakonec uložte obrázek. Tento postup vytvoří hladkou křivku jedním voláním metody a nevyžaduje žádné ruční výpočty pixelů.

### Krok 1: vytvořit instanci obrázku
Třída `PsdImage` je nejvyšší objekt knihovny Aspose.PSD, který představuje jeden PSD soubor v paměti. Nejprve je třeba vytvořit instanci třídy `PsdImage`, která představuje PSD obrázek v paměti.

```java
String dataDir = "Your Document Directory";
Image image = new PsdImage(100, 100);
```
Vysvětlení:
- `PsdImage` je vytvořena s parametry šířky a výšky (100 × 100 pixelů v tomto příkladu).

### Krok 2: inicializovat grafický kontext
Třída `Graphics` poskytuje kreslicí schopnosti na `PsdImage`. Dále inicializujte instanci třídy `Graphics` pro provádění kreslicích operací na obrázku.

```java
Graphics graphics = new Graphics(image);
```
Vysvětlení:
- Objekt `Graphics` je inicializován s instancí `image`, což umožňuje kreslicí operace.

### Krok 3: vymazat grafický povrch
Metoda `clear()` nastavuje barvu pozadí grafického povrchu. Vymažte grafický povrch pomocí konkrétní barvy pozadí, zde `Color.getYellow()`.

```java
graphics.clear(Color.getYellow());
```
Vysvětlení:
- Metoda `clear()` nastavuje barvu pozadí grafického povrchu.

### Krok 4: inicializovat pero pro kreslení
Objekt `Pen` definuje atributy tahu, jako je barva a šířka. Nastavte objekt `Pen` s vlastnostmi jako barva a šířka, aby definoval, jak bude křivka kreslena.

```java
Pen blackPen = new Pen(Color.getBlack(), 3);
```
Vysvětlení:
- `Pen` je inicializováno s černou barvou a šířkou 3 pixelů.

### Krok 5: definovat parametry Bezierovy křivky
Řídicí body určují zakřivení. Zadejte řídicí body a koncové body pro Bezierovu křivku.

```java
float startX = 10, startY = 25;
float controlX1 = 20, controlY1 = 5;
float controlX2 = 55, controlY2 = 10;
float endX = 90, endY = 25;
```
Vysvětlení:
- `startX`, `startY`: Počáteční bod křivky.  
- `controlX1`, `controlY1`: První řídicí bod.  
- `controlX2`, `controlY2`: Druhý řídicí bod.  
- `endX`, `endY`: Koncový bod křivky.

### Krok 6: nakreslit Bezierovu křivku
Metoda `drawBezier()` vykresluje křivku pomocí dodaného `Pen` a bodů. Použijte metodu `drawBezier()` k nakreslení Bezierovy křivky na obrázek pomocí dříve definovaného `Pen` a řídicích bodů.

```java
graphics.drawBezier(blackPen, startX, startY, controlX1, controlY1, controlX2, controlY2, endX, endY);
```
Vysvětlení:
- Metoda `drawBezier()` kreslí křivku se zadanými parametry pomocí `blackPen`.

### Krok 7: uložit obrázek
Uložení obrázku zachová kresbu na disku. Uložte nakreslený obrázek ve formátu BMP.

```java
String outpath = dataDir + "Bezier.bmp";
BmpOptions saveOptions = new BmpOptions();
image.save(outpath, saveOptions);
```

## Časté problémy a řešení
- **Křivka vypadá plochá** – Ověřte, že řídicí body nejsou kolineární s počátečním a koncovým bodem. Mírně je posuňte, aby vzniklo zakřivení.  
- **Barva se nezmění** – Ujistěte se, že měníte barvu `Pen` před voláním `drawBezier()`.  
- **Chyby nedostatku paměti na velkých plátnech** – Použijte konstruktory `PsdImage`, které umožňují streamování, nebo rozdělte kresbu na dlaždice.

## Často kladené otázky

**Q: Můžu kreslit více Bezierových křivek ve stejném obrázku?**  
A: Ano, opakujte volání `drawBezier()` uvnitř smyčky a aktualizujte řídicí body pro každou křivku.

**Q: Jak mohu změnit barvu Bezierovy křivky?**  
A: Změňte vlastnost barvy objektu `Pen` (`Color.getBlack()` v příkladu) před voláním `drawBezier()`.

**Q: Je Aspose.PSD pro Javu vhodný pro obrázky ve vysokém rozlišení?**  
A: Ano, Aspose.PSD pro Javu podporuje obrázky ve vysokém rozlišení s efektivní správou paměti, zpracovává soubory větší než 500 MB bez načítání celého souboru do paměti.

**Q: Mohu exportovat obrázek do jiných formátů než BMP?**  
A: Ano, Aspose.PSD pro Javu podporuje export do PNG, JPEG, TIFF a mnoha dalších rastrových formátů.

**Q: Kde mohu najít více příkladů a dokumentaci?**  
A: Navštivte [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) pro komplexní návody a ukázky kódu.

---

**Poslední aktualizace:** 2026-09-08  
**Testováno s:** Aspose.PSD for Java 24.11  
**Autor:** Aspose

## Související tutoriály

- [Změna velikosti obrázku s Aspose.PSD pro Java – kreslení tvarů a základní operace s obrázkem](/psd/java/basic-image-operations/)
- [Kreslení a uložení obdélníku v PSD pomocí Aspose.PSD pro Java](/psd/java/basic-image-operations/simple-drawing/)
- [Jak změnit barvu tahu v Javě pomocí Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}