---
date: 2025-11-30
description: Leer hoe je een lijn kunt toevoegen en de PSD‑lijnkleur kunt wijzigen
  met Aspose.PSD voor Java. Volg deze stapsgewijze handleiding om de kleur en doorzichtigheid
  van de lijnlaag aan te passen.
linktitle: Add Stroke Layer Color
second_title: Aspose.PSD Java API
title: Hoe een lijnkleurlaag toevoegen in Aspose.PSD voor Java
url: /nl/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe een Stroke-laagkleur toe te voegen in Aspose.PSD voor Java

## Introductie

Als je programmatically een **stroke wilt toevoegen** aan een Photoshop-document, maakt Aspose.PSD voor Java het eenvoudig. In deze tutorial lopen we door het toevoegen van een stroke-laagkleur, het aanpassen van de opacity, en het opslaan van het resultaat. Aan het einde zie je ook hoe je **de stroke-kleur kunt wijzigen** (of *de PSD stroke-kleur wijzigen*) voor elke bestaande laag, waardoor je volledige creatieve controle hebt vanuit je Java-code.

## Snelle antwoorden
- **Welke bibliotheek is vereist?** Aspose.PSD for Java (latest version).  
- **Kan ik de stroke-kleur wijzigen?** Ja – gebruik `ColorFillSettings` om elke `Color` in te stellen.  
- **Heb ik een licentie nodig?** Een tijdelijke licentie werkt voor evaluatie; een volledige licentie is vereist voor productie.  
- **Welke Java-versie wordt ondersteund?** Java 8 of hoger.  
- **Hoe lang duurt de implementatie?** Meestal minder dan 10 minuten voor een eenvoudige stroke-wijziging.

## Wat is een Stroke-laag in een PSD?
Een stroke-laag is een vector-effect dat een omtrek rond de inhoud van een laag tekent. Het kan worden aangepast met kleur, dikte, opacity en blend‑mode. Het programmatically wijzigen van dit effect maakt geautomatiseerde branding, batch‑verwerking of dynamische grafiekgeneratie mogelijk.

## Waarom Aspose.PSD gebruiken om de Stroke-kleur te wijzigen?
- **Geen Photoshop vereist** – werk volledig in Java.  
- **Volledige PSD-specificatie‑naleving** – alle moderne PSD-functies worden ondersteund.  
- **Hoge prestaties** – verwerk grote bestanden snel.  
- **Cross‑platform** – draait op elk OS met een JVM.

## Vereisten

- **Aspose.PSD Bibliotheek** – download van de [official documentation](https://reference.aspose.com/psd/java/).  
- **Java Development Kit (JDK)** – versie 8 of nieuwer.  
- **IDE** – Eclipse, IntelliJ IDEA, of een andere Java‑compatibele editor.

## Import pakketten

Importeer eerst de klassen die je nodig hebt. Dit geeft je project toegang tot de PSD‑verwerking en stroke‑effect API's.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Stap 1: Stel je project in

Maak een nieuw Java‑project, voeg de Aspose.PSD‑JAR toe aan het build‑pad, en controleer of de bibliotheek zonder fouten laadt.

## Stap 2: Laad het PSD‑bestand

Schakel het laden van effect‑resources in zodat de stroke‑informatie beschikbaar is.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Stap 3: Toegang tot de Stroke‑effectlaag

Haal het eerste stroke‑effect op van de tweede laag (index 1).

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## Stap 4: Valideer Stroke‑eigenschappen

Bevestig de bestaande eigenschappen voordat je wijzigingen aanbrengt. Dit helpt onverwachte resultaten te voorkomen.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## Stap 5: Stel kleur en opacity in (Hoe de Stroke‑kleur wijzigen)

Hier **wijzigen we de PSD stroke‑kleur** naar geel en verlagen we de opacity tot 50 % (127 / 255).

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## Stap 6: Sla de aangepaste PSD op

Schrijf de bijgewerkte afbeelding terug naar de schijf. Het nieuwe bestand bevat nu de aangepaste stroke.

```java
im.save(exportPath);
```

## Veelvoorkomende valkuilen & tips

- **Null‑controles** – controleer altijd dat `getEffects()` een niet‑null array retourneert vóór het casten.  
- **Laag‑index** – PSD‑lagen zijn nul‑gebaseerd; zorg ervoor dat je de juiste laag target.  
- **Kleurformaat** – `Color.getYellow()` is slechts een voorbeeld; je kunt aangepaste kleuren maken met `new Color(r, g, b)`.  
- **Opacity‑bereik** – opacity is een byte (0–255); waarden boven 255 worden afgekapt.

## Conclusie

Je hebt nu geleerd **hoe een stroke toe te voegen** aan een PSD‑bestand en **hoe de stroke‑kleur te wijzigen** met Aspose.PSD voor Java. Experimenteer met verschillende kleuren, blend‑modes en opacities om de exacte visuele stijl te bereiken die je project nodig heeft.

## Veelgestelde vragen

**V: Kan ik Aspose.PSD gebruiken met andere Java‑grafische bibliotheken?**  
A: Ja, Aspose.PSD kan worden gecombineerd met bibliotheken zoals Apache Commons Imaging of Java2D voor uitgebreide functionaliteit.

**V: Is Aspose.PSD compatibel met het nieuwste PSD‑bestandformaat?**  
A: Absoluut. De bibliotheek wordt regelmatig bijgewerkt om de nieuwste Photoshop‑specificaties te ondersteunen.

**V: Hoe ga ik om met uitzonderingen bij het gebruik van Aspose.PSD?**  
A: Raadpleeg het [support forum](https://forum.aspose.com/c/psd/34) voor gedetailleerde probleemoplossing en voorbeeld‑code voor foutafhandeling.

**V: Kan ik Aspose.PSD uitproberen voordat ik het koop?**  
A: Zeker! Pak een [free trial](https://releases.aspose.com/) om alle functies te verkennen.

**V: Waar kan ik een tijdelijke licentie voor Aspose.PSD krijgen?**  
A: Verkrijg een [temporary license](https://purchase.aspose.com/temporary-license/) om de bibliotheek te evalueren in je ontwikkelomgeving.

---

**Laatst bijgewerkt:** 2025-11-30  
**Getest met:** Aspose.PSD 24.11 for Java  
**Auteur:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}