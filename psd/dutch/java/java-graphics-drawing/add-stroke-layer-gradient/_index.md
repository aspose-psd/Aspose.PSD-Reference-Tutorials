---
date: 2026-01-14
description: Leer hoe je een gradient‑strokelaag maakt en lijnkleurverlopen in PSD‑bestanden
  aanpast met Aspose.PSD voor Java in deze stap‑voor‑stap tutorial.
linktitle: How to Create Gradient Stroke Layer in Java
second_title: Aspose.PSD Java API
title: Hoe een gradient-strooklaag te maken in Java
url: /nl/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe een Gradient Stroke‑laag te maken in Java

## Introductie
Heb je je ooit afgevraagd hoe je een **gradient stroke layer** in je PSD‑bestanden kunt maken met Java? Je bent op de juiste plek! Vandaag duiken we in Aspose.PSD for Java – een krachtige bibliotheek waarmee je PSD‑bestanden moeiteloos kunt manipuleren. Of je nu nieuw bent in grafische programmering of bestaande ontwerpen wilt verfijnen, deze gids leidt je stap voor stap door het toevoegen en aanpassen van stroke‑gradients.

## Snelle antwoorden
- **Wat is het primaire doel?** Een gradient stroke‑laag maken op een PSD‑bestand.  
- **Welke bibliotheek is vereist?** Aspose.PSD for Java.  
- **Heb ik een licentie nodig?** Ja, een geldige (of tijdelijke) licentie is vereist voor productie.  
- **Welke Java‑versie werkt?** Java 8 of hoger.  
- **Hoe lang duurt de implementatie?** Ongeveer 10‑15 minuten voor een eenvoudige gradient stroke.

## Wat is een Gradient Stroke‑laag?
Een gradient stroke‑laag is een vectoromtrek rond een vorm of tekst die geleidelijk overloopt tussen kleuren. Met Aspose.PSD kun je programmatically de kleuren, doorzichtigheid, hoek en type (lineair, radiaal, enz.) van de stroke definiëren.

## Waarom Aspose.PSD for Java gebruiken?
- **Volledige PSD‑ondersteuning** – lees, bewerk en schrijf PSD‑bestanden zonder Photoshop.  
- **Rijke effect‑API** – toegang tot stroke, schaduw, gloed en vele andere laageffecten.  
- **Cross‑platform** – werkt op elk OS dat Java ondersteunt.  
- **Geen native afhankelijkheden** – pure Java, eenvoudig te integreren in CI‑pipelines.

## Voorvereisten
1. **Java Development Kit (JDK)** – Installeer de nieuwste JDK van [Oracle's website](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java** – Download de bibliotheek van de [Aspose.PSD downloadpagina](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse of NetBeans.  
4. **Licentie** – Verkrijg een [tijdelijke licentie](https://purchase.aspose.com/temporary-license/) als je geen volledige licentie hebt.

## Pakketten importeren
Eerst importeren we de klassen die we nodig hebben voor het laden van de PSD, het benaderen van effecten en het configureren van gradient‑vullingen.

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

Laten we nu het proces in duidelijke stappen opdelen.

## Stap 1: Laad het PSD‑bestand
We laden de bron‑PSD en schakelen effect‑resources in zodat het stroke‑effect beschikbaar is.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## Stap 2: Toegang tot het Stroke‑effect
Aangenomen dat de stroke die we willen aanpassen behoort tot de derde laag (index 2), halen we de `StrokeEffect` op.

```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```

## Stap 3: Verifieer Stroke‑effecteigenschappen
Voordat we wijzigingen aanbrengen, bevestigen we de bestaande instellingen zodat we precies weten wat we gaan updaten.

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

## Stap 4: Wijzig de instellingen van de Gradient‑vulling
Hier wijzigen we de kleur, doorzichtigheid, blend‑mode en andere eigenschappen om het gewenste uiterlijk te bereiken.

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

## Stap 5: Voeg kleur‑ en transparantiepunten toe en wijzig ze
We voegen nieuwe kleur‑ en transparantiepunten toe, en passen de bestaande aan om de gradient vorm te geven.

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

## Stap 6: Sla het gewijzigde PSD‑bestand op
Na alle aanpassingen schrijven we het bijgewerkte bestand terug naar de schijf.

```java
im.save(exportPath);
```

## Stap 7: Verifieer de wijzigingen
Laad het opgeslagen bestand en controleer of elke eigenschap de aangebrachte wijzigingen weerspiegelt.

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
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```

## Conclusie
Je weet nu hoe je **gradient stroke layer**‑effecten in PSD‑bestanden kunt maken met Aspose.PSD for Java. Door een PSD te laden, het stroke‑effect te benaderen, de gradient‑vullinginstellingen aan te passen en het resultaat op te slaan, kun je programmatically professionele graphics produceren zonder ooit Photoshop te openen.

## Veelgestelde vragen
### Wat is Aspose.PSD for Java?
Aspose.PSD for Java is een bibliotheek die ontwikkelaars in staat stelt om met PSD‑bestanden te werken in Java‑applicaties, met functies om PSD‑bestanden te maken, te manipuleren en te converteren.

### Heb ik een licentie nodig om Aspose.PSD for Java te gebruiken?
Ja, je hebt een geldige licentie nodig om Aspose.PSD for Java te gebruiken. Je kunt een [tijdelijke licentie](https://purchase.aspose.com/temporary-license/) verkrijgen voor evaluatiedoeleinden.

### Kan ik Aspose.PSD for Java gebruiken om PSD‑bestanden vanaf nul te maken?
Absoluut! Aspose.PSD for Java biedt uitgebreide API’s om PSD‑bestanden programmatically te creëren en te manipuleren.

### Is het mogelijk om andere effecten toe te passen met Aspose.PSD for Java?
Ja, je kunt verschillende effecten zoals schaduw, gloed en meer toepassen met Aspose.PSD for Java.

### Waar kan ik de documentatie voor Aspose.PSD for Java vinden?
Je kunt de documentatie vinden [hier](https://reference.aspose.com/psd/java/).

---

**Laatst bijgewerkt:** 2026-01-14  
**Getest met:** Aspose.PSD for Java 24.11  
**Auteur:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
