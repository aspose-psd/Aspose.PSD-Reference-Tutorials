---
title: Een afbeelding in een specifieke hoek roteren in Aspose.PSD voor .NET
linktitle: Een afbeelding in een specifieke hoek roteren
second_title: Aspose.PSD .NET-API
description: Ontdek de kracht van Aspose.PSD voor .NET. Roteer afbeeldingen moeiteloos onder specifieke hoeken. Download de bibliotheek en begin met het naadloos manipuleren van afbeeldingen.
weight: 16
url: /nl/net/image-manipulation/rotate-image-specific-angle/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Een afbeelding in een specifieke hoek roteren in Aspose.PSD voor .NET

Als je je verdiept in de wereld van beeldmanipulatie met .NET, biedt Aspose.PSD een krachtige oplossing. In deze zelfstudie begeleiden we u bij het roteren van een afbeelding onder een specifieke hoek met behulp van Aspose.PSD. Voordat we in de stappen duiken, laten we eerst een introductie geven.

## Invoering

Aspose.PSD voor .NET is een veelzijdige bibliotheek waarmee ontwikkelaars naadloos met PSD- en rasterafbeeldingsformaten kunnen werken. Een van de belangrijkste kenmerken is de mogelijkheid om afbeeldingen onder nauwkeurige hoeken te roteren, wat flexibiliteit bij beeldmanipulatie biedt. In deze zelfstudie wordt u door de stappen geleid om een afbeelding onder een specifieke hoek te roteren met behulp van Aspose.PSD voor .NET.

## Vereisten

Voordat we aan deze reis beginnen, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

-  Aspose.PSD voor .NET Library: Download en installeer de bibliotheek van de .NET-bibliotheek[downloadpagina](https://releases.aspose.com/psd/net/).
- Documentmap: stel een map in om uw bron- en uitvoerbestanden op te slaan.

## Naamruimten importeren

Importeer om te beginnen de benodigde naamruimten in uw .NET-project:

```csharp
using Aspose.PSD.ImageOptions;
```

Laten we het voorbeeld nu opsplitsen in meerdere stappen in een stapsgewijze handleiding.

## Stap 1: Stel uw documentmap in

```csharp
string dataDir = "Your Document Directory";
```

 Vervangen`"Your Document Directory"` met het pad naar de map waar u uw bron- en uitvoerbestanden opslaat.

## Stap 2: Laad de afbeelding

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"RotatingImageOnSpecificAngle_out.jpg";

using (RasterImage image = (RasterImage)Image.Load(sourceFile))
{
    // Hier worden aanvullende stappen ingevoegd
}
```

 Laad de afbeelding die u wilt roteren naar een exemplaar ervan`RasterImage`.

## Stap 3: Afbeeldingsgegevens in cache opslaan

```csharp
if (!image.IsCached)
{
    image.CacheData();
}
```

Cache de afbeeldingsgegevens voor betere prestaties tijdens rotatie.

## Stap 4: Roteer de afbeelding

```csharp
image.Rotate(20f, true, Color.Red);
```

Roteer de afbeelding 20 graden, behoud de proportionele grootte en gebruik een rode achtergrond.

## Stap 5: Bewaar het resultaat

```csharp
image.Save(destName, new JpegOptions());
```

Sla de geroteerde afbeelding op met de opgegeven opties (in dit geval als JPEG).

## Conclusie

 Gefeliciteerd! U hebt met succes een afbeelding onder een specifieke hoek geroteerd met Aspose.PSD voor .NET. Deze bibliotheek biedt een robuuste set hulpmiddelen voor beeldmanipulatie, en deze tutorial is slechts het topje van de ijsberg. Ontdek de[documentatie](https://reference.aspose.com/psd/net/) voor meer functies en opties.

## Veelgestelde vragen

### Vraag 1: Kan ik afbeeldingen roteren onder een andere hoek dan 20 graden?

 A1: Ja, u kunt de hoekparameter aanpassen in het`image.Rotate` methode naar elke gewenste waarde.

### V2: Ondersteunt Aspose.PSD andere afbeeldingsformaten dan JPEG?

A2: Absoluut! Aspose.PSD ondersteunt een breed scala aan formaten, waaronder PNG, GIF, BMP en TIFF.

### Vraag 3: Is het cachen van afbeeldingsgegevens nodig vóór rotatie?

A3: Hoewel het niet verplicht is, kan het cachen van gegevens de prestaties aanzienlijk verbeteren, vooral bij grotere afbeeldingen.

### V4: Waar kan ik ondersteuning krijgen voor Aspose.PSD-gerelateerde vragen?

 A4: Bezoek de[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34) voor gemeenschapsondersteuning en discussies.

### Vraag 5: Kan ik Aspose.PSD uitproberen voordat ik een aankoop doe?

 A5: Zeker! Grijp uw[gratis proefperiode](https://releases.aspose.com/)om de mogelijkheden van de bibliotheek te verkennen.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
