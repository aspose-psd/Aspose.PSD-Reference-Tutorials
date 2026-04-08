---
date: 2026-04-08
description: Leer hoe je een PSD naar PNG exporteert en een nieuwe PSD‑laag maakt
  met Aspose.PSD voor Java met behulp van een tijdelijke Aspose‑licentie. Deze stapsgewijze
  tutorial behandelt PSD‑beeldbewerking en het instellen van de laagpositie.
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: Voeg een nieuwe reguliere laag toe aan PSD
second_title: Aspose.PSD Java API
title: Exporteer PSD naar PNG & Voeg een Nieuwe Reguliere Laag toe met Aspose.PSD
  voor Java – aspose tijdelijke licentie
url: /nl/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export PSD naar PNG & Voeg een Nieuwe Reguliere Laag toe met Aspose.PSD voor Java

## Inleiding

In deze **aspose psd tutorial** ontdek je hoe je **PSD naar PNG kunt exporteren** terwijl je ook **een nieuwe reguliere laag** maakt in hetzelfde bestand, **met een aspose tijdelijke licentie** voor ontwikkeling. Of je nu web‑klaar thumbnails moet genereren, assets moet voorbereiden voor een design‑pipeline, of simpelweg wilt experimenteren met **psd image manipulation**, Aspose.PSD voor Java geeft je volledige programmeerbare controle. We lopen elke stap door — van het laden van het bronbestand tot het opslaan van zowel de bijgewerkte PSD als een PNG‑kopie — zodat je direct PSD‑lagen kunt manipuleren.

## Snelle Antwoorden
- **Kan ik PSD naar PNG exporteren met één aanroep?** Ja, na het toevoegen van lagen kun je `save` aanroepen met `PngOptions`.
- **Heb ik een licentie nodig voor ontwikkeling?** Een tijdelijke licentie werkt voor testen; een volledige licentie is vereist voor productie.
- **Welke Java‑versie wordt ondersteund?** Aspose.PSD werkt met Java 8 en nieuwer.
- **Is laagpositionering pixel‑gebaseerd?** Ja, je stelt de linker-, boven-, rechter- en onder‑coördinaten in pixels in met de **set layer position**‑methoden.
- **Behoudt de PNG de laagtransparantie?** De PNG bevat het samengevoegde resultaat van alle zichtbare lagen.

## Waarom een aspose tijdelijke licentie gebruiken?

Een **aspose temporary license** stelt je in staat om de volledige functionaliteit van Aspose.PSD te evalueren zonder enige functionele beperkingen. Het verwijdert het evaluatiewatermerk, ontgrendelt alle API's — inclusief de mogelijkheid om **create new psd layer**‑objecten te maken — en laat je je code testen in een productie‑achtige omgeving voordat je een permanente licentie aanschaft.

## Vereisten

- **Java Development Environment** – JDK 8+ en een build‑tool (Maven/Gradle) geïnstalleerd.
- **Aspose.PSD for Java** – Download de nieuwste JAR van de officiële site [here](https://releases.aspose.com/psd/java/).
- **A sample PSD file** – We gebruiken `OneLayer.psd` in de voorbeelden.

## Importeer Pakketten

Voeg de benodigde imports toe aan je Java‑klasse. Deze klassen bieden de kernfunctionaliteit voor **psd image manipulation** en laag‑beheer.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Wat is “set layer position” en waarom is het belangrijk?

Wanneer je een nieuwe laag toevoegt, moet je definiëren waar deze op het canvas verschijnt. De methoden `setLeft`, `setTop`, `setRight` en `setBottom` **set layer position** in pixelcoördinaten. Een correcte positionering zorgt ervoor dat je grafische elementen precies op de verwachte plek staan, wat cruciaal is voor taken zoals het samenvoegen van UI‑assets of het voorbereiden van print‑klare bestanden.

## Stapsgewijze handleiding

### Stap 1: Laad het PSD‑bestand

Eerst laad je de bestaande PSD die je wilt aanpassen. Dit levert een `PsdImage`‑object op waarmee je kunt werken.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Stap 2: Bereid Pixelgegevens en Rechthoeken voor

We zullen twee pixelbuffers (`int[]`) maken en de rechthoekige gebieden definiëren waar de nieuwe lagen worden geschilderd. Dit vormt de basis voor **creating a new psd layer**.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Stap 3: Initialiseert Laaggegevens

Vul de pixelbuffers met een standaard ARGB‑waarde. De waarde `-10000000` komt overeen met een half‑transparante donkere tint.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Stap 4: Voeg Reguliere Lagen toe (Manipuleer PSD‑lagen)

Nu **add regular layers** we aan de PSD‑afbeelding en **set layer position** met de linker-, boven-, rechter‑ en onder‑eigenschappen. Dit toont hoe je **manipulate PSD layers** programmatisch kunt uitvoeren.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### Stap 5: Exporteer PSD naar PNG en Sla de Bijgewerkte PSD op

Nadat de lagen op hun plaats staan, sla je het gewijzigde document op. Eerst exporteren we het resultaat naar PNG (de **export psd to png** stap), daarna bewaren we de PSD met de nieuwe lagen.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tip:** Als je alleen de PNG nodig hebt, kun je de PSD `save`‑aanroep overslaan en direct `save` aanroepen met `PngOptions`.

## Veelvoorkomende Problemen & Foutopsporing

| Symptoom | Waarschijnlijke Oorzaak | Oplossing |
|----------|--------------------------|-----------|
| PNG verschijnt leeg | Lagen zijn onzichtbaar of volledig transparant | Zorg ervoor dat je niet‑transparante pixelwaarden instelt of `layer.setVisible(true)` aanroept. |
| `ArrayIndexOutOfBoundsException` | Mismatch tussen de grootte van de rechthoek en de lengte van de pixelarray | Controleer dat `rect.width * rect.height == dataArray.length`. |
| LicenseException tijdens uitvoering | Geen geldige licentie geladen | Laad een tijdelijke of permanente licentie voordat je API‑methoden aanroept. |

## Veelgestelde Vragen

**Q: Is Aspose.PSD compatibel met Java 8?**  
A: Yes, Aspose.PSD supports Java 8 and later versions.

**Q: Kan ik transformaties (rotatie, schaal) toepassen op de toegevoegde lagen?**  
A: Absolutely! The `Layer` class provides methods such as `rotate`, `scale`, and `translate` for full transformation control.

**Q: Waar kan ik extra Aspose.PSD documentatie vinden?**  
A: Detailed API docs are available [here](https://reference.aspose.com/psd/java/).

**Q: Hoe verkrijg ik een tijdelijke licentie voor Aspose.PSD?**  
A: Visit the temporary‑license page [here](https://purchase.aspose.com/temporary-license/).

**Q: Zijn er community‑forums voor Aspose.PSD‑ondersteuning?**  
A: Yes, join the discussions on the Aspose forums [here](https://forum.aspose.com/c/psd/34).

## Conclusie

Je hebt nu geleerd hoe je **PSD naar PNG kunt exporteren** terwijl je **nieuwe reguliere lagen toevoegt** met Aspose.PSD voor Java, en je hebt gezien hoe een **aspose temporary license** je in staat stelt deze workflow zonder beperkingen uit te proberen. Deze tutorial toont de kernmogelijkheden van **psd image manipulation**: een bestand laden, lagen maken, pixelgegevens vullen en de uiteindelijke compositie exporteren. Voel je vrij om te experimenteren met verschillende rechthoekgroottes, pixelkleuren of laageffecten om de output aan de behoeften van je project aan te passen.

---

**Laatst Bijgewerkt:** 2026-04-08  
**Getest Met:** Aspose.PSD 24.11 for Java  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}