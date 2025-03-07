---
title: Voeg niveauaanpassingslaag toe in PSD
linktitle: Voeg niveauaanpassingslaag toe in PSD
second_title: Aspose.PSD Java-API
description: Leer hoe u effectief een niveauaanpassingslaag aan uw PSD-bestanden kunt toevoegen met Aspose.PSD voor Java. Verbeter uw beeldbewerkingsvaardigheden.
weight: 16
url: /nl/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Voeg niveauaanpassingslaag toe in PSD

## Invoering
Als het om beeldbewerking gaat, kan het beheren van niveaus een wereld van verschil maken in de levendigheid en helderheid van uw foto's. Een handig hulpmiddel in het Photoshop-arsenaal is de "Level Adjustment Layer", waarmee u het toonbereik en de kleurbalans van uw afbeeldingen kunt aanpassen. In deze handleiding laten we u zien hoe u een Level Adjustment Layer in een PSD-bestand implementeert met behulp van Aspose.PSD voor Java. Dus pak je Java IDE.
## Vereisten
Voordat je de wereld van niveauaanpassingen betreedt, moet je een paar dingen instellen om een soepele rit te garanderen:
1.  Java Development Kit (JDK): Zorg ervoor dat de JDK op uw computer is geïnstalleerd. Als u deze niet heeft, kunt u deze ophalen bij de[Oracle-website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) of gebruik OpenJDK.
2.  Aspose.PSD voor Java-bibliotheek: Om PSD-bestanden te manipuleren, moet u de Aspose.PSD-bibliotheek downloaden. Hiervan kunt u de nieuwste versie verkrijgen[downloadlink](https://releases.aspose.com/psd/java/) en zorg ervoor dat u de JAR in de bibliotheek van uw project hebt opgenomen.
3. Basiskennis van Java: Een fundamenteel begrip van Java-programmering zal helpen, aangezien we in deze tutorial in codefragmenten zullen duiken.
4. IDE-installatie: u kunt elke gewenste Java-IDE gebruiken, zoals IntelliJ IDEA, Eclipse of NetBeans, om uw code te schrijven en uit te voeren. Zorg ervoor dat u uw Java-project hebt ingesteld en de Aspose.PSD-bibliotheek hebt toegevoegd.

## Pakketten importeren
Voordat we beginnen met het schrijven van onze code, moeten we de benodigde pakketten importeren uit de Aspose.PSD-bibliotheek. Hier ziet u hoe u het kunt doen:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Door deze pakketten te importeren, hebben we toegang tot de klassen die nodig zijn voor het laden, wijzigen en opslaan van onze PSD-bestanden.

Laten we het proces nu opsplitsen in verteerbare stappen. Volg ons terwijl we het laden van een PSD-bestand doorlopen, de niveaus aanpassen en vervolgens uw wijzigingen opslaan. 
## Stap 1: Stel uw bestandspaden in
De eerste stap is het definiëren waar ons PSD-bestand zich bevindt en waar we de gewijzigde uitvoer willen opslaan. U kunt het mappad aanpassen aan uw behoeften.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
 Hier, vervang`"Your Document Directory"`met het daadwerkelijke pad op uw systeem waar uw PSD-bestand is opgeslagen. Dit vormt de basis voor alles wat we hierna gaan doen.
## Stap 2: Laad het PSD-bestand
 Laten we nu het PSD-bestand laden met behulp van de`PsdImage` klas. Deze stap is essentieel omdat we hierdoor toegang krijgen tot de lagen en deze kunnen manipuleren.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 Wanneer u belt`Image.load()` , zal het het PSD-bestand lezen en een exemplaar van maken`PsdImage` waar je mee kunt werken.
## Stap 3: Herhaal de lagen
Omdat we een niveauaanpassingslaag willen aanpassen, moeten we elke laag in ons PSD-bestand doorlopen. Dit helpt ons de specifieke laag te vinden die we willen wijzigen.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Verdere manipulatie zal hier plaatsvinden...
    }
}
```
 In deze lus,`instanceof LevelsLayer` controleert of de huidige laag een niveau-aanpassingslaag is. Als dat zo is, kunnen we doorgaan met het aanpassen van de eigenschappen.
## Stap 4: Pas de niveaukanaalinstellingen aan
Zodra we de juiste laag hebben geïdentificeerd, kunnen we de invoer- en uitvoerniveaus ervan aanpassen. Dit is waar de magie gebeurt! Pas verschillende parameters aan om te zien hoe deze de afbeelding beïnvloeden.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
Dit is wat elke parameter doet:
- Ingangsmiddentoonniveau: Past de middentonen aan.
- Invoerschaduwniveau: past de donkere delen van het beeld aan.
- Invoermarkeringsniveau: Wijzigt de heldere delen van het beeld.
- Uitvoerschaduwniveau: Stelt in hoe donkere schaduwen verschijnen.
- Uitvoermarkeringsniveau: Stelt in hoe lichte highlights verschijnen.
Experimenteer gerust met verschillende waarden!
## Stap 5: Sla het gewijzigde PSD-bestand op
Nu we onze aanpassingen hebben aangebracht, is het tijd om het gewijzigde PSD-bestand op te slaan. Deze stap is cruciaal om ervoor te zorgen dat uw wijzigingen worden toegepast en opgeslagen.
```java
im.save(psdPathAfterChange);
```
 U kunt uw aangepaste PSD-bestand nu vinden op het opgegeven`psdPathAfterChange`. 
## Conclusie
Je hebt zojuist geleerd hoe je een niveauaanpassingslaag aan een PSD-bestand kunt toevoegen met Aspose.PSD voor Java! Door deze handleiding te volgen, kunt u de toonkwaliteit van uw afbeeldingen moeiteloos aanpassen, waardoor de weg wordt vrijgemaakt voor een levendiger en visueel aantrekkelijker resultaat. Vergeet niet dat oefening kunst baart, dus voel je vrij om de aanpassingen aan te passen en verschillende PSD-bestanden te verkennen om de effecten van je wijzigingen te zien.
## Veelgestelde vragen
### Wat is een niveauaanpassingslaag?
Met een niveauaanpassingslaag kunt u het toonbereik in uw afbeeldingen corrigeren, waarbij schaduwen, middentonen en hooglichten in evenwicht worden gebracht.
### Kan ik Aspose.PSD gebruiken zonder aankoop?
Ja! Aspose biedt een gratis proefperiode aan om de bibliotheek te testen voordat u deze aanschaft.
### Waar kan ik documentatie voor Aspose.PSD vinden?
 U kunt de documentatie vinden[hier](https://reference.aspose.com/psd/java/).
### Is er enige community-ondersteuning voor Aspose-producten?
 Absoluut! U kunt vragen stellen en ondersteuning krijgen in de[Aspose-forum](https://forum.aspose.com/c/psd/34).
### Hoe kan ik een tijdelijke licentie krijgen voor Aspose.PSD?
 U kunt een tijdelijke vergunning aanvragen[hier](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
