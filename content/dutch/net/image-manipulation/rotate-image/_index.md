---
title: Een afbeelding roteren in Aspose.PSD voor .NET
linktitle: Een afbeelding roteren
second_title: Aspose.PSD .NET-API
description: Leer moeiteloos afbeeldingen roteren in .NET met Aspose.PSD. Volg onze stap-voor-stap handleiding.
type: docs
weight: 15
url: /nl/net/image-manipulation/rotate-image/
---
## Invoering

Als je met .NET in de wereld van beeldmanipulatie duikt, is Aspose.PSD jouw favoriete tool voor naadloze en efficiënte beeldverwerking. In deze zelfstudie concentreren we ons op een fundamentele taak: een afbeelding roteren met Aspose.PSD voor .NET. Volg mee terwijl we het proces opsplitsen in eenvoudige, uitvoerbare stappen.

## Vereisten

Voordat we beginnen, zorg ervoor dat u aan de volgende vereisten voldoet:

-  Aspose.PSD voor .NET Library: Download en installeer de bibliotheek van de .NET-bibliotheek[Aspose.PSD .NET-documentatie](https://reference.aspose.com/psd/net/).

- Uw documentenmap: stel een map in waarin uw afbeeldingen worden opgeslagen. Vervang 'Uw documentenmap' in het codefragment door het pad naar deze map.

## Naamruimten importeren

Zorg ervoor dat u de benodigde naamruimten opneemt om toegang te krijgen tot de Aspose.PSD-functionaliteit. Voeg de volgende regels toe aan het begin van uw .NET-project:

```csharp
using Aspose.PSD.ImageOptions;
```

## Stap 1: Laad de afbeelding

```csharp
string sourceFile = dataDir + @"sample.psd";

// Laad een bestaande afbeelding in een exemplaar van de RasterImage-klasse
using (Image image = Image.Load(sourceFile))
{
```

## Stap 2: Roteer de afbeelding

```csharp
    // Draai de afbeelding 270 graden met de klok mee
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Stap 3: Sla de geroteerde afbeelding op

```csharp
    // Sla de geroteerde afbeelding op als een JPEG-bestand
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

Dat is het! Met slechts een paar regels code hebt u met succes een afbeelding geroteerd met Aspose.PSD voor .NET.

## Conclusie

In deze zelfstudie hebben we de basisprincipes van het roteren van afbeeldingen onderzocht met Aspose.PSD voor .NET. Aspose.PSD biedt een robuuste set tools voor beeldmanipulatie, waardoor het een essentiële bibliotheek is voor .NET-ontwikkelaars. Experimenteer met verschillende rotaties en ontdek verdere mogelijkheden om uw beeldverwerkingsworkflows te verbeteren.

## Veelgestelde vragen

### Vraag 1: Kan ik afbeeldingen met een aangepaste hoek roteren met Aspose.PSD?

 Ja, met Aspose.PSD kunt u een aangepaste hoek voor rotatie opgeven. Vervang eenvoudigweg de`RotateFlipType.Rotate270FlipNone` lijn met de gewenste rotatiehoek.

### Vraag 2: Is Aspose.PSD compatibel met verschillende afbeeldingsformaten?

 Absoluut. Aspose.PSD ondersteunt een breed scala aan afbeeldingsformaten, waaronder PSD, JPEG, PNG en meer. Controleer de[documentatie](https://reference.aspose.com/psd/net/) voor de volledige lijst.

### V3: Hoe kan ik een tijdelijke licentie krijgen voor Aspose.PSD?

 Bezoek de[tijdelijke licentiepagina](https://purchase.aspose.com/temporary-license/) op de Aspose-website om een tijdelijke licentie voor evaluatiedoeleinden te verkrijgen.

### V4: Waar kan ik ondersteuning vinden voor Aspose.PSD?

 Voor vragen of hulp kunt u terecht op de[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34) en verbinding maken met de gemeenschap.

### Vraag 5: Kan ik Aspose.PSD kopen voor commercieel gebruik?

 Zeker. Ontdek de[aankooppagina](https://purchase.aspose.com/buy) om een licentie te verkrijgen die is afgestemd op uw behoeften.