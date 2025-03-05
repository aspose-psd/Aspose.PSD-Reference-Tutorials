---
title: Rotate an Image in Aspose.PSD for Java
linktitle: Rotate an Image
second_title: Aspose.PSD Java API
description: Explore image rotation in Java effortlessly with Aspose.PSD. Rotate, flip, and save PSD files easily.
type: docs
weight: 19
url: /java/advanced-image-manipulation/rotate-image/
---
## Introduction

Aspose.PSD for Java provides a powerful set of features for working with images, allowing developers to efficiently manipulate and process PSD files. In this tutorial, we'll focus on one specific task: rotating an image. Whether you're building a photo editing application or simply need to adjust the orientation of an image, Aspose.PSD makes the process straightforward.

## Prerequisites

Before diving into the tutorial, make sure you have the following prerequisites in place:

- Aspose.PSD for Java Library: Ensure you have downloaded and installed the Aspose.PSD for Java library. You can find the library and detailed documentation [here](https://reference.aspose.com/psd/java/).

- Java Development Environment: Make sure you have a Java development environment set up on your machine.

- Sample PSD File: Prepare a sample PSD file that you want to rotate. Adjust the `sourceFile` variable in the example code with the path to your PSD file.

## Import Packages

Start by importing the necessary packages to leverage the capabilities of Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Step 1: Load the Image

Load the existing image into an instance of the `Image` class:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Step 2: Rotate the Image

Rotate the image using the `rotateFlip` method. In this example, we rotate the image by 270 degrees:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Step 3: Save the Rotated Image

Save the rotated image using the `save` method and specifying the output format (JPEG, in this case):

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## Conclusion

Congratulations! You've successfully rotated an image using Aspose.PSD for Java. This simple yet powerful library opens up a world of possibilities for image manipulation in your Java applications.

## FAQ's

### Q1: Is Aspose.PSD compatible with different image formats?

A1: Yes, Aspose.PSD supports various image formats, including PSD, JPEG, PNG, and more.

### Q2: Can I apply custom rotations, not just predefined flips?

A2: Absolutely! Aspose.PSD provides flexibility for applying custom rotations to meet your specific requirements.

### Q3: Where can I find additional support or assistance?

A3: For any queries or issues, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) for community support.

### Q4: Is there a free trial available?

A4: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).

### Q5: How do I obtain a temporary license?

A5: If you need a temporary license, you can obtain one [here](https://purchase.aspose.com/temporary-license/).
