---
title: Roteer een afbeelding in Aspose.PSD voor Java
linktitle: Roteer een afbeelding
second_title: Aspose.PSD Java-API
description: Ontdek moeiteloos beeldrotatie in Java met Aspose.PSD. Roteer, draai en bewaar PSD-bestanden eenvoudig.
type: docs
weight: 19
url: /nl/java/advanced-image-manipulation/rotate-image/
---
## Invoering

Aspose.PSD voor Java biedt een krachtige reeks functies voor het werken met afbeeldingen, waardoor ontwikkelaars PSD-bestanden efficiënt kunnen manipuleren en verwerken. In deze tutorial concentreren we ons op één specifieke taak: een afbeelding roteren. Of u nu een fotobewerkingsprogramma bouwt of eenvoudigweg de richting van een afbeelding wilt aanpassen, Aspose.PSD maakt het proces eenvoudig.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

-  Aspose.PSD voor Java-bibliotheek: Zorg ervoor dat u de Aspose.PSD voor Java-bibliotheek hebt gedownload en geïnstalleerd. U kunt de bibliotheek en gedetailleerde documentatie vinden[hier](https://reference.aspose.com/psd/java/).

- Java-ontwikkelomgeving: Zorg ervoor dat er een Java-ontwikkelomgeving op uw computer is geïnstalleerd.

-  Voorbeeld-PSD-bestand: bereid een voorbeeld-PSD-bestand voor dat u wilt roteren. Pas de .... aan`sourceFile` variabele in de voorbeeldcode met het pad naar uw PSD-bestand.

## Pakketten importeren

Begin met het importeren van de benodigde pakketten om de mogelijkheden van Aspose.PSD te benutten:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Stap 1: Laad de afbeelding

 Laad de bestaande afbeelding in een exemplaar van het`Image` klas:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Stap 2: Roteer de afbeelding

 Roteer de afbeelding met behulp van de`rotateFlip` methode. In dit voorbeeld draaien we de afbeelding 270 graden:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Stap 3: Sla de geroteerde afbeelding op

 Sla de geroteerde afbeelding op met behulp van de`save` methode en specificeert het uitvoerformaat (JPEG, in dit geval):

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## Conclusie

Gefeliciteerd! U hebt met succes een afbeelding geroteerd met Aspose.PSD voor Java. Deze eenvoudige maar krachtige bibliotheek opent een wereld aan mogelijkheden voor beeldmanipulatie in uw Java-applicaties.

## Veelgestelde vragen

### Vraag 1: Is Aspose.PSD compatibel met verschillende afbeeldingsformaten?

A1: Ja, Aspose.PSD ondersteunt verschillende afbeeldingsformaten, waaronder PSD, JPEG, PNG en meer.

### V2: Kan ik aangepaste rotaties toepassen, en niet alleen vooraf gedefinieerde salto's?

A2: Absoluut! Aspose.PSD biedt flexibiliteit voor het toepassen van aangepaste rotaties om aan uw specifieke vereisten te voldoen.

### Vraag 3: Waar kan ik aanvullende ondersteuning of assistentie vinden?

 A3: Ga voor vragen of problemen naar de[Aspose.PSD-forum](https://forum.aspose.com/c/psd/34) voor gemeenschapssteun.

### Vraag 4: Is er een gratis proefversie beschikbaar?

 A4: Ja, u kunt Aspose.PSD verkennen met een[gratis proefperiode](https://releases.aspose.com/).

### Vraag 5: Hoe verkrijg ik een tijdelijke licentie?

 A5: Als u een tijdelijke licentie nodig heeft, kunt u er een verkrijgen[hier](https://purchase.aspose.com/temporary-license/).