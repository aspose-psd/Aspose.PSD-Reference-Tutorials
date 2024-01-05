---
title: Ändra storlek på bild proportionellt med Aspose.PSD för Java
linktitle: Ändra storlek på bild proportionellt
second_title: Aspose.PSD Java API
description: Förbättra dina Java-applikationer med Aspose.PSD. Följ vår guide för att ändra storlek på bilder proportionellt utan ansträngning. Förbättra dina bildhanteringsmöjligheter idag.
type: docs
weight: 17
url: /sv/java/advanced-image-manipulation/resize-image-proportionally/
---
## Introduktion

Välkommen till vår steg-för-steg-guide för att ändra storlek på bilder proportionellt med Aspose.PSD för Java. Om du vill förbättra dina Java-applikationer med effektiva bildstorleksförändringar har du kommit till rätt ställe. I den här handledningen går vi igenom processen med tydliga och koncisa steg.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:

1. Java-miljö: Se till att du har Java installerat på ditt system.
2.  Aspose.PSD Library: Ladda ner och installera Aspose.PSD-biblioteket. Du kan hitta de nödvändiga resurserna[här](https://releases.aspose.com/psd/java/).

## Importera paket

När du har sorterat dina förutsättningar, importera de nödvändiga paketen till ditt Java-projekt. Se till att Aspose.PSD-biblioteket är korrekt refererat i ditt projekt.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## Steg 1: Ladda bilden

Börja med att ladda bilden du vill ändra storlek på i ditt Java-program.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## Steg 2: Ange bredd och höjd

Bestäm den nya bredden och höjden för din storleksändrade bild. I det här exemplet kommer vi att ändra storlek på bilden till hälften av dess ursprungliga dimensioner.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## Steg 3: Spara den ändrade storleken på bilden

Spara den ändrade storleken på bilden på önskad plats och ange formatalternativen (PNG, i det här fallet).

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Och där har du det! Du har lyckats ändra storlek på en bild proportionellt med Aspose.PSD för Java.

## Slutsats

I den här handledningen täckte vi de väsentliga stegen för att ändra storlek på bilder proportionellt med Aspose.PSD-biblioteket för Java. Nu kan du enkelt integrera denna funktion i dina Java-applikationer för förbättrad bildhantering.

## FAQ's

### F1: Är Aspose.PSD kompatibel med alla bildformat?

 S1: Aspose.PSD stöder olika bildformat, inklusive PSD, PNG, JPEG och mer. Kolla[dokumentation](https://reference.aspose.com/psd/java/) för en omfattande lista.

### F2: Kan jag använda Aspose.PSD för kommersiella projekt?

 A2: Ja, det kan du. Besök[köpsidan](https://purchase.aspose.com/buy) för licensinformation.

### F3: Finns tillfälliga licenser tillgängliga för teständamål?

 A3: Ja, du kan få en tillfällig licens[här](https://purchase.aspose.com/temporary-license/) för utvärdering.

### F4: Var kan jag hitta support för Aspose.PSD?

 A4: Besök[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34) för samhällsstöd och hjälp.

### F5: Hur kommer jag åt Aspose.PSD-dokumentationen?

 S5: Se den detaljerade dokumentationen[här](https://reference.aspose.com/psd/java/).
`