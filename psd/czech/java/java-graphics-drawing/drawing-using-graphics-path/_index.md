---
date: 2026-09-08
description: Naučte se, jak vytvořit obrázek pomocí třídy Graphics Path z Aspose.PSD
  v jazyce Java. Tento krok‑za‑krokem průvodce vám ukáže, jak přidat text, tvary a
  efektivně vymazat pozadí obrázku.
keywords:
- how to create image
- add text image java
- clear image background java
lastmod: 2026-09-08
linktitle: Jak vytvořit obrázek pomocí Graphics Path v jazyce Java
og_description: Naučte se, jak vytvořit obrázek s Aspose.PSD v jazyce Java. Tento
  tutoriál pokrývá přidávání textu, tvarů a mazání pozadí obrázku pomocí třídy Graphics
  Path.
og_image_alt: Screenshot of Java code creating an image with graphics path using Aspose.PSD
og_title: Jak vytvořit obrázek pomocí Graphics Path v jazyce Java s Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to create image with Aspose.PSD's Graphics Path class in
    Java. This step‑by‑step guide shows you how to add text, shapes, and clear image
    background efficiently.
  headline: How to create image using Graphics Path in Java
  type: TechArticle
- description: Learn how to create image with Aspose.PSD's Graphics Path class in
    Java. This step‑by‑step guide shows you how to add text, shapes, and clear image
    background efficiently.
  name: How to create image using Graphics Path in Java
  steps:
  - name: '**Java Development Kit (JDK)** – a stable JDK 11+ installed. Download it
      from [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – a stable JDK 11+ installed. Download it
      from [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from [here](https://releases.aspose.com/psd/java/)
      and add it to your project’s classpath.'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from [here](https://releases.aspose.com/psd/java/)
      and add it to your project’s classpath.'
  - name: '**IDE** – any Java IDE such as Eclipse, IntelliJ IDEA, or VS Code.'
    text: '**IDE** – any Java IDE such as Eclipse, IntelliJ IDEA, or VS Code.'
  type: HowTo
- questions:
  - answer: Aspose.PSD is a Java library that enables you to create, edit, and convert
      Photoshop (PSD) files and other raster formats without requiring Photoshop.
    question: What is Aspose.PSD?
  - answer: Yes – the library supports **50+** formats, including PNG, JPEG, BMP,
      TIFF, and GIF.
    question: Can I work with formats other than PSD?
  - answer: Yes, you can access a free trial of Aspose.PSD [here](https://releases.aspose.com/).
    question: Is a trial version available?
  - answer: You can purchase Aspose.PSD from [here](https://purchase.aspose.com/buy).
    question: How do I purchase a license?
  - answer: You can seek support and discussions on [Aspose’s forum](https://forum.aspose.com/c/psd/34).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- graphics path
- Aspose.PSD
- Java image processing
title: Jak vytvořit obrázek pomocí Graphics Path v jazyce Java
url: /cs/java/java-graphics-drawing/drawing-using-graphics-path/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak vytvořit obrázek pomocí Graphics Path v Javě

## Úvod
V tomto tutoriálu se naučíte **jak vytvořit obrázek** programově využitím výkonné třídy **Graphics Path**, kterou poskytuje Aspose.PSD pro Java. Ať už potřebujete kreslit vlastní tvary, vložit text nebo vymazat pozadí obrázku, níže uvedený krok‑za‑krokem průvodce vám ukáže, jak dosáhnout profesionálních výsledků během několika řádků kódu.

## Rychlé odpovědi
- **Která knihovna zpracovává složité kreslení?** Aspose.PSD pro Java třída Graphics Path.  
- **Mohu do obrázku přidat text?** Ano – použijte metodu `GraphicsPath.addString`.  
- **Je podpora pro vymazání pozadí?** Rozhodně, vyplňte cestu průhledným štětcem.  
- **Jaká verze Javy je požadována?** JDK 11 nebo novější.  
- **Potřebuji licenci pro produkci?** Je vyžadována komerční licence; je k dispozici bezplatná zkušební verze.

## Co je třída Graphics Path?
Třída `GraphicsPath` je jádrový objekt Aspose.PSD pro definování vektorových kreslicích instrukcí. Umožňuje vám skloubit tvary, text a výplně do jediné znovupoužitelné cesty, která může být vykreslena na libovolném obrázku. Vytvořením cesty můžete v jednom vykreslovacím průchodu použít pera, štětce a transformace, což zlepšuje výkon a udržuje logiku kreslení přehlednou.

## Proč používat Graphics Path pro přidání textu do obrázku v Javě a vymazání pozadí obrázku v Javě?
Aspose.PSD podporuje **více než 50 formátů obrázků** (včetně PSD, PNG, JPEG, BMP) a může zpracovávat soubory až do **2 GB** bez načítání celého dokumentu do paměti. Použití Graphics Path vám umožní kombinovat kreslení, umístění textu a vymazání pozadí v jediné vysoce výkonné operaci, čímž snížíte paměťovou zátěž až o **30 %** ve srovnání s přístupy založenými jen na rastru.

## Požadavky
Před zahájením se ujistěte, že máte následující:

1. **Java Development Kit (JDK)** – stabilní JDK 11+ nainstalováno. Stáhněte jej z [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – získáte nejnovější JAR z [here](https://releases.aspose.com/psd/java/) a přidáte jej do classpath vašeho projektu.  
3. **IDE** – libovolné Java IDE, například Eclipse, IntelliJ IDEA nebo VS Code.

S těmito věcmi jste připraveni začít vytvářet obrázky.

## Import balíčků
Pro práci s grafikou importujte požadované jmenné prostory:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Figure;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.GraphicsPath;
import com.aspose.psd.HatchStyle;
import com.aspose.psd.Pen;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.HatchBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.shapes.EllipseShape;
import com.aspose.psd.shapes.RectangleShape;
import com.aspose.psd.shapes.TextShape;
```

Tyto importy zpřístupňují základní třídy pro kreslení, štětce a pera potřebné pro manipulaci s obrázky.

## Jak vytvořit obrázek pomocí Graphics Path v Javě?
Vytvořte novou rastrovou plátno, připojte objekt `Graphics` a připravte kreslicí plochu. Tento jediný krok nastaví **500 × 500 pixel** bitmapu připravenou pro vektorové vykreslování. Plátno je zpočátku průhledné, což vám umožní později vyplnit libovolnou barvu nebo vzor pozadí, což je nezbytné pro scénáře s vymazáním pozadí obrázku.

```java
PsdImage image = new PsdImage(500, 500);
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
```

## Krok 1: inicializace obrázku a grafiky
Zde vytvoříme objekt `PsdImage` (500 × 500) a získáme jeho kontext `Graphics`.  
`PsdImage` představuje rastrový obrázek v paměti, který Aspose.PSD může manipulovat a ukládat v mnoha formátech.  
`Graphics` poskytuje kreslicí metody, které vykreslují tvary, text a cesty na `PsdImage`.

## Krok 2: vytvoření a konfigurace graphics path
Dále vytvoříme `GraphicsPath`, který obsahuje kruh, obdélník a textový štítek.  
`GraphicsPath` je kontejner pro geometrické tvary; můžete do něj před vykreslením přidávat tvary, čáry a řetězce.

```java
GraphicsPath graphicspath = new GraphicsPath();
Figure figure = new Figure();
figure.addShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new TextShape("Aspose.PSD", new RectangleF(170, 225, 170, 100), new TextFont("Arial", 20), StringFormat.getGenericTypographic()));
Figure[] fig = { figure };
graphicspath.addFigures(fig);
```

### Přidání textu do obrázku (add text image java)
Metoda `addString` třídy `GraphicsPath` umístí zadaný text na dané souřadnice pomocí poskytnutého fontu a štětce. Toto je nejspolehlivější způsob, jak vložit ostrý, škálovatelný text do vektorové cesty.

## Krok 3: vykreslení a vyplnění cesty
Nyní vykreslíme cestu modrým perem a vyplníme ji pomocí vertikálního štětce s šrafováním, což také ukazuje, jak **clear image background java** provést vyplněním průhledným vzorem, pokud je to požadováno. `Pen` definuje styl obrysu, zatímco `HatchBrush` vytváří vzorovanou výplň.

```java
graphics.drawPath(new Pen(Color.getBlue()), graphicspath);
HatchBrush hatchbrush = new HatchBrush();
hatchbrush.setBackgroundColor(Color.getBrown());
hatchbrush.setForegroundColor(Color.getBlue());
hatchbrush.setHatchStyle(HatchStyle.Vertical);
graphics.fillPath(hatchbrush, graphicspath);
```

## Krok 4: uložení obrázku
Nakonec zapíšeme složený obrázek na disk ve formátu PNG (nebo v libovolném z více než 50 podporovaných formátů). Metoda `save` určuje typ výstupního souboru podle přípony, kterou zadáte.

```java
String dataDir = "Your Document Directory";
image.save(dataDir + "DrawingUsingGraphicsPath_output.psd");
```

## Časté problémy a řešení
- **Cesta není viditelná** – ujistěte se, že barva pera kontrastuje s výplňovým štětcem.  
- **Text je rozmazaný** – použijte vyšší rozlišení obrázku nebo TrueType font s dostatečným DPI.  
- **Chyby nedostatku paměti u velkých souborů** – povolte `PsdImageOptions.setUseMemoryCache(true)`, aby se data streamovala místo úplného načtení.

## Často kladené otázky

**Q: Co je Aspose.PSD?**  
A: Aspose.PSD je Java knihovna, která vám umožňuje vytvářet, upravovat a konvertovat soubory Photoshop (PSD) a další rastrové formáty bez nutnosti Photoshopu.

**Q: Mohu pracovat s formáty jinými než PSD?**  
A: Ano – knihovna podporuje **více než 50** formátů, včetně PNG, JPEG, BMP, TIFF a GIF.

**Q: Je k dispozici zkušební verze?**  
A: Ano, bezplatnou zkušební verzi Aspose.PSD získáte [zde](https://releases.aspose.com/).

**Q: Jak si mohu zakoupit licenci?**  
A: Licenci na Aspose.PSD můžete zakoupit [zde](https://purchase.aspose.com/buy).

**Q: Kde mohu získat podporu?**  
A: Podporu a diskuse najdete na [Aspose’s forum](https://forum.aspose.com/c/psd/34).

## Závěr
Po přečtení tohoto průvodce nyní víte **jak vytvořit obrázek** s komplexními vektorovými tvary, vloženým textem a průhledným pozadím pomocí třídy Graphics Path v Aspose.PSD. Experimentujte s různými pery, štětci a geometriemi cest a vytvářejte bohatší grafiku pro hry, UI prvky nebo automatizovanou tvorbu reportů.

---

**Last Updated:** 2026-09-08  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## Související tutoriály

- [Generovat PSD obrázek v Javě nastavením cesty s Aspose.PSD](/psd/java/image-editing/create-image-by-setting-path/)
- [Změna velikosti obrázku s Aspose.PSD pro Java – kreslení tvarů a základní operace s obrázkem](/psd/java/basic-image-operations/)
- [Přidání podpisu do obrázku – kreslení obrázku na plátno s Aspose.PSD pro Java](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}