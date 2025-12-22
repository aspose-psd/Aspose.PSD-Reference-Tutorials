---
title: How to Adjust Contrast of an Image with Aspose.PSD for Java
linktitle: Adjust Contrast of an Image
second_title: Aspose.PSD Java API
description: Learn how to adjust contrast of images using Aspose.PSD for Java, a leading java image manipulation library, and convert PSD to TIFF efficiently.
weight: 22
url: /java/advanced-techniques/adjust-contrast/
date: 2025-12-21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to Adjust Contrast of an Image with Aspose.PSD for Java

## Introduction

If you’re looking for **how to adjust contrast** in your Java projects, you’ve come to the right place. Aspose.PSD for Java is a powerful **java image manipulation library** that lets you fine‑tune image properties such as contrast, brightness, and more. In this tutorial we’ll walk through the exact steps to raise the contrast of a PSD file and then **convert PSD to TIFF** for downstream workflows.

## Quick Answers
- **What does “adjust contrast” mean?** It changes the difference between the darkest and brightest pixels, making details pop.
- **Which library handles this?** Aspose.PSD for Java – a full‑featured image processing toolkit.
- **Do I need a license?** A temporary license works for testing; a full license is required for production.
- **Can I save the result as TIFF?** Yes, we’ll use `TiffOptions` to export the processed image.
- **How long does the code take to run?** Typically under a second for standard‑size PSD files.

## What is Contrast Adjustment?
Contrast adjustment modifies the tonal range of an image, amplifying the distinction between light and dark areas. This is especially useful when images look flat after scanning or when preparing graphics for print.

## Why Use Aspose.PSD for Java?
- **Rich format support** – open, edit, and save PSD, TIFF, PNG, JPEG and many more.
- **High performance** – caching and raster‑image optimizations reduce memory overhead.
- **Straight‑forward API** – single‑method calls like `adjustContrast` make code readable.

## Prerequisites

Before diving in, make sure you have:

- Basic knowledge of Java programming.
- Aspose.PSD for Java library installed. You can download it [here](https://releases.aspose.com/psd/java/).

## Import Packages

Add the required imports to your Java class:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Step 1: Load the Image

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

We load the source PSD file (`sample.psd`) into an `Image` object, which serves as the entry point for all further processing.

## Step 2: Cast to RasterImage and Cache Data

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Casting to `RasterImage` gives us access to pixel‑level operations. Caching improves performance, especially for large files.

## How to Adjust Contrast of an Image

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

The `adjustContrast` method takes an integer representing the percentage change. In this example we boost contrast by **50 %**.

## Convert PSD to TIFF Using Aspose.PSD

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Here we configure `TiffOptions` (bits per sample, photometric interpretation) and write the contrast‑enhanced image to a TIFF file.

## Common Issues and Solutions
- **Image not cached:** Always call `cacheData()` for large PSDs to avoid `OutOfMemoryError`.
- **Unexpected color shift:** Verify that `setPhotometric` matches your target color space (RGB vs. CMYK).
- **File not found:** Ensure `dataDir` points to the correct folder and that the file name is spelled correctly.

## Frequently Asked Questions

### Q1: Is Aspose.PSD compatible with different image formats?

A1: Yes, Aspose.PSD supports various image formats, providing flexibility in your projects.

### Q2: How can I obtain a temporary license for Aspose.PSD?

A2: You can get a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q3: Where can I find Aspose.PSD documentation?

A3: The documentation is available [here](https://reference.aspose.com/psd/java/).

### Q4: What support options are available for Aspose.PSD?

A4: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### Q5: Can I purchase Aspose.PSD?

A5: Yes, you can buy Aspose.PSD [here](https://purchase.aspose.com/buy).

## Conclusion

You now know **how to adjust contrast** of a PSD image using Aspose.PSD for Java and how to **convert PSD to TIFF** for further processing. These steps give you fine‑grained control over image quality while keeping the code clean and maintainable. Feel free to experiment with other image‑adjustment methods such as `adjustBrightness` or `adjustGamma` to suit your specific needs.

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}