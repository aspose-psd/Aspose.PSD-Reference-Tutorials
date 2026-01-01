---
date: 2026-01-01
description: Poznaj, jak przycinać obraz w Javie przy użyciu Aspose.PSD dla Javy.
  Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby wczytać plik PSD, przyciąć
  prostokąt obrazu i przekonwertować PSD na JPEG.
linktitle: Crop Image by Rectangle
second_title: Aspose.PSD Java API
title: 'Przycinanie obrazu w Javie: przycinanie obrazu prostokątem przy użyciu Aspose.PSD'
url: /pl/java/image-editing/crop-image-by-rectangle/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crop Image Java: Crop Image by Rectangle with Aspose.PSD

## Introduction

Manipulating graphics is a routine part of **java image processing**, and Aspose.PSD for Java gives you a clean, high‑performance API to work with PSD files. In this tutorial you’ll learn **how to crop image** using a rectangle, load a PSD file, and finally convert the result to a JPEG—all with just a few lines of Java code.

## Quick Answers
- **What does “crop image java” mean?** It refers to trimming an image to a defined rectangle using Java code.  
- **Which library handles the operation?** Aspose.PSD for Java provides the necessary classes.  
- **Do I need a license for testing?** A free trial is available; a license is required for production.  
- **Can I convert the cropped PSD to JPEG?** Yes—use `JpegOptions` when saving.  
- **How long does the implementation take?** Usually under 10 minutes for a basic scenario.

## What is cropping an image rectangle in Java?

Cropping an image rectangle means selecting a specific area (defined by X, Y, width, and height) and discarding everything outside that area. This operation is common when you need to focus on a particular region of a larger PSD document.

## Why use Aspose.PSD for this task?

- **No external dependencies** – works with pure Java.  
- **Supports PSD, PNG, JPEG, and many other formats** – you can **convert PSD to JPEG** instantly.  
- **High‑fidelity rendering** – retains layer information and color profiles during the crop.  

## Prerequisites

- Java Development Kit (JDK) installed.  
- Aspose.PSD for Java library – download it from the [website](https://releases.aspose.com/psd/java/).  

## Import Packages

Make sure to include the necessary packages in your Java project to leverage the capabilities of Aspose.PSD for Java. Add the following import statements at the beginning of your Java file:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

Now, let's break down the process into multiple steps to guide you through cropping an image by a rectangle using Aspose.PSD for Java.

## Step 1: Set up Your Document Directory

```java
String dataDir = "Your Document Directory";
```

Replace `"Your Document Directory"` with the actual path where your PSD file is located.

## Step 2: Specify Source and Destination Files

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

Define the paths for your source PSD file and the destination JPEG file.

## Step 3: Load and Cache the Image

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Here we **load PSD file** into a `RasterImage` instance and cache its data to improve performance.

## Step 4: Create and Define the Crop Rectangle

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

Create an instance of the `Rectangle` class with the desired size for cropping. The parameters represent **X**, **Y**, **width**, and **height** respectively.

## Step 5: Crop and Save the Image

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

Perform the crop operation using the specified rectangle and **convert PSD to JPEG** by saving the result with `JpegOptions`.

Repeat these steps as needed, adjusting the parameters according to your specific requirements.

## Common Issues & Tips

- **Rectangle outside image bounds** – ensure the rectangle’s coordinates are within the source image dimensions.  
- **Memory consumption** – call `rasterImage.dispose()` after you’re done to free native resources.  
- **Quality control** – you can set `JpegOptions.setQuality(int)` to control the compression level of the output JPEG.

## Conclusion

In this tutorial we walked through the process of **crop image java** by a rectangle using Aspose.PSD for Java. By following these steps you can easily integrate powerful image manipulation capabilities—loading a PSD file, cropping a specific region, and converting the result to JPEG—into any Java application.

## FAQ's

### Q1: Can I use Aspose.PSD for Java with other Java frameworks?

A1: Yes, Aspose.PSD for Java can be integrated with various Java frameworks, providing flexibility in your development projects.

### Q2: Is there a free trial available for Aspose.PSD for Java?

A2: Yes, you can access the free trial version [here](https://releases.aspose.com/).

### Q3: Where can I find additional support or assistance?

A3: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community support and discussions.

### Q4: How do I obtain a temporary license for Aspose.PSD for Java?

A4: You can acquire a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q5: What are the supported image formats for cropping in Aspose.PSD for Java?

A5: Aspose.PSD for Java supports various image formats, including PSD, PNG, JPEG, and more.

---

**Last Updated:** 2026-01-01  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}