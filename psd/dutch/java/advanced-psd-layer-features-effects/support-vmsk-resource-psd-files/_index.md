---
date: 2025-12-18
description: Leer hoe je een vectormasker (Vmsk‑resource) maakt in PSD‑bestanden met
  Aspose.PSD voor Java. Deze stapsgewijze tutorial laat je zien hoe je een vectormasker
  toevoegt, PSD naar PNG converteert en meer.
linktitle: Create Vector Mask (Vmsk Resource) in PSD Files with Java
second_title: Aspose.PSD Java API
title: Vectormask (Vmsk‑resource) aanmaken in PSD‑bestanden met Java
url: /nl/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vectormask maken (Vmsk‑resource) in PSD‑bestanden met Java

## Inleiding
Als je **vectormaskers** (Vmsk) wilt **maken** in Photoshop‑bestanden (PSD), biedt Aspose.PSD voor Java een nette, programmeerbare manier om dit te doen. Of je nu een design‑automatiseringstool bouwt of aangepaste maskersondersteuning toevoegt aan een bestaande grafische pijplijn, deze tutorial leidt je stap voor stap – van het laden van een PSD, het lezen van de Vmsk‑resource, het aanpassen van de eigenschappen, tot het opslaan van het resultaat. Aan het einde kun je vectormaskers verwerken, PSD naar PNG converteren en het bestand uitbreiden met extra vector‑data.

## Snelle antwoorden
- **Wat is een Vmsk‑resource?** Het is de vectormaskergegevens die in een PSD‑bestand zijn opgeslagen en complexe vectorvormen voor een laag definiëren.  
- **Welke bibliotheek ondersteunt dit?** Aspose.PSD voor Java biedt volledige lees‑/schrijftoegang tot Vmsk‑resources.  
- **Heb ik een licentie nodig?** Er is een gratis proefversie beschikbaar; een commerciële licentie is vereist voor productiegebruik.  
- **Kan ik de bewerkte PSD naar PNG converteren?** Ja – zodra deze is opgeslagen, kun je de PSD laden en exporteren naar PNG met dezelfde API.  
- **Is Maven‑ondersteuning beschikbaar?** Absoluut; Aspose.PSD kan als Maven‑dependency worden toegevoegd (zie trefwoord “aspose psd maven”).

## Wat is een vectormasker (Vmsk‑resource)?
Een vectormasker (Vmsk) is een niet‑pixel‑gebaseerd masker dat Bézier‑curves en pad‑records gebruikt om transparante en ondoorzichtige gebieden op een laag te definiëren. Omdat het vector‑gebaseerd is, schaalt het zonder kwaliteitsverlies – perfect voor hoge resolutie‑graphics.

## Waarom een vectormasker maken met Aspose.PSD?
- **Automatisering:** Programma‑matig maskers toevoegen of wijzigen zonder Photoshop te openen.  
- **Consistentie:** Zorg ervoor dat elke gegenereerde PSD dezelfde maskerrichtlijnen volgt.  
- **Cross‑platform:** Werkt op elk OS dat Java ondersteunt.  
- **Integratie:** Combineer met andere Aspose‑API’s (bijv. PSD → PNG) voor end‑to‑end‑workflows.

## Voorvereisten
Voordat we in de code duiken, zorg dat je het volgende hebt:

### Wat je nodig hebt
- Java Development Kit (JDK): Zorg dat je JDK op je machine geïnstalleerd hebt. Zo niet, download het van de [Oracle‑website](https://www.oracle.com/java/technologies/javase-downloads.html).  
- Aspose.PSD voor Java‑bibliotheek: Een krachtige bibliotheek voor het beheren van PSD‑bestanden. Download het van de [Aspose‑release‑pagina](https://releases.aspose.com/psd/java/). Voor wie eerst wil proberen, kun je ook starten met de [gratis proefversie](https://releases.aspose.com/).  
- Een IDE: Elke Java‑IDE (zoals IntelliJ IDEA, Eclipse, enz.) werkt voor dit project.

### Je werkruimte instellen
1. **Maak een nieuw Java‑project** – Open je favoriete IDE en start een nieuw project.  
2. **Voeg de Aspose‑bibliotheek toe** – Na het downloaden van de Aspose‑JAR, voeg je deze toe aan het build‑path van je project zodat je toegang hebt tot alle PSD‑gerelateerde klassen.

Met de omgeving klaar, gaan we verder met de daadwerkelijke implementatie.

## Hoe maak je een vectormasker in PSD‑bestanden met Java
Hieronder vind je een stap‑voor‑stap‑gids. De code‑blokken zijn onveranderd ten opzichte van de originele tutorial; we hebben alleen verklarende tekst toegevoegd om elke stap glashelder te maken.

## Pakketten importeren
Voordat we met PSD‑bestanden kunnen werken, moeten we de benodigde klassen uit de Aspose.PSD‑bibliotheek importeren.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```

Nu we de basis hebben gelegd, lopen we elke bewerking door.

## Stap 1: Laad je PSD‑bestand
Het eerste wat je moet doen is je PSD‑bestand laden. Hier begint de magie.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- We stellen `dataDir` in op de map van je PSD‑bestand.  
- We maken een string `sourceFileName`, waarbij we de map combineren met de bestandsnaam van de PSD.  
- Ten slotte laden we het PSD‑bestand in een `PsdImage`‑object met `Image.load()`.

## Stap 2: Haal de Vmsk‑resource op
Nu we onze PSD‑afbeelding geladen hebben, halen we de Vmsk‑resource op.

```java
VmskResource resource = getVmskResource(im);
```

- We roepen de methode `getVmskResource()` aan, die zoekt en de Vmsk‑resource uit het beeld haalt.

## Stap 3: Valideer de eigenschappen van de Vmsk‑resource
Voordat we wijzigingen aanbrengen, is het essentieel te controleren of onze Vmsk‑resource zich in de verwachte staat bevindt.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Hier controleren we verschillende eigenschappen van de Vmsk‑resource. We willen zeker weten dat deze niet uitgeschakeld, omgekeerd of niet gekoppeld is, en dat het juiste aantal paden bevat.

## Stap 4: Toegang tot elk pad en validatie
Laten we iets dieper graven en de paden binnen de Vmsk‑resource inspecteren.

```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- We extraheren drie specifieke pad‑records en valideren hun types en eigenschappen om te verzekeren dat ze aan onze criteria voldoen.

## Stap 5: Bewerk de Vmsk‑resource
Nu komen we bij het wijzigingsgedeelte! Je kunt de eigenschappen van de Vmsk‑resource aanpassen zoals nodig.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- In dit blok schakelen we verschillende eigenschappen van de Vmsk‑resource om. Door ze op `true` te zetten, kun je bepalen hoe het masker zich gedraagt in het PSD‑bestand.

## Stap 6: Pas de Bézier‑knooppunten aan
Bézier‑knopen zijn cruciaal voor vectorpaden. Laten we hier enkele waarden wijzigen.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- We benaderen specifieke `BezierKnotRecord`‑paden en wijzigen hun punten om de vectormasker mogelijk te hervormen.

## Stap 7: Sla het gewijzigde PSD‑bestand op
Zodra alle bewerkingen voltooid zijn, is het tijd om het gewijzigde PSD‑bestand op te slaan.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- We stellen het pad in voor het geëxporteerde PSD‑bestand en roepen vervolgens `im.save()` aan om de wijzigingen naar dit nieuwe bestand te schrijven.

## Stap 8: Ruim bronnen op
Tot slot moeten we ervoor zorgen dat we de afbeelding correct vrijgeven om bronnen te besparen.

```java
im.dispose();
```

- Het is altijd een goede gewoonte om gebruikte bronnen te disposen zodra je klaar bent. Dit helpt geheugenlekken in je applicaties te voorkomen.

## Conclusie
Gefeliciteerd! Je hebt zojuist een gedetailleerd proces doorlopen voor het **maken van vectormaskers** (Vmsk) in PSD‑bestanden met Aspose.PSD voor Java. Van het laden van de afbeelding, het ophalen en valideren van de Vmsk‑resource, het bewerken van de eigenschappen, tot het opslaan van je gewijzigde PSD, je hebt nu een stevige basis voor het automatiseren van vectormasker‑workflows. Gebruik deze technieken om je design‑pijplijnen te verrijken, te integreren met andere Aspose‑API’s (zoals PSD → PNG), of om aangepaste grafische tools te bouwen.

## Veelgestelde vragen
**Q: Hoe voeg ik een nieuw vectormasker toe aan een bestaande laag?**  
A: Maak een `VmskResource`, vul deze met de benodigde pad‑records (bijv. `BezierKnotRecord`), en koppel hem aan de resources‑collectie van de laag.

**Q: Kan ik de bewerkte PSD direct naar PNG converteren zonder Photoshop te openen?**  
A: Ja – na het opslaan van de PSD laad je deze opnieuw met `Image.load()` en roep je `im.save("output.png")` aan met het PNG‑formaat.

**Q: Is er een manier om dit te automatiseren in een CI/CD‑pipeline?**  
A: Absoluut. Omdat het proces puur Java is, kun je het in Maven/Gradle‑builds, Docker‑containers of elke CI‑omgeving die Java ondersteunt, integreren.

**Q: Welke versies van Aspose.PSD zijn compatibel met Java 11+?**  
A: Alle recente releases (2024‑2025) ondersteunen Java 8 en hoger, inclusief Java 11, 17 en nieuwere LTS‑versies.

**Q: Heb ik een licentie nodig voor ontwikkel‑builds?**  
A: Een gratis evaluatielicentie werkt voor ontwikkeling en testen. Voor productie‑implementaties is een commerciële licentie vereist.

---

**Laatst bijgewerkt:** 2025-12-18  
**Getest met:** Aspose.PSD 24.11 voor Java  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
