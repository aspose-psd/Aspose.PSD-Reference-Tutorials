---
title: Export PSD to PNG & Add a New Regular Layer using Aspose.PSD for Java – aspose temporary license
linktitle: Add a New Regular Layer to PSD
second_title: Aspose.PSD Java API
description: Learn how to export PSD to PNG and create a new PSD layer with Aspose.PSD for Java using an aspose temporary license. This step‑by‑step tutorial covers psd image manipulation and set layer position.
weight: 11
url: /java/advanced-image-effects/add-new-regular-layer/
date: 2026-04-08
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export PSD to PNG & Add a New Regular Layer using Aspose.PSD for Java

## Introduction

In this **aspose psd tutorial** you’ll discover how to **export PSD to PNG** while also **creating a new regular layer** inside the same file, **using an aspose temporary license** for development. Whether you need to generate web‑ready thumbnails, prepare assets for a design pipeline, or simply experiment with **psd image manipulation**, Aspose.PSD for Java gives you full programmatic control. We'll walk through every step—from loading the source file to saving both the updated PSD and a PNG copy—so you can start manipulating PSD layers right away.

## Quick Answers
- **Can I export PSD to PNG with one call?** Yes, after adding layers you can call `save` with `PngOptions`.
- **Do I need a license for development?** A temporary license works for testing; a full license is required for production.
- **Which Java version is supported?** Aspose.PSD works with Java 8 and newer.
- **Is layer positioning pixel‑based?** Yes, you set left, top, right, bottom coordinates in pixels using the **set layer position** methods.
- **Will the PNG retain layer transparency?** The PNG will contain the merged result of all visible layers.

## Why use an aspose temporary license?

An **aspose temporary license** lets you evaluate the full feature set of Aspose.PSD without any functional restrictions. It removes the evaluation watermark, unlocks all APIs—including the ability to **create new psd layer** objects—and lets you test your code in a production‑like environment before purchasing a permanent license.

## Prerequisites

Before you begin, ensure you have:

- **Java Development Environment** – JDK 8+ and a build tool (Maven/Gradle) installed.
- **Aspose.PSD for Java** – Download the latest JAR from the official site [here](https://releases.aspose.com/psd/java/).
- **A sample PSD file** – We'll use `OneLayer.psd` in the examples.

## Import Packages

Add the required imports to your Java class. These classes provide the core functionality for **psd image manipulation** and layer handling.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## What is “set layer position” and why does it matter?

When you add a new layer, you need to define where it appears on the canvas. The methods `setLeft`, `setTop`, `setRight`, and `setBottom` **set layer position** in pixel coordinates. Correct positioning ensures that your graphics line up exactly where you expect them to, which is crucial for tasks like compositing UI assets or preparing print‑ready files.

## Step‑by‑step guide

### Step 1: Load the PSD File

First, load the existing PSD you want to modify. This gives you a `PsdImage` object you can work with.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Step 2: Prepare Pixel Data and Rectangles

We'll create two pixel buffers (`int[]`) and define the rectangular areas where the new layers will be painted. This is the foundation for **creating a new psd layer**.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Step 3: Initialize Layer Data

Fill the pixel buffers with a default ARGB value. The value `-10000000` corresponds to a semi‑transparent dark shade.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Step 4: Add Regular Layers (Manipulate PSD Layers)

Now we **add regular layers** to the PSD image and **set layer position** using the left, top, right, and bottom properties. This demonstrates how to **manipulate PSD layers** programmatically.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### Step 5: Export PSD to PNG and Save the Updated PSD

After the layers are in place, save the modified document. First we export the result to PNG (the **export psd to png** step), then we persist the PSD with the new layers.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tip:** If you only need the PNG, you can skip the PSD `save` call and directly invoke `save` with `PngOptions`.

## Common Issues & Troubleshooting

| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| PNG appears blank | Layers are invisible or fully transparent | Ensure you set non‑transparent pixel values or call `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Mismatch between rectangle size and pixel array length | Verify that `rect.width * rect.height == dataArray.length`. |
| LicenseException at runtime | No valid license loaded | Load a temporary or permanent license before calling any API methods. |

## Frequently Asked Questions

**Q: Is Aspose.PSD compatible with Java 8?**  
A: Yes, Aspose.PSD supports Java 8 and later versions.

**Q: Can I apply transformations (rotate, scale) to the added layers?**  
A: Absolutely! The `Layer` class provides methods such as `rotate`, `scale`, and `translate` for full transformation control.

**Q: Where can I find additional Aspose.PSD documentation?**  
A: Detailed API docs are available [here](https://reference.aspose.com/psd/java/).

**Q: How do I obtain a temporary license for Aspose.PSD?**  
A: Visit the temporary‑license page [here](https://purchase.aspose.com/temporary-license/).

**Q: Are there community forums for Aspose.PSD support?**  
A: Yes, join the discussions on the Aspose forums [here](https://forum.aspose.com/c/psd/34).

## Conclusion

You've now learned how to **export PSD to PNG** while **adding new regular layers** using Aspose.PSD for Java, and you’ve seen how an **aspose temporary license** enables you to try this workflow without restrictions. This tutorial showcases core **psd image manipulation** capabilities: loading a file, creating layers, populating pixel data, and exporting the final composition. Feel free to experiment with different rectangle sizes, pixel colors, or layer effects to tailor the output to your project's needs.

---

**Last Updated:** 2026-04-08  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}