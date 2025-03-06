---
title: XMP-metagegevens maken in Aspose.PSD voor .NET
linktitle: XMP-metagegevens maken
second_title: Aspose.PSD .NET-API
description: Ontdek het maken van XMP-metagegevens in Aspose.PSD voor .NET. Verbeter de organisatie van afbeeldingen met naadloze manipulatie.
weight: 10
url: /nl/net/file-and-font-handling/create-xmp-metadata/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# XMP-metagegevens maken in Aspose.PSD voor .NET

## Invoering

In de dynamische wereld van .NET-ontwikkeling is het nauwkeurig manipuleren van afbeeldingen een cruciaal aspect van veel toepassingen. Deze tutorial onderzoekt het maken van XMP-metagegevens in Aspose.PSD voor .NET, een krachtige bibliotheek die beeldverwerkingstaken vereenvoudigt. Met XMP (Extensible Metadata Platform) kunt u metagegevens in afbeeldingsbestanden insluiten, waardoor de efficiënte organisatie en het ophalen van informatie die aan afbeeldingen is gekoppeld, wordt vergemakkelijkt.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

-  Aspose.PSD voor .NET Library: Download en installeer de bibliotheek van de .NET-bibliotheek[Aspose.PSD-documentatie](https://reference.aspose.com/psd/net/).

- Ontwikkelomgeving: Zet een .NET-ontwikkelomgeving op met Visual Studio of uw favoriete IDE.

- Basiskennis van .NET: maak uzelf vertrouwd met de basisconcepten van .NET, aangezien deze tutorial uitgaat van een fundamenteel begrip van .NET-ontwikkeling.

## Naamruimten importeren

Neem in uw .NET-project de benodigde naamruimten op om toegang te krijgen tot de Aspose.PSD-functionaliteit:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.Xmp;
using Aspose.PSD.Xmp.Schemas.DublinCore;
using Aspose.PSD.Xmp.Schemas.Photoshop;
using System;
using System.IO;
```

Laten we nu het proces van het maken van XMP-metagegevens opsplitsen in een reeks uitgebreide stappen.

## Stap 1: Geef de afbeeldingsgrootte en rechthoek op

```csharp
// Het pad naar de documentenmap.
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();

//Geef de grootte van de afbeelding op door een rechthoek te definiëren
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## Stap 2: Maak een nieuwe afbeelding

```csharp
// Maak de gloednieuwe afbeelding voor voorbeelddoeleinden
using (var image = new PsdImage(rect.Width, rect.Height))
{
    // De code voor beeldmanipulatie komt hier...
}
```

## Stap 3: Maak een XMP-header en XMP-trailer

```csharp
// Maak een exemplaar van XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi(Guid.NewGuid().ToString());

// Maak een exemplaar van XMP-TrailerPi, XMPmeta-klasse om verschillende attributen in te stellen
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
XmpMeta xmpMeta = new XmpMeta();
```

## Stap 4: Stel XMP-kenmerken in

```csharp
// Stel XMP-kenmerken in, bijvoorbeeld:
xmpMeta.AddAttribute("Author", "Mr Smith");
xmpMeta.AddAttribute("Description", "The fake metadata value");
```

## Stap 5: Maak een XMP-pakketverpakking

```csharp
// Maak een exemplaar van XmpPacketWrapper dat alle metagegevens bevat
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Stap 6: Maak een Photoshop-pakket en stel attributen in

```csharp
// Maak een exemplaar van het Photoshop-pakket en stel Photoshop-kenmerken in
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.SetCity("London");
photoshopPackage.SetCountry("England");
photoshopPackage.SetColorMode(ColorMode.Rgb);
photoshopPackage.SetCreatedDate(DateTime.UtcNow);
```

## Stap 7: Voeg Photoshop-pakket toe aan XMP-metagegevens

```csharp
// Voeg een Photoshop-pakket toe aan XMP-metagegevens
xmpData.AddPackage(photoshopPackage);
```

## Stap 8: Maak een DublinCore-pakket en stel attributen in

```csharp
// Maak een exemplaar van het DublinCore-pakket en stel dublinCore-kenmerken in
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.SetAuthor("Mudassir Fayyaz");
dublinCorePackage.SetTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.AddValue("dc:movie", "Barfly");
```

## Stap 9: Voeg het DublinCore-pakket toe aan XMP-metagegevens

```csharp
// Voeg dublinCore-pakket toe aan XMP-metagegevens
xmpData.AddPackage(dublinCorePackage);
```

## Stap 10: Update XMP-metagegevens en sla afbeelding op

```csharp
using (var ms = new MemoryStream())
{
    // Update XMP-metagegevens in de afbeelding en sla de afbeelding op de schijf of in een geheugenstroom op
    image.XmpData = xmpData;
    image.Save(ms);
    image.Save(dataDir + "ee.psd");
    ms.Seek(0, System.IO.SeekOrigin.Begin);
}
```

## Stap 11: Afbeelding laden en metadata lezen

```csharp
// Laad de afbeelding vanuit de geheugenstream of vanaf schijf om de metagegevens te lezen/op te halen
using (var img = (PsdImage)Image.Load(ms))
{
    // De XMP-metagegevens ophalen
    XmpPacketWrapper imgXmpData = img.XmpData;
    foreach (XmpPackage package in imgXmpData.Packages)
    {
        // Pakketgegevens gebruiken...
    }
}
```

## Conclusie

Gefeliciteerd! U hebt met succes XMP-metagegevens gemaakt in Aspose.PSD voor .NET. Deze krachtige mogelijkheid verbetert uw beeldverwerkingsmogelijkheden, waardoor u essentiële informatie efficiënt kunt organiseren en ophalen.

## Veelgestelde vragen

### Vraag 1: Is Aspose.PSD voor .NET compatibel met alle afbeeldingsformaten?

A1: Aspose.PSD richt zich primair op het PSD-bestandsformaat (Adobe Photoshop), maar ondersteunt verschillende andere formaten.

### V2: Kan ik bestaande XMP-metagegevens manipuleren met Aspose.PSD voor .NET?

A2: Ja, met Aspose.PSD kunt u bestaande XMP-metagegevens zowel lezen als wijzigen.

### V3: Zijn er beperkingen op de afbeeldingsgrootte bij het gebruik van Aspose.PSD voor .NET?

A3: Aspose.PSD kan afbeeldingen van verschillende groottes verwerken, maar voor extreem grote afbeeldingen zijn mogelijk aanvullende overwegingen vereist.

### V4: Hoe vaak wordt Aspose.PSD voor .NET bijgewerkt?

A4: Er worden regelmatig updates uitgebracht om compatibiliteit met de nieuwste .NET-frameworkversies en industriestandaarden te garanderen.

### Vraag 5: Is er een communityforum voor Aspose.PSD-ondersteuning?

 A: Ja, u kunt ondersteuning en discussies vinden op de[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
