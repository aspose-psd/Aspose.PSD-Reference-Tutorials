---
title: Resize Image Proportionally with Aspose.PSD for Java
linktitle: Resize Image Proportionally with Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: Enhance your Java applications with Aspose.PSD. Follow our guide to resize images proportionally effortlessly. Boost your image handling capabilities today.
type: docs
weight: 17
url: /java/advanced-image-manipulation/resize-image-proportionally/
---
## Introduction

Welcome to our step-by-step guide on resizing images proportionally using Aspose.PSD for Java. If you're looking to enhance your Java applications with efficient image resizing capabilities, you've come to the right place. In this tutorial, we will walk you through the process using clear and concise steps.

## Prerequisites

Before diving into the tutorial, ensure you have the following prerequisites in place:

1. Java Environment: Make sure you have Java installed on your system.
2. Aspose.PSD Library: Download and install the Aspose.PSD library. You can find the necessary resources [here](https://releases.aspose.com/psd/java/).

## Import Packages

Once you have your prerequisites sorted, import the required packages into your Java project. Ensure that the Aspose.PSD library is correctly referenced in your project.

```java
package com.aspose.psd.examples.DrawingAndFormattingImages;

import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## Step 1: Load the Image

Begin by loading the image you want to resize into your Java application.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## Step 2: Specify Width and Height

Determine the new width and height for your resized image. In this example, we'll resize the image to half of its original dimensions.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## Step 3: Save the Resized Image

Save the resized image to your desired location, specifying the format options (PNG, in this case).

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

And there you have it! You've successfully resized an image proportionally using Aspose.PSD for Java.

## Conclusion

In this tutorial, we covered the essential steps to resize images proportionally using the Aspose.PSD library for Java. Now, you can effortlessly integrate this functionality into your Java applications for improved image handling.

## FAQ's

### Q1: Is Aspose.PSD compatible with all image formats?

A1: Aspose.PSD supports various image formats, including PSD, PNG, JPEG, and more. Check the [documentation](https://reference.aspose.com/psd/java/) for a comprehensive list.

### Q2: Can I use Aspose.PSD for commercial projects?

A2: Yes, you can. Visit the [purchase page](https://purchase.aspose.com/buy) for licensing details.

### Q3: Are temporary licenses available for testing purposes?

A3: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/) for evaluation.

### Q4: Where can I find support for Aspose.PSD?

A4: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community support and assistance.

### Q5: How can I access the Aspose.PSD documentation?

A5: Refer to the detailed documentation [here](https://reference.aspose.com/psd/java/).
`
