---
title: Ändra storlek med Resize Type Enumeration i Aspose.PSD för Java
linktitle: Ändra storlek med Resize Type Enumeration
second_title: Aspose.PSD Java API
description: Master bildstorleksändring i Java med Aspose.PSD. Steg-för-steg-guide med hjälp av Resize Type Enumeration.
type: docs
weight: 18
url: /sv/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
---
## Introduktion

I det ständigt föränderliga landskapet för Java-utveckling är effektiv bildbehandling en avgörande aspekt som utvecklare ofta brottas med. Aspose.PSD för Java framstår som en kraftfull lösning, som ger en sömlös upplevelse för att ändra storlek på bilder med den extra fördelen av Resize Type Enumeration. I den här handledningen kommer vi att fördjupa oss i krångligheterna med att ändra storlek på bilder med Aspose.PSD för Java, och bryta ner varje steg för att säkerställa en heltäckande förståelse.

## Förutsättningar

Innan du börjar med denna handledning, se till att du har följande förutsättningar på plats:

1. Java-utvecklingsmiljö: Se till att du har en Java-utvecklingsmiljö inställd på din maskin.

2. Aspose.PSD Library: Ladda ner och installera Aspose.PSD-biblioteket från[webbplats](https://releases.aspose.com/psd/java/).

3.  Exempel PSD-fil: Ha en exempel-PSD-fil redo för experiment. Du kan använda[sample.psd](Din dokumentkatalog/sample.psd)-fil för den här handledningen.

## Importera paket

För att börja, importera de nödvändiga paketen till ditt Java-projekt:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Steg 1: Ladda bilden

 Börja med att ladda en befintlig bild i en instans av`RasterImage` klass. Använd följande kodavsnitt:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Ladda en befintlig bild i en instans av RasterImage-klassen
Image image = Image.load(sourceFile);
```

## Steg 2: Ändra storlek på bilden

Ändra nu storleken på den laddade bilden med hjälp av resize Type Enumeration. I det här exemplet använder vi Lanczos Resample-metoden:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Steg 3: Spara den ändrade storleken på bilden

Efter storleksändring, spara bilden med de angivna måtten och den valda storleksändringstypen. Här sparar vi den som en JPEG-fil:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

Och där har du det! Du har lyckats ändra storlek på en bild med hjälp av resize Type Enumeration i Aspose.PSD för Java.

Sammanfattningsvis ger Aspose.PSD för Java en robust plattform för bildmanipulering, och Resize Type Enumeration lägger till ett lager av flexibilitet till denna process. Oavsett om du arbetar med ett litet projekt eller en storskalig applikation, kommer att behärska dessa steg ge dig möjlighet att hantera bildstorleksändring sömlöst.

## FAQ's

### F1: Är Aspose.PSD för Java lämplig för både små och stora projekt?

A1: Absolut! Aspose.PSD för Java är designad för att tillgodose projekt av alla storlekar, vilket ger skalbarhet och effektivitet.

### F2: Kan jag använda en annan storleksändringstyp än Lanczos Resample?

S2: Ja, Aspose.PSD för Java erbjuder olika storleksändringstyper, till exempel Nearest Neighbour, Bicubic och mer. Utforska dokumentationen för en omfattande lista.

### F3: Var kan jag hitta ytterligare stöd för Aspose.PSD för Java?

 S3: För eventuella frågor eller hjälp, besök[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34).

### F4: Finns det en gratis testversion tillgänglig för Aspose.PSD för Java?

 A4: Ja, du kan få tillgång till en gratis testversion[här](https://releases.aspose.com/).

### F5: Hur kan jag få en tillfällig licens för Aspose.PSD för Java?

 S5: För att få en tillfällig licens, besök[denna länk](https://purchase.aspose.com/temporary-license/).