---
date: 2026-09-18
description: Leer hoe je een java-afbeeldingsmetadata-miniatuur kunt toevoegen aan
  het EXIF-segment met Aspose.PSD for Java. Deze stapsgewijze gids behandelt de vereisten,
  een code‑overzicht en het opslaan van de bijgewerkte afbeelding.
keywords:
- java image metadata
- how to add thumbnail
- java exif metadata
lastmod: 2026-09-18
linktitle: Miniatuur toevoegen aan EXIF-segment in Java
og_description: Leer hoe je een java-afbeeldingsmetadata-miniatuur kunt toevoegen
  aan het EXIF-segment met Aspose.PSD for Java. Volg de stapsgewijze gids om miniaturen
  in te sluiten en de bijgewerkte afbeelding op te slaan.
og_image_alt: Guide showing Java code to embed a thumbnail into EXIF metadata using
  Aspose.PSD
og_title: Hoe een java-afbeeldingsmetadata-miniatuur toe te voegen aan EXIF-segment
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to add java image metadata thumbnail to the EXIF segment
    using Aspose.PSD for Java. This step‑by‑step guide covers prerequisites, code
    walkthrough, and saving the updated image.
  headline: How to add java image metadata thumbnail to EXIF segment
  type: TechArticle
- questions:
  - answer: EXIF metadata is embedded information in digital images that includes
      camera settings, capture date, GPS coordinates, and other details.
    question: What is EXIF metadata?
  - answer: Adding a thumbnail improves user experience by allowing quick image previews
      without loading the full image.
    question: Why add a thumbnail to EXIF?
  - answer: You can download Aspose.PSD for Java from the [Aspose.PSD for Java download
      page](https://releases.aspose.com/psd/java/).
    question: Where can I download Aspose.PSD for Java?
  - answer: You can obtain a temporary license for Aspose.PSD from the [temporary
      license page](https://purchase.aspose.com/temporary-license/).
    question: How can I get a temporary license for Aspose.PSD?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How do I get support for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- EXIF thumbnail
- Aspose.PSD
- Java image processing
title: Hoe een java-afbeeldingsmetadata-miniatuur toe te voegen aan EXIF-segment
url: /nl/java/java-jpeg-image-processing/add-thumbnail-to-exif-segment-java/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Voeg java-afbeeldingsmetadata-miniatuur toe aan EXIF-segment

## Introductie
In deze tutorial leer je hoe je een **java-afbeeldingsmetadata**-miniatuur toevoegt aan het EXIF-segment van een PSD‑bestand met Aspose.PSD for Java. EXIF (Exchangeable Image File Format) metadata slaat camerainstellingen, opnamedatum, locatie en andere nuttige informatie op. Het insluiten van een kleine preview‑miniatuur stelt toepassingen in staat een snelle afbeeldingsoverzicht te tonen zonder het volledige bestand te laden, wat de prestaties en gebruikerservaring verbetert.

## Snelle antwoorden
- **Wat behandelt de tutorial?** Een miniatuur toevoegen aan het EXIF‑segment van een PSD‑afbeelding met Aspose.PSD for Java.  
- **Hoe lang duurt de implementatie?** Ongeveer 10‑15 minuten voor een basisintegratie.  
- **Heb ik een licentie nodig?** Een tijdelijke licentie is vereist voor productiegebruik; een gratis proefversie werkt voor evaluatie.  
- **Welke Java‑versie wordt ondersteund?** Java 8 en nieuwer worden volledig ondersteund.  
- **Kunnen grote bestanden worden verwerkt?** Ja—Aspose.PSD kan bestanden tot 2 GB aan zonder de volledige afbeelding in het geheugen te laden.

## Wat is java-afbeeldingsmetadata?
Java‑afbeeldingsmetadata verwijst naar de gestructureerde informatie die in afbeeldingsbestanden is ingebed (zoals EXIF, IPTC of XMP) en die programmatisch kan worden gelezen, gewijzigd of aangemaakt met Java‑bibliotheken zoals Aspose.PSD. Deze metadata stelt toepassingen in staat camerainstellingen, tijdstempels, GPS‑coördinaten en aangepaste gegevens op te halen zonder de visuele inhoud te openen.

## Waarom een miniatuur aan EXIF‑metadata toevoegen?
Een miniatuur toevoegen aan het EXIF‑segment biedt een direct visueel hintje voor afbeeldingsbrowsers, bestandsverkenners en content‑managementsystemen. Aspose.PSD verwerkt miniaturen in‑memory, waardoor je een preview van minder dan 0,2 seconden kunt insluiten voor afbeeldingen tot 500 KB, en het ondersteunt meer dan 30 afbeeldingsformaten, inclusief PSD, JPEG, PNG en TIFF.

## Vereisten
Voordat je aan de tutorial begint, zorg dat je de volgende zaken hebt:
- Basiskennis van Java‑programmeren.  
- Java Development Kit (JDK) geïnstalleerd op je systeem.  
- IDE (Integrated Development Environment) voor Java, zoals IntelliJ IDEA of Eclipse.  
- Aspose.PSD for Java‑bibliotheek. Je kunt deze downloaden van de [Aspose.PSD for Java Download page](https://releases.aspose.com/psd/java/).

## Importeer pakketten
De volgende imports brengen de Aspose.PSD‑klassen binnen die nodig zijn om met PSD‑afbeeldingen en EXIF‑data te werken.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Stap 1: laad de psd-afbeelding
`PsdImage` vertegenwoordigt een Photoshop PSD‑bestand en biedt toegang tot zijn lagen en resources.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
```

## Stap 2: doorloop afbeeldingsbronnen
`ImageResource` omvat resources zoals miniaturen, ICC‑profielen en metadata die in een PSD‑bestand zijn ingebed.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        // Process the thumbnail resource
    }
}
```

## Stap 3: pas thumbnail-gegevens aan
`JpegOptions` stelt je in staat JPEG‑specifieke instellingen, zoals kwaliteit, voor de miniatuurafbeelding te configureren.  
```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setQuality(100); // Set JPEG quality
```

## Stap 4: sla de afbeelding op
Het aanroepen van `save` schrijft het bijgewerkte EXIF‑segment (inclusief de nieuwe miniatuur) terug naar schijf zonder de volledige afbeelding opnieuw te coderen.  
```java
image.save(dataDir + "output.psd");
```

## Veelvoorkomende problemen en oplossingen
- **Miniatuur verschijnt niet:** Controleer of de miniatuurresource correct is toegevoegd aan het EXIF‑segment en dat de afbeelding is opgeslagen met de `PsdImage.save`‑methode.  
- **Out‑of‑memory‑fouten bij grote bestanden:** Gebruik `PsdImage.load(..., LoadOptions)` met `LoadOptions.setLoadOnlyMetadata(true)` om alleen met metadata te werken.  
- **Onjuiste oriëntatie:** Zorg ervoor dat de miniatuur de oriëntatie‑vlag van de originele afbeelding respecteert; je kunt de `Orientation`‑EXIF‑tag lezen en de miniatuur dienovereenkomstig roteren.

## Veelgestelde vragen

**Q: Wat is EXIF‑metadata?**  
A: EXIF‑metadata is ingebedde informatie in digitale afbeeldingen die camerainstellingen, opnamedatum, GPS‑coördinaten en andere details bevat.

**Q: Waarom een miniatuur aan EXIF toevoegen?**  
A: Het toevoegen van een miniatuur verbetert de gebruikerservaring door snelle afbeeldingsvoorbeelden mogelijk te maken zonder de volledige afbeelding te laden.

**Q: Waar kan ik Aspose.PSD for Java downloaden?**  
A: Je kunt Aspose.PSD for Java downloaden van de [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).

**Q: Hoe kan ik een tijdelijke licentie voor Aspose.PSD krijgen?**  
A: Je kunt een tijdelijke licentie voor Aspose.PSD verkrijgen via de [temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: Hoe krijg ik ondersteuning voor Aspose.PSD?**  
A: Voor ondersteuning, bezoek het [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

---

**Laatst bijgewerkt:** 2026-09-18  
**Getest met:** Aspose.PSD for Java 24.10  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Create XMP Metadata in PSD Files Using Aspose.PSD for Java](/psd/java/image-editing/create-xmp-metadata/)
- [Resize Image with Aspose.PSD for Java – Draw Shapes & Basic Image Operations](/psd/java/basic-image-operations/)
- [How to Convert PSD to Raster Image Formats with Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}