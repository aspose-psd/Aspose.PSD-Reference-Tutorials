---
title: Rotera en bild i Aspose.PSD för .NET
linktitle: Rotera en bild
second_title: Aspose.PSD .NET API
description: Lär dig att rotera bilder utan ansträngning i .NET med Aspose.PSD. Följ vår steg-för-steg handledning.
weight: 15
url: /sv/net/image-manipulation/rotate-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rotera en bild i Aspose.PSD för .NET

## Introduktion

Om du dyker in i en värld av bildmanipulation med .NET, är Aspose.PSD ditt bästa verktyg för sömlös och effektiv bildbehandling. I den här handledningen kommer vi att fokusera på en grundläggande uppgift – att rotera en bild med Aspose.PSD för .NET. Följ med när vi delar upp processen i enkla, handlingsbara steg.

## Förutsättningar

Innan vi börjar, se till att du har följande förutsättningar på plats:

-  Aspose.PSD för .NET Library: Ladda ner och installera biblioteket från[Aspose.PSD .NET dokumentation](https://reference.aspose.com/psd/net/).

- Din dokumentkatalog: Skapa en katalog där dina bilder lagras. Ersätt "Din dokumentkatalog" i kodavsnittet med sökvägen till denna katalog.

## Importera namnområden

Se till att inkludera de nödvändiga namnområdena för att få tillgång till Aspose.PSD-funktionalitet. Lägg till följande rader i början av ditt .NET-projekt:

```csharp
using Aspose.PSD.ImageOptions;
```

## Steg 1: Ladda bilden

```csharp
string sourceFile = dataDir + @"sample.psd";

// Ladda en befintlig bild i en instans av RasterImage-klassen
using (Image image = Image.Load(sourceFile))
{
```

## Steg 2: Rotera bilden

```csharp
    // Rotera bilden 270 grader medurs
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Steg 3: Spara den roterade bilden

```csharp
    // Spara den roterade bilden som en JPEG-fil
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

Det är det! Med bara några rader kod har du framgångsrikt roterat en bild med Aspose.PSD för .NET.

## Slutsats

den här handledningen har vi utforskat grunderna för att rotera bilder med Aspose.PSD för .NET. Aspose.PSD tillhandahåller en robust uppsättning verktyg för bildmanipulering, vilket gör det till ett viktigt bibliotek för .NET-utvecklare. Experimentera med olika rotationer och utforska ytterligare funktioner för att förbättra dina arbetsflöden för bildbehandling.

## FAQ's

### F1: Kan jag rotera bilder med en anpassad vinkel med Aspose.PSD?

 Ja, Aspose.PSD låter dig ange en anpassad vinkel för rotation. Byt bara ut`RotateFlipType.Rotate270FlipNone` linje med önskad rotationsvinkel.

### F2: Är Aspose.PSD kompatibel med olika bildformat?

 Absolut. Aspose.PSD stöder ett brett utbud av bildformat, inklusive PSD, JPEG, PNG och mer. Kontrollera[dokumentation](https://reference.aspose.com/psd/net/) för hela listan.

### F3: Hur kan jag få en tillfällig licens för Aspose.PSD?

 Besök[sida för tillfällig licens](https://purchase.aspose.com/temporary-license/) på Asposes webbplats för att få en tillfällig licens för utvärderingsändamål.

### F4: Var kan jag hitta support för Aspose.PSD?

 För eventuella frågor eller hjälp, besök[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34) och få kontakt med samhället.

### F5: Kan jag köpa Aspose.PSD för kommersiellt bruk?

 Säkert. Utforska[köpsidan](https://purchase.aspose.com/buy) att skaffa en licens anpassad efter dina behov.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
