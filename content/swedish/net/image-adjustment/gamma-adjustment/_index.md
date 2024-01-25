---
title: Implementering av gammajustering i Aspose.PSD för .NET
linktitle: Implementering av gammajustering
second_title: Aspose.PSD .NET API
description: Utforska kraften i Aspose.PSD för .NET med vår steg-för-steg-guide för implementering av Gamma Adjustment. Finjustera bildens ljusstyrka och kontrast utan ansträngning.
type: docs
weight: 12
url: /sv/net/image-adjustment/gamma-adjustment/
---
## Introduktion

Välkommen till denna omfattande guide om implementering av Gamma Adjustment i Aspose.PSD för .NET! Gammajustering är en avgörande bildbehandlingsteknik som låter dig finjustera ljusstyrkan och kontrasten i en bild. I den här handledningen går vi igenom processen med det kraftfulla Aspose.PSD-biblioteket för .NET.

## Förutsättningar

Innan du går in i implementeringen, se till att du har följande förutsättningar på plats:

-  Aspose.PSD for .NET Library: Se till att du har Aspose.PSD-biblioteket för .NET installerat. Du kan ladda ner den[här](https://releases.aspose.com/psd/net/).

- .NET Framework: Denna handledning förutsätter att du har en grundläggande förståelse för .NET-utveckling och har .NET Framework installerat.

- Integrated Development Environment (IDE): Välj din föredragna IDE för .NET-utveckling, som Visual Studio.

## Importera namnområden

ditt .NET-projekt börjar du med att importera de nödvändiga namnrymden för att arbeta med Aspose.PSD:

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## Steg 1: Konfigurera ditt projekt

Skapa ett nytt .NET-projekt i din valda IDE. Se till att lägga till referenser till Aspose.PSD-biblioteket.

## Steg 2: Definiera dokumentkatalogen

```csharp
string dataDir = "Your Document Directory";
```

## Steg 3: Ladda bilden

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    // Ytterligare steg kommer att utföras i detta block.
}
```

## Steg 4: Casta till RasterImage och cachedata

```csharp
RasterImage rasterImage = (RasterImage)image;
if (!rasterImage.IsCached)
{
    rasterImage.CacheData();
}
```

## Steg 5: Justera gamma

```csharp
rasterImage.AdjustGamma(2.2f, 2.2f, 2.2f);
```

## Steg 6: Skapa TiffOptions och spara

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## Slutsats

Grattis! Du har framgångsrikt implementerat Gamma Adjustment med Aspose.PSD för .NET. Detta kraftfulla bibliotek ger robusta funktioner för bildbehandling, vilket gör det till ett värdefullt verktyg för .NET-utvecklare.

## FAQ's

### F1: Var kan jag hitta Aspose.PSD-dokumentationen?

 S1: Du kan hänvisa till dokumentationen[här](https://reference.aspose.com/psd/net/).

### F2: Hur laddar jag ner Aspose.PSD för .NET?

 A2: Du kan ladda ner biblioteket[här](https://releases.aspose.com/psd/net/).

### F3: Finns det en gratis provperiod?

 A3: Ja, du kan få en gratis provperiod[här](https://releases.aspose.com/).

### F4: Var kan jag få support för Aspose.PSD?

 S4: Du kan besöka supportforumet[här](https://forum.aspose.com/c/psd/34).

### F5: Behöver jag en tillfällig licens?

 S5: Om det behövs kan du få en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).