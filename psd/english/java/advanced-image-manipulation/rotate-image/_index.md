---
title: How to Rotate Image 270 Degrees with Aspose.PSD for Java
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
description: Learn how to rotate image 270 degrees using Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and convert PSD to JPEG.
weight: 19
url: /java/advanced-image-manipulation/rotate-image/
date: 2025-12-06
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rotate Image 270 Degrees with Aspose.PSD for Java

## Introduction

In this **java image processing tutorial**, you’ll discover how to **rotate image 270 degrees** quickly and reliably using Aspose.PSD for Java. Whether you’re building a photo‑editing tool, automating batch conversions, or just need to re‑orient a PSD layer, the library makes the task painless. We’ll also touch on flipping images and converting the rotated PSD to a JPEG, so you get a complete end‑to‑end workflow.

## Quick Answers
- **What library handles the rotation?** Aspose.PSD for Java  
- **Which rotation angle does the example use?** 270 degrees  
- **Can I also flip the image?** Yes – use `RotateFlipType` options like `Rotate90FlipX`  
- **How do I save the result?** In the example we save as JPEG using `JpegOptions`  
- **Do I need a license for production?** A valid Aspose.PSD license is required for commercial use  

## What is “rotate image 270 degrees”?
Rotating an image 270 degrees means turning the picture three‑quarters of a full circle clockwise (or 90 degrees counter‑clockwise). In many graphic‑editing scenarios this orientation matches the original portrait layout after a series of transformations.

## Why use Aspose.PSD for this task?
- **Full PSD support** – works with layers, masks, and adjustment objects.  
- **No native Photoshop required** – run on any Java runtime.  
- **Simple API** – a single method call (`rotateFlip`) handles rotation and flipping.  
- **Easy format conversion** – export directly to JPEG, PNG, or other common formats.

## Prerequisites

Before you start, make sure you have:

- **Aspose.PSD for Java** library installed. You can download it and view the full API reference [here](https://reference.aspose.com/psd/java/).  
- A Java development environment (JDK 8 or higher).  
- A sample PSD file that you want to rotate. Update the `sourceFile` variable in the code with the correct path to your file.

## Import Packages

Start by importing the necessary classes from the Aspose.PSD package:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## How to Rotate PSD – Step 1: Load the Image

Create an `Image` instance that points to your source PSD file:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## How to Rotate PSD – Step 2: Rotate the Image 270 Degrees

Use the `rotateFlip` method with `RotateFlipType.Rotate270FlipNone` to achieve a 270‑degree rotation without any flipping:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Pro tip:** If you also need to flip the image horizontally or vertically, choose a different `RotateFlipType` such as `Rotate90FlipX` or `Rotate180FlipY`.

## How to Rotate PSD – Step 3: Convert PSD to JPEG and Save

After rotating, you can **convert PSD to JPEG** (or any other supported format) using the appropriate options class:

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
A: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, and many other raster formats.

**Q: Can I apply custom rotations, not just predefined flips?**  
A: Absolutely! While `RotateFlipType` provides common angles, you can combine multiple calls or use transformation matrices for arbitrary angles.

**Q: How do I convert the rotated PSD to another format, such as PNG?**  
A: Replace `JpegOptions` with `PngOptions` (or the appropriate options class) in the `save` method.

**Q: Where can I find additional support or assistance?**  
A: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: Is there a free trial available?**  
A: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).

**Q: How do I obtain a temporary license?**  
A: If you need a temporary license, you can obtain one [here](https://purchase.aspose.com/temporary-license/).

## Conclusion

You’ve now learned how to **rotate image 270 degrees** using Aspose.PSD for Java, flip images when needed, and export the result to JPEG. This straightforward workflow can be integrated into larger Java‑based image‑processing pipelines, giving you full control over PSD manipulation without relying on Photoshop.

---

**Last Updated:** 2025-12-06  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}