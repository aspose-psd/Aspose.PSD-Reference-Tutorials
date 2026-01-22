---
date: 2026-01-22
description: Naučte se, jak vytvořit PSD obrázek v Javě pomocí Aspose.PSD, kreslit
  grafiku, vyplnit polygon a exportovat PSD do BMP. Kompletní tutoriál pro manipulaci
  s obrázky v Javě.
linktitle: Drawing Using Graphics in Java
second_title: Aspose.PSD Java API
title: Vytvoření PSD obrázku v Javě – kreslení pomocí Graphics s Aspose.PSD
url: /cs/java/java-graphics-drawing/drawing-using-graphics/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kreslení pomocí grafiky v Javě

## Úvod
V tomto **java image manipulation tutorial** vám ukážeme, jak **create PSD image java** programově pomocí Aspose.PSD. Ať už potřebujete generovat grafiku za běhu, vyplnit mnohoúhelníky nebo exportovat svou práci do BMP, tento průvodce vás provede každlnííd Graphics a Brushřebuji licenci pro vývoj?** K dispozici je bezplatná dočasná licence pro vyhodnocení.
- **Jaká verze Javy je požadována?** JDK 8 or higher.

## Předpoklady
Než se ponoříte do tohoto tutoriálu, ujistěte se, že máte následující předpoklady:
- Základní znalosti programování v Javě.
- Java Development Kit (JDK) nainstalovaný ve vašem systému.
- Integrované vývojové prostředí (IDE) jako IntelliJ IDEA nebo Eclipse.
- Knihovna Aspose.PSD pro Java. Můžete si ji stáhnout [zde](https://releases.aspose.com/psd/java/).

## Jak kreslit grafiku v Javě pomocí Aspose.PSD
Pro začátek importujte potřebné balíčky z Aspose.PSD pro Java a dalších standardních knihoven Javy:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Point;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.LinearGradientBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Krok 1: Vytvořit objekt obrázku
Nejprve vytvořte instanci objektu `PsdImage` s konkrétními rozměry:

```java
String dataDir = "Your Document Directory";
PsdImage image = new PsdImage(500, 500);
```

## Krok 2: Inicializovat objekt Graphics
Dále inicializujte objekt `Graphics` pomocí `PsdImage`:

```java
Graphics graphics = new Graphics(image);
```

## Krok 3: Vyčistit povrch obrázku
Vyčistěte povrch obrázku zadanou barvou (v tomto příkladu bílá):

```java
graphics.clear(Color.getWhite());
```

## Krok 4: Vytvořit a nakonfigurovat objekt Pen
Vytvořte objekt `Pen` pro definování vlastností tahu (barva, tloušťka atd.):

```java
Pen pen = new Pen(Color.getBlue());
```

## Krok 5: Kreslit tvary – Jak kreslit grafiku v Javě
Nakreslete elipsu na obrázek pomocí objektu `Pen` a ohraničujícího obdélníku:

```java
graphics.drawEllipse(pen, new Rectangle(10, 10, 150, 100));
```

## Vyplnit mnohoúhelník v Java Graphics
Definujte a použijte `LinearGradientBrush` pro vyplnění mnohoúhelníku gradientem:

```java
LinearGradientBrush linearGradientBrush = new LinearGradientBrush(image.getBounds(), Color.getRed(), Color.getWhite(), 45f);
Point[] points = { new Point(200, 200), new Point(400, 200), new Point(250, 350) };
graphics.fillPolygon(linearGradientBrush, points);
```

## Exportovat PSD do BMP
Nakonec uložte upravený obrázek na určené místo a ve formátu (v tomto příkladu BMP):

```java
image.save(dataDir + "DrawingUsingGraphics_output.bmp", new BmpOptions());
```

## Závěr
Po absolvování tohoto **java image manipulation tutorial** nyní víte, jak **create PSD image java**, kreslit tvary, aplikovat gradienty, vyplňovat mnohoúhelníky a **export PSD to BMP** pomocí Aspose.PSD. Experimentujte s různými štětci, barvami a geometriemi, abyste obohatili své Java aplikace o výkonné grafické možnosti.

## Často kladené otázky

**Q: Může Aspose.PSD zvládnout složité manipulace s obrázky?**  
A: Ano, Aspose.PSD podporuje širokou škálu operací včetně manipulace s vrstvami, úprav barev a vykreslování textu.

**Q: Je Aspose.PSD vhodný pro aplikace s vysokým výkonem?**  
A: Rozhodně, Aspose.PSD je optimalizován pro výkon a efektivitu paměti.

**Q: Kde mohu najít více příkladů a dokumentaci?**  
A: Navštivte [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/) pro komplexní průvodce a reference API.

**Q: Podporuje Aspose.PSD více formátů obrázků pro export?**  
A: Ano, Aspose.PSD může exportovat do BMP, PNG, JPEG, TIFF a dalších populárních formátů.

**Q: Jak mohu získat podporu nebo pomoc, pokud narazím na problémy?**  
A: Obraťte se na komunitu Aspose.PSD na [support forum](https://forum.aspose.com/c/psd/34) nebo zvažte [temporary license](https://purchase.aspose.com/temporary-license/) pro prioritní podporu.

---

**Poslední aktualizace:** 2026-01-22  
**Testováno s:** Aspose.PSD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}