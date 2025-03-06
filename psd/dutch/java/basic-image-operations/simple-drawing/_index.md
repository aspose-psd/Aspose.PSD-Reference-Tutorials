---
title: Voer eenvoudig tekenen uit met Aspose.PSD voor Java
linktitle: Voer een eenvoudige tekening uit
second_title: Aspose.PSD Java-API
description: Leer hoe u vormen in PSD-bestanden tekent met Aspose.PSD voor Java. Deze stapsgewijze handleiding behandelt het maken, toevoegen van lagen en tekenen met codevoorbeelden.
weight: 10
url: /nl/java/basic-image-operations/simple-drawing/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Voer eenvoudig tekenen uit met Aspose.PSD voor Java

## Invoering

Welkom bij deze stapsgewijze handleiding voor het uitvoeren van eenvoudige tekeningen met Aspose.PSD voor Java! In deze zelfstudie verkennen we de basisprincipes van het maken van een nieuw PSD-document, het toevoegen van lagen en het tekenen van vormen met verschillende kleuren. Aspose.PSD voor Java is een krachtige bibliotheek waarmee u PSD-bestanden programmatisch kunt manipuleren, waardoor uitgebreide functionaliteit wordt geboden voor grafische ontwerptaken.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

- Java Development Kit (JDK) op uw computer geïnstalleerd.
- Aspose.PSD voor Java-bibliotheek. Je kunt het downloaden van de[Aspose.PSD voor Java-documentatie](https://reference.aspose.com/psd/java/).

## Pakketten importeren

Importeer om te beginnen de benodigde pakketten in uw Java-project. Voeg de volgende code toe aan het begin van uw Java-bestand:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Stap 1: Maak een nieuw document

Laten we beginnen met het maken van een nieuw PSD-document met een opgegeven breedte en hoogte:

```java
//ExStart:Document maken
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:Document maken
```

## Stap 2: Voeg een laag toe

Laten we nu een laag aan het document toevoegen met behulp van de constructor zonder argumenten:

```java
//ExStart:Laag toevoegen
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:Laag toevoegen
```

## Stap 3: Vormen tekenen

In deze stap gebruiken we de klasse Graphics om vormen op de gemaakte laag te tekenen:

### Teken een rechthoek met een gele kleur

```java
//ExStart: tekenrechthoekgeel
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd: TekenRechthoekGeel
```

### Teken een rode rechthoek

```java
//ExStart: TekenRoodRechthoek
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd: teken een rode rechthoek
```

### Teken een blauwe rechthoek

```java
//ExStart: TekenBlauwe Rechthoek
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd: Teken een blauwe rechthoek
```

## Stap 4: Sla de wijzigingen op

Sla ten slotte een kopie op van het geladen PSD-bestand, inclusief de wijzigingen:

```java
//ExStart: Wijzigingen opslaan
image.save(outPsdFilePath);
//ExEnd: Wijzigingen opslaan
```

## Conclusie

Gefeliciteerd! U hebt met succes een eenvoudige tekening uitgevoerd met Aspose.PSD voor Java. Deze tutorial behandelde het maken van een nieuw document, het toevoegen van lagen en het tekenen van rechthoeken met verschillende kleuren. Ontdek gerust de meer geavanceerde functies die de bibliotheek biedt voor uw grafische ontwerpbehoeften.

## Veelgestelde vragen

### V1: Kan ik Aspose.PSD voor Java gebruiken om bestaande PSD-bestanden te manipuleren?

A1: Ja, Aspose.PSD voor Java biedt uitgebreide functionaliteit voor het bewerken en manipuleren van bestaande PSD-bestanden.

### Vraag 2: Waar kan ik ondersteuning vinden voor Aspose.PSD voor Java?

 A2: U kunt de bezoeken[Aspose.PSD voor Java Forum](https://forum.aspose.com/c/psd/34) voor alle ondersteuningsgerelateerde vragen.

### V3: Is er een gratis proefversie beschikbaar voor Aspose.PSD voor Java?

 A3: Ja, u heeft toegang tot de gratis proefversie[hier](https://releases.aspose.com/).

### V4: Hoe kan ik een licentie kopen voor Aspose.PSD voor Java?

 A4: U kunt een licentie kopen bij de[Aspose.PSD-aankooppagina](https://purchase.aspose.com/buy).

### V5: Zijn er tijdelijke licenties beschikbaar voor Aspose.PSD voor Java?

 A5: Ja, u kunt een tijdelijke licentie verkrijgen bij[hier](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
