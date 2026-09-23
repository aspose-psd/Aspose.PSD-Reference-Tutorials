---
date: 2026-09-23
description: Leer hoe u PSD-vectorvormen kunt wijzigen en PSD-bestanden batch-verwerkt
  met Aspose.PSD voor Java. Gedetailleerde stappen, tips en code placeholders voor
  een volledige oplossing.
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: Ondersteuning Length Record Data Properties in PSD - Java
og_description: Leer hoe u PSD-vectorvormen kunt wijzigen en PSD-bestanden batch-verwerkt
  met Aspose.PSD voor Java. Stapsgewijze gids met code placeholders en deskundige
  tips.
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: PSD-vectorvormen wijzigen met Aspose.PSD voor Java
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: PSD-vectorvormen wijzigen met Aspose.PSD voor Java
url: /nl/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD-vectorvormen wijzigen met Aspose.PSD voor Java

## Introductie
Als je programmatically **PSD‑vectorvormen wilt wijzigen**, biedt Aspose.PSD voor Java volledige controle over Photoshop‑bestanden rechtstreeks vanuit je Java‑code. Deze tutorial leidt je door het ondersteunen van length‑record‑eigenschappen — een essentiële stap bij het bewerken van vector‑vormlagen. Aan het einde kun je een PSD openen, de vectorvormgegevens aanpassen en het bijgewerkte bestand opslaan zonder Photoshop te starten.

## Snelle antwoorden
- **Wat betekent “modify PSD vector shapes”?** Het aanpassen van geometrie, padbewerkingen of andere attributen van vector‑gebaseerde lagen binnen een PSD‑bestand.  
- **Welke bibliotheek behandelt dit?** Aspose.PSD voor Java.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor evaluatie; een commerciële licentie is vereist voor productie.  
- **Hoe lang duurt de implementatie?** Ongeveer 10‑15 minuten voor een basis script voor vorm‑aanpassing.  
- **Wat zijn de belangrijkste vereisten?** Java JDK, Aspose.PSD voor Java, en een voorbeeld‑PSD‑bestand.

## Wat is “support length record properties”?
Het ondersteunen van length‑record‑eigenschappen betekent dat je de `LengthRecord`‑objecten benadert en bijwerkt die elk vectorpad binnen een PSD beschrijven. Deze records slaan informatie op zoals de lengte van het pad, het type en hoe het zich verbindt met andere paden. Door ze te wijzigen kun je bepalen hoe vormen combineren, kruisen of van elkaar worden afgetrokken, waardoor nauwkeurige vectorbewerkingen mogelijk zijn.

## Waarom Aspose.PSD voor Java gebruiken om length record properties te ondersteunen?
Laad je PSD, bewerk vector‑data en sla op — allemaal zonder Photoshop. Aspose.PSD verwerkt PSD‑bestanden met honderden pagina’s in minder dan 2 seconden op een typische server, biedt meer dan 150 klassen (inclusief meer dan 30 vector‑gerelateerde typen) en draait op Windows, Linux of macOS met elke JDK 11+. Deze op prestaties gerichte bibliotheek elimineert de noodzaak voor dure desktopsoftware.

## Vereisten
1. **Java Development Kit (JDK)** – download van [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) of gebruik je favoriete pakketbeheerder.  
2. **Aspose.PSD voor Java** – verkrijg de nieuwste JAR van de [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, of een andere Java‑compatibele editor.  
4. **Een PSD‑bestand** – maak er één in Photoshop of pak een voorbeeld‑PSD om mee te experimenteren.  
5. **Basiskennis van Java** – vertrouwdheid met klassen, objecten en exception‑handling.

## Pakketten importeren
De import‑verklaringen brengen de kern‑Aspose.PSD‑klassen in scope, zoals `PsdImage`, `VsmsResource` en `LengthRecord`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Stap 1: Stel je bron‑ en uitvoermappen in
Definieer waar de originele PSD zich bevindt en waar het gewijzigde bestand wordt weggeschreven.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Stap 2: Laad het PSD‑bestand
Gebruik `Image.load` om het bestand te openen en cast het naar `PsdImage` voor PSD‑specifieke functionaliteit.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Stap 3: Zoek de Vsms‑resource in de laag
`VsmsResource` is de container die vectorvormgegevens voor een laag opslaat. Loop door de resources van de tweede laag om deze te vinden.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Stap 4: Toegang tot length‑records
`LengthRecord` vertegenwoordigt een afzonderlijk vectorpad. Haal de records op die je wilt wijzigen.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Stap 5: Pad‑operatie‑eigenschappen wijzigen
`PathOperations` definieert hoe individuele vormen interageren (bijv. uitsluiting, intersectie, aftrekking). Het wijzigen van deze waarden werkt de visuele compositie van de vectorlaag bij.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Stap 6: Sla het gewijzigde PSD‑bestand op
Sla je wijzigingen op in een nieuw bestand.

```java
psdImage.save(outPsdFilePath);
```

## Stap 7: Ruim resources op
Verwijder de `PsdImage`‑instantie om geheugen vrij te maken en resource‑lekken te voorkomen.

```java
psdImage.dispose();
```

## Hoe PSD‑bestanden batch‑verwerken met support length record properties
Plaats de workflow voor één bestand in een lus die over een map met PSD‑bestanden itereren, waarbij `inPsdFilePath` en `outPsdFilePath` voor elk bestand worden bijgewerkt. Deze aanpak stelt je in staat identieke vector‑vormaanpassingen toe te passen op tientallen bestanden binnen enkele minuten, ideaal voor geautomatiseerde asset‑pijplijnen.

## Veelvoorkomende valkuilen & tips
- **Null‑controles** – controleer altijd dat `resource` niet `null` is voordat je de leden benadert.  
- **Pad‑indexgrenzen** – zorg ervoor dat de indices die je gebruikt (bijv. `[2]`, `[7]`, `[11]`) bestaan voor de specifieke PSD die je bewerkt.  
- **Licentie** – uitvoeren zonder een geldige licentie voegt een watermerk toe aan de opgeslagen PSD.  

## Conclusie
Je hebt nu een volledig, end‑to‑end voorbeeld van hoe je **PSD‑vectorvormen wijzigen** door length‑record‑eigenschappen te ondersteunen met Aspose.PSD voor Java. Of je nu een asset‑pipeline automatiseert of een aangepast ontwerpgereedschap bouwt, deze API’s bieden je de flexibiliteit om vectorlagen te manipuleren zonder handmatig Photoshop‑werk. Experimenteer met andere `PathOperations`‑waarden of combineer meerdere `LengthRecord`‑bewerkingen om complexe vormen te creëren.

## Veelgestelde vragen

**Q: Hoe ga ik om met een PSD die geen vectorvormlagen bevat?**  
A: De `VsmsResource` zal afwezig zijn, dus `resource` blijft `null`. Voeg een controle toe en sla de wijzigingsstap over of informeer de gebruiker.

**Q: Kan ik andere eigenschappen wijzigen, zoals vulkleur of lijndikte?**  
A: Ja, `LengthRecord` biedt setters voor vul, lijn en doorzichtigheid. Zie de API‑documentatie voor de volledige lijst.

**Q: Is het mogelijk om meerdere PSD‑bestanden batch‑te verwerken?**  
A: Absoluut. Plaats de code in een lus die over een map met PSD‑bestanden itereren, waarbij de invoer‑ en uitvoer‑paden elke keer worden aangepast.

**Q: Moet ik streams handmatig sluiten bij het laden vanaf een bestands‑pad?**  
A: `Image.load` behandelt bestands‑streams automatisch, maar als je laadt vanaf een `InputStream`, vergeet dan niet deze na gebruik te sluiten.

**Q: Welke versie van Aspose.PSD is vereist voor deze API’s?**  
A: De `LengthRecord`‑ en `PathOperations`‑klassen zijn beschikbaar sinds Aspose.PSD 20.10. Het gebruik van de nieuwste versie (24.11 op het moment van schrijven) wordt aanbevolen.

---

**Laatst bijgewerkt:** 2026-09-23  
**Getest met:** Aspose.PSD for Java 24.11  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Converteer PSD naar PNG en maak Vector Mask Java – Vmsk Resource in PSD‑bestanden](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [Converteer PSD naar PNG met laagmaskerondersteuning met Aspose.PSD voor Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Laagondersteuning toevoegen aan PSD‑bestanden](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}