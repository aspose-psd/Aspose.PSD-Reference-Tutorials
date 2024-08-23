---
title: Hur man lägger till Stroke Layer Pattern i Java
linktitle: Hur man lägger till Stroke Layer Pattern i Java
second_title: Aspose.PSD Java API
description: Lär dig hur du lägger till ett strecklagermönster till PSD-filer med Aspose.PSD för Java. Följ denna steg-för-steg-guide för att enkelt förbättra dina bilder.
type: docs
weight: 11
url: /sv/java/java-graphics-drawing/add-stroke-layer-pattern/
---
## Introduktion
Att lägga till ett strecklagermönster till en bild i Java kan låta som en skrämmande uppgift, men med Aspose.PSD för Java är det enklare än du tror. Oavsett om du designar grafik eller arbetar med fotoredigeringsapplikationer, kommer den här guiden att leda dig genom processen steg för steg. Redo att börja? Låt oss dyka in!
## Förutsättningar
Innan du börjar behöver du några saker:
- Java Development Kit (JDK): Se till att du har JDK installerat på ditt system.
-  Aspose.PSD för Java: Ladda ner biblioteket från[här](https://releases.aspose.com/psd/java/) och inkludera det i ditt projekt.
- En IDE: Använd din favorit Integrated Development Environment (IDE) som IntelliJ IDEA eller Eclipse.
## Importera paket
Först och främst måste du importera de nödvändiga paketen till ditt Java-projekt. Dessa paket är viktiga för att arbeta med Aspose.PSD.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
## Steg 1: Ladda PSD-filen
Det första steget för att lägga till ett strecklagermönster är att ladda PSD-filen du vill redigera.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
Genom att ladda PSD-filen kan du nu komma åt och manipulera dess lager och effekter.
## Steg 2: Förbered nya mönsterdata
Därefter måste du förbereda de nya mönsterdata som du kommer att tillämpa på linjelagret.
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
Denna mönsterdata kommer att användas för att skapa den nya streckeffekten.
## Steg 3: Få tillgång till Stroke Effect
För att ändra streckeffekten måste du komma åt det specifika lagret och dess blandningsalternativ.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
Detta säkerställer att du arbetar med rätt lager och effekt.
## Steg 4: Ändra Stroke Effect
Låt oss nu modifiera streckeffekten med den nya mönsterdatan.
### Uppdatera Stroke Effect Properties
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### Uppdatera mönsterresursen
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
Det här kodavsnittet uppdaterar mönsterresursen med den nya mönsterdatan.
## Steg 5: Applicera det nya mönstret
Till sist, tillämpa det nya mönstret på streckeffekten och spara ändringarna.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
Detta säkerställer att det nya mönstret tillämpas korrekt och att filen sparas med ändringarna.
## Steg 6: Verifiera ändringarna
För att se till att allt fungerade korrekt, ladda filen igen och verifiera ändringarna.
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
Det här steget verifierar att mönsterdata har tillämpats korrekt på streckeffekten.
## Slutsats
Och där har du det! Du har framgångsrikt lagt till ett strecklagermönster till en PSD-fil med Aspose.PSD för Java. Genom att följa dessa steg kan du enkelt anpassa och förbättra dina bilder. Glad kodning!
## FAQ's
### Vad är Aspose.PSD för Java?
Aspose.PSD för Java är ett bibliotek som låter utvecklare skapa, redigera och konvertera PSD-filer (Photoshop Document) programmatiskt.
### Kan jag använda Aspose.PSD för Java i ett kommersiellt projekt?
 Ja, du kan använda den i kommersiella projekt. Du kan köpa en licens från[här](https://purchase.aspose.com/buy).
### Finns det en gratis testversion tillgänglig för Aspose.PSD för Java?
 Ja, du kan ladda ner en gratis testversion från[här](https://releases.aspose.com/).
### Hur kan jag få support för Aspose.PSD för Java?
 Du kan få stöd från Asposes communityforum[här](https://forum.aspose.com/c/psd/34).
### Vilka är systemkraven för Aspose.PSD för Java?
Du behöver JDK installerat och en IDE för utveckling. Biblioteket stöder flera operativsystem inklusive Windows, Linux och macOS.