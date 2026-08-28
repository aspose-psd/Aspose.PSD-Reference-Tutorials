---
date: 2026-08-28
description: Voeg een pattern toe aan een laag in Java met Aspose.PSD. Volg deze stapsgewijze
  handleiding om een stroke layer effect toe te passen, pattern resources te configureren
  en uw PSD‑bestanden efficiënt op te slaan.
keywords:
- add pattern to layer
- java add layer effect
- Aspose.PSD stroke pattern
lastmod: 2026-08-28
linktitle: Hoe een Stroke Layer Pattern toe te voegen in Java
og_description: Pattern toevoegen aan een laag in Java met Aspose.PSD. Volg deze beknopte
  handleiding om een stroke layer effect toe te passen, pattern resources te configureren
  en uw PSD‑bestanden efficiënt op te slaan.
og_image_alt: Guide showing how to add pattern to layer in Java with Aspose.PSD
og_title: Pattern toevoegen aan laag in Java – Aspose.PSD tutorial
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
title: Hoe een pattern aan een laag toe te voegen in Java
url: /nl/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe een patroon aan een laag toe te voegen in Java

## Introductie
Add pattern to layer in Java is a common requirement when you need to enrich Photoshop PSD files with custom stroke effects. With Aspose.PSD for Java this task becomes straightforward, even if you’re new to the library. In this tutorial you’ll learn how to load a PSD, create a pattern resource, attach it to a stroke effect, and save the result—all with clear, step‑by‑step instructions.

## Snelle antwoorden
- **Which library is needed?** Aspose.PSD for Java.  
- **How long does implementation take?** About 10‑15 minutes for a basic pattern.  
- **Do I need a license?** A free trial works for development; a commercial license is required for production.  
- **Which Java version is supported?** JDK 8 or newer.  
- **Can I use this in a web service?** Yes, the API is platform‑agnostic and works in any Java environment.

## Wat betekent het toevoegen van een patroon aan een laag?
Adding a pattern to a layer means assigning a tiled bitmap to a stroke or fill effect so the graphic repeats across the shape’s outline. This technique is widely used for decorative borders, textures, and branding overlays, allowing designers to create consistent visual themes without manually drawing each element.

## Waarom Aspose.PSD voor deze taak gebruiken?
Aspose.PSD supports **30+ image formats** and can manipulate PSD files up to **2 GB** without loading the entire document into memory, delivering fast performance on typical server hardware. Its fluent API lets you work with layer effects programmatically, eliminating the need for Photoshop in automated pipelines.

## Vereisten
Before you start, ensure you have:
- Java Development Kit (JDK) 8 or newer installed.
- Aspose.PSD for Java – download it from the **Aspose.PSD for Java download page**([Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)) and add the JAR to your project’s classpath.
- An IDE such as IntelliJ IDEA or Eclipse for editing and running the sample code.
- A sample PSD file that contains a shape layer you want to modify.

## Importeer pakketten
First, import the namespaces that provide access to PSD objects, resources, and effects.

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

## Hoe een patroon aan een laag toe te voegen in Java?

Load the target PSD, create a pattern resource, attach it to the stroke effect of the desired layer, and finally save the file. This end‑to‑end flow takes just a few lines of code and works with any standard PSD that contains a vector shape layer.

### Stap 1: laad het PSD‑bestand
Loading the document gives you access to its layer hierarchy and effect collection.  
`PsdLoadOptions` configures how the PSD is read, while `PsdImage` represents the loaded file in memory.

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

By loading the PSD file, you can now access and manipulate its layers and effects.

### Stap 2: bereid nieuwe patroongegevens voor
Create a `PatternResource` that holds the bitmap you want to tile as a stroke pattern.  
`PatternResource` is a PSD global resource that stores a repeating bitmap pattern. `Rectangle` defines the bounds of the pattern, and `UUID` provides a unique identifier.

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

This pattern data will be used to create the new stroke effect.

### Stap 3: krijg toegang tot het stroke‑effect
Identify the shape layer that already has a stroke, then retrieve its `StrokeEffect` object.  
`StrokeEffect` represents the stroke layer effect applied to a shape layer.

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

This ensures you are working with the correct layer and effect.

### Stap 4: wijzig het stroke‑effect
Now update the stroke’s properties to reference the new pattern resource.

#### Update stroke‑effecteigenschappen
```
// Placeholder for original code.
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
```

#### Update de patroonresource
`PattResource` is a PSD global layer resource that stores pattern data.

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

These snippets replace the existing pattern with the one you supplied.

### Stap 5: pas het nieuwe patroon toe
`PatternFillSettings` holds the fill settings for a pattern‑based stroke effect. Commit the changes to the layer and write the updated PSD back to disk.

```
// Placeholder for original code.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
```

This ensures the new pattern is applied correctly and the file is saved with the changes.

### Stap 6: controleer de wijzigingen
Reload the file and inspect the stroke to confirm the pattern appears as expected.

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

This step verifies that the pattern data has been correctly applied to the stroke effect.

## Veelvoorkomende problemen en foutopsporing
- **Pattern not visible:** Ensure the pattern image’s DPI matches the PSD’s resolution, and that the stroke’s `Enabled` flag is set to `true`.  
- **Large PSD files cause OutOfMemoryError:** Use `PsdImage.load(..., LoadOptions)` with `LoadOptions.setLoadAllLayers(false)` to load layers on demand.  
- **Incorrect layer selected:** Verify the layer index or name before accessing its effects; you can enumerate `psdImage.getLayers()` to list available layers.

## Veelgestelde vragen

**Q: Wat is Aspose.PSD for Java?**  
A: Aspose.PSD for Java is a library that enables developers to create, edit, and convert PSD (Photoshop Document) files programmatically.

**Q: Kan ik Aspose.PSD for Java gebruiken in een commercieel project?**  
A: Ja, je kunt het gebruiken in commerciële projecten. Je kunt een licentie aanschaffen via de **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)).

**Q: Is er een gratis proefversie beschikbaar voor Aspose.PSD for Java?**  
A: Ja, je kunt een gratis proefversie downloaden van de **Aspose releases page**([Aspose releases page](https://releases.aspose.com/)).

**Q: Hoe kan ik ondersteuning krijgen voor Aspose.PSD for Java?**  
A: Je kunt ondersteuning krijgen via de Aspose community forums **here**([Aspose PSD community forum](https://forum.aspose.com/c/psd/34)).

**Q: Wat zijn de systeemvereisten voor Aspose.PSD for Java?**  
A: Je hebt een geïnstalleerde JDK en een IDE nodig voor ontwikkeling. De bibliotheek ondersteunt Windows, Linux en macOS.

## Conclusie
You’ve now learned how to add pattern to layer in Java using Aspose.PSD. By following the steps above you can programmatically enhance PSD files with custom stroke patterns, automate branding workflows, and integrate graphics processing into any Java‑based application. Explore other Aspose.PSD features such as layer merging, color adjustments, and export to PNG or JPEG to further extend your image‑processing toolkit.

---

**Last Updated:** 2026-08-28  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose

## Gerelateerde tutorials

- [Render Pattern Fill Layer Psd Files](/psd/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/)
- [Pattern Overlay PSD: Add Effects with Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [How to Change Stroke Color Java Using Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}