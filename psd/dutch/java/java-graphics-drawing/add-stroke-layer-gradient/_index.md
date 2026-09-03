---
date: 2026-09-03
description: Leer hoe u gradient stroke java kunt maken en stroke‑gradients kunt aanpassen
  in PSD‑bestanden met Aspose.PSD voor Java. Stapsgewijze handleiding voor ontwikkelaars.
keywords:
- create gradient stroke java
- add gradient stroke psd
- Aspose.PSD Java
- PSD gradient stroke
lastmod: 2026-09-03
linktitle: Hoe maak je een Gradient Stroke‑laag in Java
og_description: Maak gradient stroke java met Aspose.PSD voor Java in enkele minuten.
  Deze handleiding laat zien hoe u gradient strokes kunt toevoegen en aanpassen in
  PSD‑bestanden, inclusief code snippets en best practices.
og_image_alt: Screenshot of a PSD file showing a gradient stroke applied via Aspose.PSD
  Java API
og_title: Maak gradient stroke java – Aspose.PSD handleiding
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to create gradient stroke java and customize stroke gradients
    in PSD files using Aspose.PSD for Java. Step‑by‑step guide for developers.
  headline: Create gradient stroke java – Aspose.PSD tutorial guide
  type: TechArticle
- description: Learn how to create gradient stroke java and customize stroke gradients
    in PSD files using Aspose.PSD for Java. Step‑by‑step guide for developers.
  name: Create gradient stroke java – Aspose.PSD tutorial guide
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: '**Aspose.PSD for Java** – Download the library from the [Aspose.PSD download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – Download the library from the [Aspose.PSD download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
  - name: '**License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      if you don’t have a full commercial license.'
    text: '**License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      if you don’t have a full commercial license.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a pure‑Java library that lets developers create,
      edit, convert, and render Photoshop PSD files without requiring Adobe Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Yes, a valid license is required for production use. You can obtain a
      [temporary license](https://purchase.aspose.com/temporary-license/) for evaluation.
    question: Do I need a license to use Aspose.PSD for Java?
  - answer: Absolutely. Aspose.PSD provides APIs to build a new PSD document, add
      layers, apply effects, and save the file entirely programmatically.
    question: Can I create PSD files from scratch with this library?
  - answer: Yes, you can apply shadows, glows, bevels, and many other layer effects
      using the same effect‑based API.
    question: Is it possible to apply other effects besides gradient strokes?
  - answer: The official documentation is available in the [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full reference documentation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- gradient stroke
- Aspose.PSD
- Java graphics
title: Maak gradient stroke java – Aspose.PSD handleiding
url: /nl/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe maak je een gradient stroke in Java met Aspose.PSD

## Introductie
Als je **gradient stroke java** effecten wilt maken zonder Photoshop te openen, ben je op de juiste plek. In deze tutorial leer je hoe je Aspose.PSD for Java gebruikt — een pure‑Java bibliotheek die je volledige programmeercontrole over PSD‑bestanden geeft. We lopen door het laden van een PSD, het benaderen van het stroke‑effect van een laag, het configureren van een gradient‑vulling en uiteindelijk het opslaan van het resultaat. Aan het einde kun je professionele gradient‑contouren toevoegen aan vormen of tekst in slechts een paar regels code.

## Snelle antwoorden
- **Wat is het primaire doel?** Create a gradient stroke layer on a PSD file using Java.  
- **Welke bibliotheek biedt de API?** Aspose.PSD for Java (supports Java 8 +).  
- **Heb ik een licentie nodig voor productie?** Ja – een geldige of tijdelijke licentie is vereist.  
- **Hoe lang duurt een basisimplementatie?** Ongeveer 10‑15 minuten voor een eenvoudige stroke.  
- **Kan ik het gradienttype aanpassen?** Absoluut – lineaire, radiale en hoek‑gebaseerde gradients worden allemaal ondersteund.

## Wat is een gradient stroke layer?
Een gradient stroke layer is een vectorcontour waarvan de kleur soepel overloopt tussen twee of meer tinten. Het kan worden toegepast op vormen, tekst of elke vectormasker binnen een PSD‑bestand, waardoor ontwerpers een dynamisch visueel effect krijgen zonder de afbeelding te rasteren.

## Waarom Aspose.PSD for Java gebruiken?
Aspose.PSD for Java biedt **volledige PSD-ondersteuning** voor meer dan 100 functies — waaronder lagen, maskers, aanpassingslagen en laageffecten — en kan bestanden tot 2 GB verwerken zonder het volledige document in het geheugen te laden. De bibliotheek draait op elk besturingssysteem dat Java ondersteunt, heeft geen native afhankelijkheden, en wordt maandelijks bijgewerkt om compatibel te blijven met de nieuwste Photoshop‑bestandsspecificaties.

## Vereisten
1. **Java Development Kit (JDK)** – Installeer de nieuwste JDK van [Oracle's website](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java** – Download de bibliotheek van de [Aspose.PSD downloadpagina](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse of NetBeans.  
4. **Licentie** – Verkrijg een [tijdelijke licentie](https://purchase.aspose.com/temporary-license/) als je geen volledige commerciële licentie hebt.

## Pakketten importeren
De `import`‑statements brengen de benodigde klassen in scope.  

```text
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```
```

Laten we nu het proces in duidelijke stappen opdelen.

## Stap 1: Laad het PSD‑bestand
Het laden van het bronbestand is de eerste stap; je moet effect‑resources inschakelen zodat stroke‑informatie beschikbaar is voor bewerking. **PsdLoadOptions** configureert hoe een PSD‑bestand wordt geladen, waardoor je specifieke resources kunt in- of uitschakelen.  

```text
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
```

## Stap 2: Toegang tot het stroke‑effect
**StrokeEffect** vertegenwoordigt de contourstijl die op een laag wordt toegepast, inclusief breedte, kleur en gradient‑vulling.  

```text
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
```

## Stap 3: Verifieer stroke‑effecteigenschappen
Voordat je iets wijzigt, is het goed om de bestaande eigenschappen te lezen. Dit helpt je de huidige configuratie te begrijpen en te voorkomen dat je per ongeluk belangrijke instellingen overschrijft. **GradientFillSettings** bevat de gradient‑vullingsconfiguratie voor een stroke‑effect.  

```text
```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```
```

## Stap 4: Wijzig de gradient‑vullingsinstellingen
`GradientFill` definieert hoe kleuren over de stroke verlopen. Je kunt het type (lineair, radiaal), de hoek en de blend‑mode wijzigen, en vervolgens nieuwe kleur‑ en transparantiepunten toewijzen.  

```text
```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```
```

## Stap 5: Voeg kleur‑ en transparantiepunten toe en wijzig ze
Een gradient wordt opgebouwd uit een reeks kleur‑stop‑ en opacity‑stop‑punten. **GradientColorPoint** definieert een kleur‑stop in een gradient, met kleur en positie. **GradientTransparencyPoint** definieert een opacity‑stop in een gradient, met opacity en positie. Het toevoegen of aanpassen van deze punten stelt je in staat de visuele stroom van de stroke vorm te geven.  

```text
```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
```

## Stap 6: Sla het gewijzigde PSD‑bestand op
Na alle aanpassingen schrijf je het bijgewerkte document terug naar de schijf. Aspose.PSD behoudt automatisch alle andere lagen en resources.  

```text
```java
im.save(exportPath);
```
```

## Stap 7: Verifieer de wijzigingen
Laad het opgeslagen bestand opnieuw en controleer dat de gradient‑eigenschappen van de stroke overeenkomen met de waarden die je hebt ingesteld. Deze verificatiestap is essentieel voor geautomatiseerde pipelines. **Assert** biedt eenvoudige test‑asserties om voorwaarden tijdens runtime te verifiëren.  

```text
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Check transparency points
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(2411, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint1.getOpacity());
Assert.areEqual(4096, transparencyPoint1.getLocation());
```
```

## Veelvoorkomende valkuilen en tips voor probleemoplossing
- **Missing license error** – Als je een licentie‑exception ziet, controleer dan dubbel of het tijdelijke licentiebestand correct is geladen vóór enige API‑aanroep.  
- **Gradient not visible** – Zorg ervoor dat de `strokeEnabled`‑vlag van de doel‑laag op `true` staat; anders wordt het effect genegeerd tijdens het renderen.  
- **Performance on large files** – Voor PSD‑bestanden groter dan 500 MB, overweeg `PsdImage.load(..., LoadOptions)` te gebruiken met `loadResources = false` en schakel alleen de resources in die je nodig hebt.

## Veelgestelde vragen

**Q: Wat is Aspose.PSD for Java?**  
A: Aspose.PSD for Java is een pure‑Java bibliotheek die ontwikkelaars in staat stelt Photoshop PSD‑bestanden te maken, bewerken, converteren en renderen zonder Adobe Photoshop te vereisen.

**Q: Heb ik een licentie nodig om Aspose.PSD for Java te gebruiken?**  
A: Ja, een geldige licentie is vereist voor productiegebruik. Je kunt een [tijdelijke licentie](https://purchase.aspose.com/temporary-license/) verkrijgen voor evaluatie.

**Q: Kan ik PSD‑bestanden vanaf nul maken met deze bibliotheek?**  
A: Absoluut. Aspose.PSD biedt API's om een nieuw PSD‑document te bouwen, lagen toe te voegen, effecten toe te passen en het bestand volledig programmatisch op te slaan.

**Q: Is het mogelijk om andere effecten toe te passen naast gradient strokes?**  
A: Ja, je kunt schaduwen, gloed, reliëf en vele andere laageffecten toepassen met dezelfde effect‑gebaseerde API.

**Q: Waar kan ik de volledige referentiedocumentatie vinden?**  
A: De officiële documentatie is beschikbaar in de [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

## Conclusie
Je hebt nu een complete, end‑to‑end oplossing voor hoe je **gradient stroke java** effecten in PSD‑bestanden maakt met Aspose.PSD. Door een PSD te laden, het stroke‑effect te benaderen, een gradient‑vulling te configureren en het bestand op te slaan, kun je geavanceerde grafische workflows automatiseren die anders handmatig in Photoshop zouden moeten gebeuren. Experimenteer met verschillende gradient‑types, blend‑modes en opacity‑stops om precies de uitstraling te bereiken die je voor je applicatie nodig hebt.

---

**Laatst bijgewerkt:** 2026-09-03  
**Getest met:** Aspose.PSD for Java 24.11  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Gradient Fill PSD maken met Java via Aspose.PSD – Gradient Fill Layer toevoegen](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [Radiale gradient‑effecten maken in Aspose.PSD for Java](/psd/java/advanced-image-effects/add-gradient-effects/)
- [Stroke‑kleur wijzigen in Java met Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}