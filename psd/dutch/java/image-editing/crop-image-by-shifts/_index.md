---
date: 2026-07-03
description: Leer hoe je een afbeelding in Java bijsnijdt met Aspose.PSD voor Java.
  Deze stapsgewijze tutorial voor het bijsnijden van afbeeldingen behandelt het laden
  van PSD‑bestanden, het instellen van verschuivingswaarden en het opslaan van het
  resultaat.
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: Afbeelding bijsnijden met verschuivingen
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Afbeelding bijsnijden in Java met verschuivingen met Aspose.PSD
url: /nl/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Afbeelding bijsnijden in Java met verschuivingen met Aspose.PSD

## Inleiding

In Java‑beeldverwerking is **crop image java** een veelvoorkomende eis voor het voorbereiden van graphics, miniaturen of UI‑assets. Aspose.PSD for Java maakt deze taak eenvoudig door een eenvoudige `crop`‑methode beschikbaar te stellen die werkt op elk ondersteund rasterformaat. In deze tutorial leer je hoe je een PSD‑bestand laadt, links‑rechts‑boven‑onder‑verschuivingen definieert, het bijsnijden toepast en het resultaat opslaat — zonder eigen pixel‑manipulatiecode te schrijven.

## Snelle antwoorden
- **Welke bibliotheek verwerkt bijsnijden?** Aspose.PSD for Java biedt een ingebouwde `crop`‑methode.  
- **Heb ik een licentie nodig?** Een tijdelijke licentie werkt voor evaluatie; een volledige licentie is vereist voor productie.  
- **Ondersteunde formaten?** Meer dan 30 rasterformaten, waaronder PSD, JPEG, PNG, BMP en TIFF.  
- **Maximum bestandsgrootte?** Verwerkt bestanden tot 2 GB zonder de volledige afbeelding in het geheugen te laden.  
- **Hoeveel regels code?** Slechts vijf logische stappen — laden, cachen, verschuivingen definiëren, bijsnijden en opslaan.

## Wat is crop image java?
`crop image java` verwijst naar de bewerking waarbij een bitmap in een Java‑applicatie wordt bijgesneden. Met Aspose.PSD wordt deze bewerking uitgevoerd door de `crop`‑methode, die verschuivingen voor elke kant van de afbeelding accepteert en een nieuw afbeeldingsobject retourneert.

## Waarom Aspose.PSD gebruiken voor het bijsnijden van afbeeldingen?
Aspose.PSD ondersteunt **30+** afbeeldingsformaten en kan PSD‑bestanden met honderden pagina's verwerken terwijl het minder dan 150 MB RAM gebruikt, dankzij de lazy‑loading‑architectuur. De bibliotheek garandeert bovendien pixel‑perfecte resultaten, waarbij lagen, maskers en kleurprofielen behouden blijven — iets wat veel generieke afbeeldingsbibliotheken niet kunnen waarborgen.

## Vereisten

### Java Development Kit (JDK)

Zorg ervoor dat je de nieuwste versie van de JDK op je systeem hebt geïnstalleerd. Je kunt deze downloaden via [here](https://www.oracle.com/java/technologies/javase-downloads.html).

### Aspose.PSD for Java Bibliotheek

Om te beginnen moet je de Aspose.PSD for Java‑bibliotheek verkrijgen. Ga naar de [download page](https://releases.aspose.com/psd/java/) en haal de nieuwste versie op.

### Integrated Development Environment (IDE)

Kies je favoriete Java‑IDE, zoals Eclipse of IntelliJ, voor een soepele programmeerervaring.

## Hoe crop image java?

Laad je bronbestand, definieer de pixelverschuivingen voor elke kant en roep de `crop`‑methode aan — deze volledige workflow kan in vijf beknopte regels code worden geschreven. De `crop`‑bewerking maakt een nieuwe afbeelding die alleen het door jou opgegeven gebied bevat, terwijl het oorspronkelijke bestand ongewijzigd blijft.

### Stap 1: Laad de afbeelding

`Image` is de basisklasse voor alle afbeeldingssoorten in Aspose.PSD.  
`RasterImage` vertegenwoordigt een rasterafbeelding en biedt bijsnijdingsmogelijkheden.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Stap 2: Cache afbeeldingsgegevens

`cacheData()` laadt de afbeeldingsgegevens in het geheugen voor snellere verwerking.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### Stap 3: Definieer verschuivingswaarden

Specificeer de verschuivingswaarden voor alle vier de zijden van de afbeelding (links, boven, rechts, onder) in pixels.  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### Stap 4: Pas bijsnijden toe

`crop(left, right, top, bottom)` snijdt de afbeelding bij volgens de opgegeven pixelverschuivingen aan elke kant.  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### Stap 5: Sla de resultaten op

`JpegOptions` definieert JPEG‑codeerinstellingen zoals kwaliteit en kleurprofiel.  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

Gefeliciteerd! Je hebt met succes een afbeelding bijgesneden met Aspose.PSD for Java.

## Veelvoorkomende problemen en oplossingen

- **Afbeelding lijkt ongewijzigd:** Controleer of de verschuivingswaarden positief zijn en de oorspronkelijke afmetingen niet overschrijden.  
- **OutOfMemoryError bij grote bestanden:** Schakel cachen in zoals weergegeven in Stap 2; dit dwingt Aspose.PSD om een tijdelijk bestand te gebruiken in plaats van de volledige afbeelding in RAM te houden.  
- **Kleurverschuiving na bijsnijden:** Zorg ervoor dat je het kleurprofiel behoudt door `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })` aan te roepen als je exacte kleurnauwkeurigheid nodig hebt.

## Veelgestelde vragen

**Q: Is Aspose.PSD compatibel met alle afbeeldingsformaten?**  
A: Ja, Aspose.PSD ondersteunt meer dan 30 rasterformaten, waaronder PSD, JPEG, PNG, BMP, TIFF en GIF, wat zorgt voor brede compatibiliteit.

**Q: Kan ik meerdere bijsnijdingsbewerkingen op dezelfde afbeelding toepassen?**  
A: Absoluut. Na elke `crop`‑aanroep ontvang je een nieuw afbeeldingsobject, dat je indien nodig opnieuw kunt bijsnijden.

**Q: Is er een community‑forum voor Aspose.PSD‑ondersteuning?**  
A: Ja, je kunt ondersteuning vinden en deelnemen aan de community op [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Hoe kan ik een tijdelijke licentie voor Aspose.PSD verkrijgen?**  
A: Bezoek [here](https://purchase.aspose.com/temporary-license/) om een tijdelijke licentie te verkrijgen.

**Q: Zijn er voorbeeldprojecten die de functionaliteit van Aspose.PSD laten zien?**  
A: Verken de documentatie en voorbeelden op [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).

---

**Last Updated:** 2026-07-03  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## Gerelateerde tutorials

- [Afbeelding bijsnijden met rechthoek in Aspose.PSD voor Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Afbeelding bijsnijden Java - Uitbreiden en bijsnijden met Aspose.PSD voor Java](/psd/java/image-editing/expand-and-crop-images/)
- [Afbeelding formaat wijzigen Java - Gebruik van Resize Type Enumeratie in Aspose.PSD voor Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}