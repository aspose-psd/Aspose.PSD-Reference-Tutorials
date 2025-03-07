---
title: Hoe u een lijnlaagverloop kunt toevoegen in Java
linktitle: Hoe u een lijnlaagverloop kunt toevoegen in Java
second_title: Aspose.PSD Java-API
description: Leer hoe u lijnlaaggradiënten in PSD-bestanden kunt toevoegen en aanpassen met Aspose.PSD voor Java met deze uitgebreide stapsgewijze zelfstudie.
weight: 10
url: /nl/java/java-graphics-drawing/add-stroke-layer-gradient/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe u een lijnlaagverloop kunt toevoegen in Java

## Invoering
Heeft u zich ooit afgevraagd hoe u met Java een verlooplaagverloop aan uw afbeeldingen kunt toevoegen? Nou, je bent op de juiste plek! Vandaag duiken we in de wereld van Aspose.PSD voor Java, een krachtige bibliotheek waarmee je PSD-bestanden gemakkelijk kunt manipuleren. Of u nu een beginner of een doorgewinterde ontwikkelaar bent, deze stapsgewijze handleiding leidt u door het proces van het toevoegen van een lijnlaagverloop aan uw PSD-bestanden. Dus doe je gordel om en bereid je voor om je grafische bewerkingsvaardigheden te verbeteren!
## Vereisten
Voordat we aan de slag gaan, zijn er een aantal zaken die u op orde moet hebben. Zorg ervoor dat je het volgende hebt:
1.  Java Development Kit (JDK): Zorg ervoor dat JDK op uw systeem is geïnstalleerd. Je kunt het downloaden van[De website van Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD voor Java-bibliotheek: u kunt het downloaden van de[Aspose.PSD-downloadpagina](https://releases.aspose.com/psd/java/).
3. Een geïntegreerde ontwikkelomgeving (IDE): Elke IDE zoals IntelliJ IDEA, Eclipse of NetBeans zal werken.
4.  Een geldige licentie: u kunt een[tijdelijke licentie](https://purchase.aspose.com/temporary-license/) als je geen volledige hebt.
## Pakketten importeren
Laten we eerst de benodigde pakketten importeren. Deze zullen ons in staat stellen de klassen en methoden te gebruiken die nodig zijn voor het manipuleren van het PSD-bestand.
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
Laten we het voorbeeld nu in meerdere stappen opsplitsen voor een beter begrip.
## Stap 1: Laad het PSD-bestand
 Eerst moeten we het PSD-bestand laden dat we willen wijzigen. Wij gebruiken de`PsdLoadOptions` om aan te geven dat we de effectbronnen willen laden.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## Stap 2: Toegang tot het beroerte-effect
Vervolgens moeten we toegang krijgen tot het lijneffect van de laag waarin we geïnteresseerd zijn. Hier gaan we ervan uit dat dit de derde laag (index 2) in het PSD-bestand is.
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## Stap 3: Controleer de eigenschappen van het lijneffect
Voordat we wijzigingen aanbrengen, moeten we de eigenschappen van het lijneffect verifiëren om er zeker van te zijn dat we de juiste instellingen wijzigen.
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
## Stap 4: Wijzig de instellingen voor verloopvulling
Nu is het tijd om de instellingen voor de verloopvulling aan te passen aan onze vereisten. We zullen de kleur, dekking, overvloeimodus en andere eigenschappen wijzigen.
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
## Stap 5: Kleur- en transparantiepunten toevoegen en wijzigen
Laten we nieuwe kleur- en transparantiepunten toevoegen en de bestaande aanpassen om het gewenste verloopeffect te bereiken.
```java
// Nieuw kleurpunt toevoegen
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Wijzig de locatie van het vorige punt
fillSettings.getColorPoints()[1].setLocation(1899);
// Nieuw transparantiepunt toevoegen
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Wijzig de locatie van het vorige transparantiepunt
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## Stap 6: Sla het gewijzigde PSD-bestand op
Nadat we alle noodzakelijke wijzigingen hebben aangebracht, moeten we het PSD-bestand opslaan.
```java
im.save(exportPath);
```
## Stap 7: Controleer de wijzigingen
Laten we ten slotte het opgeslagen PSD-bestand laden en controleren of onze wijzigingen correct zijn toegepast.
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Controleer kleurpunten
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
// Controleer de transparantiepunten
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
En daar heb je het! U weet nu hoe u lijnlaagverlopen in PSD-bestanden kunt toevoegen en manipuleren met behulp van Aspose.PSD voor Java. Deze tutorial behandelde het laden van het PSD-bestand, het openen en wijzigen van streekeffecten en het opslaan van de wijzigingen. Met deze vaardigheden kunt u visueel aantrekkelijke verlopen creëren en uw PSD-bestanden aanpassen aan uw behoeften.
## Veelgestelde vragen
### Wat is Aspose.PSD voor Java?
Aspose.PSD voor Java is een bibliotheek waarmee ontwikkelaars met PSD-bestanden in Java-toepassingen kunnen werken en functies biedt voor het maken, manipuleren en converteren van PSD-bestanden.
### Heb ik een licentie nodig om Aspose.PSD voor Java te gebruiken?
 Ja, u heeft een geldige licentie nodig om Aspose.PSD voor Java te gebruiken. Je kunt een[tijdelijke licentie](https://purchase.aspose.com/temporary-license/) voor evaluatiedoeleinden.
### Kan ik Aspose.PSD voor Java gebruiken om helemaal opnieuw PSD-bestanden te maken?
Absoluut! Aspose.PSD voor Java biedt uitgebreide API's om PSD-bestanden programmatisch te maken en te manipuleren.
### Is het mogelijk om andere effecten toe te passen met Aspose.PSD voor Java?
Ja, je kunt verschillende effecten toepassen, zoals schaduw, gloed en meer met Aspose.PSD voor Java.
### Waar kan ik de documentatie voor Aspose.PSD voor Java vinden?
 U kunt de documentatie vinden[hier](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
