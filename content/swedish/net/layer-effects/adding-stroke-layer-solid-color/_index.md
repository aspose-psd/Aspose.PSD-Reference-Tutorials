---
title: Lägger till Stroke Layer med solid färg i Aspose.PSD för .NET
linktitle: Lägga till Stroke Layer med solid färg
second_title: Aspose.PSD .NET API
description: Förbättra dina färdigheter i .NET-bildmanipulering med Aspose.PSD. Lär dig att lägga till strecklager med solida färger steg för steg.
type: docs
weight: 11
url: /sv/net/layer-effects/adding-stroke-layer-solid-color/
---
## Introduktion

När det gäller .NET-utveckling är det ett vanligt krav att skapa visuellt tilltalande bilder. Aspose.PSD för .NET tillhandahåller en kraftfull uppsättning verktyg för att manipulera och förbättra bilder sömlöst. En av de väsentliga funktionerna är att lägga till ett strecklager med enfärgad färg, vilket ger liv och djup till dina bilder. I denna handledning guidar vi dig genom processen steg för steg med Aspose.PSD för .NET.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar:

- Grundläggande kunskap om .NET-utveckling.
- Visual Studio installerat på din dator.
- Aspose.PSD för .NET-bibliotek. Du kan ladda ner den från[webbplats](https://releases.aspose.com/psd/net/).

## Importera namnområden

Börja med att importera de nödvändiga namnområdena för att dra nytta av funktionaliteten i Aspose.PSD för .NET:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
```

## Steg 1: Ladda PSD-filen

Börja med att ladda PSD-filen som du vill förbättra med ett strecklager. Se till att du har rätt sökväg:

```csharp
string dataDir = "Your Document Directory";
string sourceFileName = dataDir + "Stroke.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // Kod för ytterligare steg kommer att läggas till här
}
```

## Steg 2: Få åtkomst till Stroke Effect Properties

Hämta egenskaperna för strokeeffekten från PSD-filen:

```csharp
var colorStroke = (StrokeEffect)im.Layers[1].BlendingOptions.Effects[0];

if ((colorStroke.BlendMode != BlendMode.Normal) ||
    (colorStroke.Opacity != 255) ||
    (colorStroke.IsVisible != true))
{
    throw new Exception("Color stroke effect was read wrong");
}
```

## Steg 3: Justera strokeinställningar

Ändra slaglängdsinställningarna enligt dina preferenser. I det här exemplet ändrar vi färgen till gul, ställer in opaciteten till 127 och använder färgblandningsläget:

```csharp
var fillSettings = (ColorFillSettings)colorStroke.FillSettings;

if ((fillSettings.Color != Color.Black) || (fillSettings.FillType != FillType.Color))
{
    throw new Exception("Color stroke effect settings were read wrong");
}

fillSettings.Color = Color.Yellow;
colorStroke.Opacity = 127;
colorStroke.BlendMode = BlendMode.Color;
```

## Steg 4: Spara den redigerade bilden

Spara bilden efter att du har tillämpat ändringarna i linjelagret:

```csharp
string exportPath = dataDir + "StrokeGradientChanged.psd";
im.Save(exportPath);
```

## Steg 5: Verifiera ändringarna

Se till att ändringarna tillämpas korrekt genom att ladda och inspektera den redigerade bilden:

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    // Kod för att verifiera ändringar kommer att läggas till här
}
```

Upprepa dessa steg för ytterligare justeringar eller experimentera med olika slageffekter för att uppnå önskad visuell effekt.

## Slutsats

Grattis! Du har framgångsrikt lärt dig hur du lägger till ett strecklager med enfärgad med Aspose.PSD för .NET. Denna kraftfulla funktion öppnar upp en värld av möjligheter för att förbättra dina bilder i .NET-miljön.

## Vanliga frågor

### F1: Är Aspose.PSD för .NET kompatibelt med de senaste .NET framework-versionerna?

S1: Ja, Aspose.PSD för .NET uppdateras regelbundet för att säkerställa kompatibilitet med de senaste .NET framework-versionerna.

### F2: Kan jag använda Aspose.PSD för .NET för kommersiella projekt?

A2: Absolut! Aspose.PSD för .NET är en kommersiell produkt, och du kan använda den i dina projekt genom att köpa en licens.

### F3: Var kan jag hitta fler exempel och dokumentation för Aspose.PSD för .NET?

 A3: Utforska[dokumentation](https://reference.aspose.com/psd/net/) för omfattande exempel och vägledning.

### F4: Finns det en gratis testversion tillgänglig för Aspose.PSD för .NET?

 A4: Ja, du kan få en gratis provperiod från[släpper sida](https://releases.aspose.com/).

### F5: Hur kan jag få support för Aspose.PSD för .NET?

 A5: Besök[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34) att söka hjälp och få kontakt med samhället.