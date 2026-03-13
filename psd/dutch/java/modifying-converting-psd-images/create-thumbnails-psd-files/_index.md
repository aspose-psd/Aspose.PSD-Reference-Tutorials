---
date: 2026-03-13
description: Leer hoe je PSD-miniaturen maakt in Java met Aspose.PSD. Volg onze stapsgewijze
  handleiding om snel miniaturen van PSD‑bestanden te genereren.
linktitle: Create Thumbnails from PSD Files using Java
second_title: Aspose.PSD Java API
title: PSD-thumbnail maken in Java – Genereer thumbnails van PSD
url: /nl/java/modifying-converting-psd-images/create-thumbnails-psd-files/
weight: 24
---

 and URLs unchanged.

Now produce final content with same markdown.

Let's craft final output.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Maak PSD Thumbnail Java – Genereer Thumbnails van PSD

## Introductie
Als je **create PSD thumbnail Java** code nodig hebt die voorbeeldafbeeldingen uit Photoshop‑bestanden haalt, ben je hier aan het juiste adres. Of je nu een digitale asset‑manager, een webgalerij of een geautomatiseerde batch‑verwerkingspipeline bouwt, het genereren van thumbnails uit PSD‑bestanden kan de prestaties en gebruikerservaring drastisch verbeteren. In deze tutorial lopen we het volledige proces door met Aspose.PSD for Java, en laten we zien hoe je een PSD laadt, de ingebedde thumbnail‑resources vindt en ze opslaat als afzonderlijke afbeeldingsbestanden.

## Snelle antwoorden
- **Welke bibliotheek is het beste voor PSD‑thumbnail‑extractie?** Aspose.PSD for Java.  
- **Hoe lang duurt de implementatie?** Ongeveer 10‑15 minuten voor een basisopzet.  
- **Heb ik Photoshop geïnstalleerd nodig?** Nee, Aspose.PSD werkt onafhankelijk.  
- **Naar welke afbeeldingsformaten kan ik de thumbnail exporteren?** Elk formaat dat door Aspose.PSD wordt ondersteund (bijv. BMP, PNG, JPEG).  
- **Is een licentie vereist voor productie?** Ja, een commerciële licentie is nodig voor gebruik in productie.

## Wat is “create PSD thumbnail Java”?
Een PSD‑thumbnail maken in Java betekent dat je programmatisch de thumbnail‑preview die in een Photoshop‑document (PSD) is opgeslagen, uitleest en opslaat als een afzonderlijk afbeeldingsbestand. Dit is handig om snelle previews te genereren zonder de volledige, vaak grote, PSD‑inhoud te laden.

## Waarom Aspose.PSD voor deze taak gebruiken?
- **Geen Photoshop‑afhankelijkheid:** Werkt op elk platform met een JDK.  
- **Volledige PSD‑ondersteuning:** Behandelt alle PSD‑versies en resources, inclusief thumbnails.  
- **Eenvoudige API:** Enkele regels code om thumbnails te extraheren en op te slaan.  
- **Prestaties‑geoptimaliseerd:** Efficiënt geheugengebruik voor grote bestanden.

## Vereisten
Voordat we ingaan op de details van het maken van thumbnails, behandelen we wat je nodig hebt om aan de slag te gaan.

### Java-ontwikkelomgeving
- **Java JDK:** Zorg ervoor dat je de Java Development Kit (JDK) op je computer hebt geïnstalleerd. Je kunt het [hier](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) downloaden.  
- **IDE:** Een Integrated Development Environment (IDE) zoals IntelliJ IDEA, Eclipse of NetBeans maakt coderen makkelijker.

### Aspose.PSD Library
- Je moet de Aspose.PSD‑bibliotheek in je project opnemen. Je kunt de nieuwste versie [hier](https://releases.aspose.com/psd/java/) downloaden.

### Basiskennis van Java
- Vertrouwdheid met de basis van Java helpt je om de voorbeeldcode effectiever te volgen. Concepten zoals klassen, objecten en lussen komen vaak terug.

## Import pakketten
Begin met het importeren van de benodigde klassen uit de Aspose.PSD‑bibliotheek. Deze stap is cruciaal omdat het je in staat stelt de functionaliteit van de bibliotheek in je code te gebruiken.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

Met de vereisten uit de weg, gaan we nu naar het hoofdonderdeel! Het maken van thumbnails uit PSD‑bestanden omvat een paar eenvoudige stappen, en ik zal ze voor je uitsplitsen.

## Hoe maak je PSD thumbnail Java – Stapsgewijze handleiding

### Stap 1: Stel je omgeving in
Hier lees je hoe je je project start en voorbereidt op thumbnail‑generatie.

1. **Maak een Java‑project**  
   - Open je IDE en maak een nieuw Java‑project.  
   - Geef het een naam zoals `"PsdThumbnailGenerator"`.

2. **Voeg de Aspose.PSD‑bibliotheek toe**  
   - Voeg het Aspose.PSD JAR‑bestand toe aan het build‑pad van je project.  
   - Als je Maven gebruikt, voeg het toe in je `pom.xml`:

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-psd</artifactId>
    <version>your_version_here</version>
</dependency>
```

### Stap 2: Laad het PSD‑bestand
Vervolgens moeten we het PSD‑bestand laden waaruit we thumbnails willen maken.

1. **Specificeer je documentmap**  
   Definieer de map waarin je PSD‑bestand zich bevindt.

```java
String dataDir = "Your Document Directory"; // Replace with your path
```

2. **Laad het PSD‑bestand**  
   Gebruik de `PsdImage`‑klasse om je PSD‑bestand te laden.

```java
PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
```

> **Pro tip:** Bewaar je PSD‑bestanden in een speciale map (bijv. `src/main/resources`) om padproblemen te voorkomen.

### Stap 3: Doorloop PSD‑resources
Nu we onze PSD‑afbeelding hebben geladen, is de volgende stap om de resources te onderzoeken.

1. **Haal het aantal resources op**  
   We lopen door alle resources in het PSD‑bestand.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Processing resources
}
```

2. **Identificeer thumbnail‑resources**  
   Controleer binnen de lus of een resource een thumbnail is.

```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    // Process the thumbnail
}
```

### Stap 4: Verwerk de thumbnail
Zodra we een thumbnail‑resource hebben geïdentificeerd, moeten we deze verwerken.

1. **Haal het thumbnail‑formaat op en controleer**  
   Als de resource inderdaad een thumbnail is, haal deze dan op en controleer het formaat.

```java
ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
    // Create and save the thumbnail
}
```

### Stap 5: Maak en sla de thumbnail op
Dit is waar de magie gebeurt! We maken een nieuwe afbeelding van de thumbnail‑data en slaan deze op.

1. **Maak een nieuwe afbeelding**  
   We gebruiken de breedte en hoogte van de thumbnail‑resource om een nieuw bitmap‑beeld te maken.

```java
PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
```

2. **Sla pixels op in de nieuwe afbeelding**  
   Breng de thumbnail‑data over naar de nieuw gemaakte afbeelding.

```java
thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
```

3. **Sla de thumbnail‑afbeelding op**  
   Sla ten slotte de thumbnail‑afbeelding op in je documentmap met een unieke naam.

```java
thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
```

> **Veelvoorkomend valkuil:** Het vergeten te sluiten van de `PsdImage`‑objecten kan leiden tot geheugenlekken. Plaats de afbeeldingscode in een try‑with‑resources‑blok als je Java 7+ gebruikt.

## Conclusie
Door deze stappen te volgen, heb je nu een solide, herbruikbare manier om **create PSD thumbnail Java** implementaties te maken die preview‑afbeeldingen uit elk Photoshop‑bestand extraheren. Deze techniek kan worden geïntegreerd in batch‑processors, webservices of desktop‑hulpmiddelen om de afbeeldingcatalogus te versnellen en de UI‑responsiviteit te verbeteren. Probeer het met je eigen PSD‑collectie en zie hoe snel je lichtgewicht previews kunt genereren!

## Veelgestelde vragen
### Wat is Aspose.PSD?
Aspose.PSD is een Java‑bibliotheek die ontwikkelaars in staat stelt met Photoshop‑bestanden te werken, waardoor het eenvoudiger wordt om PSD‑bestanden programmatisch te manipuleren en beheren.

### Kan ik Aspose.PSD gratis gebruiken?
Ja, Aspose biedt een gratis proefversie die je kunt gebruiken om de bibliotheek te testen voordat je een licentie aanschaft.

### In welke formaten kan ik de thumbnails opslaan?
In dit voorbeeld hebben we de thumbnails opgeslagen in BMP‑formaat, maar Aspose.PSD ondersteunt ook diverse andere formaten.

### Heb ik Photoshop geïnstalleerd nodig om Aspose.PSD te gebruiken?
Nee, Aspose.PSD werkt onafhankelijk van Photoshop.

### Waar vind ik meer informatie over Aspose.PSD?
Je kunt de [Aspose.PSD documentatie](https://reference.aspose.com/psd/java/) raadplegen voor meer details, tutorials en bronnen.

## Frequently Asked Questions

**V: Hoe haal ik thumbnails uit een met wachtwoord beveiligde PSD?**  
A: Laad de PSD met de juiste overload van `Image.load` die een wachtwoordparameter accepteert.

**V: Kan ik thumbnails genereren in PNG in plaats van BMP?**  
A: Absoluut. Verander de bestandsextensie in de `save`‑methode en Aspose.PSD regelt de conversie.

**V: Is er een manier om meerdere PSD‑bestanden batch‑gewijs te verwerken?**  
A: Plaats de code in een lus die over een map met PSD‑bestanden iterereert, en hergebruik dezelfde extractielogica voor elk bestand.

**V: Welke Java‑versie is vereist?**  
A: Aspose.PSD ondersteunt Java 8 en later. Het gebruik van de nieuwste JDK wordt aanbevolen voor prestaties en beveiliging.

**V: Handelt de bibliotheek grote PSD‑bestanden efficiënt?**  
A: Ja, Aspose.PSD maakt gebruik van lazy loading en geoptimaliseerd geheugengebruik om met grote bestanden te werken zonder de heap‑ruimte uit te putten.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Laatst bijgewerkt:** 2026-03-13  
**Getest met:** Aspose.PSD 24.11 for Java (latest at time of writing)  
**Auteur:** Aspose  

---