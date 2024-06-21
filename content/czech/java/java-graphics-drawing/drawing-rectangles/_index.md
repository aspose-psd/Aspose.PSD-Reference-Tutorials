---
title: Kreslení obdélníků v Javě
linktitle: Kreslení obdélníků v Javě
second_title: Aspose.PSD Java API
description: Naučte se kreslit obdélníky na obrázky pomocí Aspose.PSD pro Java. Tento tutoriál krok za krokem provede vývojáře Java. Ideální pro úkoly manipulace s obrázky.
type: docs
weight: 17
url: /cs/java/java-graphics-drawing/drawing-rectangles/
---
## Úvod
Ve světě vývoje v Javě je manipulace a programové generování obrázků běžným požadavkem napříč různými aplikacemi. Jedním z takových úkolů, se kterými se často setkáváme, je kreslení tvarů, jako jsou obdélníky, na obrázky. Aspose.PSD for Java poskytuje robustní sadu nástrojů a funkcí, jak toho dosáhnout efektivně. Tento tutoriál vás krok za krokem provede procesem kreslení obdélníků na obrázek pomocí Aspose.PSD for Java.
## Předpoklady
Než se pustíte do výukového programu, ujistěte se, že máte nastaveny následující předpoklady:
### Vývojové prostředí Java
Ujistěte se, že máte v systému nainstalovanou sadu Java Development Kit (JDK), nejlépe JDK 8 nebo vyšší.
### Aspose.PSD pro Javu
 Musíte mít Aspose.PSD pro Java knihovnu. Můžete si jej stáhnout z[Aspose.PSD pro stahování Java stránky](https://releases.aspose.com/psd/java/) a postupujte podle pokynů k instalaci uvedených v jejich dokumentaci.
## Importujte balíčky
Chcete-li začít, importujte potřebné balíčky Aspose.PSD for Java do vašeho souboru Java:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
Tyto importy vám umožní přístup ke třídám a metodám potřebným pro kreslení obdélníků na obrázky.
## Krok 1: Vytvořte nový obrázek
 Nejprve vytvořte novou instanci souboru`PsdImage` třídy s konkrétní šířkou a výškou.
```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Vytvořte instanci BmpOptions a nastavte její vlastnosti
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Vytvořte instanci PsdImage se zadanými rozměry
Image image = new PsdImage(100, 100);
```
 V tomto kroku`PsdImage` je inicializována s šířkou a výškou 100 pixelů.
## Krok 2: Inicializujte grafický objekt
 Dále inicializujte a`Graphics` objekt pomocí`image` vytvořené v předchozím kroku.
```java
// Inicializujte grafický objekt
Graphics graphic = new Graphics(image);
```
 Tento`Graphics`objekt bude použit k provádění operací kreslení na obrázku.
## Krok 3: Vyčistěte grafický povrch
Vyčistěte grafický povrch obrázku pomocí určité barvy.
```java
// Čirý grafický povrch se žlutou barvou
graphic.clear(Color.YELLOW);
```
Tím nastavíte pozadí obrázku na žluté.
## Krok 4: Nakreslete obdélníky
Nyní nakreslete na obrázek obdélníky pomocí různých barev a rozměrů.
```java
// Nakreslete červený obdélník
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Nakreslete modrý obdélník
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
Tyto příkazy kreslí obdélníky se zadanými barvami (červená a modrá) a pozicemi na obrázku.
## Krok 5: Exportujte obrázek
Nakonec upravený obrázek uložte do souboru ve formátu BMP.
```java
// Export obrázku do formátu souboru BMP
image.save(outpath, saveOptions);
```
 Tím se obrázek s nakreslenými obdélníky uloží do souboru BMP určeného pomocí`outpath`.

## Závěr
Programové kreslení obdélníků na obrázky v Javě pomocí Aspose.PSD pro Javu je se správnými nástroji a knihovnami přímočaré. Podle tohoto kurzu jste se naučili, jak inicializovat obrázek, manipulovat s grafickými objekty, kreslit tvary a uložit upravený obrázek do souboru. Experimentování s různými tvary, barvami a rozměry dále zlepší vaše chápání manipulace s obrázky v Javě.
## FAQ
### Dokáže Aspose.PSD for Java zpracovat jiné tvary kromě obdélníků?
Aspose.PSD for Java podporuje kromě obdélníků kreslení různých tvarů, jako jsou elipsy, čáry a mnohoúhelníky.
### Jak mohu upravit tloušťku okraje obdélníku?
 Tloušťku okraje obdélníku můžete upravit nastavením`Pen` vlastnost tloušťky.
### Je Aspose.PSD for Java vhodný pro vysoce výkonné úlohy zpracování obrazu?
Ano, Aspose.PSD for Java je navržen pro vysoce výkonné zpracování obrazu s rozsáhlými funkcemi pro jednoduché i složité operace.
### Kde najdu další příklady a návody pro Aspose.PSD pro Javu?
 Další příklady a podrobnou dokumentaci můžete prozkoumat na[Aspose.PSD pro dokumentaci Java](https://reference.aspose.com/psd/java/).
### Podporuje Aspose.PSD for Java jiné obrazové formáty kromě BMP?
Ano, Aspose.PSD for Java podporuje širokou škálu obrazových formátů včetně PNG, JPEG, TIFF a GIF.