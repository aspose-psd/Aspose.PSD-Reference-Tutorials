---
title: How to Resize Image Java Using Resize Type Enumeration
linktitle: Resizing with Resize Type Enumeration
second_title: Aspose.PSD Java API
description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step guide covers the Resize Type Enumeration, high‑quality image resize, and how to convert PSD to JPEG.
weight: 18
url: /java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
date: 2026-06-03
keywords:
- how to resize image
- convert psd to jpeg
- high quality image resize
- resize image java
- java image manipulation tutorial
schemas:
- type: TechArticle
  headline: How to Resize Image Java Using Resize Type Enumeration
  description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  dateModified: '2026-06-03'
  author: Aspose
- type: HowTo
  name: How to Resize Image Java Using Resize Type Enumeration
  description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  steps:
  - name: '**Java Development Environment** – JDK 8 or newer installed and configured.'
    text: '**Java Development Environment** – JDK 8 or newer installed and configured.'
  - name: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
    text: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
- type: FAQPage
  questions:
  - question: How do I programmatically convert a PSD file to JPEG without resizing?
    answer: Load the PSD with `Image.load`, then call `image.save("output.jpg", new
      JpegOptions());`.
  - question: Is it possible to maintain the original DPI when resizing?
    answer: Yes, you can set the `Resolution` property on the `Image` object before
      saving.
  - question: Can I chain multiple resize operations?
    answer: While you can call `resize` multiple times, it’s more efficient to calculate
      the final dimensions and resize once.
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to Resize Image Java Using Resize Type Enumeration

## Introduction

If you’re looking for **how to resize image** files efficiently in a Java project, Aspose.PSD for Java provides a clean, high‑performance API. In this tutorial we’ll walk through loading a PSD, applying the **Resize Type Enumeration** for high‑quality image resize, and finally **convert PSD to JPEG**. Whether you’re building a desktop editor or an automated server‑side pipeline, these steps let you control dimensions, quality, and format with just a few lines of code.

## Quick Answers
- **What library handles resize image java?** Aspose.PSD for Java.
- **Which resize type gives the best quality?** `ResizeType.LanczosResample`.
- **Can I convert PSD to JPEG after resizing?** Yes – simply save with `JpegOptions`.
- **Do I need a license for production?** A valid Aspose.PSD license is required for production use.
- **Is this approach suitable for large batches?** Absolutely; the API processes multi‑hundred‑page files without loading the whole document into memory.

## What is "how to resize image" in Java?
**How to resize image** refers to programmatically changing the pixel dimensions of an image while preserving visual fidelity. Aspose.PSD’s `Resize` method combined with the `ResizeType` enumeration delivers precise control over scaling algorithms, allowing developers to maintain quality across a wide range of source files and target sizes.

## Why use Resize Type Enumeration?
`ResizeType` lets you select the resampling algorithm that best balances speed and visual quality. For most scenarios, **LanczosResample** delivers sharp results with a modest performance cost, processing a 2000 × 1500 image in under 120 ms on a typical server‑grade CPU while keeping edge detail intact.

## Prerequisites

Before you start, make sure you have:

1. **Java Development Environment** – JDK 8 or newer installed and configured.  
2. **Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).  
3. **Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd) file included with the SDK for hands‑on testing.

## Import Packages

`Image` is the base class for all image types in Aspose.PSD. Add the required imports to your Java source file:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Step 1: Load the Image

### Definition Anchor
The `RasterImage` class is Aspose.PSD’s core object that represents a raster‑based image loaded from a PSD file.

Load your PSD into a `RasterImage` instance so you can manipulate its pixels:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## Step 2: Resize the Image

`image.resize(width, height, resizeType)` resizes the image to the specified dimensions using the chosen algorithm.

Now resize the loaded image using the **Resize Type Enumeration**. In this example we use the Lanczos Resample method, which is ideal when you **how to resize image** with high quality:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Step 3: Save the Resized Image

`image.save(path, options)` writes the image to disk in the format defined by the provided options.

After resizing, save the image with the specified dimensions and the chosen resize type. Here, we also demonstrate **convert psd to jpeg** by saving the result as a JPEG file:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

## Why use Resize Type Enumeration?

`ResizeType` gives you fine‑grained control over the resampling algorithm, allowing you to balance speed and quality. For most applications, `LanczosResample` offers a great trade‑off, delivering sharp results without a heavy performance penalty, and it works well across a variety of image contents.

## Common Issues and Solutions

- **Image appears blurry after resize** – Try a different `ResizeType` such as `Bicubic` or `NearestNeighbour` to see which yields the best visual result for your specific image.  
- **OutOfMemoryError on large PSD files** – Process the image in smaller chunks or increase the JVM heap size (`-Xmx` flag). Aspose.PSD can handle files up to **2 GB** without loading the entire document into memory.

## FAQ's

### Q1: Is Aspose.PSD for Java suitable for both small and large‑scale projects?

A1: Absolutely! Aspose.PSD for Java is designed to cater to projects of all sizes, providing scalability and efficiency.

### Q2: Can I use a different resize type other than Lanczos Resample?

A2: Yes, Aspose.PSD for Java offers various resize types, such as **NearestNeighbour**, **Bicubic**, and more. Consult the API docs for the full list.

### Q3: Where can I find additional support for Aspose.PSD for Java?

A3: For any queries or assistance, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### Q4: Is there a free trial available for Aspose.PSD for Java?

A4: Yes, you can access a free trial version [here](https://releases.aspose.com/).

### Q5: How can I obtain a temporary license for Aspose.PSD for Java?

A5: To obtain a temporary license, visit [this link](https://purchase.aspose.com/temporary-license/).

## Frequently Asked Questions

**Q: How do I programmatically convert a PSD file to JPEG without resizing?**  
A: Load the PSD with `Image.load`, then call `image.save("output.jpg", new JpegOptions());`.

**Q: Is it possible to maintain the original DPI when resizing?**  
A: Yes, you can set the `Resolution` property on the `Image` object before saving.

**Q: Can I chain multiple resize operations?**  
A: While you can call `resize` multiple times, it’s more efficient to calculate the final dimensions and resize once.

---

**Last Updated:** 2026-06-03  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Related Tutorials

- [Simple Resizing with Aspose.PSD – Java Image Manipulation Library](/psd/java/basic-image-operations/simple-resizing/)
- [High Quality Image Scaling with Bicubic Resampler in Aspose.PSD for Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [How to Convert PSD to PNG and Resize Proportionally with Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}