---
title: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
description: Learn how to convert PSD to JPEG and rotate image 270 degrees using Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and convert PSD to JPEG.
weight: 19
url: /java/advanced-image-manipulation/rotate-image/
date: 2026-05-19
keywords:
- convert psd to jpeg
- how to rotate psd
- flip image java
- rotate psd layer
- rotate image without photoshop
schemas:
- type: TechArticle
  headline: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  dateModified: '2026-05-19'
  author: Aspose
- type: HowTo
  name: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  steps:
  - name: Load the PSD File
    text: '`Image` is Aspose.PSD''s core class that represents a single PSD document
      in memory. Instantiating it reads only the header information, keeping memory
      usage low.'
  - name: Rotate the Image 270 Degrees
    text: '`rotateFlip` performs the specified rotation and optional flip on the image.
      `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise
      while leaving the image orientation unchanged. > **Pro tip:** If you also need
      to flip the image horizontally or vertically, choose a different `Ro'
  - name: Convert PSD to JPEG and Save
    text: '`JpegOptions` defines JPEG‑specific parameters such as compression quality.
      The `save` method writes the transformed image to disk in the desired format.
      The file `RotatedImage_out.jpg` now contains the original PSD content rotated
      270 degrees and saved as a JPEG.'
- type: FAQPage
  questions:
  - question: Is Aspose.PSD compatible with different image formats?
    answer: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other
      raster formats.
  - question: Can I apply custom rotations, not just predefined flips?
    answer: Absolutely! While `RotateFlipType` provides common angles, you can chain
      multiple calls or use transformation matrices for arbitrary angles.
  - question: How do I convert the rotated PSD to another format, such as PNG?
    answer: Replace `JpegOptions` with `PngOptions` (or the appropriate options class)
      in the `save` method.
  - question: Where can I find additional support or assistance?
    answer: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).
  - question: Is there a free trial available?
    answer: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convert PSD to JPEG & Rotate Image 270 Degrees with Aspose.PSD for Java

## Introduction

In this **Java image‑processing tutorial**, you’ll learn how to **convert PSD to JPEG** while rotating the image 270 degrees using Aspose.PSD for Java. Whether you’re building a batch‑processing pipeline, a web‑based editor, or a desktop utility, the library lets you manipulate PSD layers without Photoshop. We’ll also cover optional flipping and show the full end‑to‑end flow from loading a PSD file to saving a JPEG.

## Quick Answers
- **What library handles the rotation?** Aspose.PSD for Java  
- **Which rotation angle does the example use?** 270 degrees  
- **Can I also flip the image?** Yes – use `RotateFlipType` options like `Rotate90FlipX`  
- **How do I save the result?** In the example we save as JPEG using `JpegOptions`  
- **Do I need a license for production?** A valid Aspose.PSD license is required for commercial use  

## What is “rotate image 270 degrees”?
Rotating an image 270 degrees means turning the picture three‑quarters of a full circle clockwise (or 90 degrees counter‑clockwise). This orientation often restores the original portrait layout after prior transformations, and it is commonly used when images were captured in landscape mode but need to be displayed in portrait. The result is a correctly oriented visual without loss of quality.

## Why use Aspose.PSD for this task?
Aspose.PSD supports **50+ input and output formats**—including PSD, JPEG, PNG, BMP, GIF, and TIFF—and can process files up to **2 GB** without loading the entire document into memory. The API works on any Java runtime (JDK 8+), requires no native Photoshop installation, and provides a single `rotateFlip` call that handles both rotation and flipping in one step.

## Prerequisites

Before you start, make sure you have:

- **Aspose.PSD for Java** library installed. You can download it and view the full API reference [here](https://reference.aspose.com/psd/java/).  
- A Java development environment (JDK 8 or higher).  
- A sample PSD file that you want to rotate. Update the `sourceFile` variable in the code with the correct path to your file.

## Import Packages

The `Image`, `RotateFlipType`, and `JpegOptions` classes are required for loading, transforming, and saving the file.  
`Image` is the core class representing a PSD document in memory.  
`RotateFlipType` enumerates the supported rotation and flip operations.  
`JpegOptions` configures JPEG output settings such as quality.  

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## How to Convert PSD to JPEG after rotating?

Load the source PSD, apply a 270‑degree rotation, and immediately save it as a JPEG. This three‑step flow runs in under a second for typical 10‑MP images on a modern CPU, making it ideal for high‑throughput batch jobs. By processing only the necessary image data, memory consumption stays low, and the resulting JPEG retains visual fidelity while reducing file size.

### Step 1: Load the PSD File

`Image` is Aspose.PSD's core class that represents a single PSD document in memory. Instantiating it reads only the header information, keeping memory usage low.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### Step 2: Rotate the Image 270 Degrees

`rotateFlip` performs the specified rotation and optional flip on the image. `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise while leaving the image orientation unchanged.

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Pro tip:** If you also need to flip the image horizontally or vertically, choose a different `RotateFlipType` such as `Rotate90FlipX` or `Rotate180FlipY`.

### Step 3: Convert PSD to JPEG and Save

`JpegOptions` defines JPEG‑specific parameters such as compression quality. The `save` method writes the transformed image to disk in the desired format.

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

The file `RotatedImage_out.jpg` now contains the original PSD content rotated 270 degrees and saved as a JPEG.

## Common Issues and Solutions

| Issue | Solution |
|-------|----------|
| **Image appears upside‑down** | Verify you used `Rotate270FlipNone`. For a 90‑degree clockwise rotation use `Rotate90FlipNone`. |
| **Output file is corrupted** | Ensure the destination folder exists and you have write permissions. |
| **License exception** | Install a temporary or permanent Aspose.PSD license before loading the image in production. |

## Frequently Asked Questions

**Q: Is Aspose.PSD compatible with different image formats?**  
A: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other raster formats.

**Q: Can I apply custom rotations, not just predefined flips?**  
A: Absolutely! While `RotateFlipType` provides common angles, you can chain multiple calls or use transformation matrices for arbitrary angles.

**Q: How do I convert the rotated PSD to another format, such as PNG?**  
A: Replace `JpegOptions` with `PngOptions` (or the appropriate options class) in the `save` method.

**Q: Where can I find additional support or assistance?**  
A: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Is there a free trial available?**  
A: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).

**Q: How do I obtain a temporary license?**  
A: If you need a temporary license, you can obtain one [here](https://purchase.aspose.com/temporary-license/).

---

**Last Updated:** 2026-05-19  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Related Tutorials

- [Convert PSD to Raster Image Formats with Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Convert PSD to PNG and Rotate Layers in PSD Files using Java](/psd/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/)
- [How to Rotate Image in Java with Aspose.PSD](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}