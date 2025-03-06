---
title: Rotate an Image on a Specific Angle with Aspose.PSD for Java
linktitle: Rotate an Image on a Specific Angle
second_title: Aspose.PSD Java API
description: Explore image rotation in Java with Aspose.PSD for Java. Rotate images effortlessly on specific angles.
weight: 20
url: /java/advanced-image-manipulation/rotate-image-specific-angle/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rotate an Image on a Specific Angle with Aspose.PSD for Java

## Introduction

In the dynamic world of Java development, manipulating images is a common requirement for various applications. Aspose.PSD for Java emerges as a robust solution, providing powerful features to effortlessly handle image rotation. In this tutorial, we will guide you through the process of rotating an image on a specific angle using Aspose.PSD for Java. Before diving into the details, let's set the stage with some prerequisites.

## Prerequisites

Before you embark on this image rotation journey, ensure that you have the following prerequisites in place:

### 1. Java Development Environment
Make sure you have a Java development environment set up on your system.

### 2. Aspose.PSD for Java Library
Download and install the Aspose.PSD for Java library. You can find the necessary library and documentation [here](https://reference.aspose.com/psd/java/).

### 3. Sample Image
Prepare a sample image (e.g., "sample.psd") that you want to rotate. Place it in your document directory.

## Import Packages

Now, let's import the necessary packages to get started with the image rotation process:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

Now, let's break down the process of rotating an image on a specific angle into a series of easy-to-follow steps.

## Step 1: Define Your Document Directory

```java
String dataDir = "Your Document Directory";
```

Ensure to replace "Your Document Directory" with the actual path to your document directory.

## Step 2: Specify Source and Destination File Paths

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

Set the source file path to the location of your sample image and specify the destination file path for the rotated image.

## Step 3: Load the Image

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

Load the sample image using Aspose.PSD.

## Step 4: Cache Image Data

```java
if (!image.isCached())
{
    image.cacheData();
}
```

Cache the image data for better performance during rotation.

## Step 5: Rotate the Image

```java
image.rotate(20f, true, Color.getRed());
```

Perform the rotation on a 20-degree angle while maintaining proportional size and using a red background color.

## Step 6: Save the Result

```java
image.save(destName, new JpegOptions());
```

Save the rotated image to a new file with specified options (in this case, using JpegOptions).

Congratulations! You have successfully rotated an image on a specific angle using Aspose.PSD for Java.

## Conclusion

In this tutorial, we explored the seamless process of rotating images with Aspose.PSD for Java. The library's robust features empower Java developers to manipulate images effortlessly, opening doors to a myriad of creative possibilities.

## FAQ's

### Q1: Can I rotate images with transparency using Aspose.PSD for Java?

Yes, Aspose.PSD for Java supports the rotation of images with transparency. Ensure to handle transparency-related options accordingly in your code.

### Q2: Are there any limitations on the image file formats supported for rotation?

No, Aspose.PSD for Java supports a wide range of image file formats, including PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF, and more.

### Q3: Can I rotate images by a negative angle?

Certainly! You can specify a negative angle in the `image.rotate()` method to rotate images in the opposite direction.

### Q4: Does Aspose.PSD for Java provide real-time image preview during rotation?

Aspose.PSD for Java primarily focuses on backend image processing. For real-time image preview, you may need to implement a frontend solution using other technologies.

### Q5: Is there a community forum for Aspose.PSD where I can seek help?

Yes, you can visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) to engage with the community, ask questions, and seek assistance.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
