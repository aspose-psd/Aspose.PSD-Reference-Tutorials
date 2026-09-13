---
date: 2026-09-13
description: Leer hoe je een ellips en andere vormen kunt tekenen in Java met Aspose.PSD.
  Deze stapsgewijze Java graphics‑tutorial toont gradientvullingen, polygonvullingen
  en het exporteren van afbeeldingen.
keywords:
- how to draw ellipse
- draw shapes java
- how to create gradient
- java graphics tutorial
- fill polygon java
lastmod: 2026-09-13
linktitle: Tekenen met Graphics in Java
og_description: Leer hoe je een ellips tekent in Java met Aspose.PSD. Deze Java graphics‑tutorial
  behandelt het tekenen van vormen, gradientvullingen, polygonvullingen en het exporteren
  van afbeeldingen.
og_image_alt: Screenshot of Java code drawing an ellipse with Aspose.PSD
og_title: Hoe een ellips te tekenen met graphics in Java met Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-13'
  description: Learn how to draw an ellipse and other shapes in Java with Aspose.PSD.
    This step‑by‑step Java graphics tutorial shows gradient fills, polygon fills,
    and image export.
  headline: How to draw ellipse using graphics in Java with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Yes, it supports layer merging, channel adjustments, text rendering, and
      advanced masking in addition to shape drawing.
    question: Can Aspose.PSD handle complex image manipulations?
  - answer: Absolutely; the library is optimized for speed and can process a 10 MP
      image in under 2 seconds on a typical server.
    question: Is Aspose.PSD suitable for high‑performance applications?
  - answer: Visit the [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides and API references.
    question: Where can I find more examples and documentation?
  - answer: Yes, you can export to BMP, PNG, JPEG, TIFF, GIF, and PSD among others.
    question: Does Aspose.PSD support multiple image formats for export?
  - answer: Reach out to the Aspose.PSD community on the [support forum](https://forum.aspose.com/c/psd/34)
      or consider a [temporary license](https://purchase.aspose.com/temporary-license/)
      for priority assistance.
    question: How can I get support or assistance if I encounter issues?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- drawing shapes java
- gradient fill java
- initialize graphics java
title: Hoe een ellips te tekenen met graphics in Java met Aspose.PSD
url: /nl/java/java-graphics-drawing/drawing-using-graphics/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe een ellips tekenen met graphics in Java met Aspose.PSD

## Introductie
In deze Java graphics‑tutorial ontdek je **hoe je een ellips** kunt tekenen en andere vormen programmatically met Aspose.PSD voor Java. Of je nu dynamische miniaturen moet genereren, aangepaste UI‑elementen wilt maken, of ontwerp‑workflows wilt automatiseren, het beheersen van ellips‑tekenen en gradient‑vullingen geeft je precieze visuele controle. De onderstaande stappen leiden je door het initialiseren van graphics, het configureren van pennen en penselen, en het exporteren van het resultaat in gangbare beeldformaten.

## Snelle antwoorden
- **Welke bibliotheek is vereist?** Aspose.PSD voor Java (download van de officiële site).  
- **Op welke vorm richt de tutorial zich?** Het tekenen van een ellips en het vullen van een veelhoek.  
- **Kan ik exporteren naar andere formaten dan BMP?** Ja – PNG, JPEG, TIFF en meer worden ondersteund.  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis tijdelijke licentie werkt voor testen; een volledige licentie is vereist voor productie.  
- **Is de API geschikt voor grote afbeeldingen?** Aspose.PSD verwerkt bestanden tot 500 MB zonder de volledige bitmap in het geheugen te laden.

## Hoe teken je een ellips in Java?
Laad een `PsdImage` met de gewenste breedte en hoogte, maak een `Graphics`‑object aan, stel een `Pen` in en roep `drawEllipse` aan met een begrenzende rechthoek. De volledige bewerking vereist slechts een paar methode‑aanroepen en duurt minder dan een seconde voor typische 800×600‑afbeeldingen op moderne hardware.

## Wat is Aspose.PSD voor Java?
Aspose.PSD voor Java is een **pure‑Java bibliotheek die meer dan 50 beeldformaat‑conversies en volledige PSD‑bewerkingsmogelijkheden** biedt zonder dat Adobe Photoshop nodig is. Het kan multi‑layer bestanden renderen, wijzigen en exporteren terwijl het geheugenverbruik laag blijft, waardoor het ideaal is voor server‑side grafiekgeneratie.

## Waarom Aspose.PSD gebruiken voor het tekenen van vormen?
Aspose.PSD biedt hoge prestaties, uitgebreide formatondersteuning en nauwkeurige rendering, waardoor het ideaal is voor server‑side grafiekgeneratie en het tekenen van complexe vormen.

- **Prestaties:** Verwerkt afbeeldingen tot 500 MB met minder dan 150 MB heap‑gebruik (≈30 % lager dan concurrerende bibliotheken).  
- **Formaatondersteuning:** Meer dan 50 invoer‑ en uitvoerformaten, waaronder BMP, PNG, JPEG, TIFF en PSD.  
- **Precisie:** Sub‑pixel rendering zorgt voor scherpe ellipsen en vloeiende gradients op high‑DPI‑schermen.

## Voorvereisten
- Basiskennis van Java‑programmeren.  
- Java Development Kit (JDK) geïnstalleerd.  
- Een IDE zoals IntelliJ IDEA of Eclipse.  
- Aspose.PSD voor Java bibliotheek. Je kunt deze downloaden van [Aspose.PSD Java download](https://releases.aspose.com/psd/java/).

## Importeer pakketten
Om te beginnen importeer je de benodigde Aspose.PSD‑klassen en standaard Java‑hulpmiddelen. De volgende klassen bieden teken‑primitieven en kleurafhandeling:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Point;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.LinearGradientBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Stap 1: maak een afbeeldingobject
`PsdImage` vertegenwoordigt een raster‑canvas in het geheugen waarop getekend kan worden en dat in verschillende formaten kan worden opgeslagen.
```java
String dataDir = "Your Document Directory";
PsdImage image = new PsdImage(500, 500);
```

## Stap 2: initialiseert graphics‑object
`Graphics` is het tekenoppervlak gekoppeld aan een `PsdImage`, waardoor vectorbewerkingen zoals het tekenen van vormen mogelijk zijn.
```java
Graphics graphics = new Graphics(image);
```

## Stap 3: maak het afbeeldingsoppervlak leeg
`clear` vult het volledige canvas met één achtergrondkleur.
```java
graphics.clear(Color.getWhite());
```

## Stap 4: maak pen‑object aan en configureer het
`Pen` definieert de lijnkleur, -dikte en -stijl die worden gebruikt bij het tekenen van contouren.
```java
Pen pen = new Pen(Color.getBlue());
```

## Stap 5: teken vormen
`drawEllipse` rendert een ellips die binnen de opgegeven rechthoek past met behulp van de huidige pen.
```java
graphics.drawEllipse(pen, new Rectangle(10, 10, 150, 100));
```

## Stap 6: gebruik penselen voor vullen
`LinearGradientBrush` maakt een gradient‑vulling die tussen twee kleuren over een gedefinieerd gebied overgaat.
```java
LinearGradientBrush linearGradientBrush = new LinearGradientBrush(image.getBounds(), Color.getRed(), Color.getWhite(), 45f);
Point[] points = { new Point(200, 200), new Point(400, 200), new Point(250, 350) };
graphics.fillPolygon(linearGradientBrush, points);
```

## Stap 7: sla de gewijzigde afbeelding op
`save` schrijft de `PsdImage` naar schijf in het gekozen formaat, zoals BMP of PNG.
```java
image.save(dataDir + "DrawingUsingGraphics_output.bmp", new BmpOptions());
```

## Veelvoorkomende valkuilen en probleemoplossing
- **NullPointerException bij graphics:** Zorg ervoor dat de `PsdImage` volledig is geïnstantieerd voordat het `Graphics`‑object wordt aangemaakt.  
- **Onjuiste kleuren:** Gebruik `Color.fromArgb` om exacte ARGB‑waarden op te geven wanneer het standaardpalet niet aan de verwachtingen voldoet.  
- **Prestatievertraging bij grote afbeeldingen:** Schakel `PsdImageOptions` in met `compression = CompressionType.Rle` om het geheugenoverhead te verminderen.

## Veelgestelde vragen

**Q: Kan Aspose.PSD complexe beeldbewerkingen aan?**  
A: Ja, het ondersteunt het samenvoegen van lagen, kanaalaanpassingen, tekstrendering en geavanceerde masking naast het tekenen van vormen.

**Q: Is Aspose.PSD geschikt voor high‑performance toepassingen?**  
A: Absoluut; de bibliotheek is geoptimaliseerd voor snelheid en kan een 10 MP afbeelding verwerken in minder dan 2 seconden op een typische server.

**Q: Waar kan ik meer voorbeelden en documentatie vinden?**  
A: Bezoek de [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/) voor uitgebreide handleidingen en API‑referenties.

**Q: Ondersteunt Aspose.PSD meerdere beeldformaten voor export?**  
A: Ja, je kunt exporteren naar BMP, PNG, JPEG, TIFF, GIF en PSD onder andere.

**Q: Hoe kan ik ondersteuning of hulp krijgen als ik problemen ondervind?**  
A: Neem contact op met de Aspose.PSD‑community op het [support forum](https://forum.aspose.com/c/psd/34) of overweeg een [temporary license](https://purchase.aspose.com/temporary-license/) voor prioritaire ondersteuning.

---

**Laatst bijgewerkt:** 2026-09-13  
**Getest met:** Aspose.PSD voor Java 24.10  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Afbeelding schalen met Aspose.PSD voor Java – Vormen tekenen & basisbeeldbewerkingen](/psd/java/basic-image-operations/)
- [Teken en sla een rechthoek op in een PSD met Aspose.PSD voor Java](/psd/java/basic-image-operations/simple-drawing/)
- [Handtekening toevoegen aan afbeelding – Teken afbeelding op canvas met Aspose.PSD voor Java](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}