---
title: Java Image Processing – Adjust Gamma with Aspose.PSD
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
description: Learn how to perform java image processing by adjusting image gamma with Aspose.PSD. Step‑by‑step guide to convert PSD to TIFF and apply gamma correction.
weight: 23
url: /java/advanced-techniques/adjust-gamma/
date: 2025-12-21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Image Processing – Adjust Gamma with Aspose.PSD

## Introduction

If you’re working on **java image processing**, adjusting the gamma of a picture is a fundamental technique to improve brightness and contrast without losing detail. In this tutorial we’ll walk through how to use **Aspose.PSD for Java** to apply gamma correction to a PSD file and then export the result as a TIFF image. You’ll see why this approach is fast, reliable, and perfect for server‑side image pipelines.

## Quick Answers
- **What does gamma correction do?** It remaps luminance values to make dark areas brighter or bright areas darker while preserving overall detail.  
- **Which library handles the processing?** Aspose.PSD for Java provides a dedicated `adjustGamma` method for raster images.  
- **Can I convert PSD to TIFF in the same flow?** Yes – after gamma adjustment you can save the image directly to TIFF using `TiffOptions`.  
- **Do I need a license for development?** A free trial works for testing; a commercial license is required for production use.  
- **What Java version is supported?** Aspose.PSD supports Java 8 and later.

## What is java image processing?

Java image processing refers to the manipulation, analysis, and transformation of visual data using Java libraries. Tasks include resizing, filtering, color correction, and format conversion—all of which can be automated in desktop or web applications.

## Why use Aspose.PSD for gamma correction?

Aspose.PSD offers a high‑level API that abstracts the complexity of the PSD format, letting you focus on the actual image adjustments. It handles caching, colour profiles, and provides a straightforward `adjustGamma` call, making it ideal for **image gamma correction** and **convert psd to tiff** workflows.

## Prerequisites

Before diving into the tutorial, make sure you have the following prerequisites set up:

1. **Java Development Environment** – Ensure you have a Java development environment installed on your system.  
2. **Aspose.PSD Library** – Download and integrate the Aspose.PSD library into your Java project. You can find the necessary resources in the [documentation](https://reference.aspose.com/psd/java/).  
3. **Sample Image** – Prepare a sample PSD image that you'll use to apply the gamma adjustment.

## Import Packages

To kick off the process, import the required packages in your Java project. This sets the stage for utilizing Aspose.PSD functionalities seamlessly.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Step 1: Load the Image

Start by loading the sample PSD image into an instance of the `RasterImage` class. This is the foundation for subsequent gamma adjustments.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## Step 2: Adjust Gamma

Now, adjust the gamma of the loaded image using the `adjustGamma` method. Fine‑tune the gamma values according to your requirements.

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Step 3: Create TiffOptions

Create an instance of `TiffOptions` for the resultant image. Set various properties, such as bits per sample and photometric options, to tailor the output to your specifications.

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Step 4: Save the Resultant Image

Save the manipulated image to TIFF format using the previously defined `TiffOptions`.

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Common Issues and Solutions

| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **Image appears washed out** | Gamma value too high (e.g., > 2.5) | Lower the gamma factor to a value between 1.8 and 2.2. |
| **`rasterImage.isCached()` returns false** | Image not yet loaded into memory | Call `rasterImage.cacheData()` before adjusting gamma. |
| **TIFF file size is large** | Bits per sample set to 16‑bit | Use an 8‑bit sample (`{8,8,8}`) as shown in the example. |

## Frequently Asked Questions

**Q: Can I apply different gamma values to each colour channel?**  
A: Yes – the `adjustGamma` method accepts separate float values for red, green, and blue channels.

**Q: Is it possible to chain multiple image adjustments before saving?**  
A: Absolutely. You can perform resizing, cropping, or colour corrections sequentially on the same `RasterImage` instance.

**Q: Does Aspose.PSD support multi‑page PSD files?**  
A: Yes, each layer can be accessed and processed individually.

**Q: What format can I export to besides TIFF?**  
A: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective options classes.

## Conclusion

Congratulations! You’ve successfully performed **java image processing** by adjusting the gamma of a PSD file and exporting it as a TIFF image using Aspose.PSD for Java. This workflow gives you fine‑grained control over image brightness and contrast, making it ideal for automated graphics pipelines, web services, or desktop utilities.

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

## FAQ's

### Q1: Where can I find the Aspose.PSD documentation?

A1: You can access the documentation at [https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### Q2: How do I download Aspose.PSD for Java?

A2: Download the library from [https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### Q3: Where can I purchase Aspose.PSD?

A3: Visit [https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) to purchase Aspose.PSD.

### Q4: Is there a free trial available?

A4: Yes, you can explore a free trial at [https://releases.aspose.com/](https://releases.aspose.com/).

### Q5: Where can I seek support for Aspose.PSD?

A5: For support, visit the Aspose.PSD forum at [https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).

---