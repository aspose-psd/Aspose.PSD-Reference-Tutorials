---
title: Kreslení pomocí grafické cesty v Javě
linktitle: Kreslení pomocí grafické cesty v Javě
second_title: Aspose.PSD Java API
description: Naučte se vytvářet komplexní grafiku v Javě pomocí třídy Graphics Path Aspose.PSD. Tento výukový program vás provede každým krokem k vytvoření úžasného obrazu.
type: docs
weight: 19
url: /cs/java/java-graphics-drawing/drawing-using-graphics-path/
---
## Úvod
Vytváření a manipulace s obrázky programově může být pro vývojáře v Javě vzrušujícím úkolem, zejména při použití knihoven jako Aspose.PSD. V tomto tutoriálu se ponoříme do procesu kreslení složité grafiky pomocí třídy Graphics Path v Javě s Aspose.PSD.
## Předpoklady
Než přejdeme k části kódování, ujistěte se, že máte následující předpoklady:
1.  Java Development Kit (JDK): Stabilní verze JDK nainstalovaná na vašem počítači. Můžete si jej stáhnout z[Web společnosti Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD for Java Library: Stáhněte si knihovnu Aspose.PSD for Java z[tady](https://releases.aspose.com/psd/java/). Po stažení přidejte soubor JAR do cesty třídy vašeho projektu.
3. Integrované vývojové prostředí (IDE): Ať už je to Eclipse, IntelliJ IDEA nebo jakékoli jiné, k psaní a spouštění kódu Java potřebujete IDE.
S těmito předpoklady se podíváme na to, jak vytvořit vizuálně poutavé obrázky pomocí třídy Graphics Path.
## Importujte balíčky
Chcete-li začít, musíte importovat potřebné balíčky:
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
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.shapes.EllipseShape;
import com.aspose.psd.shapes.RectangleShape;
import com.aspose.psd.shapes.TextShape;
```
Tyto importy poskytují přístup k základním funkcím potřebným k vytváření a manipulaci s obrázky pomocí Aspose.PSD.
## Krok 1: Inicializujte obrázek a grafiku
Pro začátek si nastavíme nový obrázek a inicializujeme grafický objekt:
```java
PsdImage image = new PsdImage(500, 500);
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
```
Zde vytvoříme obrázek 500x500 pixelů a grafický objekt pro kreslení.
## Krok 2: Vytvořte a nakonfigurujte grafickou cestu
 Dále vytvoříme a`GraphicsPath` objekt pro definování cesty kreslení:
```java
GraphicsPath graphicspath = new GraphicsPath();
Figure figure = new Figure();
figure.addShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new TextShape("Aspose.PSD", new RectangleF(170, 225, 170, 100), new TextFont("Arial", 20), StringFormat.getGenericTypographic()));
Figure[] fig = { figure };
graphicspath.addFigures(fig);
```
V tomto kroku přidáme k našemu obrázku kruh, obdélník a textový štítek a poté přidáme tento obrázek do naší grafické cesty.
## Krok 3: Nakreslete a vyplňte cestu
Nyní, když máme cestu definovanou, můžeme ji nakreslit a vyplnit:
```java
graphics.drawPath(new Pen(Color.getBlue()), graphicspath);
HatchBrush hatchbrush = new HatchBrush();
hatchbrush.setBackgroundColor(Color.getBrown());
hatchbrush.setForegroundColor(Color.getBlue());
hatchbrush.setHatchStyle(HatchStyle.Vertical);
graphics.fillPath(hatchbrush, graphicspath);
```
tomto kroku nakreslíme cestu modrým perem a vyplníme ji svislým šrafovacím vzorem pomocí šrafovacího štětce.
## Krok 4: Uložte obrázek
Nakonec uložte obrázek do souboru:
```java
String dataDir = "Your Document Directory";
image.save(dataDir + "DrawingUsingGraphicsPath_output.psd");
```
Tímto posledním krokem je tvorba obrázku pomocí grafické cesty dokončena.
## Závěr
Vytváření složitých obrázků pomocí třídy Graphics Path s Aspose.PSD je výkonné a poutavé. Podle této příručky můžete rozšířit možnosti své Java aplikace v oblasti grafického designu.
## FAQ
### Co je Aspose.PSD?
Aspose.PSD je knihovna, která umožňuje vývojářům pracovat se soubory Photoshopu a programově manipulovat s vrstvami obrázků.
### Mohu použít Aspose.PSD pro jiné formáty než PSD?
Od této příručky se Aspose.PSD konkrétně zabývá soubory PSD, ale nabízí rozšíření pro práci s různými formáty obrázků.
### Je k dispozici zkušební verze pro Aspose.PSD?
 Ano, máte přístup k bezplatné zkušební verzi Aspose.PSD.[tady](https://releases.aspose.com/).
### Jak mohu zakoupit Aspose.PSD?
 Aspose.PSD můžete zakoupit od[tady](https://purchase.aspose.com/buy).
### Kde mohu získat podporu pro Aspose.PSD?
Můžete hledat podporu a diskuse na[Asposeho fórum](https://forum.aspose.com/c/psd/34).