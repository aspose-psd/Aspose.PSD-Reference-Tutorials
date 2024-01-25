---
title: Afbeeldingen uitbreiden en bijsnijden in Aspose.PSD voor .NET
linktitle: Afbeeldingen uitbreiden en bijsnijden
second_title: Aspose.PSD .NET-API
description: Leer hoe u afbeeldingen dynamisch kunt uitbreiden en bijsnijden met Aspose.PSD voor .NET. Volg onze stapsgewijze handleiding voor naadloze beeldmanipulatie.
type: docs
weight: 13
url: /nl/net/image-manipulation/expand-crop-images/
---
## Invoering

Aspose.PSD voor .NET is een uitgebreide beeldbibliotheek waarmee ontwikkelaars met verschillende beeldformaten kunnen werken in hun .NET-toepassingen. Een van de opvallende kenmerken is de mogelijkheid om afbeeldingen gemakkelijk te manipuleren. In deze zelfstudie concentreren we ons op het uitbreiden en bijsnijden van afbeeldingen, zodat u een praktische handleiding krijgt om deze taken uit te voeren met Aspose.PSD.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

-  Aspose.PSD voor .NET-bibliotheek: Zorg ervoor dat de Aspose.PSD voor .NET-bibliotheek is geïnstalleerd. Je kunt het downloaden van de[Aspose.PSD voor .NET-documentatie](https://reference.aspose.com/psd/net/).

- Voorbeeldafbeelding: bereid een voorbeeldafbeeldingsbestand voor (bijvoorbeeld "example1.psd") dat u voor de zelfstudie gaat gebruiken.

Laten we nu aan de slag gaan met de stapsgewijze handleiding.

## Naamruimten importeren

Begin met het importeren van de benodigde naamruimten om gebruik te maken van de functionaliteiten van Aspose.PSD voor .NET. Voeg de volgende naamruimten toe aan uw code:

```csharp
using Aspose.PSD.ImageOptions;
```

## Stap 1: Stel het project in

 Zorg ervoor dat u een project hebt opgezet waarin Aspose.PSD voor .NET is geïntegreerd. Zo niet, volg dan de[documentatie](https://reference.aspose.com/psd/net/) voor begeleiding.

## Stap 2: Laad de afbeelding

Laad de voorbeeldafbeelding met behulp van de volgende code:

```csharp
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();
string sourceFile = dataDir + @"example1.psd";

// Laad de afbeelding
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    // Aanvullende code voor beeldverwerking komt hier terecht
}
```

## Stap 3: Afbeeldingsgegevens in cache opslaan

Cache de afbeeldingsgegevens om de prestaties te optimaliseren:

```csharp
rasterImage.CacheData();
```

## Stap 4: Definieer de bestemmingsrechthoek

Maak een exemplaar van de klasse Rectangle en definieer de X, Y, Breedte en Hoogte van de rechthoek. Dit is het gebied waarnaar de afbeelding wordt vergroot of bijgesneden.

```csharp
Rectangle destRect = new Rectangle { X = -200, Y = -200, Width = 300, Height = 300 };
```

## Stap 5: Sla de uitvoerafbeelding op

Sla de uitvoerafbeelding op met de opgegeven opties en doelrechthoek:

```csharp
string destName = dataDir + @"jpeg_out.jpg";
rasterImage.Save(destName, new JpegOptions(), destRect);
```

## Conclusie

Gefeliciteerd! U hebt met succes geleerd hoe u afbeeldingen kunt uitbreiden en bijsnijden met Aspose.PSD voor .NET. Deze krachtige bibliotheek opent een wereld aan mogelijkheden voor beeldmanipulatie binnen uw .NET-applicaties.

## Veelgestelde vragen

### Vraag 1: Kan Aspose.PSD naast PSD ook andere afbeeldingsformaten verwerken?

A1: Ja, Aspose.PSD ondersteunt een breed scala aan afbeeldingsformaten, waaronder JPEG, PNG, GIF en meer.

### Vraag 2: Waar kan ik ondersteuning vinden voor Aspose.PSD?

 A2: U kunt ondersteuning vinden en in contact komen met de gemeenschap op[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34).

### Q3 Is er een gratis proefversie beschikbaar voor Aspose.PSD voor .NET?

 A3: Ja, u kunt de functies verkennen met een gratis proefversie die beschikbaar is op[Gratis proefversie van Aspose.PSD](https://releases.aspose.com/).

### V4: Hoe verkrijg ik een tijdelijke licentie voor Aspose.PSD?

 A4: U kunt een tijdelijke licentie krijgen van[Aspose.PSD Tijdelijke licentie](https://purchase.aspose.com/temporary-license/).

### V5: Waar kan ik Aspose.PSD voor .NET kopen?

 A5: Je kunt de bibliotheek kopen bij de[Aspose.PSD-aankooppagina](https://purchase.aspose.com/buy).