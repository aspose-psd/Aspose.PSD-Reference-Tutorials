---
title: Beskär bilder med Shifts i Aspose.PSD för .NET
linktitle: Beskär bilder med Shifts
second_title: Aspose.PSD .NET API
description: Lär dig att beskära bilder utan ansträngning med Aspose.PSD för .NET. Följ vår steg-för-steg-guide för exakta bildjusteringar.
type: docs
weight: 12
url: /sv/net/image-manipulation/crop-image-shifts/
---
## Introduktion

Inom .NET-utvecklingens område framstår Aspose.PSD som en kraftfull verktygslåda för bildbehandlingsuppgifter. En av dess anmärkningsvärda egenskaper är möjligheten att beskära bilder med precision, tack vare funktionen "Cropping by Shifts". I den här steg-för-steg-guiden går vi igenom processen att beskära bilder sömlöst med Aspose.PSD för .NET.

## Förutsättningar

Innan du fördjupar dig i handledningen, se till att du har följande förutsättningar på plats:

-  Aspose.PSD för .NET Library: Se till att du har biblioteket installerat. Om inte kan du ladda ner den från[släpp sida](https://releases.aspose.com/psd/net/).

- .NET-miljö: Se till att du har en .NET-utvecklingsmiljö inställd på din dator.

- Exempelbild: Förbered en exempelbild i PSD-format som du vill arbeta med.

## Importera namnområden

Börja med att importera de nödvändiga namnområdena till ditt .NET-projekt. Dessa namnrymder ger tillgång till Aspose.PSD-klasserna och metoderna som krävs för bildbeskärning.

```csharp
using Aspose.PSD.ImageOptions;
```

## Steg 1: Definiera din dokumentkatalog

Ställ in sökvägen till din dokumentkatalog där käll- och målfilerna kommer att finnas.

```csharp
string dataDir = "Your Document Directory";
```

## Steg 2: Ladda källbilden

Ladda PSD-bilden som du vill beskära. Se till att ersätta "sample.psd" med namnet på din källfil.

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"CroppingByShifts_out.jpg";
```

## Steg 3: Cachelagra bilddata för bättre prestanda

Innan du beskär, är det lämpligt att cachelagra bilddata för förbättrad prestanda.

```csharp
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
```

## Steg 4: Definiera skiftvärden för beskärning

Ange skiftvärdena för vänster, höger, övre och nedre sidor av bilden. Justera dessa värden baserat på dina beskärningskrav.

```csharp
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

## Steg 5: Använd beskärning och spara resultat

 Använd`Crop` metod för att tillämpa de angivna skiftningarna och spara den beskurna bilden till målfilen.

```csharp
rasterImage.Crop(leftShift, rightShift, topShift, bottomShift);
rasterImage.Save(destName, new JpegOptions());
}
```

## Slutsats

Grattis! Du har framgångsrikt lärt dig att beskära bilder genom skiftningar med Aspose.PSD för .NET. Denna kraftfulla funktion ger dig den precision och kontroll som behövs för olika bildbehandlingsuppgifter.

## FAQ's

### F1: Kan jag beskära bilder i olika format, inte bara PSD?

S1: Ja, Aspose.PSD stöder olika bildformat, så att du kan beskära bilder i format som JPEG, PNG och mer.

### F2: Finns det en testversion innan du köper Aspose.PSD för .NET?

 A2: Visst! Du kan utforska verktygslådan med en gratis provversion tillgänglig[här](https://releases.aspose.com/).

### F3: Hur får jag en tillfällig licens för Aspose.PSD för .NET?

 S3: Du kan skaffa en tillfällig licens för teständamål.[här](https://purchase.aspose.com/temporary-license/).

### F4: Var kan jag hitta ytterligare stöd och diskussioner relaterade till Aspose.PSD?

 A4: Besök[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34) för stöd och engagerande diskussioner.

### F5: Kan jag köpa Aspose.PSD för .NET direkt från webbplatsen?

 S5: Ja, du kan köpa biblioteket säkert från[köpsidan](https://purchase.aspose.com/buy).
