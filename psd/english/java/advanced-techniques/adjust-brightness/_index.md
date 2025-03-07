---
title: Adjust Brightness of an Image with Aspose.PSD for Java
linktitle: Adjust Brightness of an Image
second_title: Aspose.PSD Java API
description: Enhance image brightness in Java with Aspose.PSD. Step-by-step guide to adjust image brightness programmatically. 
weight: 21
url: /java/advanced-techniques/adjust-brightness/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Adjust Brightness of an Image with Aspose.PSD for Java

## Introduction

Enhancing images is a common requirement in graphic design and digital photography. Aspose.PSD for Java provides a powerful solution for adjusting image brightness programmatically. In this tutorial, we'll explore how to utilize the Aspose.PSD for Java library to adjust the brightness of an image, step by step.

## Prerequisites

Before diving into the tutorial, ensure you have the following prerequisites:

- Aspose.PSD for Java Library: Download and install the library from the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).

## Import Packages

To begin, import the necessary packages into your Java project. In this example, we'll use the following:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Now, let's break down the process of adjusting the brightness of an image into simple steps:

## Step 1: Load the Image

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

In this step, we load the target image and cast it to a `RasterImage` for further processing.

## Step 2: Adjust Brightness

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Here, we use the `adjustBrightness` method to modify the brightness of the image. In this example, we decrease the brightness by 50 units, but you can customize this value based on your requirements.

## Step 3: Set TiffOptions

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Configure the `TiffOptions` for saving the adjusted image. Adjust the `bitsPerSample` and `photometric` properties based on your specific needs.

## Step 4: Save the Resultant Image

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Finally, save the modified image using the specified `TiffOptions`.

## Conclusion

Adjusting the brightness of an image programmatically is made easy with Aspose.PSD for Java. This tutorial has provided a comprehensive guide on implementing this functionality in your Java applications.

## FAQ's

### Q1: Can I adjust brightness in other image formats besides PSD?

A1: Yes, Aspose.PSD for Java supports various image formats like JPEG, PNG, and TIFF.

### Q2: How can I handle errors during the image adjustment process?

A2: You can implement error handling using try-catch blocks to manage exceptions that may occur.

### Q3: Is there a limit to the range of brightness adjustment?

A3: The range of adjustment depends on the image content and format, but Aspose.PSD provides flexibility in customization.

### Q4: Can I use Aspose.PSD for Java in commercial projects?

A4: Yes, Aspose.PSD for Java is a commercial library, and you can obtain a license from [here](https://purchase.aspose.com/buy).

### Q5: Is there a free trial available for Aspose.PSD for Java?

A5: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
