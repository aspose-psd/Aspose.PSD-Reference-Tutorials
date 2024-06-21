---
title: Het formaat wijzigen met Resize Type Enumeration in Aspose.PSD voor Java
linktitle: Formaat wijzigen met Resize Type Enumeration
second_title: Aspose.PSD Java-API
description: Het formaat van de hoofdafbeelding wijzigen in Java met Aspose.PSD. Stapsgewijze handleiding met behulp van Resize Type Enumeration.
type: docs
weight: 18
url: /nl/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
---
## Invoering

In het voortdurend evoluerende landschap van Java-ontwikkeling is efficiënte beeldverwerking een cruciaal aspect waar ontwikkelaars vaak mee worstelen. Aspose.PSD voor Java komt naar voren als een krachtige oplossing, die een naadloze ervaring biedt voor het wijzigen van het formaat van afbeeldingen met het extra voordeel van de Resize Type Enumeration. In deze zelfstudie verdiepen we ons in de fijne kneepjes van het wijzigen van het formaat van afbeeldingen met Aspose.PSD voor Java, waarbij we elke stap opsplitsen om een uitgebreid begrip te garanderen.

## Vereisten

Voordat u aan deze zelfstudie begint, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

1. Java-ontwikkelomgeving: Zorg ervoor dat er een Java-ontwikkelomgeving op uw computer is geïnstalleerd.

2. Aspose.PSD-bibliotheek: Download en installeer de Aspose.PSD-bibliotheek van de[website](https://releases.aspose.com/psd/java/).

3.  Voorbeeld-PSD-bestand: Zorg dat u een voorbeeld-PSD-bestand gereed heeft om mee te experimenteren. U kunt gebruik maken van de[sample.psd](Uw documentenmap/sample.psd) voor deze zelfstudie.

## Pakketten importeren

Importeer om te beginnen de benodigde pakketten in uw Java-project:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Stap 1: Laad de afbeelding

 Begin met het laden van een bestaande afbeelding in een exemplaar van het`RasterImage` klas. Gebruik het volgende codefragment:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Laad een bestaande afbeelding in een exemplaar van de RasterImage-klasse
Image image = Image.load(sourceFile);
```

## Stap 2: Pas het formaat van de afbeelding aan

Wijzig nu het formaat van de geladen afbeelding met behulp van de Resize Type Enumeration. In dit voorbeeld gebruiken we de Lanczos Resample-methode:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Stap 3: Sla de gewijzigde afbeelding op

Nadat u het formaat heeft gewijzigd, slaat u de afbeelding op met de opgegeven afmetingen en het gekozen formaattype. Hier slaan we het op als een JPEG-bestand:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

En daar heb je het! U hebt het formaat van een afbeelding met succes aangepast met behulp van de Resize Type Enumeration in Aspose.PSD voor Java.

Kortom, Aspose.PSD voor Java biedt een robuust platform voor beeldmanipulatie, en de Resize Type Enumeration voegt een laag flexibiliteit toe aan dit proces. Of u nu aan een klein project of aan een grootschalige toepassing werkt, als u deze stappen beheerst, kunt u het formaat van afbeeldingen naadloos aanpassen.

## Veelgestelde vragen

### Vraag 1: Is Aspose.PSD voor Java geschikt voor zowel kleine als grootschalige projecten?

A1: Absoluut! Aspose.PSD voor Java is ontworpen voor projecten van elke omvang en biedt schaalbaarheid en efficiëntie.

### Vraag 2: Kan ik een ander formaattype gebruiken dan Lanczos Resample?

A2: Ja, Aspose.PSD voor Java biedt verschillende typen formaatwijzigingen, zoals Nearest Neighbor, Bicubic en meer. Bekijk de documentatie voor een uitgebreide lijst.

### V3: Waar kan ik aanvullende ondersteuning vinden voor Aspose.PSD voor Java?

 A3: Ga voor vragen of hulp naar de[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34).

### V4: Is er een gratis proefversie beschikbaar voor Aspose.PSD voor Java?

 A4: Ja, u heeft toegang tot een gratis proefversie.[hier](https://releases.aspose.com/).

### V5: Hoe kan ik een tijdelijke licentie verkrijgen voor Aspose.PSD voor Java?

 A5: Ga naar om een tijdelijke licentie te verkrijgen[deze link](https://purchase.aspose.com/temporary-license/).