---
date: 2025-12-27
description: Leer hoe u rode rechthoeken en andere vormen kunt tekenen in PSD‑bestanden
  met Aspose.PSD voor Java. Deze stapsgewijze handleiding behandelt het maken van
  documenten, het toevoegen van lagen en tekenen met codevoorbeelden.
linktitle: Perform Simple Drawing
second_title: Aspose.PSD Java API
title: Teken rode rechthoek met Aspose.PSD voor Java
url: /nl/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rode rechthoek tekenen met Aspose.PSD for Java

## Introductie

Welkom bij deze stapsgewijze gids over hoe je **rode rechthoek** kunt tekenen met Aspose.PSD for Java! In deze tutorial lopen we door het maken van een nieuw PSD‑document, het toevoegen van een laag en het tekenen van vormen met aangepaste kleuren. Of je nu grafische assets automatiseert of een backend voor een ontwerptool bouwt, deze tutorial biedt je de essentiële bouwstenen.

## Snelle Antwoorden
- **Wat is de primaire klasse om een PSD‑bestand te maken?** `PsdImage`
- **Welke methode wist de achtergrondkleur van een laag?** `Graphics.clear(Color)`
- **Hoe teken je een rode rechthoek?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een licentie is vereist voor productie.
- **Kan ik bestaande PSD‑bestanden manipuleren met dezelfde API?** Ja, Aspose.PSD ondersteunt volledige PSD‑bewerking.

## Wat is het tekenen van een rode rechthoek in een PSD‑bestand?

Het tekenen van een rode rechthoek betekent dat je het `Graphics`‑object gebruikt om een rechthoekige vorm, gevuld of omlijnd met de kleur rood, op een specifieke laag van een PSD‑afbeelding te renderen. Deze bewerking wordt vaak gebruikt om gebieden te markeren, tijdelijke aanduidingen te maken of eenvoudige grafische elementen programmatisch toe te voegen.

## Waarom Aspose.PSD for Java gebruiken om PSD‑bestanden te manipuleren?

Aspose.PSD biedt een pure‑Java API waarmee je Photoshop PSD‑bestanden kunt lezen, bewerken en schrijven zonder dat Photoshop geïnstalleerd hoeft te zijn. Het ondersteunt laagbeheer, kleurbewerking en vectortekenen, waardoor het ideaal is voor server‑side beeldverwerking, geautomatiseerde asset‑pijplijnen en aangepaste grafiekgeneratie.

## Vereisten

- Java Development Kit (JDK) geïnstalleerd op je machine.  
- Aspose.PSD for Java bibliotheek. Je kunt deze downloaden van de [Aspose.PSD for Java Documentatie](https://reference.aspose.com/psd/java/).

## Pakketten importeren

Om te beginnen importeer je de benodigde klassen in je Java‑project:

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

Eerst maak je een fris PSD‑document met de gewenste canvasgrootte. Dit document host de laag waarop we gaan tekenen.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Stap 2: Voeg een laag toe

Vervolgens voeg je een nieuwe lege laag toe die de volledige breedte en hoogte van de afbeelding beslaat. Lagen zijn essentieel voor het scheiden van tekenbewerkingen.

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## Stap 3: Teken vormen

We gebruiken de `Graphics`‑klasse om de pixelgegevens van de laag te manipuleren. Hieronder staan drie voorbeelden die laten zien hoe je de achtergrond wist en rechthoeken tekent met verschillende kleuren.

### Laagkleur wissen (achtergrond instellen op geel)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Teken een rode rechthoek (primaire focus)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### Teken een blauwe rechthoek (extra voorbeeld)

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Stap 4: Sla de wijzigingen op

Tot slot schrijf je de gewijzigde PSD‑afbeelding naar schijf. Het bestand bevat de nieuwe laag en de getekende vormen.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## Veelvoorkomende problemen en oplossingen

- **Laag niet zichtbaar na tekenen:** Zorg ervoor dat de laag aan de afbeelding is toegevoegd **voordat** het `Graphics`‑object wordt aangemaakt.
- **Kleuren verschijnen onjuist:** Controleer of je `Color.getRed()` (of andere statische methoden) gebruikt in plaats van aangepaste RGB‑waarden die buiten het bereik kunnen liggen.
- **Bestand niet opgeslagen:** Bevestig dat het pad `outputDir` bestaat en dat de applicatie schrijfrechten heeft.

## Veelgestelde vragen

### V1: Kan ik Aspose.PSD for Java gebruiken om bestaande PSD‑bestanden te manipuleren?

A1: Ja, Aspose.PSD for Java biedt uitgebreide functionaliteit om bestaande PSD‑bestanden te bewerken en te manipuleren.

### V2: Waar kan ik ondersteuning vinden voor Aspose.PSD for Java?

A2: Je kunt het [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) bezoeken voor vragen met betrekking tot ondersteuning.

### V3: Is er een gratis proefversie beschikbaar voor Aspose.PSD for Java?

A3: Ja, je kunt de gratis proefversie bereiken [hier](https://releases.aspose.com/).

### V4: Hoe kan ik een licentie kopen voor Aspose.PSD for Java?

A4: Je kunt een licentie kopen via de [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy).

### V5: Zijn tijdelijke licenties beschikbaar voor Aspose.PSD for Java?

A5: Ja, je kunt een tijdelijke licentie verkrijgen [hier](https://purchase.aspose.com/temporary-license/).

## Aanvullende veelgestelde vragen

**Q: Kan ik andere vormen tekenen naast rechthoeken?**  
A: Ja, de `Graphics`‑klasse ondersteunt ook het tekenen van ellipsen, lijnen en aangepaste paden.

**Q: Ondersteunt Aspose.PSD transparantie in getekende vormen?**  
A: Absoluut; je kunt `SolidBrush` gebruiken met een ARGB‑kleur om alfatransparantie op te nemen.

**Q: Is het mogelijk de opacity van een laag te bewerken?**  
A: Ja, elk `Layer`‑object heeft een `setOpacity`‑methode die een waarde van 0 tot 255 accepteert.

**Q: Hoe laad ik een bestaand PSD‑bestand in plaats van een nieuw te maken?**  
A: Gebruik `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` voordat je lagen manipuleert.

## Conclusie

Je hebt nu geleerd hoe je **rode rechthoek** en andere basisvormen kunt tekenen in een PSD‑bestand met Aspose.PSD for Java. Door een document te maken, een laag toe te voegen, de achtergrond te wissen en te tekenen met de `Graphics`‑API, kun je veel grafisch‑ontwerptaken automatiseren. Verken verder door te experimenteren met verschillende penselen, laageffecten en bestandsformaten.

---

**Last Updated:** 2025-12-27  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}