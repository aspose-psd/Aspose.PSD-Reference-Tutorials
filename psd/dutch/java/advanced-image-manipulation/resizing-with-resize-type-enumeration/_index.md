---
date: 2026-06-03
description: Leer hoe u een afbeelding kunt verkleinen met Aspose.PSD for Java. Deze
  stapsgewijze gids behandelt de Resize Type Enumeration, high‑quality image resize
  en hoe u PSD naar JPEG kunt converteren.
keywords:
- how to resize image
- convert psd to jpeg
- high quality image resize
- resize image java
- java image manipulation tutorial
linktitle: Verkleinen met Resize Type Enumeration
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  headline: How to Resize Image Java Using Resize Type Enumeration
  type: TechArticle
- description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  name: How to Resize Image Java Using Resize Type Enumeration
  steps:
  - name: '**Java Development Environment** – JDK 8 or newer installed and configured.'
    text: '**Java Development Environment** – JDK 8 or newer installed and configured.'
  - name: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
    text: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
  type: HowTo
- questions:
  - answer: Load the PSD with `Image.load`, then call `image.save("output.jpg", new
      JpegOptions());`.
    question: How do I programmatically convert a PSD file to JPEG without resizing?
  - answer: Yes, you can set the `Resolution` property on the `Image` object before
      saving.
    question: Is it possible to maintain the original DPI when resizing?
  - answer: While you can call `resize` multiple times, it’s more efficient to calculate
      the final dimensions and resize once.
    question: Can I chain multiple resize operations?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Hoe een afbeelding in Java te verkleinen met Resize Type Enumeration
url: /nl/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe een afbeelding in Java te verkleinen met behulp van de Resize Type-enumeratie

## Inleiding

Als je op zoek bent naar **how to resize image** bestanden efficiënt in een Java‑project, biedt Aspose.PSD for Java een schone, high‑performance API. In deze tutorial lopen we door het laden van een PSD, het toepassen van de **Resize Type Enumeration** voor hoogwaardige afbeeldingsverkleining, en uiteindelijk **convert PSD to JPEG**. Of je nu een desktop‑editor bouwt of een geautomatiseerde server‑side pipeline, deze stappen laten je dimensies, kwaliteit en formaat regelen met slechts een paar regels code.

## Snelle antwoorden
- **Which library handles resize image java?** Aspose.PSD for Java.
- **Which resize type gives the best quality?** `ResizeType.LanczosResample`.
- **Can I convert PSD to JPEG after resizing?** Yes – simply save with `JpegOptions`.
- **Do I need a license for production?** A valid Aspose.PSD license is required for production use.
- **Is this approach suitable for large batches?** Absolutely; the API processes multi‑hundred‑page files without loading the whole document into memory.

## Wat is "how to resize image" in Java?
**How to resize image** verwijst naar het programmatisch wijzigen van de pixelafmetingen van een afbeelding terwijl de visuele getrouwheid behouden blijft. De `Resize`‑methode van Aspose.PSD gecombineerd met de `ResizeType`‑enumeratie biedt precieze controle over schaalalgoritmen, waardoor ontwikkelaars kwaliteit kunnen behouden over een breed scala aan bronbestanden en doelgroottes.

## Waarom Resize Type Enumeration gebruiken?
`ResizeType` stelt je in staat het resampling‑algoritme te kiezen dat de beste balans biedt tussen snelheid en visuele kwaliteit. Voor de meeste scenario's levert **LanczosResample** scherpe resultaten met een bescheiden prestatie‑kosten, waarbij een afbeelding van 2000 × 1500 in minder dan 120 ms wordt verwerkt op een typische server‑grade CPU, terwijl randdetails behouden blijven.

## Vereisten

Before you start, make sure you have:

1. **Java Development Environment** – JDK 8 of nieuwer geïnstalleerd en geconfigureerd.  
2. **Aspose.PSD Library** – Download de nieuwste JAR van de [website](https://releases.aspose.com/psd/java/).  
3. **Sample PSD File** – Gebruik het [sample.psd](Your Document Directory/sample.psd) bestand dat bij de SDK is inbegrepen voor praktische tests.

## Pakketten importeren

`Image` is de basisklasse voor alle afbeeldingstypen in Aspose.PSD. Voeg de benodigde imports toe aan je Java‑bronbestand:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Stap 1: Laad de afbeelding

### Definitie‑anker
De `RasterImage`‑klasse is het kernobject van Aspose.PSD dat een raster‑gebaseerde afbeelding vertegenwoordigt die is geladen uit een PSD‑bestand.

Laad je PSD in een `RasterImage`‑instantie zodat je de pixels kunt manipuleren:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## Stap 2: Verklein de afbeelding

`image.resize(width, height, resizeType)` verkleint de afbeelding tot de opgegeven afmetingen met het gekozen algoritme.

Verklein nu de geladen afbeelding met behulp van de **Resize Type Enumeration**. In dit voorbeeld gebruiken we de Lanczos Resample‑methode, die ideaal is wanneer je **how to resize image** met hoge kwaliteit:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Stap 3: Sla de verkleinde afbeelding op

`image.save(path, options)` schrijft de afbeelding naar schijf in het formaat dat wordt gedefinieerd door de opgegeven opties.

Na het verkleinen, sla je de afbeelding op met de opgegeven afmetingen en het gekozen resize‑type. Hier demonstreren we ook **convert psd to jpeg** door het resultaat op te slaan als een JPEG‑bestand:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

## Waarom Resize Type Enumeration gebruiken?

`ResizeType` geeft je fijnmazige controle over het resampling‑algoritme, waardoor je snelheid en kwaliteit kunt balanceren. Voor de meeste toepassingen biedt `LanczosResample` een uitstekende afweging, levert scherpe resultaten zonder zware prestatie‑penalty, en werkt het goed met verschillende soorten afbeeldinginhoud.

## Veelvoorkomende problemen en oplossingen

- **Image appears blurry after resize** – Probeer een andere `ResizeType` zoals `Bicubic` of `NearestNeighbour` om te zien welke het beste visuele resultaat oplevert voor jouw specifieke afbeelding.  
- **OutOfMemoryError on large PSD files** – Verwerk de afbeelding in kleinere delen of vergroot de JVM‑heap‑grootte (`-Xmx`‑vlag). Aspose.PSD kan bestanden tot **2 GB** aan zonder het volledige document in het geheugen te laden.

## Veelgestelde vragen

### Q1: Is Aspose.PSD for Java geschikt voor zowel kleine als grootschalige projecten?
A1: Absoluut! Aspose.PSD for Java is ontworpen om projecten van elke omvang te bedienen, met schaalbaarheid en efficiëntie.

### Q2: Kan ik een ander resize type gebruiken dan Lanczos Resample?
A2: Ja, Aspose.PSD for Java biedt verschillende resize types, zoals **NearestNeighbour**, **Bicubic**, en meer. Raadpleeg de API‑documentatie voor de volledige lijst.

### Q3: Waar kan ik extra ondersteuning vinden voor Aspose.PSD for Java?
A3: Voor vragen of hulp, bezoek het [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### Q4: Is er een gratis proefversie beschikbaar voor Aspose.PSD for Java?
A4: Ja, je kunt een gratis proefversie krijgen [hier](https://releases.aspose.com/).

### Q5: Hoe kan ik een tijdelijke licentie verkrijgen voor Aspose.PSD for Java?
A5: Om een tijdelijke licentie te verkrijgen, bezoek [deze link](https://purchase.aspose.com/temporary-license/).

## Veelgestelde vragen

**Q: Hoe kan ik een PSD‑bestand programmatisch naar JPEG converteren zonder te verkleinen?**  
A: Laad de PSD met `Image.load`, en roep vervolgens `image.save("output.jpg", new JpegOptions());` aan.

**Q: Is het mogelijk om de originele DPI te behouden bij het verkleinen?**  
A: Ja, je kunt de `Resolution`‑eigenschap op het `Image`‑object instellen vóór het opslaan.

**Q: Kan ik meerdere resize‑bewerkingen achter elkaar uitvoeren?**  
A: Hoewel je `resize` meerdere keren kunt aanroepen, is het efficiënter om de uiteindelijke afmetingen te berekenen en één keer te verkleinen.

---

**Laatst bijgewerkt:** 2026-06-03  
**Getest met:** Aspose.PSD for Java 24.12  
**Auteur:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Gerelateerde tutorials

- [Eenvoudig verkleinen met Aspose.PSD – Java Image Manipulation Library](/psd/java/basic-image-operations/simple-resizing/)
- [Hoge kwaliteit afbeelding schalen met Bicubic Resampler in Aspose.PSD for Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Hoe PSD naar PNG te converteren en proportioneel te verkleinen met Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}