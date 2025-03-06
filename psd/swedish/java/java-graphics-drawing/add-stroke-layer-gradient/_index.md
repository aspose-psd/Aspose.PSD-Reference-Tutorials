---
title: Hur man lägger till Stroke Layer Gradient i Java
linktitle: Hur man lägger till Stroke Layer Gradient i Java
second_title: Aspose.PSD Java API
description: Lär dig hur du lägger till och anpassar linjeskiktsgradienter i PSD-filer med Aspose.PSD för Java med denna omfattande steg-för-steg handledning.
weight: 10
url: /sv/java/java-graphics-drawing/add-stroke-layer-gradient/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man lägger till Stroke Layer Gradient i Java

## Introduktion
Har du någonsin undrat hur man lägger till en linjelagergradient till dina bilder med Java? Tja, du är på rätt plats! Idag dyker vi in i världen av Aspose.PSD för Java, ett kraftfullt bibliotek som hjälper dig att manipulera PSD-filer med lätthet. Oavsett om du är nybörjare eller en erfaren utvecklare, kommer den här steg-för-steg-guiden att leda dig genom processen att lägga till en linjelagergradient till dina PSD-filer. Så, spänn fast dig och gör dig redo att förbättra dina grafiska redigeringsfärdigheter!
## Förutsättningar
Innan vi sätter igång är det några saker du måste ha på plats. Se till att du har följande:
1.  Java Development Kit (JDK): Se till att du har JDK installerat på ditt system. Du kan ladda ner den från[Oracles hemsida](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD för Java Library: Du kan ladda ner det från[Aspose.PSD nedladdningssida](https://releases.aspose.com/psd/java/).
3. En integrerad utvecklingsmiljö (IDE): Alla IDE som IntelliJ IDEA, Eclipse eller NetBeans kommer att fungera.
4.  En giltig licens: Du kan få en[tillfällig licens](https://purchase.aspose.com/temporary-license/) om du inte har en full.
## Importera paket
Först till kvarn, låt oss importera de nödvändiga paketen. Dessa kommer att göra det möjligt för oss att använda de klasser och metoder som krävs för att manipulera PSD-filen.
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
Låt oss nu dela upp exemplet i flera steg för bättre förståelse.
## Steg 1: Ladda PSD-filen
 Först måste vi ladda PSD-filen som vi vill ändra. Vi kommer att använda`PsdLoadOptions` för att ange att vi vill ladda effektresurserna.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## Steg 2: Få tillgång till Stroke Effect
Därefter måste vi komma åt streckeffekten för lagret vi är intresserade av. Här antar vi att det är det tredje lagret (index 2) i PSD-filen.
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## Steg 3: Verifiera egenskaper för strokeeffekt
Innan vi gör några ändringar, låt oss verifiera egenskaperna för slageffekten för att säkerställa att vi ändrar de korrekta inställningarna.
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
## Steg 4: Ändra inställningarna för gradientfyllning
Nu är det dags att ändra inställningarna för gradientfyllning enligt våra krav. Vi kommer att ändra färg, opacitet, blandningsläge och andra egenskaper.
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
## Steg 5: Lägg till och ändra färg- och transparenspunkter
Låt oss lägga till nya färg- och transparenspunkter och modifiera de befintliga för att uppnå önskad gradienteffekt.
```java
// Lägg till ny färgpunkt
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Ändra plats för föregående punkt
fillSettings.getColorPoints()[1].setLocation(1899);
// Lägg till ny transparenspunkt
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Ändra plats för tidigare transparenspunkt
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## Steg 6: Spara den modifierade PSD-filen
Efter att ha gjort alla nödvändiga ändringar måste vi spara PSD-filen.
```java
im.save(exportPath);
```
## Steg 7: Verifiera ändringarna
Slutligen, låt oss ladda den sparade PSD-filen och verifiera att våra ändringar har tillämpats korrekt.
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Kontrollera färgpunkter
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
// Kontrollera transparenspunkter
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
## Slutsats
Och där har du det! Du vet nu hur du lägger till och manipulerar linjeskiktsgradienter i PSD-filer med Aspose.PSD för Java. Denna handledning omfattade att ladda PSD-filen, komma åt och ändra slageffekter och spara ändringarna. Med dessa färdigheter kan du skapa visuellt tilltalande gradienter och anpassa dina PSD-filer för att passa dina behov.
## FAQ's
### Vad är Aspose.PSD för Java?
Aspose.PSD för Java är ett bibliotek som gör det möjligt för utvecklare att arbeta med PSD-filer i Java-applikationer, vilket ger funktioner för att skapa, manipulera och konvertera PSD-filer.
### Behöver jag en licens för att använda Aspose.PSD för Java?
 Ja, du behöver en giltig licens för att använda Aspose.PSD för Java. Du kan få en[tillfällig licens](https://purchase.aspose.com/temporary-license/) i utvärderingssyfte.
### Kan jag använda Aspose.PSD för Java för att skapa PSD-filer från början?
Absolut! Aspose.PSD för Java tillhandahåller omfattande API:er för att skapa och manipulera PSD-filer programmatiskt.
### Är det möjligt att använda andra effekter med Aspose.PSD för Java?
Ja, du kan använda olika effekter som skugga, glöd och mer med Aspose.PSD för Java.
### Var kan jag hitta dokumentationen för Aspose.PSD för Java?
 Du hittar dokumentationen[här](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
