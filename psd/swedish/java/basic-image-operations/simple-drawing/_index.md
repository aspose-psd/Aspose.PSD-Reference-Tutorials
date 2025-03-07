---
title: Utför enkel ritning med Aspose.PSD för Java
linktitle: Utför enkel ritning
second_title: Aspose.PSD Java API
description: Lär dig hur du ritar former i PSD-filer med Aspose.PSD för Java. Den här steg-för-steg-guiden täcker att skapa, lägga till lager och rita med kodexempel.
weight: 10
url: /sv/java/basic-image-operations/simple-drawing/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Utför enkel ritning med Aspose.PSD för Java

## Introduktion

Välkommen till denna steg-för-steg-guide för att utföra enkel ritning med Aspose.PSD för Java! I den här handledningen kommer vi att utforska grunderna för att skapa ett nytt PSD-dokument, lägga till lager och rita former med olika färger. Aspose.PSD för Java är ett kraftfullt bibliotek som gör att du kan manipulera PSD-filer programmatiskt, vilket ger omfattande funktionalitet för grafiska designuppgifter.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:

- Java Development Kit (JDK) installerat på din maskin.
- Aspose.PSD för Java-bibliotek. Du kan ladda ner den från[Aspose.PSD för Java-dokumentation](https://reference.aspose.com/psd/java/).

## Importera paket

För att komma igång, importera nödvändiga paket till ditt Java-projekt. Inkludera följande kod i början av din Java-fil:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Steg 1: Skapa ett nytt dokument

Låt oss börja med att skapa ett nytt PSD-dokument med en specificerad bredd och höjd:

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Steg 2: Lägg till ett lager

Låt oss nu lägga till ett lager i dokumentet med hjälp av no-argument-konstruktorn:

```java
//ExStart: AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd: AddLayer
```

## Steg 3: Rita former

I det här steget kommer vi att använda klassen Graphics för att rita former på det skapade lagret:

### Rita en rektangel med en gul färg

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Rita en röd rektangel

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### Rita en blå rektangel

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Steg 4: Spara ändringarna

Slutligen, spara en kopia av den laddade PSD-filen inklusive ändringarna:

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## Slutsats

Grattis! Du har framgångsrikt utfört enkel ritning med Aspose.PSD för Java. Denna handledning omfattade att skapa ett nytt dokument, lägga till lager och rita rektanglar med olika färger. Utforska gärna mer avancerade funktioner som biblioteket erbjuder för dina grafiska designbehov.

## FAQ's

### F1: Kan jag använda Aspose.PSD för Java för att manipulera befintliga PSD-filer?

S1: Ja, Aspose.PSD för Java tillhandahåller omfattande funktionalitet för att redigera och manipulera befintliga PSD-filer.

### F2: Var kan jag hitta support för Aspose.PSD för Java?

 A2: Du kan besöka[Aspose.PSD för Java-forum](https://forum.aspose.com/c/psd/34) för alla supportrelaterade frågor.

### F3: Finns det en gratis testversion tillgänglig för Aspose.PSD för Java?

 A3: Ja, du kan komma åt den kostnadsfria testversionen[här](https://releases.aspose.com/).

### F4: Hur kan jag köpa en licens för Aspose.PSD för Java?

 A4: Du kan köpa en licens från[Aspose.PSD köpsida](https://purchase.aspose.com/buy).

### F5: Finns tillfälliga licenser tillgängliga för Aspose.PSD för Java?

 S5: Ja, du kan få en tillfällig licens från[här](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
