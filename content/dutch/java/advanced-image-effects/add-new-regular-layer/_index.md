---
title: Voeg een nieuwe reguliere laag toe aan PSD met Aspose.PSD voor Java
linktitle: Voeg een nieuwe reguliere laag toe aan PSD
second_title: Aspose.PSD Java-API
description: Leer hoe u een nieuwe reguliere laag aan PSD-bestanden kunt toevoegen met Aspose.PSD voor Java. Volg onze stapsgewijze handleiding voor naadloze PSD-manipulatie.
type: docs
weight: 11
url: /nl/java/advanced-image-effects/add-new-regular-layer/
---
## Invoering

Welkom bij deze uitgebreide tutorial over het gebruik van Aspose.PSD voor Java om een nieuwe reguliere laag aan een PSD-bestand toe te voegen. Aspose.PSD is een krachtige Java-bibliotheek waarmee ontwikkelaars PSD-bestanden efficiënt kunnen manipuleren en ermee kunnen werken. In deze zelfstudie begeleiden we u bij het toevoegen van een nieuwe reguliere laag aan een PSD-bestand, met gedetailleerde stappen en codevoorbeelden.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

- Java-ontwikkelomgeving: Zorg ervoor dat er een Java-ontwikkelomgeving op uw systeem is geïnstalleerd.
-  Aspose.PSD-bibliotheek: Download en installeer de Aspose.PSD voor Java-bibliotheek. Je kunt de bibliotheek vinden[hier](https://releases.aspose.com/psd/java/).

## Pakketten importeren

Importeer om te beginnen de benodigde pakketten in uw Java-project. Deze pakketten zijn essentieel voor het werken met Aspose.PSD-functionaliteiten. Voeg de volgende regels toe aan het begin van uw Java-bestand:

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Stap 1: PSD-bestand laden

Laad het PSD-bestand dat u wilt bewerken met de volgende code:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Stap 2: Bereid gegevensarrays en rechthoeken voor

Bereid twee int-arrays en twee Rectangle-objecten als volgt voor:

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## Stap 3: Initialiseer laaggegevens

Initialiseer data-arrays met een standaardwaarde:

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## Stap 4: Voeg reguliere lagen toe

Voeg twee reguliere lagen toe aan de PSD-afbeelding:

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

## Stap 5: Bewaar PSD en PNG

Sla de gewijzigde PSD en een extra PNG-bestand op:

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

Gefeliciteerd! U hebt met succes een nieuwe reguliere laag aan een PSD-bestand toegevoegd met behulp van Aspose.PSD voor Java.

## Conclusie

In deze zelfstudie hebben we het proces besproken van het toevoegen van een nieuwe reguliere laag aan een PSD-bestand met behulp van Aspose.PSD voor Java. Deze krachtige bibliotheek vereenvoudigt PSD-manipulatie, waardoor deze toegankelijk wordt voor Java-ontwikkelaars. Experimenteer met verschillende parameters en functionaliteiten om het volledige potentieel van Aspose.PSD te verkennen.

## Veelgestelde vragen

### Vraag 1: Is Aspose.PSD compatibel met Java 8?

A1: Ja, Aspose.PSD ondersteunt Java 8 en latere versies.

### V2: Kan ik transformaties toepassen op de toegevoegde lagen?

A2: Absoluut! Aspose.PSD biedt een reeks transformatieopties voor lagen.

### V3: Waar kan ik aanvullende Aspose.PSD-documentatie vinden?

 A3: U kunt de documentatie raadplegen[hier](https://reference.aspose.com/psd/java/).

### V4: Hoe kan ik een tijdelijke licentie voor Aspose.PSD verkrijgen?

 A4: Bezoek[deze koppeling](https://purchase.aspose.com/temporary-license/) voor tijdelijke licentieopties.

### Vraag 5: Zijn er communityforums voor Aspose.PSD-ondersteuning?

 A5: Ja, u kunt ondersteuning en discussies vinden[hier](https://forum.aspose.com/c/psd/34).