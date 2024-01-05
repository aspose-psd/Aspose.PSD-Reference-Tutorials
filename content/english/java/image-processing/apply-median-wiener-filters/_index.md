---
title: Apply Median and Wiener Filters with Aspose.PSD for Java
linktitle: Apply Median and Wiener Filters
second_title: Aspose.PSD Java API
description: Explore the power of image processing in Java with Aspose.PSD. Learn how to apply Median and Wiener Filters step by step. Enhance image quality effortlessly.
type: docs
weight: 12
url: /java/image-processing/apply-median-wiener-filters/
---
## Introduction

In the realm of Java programming, Aspose.PSD stands out as a powerful tool for image manipulation and processing. One of the key functionalities it offers is the application of Median and Wiener Filters, which play a crucial role in enhancing image quality and reducing noise. This step-by-step guide will walk you through the process of applying these filters using Aspose.PSD for Java.

## Prerequisites

Before diving into the tutorial, ensure that you have the following prerequisites in place:

1. Aspose.PSD for Java Library: Download and install the library from [here](https://releases.aspose.com/psd/java/).
2. Java Development Environment: Make sure you have a Java development environment set up on your system.

## Import Packages

Begin by importing the necessary packages to leverage Aspose.PSD functionality within your Java project:

```java
package com.aspose.psd.examples.Conversion;

import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.MedianFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

## Applying Median Filter

### Step 1: Load the Image

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load the source image
Image image = Image.load(sourceFile);
```

### Step 2: Cast Image into RasterImage

```java
// Cast the image into RasterImage
RasterImage rasterImage = (RasterImage)image;
if (rasterImage == null) {
    return;
}
```

### Step 3: Create MedianFilterOptions Instance

```java
// Create an instance of MedianFilterOptions class and set the filter size
MedianFilterOptions options = new MedianFilterOptions(4);
```

### Step 4: Apply Median Filter

```java
// Apply MedianFilterOptions filter to RasterImage object
rasterImage.filter(image.getBounds(), options);
```

### Step 5: Save the Resultant Image

```java
String destName = dataDir + "median_test_denoise_out.gif";
// Save the resultant image as a GIF
image.save(destName, new GifOptions());
```

By following these steps, you have successfully applied the Median Filter to your image using Aspose.PSD for Java.

## Conclusion

In this tutorial, we explored the process of applying Median and Wiener Filters using Aspose.PSD for Java. These filters are indispensable for enhancing image quality and reducing noise in your Java applications. By leveraging the power of Aspose.PSD, you can effortlessly incorporate these filters into your image processing workflows.

## FAQ's

### Q1: Can I apply these filters to images of any format?

A1: Yes, Aspose.PSD supports a wide range of image formats, making it versatile for various projects.

### Q2: Is there a free trial available for Aspose.PSD for Java?

A2: Yes, you can get a free trial [here](https://releases.aspose.com/).

### Q3: How do I get support for Aspose.PSD for Java?

A3: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community support.

### Q4: Where can I find the documentation for Aspose.PSD for Java?

A4: Refer to the documentation [here](https://reference.aspose.com/psd/java/).

### Q5: How can I purchase Aspose.PSD for Java?

A5: You can buy the product [here](https://purchase.aspose.com/buy).
