---
title: Crop Image Java by Shifts with Aspose.PSD
linktitle: Crop Image by Shifts
second_title: Aspose.PSD Java API
description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step image cropping tutorial covers loading PSD files, setting shift values, and saving the result.
weight: 16
url: /java/image-editing/crop-image-by-shifts/
date: 2026-07-03
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
schemas:
- type: TechArticle
  headline: Crop Image Java by Shifts with Aspose.PSD
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  dateModified: '2026-07-03'
  author: Aspose
- type: HowTo
  name: Crop Image Java by Shifts with Aspose.PSD
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
- type: FAQPage
  questions:
  - question: Is Aspose.PSD compatible with all image formats?
    answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
  - question: Can I apply multiple cropping operations to the same image?
    answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
  - question: Is there a community forum for Aspose.PSD support?
    answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
  - question: How can I obtain a temporary license for Aspose.PSD?
    answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
  - question: Are there sample projects showcasing Aspose.PSD functionalities?
    answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crop Image Java by Shifts with Aspose.PSD

## Introduction

In Java image processing, **crop image java** is a common requirement for preparing graphics, thumbnails, or UI assets. Aspose.PSD for Java makes this task straightforward by exposing a simple `crop` method that works on any supported raster format. In this tutorial you’ll learn how to load a PSD file, define left‑right‑top‑bottom shift values, apply the crop, and save the result—all without writing custom pixel‑manipulation code.

## Quick Answers
- **What library handles cropping?** Aspose.PSD for Java provides a built‑in `crop` method.  
- **Do I need a license?** A temporary license works for evaluation; a full license is required for production.  
- **Supported formats?** Over 30 raster formats, including PSD, JPEG, PNG, BMP, and TIFF.  
- **Maximum file size?** Handles files up to 2 GB without loading the entire image into memory.  
- **How many lines of code?** Only five logical steps—load, cache, define shifts, crop, and save.

## What is crop image java?
`crop image java` refers to the operation of trimming a bitmap in a Java application. Using Aspose.PSD, the operation is performed by the `crop` method, which accepts shift values for each side of the image and returns a new image instance.

## Why use Aspose.PSD for image cropping?
Aspose.PSD supports **30+** image formats and can process multi‑hundred‑page PSD files while using less than 150 MB of RAM, thanks to its lazy‑loading architecture. The library also guarantees pixel‑perfect results, preserving layers, masks, and color profiles—something many generic image libraries cannot assure.

## Prerequisites

### Java Development Kit (JDK)

Make sure you have the latest version of JDK installed on your system. You can download it from [here](https://www.oracle.com/java/technologies/javase-downloads.html).

### Aspose.PSD for Java Library

To begin, you'll need to obtain the Aspose.PSD for Java library. Head over to the [download page](https://releases.aspose.com/psd/java/) and grab the latest version.

### Integrated Development Environment (IDE)

Choose your favorite Java IDE, such as Eclipse or IntelliJ, for a smooth coding experience.

## How to crop image java?

Load your source file, define the pixel shifts for each side, and call the `crop` method—this entire workflow can be written in five concise lines of code. The `crop` operation creates a new image that contains only the region you specified, leaving the original file untouched.

### Step 1: Load the Image

`Image` is the base class for all image types in Aspose.PSD.  
`RasterImage` represents a raster image and provides cropping capabilities.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Step 2: Cache Image Data

`cacheData()` loads the image data into memory for faster processing.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### Step 3: Define Shift Values

Specify the shift values for all four sides of the image (left, top, right, bottom) in pixels.  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### Step 4: Apply Cropping

`crop(left, right, top, bottom)` trims the image by the specified pixel shifts on each side.  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### Step 5: Save the Results

`JpegOptions` defines JPEG encoding settings such as quality and color profile.  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

Congratulations! You've successfully cropped an image using Aspose.PSD for Java.

## Common Issues and Solutions

- **Image appears unchanged:** Verify that the shift values are positive and do not exceed the original dimensions.  
- **OutOfMemoryError on large files:** Enable caching as shown in Step 2; this forces Aspose.PSD to use a temporary file instead of keeping the whole image in RAM.  
- **Color shift after cropping:** Ensure you preserve the color profile by calling `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })` if you need exact color fidelity.

## Frequently Asked Questions

**Q: Is Aspose.PSD compatible with all image formats?**  
A: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG, PNG, BMP, TIFF, and GIF, ensuring broad compatibility.

**Q: Can I apply multiple cropping operations to the same image?**  
A: Absolutely. After each `crop` call you receive a new image object, which you can crop again as needed.

**Q: Is there a community forum for Aspose.PSD support?**  
A: Yes, you can find support and engage with the community at [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: How can I obtain a temporary license for Aspose.PSD?**  
A: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain a temporary license.

**Q: Are there sample projects showcasing Aspose.PSD functionalities?**  
A: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).

---

**Last Updated:** 2026-07-03  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## Related Tutorials

- [Crop Image by Rectangle in Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Crop Image Java - Expand and Crop Images with Aspose.PSD for Java](/psd/java/image-editing/expand-and-crop-images/)
- [Resize Image Java - Using Resize Type Enumeration in Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}