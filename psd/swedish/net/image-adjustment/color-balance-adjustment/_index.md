---
title: Tillämpa färgbalansjustering i Aspose.PSD för .NET
linktitle: Använder färgbalansjustering
second_title: Aspose.PSD .NET API
description: Förbättra PSD-bildfärger utan ansträngning med Aspose.PSD för .NETs funktion för färgbalansjustering. Följ vår steg-för-steg-guide för fantastiska resultat.
weight: 14
url: /sv/net/image-adjustment/color-balance-adjustment/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tillämpa färgbalansjustering i Aspose.PSD för .NET

## Introduktion

Välkommen till den här omfattande guiden om att tillämpa färgbalansjustering i Aspose.PSD för .NET! Aspose.PSD är ett kraftfullt .NET-bibliotek som låter utvecklare arbeta med PSD-filer effektivt. I den här handledningen kommer vi att fokusera på funktionen för justering av färgbalans, vilket gör att du enkelt kan förbättra färgbalansen i dina PSD-bilder.

## Förutsättningar

Innan vi dyker in i handledningen, se till att du har följande förutsättningar på plats:

-  Aspose.PSD för .NET Library: Ladda ner och installera biblioteket från[Aspose.PSD webbplats](https://releases.aspose.com/psd/net/).
- Utvecklingsmiljö: Se till att du har en fungerande .NET-utvecklingsmiljö inställd på din dator.
- PSD-fil: Ha en PSD-fil redo som du vill tillämpa färgbalansjusteringen på.

## Importera namnområden

I ditt .NET-projekt, inkludera de nödvändiga namnområdena för att använda Aspose.PSD-funktioner. Lägg till följande rader i din kod:

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

Låt oss nu dela upp färgbalansjusteringsprocessen i flera steg:

## Steg 1: Ladda PSD-filen

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    // Koden för färgbalansjusteringen kommer att läggas till i följande steg.
}
```

## Steg 2: Gå till och justera färgbalansen

```csharp
foreach (var layer in im.Layers)
{
    var cbLayer = layer as ColorBalanceAdjustmentLayer;
    if (cbLayer != null)
    {
        cbLayer.ShadowsCyanRedBalance = 30;
        cbLayer.ShadowsMagentaGreenBalance = -15;
        cbLayer.ShadowsYellowBlueBalance = 40;
        cbLayer.MidtonesCyanRedBalance = -90;
        cbLayer.MidtonesMagentaGreenBalance = -25;
        cbLayer.MidtonesYellowBlueBalance = 20;
        cbLayer.HighlightsCyanRedBalance = -30;
        cbLayer.HighlightsMagentaGreenBalance = 67;
        cbLayer.HighlightsYellowBlueBalance = -95;
        cbLayer.PreserveLuminosity = true;
    }
}
```

## Steg 3: Spara den justerade bilden

```csharp
im.Save(outputPath);
```

Nu har du framgångsrikt tillämpat Color Balance Adjustment på din PSD-fil med Aspose.PSD för .NET!

## Slutsats

Grattis! Du har lärt dig hur du förbättrar färgbalansen i dina PSD-bilder med Aspose.PSD för .NET. Experimentera med olika balansvärden för att uppnå önskade visuella effekter.

## FAQ's

### F1: Kan jag tillämpa Color Balance Adjustment på flera lager?

S1: Ja, du kan iterera genom alla lager i din PSD-fil och justera färgbalansen efter behov.

### F2: Är Aspose.PSD för .NET lämplig för batchbearbetning av PSD-filer?

A2: Absolut! Aspose.PSD tillhandahåller effektiva batchbearbetningsmöjligheter för PSD-filer.

### F3: Hur kan jag få en tillfällig licens för Aspose.PSD för .NET?

 A3: Besök[Aspose.PSD Temporary License](https://purchase.aspose.com/temporary-license/) för en tillfällig licens.

### F4: Var kan jag hitta fler exempel och dokumentation?

 A4: Utforska[Aspose.PSD-dokumentation](https://reference.aspose.com/psd/net/) för detaljerade exempel och guider.

### F5: Vilka supportalternativ finns tillgängliga för Aspose.PSD för .NET?

 A5: Besök[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34) för samhällsstöd och diskussioner.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
