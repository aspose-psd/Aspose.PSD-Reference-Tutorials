---
title: Lijneffecten toevoegen aan lagen in Aspose.PSD voor .NET
linktitle: Lijneffecten aan lagen toevoegen
second_title: Aspose.PSD .NET-API
description: Verbeter de beeldesthetiek met Aspose.PSD voor .NET. Leer stap voor stap hoe u streekeffecten kunt toevoegen. Download, koop of probeer nu de gratis proefversie.
type: docs
weight: 10
url: /nl/net/layer-effects/adding-stroke-effects/
---
## Invoering

Welkom bij deze stapsgewijze zelfstudie over het toevoegen van streekeffecten aan lagen in Aspose.PSD voor .NET. Het verbeteren van de visuele aantrekkingskracht van uw afbeeldingen is een fluitje van een cent met het lijneffect, en Aspose.PSD maakt het naadloos voor .NET-ontwikkelaars. In deze handleiding leiden we u door het proces en geven we duidelijke stappen en voorbeelden om u te helpen deze krachtige functie onder de knie te krijgen.

## Vereisten

Voordat we ingaan op de tutorial, zorg ervoor dat je aan de volgende vereisten voldoet:

- Aspose.PSD voor .NET: Download en installeer de Aspose.PSD-bibliotheek van de[website](https://releases.aspose.com/psd/net/).

- Documentmap: bereid een map voor met het PSD-document waarop u streekeffecten wilt toepassen.

- Uitvoermap: Zorg voor een aparte map voor het opslaan van de uitvoerafbeeldingen met lijneffecten.

- Visual Studio: Zorg ervoor dat u Visual Studio of een andere .NET-ontwikkelomgeving van uw voorkeur hebt ingesteld.

## Naamruimten importeren

Neem in uw .NET-project de benodigde naamruimten op om de Aspose.PSD-functionaliteit te benutten:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## Stap 1: Laad het PSD-document

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // Hier vindt u uw code voor het laden van het PSD-document
}
```

## Stap 2: Voeg een kleurstreekeffect toe

```csharp
// Voegt kleurvulling toe, op positie Binnen
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Stap 3: Buitenpositie

```csharp
// Voegt kleurvulling toe, op positie Buiten
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Stap 4: Middenpositie

```csharp
// Voegt kleurvulling toe, op positie Midden
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

Herhaal soortgelijke stappen voor verloop- en patroonvullingen en pas de instellingen dienovereenkomstig aan.

## Conclusie

Gefeliciteerd! U hebt met succes geleerd hoe u streekeffecten aan lagen kunt toevoegen met Aspose.PSD voor .NET. Experimenteer met verschillende instellingen om de gewenste visuele impact in uw afbeeldingen te bereiken.

## Veelgestelde vragen

### Vraag 1: Kan ik streekeffecten alleen op specifieke lagen toepassen?

A1: Ja, u kunt specifieke lagen targeten door de laagindex in de code aan te passen.

### Vraag 2: Is Aspose.PSD compatibel met het nieuwste .NET-framework?

A2: Absoluut! Aspose.PSD is ontworpen om naadloos te integreren met de nieuwste .NET-frameworks.

### Vraag 3: Hoe kan ik de streekkleur aanpassen?

 A3: Wijzig eenvoudigweg de`Color` eigenschap in de code om de gewenste lijnkleur te bereiken.

### V4: Ondersteunt Aspose.PSD batchverwerking voor meerdere PSD-bestanden?

A4: Ja, u kunt meerdere PSD-bestanden doorlopen en het lijneffect op een vergelijkbare manier toepassen.

### V5: Kan ik de proefversie gebruiken voordat ik Aspose.PSD aanschaf?

 A5: Zeker! Grijp de[gratis proefperiode](https://releases.aspose.com/) om de mogelijkheden van Aspose.PSD te verkennen voordat u een aankoop doet.