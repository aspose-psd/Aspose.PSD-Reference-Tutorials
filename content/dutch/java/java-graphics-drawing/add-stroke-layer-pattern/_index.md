---
title: Hoe u een lijnlaagpatroon kunt toevoegen in Java
linktitle: Hoe u een lijnlaagpatroon kunt toevoegen in Java
second_title: Aspose.PSD Java-API
description: Leer hoe u een streeklaagpatroon aan PSD-bestanden kunt toevoegen met Aspose.PSD voor Java. Volg deze stapsgewijze handleiding om uw afbeeldingen eenvoudig te verbeteren.
type: docs
weight: 11
url: /nl/java/java-graphics-drawing/add-stroke-layer-pattern/
---
## Invoering
Het toevoegen van een lijnlaagpatroon aan een afbeelding in Java klinkt misschien als een hele klus, maar met Aspose.PSD voor Java is het eenvoudiger dan u denkt. Of u nu afbeeldingen ontwerpt of aan fotobewerkingsprogramma's werkt, deze handleiding begeleidt u stap voor stap door het proces. klaar om te beginnen? Laten we erin duiken!
## Vereisten
Voordat je begint, heb je een paar dingen nodig:
- Java Development Kit (JDK): Zorg ervoor dat JDK op uw systeem is geïnstalleerd.
-  Aspose.PSD voor Java: download de bibliotheek van[hier](https://releases.aspose.com/psd/java/) en neem het op in uw project.
- Een IDE: gebruik uw favoriete Integrated Development Environment (IDE) zoals IntelliJ IDEA of Eclipse.
## Pakketten importeren
Allereerst moet u de benodigde pakketten in uw Java-project importeren. Deze pakketten zijn essentieel voor het werken met Aspose.PSD.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
## Stap 1: Laad het PSD-bestand
De eerste stap bij het toevoegen van een streeklaagpatroon is het laden van het PSD-bestand dat u wilt bewerken.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
Door het PSD-bestand te laden, kunt u nu de lagen en effecten ervan openen en manipuleren.
## Stap 2: Bereid nieuwe patroongegevens voor
Vervolgens moet u de nieuwe patroongegevens voorbereiden die u op de streeklaag gaat toepassen.
```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```
Deze patroongegevens worden gebruikt om het nieuwe streekeffect te creëren.
## Stap 3: Toegang tot het beroerte-effect
Om het streekeffect te wijzigen, heeft u toegang nodig tot de specifieke laag en de overvloeiopties ervan.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
Dit zorgt ervoor dat u met de juiste laag en effect werkt.
## Stap 4: Pas het lijneffect aan
Laten we nu het streekeffect aanpassen met de nieuwe patroongegevens.
### Werk de eigenschappen van het lijneffect bij
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### Werk de patroonbron bij
```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```
Met dit codefragment wordt de patroonbron bijgewerkt met de nieuwe patroongegevens.
## Stap 5: Pas het nieuwe patroon toe
Pas ten slotte het nieuwe patroon toe op het streekeffect en sla de wijzigingen op.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
Dit zorgt ervoor dat het nieuwe patroon correct wordt toegepast en dat het bestand met de wijzigingen wordt opgeslagen.
## Stap 6: Controleer de wijzigingen
Om er zeker van te zijn dat alles correct werkt, laadt u het bestand opnieuw en controleert u de wijzigingen.
```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```
Met deze stap wordt gecontroleerd of de patroongegevens correct zijn toegepast op het streekeffect.
## Conclusie
En daar heb je het! U hebt met succes een lijnlaagpatroon aan een PSD-bestand toegevoegd met Aspose.PSD voor Java. Door deze stappen te volgen, kunt u uw afbeeldingen eenvoudig aanpassen en verbeteren. Veel codeerplezier!
## Veelgestelde vragen
### Wat is Aspose.PSD voor Java?
Aspose.PSD voor Java is een bibliotheek waarmee ontwikkelaars PSD-bestanden (Photoshop Document) programmatisch kunnen maken, bewerken en converteren.
### Kan ik Aspose.PSD voor Java gebruiken in een commercieel project?
 Ja, u kunt het gebruiken in commerciële projecten. U kunt een licentie kopen bij[hier](https://purchase.aspose.com/buy).
### Is er een gratis proefversie beschikbaar voor Aspose.PSD voor Java?
 Ja, u kunt een gratis proefversie downloaden van[hier](https://releases.aspose.com/).
### Hoe kan ik ondersteuning krijgen voor Aspose.PSD voor Java?
 U kunt ondersteuning krijgen van de Aspose-communityforums[hier](https://forum.aspose.com/c/psd/34).
### Wat zijn de systeemvereisten voor Aspose.PSD voor Java?
Je hebt JDK nodig en een IDE voor ontwikkeling. De bibliotheek ondersteunt meerdere besturingssystemen, waaronder Windows, Linux en macOS.