---
title: Rita ellipser i Java
linktitle: Rita ellipser i Java
second_title: Aspose.PSD Java API
description: Lär dig hur du ritar ellipser i Java med Aspose.PSD för exakt grafisk design och bildmanipulation. Bemästra steg-för-steg tutorials.
weight: 15
url: /sv/java/java-graphics-drawing/drawing-ellipses/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rita ellipser i Java

## Introduktion
I den här handledningen kommer du att lära dig hur du ritar ellipser med Aspose.PSD för Java. Aspose.PSD är ett kraftfullt bibliotek som låter Java-utvecklare arbeta med PSD-filer och manipulera bilder med lätthet. Att rita former som ellipser är en grundläggande uppgift inom bildbehandling och grafisk design. Genom att följa den här guiden får du praktisk erfarenhet av att skapa ellipser programmatiskt med Aspose.PSD.
## Förutsättningar
Innan du börjar, se till att du har följande:
- Grundläggande kunskaper i Java-programmering.
- JDK (Java Development Kit) installerat på ditt system.
- Integrated Development Environment (IDE) som IntelliJ IDEA eller Eclipse.
-  Aspose.PSD för Java-bibliotek. Du kan ladda ner den från[här](https://releases.aspose.com/psd/java/).
## Importera paket
Först måste du importera nödvändiga paket från Aspose.PSD:
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
## Steg 1: Konfigurera ditt Java-projekt
Innan du börjar koda, se till att ditt Java-projekt är korrekt inställt med Aspose.PSD inkluderat som ett beroende.
## Steg 2: Skapa en instans av PsdImage
Initiera en ny instans av PsdImage med önskad bredd och höjd.
```java
Image image = new PsdImage(100, 100);
```
## Steg 3: Initiera grafikobjekt
Skapa och initiera en instans av grafik för att arbeta med bilden.
```java
Graphics graphics = new Graphics(image);
```
## Steg 4: Rensa grafikytan
Innan du ritar, rensa grafikytan med en specifik färg (valfritt).
```java
graphics.clear(Color.getYellow());
```
## Steg 5: Rita en prickad ellips
Använd ett Pen-objekt med en röd färg och rita en prickad ellips inom en angiven rektangel.
```java
graphics.drawEllipse(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
```
## Steg 6: Rita en kontinuerlig ellips
Skapa ett Pen-objekt med en solid blå pensel och rita en kontinuerlig ellips i en annan rektangel.
```java
graphics.drawEllipse(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
```
## Steg 7: Spara bilden
Slutligen, spara den genererade bilden i BMP-format till en angiven sökväg.
```java
String outputPath = "Your Document Directory/Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

## Slutsats
Grattis! Du har framgångsrikt lärt dig hur man ritar ellipser programmatiskt med Aspose.PSD för Java. Denna handledning behandlade hur du ställer in ditt projekt, initialiserar grafik, ritar prickade och kontinuerliga ellipser och sparar den resulterande bilden. Nu kan du integrera dessa tekniker i dina Java-applikationer för olika grafiska design- och bildmanipuleringsuppgifter.
## FAQ's
### Kan jag använda Aspose.PSD gratis?
Aspose.PSD erbjuder en gratis testversion, så att du kan utvärdera dess funktioner innan du köper.
### Var kan jag hitta fler exempel och dokumentation?
 Besök[Aspose.PSD-dokumentation](https://reference.aspose.com/psd/java/) för omfattande guider och exempel.
### Hur kan jag få tillfälliga licenser för Aspose.PSD?
 Tillfälliga licenser kan erhållas från[Aspose.PSD Temporary License](https://purchase.aspose.com/temporary-license/).
### Vilka format kan Aspose.PSD spara bilder till?
Aspose.PSD stöder att spara bilder i olika format inklusive BMP, PNG, JPEG och PSD.
### Är Aspose.PSD lämplig för företagsanvändning?
Ja, Aspose.PSD är designad för professionell bildbehandling och bildbehandlingsuppgifter på företagsnivå.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
