---
title: Renderniveau-aanpassingslaag in PSD-bestanden - Java
linktitle: Renderniveau-aanpassingslaag in PSD-bestanden - Java
second_title: Aspose.PSD Java-API
description: Leer hoe u moeiteloos het contrast en de levendigheid van afbeeldingen kunt verbeteren met Aspose.PSD voor Java. Beheers niveau-aanpassingslagen met deze stapsgewijze handleiding.
type: docs
weight: 17
url: /nl/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---
## Invoering

Heeft u ooit een PSD-bestand geopend en ontdekt dat de afbeelding geen contrast of levendigheid heeft? Wees niet bang, beeldbewerkingsstrijders! Aspose.PSD voor Java komt te hulp met zijn krachtige mogelijkheden voor niveau-aanpassingslaagmanipulatie. Deze gids geeft u de kennis om uw afbeeldingen in een handomdraai te verfijnen met behulp van Niveaus. 

## Vereisten

- Java Development Kit (JDK): Zorg ervoor dat er een recente versie van JDK op uw systeem is geïnstalleerd. U kunt het downloaden van de Oracle-website ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).
- Aspose.PSD voor Java-bibliotheek: Download de Aspose.PSD voor Java-bibliotheek vanaf de downloadpagina ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). U heeft een geldige licentie nodig om de volledige functies te kunnen gebruiken, maar er is een gratis proefversie beschikbaar om u op weg te helpen ([https://releases.aspose.com/](https://releases.aspose.com/)).

## Pakketten importeren

Voordat we in de code duiken, moeten we de benodigde Aspose.PSD-klassen importeren om met PSD-bestanden te kunnen communiceren. Dit is wat je nodig hebt:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

 De`com.aspose.psd` pakket biedt toegang tot functionaliteiten voor PSD-manipulatie, terwijl`com.aspose.psd.imaging.PngOptions` stelt ons in staat opties te definiëren bij het opslaan van de afbeelding als PNG.

Laten we nu beginnen aan ons avontuur voor het aanpassen van niveaus:

## Stap 1: Bestandspaden instellen:

- Definieer variabelen voor uw documentmap (`dataDir`), bron-PSD-bestandsnaam (`sourceFileName`), doel-PSD-bestandsnaam na wijziging (`psdPathAfterChange`), en het uiteindelijke PNG-exportpad (`pngExportPath`). Overweeg het gebruik van beschrijvende namen om de leesbaarheid van de code te verbeteren.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## Stap 2: Het laden van de PSD-afbeelding:

-  Gebruik de`Image.load` methode om het PSD-bronbestand te openen en op te slaan in een`PsdImage`voorwerp (`im`). Aspose.PSD detecteert automatisch het bestandsformaat.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Stap 3: Itereren door lagen:

- We moeten de niveau-aanpassingslaag in uw PSD vinden. Aspose biedt een handige manier om door alle lagen te itereren met behulp van een lus.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (code om te controleren op Niveauslaag wordt hier toegevoegd)
}
```

## Stap 4: Identificatie van de niveaulaag:

- Controleer binnen de lus of de huidige laag (`im.getLayers()[i]` ) is een exemplaar van de`LevelsLayer` klas met behulp van de`instanceof` exploitant. 
-  Als dit het geval is, cast u de laag naar a`LevelsLayer` object voor verdere manipulatie.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (code om niveaus aan te passen wordt hier toegevoegd)
   }
}
```
## Stap 5: Niveaus afstemmen (vervolg):

-  Pas de uitgangsniveaus aan met`setOutputShadowLevel` En`setOutputHighlightLevel` om de duisternis en lichtheid van het resulterende beeld te beheersen. Deze waarden bepalen het bereik van de ingangsniveaus die aan het uitgangsbereik worden toegewezen.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Ingangsniveaus aanpassen (0-255):
	   channel.setInputShadowLevel((short) 10); // Maak schaduwen iets donkerder
	   channel.setInputMidtoneLevel(2.0f);     // Verhoog de middentonen
	   channel.setInputHighlightLevel((short) 230); // Verminder hoogtepunten

	   // Uitgangsniveaus aanpassen (0-255):
	   channel.setOutputShadowLevel((short) 20); // Maak schaduwen nog donkerder
	   channel.setOutputHighlightLevel((short) 200); //Maak hoogtepunten helderder
   }
}
```

## Stap 6: De gewijzigde PSD opslaan:

-  Gebruik de`save` werkwijze van de`PsdImage` object om de gewijzigde afbeelding op te slaan in het opgegeven pad (`psdPathAfterChange`).

```java
im.save(psdPathAfterChange);
```

## Stap 7: Exporteren als PNG (optioneel):

-  Als je een PNG-versie van de aangepaste afbeelding nodig hebt, maak dan een`PngOptions` object en stel het kleurtype in`TruecolorWithAlpha` . Gebruik dan de`save` methode opnieuw met het PNG-exportpad en de opties.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

En daar heb je het! U hebt de Levels Adjustment Layer in uw PSD-bestand met succes aangepast met Aspose.PSD voor Java. Door deze stappen te begrijpen en met verschillende waarden te experimenteren, kunt u het contrast en de algehele uitstraling van uw afbeeldingen verbeteren.

## Conclusie

Aspose.PSD voor Java geeft u de controle over uw beeldbewerkingsproces. Door de aanpassingslaag voor niveaus onder de knie te krijgen, kunt u uw foto's en ontwerpen nieuw leven inblazen. Vergeet niet dat oefening kunst baart, dus aarzel niet om te experimenteren en het volledige potentieel van dit krachtige hulpmiddel te verkennen.
 
## Veelgestelde vragen

### Kan ik individuele kleurkanalen (RGB) afzonderlijk aanpassen? 
Ja, u heeft toegang tot elk kleurkanaal via de`getChannel` werkwijze van de`LevelsLayer` object en wijzig de niveaus ervan onafhankelijk.

### Hoe ga ik om met meerdere aanpassingslagen voor niveaus in een PSD?
De code herhaalt zich door alle lagen, zodat eventuele extra Levels-lagen in de afbeelding automatisch worden verwerkt.

### Zijn er naast Niveaus nog andere manieren om het beeldcontrast aan te passen?
Absoluut! Aspose.PSD biedt verschillende hulpmiddelen voor beeldaanpassing, zoals curven, helderheid/contrast en meer.

### Kan ik dit proces voor meerdere afbeeldingen automatiseren? 
Ja, u kunt deze code opnemen in een lus- of batchverwerkingsscript om meerdere PSD-bestanden efficiënt te verwerken.

### Waar kan ik meer informatie en ondersteuning vinden?
Aspose biedt uitgebreide documentatie ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) en een ondersteuningsforum ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) voor eventuele vragen of problemen die u tegenkomt.