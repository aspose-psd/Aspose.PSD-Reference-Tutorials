---
title: Save PSD as PNG and Apply Rendering Drop Shadow in Aspose.PSD for Java
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
description: Learn how to save PSD as PNG, export PNG with alpha, and add a drop shadow layer using Aspose.PSD for Java – a complete, step‑by‑step guide.
weight: 16
url: /java/advanced-image-manipulation/rendering-drop-shadow/
date: 2026-04-22
keywords:
- save psd as png
- convert psd to png
- export png with alpha
- batch psd to png
- preserve png transparency
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Save PSD as PNG and Apply Rendering Drop Shadow in Aspose.PSD for Java

## Introduction

If you're working with Photoshop files in Java, **saving PSD as PNG** is one of the most common tasks you’ll encounter. In many projects you’ll need to **save psd as png** to ship assets to the web or mobile apps, while preserving transparency and visual effects. With Aspose.PSD you can not only **convert PSD to PNG** but also enhance the image by **adding a drop shadow layer**. In this tutorial we’ll walk through the entire process—loading a PSD, applying a rendering drop shadow, and finally **saving the PSD as a PNG** file—so you can integrate the workflow into your own projects with confidence.

## Quick Answers
- **What library handles PSD to PNG conversion?** Aspose.PSD for Java.  
- **How long does the drop‑shadow implementation take?** About 10‑15 minutes for a basic example.  
- **Do I need a license to run the code?** A free trial works for evaluation; a license is required for production.  
- **Can I apply the shadow to multiple layers?** Yes—just loop through the desired layers, which also lets you perform a batch psd to png conversion.  
- **Which Java version is required?** Java 8 or higher.

## What is “save PSD as PNG” and why does it matter?

**Saving a PSD as PNG** creates a widely‑supported, lossless image that retains transparency. This is essential when you need to display Photoshop assets on the web, in mobile apps, or as part of a larger image‑processing pipeline. Adding a drop shadow at the same time lets you produce a polished visual effect without opening Photoshop.

## Why use Aspose.PSD for this workflow?

* **Full control from code** – No need to launch Photoshop or rely on external tools.  
* **Preserves layer effects** – Drop shadows, glows, and other effects are rendered exactly as they appear in the original file.  
* **Export PNG with alpha** – The PNG output keeps the transparent background, ensuring you **preserve PNG transparency** for UI or web use.  
* **Cross‑platform** – Works on any OS that supports Java 8+.  

## Prerequisites

Before we dive in, make sure you have:

- **Java Development Environment** – JDK 8 or newer installed.  
- **Aspose.PSD for Java** – Download the latest JAR from the [Aspose.PSD download page](https://releases.aspose.com/psd/java/).  
- **A PSD file** – The file should contain at least one layer you want to enhance with a drop shadow (e.g., *Shadow.psd*).  

## Import Packages

First, import the classes we’ll need. This gives us access to image loading, layer effects, and PNG export options.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

## Step‑by‑Step Guide

### Step 1: Define Document Directory  
Tell the program where your source PSD lives.

```java
String dataDir = "Your Document Directory";
```

### Step 2: Set PSD and PNG File Paths  
Specify both the input PSD and the output PNG that will contain the rendered drop shadow.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Step 3: Load PSD File with Effects  
Enable the loading of effect resources so that we can manipulate the drop‑shadow effect.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Step 4: Access Drop Shadow Effect  
Grab the first drop‑shadow effect from the second layer (index 1). This is where we’ll verify or modify the parameters.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Step 5: Validate Shadow Effect Properties  
Make sure the effect’s properties match what you expect before saving. You can also tweak these values to achieve a different look.

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

### Step 6: Save as PNG – the “save PSD as PNG” step  
Export the modified image to PNG, preserving the alpha channel so the shadow blends correctly.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

At this point you have successfully **converted PSD to PNG**, **exported PNG with alpha**, and applied a rendering drop shadow in a single workflow.

## Export PNG with Alpha Transparency

When you need the PNG output to retain its transparent background—especially for UI overlays or web graphics—make sure you use `PngColorType.TruecolorWithAlpha` as shown in the save step above. This guarantees that the drop shadow sits on a transparent canvas rather than a solid background, helping you **preserve PNG transparency**.

## Add Drop Shadow Layer Using Java

If your PSD contains multiple layers that require shadows, simply repeat **Step 4** and **Step 5** inside a loop that iterates over `im.getLayers()`. Each iteration can create or modify a `DropShadowEffect` instance, giving you fine‑grained control over opacity, distance, size, and angle per layer. This approach also enables a **batch psd to png** conversion where every file receives the same shadow treatment.

## Common Use Cases for Saving PSD as PNG

* **Web asset pipelines** – Convert designer‑provided PSDs into web‑ready PNGs with built‑in shadows.  
* **Mobile app resources** – Generate transparent PNG icons on the fly, avoiding manual export.  
* **Batch processing** – Automate conversion of hundreds of PSD files in a server‑side job, ensuring each PNG keeps its alpha channel and visual effects.  

## Common Issues and Solutions

| Issue | Likely Cause | Fix |
|-------|--------------|-----|
| **Shadow not visible** | `Opacity` set to 0 or layer is hidden | Verify `shadowEffect.getOpacity()` > 0 and layer visibility. |
| **PNG appears flat (no transparency)** | Wrong `PngColorType` used | Use `PngColorType.TruecolorWithAlpha` as shown. |
| **Exception on loading** | Effects not loaded | Ensure `loadOptions.setLoadEffectsResource(true)` is called. |
| **Incorrect layer index** | PSD structure differs | Inspect `im.getLayers()` and pick the correct index. |

## Frequently Asked Questions

**Q: Can I apply drop shadows to multiple layers simultaneously?**  
A: Yes. Loop through `im.getLayers()` and add or modify a `DropShadowEffect` for each target layer, which also lets you perform a batch psd to png conversion.

**Q: What does the ‘Spread’ parameter control?**  
A: `Spread` determines how abruptly the shadow transitions from full opacity to transparent. A higher value creates a harder edge.

**Q: Is Aspose.PSD compatible with all Photoshop versions?**  
A: Aspose.PSD supports PSD files from Photoshop 3.0 up to the latest version, handling most layer types and effects.

**Q: How can I test the code before purchasing a license?**  
A: Download the free trial from the [Aspose.PSD download page](https://releases.aspose.com/psd/java/) and run the sample without a license key.

**Q: Where can I get help if I run into problems?**  
A: Post your question on the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) where the community and Aspose engineers can assist.

## Conclusion

You now know how to **save psd as png**, **export PNG with alpha**, **convert PSD to PNG**, and **apply a drop shadow layer** using Aspose.PSD for Java. This combination lets you automate high‑quality image preparation for web, mobile, or desktop applications—without ever opening Photoshop.

---

**Last Updated:** 2026-04-22  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}