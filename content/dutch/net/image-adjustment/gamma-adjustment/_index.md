---
title: Gamma-aanpassing implementeren in Aspose.PSD voor .NET
linktitle: Gamma-aanpassing implementeren
second_title: Aspose.PSD .NET-API
description: Ontdek de kracht van Aspose.PSD voor .NET met onze stapsgewijze handleiding voor het implementeren van Gamma-aanpassing. Stel de helderheid en het contrast van het beeld moeiteloos af.
type: docs
weight: 12
url: /nl/net/image-adjustment/gamma-adjustment/
---
## Invoering

Welkom bij deze uitgebreide handleiding over het implementeren van Gamma-aanpassing in Aspose.PSD voor .NET! Gamma-aanpassing is een cruciale beeldverwerkingstechniek waarmee u de helderheid en het contrast van een afbeelding kunt verfijnen. In deze zelfstudie leiden we u door het proces met behulp van de krachtige Aspose.PSD-bibliotheek voor .NET.

## Vereisten

Voordat u in de implementatie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

-  Aspose.PSD voor .NET-bibliotheek: Zorg ervoor dat de Aspose.PSD-bibliotheek voor .NET is geïnstalleerd. Je kunt het downloaden[hier](https://releases.aspose.com/psd/net/).

- .NET Framework: Deze tutorial gaat ervan uit dat je een basiskennis hebt van .NET-ontwikkeling en dat je het .NET Framework hebt geïnstalleerd.

- Integrated Development Environment (IDE): Kies de IDE van uw voorkeur voor .NET-ontwikkeling, zoals Visual Studio.

## Naamruimten importeren

Begin in uw .NET-project met het importeren van de benodigde naamruimten voor het werken met Aspose.PSD:

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## Stap 1: Stel uw project in

Maak een nieuw .NET-project in de door u gekozen IDE. Zorg ervoor dat u verwijzingen toevoegt aan de Aspose.PSD-bibliotheek.

## Stap 2: Definieer de documentmap

```csharp
string dataDir = "Your Document Directory";
```

## Stap 3: Laad de afbeelding

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    // Binnen dit gebruiksblok worden aanvullende stappen uitgevoerd.
}
```

## Stap 4: Casten naar RasterImage en cachegegevens

```csharp
RasterImage rasterImage = (RasterImage)image;
if (!rasterImage.IsCached)
{
    rasterImage.CacheData();
}
```

## Stap 5: Gamma aanpassen

```csharp
rasterImage.AdjustGamma(2.2f, 2.2f, 2.2f);
```

## Stap 6: Maak TiffOptions en sla op

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## Conclusie

Gefeliciteerd! U hebt Gamma-aanpassing met succes geïmplementeerd met Aspose.PSD voor .NET. Deze krachtige bibliotheek biedt robuuste mogelijkheden voor beeldverwerking, waardoor het een waardevol hulpmiddel is voor .NET-ontwikkelaars.

## Veelgestelde vragen

### V1: Waar kan ik de Aspose.PSD-documentatie vinden?

 A1: U kunt de documentatie raadplegen[hier](https://reference.aspose.com/psd/net/).

### V2: Hoe download ik Aspose.PSD voor .NET?

 A2: U kunt de bibliotheek downloaden.[hier](https://releases.aspose.com/psd/net/).

### Vraag 3: Is er een gratis proefversie beschikbaar?

 A3: Ja, u kunt een gratis proefperiode krijgen.[hier](https://releases.aspose.com/).

### V4: Waar kan ik ondersteuning krijgen voor Aspose.PSD?

 A4: U kunt het ondersteuningsforum bezoeken.[hier](https://forum.aspose.com/c/psd/34).

### Vraag 5: Heb ik een tijdelijke licentie nodig?

 A5: Indien nodig kunt u een tijdelijke licentie verkrijgen.[hier](https://purchase.aspose.com/temporary-license/).