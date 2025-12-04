---
date: 2025-12-04
description: Leer hoe je een PSD als PNG opslaat en een rendering dropshadow toepast
  met Aspose.PSD voor Java. Deze gids behandelt hoe je een schaduw toevoegt, een PSD
  naar PNG converteert en een dropshadow toepast in Java.
language: nl
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: PSD opslaan als PNG & slagschaduw toevoegen met Aspose.PSD Java
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD opslaan als PNG & Drop Shadow toevoegen met Aspose.PSD Java

## Inleiding

Als je met Photoshop‑bestanden in Java werkt, is **PSD opslaan als PNG** terwijl je een professioneel uitziende drop shadow toevoegt een veelvoorkomende eis. Aspose.PSD maakt deze taak eenvoudig, zodat je **PSD naar PNG kunt converteren** en **drop shadow Java** kunt toepassen in slechts een paar regels code. In deze tutorial lopen we het volledige proces door, van het laden van een PSD‑bestand tot het exporteren van de uiteindelijke PNG met een gerenderd schaduweffect.

## Snelle antwoorden
- **Wat betekent “save PSD as PNG”?** Het converteert een gelaagd Photoshop‑bestand naar een plat PNG‑beeld, waarbij transparantie behouden blijft.  
- **Kan ik een drop shadow toevoegen tijdens het converteren?** Ja – Aspose.PSD laat je laag‑effecten aanpassen vóór export.  
- **Heb ik een licentie nodig om de code uit te voeren?** Een gratis proefversie werkt voor evaluatie; een licentie is vereist voor productie.  
- **Welke Java‑versie wordt ondersteund?** Java 8 of hoger.  
- **Is het drop‑shadow‑effect aanpasbaar?** Absoluut – je kunt kleur, dekking, afstand, grootte, hoek en meer aanpassen.

## Vereisten

Voordat we beginnen, zorg dat je het volgende hebt:

- **Java‑ontwikkelomgeving** – JDK 8 of nieuwer geïnstalleerd.  
- **Aspose.PSD‑bibliotheek** – Download de nieuwste JAR van de officiële site [here](https://releases.aspose.com/psd/java/).  
- **Een PSD‑bestand** – Een bestand dat minstens één laag bevat die je wilt verrijken met een schaduw.  

## Hoe sla je PSD op als PNG met een drop shadow in Java?

Hieronder vind je een stap‑voor‑stap‑gids. Elke stap bevat een korte uitleg gevolgd door de exacte code die je moet kopiëren.

### Stap 1: Importeer de vereiste pakketten

We beginnen met het importeren van de klassen die beeldladen, effectverwerking en PNG‑export mogelijk maken.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

### Stap 2: Definieer de documentmap

Stel de map in waar je bron‑PSD en de resulterende PNG zich bevinden.

```java
String dataDir = "Your Document Directory";
```

### Stap 3: Stel PSD‑ en PNG‑bestandspaden in

Geef de volledige paden op voor de invoer‑PSD en de uitvoer‑PNG.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Stap 4: Laad het PSD‑bestand met effecten ingeschakeld

Het inschakelen van **loadEffectsResource** zorgt ervoor dat laag‑effecten (zoals schaduwen) beschikbaar zijn voor bewerking.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Stap 5: Toegang tot het Drop Shadow‑effect

Hier halen we het eerste effect op dat is toegepast op de tweede laag (index 1). Hier lezen of wijzigen we de schaduwparameters.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Stap 6: Valideer de eigenschappen van het schaduweffect (optioneel maar handig)

Het controleren van de bestaande eigenschappen helpt je te bepalen of je iets moet aanpassen. De onderstaande asserts bevestigen de standaardwaarden.

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

> **Pro tip:** Als je **how to add shadow** met aangepaste instellingen wilt, wijzig dan de eigenschappen op `shadowEffect` vóór het opslaan (bijv. `shadowEffect.setColor(Color.getRed());`).

### Stap 7: Sla de gewijzigde afbeelding op als PNG

Tot slot exporteren we de PSD (met de gerenderde schaduw) naar een PNG‑bestand. De optie `TruecolorWithAlpha` behoudt transparantie.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

En daar heb je het – een volledige **convert PSD to PNG**‑workflow die ook **apply drop shadow java** in één stap uitvoert.

## Waarom Aspose.PSD voor deze taak gebruiken?

- **Geen native Photoshop vereist** – Werkt op elk platform dat Java ondersteunt.  
- **Volledige PSD‑getrouwheid** – Alle laag‑informatie, maskers en effecten blijven behouden.  
- **Fijnmazige controle** – Pas elk parameter van de drop shadow aan vóór export.  
- **Hoge prestaties** – Geoptimaliseerd voor grote bestanden en batchverwerking.

## Veelvoorkomende problemen & foutoplossing

| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| `NullPointerException` on `shadowEffect` | De doel‑laag heeft geen effecten of de index is onjuist. | Controleer de laag‑index (`im.getLayers()[i]`) en zorg dat er een effect bestaat. |
| Exported PNG is blank | PNG‑opties niet correct ingesteld of afbeelding niet opgeslagen. | Gebruik `PngColorType.TruecolorWithAlpha` en bevestig dat het pad in `im.save()` schrijfbaar is. |
| Shadow color is not visible | Schaduw‑opacity staat op 0 of de kleur komt overeen met de achtergrond. | Stel `shadowEffect.setOpacity(255);` in en kies een contrasterende kleur. |

## Veelgestelde vragen

**V: Kan ik drop shadows op meerdere lagen tegelijk toepassen?**  
A: Ja. Loop door `im.getLayers()` en wijzig elke laag’s `DropShadowEffect` naar behoefte.

**V: Wat doet de parameter ‘Spread’?**  
A: Het bepaalt hoe scherp de schaduw overgaat van volledig ondoorzichtig naar transparant. Een hogere spread geeft een hardere rand.

**V: Is Aspose.PSD compatibel met alle Photoshop‑versies?**  
A: Het ondersteunt een breed scala aan PSD‑versies, van vroege releases tot de nieuwste Photoshop CC‑bestanden.

**V: Hoe krijg ik hulp als ik tegen problemen aanloop?**  
A: Bezoek het [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) voor community‑ondersteuning en officiële assistentie.

**V: Kan ik Aspose.PSD eerst uitproberen voordat ik koop?**  
A: Absoluut. Download een gratis proefversie van de [Aspose website](https://releases.aspose.com/).

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Last Updated:** 2025-12-04  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose