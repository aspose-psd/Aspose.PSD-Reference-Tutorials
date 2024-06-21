---
title: Lägg till ett nytt vanligt lager till PSD med Aspose.PSD för Java
linktitle: Lägg till ett nytt vanligt lager till PSD
second_title: Aspose.PSD Java API
description: Lär dig hur du lägger till ett nytt vanligt lager till PSD-filer med Aspose.PSD för Java. Följ vår steg-för-steg-guide för sömlös PSD-manipulation.
type: docs
weight: 11
url: /sv/java/advanced-image-effects/add-new-regular-layer/
---
## Introduktion

Välkommen till denna omfattande handledning om hur du använder Aspose.PSD för Java för att lägga till ett nytt vanligt lager till en PSD-fil. Aspose.PSD är ett kraftfullt Java-bibliotek som tillåter utvecklare att manipulera och arbeta med PSD-filer effektivt. I den här handledningen guidar vi dig genom processen att lägga till ett nytt vanligt lager till en PSD-fil, med detaljerade steg och kodexempel.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:

- Java-utvecklingsmiljö: Se till att du har en Java-utvecklingsmiljö inställd på ditt system.
-  Aspose.PSD Library: Ladda ner och installera Aspose.PSD för Java-biblioteket. Du hittar biblioteket[här](https://releases.aspose.com/psd/java/).

## Importera paket

För att komma igång, importera nödvändiga paket till ditt Java-projekt. Dessa paket är viktiga för att arbeta med Aspose.PSD-funktioner. Inkludera följande rader i början av din Java-fil:

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Steg 1: Ladda PSD-fil

Ladda PSD-filen du vill redigera med följande kod:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Steg 2: Förbered datamatriser och rektanglar

Förbered två int-matriser och två rektangelobjekt enligt följande:

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## Steg 3: Initiera lagerdata

Initiera datamatriser med ett standardvärde:

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## Steg 4: Lägg till vanliga lager

Lägg till två vanliga lager till PSD-bilden:

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

## Steg 5: Spara PSD och PNG

Spara den modifierade PSD:n och ytterligare en PNG-fil:

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

Grattis! Du har framgångsrikt lagt till ett nytt vanligt lager till en PSD-fil med Aspose.PSD för Java.

## Slutsats

I den här handledningen täckte vi processen att lägga till ett nytt vanligt lager till en PSD-fil med Aspose.PSD för Java. Detta kraftfulla bibliotek förenklar PSD-manipulation, vilket gör det tillgängligt för Java-utvecklare. Experimentera med olika parametrar och funktioner för att utforska den fulla potentialen av Aspose.PSD.

## FAQ's

### F1: Är Aspose.PSD kompatibel med Java 8?

S1: Ja, Aspose.PSD stöder Java 8 och senare versioner.

### F2: Kan jag tillämpa transformationer på de tillagda lagren?

A2: Absolut! Aspose.PSD tillhandahåller en rad transformationsalternativ för lager.

### F3: Var kan jag hitta ytterligare Aspose.PSD-dokumentation?

 S3: Du kan hänvisa till dokumentationen.[här](https://reference.aspose.com/psd/java/).

### F4: Hur kan jag få en tillfällig licens för Aspose.PSD?

 A4: Besök[den här länken](https://purchase.aspose.com/temporary-license/) för tillfälliga licensalternativ.

### F5: Finns det några forum för Aspose.PSD-stöd?

 A5: Ja, du kan hitta stöd och diskussioner.[här](https://forum.aspose.com/c/psd/34).