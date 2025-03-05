---
title: Apply Gaussian and Wiener Filters in Aspose.PSD for Java
linktitle: Apply Gaussian and Wiener Filters
second_title: Aspose.PSD Java API
description: Enhance your Java image processing with Aspose.PSD. Learn to apply Gaussian and Wiener filters step-by-step for stunning visual results.
type: docs
weight: 10
url: /java/image-processing/apply-gaussian-wiener-filters/
---
## Introduction

Welcome to our comprehensive tutorial on applying Gaussian and Wiener filters in Aspose.PSD for Java! In this guide, we'll walk you through the process of enhancing your images using these powerful filters. Aspose.PSD for Java provides a robust set of features for image processing, and with the application of Gaussian and Wiener filters, you can achieve smoother and more refined images.

## Prerequisites

Before we dive into the tutorial, make sure you have the following prerequisites in place:

- Java Development Environment: Ensure that you have a Java development environment set up on your machine.

- Aspose.PSD for Java Library: Download and install the Aspose.PSD for Java library. You can find the download link [here](https://releases.aspose.com/psd/java/).

## Import Packages

In your Java project, import the necessary packages for Aspose.PSD. Here's a sample import statement to get you started:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

Now, let's break down the example into multiple steps to apply Gaussian and Wiener filters.

## Step 1: Load Image

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);
RasterImage rasterImage = (RasterImage)image;
```

In this step, we load the PSD image file from the specified directory.

## Step 2: Check RasterImage

```java
if (rasterImage == null) {
    return;
}
```

Ensure that the loaded image is a valid RasterImage; otherwise, the process is terminated.

## Step 3: Configure Filter Options

```java
GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
options.setGrayscale(true);
```

Create an instance of GaussWienerFilterOptions, set the radius size, smooth value, and specify if you want to apply the filter in grayscale.

## Step 4: Apply Filter and Save

```java
rasterImage.filter(image.getBounds(), options);
String destName = dataDir + "gauss_wiener_out.gif";
image.save(destName, new GifOptions());
```

Finally, apply the configured Gaussian and Wiener filters to the RasterImage and save the resultant image in GIF format.

## Conclusion

Congratulations! You've successfully learned how to apply Gaussian and Wiener filters using Aspose.PSD for Java. Experiment with different parameters to achieve the desired image enhancements.

## FAQ's

### Q1: Can I apply these filters to images in formats other than PSD?

A1: Yes, Aspose.PSD for Java supports various image formats beyond PSD.

### Q2: Are there any restrictions in the trial version of Aspose.PSD for Java?

A2: The trial version has limitations, and you can explore the full capabilities by obtaining a valid license.

### Q3: How can I get support for Aspose.PSD for Java?

A3: Visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) for community support and discussions.

### Q4: Is there a temporary license available for testing purposes?

A4: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q5: Where can I find detailed documentation for Aspose.PSD for Java?

A5: Refer to the [documentation](https://reference.aspose.com/psd/java/) for in-depth information.
