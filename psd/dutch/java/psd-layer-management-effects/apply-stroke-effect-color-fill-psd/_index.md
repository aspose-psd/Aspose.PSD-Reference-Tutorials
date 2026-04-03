---
date: 2026-04-03
description: Leer hoe je een PSD opslaat als PNG met een lijn‑effect en kleurvulling
  met Aspose.PSD voor Java. Deze stapsgewijze gids laat zien hoe je PSD snel naar
  PNG exporteert.
keywords:
- save psd as png
- export psd to png
- set stroke color
- apply layer effects
- customize stroke width
linktitle: PSD opslaan als PNG met Stroke‑effect – Java
second_title: Aspose.PSD Java API
title: PSD opslaan als PNG met Stroke‑effect – Java
url: /nl/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Opslaan van PSD als PNG met Stroke-effect en Kleurvulling – Java

## Introductie

In deze gids leer je hoe je **PSD als PNG** kunt opslaan terwijl je een stroke-effect met een kleurvulling toepast met Aspose.PSD voor Java. Of je nu een ervaren ontwikkelaar bent of net begint, deze stap‑voor‑stap tutorial maakt het gemakkelijk om de taak uit te voeren. We behandelen alles, van het opzetten van je omgeving tot het exporteren van de uiteindelijke afbeelding, zodat je snel **PSD naar PNG kunt exporteren** in je eigen projecten.

## Snelle Antwoorden
- **Wat bereikt deze tutorial?** Het laat zien hoe je een PSD‑bestand als PNG kunt opslaan na het toepassen van een aanpasbaar stroke‑effect.  
- **Welke bibliotheek wordt gebruikt?** Aspose.PSD voor Java.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor testen; een licentie is vereist voor productie.  
- **Kan ik de stroke‑kleur wijzigen?** Ja – je kunt elke kleur instellen via de `ColorFillSettings`.  
- **Is batchverwerking mogelijk?** Absoluut – plaats de code in een lus om meerdere PSD‑bestanden te verwerken.

## Wat betekent “PSD als PNG opslaan”?
Een PSD als PNG opslaan betekent dat je Photoshop’s native gelaagde bestand converteert naar een plat, web‑vriendelijk afbeeldingsformaat, terwijl je de visuele getrouwheid behoudt. Dit is handig wanneer je PSD‑inhoud moet weergeven op websites, mobiele apps of elk platform dat PSD‑bestanden niet direct ondersteunt.

## Waarom een stroke‑effect met kleurvulling toepassen?
Een stroke voegt een scherpe omtrek toe rond de inhoud van een laag, waardoor graphics opvallen tegen complexe achtergronden. Door dit te combineren met een aangepaste vulkleur kun je afbeeldingen branden, UI‑elementen markeren of opvallende miniaturen maken zonder Photoshop te verlaten.

## Vereisten

1. **Java Development Kit (JDK) 8+** – zorg ervoor dat `java` in je PATH staat.  
2. **Aspose.PSD voor Java** – download van de [website](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, of elke editor die je verkiest.  
4. **Voorbeeld‑PSD** – een bestand dat al een stroke‑effect bevat (of voeg er een toe in Photoshop).  
5. **Basiskennis van Java** – je zult een paar regels code schrijven, maar niets geavanceerd.

Zodra je deze klaar hebt, kunnen we beginnen met coderen.

## Pakketten importeren

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

Deze imports brengen alle klassen die nodig zijn om een PSD te laden, de stroke te wijzigen, en zowel PSD‑ als PNG‑uitvoer op te slaan.

## Hoe PSD als PNG opslaan met Stroke‑effect

### Stap 1: Laad het PSD‑bestand

Eerst, wijs naar de map die je bron‑PSD bevat.

```java
String dataDir = "Your Document Directory";
```

Vervang `"Your Document Directory"` door het daadwerkelijke pad op je machine.

Laad nu het bestand terwijl je eventuele bestaande effect‑resources behoudt:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Stap 2: Stel de stroke‑kleur in (en pas eventueel de breedte aan)

De onderstaande lus doorloopt elke laag, pakt de eerste `StrokeEffect` en verandert de vulkleur. Je kunt ook `setWidth` of `setPosition` op het `StrokeEffect`‑object aanpassen als je de **stroke‑breedte wilt aanpassen**.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    // Set the stroke color – change to any Color you like
    settings.setColor(Color.getDeepPink());
}
```

> **Pro tip:** `Color.getDeepPink()` is slechts een voorbeeld. Gebruik `new Color(r, g, b)` voor aangepaste RGB‑waarden.

### Stap 3: Sla de gewijzigde PSD op (optioneel)

Als je een PSD‑versie wilt behouden met de bijgewerkte stroke, sla deze dan op als volgt:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

### Stap 4: Exporteer de afbeelding als PNG (de kernstap “PSD als PNG opslaan”)

Converteer tenslotte de bewerkte PSD naar een PNG‑bestand dat klaar is voor webgebruik:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

De PNG behoudt de dieproze stroke die je eerder hebt ingesteld, en de `TruecolorWithAlpha`‑optie zorgt ervoor dat transparantie behouden blijft.

## Veelvoorkomende problemen & oplossingen

| Probleem | Reden | Oplossing |
|----------|-------|-----------|
| **`ArrayIndexOutOfBoundsException`** | De laag heeft geen effecten of het eerste effect is geen `StrokeEffect`. | Controleer of de laag daadwerkelijk een stroke bevat of doorloop `getEffects()` om het juiste type te vinden. |
| **Kleur verandert niet** | Je bewerkt mogelijk een kopie van de instellingen in plaats van het origineel. | Zorg ervoor dat je direct cast naar `ColorFillSettings` vanuit `effect.getFillSettings()`. |
| **PNG verschijnt leeg** | De PSD werd geladen zonder de laag te rasteren. | Roep `im.save(..., new PngOptions())` aan na alle aanpassingen; vermijd het opslaan van de originele `im` vóór wijzigingen. |

## Veelgestelde vragen

**V: Kan ik meerdere effecten toepassen op één laag met Aspose.PSD voor Java?**  
A: Ja, je kunt de mengopties van de laag benaderen en zoveel effecten toevoegen als nodig, inclusief schaduwen, gloed en strokes.

**V: Is het mogelijk om het proces te automatiseren voor een batch van PSD‑bestanden?**  
A: Absoluut. Plaats de laad‑, effect‑toepassings‑ en opslaglogica in een `for‑each`‑lus die over bestanden in een map itereren.

**V: Hoe kan ik wijzigingen aan een PSD‑bestand terugdraaien?**  
A: Laad het originele bestand opnieuw voordat je wijzigingen opslaat; Aspose.PSD biedt geen undo‑stack.

**V: Kan ik de stroke‑breedte en positie aanpassen?**  
A: Ja. Gebruik `effect.setWidth(float)` en `effect.setPosition(StrokeEffect.Position)` om de dikte en plaatsing (binnen, buiten of gecentreerd) te regelen.

**V: Is de Aspose.PSD voor Java‑bibliotheek gratis te gebruiken?**  
A: Een gratis proefversie is beschikbaar voor evaluatie. Volledige functionaliteit vereist een aangeschafte licentie. Zie de [koopopties](https://purchase.aspose.com/buy) voor details.

---

**Laatst bijgewerkt:** 2026-04-03  
**Getest met:** Aspose.PSD 24.12 voor Java  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}