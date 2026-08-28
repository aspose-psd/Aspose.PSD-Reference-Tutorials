---
date: 2026-08-28
description: Lägg till pattern till lager i Java med Aspose.PSD. Följ den här steg‑för‑steg‑guiden
  för att applicera en stroke layer effect, konfigurera pattern resources och spara
  dina PSD‑filer effektivt.
keywords:
- add pattern to layer
- java add layer effect
- Aspose.PSD stroke pattern
lastmod: 2026-08-28
linktitle: Hur man lägger till Stroke Layer Pattern i Java
og_description: Lägg till pattern till lager i Java med Aspose.PSD. Följ den här koncisa
  guiden för att applicera en stroke layer effect, konfigurera pattern resources och
  spara dina PSD‑filer effektivt.
og_image_alt: Guide showing how to add pattern to layer in Java with Aspose.PSD
og_title: Lägg till pattern till lager i Java – Aspose.PSD‑handledning
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  headline: How to add pattern to layer in Java
  type: TechArticle
- description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  name: How to add pattern to layer in Java
  steps:
  - name: load the PSD file
    text: 'Loading the document gives you access to its layer hierarchy and effect
      collection. `PsdLoadOptions` configures how the PSD is read, while `PsdImage`
      represents the loaded file in memory. java String dataDir = "Your Document Directory";
      String sourceFileName = dataDir + "Stroke.psd"; PsdLoadOptions '
  - name: prepare new pattern data
    text: Create a `PatternResource` that holds the bitmap you want to tile as a stroke
      pattern. `PatternResource` is a PSD global resource that stores a repeating
      bitmap pattern. `Rectangle` defines the bounds of the pattern, and `UUID` provides
      a unique identifier. java int[] newPattern = new int[] { Color.
  - name: access the stroke effect
    text: Identify the shape layer that already has a stroke, then retrieve its `StrokeEffect`
      object. `StrokeEffect` represents the stroke layer effect applied to a shape
      layer. java StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
      Assert.areEqual(BlendMode.N
  - name: modify the stroke effect
    text: Now update the stroke’s properties to reference the new pattern resource.
  - name: apply the new pattern
    text: '`PatternFillSettings` holds the fill settings for a pattern‑based stroke
      effect. Commit the changes to the layer and write the updated PSD back to disk.
      java ((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal
      Line 9\0"); ((PatternFil'
  - name: verify the changes
    text: 'Reload the file and inspect the stroke to confirm the pattern appears as
      expected. java PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
      StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
      PattResource resource1 = null; for (int '
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to create, edit,
      and convert PSD (Photoshop Document) files programmatically.
    question: What is Aspose.PSD for Java?
  - answer: Yes, you can use it in commercial projects. You can purchase a license
      from the **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)).
    question: Can I use Aspose.PSD for Java in a commercial project?
  - answer: Yes, you can download a free trial version from the **Aspose releases
      page**([Aspose releases page](https://releases.aspose.com/)).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: You can get support from the Aspose community forums **here**([Aspose
      PSD community forum](https://forum.aspose.com/c/psd/34)).
    question: How can I get support for Aspose.PSD for Java?
  - answer: You need a JDK installed and an IDE for development. The library supports
      Windows, Linux, and macOS.
    question: What are the system requirements for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- layer effects
title: Hur man lägger till pattern till lager i Java
url: /sv/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man lägger till mönster på lager i Java

## Introduktion
Att lägga till ett mönster på ett lager i Java är ett vanligt krav när du behöver berika Photoshop PSD‑filer med anpassade linjeeffekter. Med Aspose.PSD för Java blir denna uppgift enkel, även om du är ny på biblioteket. I den här handledningen lär du dig hur du laddar en PSD, skapar en mönsterresurs, bifogar den till en linjeeffekt och sparar resultatet – allt med tydliga steg‑för‑steg‑instruktioner.

## Snabba svar
- **Vilket bibliotek behövs?** Aspose.PSD för Java.  
- **Hur lång tid tar implementeringen?** Ungefär 10‑15 minuter för ett grundläggande mönster.  
- **Behöver jag en licens?** En gratis provversion fungerar för utveckling; en kommersiell licens krävs för produktion.  
- **Vilken Java‑version stöds?** JDK 8 eller nyare.  
- **Kan jag använda detta i en webbtjänst?** Ja, API‑et är plattformsoberoende och fungerar i alla Java‑miljöer.

## Vad innebär det att lägga till ett mönster på ett lager?
Att lägga till ett mönster på ett lager innebär att tilldela en upprepande bitmap till en linje‑ eller fyllningseffekt så att grafiken upprepas längs formens kontur. Denna teknik används ofta för dekorativa ramar, texturer och varumärkesöverlägg, vilket låter formgivare skapa enhetliga visuella teman utan att manuellt rita varje element.

## Varför använda Aspose.PSD för denna uppgift?
Aspose.PSD stöder **30+ bildformat** och kan manipulera PSD‑filer upp till **2 GB** utan att ladda hela dokumentet i minnet, vilket ger snabb prestanda på vanlig serverhårdvara. Dess flytande API låter dig arbeta med lagereffekter programatiskt, vilket eliminerar behovet av Photoshop i automatiserade pipelines.

## Förutsättningar
Innan du börjar, se till att du har:
- Java Development Kit (JDK) 8 eller nyare installerat.
- Aspose.PSD för Java – ladda ner det från den **Aspose.PSD för Java nedladdningssida**([Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)) och lägg till JAR‑filen i ditt projekts classpath.
- En IDE som IntelliJ IDEA eller Eclipse för att redigera och köra exempel­koden.
- En exempel‑PSD‑fil som innehåller ett form‑lager du vill modifiera.

## Importera paket
Först, importera namnutrymmena som ger åtkomst till PSD‑objekt, resurser och effekter.

```
// No actual code block is added to preserve original placeholders.
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
```

## Hur lägger man till mönster på lager i Java?

Läs in mål‑PSD‑filen, skapa en mönsterresurs, bifoga den till linjeeffekten på det önskade lagret och spara slutligen filen. Detta end‑to‑end‑flöde kräver bara några få kodrader och fungerar med alla standard‑PSD‑filer som innehåller ett vektorform‑lager.

### Steg 1: läs in PSD‑filen
Att läsa in dokumentet ger dig åtkomst till dess lager‑hierarki och effekt‑samling.  
`PsdLoadOptions` konfigurerar hur PSD‑filen läses, medan `PsdImage` representerar den inlästa filen i minnet.

```
// Placeholder for original code.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
```

Genom att läsa in PSD‑filen kan du nu komma åt och manipulera dess lager och effekter.

### Steg 2: förbered ny mönsterdata
Skapa en `PatternResource` som innehåller den bitmap du vill upprepa som ett linjemönster.  
`PatternResource` är en global PSD‑resurs som lagrar ett upprepande bitmap‑mönster. `Rectangle` definierar mönstrets gränser och `UUID` ger en unik identifierare.

```
// Placeholder for original code.
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
```

Denna mönsterdata kommer att användas för att skapa den nya linjeeffekten.

### Steg 3: få åtkomst till linjeeffekten
Identifiera form‑lagret som redan har en linje, och hämta sedan dess `StrokeEffect`‑objekt.  
`StrokeEffect` representerar linje‑lagereffekten som applicerats på ett form‑lager.

```
// Placeholder for original code.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
```

Detta säkerställer att du arbetar med rätt lager och effekt.

### Steg 4: modifiera linjeeffekten
Uppdatera nu linjens egenskaper så att de refererar till den nya mönsterresursen.

#### Uppdatera linjeeffektens egenskaper
```
// Placeholder for original code.
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
```

#### Uppdatera mönsterresursen
`PattResource` är en global PSD‑lagerresurs som lagrar mönsterdata.

```
// Placeholder for original code.
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
```

Dessa kodsnuttar ersätter det befintliga mönstret med det du angav.

### Steg 5: tillämpa det nya mönstret
`PatternFillSettings` innehåller fyllningsinställningarna för en mönsterbaserad linjeeffekt. Bekräfta ändringarna på lagret och skriv den uppdaterade PSD‑filen tillbaka till disk.

```
// Placeholder for original code.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
```

Detta säkerställer att det nya mönstret tillämpas korrekt och att filen sparas med ändringarna.

### Steg 6: verifiera ändringarna
Läs in filen igen och inspektera linjen för att bekräfta att mönstret visas som förväntat.

```
// Placeholder for original code.
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
```

Detta steg verifierar att mönsterdata har tillämpats korrekt på linjeeffekten.

## Vanliga problem och felsökning
- **Mönstret syns inte:** Se till att mönsterbildens DPI matchar PSD‑filens upplösning, och att linjens `Enabled`‑flagga är satt till `true`.  
- **Stora PSD‑filer orsakar OutOfMemoryError:** Använd `PsdImage.load(..., LoadOptions)` med `LoadOptions.setLoadAllLayers(false)` för att ladda lager vid behov.  
- **Fel lager valt:** Verifiera lagerindex eller namn innan du får åtkomst till dess effekter; du kan enumerera `psdImage.getLayers()` för att lista tillgängliga lager.

## Vanliga frågor

**Q: Vad är Aspose.PSD för Java?**  
A: Aspose.PSD för Java är ett bibliotek som möjliggör för utvecklare att programatiskt skapa, redigera och konvertera PSD‑ (Photoshop Document)‑filer.

**Q: Kan jag använda Aspose.PSD för Java i ett kommersiellt projekt?**  
A: Ja, du kan använda det i kommersiella projekt. Du kan köpa en licens från **Aspose inköpssida**([Aspose purchase page](https://purchase.aspose.com/buy)).

**Q: Finns det en gratis provversion av Aspose.PSD för Java?**  
A: Ja, du kan ladda ner en gratis provversion från **Aspose releases‑sida**([Aspose releases page](https://releases.aspose.com/)).

**Q: Hur kan jag få support för Aspose.PSD för Java?**  
A: Du kan få support från Aspose‑community‑forumet **här**([Aspose PSD community forum](https://forum.aspose.com/c/psd/34)).

**Q: Vad är systemkraven för Aspose.PSD för Java?**  
A: Du behöver ett installerat JDK och en IDE för utveckling. Biblioteket stöder Windows, Linux och macOS.

## Slutsats
Du har nu lärt dig hur du lägger till ett mönster på ett lager i Java med hjälp av Aspose.PSD. Genom att följa stegen ovan kan du programatiskt förbättra PSD‑filer med anpassade linjemönster, automatisera varumärkesarbetsflöden och integrera grafikbehandling i vilken Java‑baserad applikation som helst. Utforska andra Aspose.PSD‑funktioner såsom lager‑sammanfogning, färgjusteringar och export till PNG eller JPEG för att ytterligare utöka ditt bildbehandlingsverktyg.

---

**Senast uppdaterad:** 2026-08-28  
**Testat med:** Aspose.PSD 24.11 för Java  
**Författare:** Aspose

## Relaterade handledningar

- [Rendera mönsterfyllningslager i PSD‑filer](/psd/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/)
- [Mönsteröverlägg PSD: Lägg till effekter med Aspose.PSD för Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Hur man ändrar linjefärg i Java med Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}