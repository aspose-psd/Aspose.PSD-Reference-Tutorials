---
title: Lägga till strokeeffekter till lager i Aspose.PSD för .NET
linktitle: Lägga till streckeffekter till lager
second_title: Aspose.PSD .NET API
description: Förbättra bildens estetik med Aspose.PSD för .NET. Lär dig att lägga till slageffekter steg för steg. Ladda ner, köp eller prova den kostnadsfria testversionen nu.
type: docs
weight: 10
url: /sv/net/layer-effects/adding-stroke-effects/
---
## Introduktion

Välkommen till denna steg-för-steg handledning om att lägga till streckeffekter till lager i Aspose.PSD för .NET. Att förbättra det visuella tilltalande av dina bilder är enkelt med stroke-effekten, och Aspose.PSD gör det sömlöst för .NET-utvecklare. I den här guiden leder vi dig genom processen och ger tydliga steg och exempel som hjälper dig att bemästra denna kraftfulla funktion.

## Förutsättningar

Innan vi dyker in i handledningen, se till att du har följande förutsättningar på plats:

- Aspose.PSD för .NET: Ladda ner och installera Aspose.PSD-biblioteket från[webbplats](https://releases.aspose.com/psd/net/).

- Dokumentkatalog: Förbered en katalog som innehåller det PSD-dokument som du vill använda streckeffekter på.

- Utdatakatalog: Ha en separat katalog för lagring av utdatabilder med streckeffekter.

- Visual Studio: Se till att du har Visual Studio eller någon annan föredragen .NET-utvecklingsmiljö inställd.

## Importera namnområden

I ditt .NET-projekt, inkludera de nödvändiga namnområdena för att utnyttja Aspose.PSD-funktionaliteten:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## Steg 1: Ladda PSD-dokumentet

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // Din kod för att ladda PSD-dokumentet går här
}
```

## Steg 2: Lägg till Color Stroke Effect

```csharp
// Lägger till färgfyllning vid position Inuti
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Steg 3: Yttre position

```csharp
// Lägger till färgfyllning vid position utanför
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Steg 4: Mittposition

```csharp
// Lägger till färgfyllning, vid position Center
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

Upprepa liknande steg för övertoning och mönsterfyllningar, justera inställningarna därefter.

## Slutsats

Grattis! Du har framgångsrikt lärt dig hur du lägger till streckeffekter i lager med Aspose.PSD för .NET. Experimentera med olika inställningar för att uppnå önskad visuell effekt i dina bilder.

## FAQ's

### F1: Kan jag tillämpa streckeffekter endast på specifika lager?

S1: Ja, du kan rikta in dig på specifika lager genom att justera lagerindexet i koden.

### F2: Är Aspose.PSD kompatibel med det senaste .NET-ramverket?

A2: Absolut! Aspose.PSD är designad för att sömlöst integreras med de senaste .NET-ramverken.

### F3: Hur kan jag anpassa streckfärgen?

 A3: Ändra helt enkelt`Color` egenskapen i koden för att uppnå önskad linjefärg.

### F4: Stöder Aspose.PSD batchbearbetning för flera PSD-filer?

S4: Ja, du kan loopa igenom flera PSD-filer och tillämpa streckeffekten med ett liknande tillvägagångssätt.

### F5: Kan jag använda testversionen innan jag köper Aspose.PSD?

 A5: Visst! Ta tag i[gratis provperiod](https://releases.aspose.com/) för att utforska Aspose.PSD:s möjligheter innan du gör ett köp.