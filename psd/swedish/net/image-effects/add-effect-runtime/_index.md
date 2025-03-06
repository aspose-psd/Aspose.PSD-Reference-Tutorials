---
title: Lägga till effekter vid körning i Aspose.PSD för .NET
linktitle: Lägga till effekter vid körning
second_title: Aspose.PSD .NET API
description: Utforska dynamiska bildförbättringar med Aspose.PSD för .NET. Lägg till effekter vid körning med lätthet.
weight: 10
url: /sv/net/image-effects/add-effect-runtime/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lägga till effekter vid körning i Aspose.PSD för .NET

## Introduktion

Att förbättra den visuella attraktionskraften hos bilder är ett vanligt krav i grafisk design och bildbehandlingsapplikationer. I den här handledningen kommer vi att utforska hur man lägger till effekter vid körning med Aspose.PSD för .NET. Aspose.PSD är ett kraftfullt API som låter utvecklare arbeta med Adobe Photoshop-filer sömlöst. 

## Förutsättningar

Innan vi dyker in i steg-för-steg-guiden, se till att du har följande:

- Grundläggande kunskaper i C# och .NET framework.
-  Aspose.PSD för .NET installerat. Du kan ladda ner den från[här](https://releases.aspose.com/psd/net/).

## Importera namnområden

För att komma igång, se till att du inkluderar de nödvändiga namnrymden i ditt C#-projekt. Dessa namnutrymmen är viktiga för att kunna använda funktionen som tillhandahålls av Aspose.PSD.

```csharp
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageLoadOptions;
```

## Steg 1: Konfigurera din dokumentkatalog

```csharp
string dataDir = "Your Document Directory";
```

Ersätt "Din dokumentkatalog" med den faktiska sökvägen där dina PSD-filer finns.

## Steg 2: Ladda PSD-bilden med Effects Resource

```csharp
string sourceFileName = dataDir + "ThreeRegularLayers.psd";
string exportPath = dataDir + "ThreeRegularLayersChanged.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
```

Detta steg laddar PSD-bilden, vilket möjliggör laddning av effektresurser.

## Steg 3: Lägg till färgöverlagringseffekt

```csharp
var effect = im.Layers[1].BlendingOptions.AddColorOverlay();
effect.Color = Color.Green;
effect.Opacity = 128;
effect.BlendMode = BlendMode.Normal;
```

Här lägger vi till en färgöverlagringseffekt till det andra lagret av PSD-bilden. Du kan anpassa färg, opacitet och blandningsläge efter dina önskemål.

## Steg 4: Spara den ändrade bilden

```csharp
im.Save(exportPath);
```

Spara slutligen bilden med den tillämpade effekten till den angivna exportsökvägen.

## Slutsats

Att lägga till effekter vid körning i Aspose.PSD för .NET är en enkel process. Med bara några rader kod kan du förbättra dina bilders visuella tilltalande dynamiskt. Experimentera med olika effekter och parametrar för att uppnå önskat resultat.

## FAQ's

### F1: Är Aspose.PSD kompatibel med det senaste .NET-ramverket?

S1: Ja, Aspose.PSD uppdateras regelbundet för att säkerställa kompatibilitet med de senaste .NET framework-versionerna.

### F2: Kan jag använda flera effekter på ett enda lager?

A2: Absolut! Du kan kedja flera effekter på ett lager för att skapa komplexa visuella förbättringar.

### F3: Finns det några begränsningar för vilka typer av effekter jag kan lägga till?

S3: Aspose.PSD erbjuder ett brett utbud av effekter, men det är tillrådligt att kontrollera dokumentationen för specifik information om effekter som stöds.

### F4: Hur kan jag få en tillfällig licens för teständamål?

 A4: Du kan få en tillfällig licens[här](https://purchase.aspose.com/temporary-license/) för testning och utvärdering.

### F5: Var kan jag hitta ytterligare stöd och diskussioner i samhället?

 A5: Besök[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34) för stöd och diskussioner.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
