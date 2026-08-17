---
date: 2026-03-07
description: Leer hoe je niveaus kunt aanpassen door een Niveau‑aanpassingslaag toe
  te voegen in PSD‑bestanden met Aspose.PSD voor Java. Beheers toonaanpassingen snel.
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
title: Hoe niveaus aanpassen – Voeg een niveausaanpassingslaag toe in PSD
url: /nl/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Niveausaanpassingslaag toevoegen in PSD

## Introductie
Als je wilt weten **hoe je niveaus kunt aanpassen** in je Photoshop‑documenten, is de Niveausaanpassingslaag het perfecte hulpmiddel. Het stelt je in staat om schaduwen, middentonen en hooglichten fijn af te stemmen zonder de originele pixels permanent te wijzigen. In deze tutorial laten we stap voor stap zien hoe je een Niveausaanpassingslaag toevoegt aan een PSD‑bestand met Aspose.PSD voor Java, zodat je professionele toonregeling bereikt in slechts een paar stappen.

## Snelle antwoorden
- **Wat doet een Niveausaanpassingslaag?** Hij wijzigt het toonbereik van een afbeelding niet‑destructief.  
- **Welke bibliotheek wordt gebruikt?** Aspose.PSD voor Java.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor ontwikkeling; een licentie is vereist voor productie.  
- **Hoe lang duurt de implementatie?** Ongeveer 10‑15 minuten voor een basisaanpassing.  
- **Kan ik meerdere kanalen aanpassen?** Ja, je kunt invoer‑/uitvoerniveaus voor elk kleurkanaal afzonderlijk instellen.

## Wat is een Niveausaanpassingslaag?
Een Niveausaanpassingslaag stelt je in staat de toonbalans van een afbeelding te corrigeren door invoerschaduwen, middentonen en hooglichten evenals uitvoerniveaus aan te passen. Omdat hij op een eigen laag staat, kun je de zichtbaarheid in- of uitschakelen of de laag verwijderen zonder invloed op de onderliggende artwork.

## Waarom een Niveausaanpassingslaag toevoegen met Aspose.PSD?
- **Automatisering:** Integreer toonaanpassingen in batch‑verwerkingspijplijnen.  
- **Cross‑platform:** Werkt op elk besturingssysteem dat Java ondersteunt.  
- **Precisie:** Toegang tot de instellingen van elk kanaal programmatically voor exacte resultaten.  

## Voorvereisten
1. Java Development Kit (JDK). Als je die niet hebt, download hem van de [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) of gebruik OpenJDK.  
2. Aspose.PSD voor Java‑bibliotheek – haal de nieuwste JAR op via deze [download link](https://releases.aspose.com/psd/java/).  
3. Basiskennis van Java‑programmeren.  
4. Een IDE zoals IntelliJ IDEA, Eclipse of NetBeans met de Aspose.PSD‑JAR toegevoegd aan het classpath van het project.

## Pakketten importeren
Voordat we beginnen met het schrijven van onze code, moeten we de benodigde pakketten uit de Aspose.PSD‑bibliotheek importeren. Zo doe je dat:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Deze imports geven ons toegang tot klassen voor het laden van PSD‑bestanden, werken met niveausaanpassingslagen en het manipuleren van individuele kanaalinstellingen.

## Hoe niveaus aanpassen in een PSD‑bestand
Hieronder vind je een stapsgewijze handleiding die precies laat **hoe je niveaus kunt aanpassen** programmatically.

### Stap 1: Stel je bestands‑paden in
Definieer waar de bron‑PSD zich bevindt en waar het bewerkte bestand moet worden opgeslagen.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
Vervang `"Your Document Directory"` door de daadwerkelijke map op jouw computer.

### Stap 2: Laad het PSD‑bestand
Maak een `PsdImage`‑instantie aan vanuit het bronbestand.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
Nu heb je volledige toegang tot alle lagen binnen de PSD.

### Stap 3: Doorloop de lagen
Zoek de Niveausaanpassingslaag die je wilt wijzigen.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
De `instanceof LevelsLayer`‑controle zorgt ervoor dat we alleen met niveausaanpassingslagen werken.

### Stap 4: Pas de kanaalinstellingen van de niveaus aan
Stel de invoer‑ en uitvoerwaarden in voor het geselecteerde kanaal.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
- **Invoermiddentoon‑niveau:** Verplaatst het middentoonbereik.  
- **Invoerschaduw‑niveau:** Maakt schaduwen donkerder of lichter.  
- **Invoerhooglicht‑niveau:** Regelt de helderste delen.  
- **Uitvoerschaduw/‑hooglicht‑niveaus:** Bepalen het uiteindelijke uitvoerbereik.

Voel je vrij om met verschillende waarden te experimenteren om te zien hoe ze de afbeelding beïnvloeden.

### Stap 5: Sla het gewijzigde PSD‑bestand op
Sla je wijzigingen op in een nieuw bestand.
```java
im.save(psdPathAfterChange);
```
Je vindt de bijgewerkte PSD op de locatie die je hebt opgegeven in `psdPathAfterChange`.

## Veelvoorkomende problemen en oplossingen
- **Bestand niet gevonden:** Controleer of `dataDir` naar de juiste map wijst en of de bron‑PSD bestaat.  
- **ClassCastException:** Zorg ervoor dat het bestand dat je laadt inderdaad een PSD is; andere formaten vereisen andere klassen.  
- **Licentiefouten:** Gebruik een geldige Aspose.PSD‑licentie voor productie‑builds; de proefversie werkt voor ontwikkeling.

## Conclusie
Je weet nu **hoe je niveaus kunt aanpassen** door een Niveausaanpassingslaag toe te voegen en te configureren in een PSD‑bestand met Aspose.PSD voor Java. Deze techniek geeft je nauwkeurige controle over de toonbalans terwijl je workflow volledig geautomatiseerd blijft. Blijf experimenteren met verschillende kanaalwaarden en verken batch‑verwerking om dezelfde aanpassingen op meerdere afbeeldingen toe te passen.

## Veelgestelde vragen

**Q: Wat is een Niveausaanpassingslaag?**  
A: Het is een niet‑destructieve laag die je in staat stelt het toonbereik (schaduwen, middentonen, hooglichten) van een afbeelding te wijzigen.

**Q: Kan ik Aspose.PSD gebruiken zonder een licentie aan te schaffen?**  
A: Ja, je kunt de bibliotheek evalueren met een gratis proefversie, maar een licentie is vereist voor commerciële inzet.

**Q: Waar vind ik documentatie voor Aspose.PSD?**  
A: Je kunt de documentatie vinden [hier](https://reference.aspose.com/psd/java/).

**Q: Is er community‑ondersteuning voor Aspose‑producten?**  
A: Absoluut! Je kunt vragen stellen en hulp krijgen in het [Aspose‑forum](https://forum.aspose.com/c/psd/34).

**Q: Hoe kan ik een tijdelijke licentie voor Aspose.PSD krijgen?**  
A: Je kunt een tijdelijke licentie aanvragen [hier](https://purchase.aspose.com/temporary-license/).

---

**Laatst bijgewerkt:** 2026-03-07  
**Getest met:** Aspose.PSD nieuwste versie (Java)  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}