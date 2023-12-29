---
title: Rotera en bild på en specifik vinkel i Aspose.PSD för .NET
linktitle: Rotera en bild i en specifik vinkel
second_title: Aspose.PSD .NET API
description: Utforska kraften i Aspose.PSD för .NET. Rotera bilder utan ansträngning i specifika vinklar. Ladda ner biblioteket och börja manipulera bilder sömlöst.
type: docs
weight: 16
url: /sv/net/image-manipulation/rotate-image-specific-angle/
---
Om du fördjupar dig i en värld av bildmanipulation med .NET, erbjuder Aspose.PSD en kraftfull lösning. I den här handledningen guidar vi dig genom processen att rotera en bild i en specifik vinkel med Aspose.PSD. Innan vi dyker in i stegen, låt oss sätta scenen med en introduktion.

## Introduktion

Aspose.PSD för .NET är ett mångsidigt bibliotek som gör det möjligt för utvecklare att arbeta med PSD- och rasterbildsformat sömlöst. En av dess nyckelfunktioner är förmågan att rotera bilder i exakta vinklar, vilket ger flexibilitet vid bildmanipulation. Denna handledning går igenom stegen för att rotera en bild i en specifik vinkel med Aspose.PSD för .NET.

## Förutsättningar

Innan vi ger oss ut på denna resa, se till att du har följande förutsättningar på plats:

-  Aspose.PSD för .NET Library: Ladda ner och installera biblioteket från[nedladdningssida](https://releases.aspose.com/psd/net/).
- Dokumentkatalog: Skapa en katalog för att lagra dina käll- och utdatafiler.

## Importera namnområden

För att komma igång, importera nödvändiga namnområden i ditt .NET-projekt:

```csharp
using Aspose.PSD.ImageOptions;
```

Låt oss nu dela upp exemplet i flera steg i ett steg-för-steg-guideformat.

## Steg 1: Ställ in din dokumentkatalog

```csharp
string dataDir = "Your Document Directory";
```

 Byta ut`"Your Document Directory"` med sökvägen till katalogen där du lagrar dina käll- och utdatafiler.

## Steg 2: Ladda bilden

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"RotatingImageOnSpecificAngle_out.jpg";

using (RasterImage image = (RasterImage)Image.Load(sourceFile))
{
    // Ytterligare steg kommer att infogas här
}
```

 Ladda bilden du vill rotera till en instans av`RasterImage`.

## Steg 3: Cachelagra bilddata

```csharp
if (!image.IsCached)
{
    image.CacheData();
}
```

Cachelagra bilddata för bättre prestanda under rotation.

## Steg 4: Rotera bilden

```csharp
image.Rotate(20f, true, Color.Red);
```

Rotera bilden 20 grader, bibehåll proportionell storlek och använd en röd bakgrund.

## Steg 5: Spara resultatet

```csharp
image.Save(destName, new JpegOptions());
```

Spara den roterade bilden med angivna alternativ (i det här fallet som en JPEG).

## Slutsats

 Grattis! Du har framgångsrikt roterat en bild i en specifik vinkel med Aspose.PSD för .NET. Det här biblioteket tillhandahåller en robust uppsättning verktyg för bildmanipulation, och den här handledningen är bara toppen av ett isberg. Utforska[dokumentation](https://reference.aspose.com/psd/net/) för fler funktioner och alternativ.

## FAQ's

### F1: Kan jag rotera bilder med andra vinklar än 20 grader?

 A1: Ja, du kan anpassa vinkelparametern i`image.Rotate` metod till valfritt värde.

### F2: Stöder Aspose.PSD andra bildformat än JPEG?

A2: Absolut! Aspose.PSD stöder ett brett utbud av format, inklusive PNG, GIF, BMP och TIFF.

### F3: Är cachning av bilddata nödvändigt före rotation?

S3: Även om det inte är obligatoriskt kan cachelagring av data förbättra prestandan avsevärt, särskilt för större bilder.

### F4: Var kan jag få support för Aspose.PSD-relaterade frågor?

 A4: Besök[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34) för samhällsstöd och diskussioner.

### F5: Kan jag prova Aspose.PSD innan jag köper?

 A5: Visst! Ta din[gratis provperiod](https://releases.aspose.com/) att utforska bibliotekets möjligheter.