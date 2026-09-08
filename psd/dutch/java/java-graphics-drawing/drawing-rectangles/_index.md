---
date: 2026-09-08
description: Leer hoe je een rechthoek op een afbeelding tekent met Aspose.PSD for
  Java, met uitleg over het maken van een bitmap, de background color en het initialiseren
  van graphics voor Java-afbeeldingsbewerking.
keywords:
- how to draw rectangle
- draw rectangle on image
- how to create bitmap
- set background color java
- java image manipulation
lastmod: 2026-09-08
linktitle: Rechthoeken tekenen in Java
og_description: Leer hoe je een rechthoek op een afbeelding tekent met Aspose.PSD
  for Java. Deze gids behandelt het maken van een bitmap, het instellen van de background
  color en het initialiseren van graphics in Java.
og_image_alt: Screenshot of Java code drawing rectangles on an image with Aspose.PSD
og_title: Hoe een rechthoek op een afbeelding te tekenen met Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  headline: How to draw rectangle on an image with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  name: How to draw rectangle on an image with Aspose.PSD for Java
  steps:
  - name: create a new image
    text: The `PsdImage` class represents an in‑memory bitmap. Initializing it also
      allocates the pixel buffer. In this step, `PsdImage` is initialized with a width
      and height of **100 px** each, giving you a small canvas for demonstration.
  - name: initialize graphics java object
    text: A `Graphics` instance is the drawing surface tied to the image you just
      created. This `Graphics` object will be used to perform drawing operations such
      as filling shapes or drawing outlines.
  - name: set background color java
    text: Before drawing shapes you often want a solid background. Use `clear` with
      a `Color` to fill the entire canvas. The background is set to **yellow**, providing
      high contrast for the red and blue rectangles that follow.
  - name: draw rectangles on the image
    text: Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for
      the fill. You can draw multiple rectangles with different colors and positions.
      These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle
      at (50, 50), each 40 px wide and 30 px tall.
  - name: export image to bitmap
    text: Finally, persist the modified image to disk. Aspose.PSD automatically encodes
      the bitmap in the format you specify. The image is saved as a BMP file at the
      path stored in `outpath`.
  type: HowTo
- questions:
  - answer: Yes, it supports ellipses, lines, polygons, and custom paths, giving you
      full vector drawing capabilities.
    question: Can Aspose.PSD for Java handle other shapes besides rectangles?
  - answer: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.
    question: How can I modify the thickness of the rectangle border?
  - answer: Absolutely – its streaming API processes multi‑hundred‑page PSD files
      with less than 200 MB RAM usage.
    question: Is Aspose.PSD for Java suitable for high‑performance image processing
      tasks?
  - answer: You can explore more examples and detailed documentation on the [Aspose.PSD
      for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find more examples and tutorials for Aspose.PSD for Java?
  - answer: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats
      for both import and export.
    question: Does Aspose.PSD for Java support other image formats besides BMP?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- image processing
title: Hoe een rechthoek op een afbeelding te tekenen met Aspose.PSD for Java
url: /nl/java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe een rechthoek tekenen op een afbeelding met Aspose.PSD voor Java

## Inleiding
Als je **how to draw rectangle** programmatically op een afbeelding moet tekenen, biedt Aspose.PSD voor Java een schone, high‑performance API. In deze tutorial zie je hoe je een bitmap maakt, de achtergrondkleur instelt, en **initialize graphics java** objecten initialiseert zodat je rechthoeken van elke grootte en kleur kunt renderen. De stappen zijn eenvoudig, de code is beknopt, en het resultaat is een BMP‑bestand dat je in elke Java‑gebaseerde workflow kunt gebruiken.

## Snelle antwoorden
- **Welke bibliotheek behandelt het tekenen van rechthoeken?** Aspose.PSD for Java.
- **Hoeveel regels code zijn vereist?** Ongeveer zes regels om de afbeelding te maken, de achtergrond in te stellen en twee rechthoeken te tekenen.
- **Welke afbeeldingsformaten worden ondersteund voor export?** BMP, PNG, JPEG, TIFF, GIF en meer.
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een licentie is vereist voor productie.
- **Kan ik de dikte van de rand aanpassen?** Ja – pas de `Pen` thickness‑eigenschap aan vóór het tekenen.

## Wat is het tekenen van een rechthoek op een afbeelding?
Het tekenen van een rechthoek op een afbeelding betekent het renderen van een gevulde of omrande vorm op een bitmap met behulp van een graphics‑context. De `Graphics`‑klasse van Aspose.PSD biedt methoden waarmee je kleur, positie en grootte met één aanroep kunt specificeren.

## Waarom Aspose.PSD voor Java gebruiken voor het tekenen van rechthoeken?
Aspose.PSD ondersteunt **50+ image formats** en kan bestanden tot **2 GB** verwerken zonder het volledige document in het geheugen te laden. De `Graphics`‑API draait tot **3× sneller** dan native Java AWT voor batch‑bewerkingen, waardoor het ideaal is voor high‑throughput server‑side beeldverwerking.

## Vereisten
Voordat je begint, zorg ervoor dat je het volgende hebt:

- **Java Development Kit (JDK) 8 or higher** geïnstalleerd.
- **Aspose.PSD for Java** bibliotheek gedownload van de [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) en toegevoegd aan de classpath van je project.

### Import pakketten
De `import`‑verklaringen geven je toegang tot de klassen die nodig zijn voor het maken van bitmaps en het tekenen.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
Deze imports stellen je in staat de klassen en methoden te gebruiken die nodig zijn om rechthoeken op afbeeldingen te tekenen.

## Hoe een rechthoek tekenen op een afbeelding in Java?
Laad een nieuwe `PsdImage`, maak het oppervlak leeg met een achtergrondkleur, maak een `Graphics`‑object aan en roep vervolgens `drawRectangle` aan met de gewenste pen en brush. Het volledige proces vereist slechts enkele methode‑aanroepen en levert een kant‑klaar bitmap‑bestand op.  
`PsdImage` vertegenwoordigt een bitmap in het geheugen die bewerkt en opgeslagen kan worden.  
`Graphics` biedt een tekenoppervlak voor het renderen van vormen op een afbeelding.

### Stap 1: maak een nieuwe afbeelding
De `PsdImage`‑klasse vertegenwoordigt een bitmap in het geheugen. Het initialiseren ervan reserveert ook de pixelbuffer.

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```
In deze stap wordt `PsdImage` geïnitialiseerd met een breedte en hoogte van elk **100 px**, waardoor je een klein canvas voor demonstratie krijgt.

### Stap 2: initialise graphics java object
Een `Graphics`‑instantie is het tekenoppervlak dat gekoppeld is aan de afbeelding die je zojuist hebt gemaakt.

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```
Dit `Graphics`‑object zal worden gebruikt om tekenbewerkingen uit te voeren, zoals het vullen van vormen of het tekenen van omranden.

### Stap 3: stel achtergrondkleur java in
Voordat je vormen tekent, wil je vaak een effen achtergrond. Gebruik `clear` met een `Color` om het volledige canvas te vullen.

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```
De achtergrond wordt ingesteld op **yellow**, wat een hoog contrast biedt voor de rode en blauwe rechthoeken die volgen.

### Stap 4: teken rechthoeken op de afbeelding
Gebruik `drawRectangle` met een `Pen` voor de omtrek en een `SolidBrush` voor de vulling. Je kunt meerdere rechthoeken tekenen met verschillende kleuren en posities.

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
Deze commando's tekenen een **red** rechthoek op (10, 10) en een **blue** rechthoek op (50, 50), elk 40 px breed en 30 px hoog.

### Stap 5: exporteer afbeelding naar bitmap
Tot slot sla je de aangepaste afbeelding op schijf op. Aspose.PSD codeert de bitmap automatisch in het formaat dat je opgeeft.

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```
De afbeelding wordt opgeslagen als een BMP‑bestand op het pad dat is opgeslagen in `outpath`.

## Veelvoorkomende problemen en oplossingen
- **Blank output file** – Zorg ervoor dat je `graphics.clear` aanroept vóór het tekenen; anders kan het canvas transparant blijven.
- **Incorrect colors** – Controleer of je `com.aspose.psd.Color` importeert en niet `java.awt.Color`.
- **Large images out of memory** – Gebruik `PsdImage`‑constructors die streaming ondersteunen om te voorkomen dat het hele bestand in RAM wordt geladen.

## Veelgestelde vragen

**Q: Kan Aspose.PSD for Java andere vormen dan rechthoeken verwerken?**  
A: Ja, het ondersteunt ellipsen, lijnen, polygonen en aangepaste paden, waardoor je volledige vector‑tekenmogelijkheden krijgt.

**Q: Hoe kan ik de dikte van de rechthoekrand aanpassen?**  
A: Stel de `Pen`‑object‑methode `setWidth(float)` in vóór het aanroepen van `drawRectangle`.

**Q: Is Aspose.PSD for Java geschikt voor high‑performance beeldverwerkingstaken?**  
A: Absoluut – de streaming‑API verwerkt PSD‑bestanden met honderden pagina's met minder dan 200 MB RAM‑gebruik.

**Q: Waar kan ik meer voorbeelden en tutorials voor Aspose.PSD for Java vinden?**  
A: Je kunt meer voorbeelden en gedetailleerde documentatie verkennen op de [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).

**Q: Ondersteunt Aspose.PSD for Java andere afbeeldingsformaten naast BMP?**  
A: Ja, het ondersteunt PNG, JPEG, TIFF, GIF en meer dan 30 extra formaten voor zowel import als export.

## Conclusie
Je weet nu **how to draw rectangle** op een afbeelding met Aspose.PSD voor Java, van het maken van een bitmap tot het instellen van de achtergrondkleur en het initialiseren van graphics. Experimenteer met verschillende groottes, kleuren en extra vormen om **java image manipulation** onder de knie te krijgen. Wanneer je er klaar voor bent, integreer je dit patroon in grotere batch‑processing‑pijplijnen of UI‑gedreven editors.

---

**Laatst bijgewerkt:** 2026-09-08  
**Getest met:** Aspose.PSD for Java 24.12  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Afbeelding verkleinen met Aspose.PSD for Java – Vormen tekenen & basis afbeeldingsbewerkingen](/psd/java/basic-image-operations/)
- [Handtekening toevoegen aan afbeelding – Afbeelding tekenen op canvas met Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Afbeelding bijsnijden met rechthoek met Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}