---
title: Rita med hjälp av grafisk sökväg i Java
linktitle: Rita med hjälp av grafisk sökväg i Java
second_title: Aspose.PSD Java API
description: Lär dig hur du skapar komplex grafik i Java med Aspose.PSDs Graphics Path-klass. Denna handledning guidar dig genom varje steg för att skapa fantastiska bilder.
weight: 19
url: /sv/java/java-graphics-drawing/drawing-using-graphics-path/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rita med hjälp av grafisk sökväg i Java

## Introduktion
Att skapa och manipulera bilder programmatiskt kan vara en spännande uppgift för Java-utvecklare, särskilt när du använder bibliotek som Aspose.PSD. I den här handledningen kommer vi att dyka in i processen att rita komplex grafik med klassen Graphics Path i Java med Aspose.PSD.
## Förutsättningar
Innan vi går in i kodningsdelen, se till att du har följande förutsättningar:
1.  Java Development Kit (JDK): En stabil version av JDK installerad på din maskin. Du kan ladda ner den från[Oracles webbplats](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD for Java Library: Ladda ner Aspose.PSD for Java-biblioteket från[här](https://releases.aspose.com/psd/java/). Efter nedladdning, lägg till JAR-filen i ditt projekts klassväg.
3. Integrated Development Environment (IDE): Oavsett om det är Eclipse, IntelliJ IDEA eller något annat, behöver du en IDE för att skriva och köra Java-kod.
Med dessa förutsättningar på plats, låt oss utforska hur man skapar visuellt engagerande bilder med klassen Graphics Path.
## Importera paket
För att komma igång måste du importera nödvändiga paket:
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
Dessa importer ger tillgång till kärnfunktionaliteten som behövs för att skapa och manipulera bilder med Aspose.PSD.
## Steg 1: Initiera bild och grafik
Till att börja, låt oss skapa en ny bild och initiera ett grafikobjekt:
```java
PsdImage image = new PsdImage(500, 500);
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
```
Här skapar vi en bild på 500x500 pixlar och ett grafikobjekt för att rita.
## Steg 2: Skapa och konfigurera grafisk sökväg
 Därefter skapar vi en`GraphicsPath` objekt för att definiera ritbanan:
```java
GraphicsPath graphicspath = new GraphicsPath();
Figure figure = new Figure();
figure.addShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new TextShape("Aspose.PSD", new RectangleF(170, 225, 170, 100), new TextFont("Arial", 20), StringFormat.getGenericTypographic()));
Figure[] fig = { figure };
graphicspath.addFigures(fig);
```
I det här steget lägger vi till en cirkel, en rektangel och en textetikett till vår figur och lägger sedan till den här figuren i vår grafiska väg.
## Steg 3: Rita och fyll sökväg
Nu när vi har definierat vår väg kan vi rita och fylla den:
```java
graphics.drawPath(new Pen(Color.getBlue()), graphicspath);
HatchBrush hatchbrush = new HatchBrush();
hatchbrush.setBackgroundColor(Color.getBrown());
hatchbrush.setForegroundColor(Color.getBlue());
hatchbrush.setHatchStyle(HatchStyle.Vertical);
graphics.fillPath(hatchbrush, graphicspath);
```
det här steget ritar vi banan med en blå penna och fyller den med ett vertikalt kläckmönster med hjälp av en kläckborste.
## Steg 4: Spara bilden
Slutligen sparar du bilden till en fil:
```java
String dataDir = "Your Document Directory";
image.save(dataDir + "DrawingUsingGraphicsPath_output.psd");
```
Med detta sista steg är din bildskapande med hjälp av grafisk sökväg klar.
## Slutsats
Att skapa komplexa bilder med klassen Graphics Path med Aspose.PSD är både kraftfullt och engagerande. Genom att följa den här guiden kan du utöka din Java-applikations kapacitet inom grafisk design.
## FAQ's
### Vad är Aspose.PSD?
Aspose.PSD är ett bibliotek som låter utvecklare arbeta med Photoshop-filer och manipulera bildlager programmatiskt.
### Kan jag använda Aspose.PSD för andra format än PSD?
Från och med den här guiden handlar Aspose.PSD specifikt om PSD-filer men erbjuder tillägg för att hantera olika bildformat.
### Finns en testversion tillgänglig för Aspose.PSD?
 Ja, du kan få tillgång till en gratis testversion av Aspose.PSD[här](https://releases.aspose.com/).
### Hur kan jag köpa Aspose.PSD?
 Du kan köpa Aspose.PSD från[här](https://purchase.aspose.com/buy).
### Var kan jag få support för Aspose.PSD?
Du kan söka stöd och diskussioner om[Asposes forum](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
