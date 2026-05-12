---
date: 2026-02-22
description: Leer hoe je een vectormasker in Java maakt met Aspose.PSD voor Java,
  een vectormasker aan een PSD toevoegt en Vmsk‑resources programmatisch manipuleert.
linktitle: Create Vector Mask Java – Vmsk Resource in PSD Files
second_title: Aspose.PSD Java API
title: Vectormask maken in Java – Vmsk‑resource in PSD‑bestanden
url: /nl/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vectormask Java maken – Vmsk‑resource in PSD‑bestanden

## Inleiding
Als je **vectormaskers** (Vmsk) wilt **maken** in Photoshop‑bestanden (PSD), biedt Aspose.PSD voor Java een nette, programmeerbare manier om dit te doen. Of je nu een design‑automatiseringstool bouwt of aangepaste maskers toevoegt aan een bestaande grafische pijplijn, deze tutorial leidt je door elke stap – het laden van een PSD, het lezen van de Vmsk‑resource, het aanpassen van de eigenschappen en het opslaan van het resultaat. Aan het einde kun je vectormaskers verwerken, PSD naar PNG converteren en het bestand uitbreiden met extra vectordata – alles met **create vector mask java**‑technieken.

## Snelle antwoorden
- **Wat is een Vmsk‑resource?** Het is de vectormaskergegevens die in een PSD‑bestand zijn opgeslagen en complexe vectorvormen voor een laag definiëren.  
- **Welke bibliotheek ondersteunt dit?** Aspose.PSD voor Java biedt volledige lees‑/schrijftoegang tot Vmsk‑resources.  
- **Heb ik een licentie nodig?** Er is een gratis proefversie beschikbaar; een commerciële licentie is vereist voor productiegebruik.  
- **Kan ik de bewerkte PSD naar PNG converteren?** Ja – na het opslaan kun je de PSD laden en exporteren naar PNG met dezelfde API.  
- **Is Maven‑ondersteuning beschikbaar?** Absoluut; Aspose.PSD kan worden toegevoegd als Maven‑dependency (zie het trefwoord “aspose psd maven”).

## Wat is een vectormasker (Vmsk‑resource)?
Een vectormasker (Vmsk) is een niet‑pixel‑gebaseerd masker dat Bézier‑curves en pad‑records gebruikt om transparante en ondoorzichtige gebieden op een laag te definiëren. Omdat het vector‑gebaseerd is, schaalt het zonder kwaliteitsverlies – perfect voor hoge resolutie‑graphics.

## Waarom een vectormasker maken met Aspose.PSD?
- **Automatisering:** Programmeerbaar maskers toevoegen of wijzigen zonder Photoshop te openen.  
- **Consistentie:** Zorg dat elke gegenereerde PSD dezelfde maskerrichtlijnen volgt.  
- **Cross‑platform:** Werkt op elk OS dat Java ondersteunt.  
- **Integratie:** Combineer met andere Aspose‑API’s (bijv. PSD → PNG) voor end‑to‑end‑workflows.  
- **Schaalbaarheid:** Vectormaskers blijven scherp op elke grootte, ideaal voor responsieve ontwerpen.

## Waarom dit belangrijk is voor Java‑ontwikkelaars
Met **create vector mask java**‑technieken kun je geavanceerde grafische logica direct in back‑end services, CI‑pipelines of desktop‑hulpmiddelen embedden. Je hebt geen ontwerper meer nodig die handmatig maskers toevoegt; je code kan ze on‑the‑fly genereren of aanpassen, waardoor tijd wordt bespaard en menselijke fouten worden verminderd.

## Voorvereisten
Voordat we in de code duiken, zorg dat je het volgende hebt:

### Wat je nodig hebt
- Java Development Kit (JDK): Zorg dat JDK op je machine geïnstalleerd is. Zo niet, download het van de [Oracle‑website](https://www.oracle.com/java/technologies/javase-downloads.html).  
- Aspose.PSD voor Java‑bibliotheek: Een krachtige bibliotheek voor het beheren van PSD‑bestanden. Download deze van de [Aspose‑release‑pagina](https://releases.aspose.com/psd/java/). Voor wie eerst wil proberen, kun je ook starten met de [gratis proefversie](https://releases.aspose.com/).  
- Een IDE: Elke Java‑IDE (zoals IntelliJ IDEA, Eclipse, enz.) werkt voor dit project.

### Je werkruimte instellen
1. **Maak een nieuw Java‑project** – Open je favoriete IDE en start een nieuw project.  
2. **Voeg de Aspose‑bibliotheek toe** – Na het downloaden van de Aspose‑JAR, voeg je deze toe aan het build‑path van je project zodat je toegang hebt tot alle PSD‑gerelateerde klassen.

Met de omgeving klaar, gaan we verder met de daadwerkelijke implementatie.

## Hoe vectormasker maken in PSD‑bestanden met Java
Hieronder vind je een stap‑voor‑stap‑gids. De code‑blokken blijven ongewijzigd; we hebben alleen verklarende tekst toegevoegd om elke stap glashelder te maken.

### Pakketten importeren
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

### Stap 1: Laad je PSD‑bestand
Het eerste wat je doet, is je PSD‑bestand laden. Hier begint de magie.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- We stellen `dataDir` in op de map van je PSD‑bestand.  
- We maken een string `sourceFileName`, waarbij we de map combineren met de bestandsnaam van de PSD.  
- Ten slotte laden we het PSD‑bestand in een `PsdImage`‑object met `Image.load()`.

### Stap 2: Haal de Vmsk‑resource op
Nu de PSD‑afbeelding geladen is, halen we de Vmsk‑resource op.

```java
VmskResource resource = getVmskResource(im);
```

- We roepen de methode `getVmskResource()` aan, die zoekt en de Vmsk‑resource uit het beeld haalt.

### Stap 3: Valideer Vmsk‑resource‑eigenschappen
Voordat we wijzigingen aanbrengen, is het essentieel te controleren of de Vmsk‑resource in de verwachte staat verkeert.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Hier controleren we verschillende eigenschappen van de Vmsk‑resource. We willen zeker weten dat deze niet uitgeschakeld, omgekeerd of niet gekoppeld is, en dat het juiste aantal paden aanwezig is.

### Stap 4: Toegang tot elk pad en validatie
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

- We extraheren drie specifieke pad‑records en valideren hun typen en eigenschappen om te bevestigen dat ze aan onze criteria voldoen.

### Stap 5: De Vmsk‑resource bewerken
Nu komen we bij het wijzigingsgedeelte! Je kunt de eigenschappen van de Vmsk‑resource aanpassen waar nodig.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- In dit blok schakelen we verschillende eigenschappen van de Vmsk‑resource om. Door ze op `true` te zetten, kun je bepalen hoe het masker zich gedraagt in het PSD‑bestand.

### Stap 6: De Bézier‑knoop‑punten aanpassen
Bézier‑knopen zijn cruciaal voor vectorpaden. Laten we hier enkele waarden wijzigen.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- We benaderen specifieke `BezierKnotRecord`‑paden en wijzigen hun punten om de vectormasker mogelijk te hervormen.

### Stap 7: Het gewijzigde PSD‑bestand opslaan
Zodra alle bewerkingen voltooid zijn, is het tijd om het aangepaste PSD‑bestand op te slaan.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- We stellen het pad voor het geëxporteerde PSD‑bestand in en roepen vervolgens `im.save()` aan om de wijzigingen naar dit nieuwe bestand te schrijven.

### Stap 8: Resources opruimen
Tot slot moeten we ervoor zorgen dat we het beeld correct vrijgeven om resources te besparen.

```java
im.dispose();
```

- Het is altijd een goede gewoonte om resources te disposen zodra je klaar bent. Dit helpt geheugenlekken in je applicaties te voorkomen.

## Veelvoorkomende problemen en oplossingen
| Probleem | Waarom het gebeurt | Hoe op te lossen |
|----------|--------------------|------------------|
| **`VmskResource` niet gevonden** | De PSD bevat geen vectormasker‑laag. | Controleer of de bron‑PSD een vectormasker heeft of voeg er handmatig één toe in Photoshop voordat je de code uitvoert. |
| **`ArrayIndexOutOfBoundsException` bij pad‑toegang** | Het verwachte aantal pad‑records verschilt. | Inspecteer `resource.getPaths().length` en pas het indexgebruik dienovereenkomstig aan. |
| **Licentie‑exception** | Uitvoeren zonder een geldige Aspose.PSD‑licentie. | Pas een proef‑ of aangekochte licentie toe met `License license = new License(); license.setLicense("Aspose.PSD.lic");`. |
| **Geheugenlek** | Afbeelding niet disposed in langdurige processen. | Roep altijd `im.dispose()` aan in een `finally`‑block of gebruik try‑with‑resources indien ondersteund. |

## Veelgestelde vragen

**V: Hoe voeg ik een nieuw vectormasker toe aan een bestaande laag?**  
A: Maak een `VmskResource`, vul deze met de benodigde pad‑records (bijv. `BezierKnotRecord`) en koppel hem aan de resources‑collectie van de laag.

**V: Kan ik de bewerkte PSD direct naar PNG converteren zonder Photoshop te openen?**  
A: Ja – na het opslaan laad je de PSD opnieuw met `Image.load()` en roep je `im.save("output.png")` aan, waarbij je het PNG‑formaat specificeert.

**V: Is er een manier om dit te automatiseren in een CI/CD‑pipeline?**  
A: Absoluut. Omdat het proces puur Java is, kun je het in Maven/Gradle‑builds, Docker‑containers of elke CI‑omgeving die Java ondersteunt integreren.

**V: Welke versies van Aspose.PSD zijn compatibel met Java 11+?**  
A: Alle recente releases (2024‑2025) ondersteunen Java 8 en hoger, inclusief Java 11, 17 en nieuwere LTS‑versies.

**V: Heb ik een licentie nodig voor ontwikkel‑builds?**  
A: Een gratis evaluatielicentie werkt voor ontwikkeling en testen. Voor productie‑implementaties is een commerciële licentie vereist.

---

**Laatst bijgewerkt:** 2026-02-22  
**Getest met:** Aspose.PSD 24.11 voor Java  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}