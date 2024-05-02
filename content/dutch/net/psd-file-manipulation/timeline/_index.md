---
title: Werken met tijdlijn in Aspose.PSD voor .NET
linktitle: Werken met tijdlijn
second_title: Aspose.PSD .NET-API
description: Verbeter PSD-beeldmanipulatie met Aspose.PSD voor .NET Timeline-klasse. Beheer frame-eigenschappen en laagstatussen en ontketen moeiteloos creatieve mogelijkheden.
type: docs
weight: 16
url: /nl/net/psd-file-manipulation/timeline/
---
## Invoering
In de dynamische wereld van grafisch ontwerp en beeldmanipulatie is het vermogen om de tijdlijn van afbeeldingen te controleren en te manipuleren cruciaal. Aspose.PSD voor .NET biedt een krachtige oplossing met zijn Timeline-klasse. Met deze hoogwaardige functie kunnen gebruikers wijzigingen aanbrengen in de tijdlijn van PsdImage, zoals het wijzigen van framevertraging, het bewerken van laagstatussen op specifieke frames en meer.
## Vereisten
Voordat u zich verdiept in de opwindende mogelijkheden die de Timeline-klasse biedt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:
-  Aspose.PSD voor .NET-bibliotheek: Zorg ervoor dat de Aspose.PSD voor .NET-bibliotheek is geïnstalleerd. Je kunt het downloaden van de[Aspose.PSD voor .NET-documentatie](https://reference.aspose.com/psd/net/).
-  Document- en uitvoermappen: definieer de paden voor uw document- en uitvoermappen in de code. Pas de .... aan`baseDir` En`outputDir` variabelen volgens uw projectstructuur.
Laten we nu stap voor stap bekijken hoe u de klasse Tijdlijn kunt gebruiken.
## Naamruimten importeren
Om met de klasse Tijdlijn te gaan werken, importeert u de benodigde naamruimten in uw code:
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.Animation;
```
## Stap 1: PSD-afbeelding laden
Begin met het laden van de PSD-afbeelding uit het opgegeven bronbestand. Zorg ervoor dat het bronbestandspad correct is ingesteld:
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    //Uw code voor verdere bewerkingen vindt u hier
}
```
## Stap 2: Toegang tot de tijdlijn
Zodra de PSD-afbeelding is geladen, opent u de tijdlijn met behulp van de volgende code:
```csharp
Timeline timeline = psdImage.Timeline;
```
## Stap 3: Wijzig de afvoermethode
Manipuleer de afvoermethode van een specifiek frame. In dit voorbeeld wijzigen we de afvoermethode van frame 1:
```csharp
timeline.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;
```
## Stap 4: Pas de framevertraging aan
Wijzig de vertraging van een bepaald frame. Hier veranderen we de vertraging van frame 2 in 15:
```csharp
timeline.Frames[1].Delay = 15;
```
## Stap 5: Bewerk de laagstatus
Wijzig de dekking van 'Laag 1' op een specifiek frame. In dit geval hebben we de dekking op frame 2 ingesteld op 50:
```csharp
LayerState layerState11 = timeline.Frames[1].LayerStates[1];
layerState11.Opacity = 50;
```
## Stap 6: Verplaats laag
Verplaats 'Laag 1' naar de linkerbenedenhoek op een specifiek frame (frame 3 in dit voorbeeld):
```csharp
LayerState layerState21 = timeline.Frames[2].LayerStates[1];
layerState21.PositionOffset = new Point(-50, 230);
```
## Stap 7: Nieuw frame toevoegen
Voeg een nieuw frame toe aan de tijdlijn:
```csharp
List<Frame> frames = new List<Frame>(timeline.Frames);
frames.Add(new Frame());
timeline.Frames = frames.ToArray();
```
## Stap 8: Wijzig de mengmodus
Wijzig de overvloeimodus van 'Laag 1' op een specifiek frame (frame 4 in dit geval):
```csharp
LayerState layerState31 = timeline.Frames[3].LayerStates[1];
layerState31.BlendMode = BlendMode.Dissolve;
```
## Stap 9: Wijzigingen opslaan
Pas de wijzigingen weer toe op de PsdImage-instantie en sla de gewijzigde PSD-afbeelding op:
```csharp
psdImage.Save(outputPsd);
```
## Stap 10: Opruimen
Ruim ten slotte op door het tijdelijke uitvoerbestand te verwijderen:
```csharp
File.Delete(outputPsd);
```
## Conclusie

Concluderend stelt de Timeline-klasse in Aspose.PSD voor .NET ontwikkelaars in staat gedetailleerde controle te hebben over de tijdlijn van PSD-afbeeldingen. Via een reeks eenvoudige stappen kunt u frame-eigenschappen, laagstatussen en meer manipuleren, waardoor een rijk aan creatieve mogelijkheden wordt geopend.

## Veelgestelde vragen

### Vraag 1: Is Aspose.PSD voor .NET geschikt voor beginners?

A1: Absoluut! Aspose.PSD voor .NET biedt een gebruiksvriendelijke interface en uitgebreide documentatie, waardoor het toegankelijk is voor zowel beginners als doorgewinterde ontwikkelaars.

### Vraag 2: Kan ik tijdlijnwijzigingen toepassen op GIF-afbeeldingen?

A2: De klasse Tijdlijn is speciaal ontworpen voor PSD-afbeeldingen. Voor GIF-manipulatie raadpleegt u Aspose.GIF voor .NET.

### Vraag 3: Waar kan ik aanvullende ondersteuning vinden of problemen bespreken?

 A3: Bezoek de[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34) voor gemeenschapsondersteuning en discussies over kwesties.

### V4: Hoe kan ik een tijdelijke licentie verkrijgen voor Aspose.PSD voor .NET?

 A4: Schaf een tijdelijke licentie aan[hier](https://purchase.aspose.com/temporary-license/).

### V5: Wat zijn de belangrijkste voordelen van het gebruik van Aspose.PSD voor .NET?

A5: Aspose.PSD voor .NET biedt geavanceerde beeldverwerkingsmogelijkheden, manipulatie van PSD-bestanden en hoogwaardige weergave.