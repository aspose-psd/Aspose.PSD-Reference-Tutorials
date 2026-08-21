---
date: 2026-06-13
description: Leer hoe je een rechthoek tekent in PSD‑bestanden met Aspose.PSD voor
  Java. Deze gids toont step‑by‑step code, het toevoegen van lagen, server‑side image
  processing en shape drawing.
keywords:
- how to draw rectangle
- how to create psd
- java graphics draw rectangle
- server side image processing
- add layer to psd
linktitle: Eenvoudige tekening uitvoeren
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to draw rectangle in PSD files using Aspose.PSD for Java.
    This guide shows step‑by‑step code, adding layers, server‑side image processing
    and shape drawing.
  headline: How to Draw Rectangle in PSD with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Yes, the `Graphics` class also supports drawing ellipses, lines, and custom
      paths via the `drawPath` method.
    question: Can I draw other shapes besides rectangles?
  - answer: Absolutely; you can use `SolidBrush` with an ARGB color to include alpha
      transparency, enabling semi‑transparent overlays.
    question: Does Aspose.PSD support transparency in drawn shapes?
  - answer: Yes, each `Layer` object has a `setOpacity` method that accepts a value
      from 0 to 255, allowing fine‑grained control over layer transparency.
    question: Is it possible to edit the opacity of a layer?
  - answer: Use `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` before
      manipulating layers. The loaded image retains all original layers and masks.
    question: How do I load an existing PSD file instead of creating a new one?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Hoe een rechthoek tekenen in PSD met Aspose.PSD voor Java
url: /nl/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe een rechthoek te tekenen in PSD met Aspose.PSD voor Java

## Introductie

In deze tutorial ontdek je **hoe je een rechthoek tekent** vormen in een Photoshop PSD‑bestand met behulp van de pure‑Java Aspose.PSD‑bibliotheek. Of je nu een server‑side asset‑pipeline bouwt, miniatuur‑generatie automatiseert, of dynamische graphics toevoegt aan bestaande ontwerpen, de onderstaande stappen bieden een complete, productie‑klare oplossing. We behandelen het maken van een nieuw PSD‑document, het toevoegen van een laag, het wissen van de achtergrond, en uiteindelijk het tekenen van zowel rode als blauwe rechthoeken — zonder ooit Photoshop te starten.

## Snelle antwoorden
- **Wat is de primaire klasse om een PSD‑bestand te maken?** `PsdImage`
- **Welke methode wist de achtergrondkleur van een laag?** `Graphics.clear(Color)`
- **Hoe teken je een rode rechthoek?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een licentie is vereist voor productie.
- **Kan ik bestaande PSD‑bestanden manipuleren met dezelfde API?** Ja, Aspose.PSD ondersteunt volledige PSD‑bewerking.

## Wat betekent het tekenen van een rode rechthoek in een PSD‑bestand?

Het tekenen van een rode rechthoek betekent dat je het `Graphics`‑object gebruikt om een rechthoekige vorm, gevuld of omlijnd met de kleur rood, op een specifieke laag van een PSD‑afbeelding te renderen. Deze bewerking is gebruikelijk voor het markeren van gebieden, het maken van tijdelijke aanduidingen, of het programmatisch toevoegen van eenvoudige graphics.

## Waarom Aspose.PSD voor Java gebruiken om PSD‑bestanden te manipuleren?

Aspose.PSD voor Java ondersteunt **meer dan 50 invoer‑ en uitvoerformaten**, kan multi‑honderd‑pagina PSD‑bestanden verwerken zonder het volledige bestand in het geheugen te laden, en draait op elk platform dat Java 8 of hoger ondersteunt. De server‑side beeldverwerkingsengine elimineert de noodzaak voor Photoshop, verlaagt licentiekosten, en maakt geautomatiseerde workflows mogelijk die tot **10 GB** aan beeldgegevens per uur aankunnen op een bescheiden VM.

## Vereisten

- Java Development Kit (JDK) 8 of hoger geïnstalleerd op uw machine.  
- Aspose.PSD voor Java‑bibliotheek. U kunt deze downloaden van de [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/).

## Importer pakketten

De `import`‑verklaringen brengen de benodigde klassen in scope zodat u kunt werken met PSD‑afbeeldingen, lagen, kleuren en graphics.

- De `PsdImage`‑klasse is het top‑level object van Aspose.PSD dat een enkel PSD‑bestand in het geheugen vertegenwoordigt.  
- `Graphics` biedt tekenprimitieven zoals lijnen, rechthoeken en ellipsen.  
- `Color` en `Pen` laten u de lijnkleur en dikte specificeren.  
- De `Layer`‑klasse vertegenwoordigt een individuele afbeeldingslaag binnen een PSD‑document.  
- De `Rectangle`‑klasse definieert de positie en grootte van een rechthoekig gebied dat wordt gebruikt voor tekenbewerkingen.  
- De `SolidBrush`‑klasse vult vormen met een effen kleur.

## Wat is de eerste stap om een PSD‑document te maken?

U maakt een instantie van `PsdImage` door de breedte en hoogte van het canvas in pixels op te geven, waardoor een lege PSD‑bestandstructuur wordt gecreëerd. Nadat u eventuele initiële lagen of de achtergrond hebt ingesteld, roept u de `save`‑methode aan met een bestandspad om het document naar schijf te schrijven. Dit maakt de afbeelding klaar voor daaropvolgende bewerkingsbewerkingen.

## Stap 1: Maak een nieuw document

Maak eerst een nieuw PSD‑document met de gewenste canvasgrootte. Dit document zal de laag bevatten waarop we gaan tekenen.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Hoe voeg je een nieuwe lege laag toe aan een PSD‑afbeelding?

Maak eerst een nieuwe `Layer`‑instantie met dezelfde breedte en hoogte als de bovenliggende `PsdImage`. Voeg vervolgens deze laag toe aan de `Layers`‑collectie van de afbeelding met de `add`‑methode. Zodra de laag deel uitmaakt van de afbeelding, haalt u het `Graphics`‑object op om tekenbewerkingen uit te voeren; zonder deze stap verschijnen de tekeningen niet.

## Stap 2: Voeg een laag toe

Voeg vervolgens een nieuwe lege laag toe die de volledige breedte en hoogte van de afbeelding beslaat. Lagen zijn essentieel om tekenbewerkingen te scheiden.

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Wat is het doel van het wissen van de achtergrondkleur van een laag?

Het aanroepen van `Graphics.clear` met een specifieke `Color` vult de hele laag met die kleur, waardoor alle pixelgegevens effectief worden gereset. Dit zorgt ervoor dat eerdere inhoud wordt verwijderd en dat de laag start vanaf een bekende achtergrond, wat onverwachte transparantie of kleurbewerking voorkomt wanneer de PSD later in Photoshop wordt geopend of bewerkt.

## Stap 3: Teken vormen

We zullen de `Graphics`‑klasse gebruiken om de pixelgegevens van de laag te manipuleren. Hieronder staan drie voorbeelden die het wissen van de achtergrond en het tekenen van rechthoeken met verschillende kleuren illustreren.

### Kleur van laag wissen (achtergrond instellen op geel)

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

### Teken een rode rechthoek (primaire focus)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Teken een blauwe rechthoek (extra voorbeeld)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

## Hoe sla je het bewerkte PSD‑bestand op schijf op?

Gebruik de `save`‑methode op het `PsdImage`‑object, waarbij u het volledige bestandspad opgeeft en eventueel het gewenste afbeeldingsformaat specificeert (standaard PSD). Dit schrijft alle lagen, maskers en tekenopdrachten naar één PSD‑bestand dat voldoet aan de Photoshop‑specificatie, zodat het zonder waarschuwingen kan worden geopend.

## Stap 4: Sla de wijzigingen op

Schrijf tenslotte de gewijzigde PSD‑afbeelding naar schijf. Het bestand zal de nieuwe laag en de getekende vormen bevatten.

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Veelvoorkomende problemen en oplossingen

- **Laag niet zichtbaar na tekenen:** Zorg ervoor dat de laag aan de afbeelding is toegevoegd **voordat** het `Graphics`‑object wordt aangemaakt. Het tekenoppervlak moet aan een geldige laag zijn gekoppeld.
- **Kleuren lijken onjuist:** Controleer of u `Color.getRed()` (of `Color.getBlue()`) gebruikt in plaats van een aangepaste RGB‑waarde die buiten het bereik 0‑255 valt.
- **Bestand niet opgeslagen:** Controleer of het pad `outputDir` bestaat en de applicatie schrijfrechten heeft. Op Linux moet u mogelijk de map‑eigendom aanpassen of `Files.createDirectories` gebruiken.
- **Prestatievermindering bij grote bestanden:** Gebruik `PsdImage`’s `setLoadOptions` om alleen de benodigde kanalen te laden, waardoor het geheugenverbruik voor PSD‑bestanden groter dan 200 MB wordt verminderd.

## Veelgestelde vragen

**Q1: Kan ik Aspose.PSD voor Java gebruiken om bestaande PSD‑bestanden te manipuleren?**  
A1: Ja, Aspose.PSD voor Java biedt uitgebreide functionaliteit om bestaande PSD‑bestanden te bewerken en te manipuleren, inclusief het herschikken van lagen, maskeraanpassingen en vectortekeningen.

**Q2: Waar kan ik ondersteuning vinden voor Aspose.PSD voor Java?**  
A2: U kunt het [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) bezoeken voor door de community gedreven hulp en officiële Aspose‑reacties.

**Q3: Is er een gratis proefversie beschikbaar voor Aspose.PSD voor Java?**  
A3: Ja, u kunt de gratis proefversie [hier](https://releases.aspose.com/) openen. De proefversie bevat alle functies maar voegt een watermerk toe aan opgeslagen bestanden.

**Q4: Hoe kan ik een licentie voor Aspose.PSD voor Java aanschaffen?**  
A4: U kunt een licentie kopen via de [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy). Licentie‑opties omvatten perpetual, abonnement en site‑licenties.

**Q5: Zijn tijdelijke licenties beschikbaar voor Aspose.PSD voor Java?**  
A5: Ja, u kunt een tijdelijke licentie verkrijgen via [hier](https://purchase.aspose.com/temporary-license/).

## Aanvullende veelgestelde vragen

**Q: Kan ik andere vormen tekenen naast rechthoeken?**  
A: Ja, de `Graphics`‑klasse ondersteunt ook het tekenen van ellipsen, lijnen en aangepaste paden via de `drawPath`‑methode.

**Q: Ondersteunt Aspose.PSD transparantie in getekende vormen?**  
A: Absoluut; u kunt `SolidBrush` gebruiken met een ARGB‑kleur om alfatransparantie toe te voegen, waardoor semi‑transparante overlays mogelijk zijn.

**Q: Is het mogelijk de opacity van een laag te bewerken?**  
A: Ja, elk `Layer`‑object heeft een `setOpacity`‑methode die een waarde van 0 tot 255 accepteert, waardoor fijnmazige controle over laagtransparantie mogelijk is.

**Q: Hoe laad ik een bestaand PSD‑bestand in plaats van een nieuw te maken?**  
A: Gebruik `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` voordat u lagen manipuleert. De geladen afbeelding behoudt alle originele lagen en maskers.

## Conclusie

U heeft nu geleerd **hoe je een rechthoek tekent** vormen en lagen binnen een PSD‑bestand te manipuleren met Aspose.PSD voor Java. Door een document te maken, een laag toe te voegen, de achtergrond te wissen en te tekenen met de `Graphics`‑API, kunt u talloze grafisch‑ontwerptaken op de server‑side automatiseren. Experimenteer met verschillende pennen, brushes en laageffecten om deze basis uit te breiden tot volledige beeldgeneratie‑pijplijnen.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

{{< blocks/products/products-backtop-button >}}

## Gerelateerde tutorials

- [Hoe vormen tekenen Java – Basisbeeldbewerkingen](/psd/java/basic-image-operations/)
- [Eenvoudig schalen met Aspose.PSD – Java Image Manipulation Library](/psd/java/basic-image-operations/simple-resizing/)
- [Afbeelding bijsnijden door rechthoek in Aspose.PSD voor Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

---

**Laatst bijgewerkt:** 2026-06-13  
**Getest met:** Aspose.PSD for Java 24.12 (latest op het moment van schrijven)  
**Auteur:** Aspose