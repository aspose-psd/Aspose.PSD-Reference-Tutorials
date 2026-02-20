---
date: 2026-02-20
description: Leer hoe u lengte‑recordeigenschappen ondersteunt en PSD‑bestanden batch
  verwerkt met Aspose.PSD voor Java. Stapsgewijze handleiding met codevoorbeelden.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Ondersteun lengte‑recordeigenschappen – Wijzig PSD‑vectorvormen (Java)
url: /nl/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ondersteun Length Record‑eigenschappen – Bewerk PSD‑vectorvormen (Java)

## Inleiding
Als je **PSD‑vectorvormen** programmatisch wilt **wijzigen**, geeft de Aspose.PSD for Java‑bibliotheek je volledige controle over Photoshop‑bestanden direct vanuit je Java‑code. In deze tutorial lopen we alles door wat je moet weten om **length record‑eigenschappen te ondersteunen**—een essentiële stap wanneer je vector‑vormlagen wilt bewerken. Aan het einde kun je een PSD openen, de vector‑vormeigenschappen aanpassen en het bijgewerkte bestand opslaan zonder je IDE te verlaten. Laten we beginnen!

## Snelle antwoorden
- **Wat betekent “modify PSD vector shapes”?** Het aanpassen van de geometrie, padbewerkingen of andere eigenschappen van vector‑gebaseerde lagen binnen een PSD‑bestand.  
- **Welke bibliotheek behandelt dit?** Aspose.PSD for Java.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor evaluatie; een commerciële licentie is vereist voor productie.  
- **Hoe lang duurt de implementatie?** Ongeveer 10‑15 minuten voor een basis script voor vormaanpassing.  
- **Wat zijn de belangrijkste vereisten?** Java JDK, Aspose.PSD for Java, en een voorbeeld‑PSD‑bestand.

## Wat is “support length record properties”?
Het ondersteunen van length record‑eigenschappen betekent dat je de `LengthRecord`‑objecten benadert en bijwerkt die elk vectorpad binnen een PSD beschrijven. Het wijzigen van deze records stelt je in staat te bepalen hoe vormen combineren, snijden of van elkaar worden afgetrokken.

## Waarom Aspose.PSD for Java gebruiken om length record‑eigenschappen te ondersteunen?
- **Geen Photoshop vereist** – werk direct met PSD‑bestanden op elke server.  
- **Rijke API** – krijg toegang tot lagen, bronnen en vectordata met sterk getypeerde klassen.  
- **Cross‑platform** – draait op Windows, Linux of macOS met elke JDK.  
- **Prestatiegericht** – efficiënt geheugenbeheer en snelle opslaan‑bewerkingen.  

## Vereisten
1. **Java Development Kit (JDK)** – download van [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) of gebruik je favoriete pakketbeheerder.  
2. **Aspose.PSD for Java** – verkrijg de nieuwste JAR van de [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, of een andere Java‑compatibele editor.  
4. **Een PSD‑bestand** – maak er één in Photoshop of pak een voorbeeld‑PSD om mee te experimenteren.  
5. **Basiskennis van Java** – vertrouwdheid met klassen, objecten en exception‑handling.

## Importeer pakketten
Importeer eerst de klassen die je nodig hebt om met PSD‑bestanden en vectorvorm‑bronnen te werken.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Stap 1: Stel je bron- en uitvoermappen in
Definieer waar de originele PSD zich bevindt en waar je het gewijzigde bestand wilt opslaan.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Stap 2: Laad het PSD‑bestand
Gebruik `Image.load` om het bestand te openen en cast het naar `PsdImage` voor PSD‑specifieke functies.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Stap 3: Zoek de Vsms‑resource in de laag
Vectorvormgegevens bevinden zich in een `VsmsResource`. Loop door de resources van de tweede laag om deze te vinden.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Stap 4: Toegang tot Length‑records
Elke `LengthRecord` vertegenwoordigt een afzonderlijk vectorpad. Pak de records die je wilt wijzigen.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Stap 5: Wijzig padbewerkings‑eigenschappen
Nu kun je **PSD‑vectorvormen** wijzigen door hun `PathOperations` aan te passen. Dit bepaalt hoe vormen interageren (bijv. uitsluiting, intersectie, aftrekking).

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

## Stap 7: Ruim bronnen op
Dispose van de `PsdImage` om geheugen vrij te maken.

```java
psdImage.dispose();
```

## Hoe PSD‑bestanden batch‑verwerken met support length record‑eigenschappen
Als je dezelfde vector‑vormaanpassingen op veel PSD‑bestanden wilt toepassen, wikkel je de bovenstaande code in een lus die over een map met bestanden iterereert. Werk `inPsdFilePath` en `outPsdFilePath` bij voor elke iteratie, en je kunt **PSD‑bestanden batch‑verwerken** efficiënt.

## Veelvoorkomende valkuilen & tips
- **Null‑controles** – controleer altijd dat `resource` niet `null` is voordat je paden benadert.  
- **Pad‑indexgrenzen** – zorg ervoor dat de indices die je gebruikt (`[2]`, `[7]`, `[11]`) bestaan voor de specifieke PSD die je bewerkt.  
- **Licentie** – uitvoeren zonder een geldige licentie zal een watermerk in de opgeslagen PSD plaatsen.  

## Conclusie
Je hebt nu een compleet, end‑to‑end voorbeeld van hoe je **PSD‑vectorvormen** kunt **wijzigen** door length record‑eigenschappen te ondersteunen met Aspose.PSD for Java. Of je nu asset‑pijplijnen automatiseert of een aangepaste ontwerptool bouwt, deze API’s geven je de flexibiliteit om vectorlagen te manipuleren zonder handmatig Photoshop‑werk. Verken verder door te experimenteren met andere `PathOperations` of door meerdere `LengthRecord`‑bewerkingen te combineren voor complexe vormen.

## Veelgestelde vragen

**Q: Hoe ga ik om met een PSD die geen vectorvormlagen bevat?**  
A: De `VsmsResource` zal afwezig zijn, dus `resource` blijft `null`. Voeg een controle toe en sla de wijzigingsstap over of informeer de gebruiker.

**Q: Kan ik andere eigenschappen wijzigen, zoals vulkleur of lijndikte?**  
A: Ja, `LengthRecord` biedt extra setters voor vul, lijn en doorzichtigheid. Raadpleeg de API‑documentatie voor volledige details.

**Q: Is het mogelijk om meerdere PSD‑bestanden batch‑te verwerken?**  
A: Absoluut. Wikkel de code in een lus die over een map met PSD‑bestanden iterereert, waarbij je de invoer‑ en uitvoer‑paden telkens aanpast.

**Q: Moet ik streams handmatig sluiten bij het laden vanaf een bestandspad?**  
A: De `Image.load`‑methode behandelt bestands‑streams intern, maar als je laadt vanaf een `InputStream`, vergeet dan niet deze na gebruik te sluiten.

**Q: Welke versie van Aspose.PSD is vereist voor deze API’s?**  
A: De `LengthRecord`‑ en `PathOperations`‑klassen zijn beschikbaar sinds Aspose.PSD 20.10. Het gebruik van de nieuwste versie wordt aanbevolen.

---

**Last Updated:** 2026-02-20  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}