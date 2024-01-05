---
title: Adjust Gamma of an Image with Aspose.PSD for Java
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
description: Learn to adjust image gamma effortlessly using Aspose.PSD for Java. Follow our step-by-step guide for optimal results.
type: docs
weight: 23
url: /java/advanced-techniques/adjust-gamma/
---
## Introduction

In the realm of image processing, adjusting the gamma of an image is a crucial step to enhance its visual appeal. Aspose.PSD for Java offers a powerful solution for Java developers to effortlessly manipulate image gamma. In this tutorial, we'll explore how to adjust gamma using Aspose.PSD, breaking down each step to ensure a seamless implementation.

## Prerequisites

Before diving into the tutorial, make sure you have the following prerequisites set up:

1. Java Development Environment: Ensure you have a Java development environment installed on your system.
2. Aspose.PSD Library: Download and integrate the Aspose.PSD library into your Java project. You can find the necessary resources in the [documentation](https://reference.aspose.com/psd/java/).
3. Sample Image: Prepare a sample PSD image that you'll use to apply the gamma adjustment.

## Import Packages

To kick off the process, import the required packages in your Java project. This sets the stage for utilizing Aspose.PSD functionalities seamlessly.

```java
package com.aspose.psd.examples.DrawingAndFormattingImages;

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

Now, adjust the gamma of the loaded image using the `adjustGamma` method. Fine-tune the gamma values according to your requirements.

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

## Conclusion

Congratulations! You've successfully adjusted the gamma of an image using Aspose.PSD for Java. This process empowers developers to enhance image quality effortlessly, contributing to a visually appealing user experience.

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
