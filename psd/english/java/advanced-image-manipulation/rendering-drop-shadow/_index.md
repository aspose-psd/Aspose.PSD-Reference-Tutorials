---
date: 2026-11-04
description: Learn how to save PSD as PNG, export PNG with alpha, and add a drop shadow
  layer using Aspose.PSD for Java – a complete, step‑by‑step guide.
images:
- /java/advanced-image-manipulation/rendering-drop-shadow/og-image.png
keywords:
- save psd as png
- convert psd to png
- export png with alpha
- batch psd to png
- java image manipulation
lastmod: 2026-11-04
linktitle: Apply Rendering Drop Shadow
og_description: Save psd as png with Aspose.PSD for Java, export PNG with alpha transparency,
  and add a rendering drop shadow—step‑by‑step guide for Java developers.
og_image_alt: Developer guide showing how to convert PSD to PNG and apply drop shadow
  using Aspose.PSD Java
og_title: Save psd as png and apply rendering drop shadow in Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to save PSD as PNG, export PNG with alpha, and add a drop
    shadow layer using Aspose.PSD for Java – a complete, step‑by‑step guide.
  headline: Save psd as png and apply rendering drop shadow in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG, export PNG with alpha, and add a drop
    shadow layer using Aspose.PSD for Java – a complete, step‑by‑step guide.
  name: Save psd as png and apply rendering drop shadow in Aspose.PSD for Java
  steps:
  - name: define document directory
    text: Define the directory path where your PSD files are stored.
  - name: set psd and png file paths
    text: Specify the full file paths for the source PSD and the target PNG.
  - name: load psd file with effects
    text: '`PsdImage` loads the PSD and gives access to its layers and effects.'
  - name: access drop shadow effect
    text: '`DropShadowEffect` represents a drop‑shadow layer effect that can be read
      or modified.'
  - name: validate shadow effect properties
    text: '`shadowEffect` holds the properties of the drop‑shadow such as opacity,
      distance, and size. > **Pro tip:** Adjust `setSpread()` or `setNoise()` to create
      softer or more textured shadows.'
  - name: save as png – the “save psd as png” step
    text: '`PngOptions` configures PNG export settings, including color type and alpha
      channel handling. At this point you have successfully **converted psd to png**,
      **exported png with alpha**, and applied a rendering drop shadow in a single
      workflow.'
  type: HowTo
- questions:
  - answer: Yes. Loop through `im.getLayers()` and add or modify a `DropShadowEffect`
      for each target layer, which also lets you perform a batch psd to png conversion.
    question: Can I apply drop shadows to multiple layers simultaneously?
  - answer: '`Spread` determines how abruptly the shadow transitions from full opacity
      to transparent. A higher value creates a harder edge.'
    question: What does the ‘Spread’ parameter control?
  - answer: Aspose.PSD supports PSD files from Photoshop 3.0 up to the latest release,
      handling most layer types and effects.
    question: Is Aspose.PSD compatible with all Photoshop versions?
  - answer: Download the free trial from the [Aspose.PSD download page](https://releases.aspose.com/psd/java/)
      and run the sample without a license key.
    question: How can I test the code before purchasing a license?
  - answer: Post your question on the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)
      where the community and Aspose engineers can assist.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- save psd as png
- aspose psd java
- java image manipulation
- png transparency
- rendering drop shadow
title: Save psd as png and apply rendering drop shadow in Aspose.PSD for Java
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Save psd as png and apply rendering drop shadow in Aspose.PSD for Java

## Introduction

If you're working with Photoshop files in Java, **saving psd as png** is one of the most common tasks you’ll encounter. In many projects you’ll need to **save psd as png** to ship assets to the web or mobile apps, while preserving transparency and visual effects. With Aspose.PSD you can not only **convert psd to png** but also enhance the image by **adding a drop shadow layer**. In this tutorial we’ll walk through the entire process—loading a PSD, applying a rendering drop shadow, and finally **saving the PSD as a PNG** file—so you can integrate the workflow into your own projects with confidence.

## Quick answers
- **What library handles PSD to PNG conversion?** Aspose.PSD for Java.  
- **How long does the drop‑shadow implementation take?** About 10‑15 minutes for a basic example.  
- **Do I need a license to run the code?** A free trial works for evaluation; a license is required for production.  
- **Can I apply the shadow to multiple layers?** Yes—just loop through the desired layers, which also lets you perform a batch psd to png conversion.  
- **Which Java version is required?** Java 8 or higher.

## What is “save psd as png” and why does it matter?

**Saving a PSD as PNG creates a widely‑supported, lossless image that retains transparency.** This format is essential when you need to display Photoshop assets on the web, in mobile apps, or as part of a larger image‑processing pipeline. Adding a drop shadow at the same time lets you produce a polished visual effect without opening Photoshop.

## Why use Aspose.PSD for this workflow?

Load‑time rendering of layer effects is built‑in, so you don’t need Photoshop. Aspose.PSD supports over 50 input and output formats (PSD, PNG, JPEG, TIFF, BMP) and can process large documents without loading the whole file into memory. It preserves effects like drop shadows and glows exactly as they appear, and automatically exports PNG with alpha transparency.

## Prerequisites

Before we dive in, make sure you have:

- **Java Development Environment** – JDK 8 or newer installed.  
- **Aspose.PSD for Java** – Download the latest JAR from the [Aspose.PSD download page](https://releases.aspose.com/psd/java/).  
- **A PSD file** – The file should contain at least one layer you want to enhance with a drop shadow (e.g., *Shadow.psd*).  

## Import packages

The `com.aspose.psd` namespace provides the core classes for loading images, manipulating layers, and exporting PNG files.  
`PsdImage` is the main class used to load and manipulate PSD files.  

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

## Step‑by‑step guide

### Step 1: define document directory
Define the directory path where your PSD files are stored.  

```java
String dataDir = "Your Document Directory";
```

### Step 2: set psd and png file paths
Specify the full file paths for the source PSD and the target PNG.  

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Step 3: load psd file with effects
`PsdImage` loads the PSD and gives access to its layers and effects.  

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Step 4: access drop shadow effect
`DropShadowEffect` represents a drop‑shadow layer effect that can be read or modified.  

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Step 5: validate shadow effect properties
`shadowEffect` holds the properties of the drop‑shadow such as opacity, distance, and size.  

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

> **Pro tip:** Adjust `setSpread()` or `setNoise()` to create softer or more textured shadows.

### Step 6: save as png – the “save psd as png” step
`PngOptions` configures PNG export settings, including color type and alpha channel handling.  

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

At this point you have successfully **converted psd to png**, **exported png with alpha**, and applied a rendering drop shadow in a single workflow.

## Export png with alpha transparency

When you need the PNG output to retain its transparent background—especially for UI overlays or web graphics—make sure you use `PngColorType.TruecolorWithAlpha` as shown in the save step above. This guarantees that the drop shadow sits on a transparent canvas rather than a solid background, helping you **preserve png transparency**.

## Add drop shadow layer using Java

If your PSD contains multiple layers that require shadows, simply repeat **Step 4** and **Step 5** inside a loop that iterates over `im.getLayers()`. Each iteration can create or modify a `DropShadowEffect` instance, giving you fine‑grained control over opacity, distance, size, and angle per layer. This approach also enables a **batch psd to png** conversion where every file receives the same shadow treatment.

## Common use cases for saving psd as png

* **Web asset pipelines** – Convert designer‑provided PSDs into web‑ready PNGs with built‑in shadows.  
* **Mobile app resources** – Generate transparent PNG icons on the fly, avoiding manual export.  
* **Batch processing** – Automate conversion of hundreds of PSD files in a server‑side job, ensuring each PNG keeps its alpha channel and visual effects.  

## Common issues and solutions

| Issue | Likely cause | Fix |
|-------|--------------|-----|
| **Shadow not visible** | `Opacity` set to 0 or layer is hidden | Verify `shadowEffect.getOpacity()` > 0 and layer visibility. |
| **PNG appears flat (no transparency)** | Wrong `PngColorType` used | Use `PngColorType.TruecolorWithAlpha` as shown. |
| **Exception on loading** | Effects not loaded | Ensure `loadOptions.setLoadEffectsResource(true)` is called. |
| **Incorrect layer index** | PSD structure differs | Inspect `im.getLayers()` and pick the correct index. |

## Frequently asked questions

**Q: Can I apply drop shadows to multiple layers simultaneously?**  
A: Yes. Loop through `im.getLayers()` and add or modify a `DropShadowEffect` for each target layer, which also lets you perform a batch psd to png conversion.

**Q: What does the ‘Spread’ parameter control?**  
A: `Spread` determines how abruptly the shadow transitions from full opacity to transparent. A higher value creates a harder edge.

**Q: Is Aspose.PSD compatible with all Photoshop versions?**  
A: Aspose.PSD supports PSD files from Photoshop 3.0 up to the latest release, handling most layer types and effects.

**Q: How can I test the code before purchasing a license?**  
A: Download the free trial from the [Aspose.PSD download page](https://releases.aspose.com/psd/java/) and run the sample without a license key.

**Q: Where can I get help if I run into problems?**  
A: Post your question on the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) where the community and Aspose engineers can assist.

## Conclusion

You now know how to **save psd as png**, **export png with alpha**, **convert psd to png**, and **apply a drop shadow layer** using Aspose.PSD for Java. This combination lets you automate high‑quality image preparation for web, mobile, or desktop applications—without ever opening Photoshop.

---

**Last Updated:** 2026-11-04  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose

## Related Tutorials

- [Convert PSD to PNG with Color Overlay – Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)
- [How to Add Shadow in PSD Using Java – Advanced Layer Effects](/psd/java/advanced-psd-layer-features-effects/)
- [How to Convert PSD to Raster Image Formats with Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}