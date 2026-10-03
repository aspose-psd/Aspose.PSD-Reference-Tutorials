---
date: 2026-10-03
description: Leer hoe u een miniatuur uit een PSD in Java kunt extraheren met Aspose.PSD.
  Deze stapsgewijze gids behandelt de installatie, code‑fragmenten en het opslaan
  van de miniatuur als een JPEG‑afbeelding.
keywords:
- extract thumbnail from psd
- java aspose psd
- psd thumbnail extraction
lastmod: 2026-10-03
linktitle: Miniatuur extraheren uit PSD in Java
og_description: Leer hoe u een miniatuur uit een PSD in Java kunt extraheren met Aspose.PSD.
  Deze gids leidt u door de installatie, het laden van het bestand, het extraheren
  van de miniatuur en het opslaan ervan als een JPEG‑afbeelding.
og_image_alt: Screenshot showing Java code extracting a thumbnail from a PSD file
  using Aspose.PSD
og_title: Miniatuur extraheren uit PSD in Java met Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to extract thumbnail from PSD in Java using Aspose.PSD. This
    step‑by‑step guide covers setup, code snippets, and saving the thumbnail as a
    JPEG image.
  headline: Extract thumbnail from PSD in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is a Java library that enables programmatic creation, manipulation,
      and conversion of PSD and other raster image formats without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD?
  - answer: You can refer to the [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references and examples.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library’s capabilities.
    question: Can I try Aspose.PSD for free before purchasing?
  - answer: Temporary licenses are available from the [temporary license](https://purchase.aspose.com/temporary-license/)
      page.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Yes, Aspose.PSD can be used in both personal and commercial projects under
      its licensing terms.
    question: Is Aspose.PSD suitable for commercial use?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose.psd
- thumbnail extraction
title: Miniatuur extraheren uit PSD in Java
url: /nl/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Thumbnail uit PSD extraheren in Java

## Inleiding
Extracting a thumbnail from a PSD file lets you generate quick previews without loading the full‑resolution image. In Java, Aspose.PSD makes this process straightforward and performant. In this tutorial you’ll learn how to set up the library, locate the thumbnail resource, and save it as a JPEG file—all with just a few lines of code.

## Snelle antwoorden
- **Welke bibliotheek behandelt PSD‑miniaturen?** Aspose.PSD for Java.
- **Hoeveel regels code zijn vereist?** Ongeveer vijf regels om te laden, extraheren en op te slaan.
- **Kan ik miniaturen extraheren uit grote PSD‑bestanden?** Ja, Aspose.PSD verwerkt bestanden tot 500 MB zonder volledige geheugenlading.
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor evaluatie; een licentie is vereist voor productie.
- **Welke uitvoerformaten worden ondersteund?** De geëxtraheerde thumbnail kan worden opgeslagen als JPEG, PNG of BMP.

## Wat is thumbnail extraheren uit PSD?
Extract thumbnail from PSD is the process of reading the small preview image embedded inside a Photoshop (PSD) document. This preview is stored as a resource and can be saved independently for cataloging or display purposes. The thumbnail is typically a low‑resolution representation used by applications to show a quick visual summary without loading the full‑size image.

## Waarom Aspose.PSD voor deze taak gebruiken?
Aspose.PSD ondersteunt **30+ beeldformaten** en kan PSD‑bestanden tot **500 MB** verwerken terwijl het geheugenverbruik laag blijft omdat het resources op aanvraag leest. De API biedt ook robuuste foutafhandeling, zodat je betrouwbaar thumbnails kunt extraheren, zelfs uit corrupte bestanden.

## Vereisten
Voordat we beginnen, zorg ervoor dat je het volgende hebt:
- Java Development Kit (JDK) geïnstalleerd.
- Aspose.PSD for Java‑bibliotheek gedownload van [Aspose.PSD for Java download](https://releases.aspose.com/psd/java/).
- Basiskennis van Java‑syntaxis en projectconfiguratie.

## Hoe extraheren we een thumbnail uit een PSD‑bestand in Java?
Laad het PSD‑bestand met `PsdImage`, zoek de `ThumbnailResource` en sla de afbeeldingsgegevens op als een JPEG. Aspose.PSD abstraheert de low‑level parsing, zodat je alleen `getResources()` hoeft aan te roepen en vervolgens `save()` op de geëxtraheerde afbeelding. Deze aanpak werkt voor elke PSD die een thumbnail bevat, ongeacht de bestandsgrootte.

## Pakketten importeren
`Image` is de basisklasse voor het laden van afbeeldingen. `PsdImage` vertegenwoordigt een PSD‑document. `ThumbnailResource` en `Thumbnail4Resource` vertegenwoordigen thumbnail‑resources. `JpegOptions` specificeert JPEG‑opslaanopties.

```text
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
```

## Stap 1: laad het PSD‑bestand
Eerst maak je een `PsdImage`‑instantie die naar je PSD‑bestand wijst. De constructor leest alleen de header en vereiste resources, waardoor het geheugenverbruik minimaal blijft.

```text
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
```

Vervang `"Your_Document_Directory/"` door het pad naar de map waar je PSD‑bestand zich bevindt, en `"your_file.psd"` door de naam van je PSD‑bestand.

## Stap 2: doorbeeldresources itereren
Aspose.PSD slaat thumbnails op als `ThumbnailResource`‑objecten binnen de resource‑collectie van de afbeelding. Loop door de collectie, controleer het resource‑type en vang de eerste thumbnail die je tegenkomt.

```text
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```
```

## Stap 3: sla de geëxtraheerde thumbnail op
Zodra je de thumbnail‑afbeelding hebt, roep je de `save`‑methode aan om deze naar schijf te schrijven. Je kunt kiezen voor JPEG, PNG of BMP; JPEG is het meest gebruikelijk voor web‑previews.

## Stap 4: omgaan met verschillende thumbnail‑typen
Als een PSD meerdere thumbnail‑varianten bevat, zoals `Thumbnail4Resource`, breid dan de iteratielogica uit om elk type te controleren. De API biedt afzonderlijke klassen voor elke resource, zodat je de gewenste resolutie kunt selecteren.

## Veelvoorkomende problemen en oplossingen
- **Geen thumbnail gevonden:** Niet alle PSD‑bestanden bevatten een preview. Controleer het bronbestand in het “File → File Info”‑paneel van Photoshop.
- **Niet‑ondersteunde formaatfout:** Zorg ervoor dat je de nieuwste versie van Aspose.PSD gebruikt; oudere releases kunnen nieuwere thumbnail‑resource‑typen missen.
- **Out‑of‑memory bij grote bestanden:** Gebruik `PsdImage.load(..., LoadOptions)` met `LoadOptions.setLoadResourcesOnly(true)` om te voorkomen dat de volledige afbeeldingsgegevens worden geladen wanneer je alleen de thumbnail nodig hebt.

## Veelgestelde vragen

**Q: Wat is Aspose.PSD?**  
A: Aspose.PSD is een Java‑bibliotheek die programmatische creatie, manipulatie en conversie van PSD en andere raster‑beeldformaten mogelijk maakt zonder Adobe Photoshop te vereisen.

**Q: Waar kan ik meer documentatie vinden over Aspose.PSD voor Java?**  
A: Je kunt de [documentatie](https://reference.aspose.com/psd/java/) raadplegen voor gedetailleerde API‑referenties en voorbeelden.

**Q: Kan ik Aspose.PSD gratis uitproberen voordat ik aankoop?**  
A: Ja, je kunt een [gratis proefversie](https://releases.aspose.com/) downloaden om de mogelijkheden van de bibliotheek te evalueren.

**Q: Hoe kan ik een tijdelijke licentie voor Aspose.PSD verkrijgen?**  
A: Tijdelijke licenties zijn beschikbaar op de [temporary license](https://purchase.aspose.com/temporary-license/) pagina.

**Q: Is Aspose.PSD geschikt voor commercieel gebruik?**  
A: Ja, Aspose.PSD kan zowel in persoonlijke als commerciële projecten worden gebruikt onder de licentievoorwaarden.

---

**Laatst bijgewerkt:** 2026-10-03  
**Getest met:** Aspose.PSD for Java 24.12  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Hoe PSD omzetten naar raster‑beeldformaten met Aspose.PSD voor Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [PSD opslaan als JPEG en RGB‑kleur ondersteunen met Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [Afbeelding schalen met Aspose.PSD voor Java – Vormen tekenen & basis‑afbeeldingsbewerkingen](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}