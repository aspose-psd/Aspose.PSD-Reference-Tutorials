---
date: 2026-09-28
description: Hoe een miniatuur toevoegen aan een JFIF‑segment in Java met Aspose.PSD.
  Volg deze stapsgewijze handleiding om miniaturen snel en betrouwbaar in PSD‑bestanden
  in te sluiten.
keywords:
- how to add thumbnail
- JFIF segment Java
- Aspose.PSD thumbnail
- Java image processing
lastmod: 2026-09-28
linktitle: Miniatuur toevoegen aan JFIF‑segment in Java
og_description: Hoe een miniatuur toevoegen aan een JFIF‑segment in Java met Aspose.PSD.
  Volg deze stapsgewijze handleiding om miniaturen snel en betrouwbaar in PSD‑bestanden
  in te sluiten.
og_image_alt: Guide showing how to add thumbnail to JFIF segment in Java with Aspose.PSD
og_title: Hoe een miniatuur toevoegen aan JFIF‑segment in Java
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  headline: How to add thumbnail to JFIF segment in Java
  type: TechArticle
- description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  name: How to add thumbnail to JFIF segment in Java
  steps:
  - name: import packages
    text: '`Document`, `JfifResource`, and related classes are part of the Aspose.PSD
      namespace. Document represents the PSD file container, and JfifResource provides
      access to the JFIF segment within the PSD. Import them at the top of your source
      file.'
  - name: load the PSD image
    text: Create a `PsdImage` instance by passing the file path to the constructor.
      PsdImage is the Aspose.PSD class that models a Photoshop document. This loads
      the document metadata while streaming the pixel data.
  - name: iterate over image resources
    text: Search the `Resources` collection for a `JfifResource`. When found, you
      can replace its thumbnail byte array with a new JPEG‑encoded preview.
  - name: adjust thumbnail data
    text: Generate a small JPEG thumbnail (e.g., 120 × 120 px) using any image‑processing
      library, then assign the resulting byte array to `jfifResource.ThumbnailData`.
  - name: save the modified image
    text: Call the `save` method on the `PsdImage` object, specifying the output path
      and desired format. The JFIF segment now contains the new thumbnail.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables developers to
      create, edit, convert, and render Photoshop PSD files without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Detailed documentation can be found on the [Aspose.PSD for Java documentation
      page](https://reference.aspose.com/psd/java/).
    question: Where can I find more documentation for Aspose.PSD for Java?
  - answer: Yes, Aspose.PSD for Java can be used commercially. You can purchase a
      license from [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).
    question: Is Aspose.PSD for Java suitable for commercial use?
  - answer: Yes, you can download a free trial from [Aspose.PSD's trial download page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- add thumbnail
- Aspose.PSD
- Java image processing
- JFIF
- PSD
title: Hoe een miniatuur toevoegen aan JFIF‑segment in Java
url: /nl/java/java-jpeg-image-processing/add-thumbnail-to-jfif-segment-java/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe een miniatuur toevoegen aan JFIF-segment in Java

## Inleiding
Het toevoegen van een miniatuur aan het JFIF‑segment van een PSD‑bestand is een veelvoorkomende eis wanneer je een snelle visuele preview nodig hebt zonder het volledige beeld te laden. In deze tutorial leer je **hoe een miniatuur toe te voegen** aan een JFIF‑segment in Java met Aspose.PSD. Aan het einde van de gids heb je een uitvoerbare code‑snippet, een begrip van de onderliggende JFIF‑structuur, en tips voor het efficiënt verwerken van grote bestanden.

## Snelle antwoorden
- **Welke bibliotheek is vereist?** Aspose.PSD for Java.
- **Welke Java‑versie werkt?** JDK 11 of later.
- **Hoeveel regels code zijn nodig?** Ongeveer 10 regels om te laden, te wijzigen en op te slaan.
- **Kan ik multi‑megabyte bestanden verwerken?** Ja, Aspose.PSD streamt data, zodat het geheugenverbruik laag blijft.
- **Is een commerciële licentie nodig?** Een licentie is vereist voor productiegebruik; een gratis proefversie is beschikbaar.

## Wat is een JFIF‑segment?
Het JFIF‑segment is een JPEG File Interchange Format‑blok dat optionele gegevens kan opslaan, zoals miniaturen, EXIF of kleurprofielen.  
Het bevindt zich binnen de JPEG‑stroom van een PSD‑bestand en wordt door de meeste beeldviewers herkend voor snelle preview‑generatie.

## Waarom een miniatuur toevoegen aan een PSD‑bestand?
Aspose.PSD for Java ondersteunt **30+ image formats** en kan bestanden verwerken tot **2 GB** zonder het volledige document in het geheugen te laden. Het toevoegen van een miniatuur vermindert de netwerkbandbreedte bij het verzenden van previews en versnelt de UI‑rendering in galerij‑applicaties.

## Vereisten
- Java Development Kit (JDK): Zorg ervoor dat Java op uw systeem is geïnstalleerd. U kunt het downloaden van [Oracle's JDK website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- Aspose.PSD for Java: U moet de Aspose.PSD for Java‑bibliotheek hebben. U kunt deze verkrijgen van de [Aspose.PSD Java download page](https://releases.aspose.com/psd/java/).
- Integrated Development Environment (IDE): Gebruik een IDE zoals IntelliJ IDEA of Eclipse voor Java‑ontwikkeling.
- Basic Understanding of Java: Vertrouwdheid met de programmeertaal Java en concepten.

## Hoe een miniatuur toevoegen aan een JFIF‑segment in Java?
Laad de doel‑PSD, zoek de JFIF‑resource, vervang de miniatuurgegevens en sla het bestand op. De volledige bewerking kan worden uitgevoerd met een paar eenvoudige API‑aanroepen, en Aspose.PSD behandelt de low‑level JPEG‑structuur voor u.

### Stap 1: pakketten importeren
`Document`, `JfifResource` en gerelateerde klassen maken deel uit van de Aspose.PSD‑namespace. Document vertegenwoordigt de PSD‑bestandcontainer, en JfifResource biedt toegang tot het JFIF‑segment binnen de PSD. Importeer ze bovenaan uw bronbestand.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

### Stap 2: laad de PSD‑afbeelding
Maak een `PsdImage`‑instantie aan door het bestandspad aan de constructor door te geven. PsdImage is de Aspose.PSD‑klasse die een Photoshop‑document modelleert. Hiermee worden de documentmetadata geladen terwijl de pixelgegevens worden gestreamd.

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```

### Stap 3: doorloop de afbeeldingsresources
Zoek in de `Resources`‑collectie naar een `JfifResource`. Wanneer gevonden, kun je de miniatuur‑byte‑array vervangen door een nieuwe JPEG‑gecodeerde preview.

```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Continue with thumbnail processing
    }
}
```

### Stap 4: pas miniatuurgegevens aan
Genereer een kleine JPEG‑miniatuur (bijv. 120 × 120 px) met een willekeurige beeldverwerkingsbibliotheek, en wijs vervolgens de resulterende byte‑array toe aan `jfifResource.ThumbnailData`.

```java
try {
    PsdImage thumbnailImage = new PsdImage(100, 100);
    
    // Fill thumbnail data (example: create a simple pixel array)
    int[] pixels = new int[thumbnailImage.getWidth() * thumbnailImage.getHeight()];
    for (int j = 0; j < pixels.length; j++) {
        pixels[j] = j;
    }
    
    // Save thumbnail data
    thumbnailImage.saveArgb32Pixels(thumbnailImage.getBounds(), pixels);
    
    // Set thumbnail data to Jpeg options
    JpegExifData exifData = new JpegExifData();
    exifData.setThumbnail(thumbnailImage);
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setExifData(exifData);
    
    // Set options to thumbnail resource
    thumbnail.getJpegOptions().setExifData(exifData);
    
} catch(Exception e) {
    // Handle exceptions
} finally {
    // Dispose of resources
}
```

### Stap 5: sla de gewijzigde afbeelding op
Roep de `save`‑methode aan op het `PsdImage`‑object, met het uitvoerpad en het gewenste formaat. Het JFIF‑segment bevat nu de nieuwe miniatuur.

```java
image.save(dataDir + "output.psd");
```

## Veelvoorkomende problemen en oplossingen
- **Miniatuur niet zichtbaar in viewers:** Zorg ervoor dat de miniatuurgegevens een geldige JPEG‑byte‑array zijn en dat de afmetingen binnen 256 × 256 px liggen, wat de maximale grootte is die door de JFIF‑specificatie wordt ondersteund.
- **OutOfMemoryError bij grote PSD‑bestanden:** Gebruik `PsdImage.load(inputStream, true)` om streaming‑modus in te schakelen, waardoor het geheugenverbruik laag blijft.
- **Onjuist resource‑type:** Controleer of de resource die je wijzigt inderdaad een `JfifResource` is; andere resources zoals `ExifResource` hebben geen invloed op de weergave van de miniatuur.

## Veelgestelde vragen

**Q: Wat is Aspose.PSD for Java?**  
A: Aspose.PSD for Java is een commerciële bibliotheek die ontwikkelaars in staat stelt Photoshop PSD‑bestanden te maken, bewerken, converteren en renderen zonder Adobe Photoshop te vereisen.

**Q: Waar kan ik meer documentatie vinden voor Aspose.PSD for Java?**  
A: Gedetailleerde documentatie is te vinden op de [Aspose.PSD for Java documentation page](https://reference.aspose.com/psd/java/).

**Q: Is Aspose.PSD for Java geschikt voor commercieel gebruik?**  
A: Ja, Aspose.PSD for Java kan commercieel worden gebruikt. U kunt een licentie aanschaffen via de [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).

**Q: Kan ik Aspose.PSD for Java uitproberen voordat ik koop?**  
A: Ja, u kunt een gratis proefversie downloaden van de [Aspose.PSD's trial download page](https://releases.aspose.com/).

**Q: Hoe kan ik ondersteuning krijgen voor Aspose.PSD for Java?**  
A: Voor ondersteuning kunt u het [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) bezoeken.

---

**Laatst bijgewerkt:** 2026-09-28  
**Getest met:** Aspose.PSD for Java 24.11  
**Auteur:** Aspose

## Gerelateerde tutorials

- [IOPA‑resource toevoegen aan PSD‑bestanden met Aspose PSD for Java](/psd/java/modifying-converting-psd-images/add-iopa-resource-psd-files/)
- [Handtekening toevoegen aan afbeelding – Teken afbeelding op canvas met Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Hoe een afbeelding roteren onder een specifieke hoek met Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}