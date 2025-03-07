---
title: Maak lagen in PSD-bestanden plat met Aspose.PSD Java
linktitle: Maak lagen in PSD-bestanden plat met Aspose.PSD Java
second_title: Aspose.PSD Java-API
description: Maak lagen in PSD-bestanden moeiteloos plat en voeg ze samen met Aspose.PSD voor Java. Volg deze stapsgewijze handleiding om uw PSD-bestandsbeheer te vereenvoudigen.
weight: 13
url: /nl/java/psd-layer-management-effects/flatten-layers-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Maak lagen in PSD-bestanden plat met Aspose.PSD Java

## Invoering

Heeft u ooit met Photoshop-bestanden gewerkt en wenste u een eenvoudigere manier om die complexe lagen te beheren? Nou, je hebt geluk! Vandaag duiken we in de wereld van Aspose.PSD voor Java, een krachtig hulpmiddel dat het een fluitje van een cent maakt om programmatisch met PSD-bestanden te werken. Een van de handige functies die we gaan onderzoeken is het afvlakken van lagen. Of u nu een hele afbeelding wilt afvlakken of selectief specifieke lagen wilt samenvoegen, Aspose.PSD voor Java heeft de oplossing. Deze tutorial begeleidt u stap voor stap door het proces, zodat u er zeker van bent dat u met vertrouwen aan de slag kunt met uw PSD-bestanden.

## Vereisten

Voordat we ingaan op de code, zorgen we ervoor dat je alles hebt wat je nodig hebt:

1. Java Development Kit (JDK): Zorg ervoor dat JDK 8 of hoger op uw systeem is geïnstalleerd.
2.  Aspose.PSD voor Java: Download de Aspose.PSD-bibliotheek en voeg deze toe aan uw project. Je kunt het vinden[hier](https://releases.aspose.com/psd/java/).
3. Integrated Development Environment (IDE): Een IDE zoals IntelliJ IDEA of Eclipse zal uw codeerervaring soepeler maken.
4. Basiskennis van Java: Hoewel deze tutorial beginnersvriendelijk is, zal enige basiskennis van Java u helpen gemakkelijker te volgen.
5. Voorbeeld PSD-bestand: Zorg ervoor dat u een PSD-bestand gereed heeft om mee te experimenteren. We gebruiken er een met meerdere lagen om het afvlakkingsproces te demonstreren.

Nu we de essentie achter de rug hebben, gaan we naar het leuke gedeelte: werken met de code!

## Pakketten importeren

Om te beginnen moet u de benodigde pakketten in uw Java-project importeren. Met deze pakketten kunt u met PSD-bestanden werken met Aspose.PSD voor Java.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

Met deze import kunnen we PSD-bestanden laden, lagen manipuleren en de wijzigingen opslaan. Laten we nu het proces van het afvlakken van lagen opsplitsen in beheersbare stappen.

## Stap 1: Het volledige PSD-beeld plat maken

De eerste taak is om het gehele PSD-beeld plat te maken. Dit is handig als u alle lagen in één laag wilt combineren, waardoor de afbeelding gemakkelijker te beheren en te exporteren is.

### 1.1 Laad het PSD-bestand

 Eerst laden we het PSD-bestand in ons programma. Dit bestand moet in uw projectmap worden geplaatst, waarnaar we zullen verwijzen als`Your Document Directory`.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ThreeRegularLayersSemiTransparent.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

Dit codefragment laadt het PSD-bestand met de naam`ThreeRegularLayersSemiTransparent.psd` uit de door u opgegeven directory.

### 1.2 Maak de afbeelding plat

Vervolgens maken we de hele afbeelding plat. Met afvlakking worden alle zichtbare lagen gecombineerd tot één enkele achtergrondlaag.

```java
im.flattenImage();
```

Met deze oneliner worden alle lagen in je PSD-bestand samengevoegd tot één.

### 1.3 Sla de afgeplatte afbeelding op

Ten slotte slaan we de afgeplatte afbeelding op in een nieuw bestand.

```java
String exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattened.psd";
im.save(exportPath);
```

 Hierdoor wordt het afgeplatte PSD-bestand onder de nieuwe naam opgeslagen`ThreeRegularLayersSemiTransparentFlattened.psd`. Gefeliciteerd! U hebt zojuist uw eerste PSD-afbeelding afgevlakt met Aspose.PSD voor Java.

## Stap 2: Specifieke lagen samenvoegen

Soms wilt u misschien niet de hele afbeelding plat maken, maar alleen bepaalde lagen samenvoegen. Laten we eens kijken hoe u dat kunt bereiken.

### 2.1 Laad het PSD-bestand opnieuw

Omdat we een andere bewerking uitvoeren, begint u met het opnieuw laden van het PSD-bestand.

```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

Hierdoor wordt hetzelfde PSD-bestand geladen, klaar voor laagspecifieke bewerkingen.

### 2.2 Identificeer en selecteer lagen

Om specifieke lagen samen te voegen, identificeert en selecteert u eerst de lagen die u wilt samenvoegen.

```java
Layer bottomLayer = img.getLayers()[0];
Layer middleLayer = img.getLayers()[1];
Layer topLayer = img.getLayers()[2];
```

Hier selecteren we de eerste, tweede en derde laag van het PSD-bestand. Deze lagen worden opgeslagen in een array en u kunt ze openen via hun index.

### 2.3 Voeg de lagen samen

Laten we nu de geselecteerde lagen samenvoegen. We beginnen met het samenvoegen van de onderste en middelste laag en voegen vervolgens het resultaat samen met de bovenste laag.

```java
Layer layer1 = img.mergeLayers(bottomLayer, middleLayer);
Layer layer2 = img.mergeLayers(layer1, topLayer);
```

Deze code voegt de lagen opeenvolgend samen, wat resulteert in een enkele gecombineerde laag.

### 2.4 Vervang de bestaande lagen door de samengevoegde laag

Na het samenvoegen moet u de bestaande lagen in de afbeelding vervangen door de nieuw samengevoegde laag.

```java
img.setLayers(new Layer[]{layer2});
```

Deze stap zorgt ervoor dat de afbeelding nu alleen de samengevoegde laag bevat.

### 2.5 Sla het bijgewerkte PSD-bestand op

Sla ten slotte het bijgewerkte PSD-bestand op met de samengevoegde lagen.

```java
exportPath = dataDir + "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";
img.save(exportPath);
```

Hierdoor wordt de PSD met de samengevoegde lagen onder een nieuwe naam opgeslagen, zodat u het originele bestand intact kunt houden.

## Conclusie

Werken met lagen in PSD-bestanden kan vaak het gevoel geven dat u door een labyrint navigeert, maar met Aspose.PSD voor Java is het alsof u een kaart in handen heeft. Of u nu een hele afbeelding plat wilt maken of geselecteerde lagen zorgvuldig wilt samenvoegen, Aspose.PSD vereenvoudigt het proces, waardoor een soms lastige taak in een eenvoudige handeling wordt omgezet. Door deze tutorial te volgen, zou u nu vertrouwd moeten zijn met het hanteren van laagmanipulatie in PSD-bestanden met behulp van Java. Dus waarom probeert u het niet eens met uw eigen projecten en ziet u hoeveel tijd en moeite u bespaart?

## Veelgestelde vragen

### Kan ik het afvlakken van lagen in Aspose.PSD ongedaan maken?  
Nee, zodra u lagen plat maakt met Aspose.PSD, is de actie onomkeerbaar. Het is altijd een goede gewoonte om een back-up van het originele bestand te bewaren.

### Is het mogelijk om alleen zichtbare lagen plat te maken?  
 Ja, u kunt bepalen welke lagen u wilt afvlakken op basis van hun zichtbaarheid. Zorg ervoor dat alleen de lagen die u wilt afvlakken zichtbaar zijn voordat u de`flattenImage` methode.

### Verkleint het afvlakken van lagen de bestandsgrootte?  
Het afvlakken van lagen kan de bestandsgrootte verkleinen, vooral als er veel complexe lagen zijn. De exacte reductie is echter afhankelijk van de inhoud van de lagen.

### Kan ik lagen met verschillende overvloeimodi samenvoegen?  
Ja, u kunt lagen met verschillende overvloeimodi samenvoegen met Aspose.PSD, en de resulterende laag behoudt het uiterlijk van de samengevoegde lagen.

### Wat gebeurt er als ik probeer lagen samen te voegen die niet aangrenzend zijn?  
Met Aspose.PSD kunt u alle lagen samenvoegen, ongeacht hun volgorde in de lagenstapel. Het samenvoegproces combineert de geselecteerde lagen zoals gespecificeerd.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
