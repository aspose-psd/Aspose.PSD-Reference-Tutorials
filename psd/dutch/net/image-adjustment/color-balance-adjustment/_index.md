---
title: Kleurbalansaanpassing toepassen in Aspose.PSD voor .NET
linktitle: Kleurbalansaanpassing toepassen
second_title: Aspose.PSD .NET-API
description: Verbeter PSD-beeldkleuren moeiteloos met Aspose.PSD voor de functie Kleurbalansaanpassing van .NET. Volg onze stapsgewijze handleiding voor verbluffende resultaten.
type: docs
weight: 14
url: /nl/net/image-adjustment/color-balance-adjustment/
---
## Invoering

Welkom bij deze uitgebreide handleiding over het toepassen van kleurbalansaanpassing in Aspose.PSD voor .NET! Aspose.PSD is een krachtige .NET-bibliotheek waarmee ontwikkelaars efficiënt met PSD-bestanden kunnen werken. In deze zelfstudie concentreren we ons op de functie Kleurbalansaanpassing, waarmee u de kleurbalans van uw PSD-afbeeldingen eenvoudig kunt verbeteren.

## Vereisten

Voordat we ingaan op de tutorial, zorg ervoor dat je aan de volgende vereisten voldoet:

-  Aspose.PSD voor .NET Library: Download en installeer de bibliotheek van de .NET-bibliotheek[Aspose.PSD-website](https://releases.aspose.com/psd/net/).
- Ontwikkelomgeving: Zorg ervoor dat er een werkende .NET-ontwikkelomgeving op uw computer is geïnstalleerd.
- PSD-bestand: Zorg ervoor dat u een PSD-bestand bij de hand heeft waarop u de kleurbalansaanpassing wilt toepassen.

## Naamruimten importeren

Neem in uw .NET-project de benodigde naamruimten op om de Aspose.PSD-functies te gebruiken. Voeg de volgende regels toe aan uw code:

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

Laten we nu het proces voor het aanpassen van de kleurbalans opsplitsen in meerdere stappen:

## Stap 1: Laad het PSD-bestand

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    // Code voor de kleurbalansaanpassing wordt in de volgende stappen toegevoegd.
}
```

## Stap 2: Kleurbalans openen en aanpassen

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

## Stap 3: Sla de aangepaste afbeelding op

```csharp
im.Save(outputPath);
```

Nu hebt u met succes de kleurbalansaanpassing op uw PSD-bestand toegepast met behulp van Aspose.PSD voor .NET!

## Conclusie

Gefeliciteerd! U hebt geleerd hoe u de kleurbalans van uw PSD-afbeeldingen kunt verbeteren met Aspose.PSD voor .NET. Experimenteer met verschillende balanswaarden om de gewenste visuele effecten te bereiken.

## Veelgestelde vragen

### Vraag 1: Kan ik kleurbalansaanpassing op meerdere lagen toepassen?

A1: Ja, u kunt alle lagen in uw PSD-bestand doorlopen en de kleurbalans indien nodig aanpassen.

### V2: Is Aspose.PSD voor .NET geschikt voor batchverwerking van PSD-bestanden?

A2: Absoluut! Aspose.PSD biedt efficiënte batchverwerkingsmogelijkheden voor PSD-bestanden.

### V3: Hoe kan ik een tijdelijke licentie krijgen voor Aspose.PSD voor .NET?

 A3: Bezoek[Aspose.PSD Tijdelijke licentie](https://purchase.aspose.com/temporary-license/) voor een tijdelijke vergunning.

### Vraag 4: Waar kan ik meer voorbeelden en documentatie vinden?

 A4: Ontdek de[Aspose.PSD-documentatie](https://reference.aspose.com/psd/net/) voor gedetailleerde voorbeelden en handleidingen.

### V5: Welke ondersteuningsopties zijn beschikbaar voor Aspose.PSD voor .NET?

 A5: Bezoek de[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34) voor gemeenschapsondersteuning en discussies.
