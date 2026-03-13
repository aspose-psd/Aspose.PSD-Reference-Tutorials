---
date: 2026-03-13
description: Learn how to add hue saturation layer to PSD files using Aspose.PSD for
  Java. This guide also shows how to batch process PSD files and create hue adjustment
  layer programmatically.
linktitle: Add Hue Saturation Layer to PSD
second_title: Aspose.PSD Java API
title: Hue Saturation‑laag toevoegen aan PSD met Aspose.PSD voor Java
url: /nl/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hue Saturation Layer toevoegen aan PSD

## Inleiding
Als het gaat om grafisch ontwerp, speelt kleurmanipulatie een cruciale rol—specifiek, het aanpassen van hue, saturation en lightness kan de sfeer en kwaliteit van een afbeelding drastisch veranderen. Een effectieve manier om dit te bereiken is via aanpassingslagen in Photoshop (PSD‑bestanden). Als je **add hue saturation layer** programmatically wilt toevoegen met Java, staat de Aspose.PSD‑bibliotheek voor je klaar! Deze tutorial leidt je stap voor stap door het toevoegen van een Hue Saturation Adjustment Layer aan je PSD‑bestanden, waardoor je workflow productiever en efficiënter wordt.

## Snelle antwoorden
- **Welke bibliotheek stelt je in staat om een hue saturation layer toe te voegen in Java?** Aspose.PSD for Java.  
- **Moet ik Photoshop geïnstalleerd hebben?** Nee, de bibliotheek werkt onafhankelijk van Photoshop.  
- **Kan ik PSD‑bestanden batchgewijs verwerken met deze aanpak?** Ja—zodra je de stappen automatiseert, kun je ze op veel bestanden toepassen.  
- **Welke Java‑versie is vereist?** JDK 8 of later.  
- **Is een licentie nodig voor productiegebruik?** Ja, een commerciële licentie is vereist na de proefperiode.

## Wat is een “add hue saturation layer” bewerking?
Een **add hue saturation layer** bewerking creëert een niet‑destructieve aanpassingslaag waarmee je hue, saturation en lightness kunt wijzigen zonder de originele pixelgegevens te veranderen. Dit is ideaal voor het fijn afstellen van kleuren over een volledige compositie of specifieke kleurbereiken.

## Waarom Aspose.PSD voor Java gebruiken?
- **Geen Photoshop‑afhankelijkheid** – werkt op elk platform dat Java ondersteunt.  
- **Volledige PSD‑getrouwheid** – behoudt alle laag‑informatie, maskers en effecten.  
- **Batch‑klaar** – je kunt door mappen itereren en dezelfde aanpassing op tientallen bestanden toepassen.  
- **Prestatie‑gericht** – geoptimaliseerd voor grote documenten en server‑side automatisering.

## Vereisten
Voordat we in de code duiken, zorg dat je het volgende hebt:

1. **Java Development Kit (JDK):** Zorg ervoor dat je JDK 8 of hoger op je machine geïnstalleerd hebt. Je kunt het downloaden via de [Java SE Development Kit Downloads](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java Library:** Je hebt de Aspose.PSD‑bibliotheek nodig, die je [hier kunt downloaden](https://releases.aspose.com/psd/java/).  
3. **IDE:** Een geschikte Integrated Development Environment (IDE) zoals IntelliJ IDEA of Eclipse voor Java‑ontwikkeling.  
4. **Basiskennis van Java:** Vertrouwdheid met Java‑programmeren is een plus, maar maak je geen zorgen—we lopen elke regel met je door.

Nu we onze vereisten op orde hebben, gaan we verder met het leuke deel—coderen!

## Pakketten importeren
Om met de Aspose.PSD‑bibliotheek te werken, is de eerste stap het importeren van de benodigde klassen. Zo doe je dat in je Java‑bestand:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```

Zorg ervoor dat de juiste bibliotheken aan je project zijn toegevoegd zodat deze imports naadloos werken.

## Stap 1: Stel je documentmap in
Elk project heeft een startpunt nodig, en dat geldt ook voor ons. Je moet een map opgeven waar je PSD‑bestanden zijn opgeslagen. Dit is cruciaal voor het correct laden en opslaan van afbeeldingen.

```java
String dataDir = "Your Document Directory"; // Update this path to your actual directory
```

## Stap 2: Laad een bestaand PSD‑bestand
Om een bestaand PSD‑bestand te manipuleren, moeten we het eerst in ons programma laden. Zo doe je dat:

```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

In deze code, werk `"HueSaturationAdjustmentLayer.psd"` bij naar de naam van jouw bestaande PSD‑bestand dat je wilt bewerken.

## Stap 3: Bewerk de Hue/Saturation‑laag
Vervolgens doorlopen we de lagen van onze geladen PSD‑afbeelding om eventuele bestaande Hue/Saturation‑lagen te vinden en te bewerken. Deze stap omvat het aanpassen van de hue-, saturation- en lightness‑waarden.

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
- We passen de hue aan naar **-25**, de saturatie naar **-12**, en de lichtheid naar **+67**.  
- De `getRange(2)`‑methode stelt ons in staat om specifieke kleurbereiken naar wens bij te stellen.

## Stap 4: Sla het gewijzigde PSD‑bestand op
Na het maken van de aanpassingen is de volgende stap het bestand opslaan. Dit is een essentieel onderdeel van ons proces, zodat de aangebrachte wijzigingen niet verloren gaan.

```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```

## Stap 5: Voeg een nieuwe Hue/Saturation‑laag toe
Als je een **create hue adjustment layer** vanaf nul wilt maken, kun je een gloednieuwe Hue/Saturation‑aanpassingslaag toevoegen aan een ander PSD‑bestand. Volg hetzelfde laadpatroon maar gebruik de `addHueSaturationAdjustmentLayer()`‑methode.

```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```

## Stap 6: Stel nieuwe Hue/Saturation‑waarden in voor de nieuwe laag
Nu je deze nieuwe laag hebt aangemaakt, pas je de gewenste hue-, saturation- en lightness‑instellingen toe, net als eerder.

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

## Stap 7: Sla het bijgewerkte PSD‑bestand op
Sla tenslotte het PSD‑bestand op met de toegevoegde Hue/Saturation‑laag zodat je je wijzigingen kunt zien.

```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```

Gefeliciteerd! Je hebt met succes PSD‑bestanden gemanipuleerd met Aspose.PSD for Java. Nu kun je experimenteren met verschillende afbeeldingen en diepere aanpassingen, waardoor je grafische ontwerpprojecten tot leven komen.

## Hoe PSD‑bestanden batchgewijs verwerken met hue‑aanpassingen
Omdat de bovenstaande code volledig scriptbaar is, kun je de hele reeks in een lus plaatsen die over elk `.psd`‑bestand in een map itereren. Dit stelt je in staat om **batch process psd files** uit te voeren en dezelfde hue-, saturation- en lightness‑aanpassingen in één run toe te passen—perfect voor grootschalige merkupdates.

## Veelvoorkomende problemen en oplossingen
- **NullPointerException bij het laden van een bestand:** Controleer of `dataDir` eindigt op de juiste bestands‑separator (`/` of `\`) en of de bestandsnaam correct is.  
- **Aanpassingswaarden buiten bereik:** Hue, saturation en lightness accepteren waarden van -255 tot 255. Houd je getallen binnen dit bereik.  
- **Laag niet gevonden:** Als de PSD geen Hue/Saturation‑laag bevat, zal de `instanceof`‑controle het blok overslaan. Gebruik `addHueSaturationAdjustmentLayer()` om er eerst een te maken.

## Veelgestelde vragen

**Q: Wat is een Hue Saturation Adjustment Layer?**  
A: Het stelt je in staat om de kleur‑eigenschappen van een afbeelding te wijzigen zonder de originele pixels permanent te veranderen.

**Q: Moet ik Photoshop geïnstalleerd hebben om Aspose.PSD te gebruiken?**  
A: Nee, Aspose.PSD is een zelfstandige bibliotheek die onafhankelijk van Photoshop werkt.

**Q: Kan ik Aspose.PSD gebruiken voor batchverwerking?**  
A: Ja, je kunt meerdere PSD‑bestanden automatiseren en batchgewijs verwerken met Aspose.PSD.

**Q: Is Aspose.PSD gratis?**  
A: Aspose.PSD biedt een gratis proefversie, maar een licentie is vereist voor langdurig gebruik. Je kunt de prijzen bekijken [hier](https://purchase.aspose.com/buy).

## Conclusie
Werken met graphics programmatically opent een wereld aan mogelijkheden. Het gebruik van Aspose.PSD for Java om **add hue saturation layer** en om **create hue adjustment layer** toe te voegen biedt flexibiliteit en efficiëntie die je ontwerp‑workflow kan stroomlijnen. Of je nu foto’s voor een project verbetert of verbluffende visuele content maakt, het beheersen van deze tools kan je output aanzienlijk verbeteren.

Voel je vrij om meer functionaliteiten van Aspose.PSD te verkennen door te duiken in de [documentation](https://reference.aspose.com/psd/java/) of overweeg een [temporary license](https://purchase.aspose.com/temporary-license/) aan te schaffen om de volledige kracht van de bibliotheek te testen.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Laatst bijgewerkt:** 2026-03-13  
**Getest met:** Aspose.PSD for Java 24.12 (latest op moment van schrijven)  
**Auteur:** Aspose