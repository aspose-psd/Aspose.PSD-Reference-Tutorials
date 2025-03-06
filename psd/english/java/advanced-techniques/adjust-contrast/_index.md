---
title: Adjust Contrast of an Image with Aspose.PSD for Java
linktitle: Adjust Contrast of an Image
second_title: Aspose.PSD Java API
description: Explore the world of image contrast adjustment in Java with Aspose.PSD. Follow our step-by-step guide for seamless image manipulation.
weight: 22
url: /java/advanced-techniques/adjust-contrast/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Adjust Contrast of an Image with Aspose.PSD for Java

## Introduction

In the realm of image processing with Java, Aspose.PSD stands out as a powerful tool. Among its myriad features, adjusting image contrast is a common requirement. This tutorial will walk you through the process of adjusting image contrast using Aspose.PSD for Java. Whether you're a seasoned developer or just starting, this guide will help you master this essential aspect of image manipulation.

## Prerequisites

Before diving into the tutorial, ensure you have the following prerequisites in place:

- Basic understanding of Java programming.
- Aspose.PSD for Java library installed. You can download it [here](https://releases.aspose.com/psd/java/).

## Import Packages

To get started, you need to import the necessary packages into your Java project. Add the following lines to your code:

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

In this step, we load the sample image ("sample.psd") using the `Image.load` method.

## Step 2: Cast to RasterImage and Cache Data

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Here, we cast the generic `Image` object to a `RasterImage` for specific processing. Caching the image data improves performance.

## Step 3: Adjust Contrast

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

The `adjustContrast` method is used to modify the contrast of the image. In this example, the contrast is increased by 50%.

## Step 4: Create TiffOptions and Save

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

Here, we set up `TiffOptions` for the output image, specifying the format and other properties. The final image is then saved to a TIFF file.

## Conclusion

Congratulations! You've successfully adjusted the contrast of an image using Aspose.PSD for Java. This tutorial covered the essential steps, from importing packages to saving the processed image.

## FAQ's

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

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
