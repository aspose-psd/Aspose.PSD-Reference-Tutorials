---
title: Pas het formaat van de afbeelding proportioneel aan met Aspose.PSD voor Java
linktitle: Formaat van afbeelding proportioneel wijzigen
second_title: Aspose.PSD Java-API
description: Verbeter uw Java-applicaties met Aspose.PSD. Volg onze gids om afbeeldingen moeiteloos proportioneel te verkleinen. Verbeter vandaag nog uw mogelijkheden voor beeldverwerking.
weight: 17
url: /nl/java/advanced-image-manipulation/resize-image-proportionally/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Pas het formaat van de afbeelding proportioneel aan met Aspose.PSD voor Java

## Invoering

Welkom bij onze stapsgewijze handleiding voor het proportioneel wijzigen van het formaat van afbeeldingen met Aspose.PSD voor Java. Als u uw Java-toepassingen wilt uitbreiden met efficiënte mogelijkheden voor het wijzigen van de afbeeldingsgrootte, bent u hier aan het juiste adres. In deze zelfstudie leiden we u door het proces aan de hand van duidelijke en beknopte stappen.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

1. Java-omgeving: Zorg ervoor dat Java op uw systeem is geïnstalleerd.
2.  Aspose.PSD-bibliotheek: Download en installeer de Aspose.PSD-bibliotheek. U kunt de benodigde hulpmiddelen vinden[hier](https://releases.aspose.com/psd/java/).

## Pakketten importeren

Zodra u uw vereisten heeft gesorteerd, importeert u de vereiste pakketten in uw Java-project. Zorg ervoor dat er correct naar de Aspose.PSD-bibliotheek wordt verwezen in uw project.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## Stap 1: Laad de afbeelding

Begin met het laden van de afbeelding waarvan u het formaat wilt wijzigen in uw Java-toepassing.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## Stap 2: Geef breedte en hoogte op

Bepaal de nieuwe breedte en hoogte voor uw gewijzigde afbeelding. In dit voorbeeld passen we de afbeelding aan tot de helft van de oorspronkelijke afmetingen.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## Stap 3: Sla de gewijzigde afbeelding op

Sla de gewijzigde afbeelding op de gewenste locatie op en geef de formaatopties op (in dit geval PNG).

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

En daar heb je het! U hebt het formaat van een afbeelding proportioneel aangepast met Aspose.PSD voor Java.

## Conclusie

In deze zelfstudie hebben we de essentiële stappen besproken om het formaat van afbeeldingen proportioneel te wijzigen met behulp van de Aspose.PSD-bibliotheek voor Java. Nu kunt u deze functionaliteit moeiteloos integreren in uw Java-applicaties voor een betere beeldverwerking.

## Veelgestelde vragen

### Vraag 1: Is Aspose.PSD compatibel met alle afbeeldingsformaten?

 A1: Aspose.PSD ondersteunt verschillende afbeeldingsformaten, waaronder PSD, PNG, JPEG en meer. Controleer de[documentatie](https://reference.aspose.com/psd/java/) voor een uitgebreide lijst.

### Vraag 2: Kan ik Aspose.PSD gebruiken voor commerciële projecten?

 A2: Ja, dat kan. Bezoek de[aankooppagina](https://purchase.aspose.com/buy) voor licentiegegevens.

### Vraag 3: Zijn er tijdelijke licenties beschikbaar voor testdoeleinden?

 A3: Ja, u kunt een tijdelijke licentie verkrijgen[hier](https://purchase.aspose.com/temporary-license/) voor evaluatie.

### V4: Waar kan ik ondersteuning vinden voor Aspose.PSD?

 A4: Bezoek de[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34) voor steun en hulp van de gemeenschap.

### Vraag 5: Hoe krijg ik toegang tot de Aspose.PSD-documentatie?

 A5: Raadpleeg de gedetailleerde documentatie[hier](https://reference.aspose.com/psd/java/).
`
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
