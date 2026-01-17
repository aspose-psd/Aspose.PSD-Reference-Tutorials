---
date: 2026-01-17
description: Lär dig hur du lägger till streckmönster i Java med Aspose.PSD för Java.
  Följ den här steg‑för‑steg‑guiden för att snabbt förbättra dina PSD‑bilder.
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: Hur man lägger till linjemönster i Java med Aspose.PSD
url: /sv/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man lägger till strokemönster i Java med Aspose.PSD

## Introduktion
Om du behöver **add stroke pattern java** till en Photoshop-fil, gör Aspose.PSD for Java det förvånansvärt enkelt. Oavsett om du bygger ett grafisk‑designverktyg, automatiserar batch‑redigeringar, eller bara experimenterar med lagereffekter, guidar den här handledningen dig genom varje steg—från att ladda PSD-filen till att verifiera det nya mönstret. Låt oss dyka ner och se hur snabbt du kan förbättra dina bilder.

## Snabba svar
- **Vilket bibliotek behöver jag?** Aspose.PSD for Java  
- **Vilken Java-version stöds?** JDK 8 eller senare  
- **Behöver jag en licens för testning?** En gratis provversion fungerar för utveckling; en licens krävs för produktion  
- **Hur lång tid tar implementeringen?** Ungefär 10‑15 minuter för ett grundläggande mönsterstrok  
- **Kan jag återanvända mönstret på flera lager?** Ja, tilldela bara samma `PattResource` till andra lager  

## Vad är add stroke pattern java?
Att lägga till ett strokemönster i Java innebär att applicera en anpassad fyllning (ofta en repeterande bitmap) på ett lagers strok‑effekt. Denna teknik låter dig skapa stiliserade konturer—tänk på en streckad linje, en tegeltextur eller en anpassad grafisk ram—direkt i en PSD-fil utan att öppna Photoshop.

## Varför använda Aspose.PSD för add stroke pattern java?
- **Full PSD‑fidelity** – Alla lagereffekter, resurser och blandningslägen bevaras.  
- **Ingen inbyggd Photoshop krävs** – Fungerar på alla OS med en JDK.  
- **Programmatisk kontroll** – Automatisera batch‑behandling eller integrera i server‑sidiga tjänster.  
- **Rik API** – Tillgång till globala resurser, mönsterfyllningar och blandningslägen i ett enda flytande gränssnitt.

## Förutsättningar
- **Java Development Kit (JDK)** – Se till att JDK 8 eller nyare är installerat.  
- **Aspose.PSD for Java** – Ladda ner biblioteket från [here](https://releases.aspose.com/psd/java/) och lägg till JAR‑filen i ditt projekts classpath.  
- **IDE** – IntelliJ IDEA, Eclipse eller någon annan editor du föredrar.

## Importera paket
Först, importera de klasser du behöver för att hantera PSD‑filer, färger, rektanglar och strok‑effekter.

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

## Steg 1: Ladda PSD‑filen
Ladda käll‑PSD‑filen så att du kan arbeta med dess lager och resurser.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Steg 2: Förbered ny mönsterdata
Skapa ett enkelt 4 × 4‑pixelers mönster som kommer att användas för strok‑effekten.

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

## Steg 3: Åtkomst till strok‑effekten
Hitta strok‑effekten på mål‑lagret (i detta exempel, det fjärde lagret).

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## Steg 4: Modifiera strok‑effekten
### Uppdatera strok‑effektens egenskaper
Justera opacitet och blandningsläge för att se den visuella påverkan av det nya mönstret.

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### Uppdatera mönsterresursen
Byt ut den befintliga globala mönsterresursen mot den du just skapade.

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

## Steg 5: Applicera det nya mönstret
Koppla den uppdaterade mönsterresursen till strok‑effekten och spara PSD‑filen.

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Steg 6: Verifiera förändringarna
Läs in filen igen och bekräfta att det nya mönstret, opaciteten och blandningsläget har tillämpats korrekt.

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

## Vanliga problem och lösningar
| Problem | Orsak | Lösning |
|---------|-------|---------|
| Mönstret visas inte | Fel `PatternId`‑referens | Se till att `PatternId` som sätts på `PattResource` matchar den som används i `PatternFillSettings`. |
| Strok försvinner efter sparning | Opacitet satt till 0 eller effekt dold | Verifiera att `setOpacity` är mellan 0‑255 och att `isVisible()` returnerar `true`. |
| Oväntade färger | Blandningsläge matchar inte | Använd `BlendMode.Color` (eller ett annat läge) som matchar din designavsikt. |

## Vanliga frågor
### Vad är Aspose.PSD for Java?
Aspose.PSD for Java är ett bibliotek som låter utvecklare skapa, redigera och konvertera PSD‑filer (Photoshop Document) programatiskt.

### Kan jag använda Aspose.PSD for Java i ett kommersiellt projekt?
Ja, du kan använda det i kommersiella projekt. Du kan köpa en licens från [here](https://purchase.aspose.com/buy).

### Finns det en gratis provversion tillgänglig för Aspose.PSD for Java?
Ja, du kan ladda ner en gratis provversion från [here](https://releases.aspose.com/).

### Hur kan jag få support för Aspose.PSD for Java?
Du kan få support från Aspose‑community‑forumet [here](https://forum.aspose.com/c/psd/34).

### Vad är systemkraven för Aspose.PSD for Java?
Du behöver ha JDK installerat och en IDE för utveckling. Biblioteket stödjer flera operativsystem inklusive Windows, Linux och macOS.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-17  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose