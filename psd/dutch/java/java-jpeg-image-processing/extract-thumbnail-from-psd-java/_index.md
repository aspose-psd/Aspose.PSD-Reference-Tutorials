---
title: Miniatuur uit PSD extraheren in Java
linktitle: Miniatuur uit PSD extraheren in Java
second_title: Aspose.PSD Java-API
description: Leer hoe u miniaturen uit PSD-bestanden kunt extraheren met Aspose.PSD voor Java. Deze stapsgewijze handleiding behandelt alles, van het instellen tot het opslaan van geëxtraheerde afbeeldingen.
weight: 15
url: /nl/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Miniatuur uit PSD extraheren in Java

## Invoering
In deze zelfstudie onderzoeken we hoe u miniaturen uit PSD-bestanden kunt extraheren met Aspose.PSD voor Java. Miniaturen kunnen handig zijn voor snelle voorbeelden of voor het maken van kleinere versies van afbeeldingen die zijn ingesloten in PSD-documenten. Laten we eens kijken naar de stappen die nodig zijn om dit te bereiken met behulp van Aspose.PSD.
## Vereisten
Voordat we beginnen, zorg ervoor dat u het volgende hebt ingesteld:
- Java Development Kit (JDK) op uw systeem geïnstalleerd.
-  Aspose.PSD voor Java-bibliotheek. Je kunt het downloaden van[hier](https://releases.aspose.com/psd/java/).
- Basiskennis van Java-programmeren.
## Pakketten importeren
Om aan de slag te gaan, neemt u het benodigde Aspose.PSD-pakket op in uw Java-klasse:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## Stap 1: Laad het PSD-bestand
Laad eerst het PSD-bestand dat de miniatuur bevat die u wilt extraheren.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
 Vervangen`"Your_Document_Directory/"` met het mappad waar uw PSD-bestand zich bevindt, en`"your_file.psd"` met de naam van uw PSD-bestand.
## Stap 2: Herhaal de afbeeldingsbronnen
Blader door de afbeeldingsbronnen om de miniatuurbron te vinden.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Miniatuurgegevens extraheren
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Maak een nieuwe afbeelding met de geëxtraheerde miniatuurgegevens
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Sla de uitgepakte miniatuur op als een afzonderlijk JPEG-bestand
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Succesbericht uitvoeren
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Verlaat de lus zodra de miniatuur is gevonden en verwerkt
    }
}
```
## Stap 3: Sla de uitgepakte miniatuur op
Sla de uitgepakte miniatuur op als een afzonderlijk afbeeldingsbestand (in dit geval als een JPEG-bestand).
## Stap 4: Omgaan met verschillende miniatuurtypen
 Als uw PSD-bestand meerdere soorten miniaturen kan bevatten, zoals`Thumbnail4Resource`, kunt u de logica uitbreiden om deze gevallen op dezelfde manier af te handelen.

## Conclusie
In deze zelfstudie hebben we onderzocht hoe u miniaturen uit PSD-bestanden kunt extraheren met Aspose.PSD voor Java. Door de hierboven beschreven stappen te volgen, kunt u op efficiënte wijze miniaturen ophalen en opslaan die zijn ingesloten in uw PSD-documenten.

## Veelgestelde vragen
### Wat is Aspose.PSD?
Aspose.PSD is een Java-bibliotheek waarmee ontwikkelaars programmatisch met PSD en andere afbeeldingsbestandsindelingen kunnen werken.
### Waar kan ik meer documentatie vinden over Aspose.PSD voor Java?
 U kunt verwijzen naar de[documentatie](https://reference.aspose.com/psd/java/) voor gedetailleerde API-referenties en voorbeelden.
### Kan ik Aspose.PSD gratis uitproberen voordat ik een aankoop doe?
 Ja, u kunt een downloaden[gratis proefperiode](https://releases.aspose.com/) om de mogelijkheden van de bibliotheek te evalueren.
### Hoe kan ik tijdelijke licenties krijgen voor Aspose.PSD?
 Tijdelijke licenties zijn verkrijgbaar bij[hier](https://purchase.aspose.com/temporary-license/).
### Is Aspose.PSD geschikt voor commercieel gebruik?
Ja, Aspose.PSD kan onder de licentievoorwaarden worden gebruikt voor zowel persoonlijke als commerciële projecten.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
