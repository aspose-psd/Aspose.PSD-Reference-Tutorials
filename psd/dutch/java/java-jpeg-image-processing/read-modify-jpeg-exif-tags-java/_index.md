---
date: 2026-10-03
description: Leer hoe je java afbeeldingsmetadata leest en JPEG EXIF-tags wijzigt
  met Aspose.PSD for Java in deze stapsgewijze gids, perfect voor ontwikkelaars die
  afbeeldingsmetadata efficiënt verwerken.
keywords:
- java read image metadata
- read EXIF tags Java
- modify JPEG metadata Java
- Aspose.PSD Java
lastmod: 2026-10-03
linktitle: Lees en wijzig JPEG EXIF-tags in Java
og_description: Leer hoe je java afbeeldingsmetadata leest en JPEG EXIF-tags wijzigt
  met Aspose.PSD for Java. Deze gids toont stapsgewijze code voor het extraheren en
  bijwerken van EXIF-informatie.
og_image_alt: Guide showing how to java read image metadata and edit JPEG EXIF tags
  using Aspose.PSD for Java
og_title: Hoe java afbeeldingsmetadata leest en JPEG EXIF-tags wijzigt
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  headline: How to java read image metadata and modify JPEG EXIF tags
  type: TechArticle
- description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  name: How to java read image metadata and modify JPEG EXIF tags
  steps:
  - name: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
    text: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
  type: HowTo
- questions:
  - answer: EXIF (Exchangeable Image File Format) metadata stores camera settings,
      timestamps, GPS coordinates, and other information embedded in JPEG and other
      image files.
    question: What is EXIF data?
  - answer: You can get a free trial from the [Aspose releases page](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for Java for free?
  - answer: Aspose.PSD for Java supports Java SE 7 and above.
    question: Is Aspose.PSD for Java compatible with all versions of Java?
  - answer: Check out the [documentation](https://reference.aspose.com/psd/java/)
      for more details.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: You can get support from the [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).
    question: How do I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- exif tags
- aspose psd
- jpeg metadata
- java tutorial
title: Hoe java afbeeldingsmetadata leest en JPEG EXIF-tags wijzigt
url: /nl/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# JPEG EXIF-tags lezen en wijzigen in Java

## Introductie
Als je **java read image metadata** van JPEG‑bestanden moet lezen en programmatically wijzigen, ben je op de juiste plek. In deze tutorial lopen we door het extraheren en bijwerken van EXIF‑tags met Aspose.PSD for Java. Aan het einde kun je cameragegevens, oriëntatie en aangepaste velden ophalen en ze terugschrijven naar het bestand — allemaal zonder een grafische editor.

## Snelle antwoorden
- **Welke bibliotheek verwerkt JPEG EXIF in Java?** Aspose.PSD for Java.
- **Hoeveel regels code zijn nodig om EXIF te lezen?** Ongeveer drie regels na het laden van de afbeelding.
- **Kun je EXIF-tags wijzigen?** Ja, je kunt elke standaard‑ of aangepaste tag wijzigen en het resultaat opslaan.
- **Ondersteunde afbeeldingsformaten?** Meer dan 150 formaten, waaronder PSD, JPEG, PNG, TIFF en BMP.
- **Minimale Java‑versie?** Java 7 of hoger.

## Waarom Aspose.PSD for Java gebruiken?
Aspose.PSD ondersteunt **150+ afbeeldingsformaten** en kan bestanden tot **2 GB** verwerken zonder het volledige document in het geheugen te laden, waardoor je snelle, geheugen‑efficiënte metadata‑bewerkingen op grote fotocollecties krijgt. Het biedt ook een eenvoudige API voor het lezen en schrijven van EXIF-, IPTC- en XMP-gegevens, waardoor batchverwerking van duizenden afbeeldingen efficiënt en betrouwbaar is.

## Voorwaarden
1. **Java Development Kit (JDK)** – zorg ervoor dat je JDK 11 of nieuwer hebt. Je kunt het downloaden van de [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – haal de nieuwste JAR van de [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, of een andere editor naar keuze.  
4. **Basiskennis van Java** – je moet vertrouwd zijn met het maken van projecten en het toevoegen van externe JAR‑bestanden.

## Wat is Java read image metadata?
Java read image metadata verwijst naar het proces van programmatic toegang tot ingebedde informatie zoals EXIF, IPTC en XMP die in afbeeldingsbestanden is opgeslagen met Java‑code. Deze metadata kan camerainstellingen, tijdstempels, GPS‑coördinaten, copyright‑vermeldingen en gebruikerscommentaren bevatten, waardoor applicaties afbeeldingen kunnen organiseren, zoeken en manipuleren op basis van hun beschrijvende gegevens.

## Pakketten importeren
Voeg eerst de Aspose.PSD JAR toe aan de classpath van je project en importeer de benodigde klassen.

Het `com.aspose.psd`‑pakket biedt de kern‑API voor het laden van afbeeldingen en het benaderen van hun resources.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Hoe lees je afbeeldingsmetadata van JPEG‑bestanden in Java?
Laad de JPEG met `PsdImage.load("image.jpg")`, zoek de thumbnail‑resource die EXIF‑gegevens bevat, en roep vervolgens `ExifData.read()` aan om een gevulde `ExifData`‑object te verkrijgen. Deze één‑stap‑benadering geeft je volledige toegang tot alle standaard‑EXIF‑velden en eventuele aangepaste tags die je hebt toegevoegd.

## Stap 1: Laad de PSD‑afbeelding
PsdImage is de Aspose.PSD‑klasse die een PSD‑bestand vertegenwoordigt en biedt methoden om toegang te krijgen tot zijn resources en metadata.  
In deze stap laden we de PSD‑afbeelding waarvan we de EXIF‑gegevens willen lezen. Zorg ervoor dat je afbeelding zich in de juiste map bevindt.

```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Stap 2: Doorloop afbeeldingsresources
ThumbnailResource vertegenwoordigt een miniatuurafbeelding die in een PSD‑bestand is opgeslagen, vaak met ingebedde EXIF‑gegevens.  
Zodra de afbeelding is geladen, is de volgende stap om door de resources te itereren om de thumbnail‑resource te vinden, die doorgaans de EXIF‑gegevens bevat.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Proceed to next step
    }
}
```

## Stap 3: EXIF‑gegevens extraheren
JpegExifData is de klasse die EXIF‑informatie bevat die uit een JPEG‑afbeelding is gehaald, waardoor je individuele tags kunt lezen en wijzigen.  
Nu we de thumbnail‑resource hebben, kunnen we de EXIF‑gegevens ervan extraheren. EXIF‑gegevens omvatten waardevolle informatie zoals de naam van de camerabezitter, de diafragmawaarde, oriëntatie en meer.

```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```

## Stap 4: EXIF‑gegevens wijzigen
Na het lezen van de EXIF‑gegevens wil je mogelijk enkele velden wijzigen. Hier is hoe je dat kunt doen:

```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```

## Stap 5: Sla de wijzigingen op
Tot slot, na het wijzigen van de EXIF‑gegevens, sla je de wijzigingen op in een nieuw PSD‑bestand.

```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Veelvoorkomende problemen en oplossingen
- **Ontbrekende thumbnail‑resource** – Sommige JPEG‑bestanden slaan EXIF direct op in de hoofd‑image‑header. Als de thumbnail‑resource ontbreekt, gebruik dan `image.getExifData()`.
- **Grote bestanden veroorzaken OutOfMemoryError** – Zorg ervoor dat je de JVM start met voldoende heap (`-Xmx2g`) of verwerk de afbeelding in streaming‑modus met `PsdImage.load(inputStream, loadOptions)`.
- **Niet‑ondersteunde tagtypen** – Aspose.PSD ondersteunt alle standaard EXIF‑tags; aangepaste tags kunnen handmatige byte‑niveau verwerking vereisen.

## Veelgestelde vragen

**Q: Wat is EXIF‑data?**  
A: EXIF (Exchangeable Image File Format) metadata slaat camerainstellingen, tijdstempels, GPS‑coördinaten en andere informatie op die in JPEG‑ en andere afbeeldingsbestanden is ingebed.

**Q: Kan ik Aspose.PSD for Java gratis gebruiken?**  
A: Je kunt een gratis proefversie krijgen via de [Aspose releases page](https://releases.aspose.com/).

**Q: Is Aspose.PSD for Java compatibel met alle versies van Java?**  
A: Aspose.PSD for Java ondersteunt Java SE 7 en hoger.

**Q: Waar kan ik meer documentatie vinden over Aspose.PSD for Java?**  
A: Bekijk de [documentation](https://reference.aspose.com/psd/java/) voor meer details.

**Q: Hoe krijg ik ondersteuning voor Aspose.PSD for Java?**  
A: Je kunt ondersteuning krijgen via het [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).

## Conclusie
Door deze stappen te volgen kun je **java read image metadata** van elke JPEG lezen, de benodigde EXIF‑velden aanpassen en de bijgewerkte gegevens terugschrijven naar het bestand — allemaal met een paar regels nette Java‑code. De rijke API van Aspose.PSD maakt metadata‑verwerking betrouwbaar en performant, zodat je het kunt integreren in batch‑verwerkingspijplijnen, fotobeheer‑tools of elke applicatie die met afbeeldingsinformatie moet werken.

---

**Last Updated:** 2026-10-03  
**Tested With:** Aspose.PSD for Java 24.5  
**Author:** Aspose

## Gerelateerde tutorials

- [Specifieke EXIF‑taginformatie lezen in Java met Aspose (asp)](/psd/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/)
- [XMP-metadata maken in PSD‑bestanden met Aspose.PSD for Java](/psd/java/image-editing/create-xmp-metadata/)
- [Afbeelding schalen met Aspose.PSD for Java – Vormen tekenen & basis afbeeldingsbewerkingen](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}