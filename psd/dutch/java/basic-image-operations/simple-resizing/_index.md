---
date: 2026-06-13
description: Leer hoe u een afbeelding in Java kunt verkleinen met een java image
  manipulation library. Volg onze stapsgewijze gids met Aspose.PSD for Java voor efficiënte
  beeldbewerking.
keywords:
- java image manipulation library
- how to resize image java
- change image dimensions java
linktitle: Voer eenvoudige schaling uit
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to resize image Java using a java image manipulation library.
    Follow our step‑by‑step guide with Aspose.PSD for Java for efficient image manipulation.
  headline: Simple Resizing with Aspose.PSD – Java Image Manipulation Library
  type: TechArticle
- description: Learn how to resize image Java using a java image manipulation library.
    Follow our step‑by‑step guide with Aspose.PSD for Java for efficient image manipulation.
  name: Simple Resizing with Aspose.PSD – Java Image Manipulation Library
  steps:
  - name: Set Your Document Directory
    text: Define the folder that contains the source PSD file. Replace the placeholder
      with your actual path.
  - name: Specify Source and Destination Paths
    text: Create full file names for the input PSD and the output JPEG.
  - name: Load the Image
    text: '`Image.load(path)` reads an image file from the given path and returns
      an `Image` instance. Load the PSD into an `Image` object.'
  - name: Resize the Image
    text: '`image.resize(width, height)` changes the image dimensions to the specified
      pixel size. Resize to the desired dimensions (e.g., 300 × 300 pixels).'
  - name: Save the Resized Image
    text: '`image.save(path, options)` writes the image to the specified file using
      the given format options. Export the resized bitmap as a JPEG file. > **Pro
      tip:** Experiment with different width/height values or maintain the aspect
      ratio by calculating one dimension from the other.'
  type: HowTo
- questions:
  - answer: Absolutely. The `resize(width, height)` method lets you define any pixel
      size you need.
    question: Can I resize images to specific dimensions using Aspose.PSD for Java?
  - answer: Yes. Besides PSD, the library supports JPEG, PNG, BMP, TIFF, and many
      more.
    question: Is Aspose.PSD for Java compatible with different image formats?
  - answer: Refer to the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)
      for a full API reference.
    question: Where can I find additional documentation for Aspose.PSD for Java?
  - answer: Certainly! Download the [free trial version](https://releases.aspose.com/)
      to explore all features.
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) to ask
      questions and share experiences with the community.
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Eenvoudig schalen met Aspose.PSD – Java Image Manipulation Library
url: /nl/java/basic-image-operations/simple-resizing/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eenvoudig schalen met Aspose.PSD – Java-afbeeldingsbewerkingsbibliotheek

## Inleiding

Als u een Java‑ontwikkelaar bent die op zoek is naar een betrouwbare **java image manipulation library**, bent u hier aan het juiste adres. In deze tutorial lopen we **hoe je image java kunt schalen** projecten door Aspose.PSD voor Java te gebruiken – een krachtige bibliotheek die beeldverwerking snel en eenvoudig maakt. Aan het einde van deze gids heeft u een duidelijk, productie‑klaar voorbeeld dat u in elke Java‑applicatie kunt opnemen.

## Snelle antwoorden
- **Welke bibliotheek wordt gebruikt?** Aspose.PSD voor Java, een toonaangevende java image manipulation library.  
- **Kan ik elke PSD schalen?** Ja – de bibliotheek ondersteunt PSD, JPEG, PNG en meer.  
- **Hoe grootte opgeven?** Roep `image.resize(width, height)` aan met de gewenste pixelafmetingen.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor ontwikkeling; een licentie is vereist voor productie.  
- **Welke Java‑versie is vereist?** Java 8 of hoger.

## Wat is een Java‑afbeeldingsbewerkingsbibliotheek?

Een **java image manipulation library** is een verzameling Java‑API's die u programmatisch rasterafbeeldingen laten bewerken — schalen, bijsnijden, formaatconversie en laagbeheer — zonder externe tools. Aspose.PSD biedt deze mogelijkheden voor PSD en vele andere formaten, met een nette object‑georiënteerde API voor ontwikkelaars.

## Waarom Aspose.PSD gebruiken voor eenvoudig schalen?

Aspose.PSD levert **prestaties‑geoptimaliseerde** algoritmen die bestanden met meer dan 500 lagen in minder dan een seconde op een typische server kunnen verwerken, en het werkt volledig in Java — geen native DLL's of externe binaries. De bibliotheek ondersteunt **30+ afbeeldingsformaten** (inclusief PSD, JPEG, PNG, TIFF, BMP, GIF) en kan bestanden groter dan 200 MB verwerken zonder het volledige document in het geheugen te laden, waardoor het ideaal is voor high‑throughput server‑side pipelines.

## Voorvereisten

Voordat we beginnen, zorg dat u het volgende heeft:

1. **Java Development Kit (JDK)** – download de nieuwste versie van de [Java website](https://www.oracle.com/java/).  
2. **Aspose.PSD voor Java** – verkrijg de bibliotheek van de [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  

Met deze zaken bent u klaar voor een soepele installatie van het schaalvoorbeeld.

## Importer pakketten

De `Image`‑klasse en gerelateerde exportopties zijn vereist voor het laden en opslaan van bestanden.

`Image` is de primaire klasse die een afbeelding vertegenwoordigt die kan worden geladen, bewerkt en opgeslagen.

`JpegOptions` specificeert instellingen voor het opslaan van een afbeelding in JPEG‑formaat.

Deze imports geven u toegang tot de kern‑`Image`‑klasse en JPEG‑exportopties.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.JpegOptions;
```

## Stapsgewijze handleiding

### Stap 1: Stel uw documentmap in

Definieer de map die het bron‑PSD‑bestand bevat. Vervang de tijdelijke aanduiding door uw eigen pad.

```java
String dataDir = "Your Document Directory";
```

### Stap 2: Specificeer bron‑ en bestemmingspaden

Maak volledige bestandsnamen voor de invoer‑PSD en de uitvoer‑JPEG.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "SimpleResizing_out.jpg";
```

### Stap 3: Laad de afbeelding

`Image.load(path)` leest een afbeeldingsbestand van het opgegeven pad en retourneert een `Image`‑instantie.

Laad de PSD in een `Image`‑object.

```java
Image image = Image.load(sourceFile);
```

### Stap 4: Schaal de afbeelding

`image.resize(width, height)` wijzigt de afbeeldingsafmetingen naar de opgegeven pixelgrootte.

Schaal naar de gewenste afmetingen (bijv. 300 × 300 pixels).

```java
image.resize(300, 300);
```

### Stap 5: Sla de geschaalde afbeelding op

`image.save(path, options)` schrijft de afbeelding naar het opgegeven bestand met de gegeven formaatopties.

Exporteer de geschaalde bitmap als een JPEG‑bestand.

```java
image.save(destName, new JpegOptions());
```

> **Pro tip:** Experimenteer met verschillende breedte/hoogte‑waarden of behoud de beeldverhouding door één dimensie te berekenen op basis van de andere.

## Hoe afbeeldingafmetingen wijzigen in Java?

Gebruik de `resize(width, height)`‑methode op de `Image`‑instantie, waarbij u de exacte pixelwaarden opgeeft die u nodig heeft. Bijvoorbeeld, `image.resize(800, 600)` levert een uitvoer van 800 × 600 pixels terwijl kleurdiepte en metadata behouden blijven. Als u de oorspronkelijke beeldverhouding wilt behouden, berekent u de tweede dimensie op basis van de oorspronkelijke breedte‑tot‑hoogte‑verhouding voordat u `resize` aanroept.

## Veelvoorkomende problemen & oplossingen

| Probleem | Reden | Oplossing |
|----------|-------|-----------|
| **`OutOfMemoryError`** | Zeer grote PSD‑bestanden kunnen de JVM‑heap overschrijden. | Verhoog de JVM‑heap‑grootte (`-Xmx2g`) of verwerk afbeeldingen in delen. |
| **Unsupported format** | Poging om een niet‑PSD‑bestand te laden zonder de juiste opties. | Gebruik de juiste `Image.load`‑overload of converteer het bestand eerst. |
| **Distorted output** | Onjuiste beeldverhouding. | Bereken de hoogte op basis van de oorspronkelijke beeldverhouding of gebruik `image.resizeProportionally`. |

## Veelgestelde vragen

**Q: Kan ik afbeeldingen schalen naar specifieke afmetingen met Aspose.PSD voor Java?**  
A: Absoluut. De `resize(width, height)`‑methode laat u elke gewenste pixelgrootte definiëren.

**Q: Is Aspose.PSD voor Java compatibel met verschillende afbeeldingsformaten?**  
A: Ja. Naast PSD ondersteunt de bibliotheek JPEG, PNG, BMP, TIFF en nog veel meer.

**Q: Waar kan ik extra documentatie vinden voor Aspose.PSD voor Java?**  
A: Raadpleeg de [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) voor een volledige API‑referentie.

**Q: Kan ik Aspose.PSD voor Java uitproberen voordat ik koop?**  
A: Zeker! Download de [free trial version](https://releases.aspose.com/) om alle functies te verkennen.

**Q: Hoe kan ik ondersteuning krijgen voor Aspose.PSD voor Java?**  
A: Bezoek het [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) om vragen te stellen en ervaringen te delen met de community.

## Conclusie

In deze tutorial hebben we laten zien hoe een **java image manipulation library** zoals Aspose.PSD **hoe je image java kunt schalen** taken moeiteloos maakt. Door de beknopte stappen hierboven te volgen, kunt u beeldschaling integreren in elke Java‑applicatie, met snelle, betrouwbare resultaten zonder externe tools.

---

**Laatst bijgewerkt:** 2026-06-13  
**Getest met:** Aspose.PSD voor Java 24.12 (latest)  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Afbeelding schalen Java - Gebruik van Resize Type-enumeratie in Aspose.PSD voor Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [Hoge kwaliteit afbeelding schalen met Bicubic Resampler in Aspose.PSD voor Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Hoe PSD naar PNG converteren en proportioneel schalen met Aspose.PSD voor Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}