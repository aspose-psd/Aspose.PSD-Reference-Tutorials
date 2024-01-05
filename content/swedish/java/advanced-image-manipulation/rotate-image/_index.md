---
title: Rotera en bild i Aspose.PSD för Java
linktitle: Rotera en bild
second_title: Aspose.PSD Java API
description: Utforska bildrotation i Java utan ansträngning med Aspose.PSD. Rotera, vänd och spara PSD-filer enkelt.
type: docs
weight: 19
url: /sv/java/advanced-image-manipulation/rotate-image/
---
## Introduktion

Aspose.PSD för Java tillhandahåller en kraftfull uppsättning funktioner för att arbeta med bilder, vilket gör det möjligt för utvecklare att effektivt manipulera och bearbeta PSD-filer. I den här handledningen kommer vi att fokusera på en specifik uppgift: att rotera en bild. Oavsett om du bygger ett fotoredigeringsprogram eller helt enkelt behöver justera orienteringen på en bild, gör Aspose.PSD processen enkel.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:

-  Aspose.PSD for Java Library: Se till att du har laddat ner och installerat Aspose.PSD for Java-biblioteket. Du hittar biblioteket och detaljerad dokumentation[här](https://reference.aspose.com/psd/java/).

- Java-utvecklingsmiljö: Se till att du har en Java-utvecklingsmiljö inställd på din maskin.

-  Exempel PSD-fil: Förbered en exempel-PSD-fil som du vill rotera. Justera`sourceFile` variabel i exempelkoden med sökvägen till din PSD-fil.

## Importera paket

Börja med att importera de nödvändiga paketen för att utnyttja funktionerna i Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Steg 1: Ladda bilden

 Ladda den befintliga bilden i en instans av`Image` klass:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Steg 2: Rotera bilden

 Rotera bilden med hjälp av`rotateFlip` metod. I det här exemplet roterar vi bilden 270 grader:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Steg 3: Spara den roterade bilden

 Spara den roterade bilden med hjälp av`save` metod och ange utdataformatet (JPEG, i det här fallet):

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## Slutsats

Grattis! Du har framgångsrikt roterat en bild med Aspose.PSD för Java. Detta enkla men kraftfulla bibliotek öppnar upp en värld av möjligheter för bildmanipulation i dina Java-applikationer.

## FAQ's

### F1: Är Aspose.PSD kompatibel med olika bildformat?

S1: Ja, Aspose.PSD stöder olika bildformat, inklusive PSD, JPEG, PNG och mer.

### F2: Kan jag använda anpassade rotationer, inte bara fördefinierade vändningar?

A2: Absolut! Aspose.PSD ger flexibilitet för att tillämpa anpassade rotationer för att möta dina specifika krav.

### F3: Var kan jag hitta ytterligare stöd eller hjälp?

 S3: För eventuella frågor eller problem, besök[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34) för samhällsstöd.

### F4: Finns det en gratis provperiod?

 A4: Ja, du kan utforska Aspose.PSD med en[gratis provperiod](https://releases.aspose.com/).

### F5: Hur får jag en tillfällig licens?

 S5: Om du behöver en tillfällig licens kan du få en[här](https://purchase.aspose.com/temporary-license/).