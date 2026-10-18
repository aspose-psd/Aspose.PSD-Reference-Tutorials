---
date: 2026-10-18
description: Leer hoe je radial gradient-effecten kunt maken in Java-afbeeldingen
  met Aspose.PSD. Volg deze stap‑voor‑stap gids voor naadloze integratie.
keywords:
- create radial gradient java
- apply gradient overlay psd
- add radial gradient image
lastmod: 2026-10-18
linktitle: Gradient-effecten toevoegen
og_description: Leer hoe je radial gradient java-effecten maakt met Aspose.PSD. Deze
  tutorial laat zien hoe je gradient‑overlays kunt toevoegen, aanpassen en opslaan
  in enkele minuten.
og_image_alt: Screenshot of Aspose.PSD Java code creating a radial gradient effect
og_title: Radial gradient java maken met Aspose.PSD – stap‑voor‑stap gids
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  headline: How to create radial gradient effects in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  name: How to create radial gradient effects in Aspose.PSD for Java
  steps:
  - name: Load the PSD file and access the gradient overlay
    text: '`PsdLoadOptions` configures how a PSD file is loaded, allowing you to enable
      loading of effect resources. `Image.load` reads the file into an `Image` object.
      In this step, we load a PSD file and retrieve the first `GradientOverlayEffect`
      from the second layer (index 1). The `loadOptions.setLoadEffec'
  - name: Verify Initial Settings
    text: Before making changes, it’s a good practice to confirm the current blend
      mode, opacity, and visibility. This helps you understand the baseline state
      of the gradient overlay.
  - name: Modify Gradient Settings
    text: Here you can customize the gradient’s color, opacity, and blend mode. The
      example changes the color to green, reduces opacity to 193 (out of 255), and
      switches the blend mode to **Lighten**. Feel free to experiment with other `BlendMode`
      values such as `Multiply`, `Screen`, or `Overlay`.
  - name: Save the Edited Image
    text: After applying your modifications, persist the changes by saving the PSD
      to a new file. This step ensures the original file remains untouched.
  - name: Verify Changes
    text: The snippet above demonstrates how to open a PSD, pull the second layer’s
      first effect (assumed to be a gradient overlay), and prepare it for modification.
  - name: Verify the original settings (optional but recommended)
    text: Before you change anything, checking the existing blend mode, opacity, and
      visibility helps you understand the baseline. The `Assert` calls in the code
      confirm that the effect is currently set to **Normal** blend mode, fully opaque,
      and visible.
  - name: Adjust gradient properties to achieve a radial style
    text: 'You can change the gradient’s color, opacity, and blend mode. For a true
      radial effect, set the gradient style: *Pro tip:* Use `Color.getGreen()` or
      any `java.awt.Color` instance to define the start color, and `gradientOverlay.setColor2(Color.getBlue())`
      for the end color.'
  - name: Save the edited PSD
    text: Calling `im.save(exportPath);` writes the modified image to disk. The saved
      file retains the radial gradient overlay and can be opened in Photoshop, previewed
      in browsers, or converted to other formats.
  type: HowTo
- questions:
  - answer: Yes. Retrieve the layer’s `BlendingOptions`, iterate through the `Effects`
      collection, and add a new `GradientOverlayEffect` for each gradient you need.
    question: Can I apply multiple gradient effects to a single image?
  - answer: Aspose.PSD provides shadows, glows, bevels, and more. Each effect appears
      in the `Effects` array and can be configured independently.
    question: What other effects can I combine with gradient overlays?
  - answer: Verify that the PSD was loaded with `setLoadEffectsResource(true)`, check
      layer visibility, and confirm you are modifying the correct effect index.
    question: How can I troubleshoot if the effects are not rendering correctly?
  - answer: Yes, you can get a free trial [here](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [purchase page](https://purchase.aspose.com/buy) for licensing
      information.
    question: Where can I purchase a license for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create radial gradient
- gradient overlay effect
- Aspose.PSD Java
title: Hoe radial gradient-effecten te creëren in Aspose.PSD voor Java
url: /nl/java/advanced-image-effects/add-gradient-effects/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe radial gradient-effecten te maken in Aspose.PSD voor Java

## Introductie

In deze gids leer je hoe je **create radial gradient java**‑effecten maakt met de Aspose.PSD‑bibliotheek. Radiale gradients zijn perfect om diepte, focus of een subtiele gloed toe te voegen aan je PSD‑lagen zonder Photoshop te openen. Aan het einde van de tutorial kun je een PSD laden, een gradient‑overlay toepassen, de eigenschappen aanpassen en het resultaat opslaan — alles vanuit Java‑code.

## Snelle antwoorden
- **Wat kan ik bereiken?** Voeg radial gradient overlays toe, bewerk en meng ze op PSD‑lagen.  
- **Welke bibliotheek is vereist?** Aspose.PSD voor Java (nieuwste versie).  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor ontwikkeling; een commerciële licentie is vereist voor productie.  
- **Hoe lang duurt de implementatie?** Ongeveer 10‑15 minuten voor een basis radial gradient overlay.  
- **Is het compatibel met Java 8+?** Ja, de API ondersteunt Java 8 en nieuwere runtimes.

## Voorvereisten

Voordat we in de tutorial duiken, zorg ervoor dat je de volgende voorwaarden hebt vervuld:

1. **Aspose.PSD for Java Library** – Zorg ervoor dat je de Aspose.PSD for Java bibliotheek hebt gedownload en geïnstalleerd. Je kunt de bibliotheek en de documentatie vinden op de [Aspose.PSD Java documentation page](https://reference.aspose.com/psd/java/).  
2. **Java Development Environment** – Richt een Java‑ontwikkelomgeving in op je machine (JDK 8 of hoger, IDE naar keuze).  
3. **Latest Aspose.PSD release** – Download de meest recente versie vanaf de [Aspose releases page](https://releases.aspose.com/).  
4. **Support resources** – Als je problemen tegenkomt, raadpleeg dan het [Aspose.PSD Support forum](https://forum.aspose.com/c/psd/34).  
5. **License purchase** – Wanneer je klaar bent voor productie, verkrijg een licentie via de [purchase page](https://purchase.aspose.com/buy).

Nu je alles hebt ingesteld, gaan we verder met de stap‑voor‑stap gids.

## Wat is een gradient overlay effect?

Een gradient overlay effect schildert een vloeiende overgang tussen twee of meer kleuren over een geselecteerd gebied van een laag. In Photoshop kan dit effect worden gemengd, gekleurd en gepositioneerd om verfijnde visuele ontwerpen te creëren. De `GradientOverlayEffect`‑klasse is Aspose.PSD’s weergave van die laag‑stijl, met eigenschappen zoals kleurstops, doorzichtigheid, mengmodus en gradient‑stijl.

## Hoe radial gradient-effect te maken

Laad de PSD, lokaliseer de doel‑laag, pas de `GradientOverlayEffect`‑eigenschappen aan en sla vervolgens het bestand op. De volledige workflow past in vier beknopte regels Java‑code zodra de afbeelding is geladen.

### Stap 1: Laad het PSD‑bestand en krijg toegang tot de gradient overlay

`PsdLoadOptions` configureert hoe een PSD‑bestand wordt geladen, zodat je het laden van effect‑resources kunt inschakelen. `Image.load` leest het bestand in een `Image`‑object.

```javaString dataDir = "Your Document Directory";

// Gradient overlay effect. Example
String sourceFileName = dataDir + "GradientOverlay.psd";
String exportPath = dataDir + "GradientOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlay = (GradientOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

In deze stap laden we een PSD‑bestand en halen we de eerste `GradientOverlayEffect` op van de tweede laag (index 1). De aanroep `loadOptions.setLoadEffectsResource(true)` zorgt ervoor dat effect‑resources beschikbaar zijn voor bewerking.

### Stap 2: Controleer de initiële instellingen

```java
// Verify initial settings
Assert.areEqual(BlendMode.Normal, gradientOverlay.getBlendMode());
Assert.areEqual(255, gradientOverlay.getOpacity());
Assert.areEqual(true, gradientOverlay.isVisible());
// ... (additional verifications)
```

Voordat je wijzigingen aanbrengt, is het een goede gewoonte om de huidige mengmodus, doorzichtigheid en zichtbaarheid te bevestigen. Dit helpt je de basisstatus van de gradient overlay te begrijpen.

### Stap 3: Pas gradientinstellingen aan

```java
// Modify gradient settings
settings.setColor(Color.getGreen());
gradientOverlay.setOpacity((byte)193);
gradientOverlay.setBlendMode(BlendMode.Lighten);
// ... (additional modifications)
```

Hier kun je de kleur, doorzichtigheid en mengmodus van de gradient aanpassen. Het voorbeeld verandert de kleur naar groen, verlaagt de doorzichtigheid naar 193 (van 255), en schakelt de mengmodus naar **Lighten**. Voel je vrij om te experimenteren met andere `BlendMode`‑waarden zoals `Multiply`, `Screen` of `Overlay`.

### Stap 4: Sla de bewerkte afbeelding op

```java
// Save the edited image
im.save(exportPath);
```

Na het toepassen van je aanpassingen, bewaar je de wijzigingen door de PSD naar een nieuw bestand op te slaan. Deze stap zorgt ervoor dat het originele bestand onaangeroerd blijft.

### Stap 5: Verifieer wijzigingen

```java
// Verify changes after editing
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlayEffect = (GradientOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];
// ... (additional verifications)
```

Het fragment hierboven toont hoe je een PSD opent, het eerste effect van de tweede laag (verondersteld een gradient overlay te zijn) ophaalt en voorbereidt op bewerking.

### Stap 2: Controleer de oorspronkelijke instellingen (optioneel maar aanbevolen)

Voordat je iets wijzigt, helpt het controleren van de bestaande mengmodus, doorzichtigheid en zichtbaarheid je de basis te begrijpen. De `Assert`‑aanroepen in de code bevestigen dat het effect momenteel is ingesteld op **Normal** mengmodus, volledig ondoorzichtig en zichtbaar.

### Stap 3: Pas gradienteigenschappen aan om een radiale stijl te bereiken

Je kunt de kleur, doorzichtigheid en mengmodus van de gradient wijzigen. Voor een echte radiale gradient stel je de gradient‑stijl in:

```java
gradientOverlay.setGradientStyle(GradientStyle.Radial);
gradientOverlay.setAngle(0f); // angle is ignored for radial, but required by API
gradientOverlay.setScale(100f); // 100 % fills the layer
```

*Pro tip:* Gebruik `Color.getGreen()` of een andere `java.awt.Color`‑instantie om de startkleur te definiëren, en `gradientOverlay.setColor2(Color.getBlue())` voor de eindkleur.

### Stap 4: Sla de bewerkte PSD op

Het aanroepen van `im.save(exportPath);` schrijft de aangepaste afbeelding naar schijf. Het opgeslagen bestand behoudt de radiale gradient overlay en kan worden geopend in Photoshop, bekeken in browsers, of geconverteerd naar andere formaten.

## Waarom radial gradient overlays maken?

Radiale gradients voegen diepte en focus toe aan ontwerpen, waardoor elementen er driedimensionaal of belicht uitzien. Ze zijn ideaal voor:

- **Achtergrondvullingen** die de aandacht naar een centraal onderwerp trekken.  
- **Knop- of pictogramaccenten** waar een subtiele gloed nodig is.  
- **Creatieve foto‑effecten** zoals vignetten of lichtflitsen.  

Aspose.PSD verwerkt **50+ invoer‑ en uitvoerformaten** en kan PSD‑bestanden met honderden pagina’s aan zonder het volledige document in het geheugen te laden, waardoor je gradient‑creatie kunt automatiseren over grote asset‑bibliotheken.

## Veelvoorkomende problemen & tips

- **Effect not visible:** Zorg ervoor dat `gradientOverlay.isVisible()` `true` retourneert. Sommige PSD‑bestanden verbergen effecten standaard.  
- **Incorrect layer index:** Lagen zijn nul‑gebaseerd; controleer dubbel of je de juiste laag target (`im.getLayers()[1]` verwijst naar de tweede laag).  
- **Opacity casting:** De `setOpacity`‑methode verwacht een `byte`. Het doorgeven van een `int` veroorzaakt een compilatiefout; cast expliciet zoals getoond.  
- **Resource loading:** Als je `null` tegenkomt bij het benaderen van effecten, controleer dan of `loadOptions.setLoadEffectsResource(true)` is ingesteld vóór het laden van de afbeelding.

## Veelgestelde vragen

**Q: Kan ik meerdere gradient‑effecten toepassen op één afbeelding?**  
A: Ja. Haal de `BlendingOptions` van de laag op, doorloop de `Effects`‑collectie en voeg een nieuwe `GradientOverlayEffect` toe voor elke gradient die je nodig hebt.

**Q: Welke andere effecten kan ik combineren met gradient overlays?**  
A: Aspose.PSD biedt schaduwen, gloed, reliëf en meer. Elk effect verschijnt in de `Effects`‑array en kan onafhankelijk worden geconfigureerd.

**Q: Hoe kan ik problemen oplossen als de effecten niet correct worden gerenderd?**  
A: Controleer of de PSD is geladen met `setLoadEffectsResource(true)`, controleer de zichtbaarheid van de laag, en bevestig dat je de juiste effect‑index wijzigt.

**Q: Is er een proefversie beschikbaar voor Aspose.PSD voor Java?**  
A: Ja, je kunt een gratis proefversie krijgen [hier](https://releases.aspose.com/).

**Q: Waar kan ik een licentie aanschaffen voor Aspose.PSD voor Java?**  
A: Bezoek de [purchase page](https://purchase.aspose.com/buy) voor licentie‑informatie.

## Aanvullende Veelgestelde Vragen

**Q: Kan ik de gradient‑richting programmatisch wijzigen?**  
A: Ja. Gebruik de methode `GradientOverlayEffect.setAngle(float angle)` om de gradient‑hoek in graden in te stellen. Voor radiale gradients wordt de hoek genegeerd, maar de methode moet wel worden aangeroepen.

**Q: Ondersteunt Aspose.PSD radiale gradients?**  
A: Absoluut. Stel de gradient‑stijl in op `GradientStyle.Radial` via de eigenschappen van `GradientOverlayEffect`.

**Q: Worden gradient overlays behouden bij conversie van PSD naar andere formaten (bijv. PNG)?**  
A: Wanneer je de PSD rastert (bijv. opslaan als PNG), blijft het visuele resultaat van de gradient overlay behouden, maar wordt het effect zelf onderdeel van de pixeldata.

**Q: Hoe verwijder ik een gradient overlay van een laag?**  
A: Haal de `BlendingOptions` van de laag op, zoek de `GradientOverlayEffect` in de `Effects`‑collectie en verwijder deze met `remove(effect)`.

**Q: Is het mogelijk om gradient‑veranderingen te animeren?**  
A: Hoewel Aspose.PSD geen animatie direct ondersteunt, kun je een reeks PSD‑bestanden genereren met variërende gradient‑parameters en deze vervolgens samenvoegen tot een video of GIF met een andere bibliotheek.

## Conclusie

Gefeliciteerd! Je hebt geleerd **how to create radial gradient java**‑effecten toe te passen op je afbeeldingen met Aspose.PSD voor Java. Door de bovenstaande stappen te volgen, kun je programmatic gradient overlays toevoegen, wijzigen en opslaan, waardoor je volledige creatieve controle krijgt over PSD‑assets. Experimenteer met verschillende kleuren, mengmodi en doorzichtigheidswaarden om de gewenste visuele impact te bereiken.

---

**Laatst bijgewerkt:** 2026-10-18  
**Getest met:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Auteur:** Aspose  








```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.*;
import com.aspose.psd.fileformats.psd.layers.layereffects.GradientOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Gerelateerde tutorials

- [Gradient Fill PSD maken met Java met Aspose.PSD – Gradient Fill-laag toevoegen](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [Pattern Overlay PSD: Effecten toevoegen met Aspose.PSD voor Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Kleuroverlay toepassen en doorzichtigheid instellen in Java met Aspose.PSD](/psd/java/image-editing/color-overlay-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}