---
title: Maak miniaturen van PSD-bestanden met behulp van Java
linktitle: Maak miniaturen van PSD-bestanden met behulp van Java
second_title: Aspose.PSD Java-API
description: Leer hoe u moeiteloos miniaturen kunt maken van PSD-bestanden met behulp van Java en Aspose.PSD. Volg onze stapsgewijze handleiding voor een naadloze beeldverwerking.
type: docs
weight: 24
url: /nl/java/modifying-converting-psd-images/create-thumbnails-psd-files/
---
## Invoering
In de wereld van grafisch ontwerp is het werken met PSD-bestanden (Photoshop Document) gemeengoed. Of u nu een doorgewinterde ontwikkelaar, grafisch ontwerper of gewoon iemand bent die zich wil verdiepen in beeldverwerking: het maken van miniaturen van PSD-bestanden kan u tijd besparen en uw workflow stroomlijnen. Deze tutorial begeleidt u door het hele proces met Aspose.PSD voor Java. Aspose.PSD is niet alleen een robuuste bibliotheek voor het beheren van Photoshop-bestanden, maar maakt de taak ook intuïtief en beheersbaar. Bent u klaar om te leren hoe u efficiënt miniaturen van PSD-bestanden kunt maken?
## Vereisten
Voordat we ingaan op de kern van het maken van thumbnails, laten we eerst bespreken wat je nodig hebt om aan de slag te gaan.
### Java-ontwikkelomgeving
-  Java JDK: Zorg ervoor dat de Java Development Kit (JDK) op uw computer is geïnstalleerd. Je kunt het downloaden[hier](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- IDE: Een Integrated Development Environment (IDE) zoals IntelliJ IDEA, Eclipse of NetBeans zal het coderen eenvoudiger maken.
### Aspose.PSD-bibliotheek
-  moet de Aspose.PSD-bibliotheek in uw project opnemen. Dat kan[download hier de nieuwste versie](https://releases.aspose.com/psd/java/).
### Basiskennis van Java
- Als u bekend bent met de basisbeginselen van Java, kunt u effectiever door de voorbeeldcode navigeren. Concepten als klassen, objecten en lussen zullen veelvuldig worden gebruikt.
## Pakketten importeren
Begin met het importeren van de benodigde klassen uit de Aspose.PSD-bibliotheek. Deze stap is cruciaal omdat u hiermee de functionaliteiten van de bibliotheek in uw code kunt benutten.
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
Nu de vereisten uit de weg zijn, gaan we naar het hoofdevenement! Het maken van miniaturen van PSD-bestanden omvat een paar eenvoudige stappen, en ik zal het voor u opsplitsen.
## Stap 1: Stel uw omgeving in
Hier leest u hoe u uw project kunt starten en hoe u zich kunt voorbereiden op het genereren van miniaturen.
1. Maak een Java-project:
   - Open uw IDE en maak een nieuw Java-project.
   - Noem het zoiets als "PsdThumbnailGenerator".
2. Inclusief Aspose.PSD-bibliotheek:
   -  Voeg het Aspose.PSD JAR-bestand toe aan het buildpad van uw project. Als u Maven gebruikt, neem dit dan op in uw`pom.xml`:
     ```xml
     <dependency>
         <groupId>com.aspose</groupId>
         <artifactId>aspose-psd</artifactId>
         <version>your_version_here</version>
     </dependency>
     ```
## Stap 2: Laad het PSD-bestand
Vervolgens moeten we het PSD-bestand laden waarvan we miniaturen willen maken. 
1. Geef uw documentmap op:
   Definieer de map waar uw PSD-bestand zich bevindt.
   ```java
   String dataDir = "Your Document Directory"; // Vervang door jouw pad
   ```
2. Laad het PSD-bestand:
    Gebruik de`PsdImage` class om uw PSD-bestand te laden.
   ```java
   PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
   ```
 Hier,`sample.psd` is de naam van uw PSD-bestand. Pas dit aan op basis van de naam van uw bestand.
## Stap 3: Herhaal de PSD-bronnen
Nu we onze PSD-afbeelding hebben geladen, is de volgende stap het onderzoeken van de bronnen ervan.
1. Krijg bronnentelling:
   We doorlopen alle bronnen in het PSD-bestand.
   ```java
   for (int i = 0; i < image.getImageResources().length; i++) {
       // Verwerking van hulpbronnen
   }
   ```
   
2. Identificeer miniatuurbronnen:
   Controleer binnen de lus of een bron een miniatuur is.
   ```java
   if (image.getImageResources()[i] instanceof ThumbnailResource) {
       // Verwerk de miniatuur
   }
   ```
## Stap 4: Verwerk de miniatuur
Zodra we een miniatuurbron hebben geïdentificeerd, moeten we deze dienovereenkomstig behandelen.
1. Miniatuurformaat ophalen en controleren:
   Als de bron inderdaad een miniatuur is, haal deze dan op en controleer het formaat ervan.
   ```java
   ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
   if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
       // Maak de miniatuur en sla deze op
   }
   ```
## Stap 5: Maak de miniatuur en sla deze op
Dit is waar de magie gebeurt! We zullen een nieuwe afbeelding maken van de miniatuurgegevens en deze opslaan.
1. Maak een nieuwe afbeelding:
   We gebruiken de breedte en hoogte van de miniatuurbron om een nieuwe bitmapafbeelding te maken.
   ```java
   PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
   ```
2. Pixels opslaan in de nieuwe afbeelding:
   Breng de miniatuurgegevens over naar de nieuw gemaakte afbeelding.
   ```java
   thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
   ```
3. Bewaar de miniatuurafbeelding:
   Sla ten slotte de miniatuurafbeelding op in uw documentmap met een unieke naam.
   ```java
   thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
   ```

## Conclusie
Het maken van miniaturen van PSD-bestanden met behulp van Java en Aspose.PSD kan een eenvoudige taak zijn als u het eenmaal in beheersbare stappen opsplitst. Met deze tutorial beschikt u nu over de mogelijkheid om eenvoudig miniaturen uit uw PSD-bestanden te extraheren, waardoor u een handig hulpmiddel krijgt om uw workflow te verbeteren. Dus wat houdt je tegen? Zorg dat je een aantal PSD-bestanden in handen krijgt en probeer het eens!
## Veelgestelde vragen
### Wat is Aspose.PSD?
Aspose.PSD is een Java-bibliotheek waarmee ontwikkelaars met Photoshop-bestanden kunnen werken, waardoor het eenvoudiger wordt om PSD-bestanden programmatisch te manipuleren en beheren.
### Kan ik Aspose.PSD gratis gebruiken?
Ja, Aspose biedt een gratis proefperiode aan die u kunt gebruiken om de bibliotheek te testen voordat u een licentie aanschaft.
### In welke formaten kan ik de thumbnails opslaan?
In dit voorbeeld hebben we de thumbnails in BMP-formaat opgeslagen, maar Aspose.PSD ondersteunt ook diverse andere formaten.
### Moet ik Photoshop installeren om Aspose.PSD te kunnen gebruiken?
Nee, Aspose.PSD werkt onafhankelijk van Photoshop.
### Waar kan ik meer informatie vinden over Aspose.PSD?
 Je kunt de[Aspose.PSD-documentatie](https://reference.aspose.com/psd/java/) voor meer details, tutorials en bronnen.