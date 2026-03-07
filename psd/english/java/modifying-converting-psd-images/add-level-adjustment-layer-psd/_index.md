---
title: "How to Adjust Levels – Add Level Adjustment Layer in PSD"
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
description: "Learn how to adjust levels by adding a Level Adjustment Layer in PSD files using Aspose.PSD for Java. Master tonal tweaks quickly."
weight: 16
url: /java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
date: 2026-03-07
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Add Level Adjustment Layer in PSD

## Introduction
If you’re looking to **how to adjust levels** in your Photoshop documents, the Level Adjustment Layer is the perfect tool. It lets you fine‑tune shadows, mid‑tones, and highlights without permanently altering the original pixels. In this tutorial we’ll walk through adding a Level Adjustment Layer to a PSD file using Aspose.PSD for Java, so you can achieve professional‑grade tonal control in just a few steps.

## Quick Answers
- **What does a Level Adjustment Layer do?** It modifies the tonal range of an image non‑destructively.  
- **Which library is used?** Aspose.PSD for Java.  
- **Do I need a license?** A free trial works for development; a license is required for production.  
- **How long does the implementation take?** About 10‑15 minutes for a basic adjustment.  
- **Can I adjust multiple channels?** Yes, you can set input/output levels for each color channel individually.

## What is a Level Adjustment Layer?
A Level Adjustment Layer lets you correct the tonal balance of an image by adjusting input shadows, mid‑tones, and highlights as well as output levels. Because it lives on its own layer, you can toggle its visibility or delete it without affecting the underlying artwork.

## Why add a Level Adjustment Layer with Aspose.PSD?
- **Automation:** Integrate level tweaks into batch processing pipelines.  
- **Cross‑platform:** Works on any OS that supports Java.  
- **Precision:** Access each channel’s settings programmatically for exact results.  

## Prerequisites
1. Java Development Kit (JDK). If you don’t have it, download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) or use OpenJDK.  
2. Aspose.PSD for Java library – get the latest JAR from this [download link](https://releases.aspose.com/psd/java/).  
3. Basic knowledge of Java programming.  
4. An IDE such as IntelliJ IDEA, Eclipse, or NetBeans with the Aspose.PSD JAR added to the project’s classpath.

## Import Packages
Before we start writing our code, we need to import the necessary packages from the Aspose.PSD library. Here’s how you can do it:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
These imports give us access to classes for loading PSD files, working with level adjustment layers, and manipulating individual channel settings.

## How to Adjust Levels in a PSD File
Below is a step‑by‑step guide that shows you exactly **how to adjust levels** programmatically.

### Step 1: Set Up Your File Paths
Define where the source PSD resides and where the edited file will be saved.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
Replace `"Your Document Directory"` with the actual folder on your machine.

### Step 2: Load the PSD File
Create a `PsdImage` instance from the source file.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
Now you have full access to all layers inside the PSD.

### Step 3: Iterate Through the Layers
Find the Level Adjustment Layer you want to modify.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
The `instanceof LevelsLayer` check ensures we only work with level adjustment layers.

### Step 4: Adjust the Level Channel Settings
Tweak the input and output values for the selected channel.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
- **Input Midtone Level:** Shifts the mid‑tone range.  
- **Input Shadow Level:** Darkens or lightens shadows.  
- **Input Highlight Level:** Controls the brightest parts.  
- **Output Shadow/Highlight Levels:** Define the final output range.

Feel free to experiment with different values to see how they affect the image.

### Step 5: Save the Modified PSD File
Persist your changes to a new file.
```java
im.save(psdPathAfterChange);
```
You’ll find the updated PSD at the location you specified in `psdPathAfterChange`.

## Common Issues and Solutions
- **File not found:** Verify that `dataDir` points to the correct folder and that the source PSD exists.  
- **ClassCastException:** Ensure the file you load is indeed a PSD; other formats require different classes.  
- **License errors:** Use a valid Aspose.PSD license for production builds; the trial works for development.

## Conclusion
You now know **how to adjust levels** by adding and configuring a Level Adjustment Layer in a PSD file with Aspose.PSD for Java. This technique gives you precise control over tonal balance while keeping your workflow fully automated. Keep experimenting with different channel values and explore batch processing to apply the same adjustments to multiple images.

## Frequently Asked Questions

**Q: What is a Level Adjustment Layer?**  
A: It’s a non‑destructive layer that lets you modify the tonal range (shadows, mid‑tones, highlights) of an image.

**Q: Can I use Aspose.PSD without purchasing a license?**  
A: Yes, you can evaluate the library with a free trial, but a license is required for commercial deployment.

**Q: Where can I find documentation for Aspose.PSD?**  
A: You can find the documentation [here](https://reference.aspose.com/psd/java/).

**Q: Is there community support for Aspose products?**  
A: Absolutely! You can ask questions and get help in the [Aspose forum](https://forum.aspose.com/c/psd/34).

**Q: How can I get a temporary license for Aspose.PSD?**  
A: You can apply for a temporary license [here](https://purchase.aspose.com/temporary-license/).

---

**Last Updated:** 2026-03-07  
**Tested With:** Aspose.PSD latest version (Java)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}