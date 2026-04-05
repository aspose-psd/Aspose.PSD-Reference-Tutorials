---
date: 2026-04-05
description: Leer hoe u PSD naar PNG exporteert en moeiteloos het contrast van afbeeldingen
  verbetert met Aspose.PSD voor Java. Beheers niveaus‑aanpassingslagen met deze stapsgewijze
  gids.
keywords:
- export psd to png
- how to adjust levels
- batch process psd files
linktitle: Exporteer PSD naar PNG en render de niveau‑aanpassingslaag in Java
second_title: Aspose.PSD Java API
title: Exporteer PSD naar PNG en render de Niveau‑aanpassingslaag in Java
url: /nl/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export PSD naar PNG en Render Level Adjustment Layer in Java

## Introductie

Heb je ooit een PSD‑bestand geopend en gemerkt dat de kleuren vlak of het contrast niet goed waren? Je kunt snel **export PSD to PNG** uitvoeren terwijl je de afbeelding fijn afstemt met een Levels Adjustment Layer met behulp van Aspose.PSD voor Java. In deze tutorial lopen we het volledige proces door—van het laden van een PSD, het aanpassen van de niveaus, tot het opslaan van het resultaat als PNG—zodat je de levendigheid kunt verhogen en web‑klare assets in enkele minuten kunt voorbereiden.

## Snelle antwoorden
- **Wat betekent “export PSD to PNG”?** Het converteert een Photoshop‑document naar een verliesvrije PNG‑afbeelding terwijl transparantie behouden blijft.  
- **Kan ik niveaus aanpassen vóór het exporteren?** Ja, Aspose.PSD stelt je in staat om invoer‑ en uitvoerniveaus programmatisch te wijzigen.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor ontwikkeling; een commerciële licentie is vereist voor productie.  
- **Is batch‑verwerking mogelijk?** Absoluut—je kunt de code in een lus plaatsen om meerdere PSD‑bestanden te verwerken.  
- **Welke Java‑versie is vereist?** Java 8 of nieuwer wordt aanbevolen.

## Wat is “export PSD to PNG”?
Exporteren van een PSD naar PNG betekent dat je het gelaagde Photoshop‑bestand plat maakt tot een Portable Network Graphics‑afbeelding. PNG ondersteunt verliesloze compressie en een alfakanaal, waardoor het ideaal is voor web‑graphics en UI‑assets.

## Waarom niveaus aanpassen vóór het exporteren?
Het aanpassen van niveaus stelt je in staat schaduwen, middentonen en hooglichten te regelen, waardoor het algehele contrast en de kleurbalans verbeteren. Deze stap zorgt ervoor dat de uiteindelijke PNG er gepolijst uitziet zonder handmatige bewerking in Photoshop.

## Voorvereisten

- **Java Development Kit (JDK)** – download de nieuwste versie van de Oracle‑website ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).  
- **Aspose.PSD for Java Library** – haal deze op van de officiële downloadpagina ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Een gratis proefversie is beschikbaar ([https://releases.aspose.com/](https://releases.aspose.com/)).  

## Import Packages

Voordat we in de code duiken, importeren we de klassen die ons toegang geven tot PSD‑manipulatie en PNG‑export:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

## Stapsgewijze handleiding

### Stap 1: Definieer bestands‑paden (Hoe PSD‑verwerking te automatiseren)

Stel duidelijke, beschrijvende variabelen in voor de bron‑PSD, de aangepaste PSD en de uiteindelijke PNG‑exportlocatie.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

### Stap 2: Laad de PSD‑afbeelding

Gebruik `Image.load` om het PSD‑bestand in een `PsdImage`‑object te lezen. Aspose.PSD detecteert automatisch het formaat.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Stap 3: Itereer door lagen (Hoe niveaus aan te passen)

Loop over elke laag om de Levels Adjustment Layer te vinden.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (code to check for Levels Layer will be added here)
}
```

### Stap 4: Identificeer de Levels‑laag

Controleer elke laag met `instanceof LevelsLayer`. Wanneer gevonden, cast je deze zodat we de eigenschappen kunnen wijzigen.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (code to adjust levels will be added here)
   }
}
```

### Stap 5: Fijn afstemmen van niveaus (Hoe niveaus aan te passen)

Pas zowel invoer‑ als uitvoerniveaus aan voor het eerste kanaal (meestal het samengestelde kanaal). Deze waarden zijn voorbeelden; voel je vrij om te experimenteren.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Adjust Input Levels (0‑255):
	   channel.setInputShadowLevel((short) 10); // Darken shadows slightly
	   channel.setInputMidtoneLevel(2.0f);     // Increase midtones
	   channel.setInputHighlightLevel((short) 230); // Reduce highlights

	   // Adjust Output Levels (0‑255):
	   channel.setOutputShadowLevel((short) 20); // Darken shadows further
	   channel.setOutputHighlightLevel((short) 200); // Brighten highlights
   }
}
```

### Stap 6: Sla de aangepaste PSD op (Hoe PSD te automatiseren)

Bewaar de wijzigingen terug in een nieuw PSD‑bestand.

```java
im.save(psdPathAfterChange);
```

### Stap 7: Exporteren als PNG (Export PSD naar PNG)

Als je een PNG‑versie nodig hebt, configureer je `PngOptions` en sla je de afbeelding op.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

## Veelvoorkomende use‑cases

- **Voorbereiding van web‑assets:** Converteer door ontwerpers geleverde PSD‑mockups naar PNG’s die klaar zijn voor browsers.  
- **Batch‑verwerking:** Automatiseer de conversie van tientallen PSD‑bestanden in een CI‑pipeline.  
- **Dynamische beeldgeneratie:** Pas niveaus on‑the‑fly aan op basis van gebruikersinvoer vóór het exporteren.

## Problemen oplossen & Tips

- **Null‑pointer bij het benaderen van lagen:** Zorg ervoor dat de PSD daadwerkelijk een Levels Adjustment Layer bevat; voeg anders een null‑check toe.  
- **Onverwachte kleuren na export:** Controleer of het PNG‑kleurtype is ingesteld op `TruecolorWithAlpha` om transparantie te behouden.  
- **Prestaties bij veel bestanden:** Hergebruik dezelfde `PsdImage`‑instantie bij het verwerken van een batch om geheugen‑overhead te verminderen.

## Veelgestelde vragen

**Q: Kan ik individuele kleurkanalen (RGB) afzonderlijk aanpassen?**  
A: Ja. Gebruik `levelsLayer.getChannel(index)` waarbij `index` = 0 (Rood), 1 (Groen), 2 (Blauw) om elk kanaal onafhankelijk bij te stellen.

**Q: Hoe ga ik om met meerdere Levels Adjustment Layers in één PSD?**  
A: De lus verwerkt elke laag; elke gevonden `LevelsLayer` wordt aangepast volgens de code binnen het `if`‑blok.

**Q: Zijn er andere manieren om contrast te verbeteren naast Levels?**  
A: Aspose.PSD biedt ook Curves, Brightness/Contrast en Histogram Equalization‑aanpassingen.

**Q: Kan ik dit automatiseren voor een map met PSD‑bestanden?**  
A: Plaats de volledige workflow in een `File[] files = new File(dataDir).listFiles((d, name) -> name.endsWith(".psd"));`‑lus en verwerk elk bestand achtereenvolgens.

**Q: Waar vind ik meer documentatie en ondersteuning?**  
A: Bezoek de officiële referentie ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) en het community‑forum ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)).

## Conclusie

Door de **export PSD to PNG**‑workflow onder de knie te krijgen en te leren **hoe niveaus programmatically aan te passen**, krijg je volledige controle over de beeldkwaliteit zonder je Java‑omgeving te verlaten. Of je nu assets voorbereidt voor het web, een design‑pipeline automatiseert, of een batch‑processor bouwt, Aspose.PSD voor Java maakt het werk eenvoudig en betrouwbaar.

---

**Laatst bijgewerkt:** 2026-04-05  
**Getest met:** Aspose.PSD 24.11 for Java  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}