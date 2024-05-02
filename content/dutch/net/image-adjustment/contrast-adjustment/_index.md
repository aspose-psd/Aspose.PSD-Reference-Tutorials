---
title: Contrastaanpassing implementeren in Aspose.PSD voor .NET
linktitle: Contrastaanpassing implementeren
second_title: Aspose.PSD .NET-API
description: Leer hoe u contrastaanpassing implementeert in Aspose.PSD voor .NET met deze stapsgewijze handleiding.
type: docs
weight: 11
url: /nl/net/image-adjustment/contrast-adjustment/
---
## Invoering

Welkom bij deze uitgebreide handleiding over het implementeren van contrastaanpassing in Aspose.PSD voor .NET! In deze zelfstudie verkennen we het proces van het verbeteren van het contrast van een afbeelding met behulp van Aspose.PSD, een krachtige .NET-beeldbibliotheek. Aan het einde van deze handleiding heeft u een goed begrip van hoe u naadloos contrastaanpassingen op uw afbeeldingen kunt toepassen.

## Vereisten

Voordat we ingaan op het stapsgewijze proces, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

1.  Aspose.PSD voor .NET-bibliotheek: Download en installeer de Aspose.PSD voor .NET-bibliotheek. Je kunt de downloadlink vinden[hier](https://releases.aspose.com/psd/net/).

2. Documentmap: stel een map in waarin uw bron- en doelbestanden worden opgeslagen. Vervang "Uw documentenmap" in de opgegeven code door het pad naar deze map.

Nu we onze vereisten op orde hebben, gaan we verder met de implementatie.

## Naamruimten importeren

In deze stap importeren we de benodigde naamruimten om toegang te krijgen tot de functionaliteiten van de Aspose.PSD-bibliotheek.

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## Stap 1: Laad de afbeelding

 Laad de bronafbeelding in een exemplaar van het`RasterImage` klas.

```csharp
//ExStart:Afbeelding laden
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    RasterImage rasterImage = (RasterImage)image;
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
    // Ga door naar de volgende stap...
}
//ExEnd:Afbeelding laden
```

## Stap 2: Pas het contrast aan

In deze stap passen we het contrast van de geladen afbeelding aan.

```csharp
//ExStart:Contrast aanpassen
rasterImage.AdjustContrast(50); // Pas het contrast aan met 50%
// Ga door naar de volgende stap...
//ExEnd:Contrast aanpassen
```

## Stap 3: Maak TIFF-opties

 Maak een exemplaar van`TiffOptions` Stel voor de resulterende afbeelding verschillende eigenschappen in en sla de afbeelding op in TIFF-indeling.

```csharp
//ExStart:TiffOptions maken
string destName = dataDir + @"AdjustContrast_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
//ExEnd: MaakTiffOptions
```

Gefeliciteerd! U hebt de contrastaanpassing met succes geïmplementeerd met Aspose.PSD voor .NET.

## Conclusie

In deze zelfstudie hebben we het proces van het verbeteren van het beeldcontrast onderzocht met Aspose.PSD voor .NET. De bibliotheek biedt een eenvoudige manier om afbeeldingseigenschappen te manipuleren, waardoor ontwikkelaars moeiteloos visueel aantrekkelijke afbeeldingen kunnen maken.

## Veelgestelde vragen

### Vraag 1: Is Aspose.PSD voor .NET geschikt voor beginners?

A1: Aspose.PSD voor .NET is ontworpen om ontwikkelaarsvriendelijk te zijn, waardoor het geschikt is voor zowel beginners als ervaren ontwikkelaars.

### Vraag 2: Kan ik Aspose.PSD gebruiken voor commerciële projecten?

 A2: Ja, Aspose.PSD voor .NET kan worden gebruikt in commerciële projecten. Ga voor licentiegegevens naar[hier](https://purchase.aspose.com/buy).

### Vraag 3: Is er een gratis proefversie beschikbaar?

 A3: Ja, u kunt een gratis proefversie van Aspose.PSD voor .NET uitproberen[hier](https://releases.aspose.com/).

### V4: Waar kan ik ondersteuning vinden voor Aspose.PSD voor .NET?

 A4: Bezoek het Aspose.PSD voor .NET-ondersteuningsforum[hier](https://forum.aspose.com/c/psd/34) Voor assistentie.

### Vraag 5: Hoe kan ik een tijdelijke licentie verkrijgen?

 A5: Indien nodig kunt u een tijdelijke licentie verkrijgen[hier](https://purchase.aspose.com/temporary-license/).