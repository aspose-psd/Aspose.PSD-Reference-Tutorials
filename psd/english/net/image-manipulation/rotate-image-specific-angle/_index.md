---
title: Rotating an Image on a Specific Angle in Aspose.PSD for .NET
linktitle: Rotating an Image on a Specific Angle
second_title: Aspose.PSD .NET API
description: Explore the power of Aspose.PSD for .NET. Rotate images effortlessly on specific angles. Download the library and start manipulating images seamlessly.
weight: 16
url: /net/image-manipulation/rotate-image-specific-angle/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rotating an Image on a Specific Angle in Aspose.PSD for .NET

If you're delving into the world of image manipulation with .NET, Aspose.PSD provides a powerful solution. In this tutorial, we'll guide you through the process of rotating an image on a specific angle using Aspose.PSD. Before we dive into the steps, let's set the stage with an introduction.

## Introduction

Aspose.PSD for .NET is a versatile library that empowers developers to work with PSD and raster image formats seamlessly. One of its key features is the ability to rotate images at precise angles, providing flexibility in image manipulation. This tutorial will walk you through the steps to rotate an image on a specific angle using Aspose.PSD for .NET.

## Prerequisites

Before we embark on this journey, ensure you have the following prerequisites in place:

- Aspose.PSD for .NET Library: Download and install the library from the [download page](https://releases.aspose.com/psd/net/).
- Document Directory: Set up a directory to store your source and output files.

## Import Namespaces

To get started, import the necessary namespaces in your .NET project:

```csharp
using Aspose.PSD.ImageOptions;
```

Now, let's break down the example into multiple steps in a step-by-step guide format.

## Step 1: Set Your Document Directory

```csharp
string dataDir = "Your Document Directory";
```

Replace `"Your Document Directory"` with the path to the directory where you store your source and output files.

## Step 2: Load the Image

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"RotatingImageOnSpecificAngle_out.jpg";

using (RasterImage image = (RasterImage)Image.Load(sourceFile))
{
    // Additional steps will be inserted here
}
```

Load the image you want to rotate into an instance of `RasterImage`.

## Step 3: Cache Image Data

```csharp
if (!image.IsCached)
{
    image.CacheData();
}
```

Cache the image data for better performance during rotation.

## Step 4: Rotate the Image

```csharp
image.Rotate(20f, true, Color.Red);
```

Rotate the image by 20 degrees, maintaining proportional size, and using a red background.

## Step 5: Save the Result

```csharp
image.Save(destName, new JpegOptions());
```

Save the rotated image with specified options (in this case, as a JPEG).

## Conclusion

Congratulations! You've successfully rotated an image on a specific angle using Aspose.PSD for .NET. This library provides a robust set of tools for image manipulation, and this tutorial is just the tip of the iceberg. Explore the [documentation](https://reference.aspose.com/psd/net/) for more features and options.

## FAQ's

### Q1: Can I rotate images by angles other than 20 degrees?

A1: Yes, you can customize the angle parameter in the `image.Rotate` method to any desired value.

### Q2: Does Aspose.PSD support other image formats besides JPEG?

A2: Absolutely! Aspose.PSD supports a wide range of formats, including PNG, GIF, BMP, and TIFF.

### Q3: Is caching image data necessary before rotation?

A3: While not mandatory, caching data can significantly enhance performance, especially for larger images.

### Q4: Where can I get support for Aspose.PSD-related queries?

A4: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community support and discussions.

### Q5: Can I try Aspose.PSD before purchasing?

A5: Certainly! Grab your [free trial](https://releases.aspose.com/) to explore the library's capabilities.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
