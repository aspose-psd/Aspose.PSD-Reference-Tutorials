---
date: 2026-01-14
description: Lär dig hur du skapar ett gradient‑strokelager och anpassar strokegraidenter
  i PSD‑filer med Aspose.PSD för Java i den här steg‑för‑steg‑handledningen.
linktitle: How to Create Gradient Stroke Layer in Java
second_title: Aspose.PSD Java API
title: Hur man skapar ett gradientlinjelager i Java
url: /sv/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Så skapar du gradient stroke layer i Java

## Introduktion
Har du någonsin funderat på hur du **skapar gradient stroke layer** i dina PSD‑filer med Java? Du har kommit till rätt ställe! Idag dyker vi ner i Aspose.PSD for Java – ett kraftfullt bibliotek som låter dig manipulera PSD‑filer utan ansträngning. Oavsett om du är ny inom grafikprogrammering eller vill finjustera befintliga designer, så guidar den här artikeln dig steg för steg genom att lägga till och anpassa stroke‑gradienter.

## Snabba svar
- **Vad är huvudmålet?** Skapa ett gradient stroke layer i en PSD‑fil.  
- **Vilket bibliotek krävs?** Aspose.PSD for Java.  
- **Behöver jag en licens?** Ja, en giltig (eller temporär) licens krävs för produktion.  
- **Vilken Java‑version fungerar?** Java 8 eller högre.  
- **Hur lång tid tar implementeringen?** Ungefär 10‑15 minuter för ett grundläggande gradient stroke.

## Vad är ett gradient stroke layer?
Ett gradient stroke layer är en vektorlinje runt en form eller text som övergår mjukt mellan färger. Med Aspose.PSD kan du programatiskt definiera färger, opacitet, vinkel och typ (linjär, radial osv.) för stroken.

## Varför använda Aspose.PSD för Java?
- **Fullt PSD‑stöd** – läs, redigera och skriv PSD‑filer utan Photoshop.  
- **Rik effekt‑API** – få åtkomst till stroke, skugga, glöd och många andra lagereffekter.  
- **Plattformsoberoende** – fungerar på alla OS som stödjer Java.  
- **Inga inhemska beroenden** – ren Java, enkelt att integrera i CI‑pipelines.

## Förutsättningar
1. **Java Development Kit (JDK)** – Installera den senaste JDK:n från [Oracle's website](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java** – Ladda ner biblioteket från [Aspose.PSD download page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse eller NetBeans.  
4. **Licens** – Skaffa en [temporary license](https://purchase.aspose.com/temporary-license/) om du inte har en fullständig licens.

## Importera paket
Först importerar vi de klasser vi behöver för att läsa PSD‑filen, komma åt effekter och konfigurera gradient‑fyllningar.

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

Nu delar vi upp processen i tydliga steg.

## Steg 1: Ladda PSD‑filen
Vi laddar käll‑PSD‑filen och aktiverar effekt‑resurser så att stroke‑effekten blir tillgänglig.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## Steg 2: Åtkomst till Stroke Effect
Förutsatt att den stroke vi vill ändra tillhör det tredje lagret (index 2), hämtar vi dess `StrokeEffect`.

```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```

## Steg 3: Verifiera Stroke Effect‑egenskaper
Innan vi gör ändringar bekräftar vi de befintliga inställningarna så att vi vet exakt vad vi uppdaterar.

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

## Steg 4: Ändra inställningarna för Gradient Fill
Här ändrar vi färg, opacitet, blandningsläge och andra egenskaper för att uppnå önskat utseende.

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
Vi lägger till nya färg‑ och transparenspunkter och justerar de befintliga för att forma gradienten.

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

## Steg 6: Spara den modifierade PSD‑filen
Efter alla justeringar skriver vi den uppdaterade filen tillbaka till disk.

```java
im.save(exportPath);
```

## Steg 7: Verifiera ändringarna
Läs in den sparade filen och kontrollera att varje egenskap speglar de förändringar vi gjort.

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

## Slutsats
Du vet nu hur du **skapar gradient stroke layer**‑effekter i PSD‑filer med Aspose.PSD for Java. Genom att ladda en PSD, komma åt stroke‑effekten, justera gradient‑fyllningsinställningarna och spara resultatet kan du programatiskt producera professionella grafik utan att någonsin öppna Photoshop.

## Vanliga frågor
### Vad är Aspose.PSD för Java?
Aspose.PSD för Java är ett bibliotek som låter utvecklare arbeta med PSD‑filer i Java‑applikationer och erbjuder funktioner för att skapa, manipulera och konvertera PSD‑filer.

### Behöver jag en licens för att använda Aspose.PSD för Java?
Ja, du behöver en giltig licens för att använda Aspose.PSD för Java. Du kan skaffa en [temporary license](https://purchase.aspose.com/temporary-license/) för utvärderingsändamål.

### Kan jag använda Aspose.PSD för Java för att skapa PSD‑filer från grunden?
Absolut! Aspose.PSD för Java tillhandahåller omfattande API:er för att skapa och manipulera PSD‑filer programatiskt.

### Är det möjligt att applicera andra effekter med Aspose.PSD för Java?
Ja, du kan applicera olika effekter som skugga, glöd och mer med Aspose.PSD för Java.

### Var kan jag hitta dokumentationen för Aspose.PSD för Java?
Du kan hitta dokumentationen [here](https://reference.aspose.com/psd/java/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Senast uppdaterad:** 2026-01-14  
**Testat med:** Aspose.PSD for Java 24.11  
**Författare:** Aspose