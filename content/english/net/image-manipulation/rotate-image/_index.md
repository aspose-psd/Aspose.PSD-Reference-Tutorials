---
title: Rotating an Image in Aspose.PSD for .NET
linktitle: Rotating an Image
second_title: Aspose.PSD .NET API
description: Learn to rotate images effortlessly in .NET with Aspose.PSD. Follow our step-by-step tutorial.
type: docs
weight: 15
url: /net/image-manipulation/rotate-image/
---
## Introduction

If you're diving into the world of image manipulation using .NET, Aspose.PSD is your go-to tool for seamless and efficient image processing. In this tutorial, we'll focus on a fundamental task – rotating an image using Aspose.PSD for .NET. Follow along as we break down the process into simple, actionable steps.

## Prerequisites

Before we begin, ensure you have the following prerequisites in place:

- Aspose.PSD for .NET Library: Download and install the library from the [Aspose.PSD .NET documentation](https://reference.aspose.com/psd/net/).

- Your Document Directory: Set up a directory where your images are stored. Replace "Your Document Directory" in the code snippet with the path to this directory.

## Import Namespaces

Make sure to include the necessary namespaces to access Aspose.PSD functionality. Add the following lines at the beginning of your .NET project:

```csharp
using Aspose.PSD.ImageOptions;
```

## Step 1: Load the Image

```csharp
string sourceFile = dataDir + @"sample.psd";

// Load an existing image into an instance of RasterImage class
using (Image image = Image.Load(sourceFile))
{
```

## Step 2: Rotate the Image

```csharp
    // Rotate the image 270 degrees clockwise
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Step 3: Save the Rotated Image

```csharp
    // Save the rotated image as a JPEG file
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

That's it! With just a few lines of code, you've successfully rotated an image using Aspose.PSD for .NET.

## Conclusion

In this tutorial, we've explored the basics of rotating images using Aspose.PSD for .NET. Aspose.PSD provides a robust set of tools for image manipulation, making it an essential library for .NET developers. Experiment with different rotations and explore further capabilities to enhance your image processing workflows.

## FAQ's

### Q1: Can I rotate images by a custom angle using Aspose.PSD?

Yes, Aspose.PSD allows you to specify a custom angle for rotation. Simply replace the `RotateFlipType.Rotate270FlipNone` line with your desired rotation angle.

### Q2: Is Aspose.PSD compatible with various image formats?

Absolutely. Aspose.PSD supports a wide range of image formats, including PSD, JPEG, PNG, and more. Check the [documentation](https://reference.aspose.com/psd/net/) for the complete list.

### Q3: How can I get a temporary license for Aspose.PSD?

Visit the [temporary license page](https://purchase.aspose.com/temporary-license/) on the Aspose website to obtain a temporary license for evaluation purposes.

### Q4: Where can I find support for Aspose.PSD?

For any queries or assistance, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) and connect with the community.

### Q5: Can I purchase Aspose.PSD for commercial use?

Certainly. Explore the [purchase page](https://purchase.aspose.com/buy) to acquire a license tailored to your needs.
