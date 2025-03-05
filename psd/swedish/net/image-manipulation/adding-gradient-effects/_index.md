---
title: Lägga till gradienteffekter till bilder i Aspose.PSD för .NET
linktitle: Lägga till övertoningseffekter till bilder
second_title: Aspose.PSD .NET API
description: Förbättra dina bilder med fängslande gradienteffekter med Aspose.PSD för .NET. Följ vår steg-för-steg handledning för kreativa visuella transformationer.
type: docs
weight: 11
url: /sv/net/image-manipulation/adding-gradient-effects/
---
## Introduktion

Att förbättra bilder med gradienteffekter kan lägga till en fängslande dimension till ditt visuella innehåll. Aspose.PSD för .NET ger en kraftfull plattform för att integrera övertoningsöverlägg i dina bilder. I den här handledningen guidar vi dig genom processen att lägga till gradienteffekter med Aspose.PSD för .NET.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:

-  Aspose.PSD för .NET Library: Ladda ner och installera biblioteket från[Aspose.PSD för .NET-dokumentation](https://reference.aspose.com/psd/net/).
- .NET-miljö: Se till att du har en fungerande .NET-miljö inställd på din dator.

## Importera namnområden

Börja med att importera de nödvändiga namnrymden till ditt projekt:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
using System.IO;
```

## Steg 1: Ladda bilden och definiera sökvägar

```csharp
// Sökvägen till dokumentkatalogen.
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";

string sourceFileName = Path.Combine(SourceDir, "GradientOverlay.psd");
string exportPath = Path.Combine(OutputDir, "GradientOverlayChanged.psd");

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};
```

## Steg 2: Bekräfta initiala inställningar

Se till att de ursprungliga inställningarna för övertoningsöverlägget är som förväntat:

```csharp
using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    var gradientOverlay = (GradientOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

    // Påstående kontrollerar för initiala inställningar
    // ...

    // Färgpunkter
    // ...

    //Transparenspunkter
    // ...
}
```

## Steg 3: Ändra inställningar för övertoning

Justera inställningarna för gradientöverlagring enligt dina preferenser:

```csharp
// Testredigering
settings.Color = Color.Green;

gradientOverlay.Opacity = 193;
gradientOverlay.BlendMode = BlendMode.Lighten;

settings.AlignWithLayer = false;
settings.GradientType = GradientType.Radial;
settings.Angle = 45;
settings.Dither = true;
settings.HorizontalOffset = 15;
settings.VerticalOffset = 11;
settings.Reverse = true;

// Lägg till ny färgpunkt
// ...

// Ändra plats för föregående punkt
// ...

// Lägg till ny transparenspunkt
// ...

// Ändra plats för tidigare transparenspunkt
// ...

im.Save(exportPath);
```

## Steg 4: Validera redigerad fil

Kontrollera om ändringarna har tillämpats framgångsrikt:

```csharp
// Testfil efter redigering
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    var gradientOverlay = (GradientOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];
    try
    {
        // Påstående kontrollerar för ändrade inställningar
        // ...
    }
    catch (Exception e)
    {
        string ex = e.StackTrace;
    }
}
```

## Slutsats

Att lägga till gradienteffekter till bilder med Aspose.PSD för .NET öppnar upp en värld av kreativa möjligheter. Experimentera med olika inställningar för att uppnå önskad visuell effekt i dina bilder.

## FAQ's

### F1: Kan jag använda gradienteffekter på flera lager samtidigt?

S1: Ja, du kan tillämpa gradienteffekter på flera lager genom att iterera genom varje lager och tillämpa önskade inställningar.

### F2: Vilka filformat stöder Aspose.PSD för .NET?

S2: Aspose.PSD för .NET stöder olika bildfilformat, inklusive PSD, PNG, JPEG, BMP och GIF.

### F3: Finns det en testversion tillgänglig för Aspose.PSD för .NET?

S3: Ja, du kan utforska funktionerna hos Aspose.PSD för .NET genom att ladda ner den kostnadsfria testversionen från[här](https://releases.aspose.com/).

### F4: Hur kan jag få support för Aspose.PSD för .NET?

 S4: För all hjälp eller frågor, besök[Aspose.PSD för .NET Support Forum](https://forum.aspose.com/c/psd/34).

### F5: Var kan jag köpa Aspose.PSD för .NET?

 S5: Du kan köpa biblioteket från[Aspose.PSD för .NET-köpsida](https://purchase.aspose.com/buy).