---
title: Elliptische vormen maken met Aspose.PSD voor .NET
linktitle: Elliptische vormen maken met Aspose.PSD voor .NET
second_title: Aspose.PSD .NET-API
description: Leer hoe u elliptische vormen tekent in .NET met Aspose.PSD. Stapsgewijze handleiding met codevoorbeelden. Creëer moeiteloos verbluffende graphics.
weight: 13
url: /nl/net/psd-drawing-techniques/creating-elliptical-shapes/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Elliptische vormen maken met Aspose.PSD voor .NET

## Invoering

Welkom bij onze uitgebreide handleiding over het maken van elliptische vormen met Aspose.PSD voor .NET. Aspose.PSD is een krachtige .NET-bibliotheek waarmee ontwikkelaars Photoshop-bestanden kunnen manipuleren en converteren zonder dat Adobe Photoshop nodig is. In deze zelfstudie begeleiden we u bij het tekenen van elliptische vormen met behulp van de bibliotheek.

## Vereisten

Voordat we ingaan op de tutorial, zorg ervoor dat je aan de volgende vereisten voldoet:

- Aspose.PSD voor .NET-bibliotheek: Zorg ervoor dat de Aspose.PSD-bibliotheek in uw .NET-project is geïnstalleerd. Je kunt het downloaden van de[Aspose.PSD voor .NET-documentatie](https://reference.aspose.com/psd/net/).

- .NET-omgeving: bij deze zelfstudie wordt ervan uitgegaan dat u praktische kennis heeft van het .NET-framework.

## Naamruimten importeren

Importeer om te beginnen de benodigde naamruimten in uw project. Dit zorgt ervoor dat u toegang heeft tot de klassen en methoden die nodig zijn voor het tekenen van elliptische vormen. Hier is een voorbeeld:

```csharp
using Aspose.PSD.Brushes;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

Laten we nu het proces van het maken van elliptische vormen in meerdere stappen opsplitsen:

## Stap 1: Stel de documentmap in

```csharp
// Het pad naar de documentenmap.
string dataDir = "Your Document Directory";
```

## Stap 2: Maak een exemplaar van BmpOptions

```csharp
// Maak een exemplaar van BmpOptions en stel de verschillende eigenschappen ervan in
string outpath = dataDir + "Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
```

## Stap 3: Maak een exemplaar van een afbeelding

```csharp
// Maak een exemplaar van Image
using (Image image = new PsdImage(100, 100))
{
    // Maak en initialiseer een exemplaar van de Graphics-klasse en het Clear Graphics-oppervlak
    Graphics graphic = new Graphics(image);
    graphic.Clear(Color.Yellow);
```

## Stap 4: Teken een gestippelde ellipsvorm

```csharp
    // Teken een gestippelde ellipsvorm door het Pen-object op te geven met een rode kleur en een omringende rechthoek
    graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
```

## Stap 5: Teken een doorlopende ellipsvorm

```csharp
    //Teken een doorlopende ellipsvorm door het Pen-object op te geven met een effen penseel met blauwe kleur en een omringende rechthoek
    graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    // Exporteer afbeelding naar bmp-bestandsformaat.
    image.Save(outpath, saveOptions);
}
```

## Conclusie

Gefeliciteerd! U hebt met succes elliptische vormen gemaakt met Aspose.PSD voor .NET. In deze tutorial werden de essentiële stappen behandeld, van het opzetten van de omgeving tot het tekenen van zowel gestippelde als doorlopende ellipsvormen.

## Veelgestelde vragen

### V1: Waar kan ik de documentatie voor Aspose.PSD voor .NET vinden?

 A1: De documentatie is beschikbaar[hier](https://reference.aspose.com/psd/net/).

### V2: Hoe download ik Aspose.PSD voor .NET?

 A2: U kunt het downloaden vanaf de releasepagina[hier](https://releases.aspose.com/psd/net/).

### Vraag 3: Is er een gratis proefversie beschikbaar?

 A3: Ja, u heeft toegang tot de gratis proefperiode[hier](https://releases.aspose.com/).

### V4: Hoe kan ik ondersteuning krijgen voor Aspose.PSD voor .NET?

 A4: Bezoek het ondersteuningsforum[hier](https://forum.aspose.com/c/psd/34).

### Vraag 5: Heb ik een tijdelijke licentie nodig om te testen?

 A5: Ja, u kunt een tijdelijke licentie verkrijgen[hier](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
