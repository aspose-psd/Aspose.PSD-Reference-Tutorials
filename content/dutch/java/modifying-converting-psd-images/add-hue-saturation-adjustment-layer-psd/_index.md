---
title: Voeg aanpassingslaag tintverzadiging toe aan PSD
linktitle: Voeg aanpassingslaag tintverzadiging toe aan PSD
second_title: Aspose.PSD Java-API
description: Leer hoe u aanpassingslagen voor tintverzadiging aan PSD kunt toevoegen met behulp van Aspose.PSD voor Java in deze uitgebreide, stapsgewijze zelfstudie. Verbeter uw grafische ontwerpworkflow.
type: docs
weight: 14
url: /nl/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---
## Invoering
Als het om grafisch ontwerp gaat, speelt kleurmanipulatie een cruciale rol; met name het aanpassen van tint, verzadiging en lichtheid kan de sfeer en kwaliteit van elk beeld drastisch veranderen. Een effectieve manier om dit te bereiken is door het gebruik van aanpassingslagen in Photoshop (PSD-bestanden). Als u uw PSD-bestanden programmatisch wilt verbeteren met Java, is de Aspose.PSD-bibliotheek hier om u te helpen! Deze tutorial leidt u door de stappen om een aanpassingslaag voor tintverzadiging aan uw PSD-bestanden toe te voegen, waardoor uw workflows productiever en efficiënter worden.
In deze handleiding behandelen we alles, van het importeren van de benodigde pakketten tot de kleinste details van de codevoorbeelden.
## Vereisten
Voordat we ingaan op de code, zorg ervoor dat je het volgende hebt geïnstalleerd:
1.  Java Development Kit (JDK): Zorg ervoor dat JDK 8 of hoger op uw computer is geïnstalleerd. Je kunt het downloaden van de[Java SE Development Kit-downloads](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD voor Java-bibliotheek: u hebt de Aspose.PSD-bibliotheek nodig, wat mogelijk is[download hier](https://releases.aspose.com/psd/java/). 
3. IDE: Een geschikte Integrated Development Environment (IDE) zoals IntelliJ IDEA of Eclipse voor Java-ontwikkeling.
4. Basiskennis van Java: Bekendheid met programmeren in Java is een pluspunt, maar maak je geen zorgen; we leiden u stap voor stap door de code.
Nu we onze vereisten op orde hebben, gaan we verder met het leuke gedeelte: coderen!
## Pakketten importeren
Om met de Aspose.PSD-bibliotheek te gaan werken, is de eerste stap het importeren van de benodigde klassen. Zo kunt u het in uw Java-bestand doen:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
Zorg ervoor dat u de juiste bibliotheken aan uw project toevoegt, zodat deze import naadloos werkt.
## Stap 1: Stel uw documentenmap in
Elk project heeft een startpunt nodig, en dat van ons is daarop geen uitzondering. U moet een map opgeven waar uw PSD-bestanden worden opgeslagen. Dit is cruciaal voor het correct laden en opslaan van afbeeldingen.
```java
String dataDir = "Your Document Directory"; // Werk dit pad bij naar uw werkelijke map
```
## Stap 2: Laad een bestaand PSD-bestand
Om een bestaand PSD-bestand te manipuleren, moeten we het eerst in ons programma laden. Hier ziet u hoe u dat kunt doen:
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Update in deze code`"HueSaturationAdjustmentLayer.psd"` naar de naam van uw bestaande PSD-bestand dat u wilt bewerken.
## Stap 3: Bewerk de tint/verzadigingslaag
Vervolgens doorlopen we de lagen van onze geladen PSD-afbeelding om eventuele bestaande tint-/verzadigingslagen te vinden en te bewerken. Deze stap omvat het wijzigen van de waarden voor tint, verzadiging en helderheid.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```
In dit voorbeeld:
- We passen de tint aan naar -25, de verzadiging naar -12 en de lichtheid naar +67.
-  De`getRange(2)` Met deze methode kunnen we specifieke kleurbereiken naar wens aanpassen.
## Stap 4: Sla het gewijzigde PSD-bestand op
Nadat u de aanpassingen heeft aangebracht, is de volgende stap het opslaan van het bestand. Dit is een essentieel onderdeel van ons proces en zorgt ervoor dat de wijzigingen die we hebben aangebracht niet verloren gaan.
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## Stap 5: Voeg een nieuwe tint / verzadigingslaag toe
Vervolgens wilt u misschien een nieuwe aanpassingslaag voor tint/verzadiging toevoegen aan een ander PSD-bestand. Volg gewoon dezelfde aanpak die u eerder gebruikte, maar met verschillende PSD-bestanden.
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## Stap 6: Stel nieuwe tint-/verzadigingswaarden in voor de nieuwe laag
Nu u deze nieuwe laag hebt gemaakt, past u de gewenste instellingen voor tint, verzadiging en helderheid toe, net als voorheen.
```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```
## Stap 7: Sla het bijgewerkte PSD-bestand op
Sla ten slotte het PSD-bestand op met de toegevoegde tint-/verzadigingslaag, zodat u uw wijzigingen kunt zien.
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
Gefeliciteerd! U hebt met succes PSD-bestanden gemanipuleerd met Aspose.PSD voor Java. Nu kunt u experimenteren met verschillende afbeeldingen en diepere wijzigingen, waardoor uw grafische ontwerpprojecten tot leven komen.
## Conclusie
Programmatisch werken met graphics opent een wereld aan mogelijkheden. Het gebruik van Aspose.PSD voor Java om aanpassingslagen voor tintverzadiging toe te voegen en te wijzigen, biedt flexibiliteit en efficiëntie die uw ontwerpworkflow kunnen stroomlijnen. Of u nu foto's voor een project verbetert of verbluffende visuele inhoud maakt, het beheersen van deze tools kan uw output aanzienlijk verbeteren.
 Voel je vrij om meer functionaliteiten van Aspose.PSD te verkennen door erin te duiken[documentatie](https://reference.aspose.com/psd/java/) of overweeg om een[tijdelijke licentie](https://purchase.aspose.com/temporary-license/) om de volledige kracht van de bibliotheek te testen.
## Veelgestelde vragen
### Wat is een aanpassingslaag voor tintverzadiging?
Met een aanpassingslaag voor tintverzadiging kunt u de kleureigenschappen van een afbeelding wijzigen zonder de oorspronkelijke pixels permanent te wijzigen.
### Moet ik Photoshop installeren om Aspose.PSD te kunnen gebruiken?
Nee, Aspose.PSD is een zelfstandige bibliotheek die onafhankelijk van Photoshop werkt.
### Kan ik Aspose.PSD gebruiken voor batchverwerking?
Ja, u kunt meerdere PSD-bestanden automatiseren en batchgewijs verwerken met Aspose.PSD.
### Is Aspose.PSD gratis?
Aspose.PSD biedt een gratis proefperiode, maar voor langdurig gebruik is een licentie vereist. U kunt de prijzen bekijken[hier](https://purchase.aspose.com/buy).