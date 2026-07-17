---
date: 2026-07-17
description: Learn step by step filter techniques to apply Median and Wiener filters
  using Aspose.PSD for Java, and convert PSD to GIF efficiently.
images:
- /java/image-processing/apply-median-wiener-filters/og-image.png
keywords:
- convert psd to gif
- remove salt pepper noise
- median filter java
- wiener filter java
lastmod: 2026-07-17
linktitle: Apply Median and Wiener Filters
og_description: Convert PSD to GIF using Aspose.PSD for Java. Learn how to apply Median
  and Wiener filters, remove salt‑pepper noise, and export high‑quality GIFs.
og_image_alt: 'Developer guide: Convert PSD to GIF with Median and Wiener filters
  in Java using Aspose.PSD'
og_title: Convert PSD to GIF – Apply Median & Wiener Filters (Java)
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn step by step filter techniques to apply Median and Wiener filters
    using Aspose.PSD for Java, and convert PSD to GIF efficiently.
  headline: Convert PSD to GIF – Step‑by‑Step Median & Wiener Filters (Java)
  type: TechArticle
- description: Learn step by step filter techniques to apply Median and Wiener filters
    using Aspose.PSD for Java, and convert PSD to GIF efficiently.
  name: Convert PSD to GIF – Step‑by‑Step Median & Wiener Filters (Java)
  steps:
  - name: Load the Image
    text: '`Image` is Aspose.PSD''s base class representing any supported image file.'
  - name: Cast Image into RasterImage
    text: '`RasterImage` extends `Image` and provides pixel‑level access for raster‑based
      operations.'
  - name: Create MedianFilterOptions Instance
    text: '`MedianFilterOptions` configures the median filter, allowing you to set
      the kernel size.'
  - name: Save the Resultant Image (Convert PSD to GIF)
    text: '`GifOptions` specifies settings for saving an image in GIF format, such
      as color depth and compression. `ExportFormat.Gif` is the enum value used to
      save an image as a GIF file. By following these steps you have successfully
      applied a Median filter and exported the cleaned image as a GIF.'
  type: HowTo
- questions:
  - answer: It reduces salt‑and‑pepper noise while preserving edges.
    question: What does the Median filter do?
  - answer: For adaptive noise reduction that considers local image variance.
    question: When should I use the Wiener filter?
  - answer: A free trial works for development; a commercial license is required for
      production.
    question: Do I need a license to run the code?
  - answer: Yes—Aspose.PSD lets you **convert PSD to GIF** in a single step.
    question: Can I save the output as GIF?
  - answer: Typically under 10 minutes for a basic setup.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
- median filter
- wiener filter
title: Convert PSD to GIF – Step‑by‑Step Median & Wiener Filters (Java)
url: /java/image-processing/apply-median-wiener-filters/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convert PSD to GIF: Apply Median & Wiener Filters (Java)

If you’re looking for a **step‑by‑step filter** workflow to clean up noisy images in Java, you’ve come to the right place. Aspose.PSD for Java makes it straightforward to apply both Median and Wiener filters, and it even lets you **convert PSD to GIF** after processing. In this guide we’ll walk through every stage—from library setup to saving the final GIF—so you can embed high‑quality image denoising into your applications with confidence.

## Quick Answers
- **What does the Median filter do?** It reduces salt‑and‑pepper noise while preserving edges.  
- **When should I use the Wiener filter?** For adaptive noise reduction that considers local image variance.  
- **Do I need a license to run the code?** A free trial works for development; a commercial license is required for production.  
- **Can I save the output as GIF?** Yes—Aspose.PSD lets you **convert PSD to GIF** in a single step.  
- **How long does the implementation take?** Typically under 10 minutes for a basic setup.

## What is a Step by Step Filter?
A *step‑by‑step filter* approach breaks image processing into clear, manageable stages—loading the image, configuring filter options, applying the filter, and finally saving the result. This methodical flow helps you debug each part, reuse code, and adapt the process for different image formats.

## Why Use Aspose.PSD for Java?
Aspose.PSD for Java supports **30+ image formats**, including PSD, PNG, JPEG, GIF, BMP, and TIFF, and can process multi‑hundred‑page documents without loading the entire file into memory. The library has **zero external dependencies**, meaning you can embed it in any Java project without worrying about native binaries. Built‑in filter options such as Median and Wiener are ready out of the box, and the API provides a one‑click conversion path to export directly to GIF, PNG, or JPEG after processing.

## Prerequisites

Before you start, make sure you have:

1. **Aspose.PSD for Java Library** – Download and install the library from [here](https://releases.aspose.com/psd/java/). For other Aspose products, see [here](https://releases.aspose.com/).  
2. **Java Development Environment** – JDK 8+ and an IDE or build tool (Maven/Gradle) set up on your machine.

## Import Packages

`Image`, `RasterImage`, and the filter option classes give you full control over image handling and noise reduction.

## How to Convert PSD to GIF Using Aspose.PSD (Java)

Load your PSD, apply the desired filter, and call `save` with the GIF format—all in a few concise lines. This direct‑answer pattern lets you see the complete conversion flow before diving into each individual step. You can also specify additional options such as color depth or compression level when saving.

## Step by Step Filter: How to Apply Median Filter

The Median filter removes **salt‑and‑pepper noise** while keeping edges sharp. It works by sliding a window over each pixel and replacing the central value with the median of the surrounding values, effectively eliminating outliers without blurring important details.

### Step 1: Load the Image

`Image` is Aspose.PSD's base class representing any supported image file.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.MedianFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

### Step 2: Cast Image into RasterImage

`RasterImage` extends `Image` and provides pixel‑level access for raster‑based operations.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load the source image
Image image = Image.load(sourceFile);
```

### Step 3: Create MedianFilterOptions Instance

`MedianFilterOptions` configures the median filter, allowing you to set the kernel size.

```java
// Cast the image into RasterImage
RasterImage rasterImage = (RasterImage)image;
if (rasterImage == null) {
    return;
}
```

### Step 4: Apply Median Filter

```java
// Create an instance of MedianFilterOptions class and set the filter size
MedianFilterOptions options = new MedianFilterOptions(4);
```

### Step 5: Save the Resultant Image (Convert PSD to GIF)

`GifOptions` specifies settings for saving an image in GIF format, such as color depth and compression. `ExportFormat.Gif` is the enum value used to save an image as a GIF file.

```java
// Apply MedianFilterOptions filter to RasterImage object
rasterImage.filter(image.getBounds(), options);
```

By following these steps you have successfully applied a Median filter and exported the cleaned image as a GIF.

## Applying Wiener Filter (Optional Extension)

The Wiener filter performs adaptive noise reduction by estimating local variance, making it ideal for images with varying noise levels. Replace the Median filter with `WienerFilterOptions` and keep the same workflow.

> **Pro tip:** Experiment with different kernel sizes for both filters to find the sweet spot between noise removal and detail preservation.

## Common Issues & Troubleshooting

| Symptom | Likely Cause | Fix |
|---------|---------------|-----|
| `ClassCastException` when casting to `RasterImage` | Input file isn’t a raster‑compatible PSD | Verify the PSD contains raster layers or convert layers to raster first |
| Output GIF is blank | Destination path is incorrect or folder lacks write permission | Ensure `dataDir` points to an existing writable directory |
| Filter seems to have no effect | Kernel size is too small for the noise level | Increase the filter size (e.g., `new MedianFilterOptions(6)`) |

## Frequently Asked Questions

**Q1: Can I apply these filters to images of any format?**  
A1: Yes, Aspose.PSD supports over 30 formats, so you can filter PSD, PNG, JPEG, BMP, TIFF, and more.

**Q2: Is there a free trial available for Aspose.PSD for Java?**  
A2: Yes, you can get a free trial [here](https://releases.aspose.com/).

**Q3: How do I get support for Aspose.PSD for Java?**  
A3: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community assistance.

**Q4: Where can I find the official documentation?**  
A4: Refer to the documentation [here](https://reference.aspose.com/psd/java/).

**Q5: How can I purchase a commercial license?**  
A5: You can buy the product [here](https://purchase.aspose.com/buy).

## Conclusion

In this guide we demonstrated a **step‑by‑step filter** process for applying Median (and optionally Wiener) filters using Aspose.PSD for Java, and we showed how to **convert PSD to GIF** after denoising. With these building blocks you can integrate robust image‑processing pipelines into any Java application—whether you’re cleaning up photos, preparing assets for the web, or automating batch conversions.

---

**Last Updated:** 2026-07-17  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Related Tutorials

- [Convert PSD to GIF - Apply Gaussian and Wiener Filters for Color Images with Aspose.PSD for Java](/psd/java/image-processing/apply-gaussian-wiener-filters-color-image/)
- [Step by Step Filter - Apply Motion Wiener Filters using Aspose.PSD for Java](/psd/java/image-processing/apply-motion-wiener-filters/)
- [How to Convert PSD to GIF Using Aspose.PSD for Java – Lossy Compressor](/psd/java/advanced-image-manipulation/implement-lossy-gif-compressor/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
String destName = dataDir + "median_test_denoise_out.gif";
// Save the resultant image as a GIF
image.save(destName, new GifOptions());
```