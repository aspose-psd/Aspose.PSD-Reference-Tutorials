---
title: Het formaat van afbeeldingen proportioneel wijzigen in Aspose.PSD voor .NET
linktitle: Het formaat van afbeeldingen proportioneel wijzigen
second_title: Aspose.PSD .NET-API
description: Ontdek het naadloos aanpassen van het formaat van afbeeldingen met Aspose.PSD voor .NET. Download de bibliotheek, volg onze tutorial en verbeter uw beeldverwerkingsmogelijkheden.
type: docs
weight: 14
url: /nl/net/image-manipulation/resize-images-proportionally/
---
Op het gebied van beeldmanipulatie onderscheidt Aspose.PSD voor .NET zich als een krachtige toolkit, die ontwikkelaars de mogelijkheid biedt om afbeeldingen gemakkelijk proportioneel te vergroten/verkleinen. In deze stapsgewijze handleiding leiden we u door het proces van het wijzigen van het formaat van afbeeldingen met Aspose.PSD voor .NET, zodat uw afbeeldingen hun verhoudingen feilloos behouden.

## Invoering

Het proportioneel aanpassen van afbeeldingen is een veel voorkomende taak in veel toepassingen, en Aspose.PSD voor .NET vereenvoudigt dit proces voor ontwikkelaars. Of u nu aan een webapplicatie, desktopsoftware of mobiele app werkt, het is van cruciaal belang om te begrijpen hoe u het formaat van afbeeldingen kunt wijzigen met behoud van hun beeldverhouding om de visuele aantrekkingskracht en consistentie te behouden.

## Vereisten

Voordat u in de magie van het vergroten/verkleinen van Aspose.PSD voor .NET duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

1.  Aspose.PSD voor .NET-bibliotheek: Zorg ervoor dat de Aspose.PSD voor .NET-bibliotheek is geïnstalleerd. Je kunt het downloaden van de[Aspose.PSD voor .NET-releases](https://releases.aspose.com/psd/net/) bladzijde.

2. Documentmap: Maak een map om uw documenten op te slaan en vervang "Uw documentmap" in de opgegeven code door het daadwerkelijke pad naar deze map.

Nu u de vereisten hebt ingesteld, gaan we naar de stapsgewijze handleiding.

## Naamruimten importeren

```csharp
using Aspose.PSD.ImageOptions;
```

Importeer de benodigde naamruimten om toegang te krijgen tot de vereiste klassen en methoden.

## Stap 1: Laad de afbeelding

```csharp
// Het pad naar de documentenmap.
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

// Laad een bestaande afbeelding in een exemplaar van de RasterImage-klasse
using (Image image = Image.Load(sourceFile))
{
	if (!image.IsCached)
	{
		image.CacheData();
	}
	// De rest van de stappen gaan hier
}
```

 Laad de bronafbeelding met behulp van de`Image.Load` methode.

## Stap 2: Geef breedte en hoogte op

```csharp
// Breedte en hoogte opgeven
int newWidth = image.Width / 2;
image.ResizeWidthProportionally(newWidth);

int newHeight = image.Height / 2;
image.ResizeHeightProportionally(newHeight);
```

Bepaal de nieuwe breedte en hoogte voor de gewijzigde afbeelding. In dit voorbeeld zijn de breedte en hoogte gehalveerd, maar u kunt deze waarden aanpassen aan uw wensen.

## Stap 3: Sla de gewijzigde afbeelding op

```csharp
string destName = dataDir + @"SimpleResizeImageProportionally_out.png";

image.Save(destName, new PngOptions());
```

 Sla de gewijzigde afbeelding op met behulp van de`Save` methode met gespecificeerde opties. In dit geval slaan we het op als een PNG-bestand.

## Conclusie

Het proportioneel aanpassen van afbeeldingen in Aspose.PSD voor .NET is een eenvoudig proces dat waarde toevoegt aan uw beeldverwerkingsworkflow. Deze handleiding heeft u de kennis gegeven om deze functionaliteit naadloos in uw applicaties te integreren.

## Veelgestelde vragen

### Vraag 1: Kan ik het formaat van afbeeldingen aanpassen aan specifieke afmetingen?

A1: Ja, u kunt de nieuwe breedte en hoogte aanpassen aan uw vereisten in de code.

### Vraag 2: Is Aspose.PSD voor .NET geschikt voor het batchgewijs wijzigen van het formaat van afbeeldingen?

A2: Absoluut! U kunt deze stappen opnemen in een lus voor batchverwerking van meerdere afbeeldingen.

### V3: Zijn er andere functies voor beeldmanipulatie in Aspose.PSD voor .NET?

A3: Ja, Aspose.PSD voor .NET biedt een breed scala aan functies, waaronder bijsnijden, roteren en het toepassen van filters op afbeeldingen.

### V4: Is er een gratis proefversie beschikbaar voor Aspose.PSD voor .NET?

 A4: Ja, u kunt de mogelijkheden van Aspose.PSD voor .NET verkennen met een gratis proefperiode. Bezoek[hier](https://releases.aspose.com/) starten.

### V5: Waar kan ik ondersteuning vinden voor Aspose.PSD voor .NET?

 A5: Bezoek de[Aspose.PSD voor .NET-forum](https://forum.aspose.com/c/psd/34) voor gemeenschapsondersteuning en discussies.