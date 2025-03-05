---
title: Creating Elliptical Shapes with Aspose.PSD for .NET
linktitle: Creating Elliptical Shapes with Aspose.PSD for .NET
second_title: Aspose.PSD .NET API
description: Learn how to draw elliptical shapes in .NET using Aspose.PSD. Step-by-step guide with code examples. Create stunning graphics effortlessly.
type: docs
weight: 13
url: /net/psd-drawing-techniques/creating-elliptical-shapes/
---
## Introduction

Welcome to our comprehensive guide on creating elliptical shapes using Aspose.PSD for .NET. Aspose.PSD is a powerful .NET library that allows developers to manipulate and convert Photoshop files without requiring Adobe Photoshop. In this tutorial, we'll walk you through the process of drawing elliptical shapes using the library.

## Prerequisites

Before we dive into the tutorial, make sure you have the following prerequisites in place:

- Aspose.PSD for .NET Library: Ensure that you have the Aspose.PSD library installed in your .NET project. You can download it from the [Aspose.PSD for .NET Documentation](https://reference.aspose.com/psd/net/).

- .NET Environment: This tutorial assumes you have a working knowledge of the .NET framework.

## Import Namespaces

To get started, import the necessary namespaces into your project. This ensures that you have access to the classes and methods required for drawing elliptical shapes. Here's an example:

```csharp
using Aspose.PSD.Brushes;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

Now, let's break down the process of creating elliptical shapes into multiple steps:

## Step 1: Set up the Document Directory

```csharp
// The path to the documents directory.
string dataDir = "Your Document Directory";
```

## Step 2: Create an Instance of BmpOptions

```csharp
// Create an instance of BmpOptions and set its various properties
string outpath = dataDir + "Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
```

## Step 3: Create an Instance of Image

```csharp
// Create an instance of Image
using (Image image = new PsdImage(100, 100))
{
    // Create and initialize an instance of Graphics class and Clear Graphics surface                    
    Graphics graphic = new Graphics(image);
    graphic.Clear(Color.Yellow);
```

## Step 4: Draw a Dotted Ellipse Shape

```csharp
    // Draw a dotted ellipse shape by specifying the Pen object having red color and a surrounding Rectangle
    graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
```

## Step 5: Draw a Continuous Ellipse Shape

```csharp
    // Draw a continuous ellipse shape by specifying the Pen object having a solid brush with blue color and a surrounding Rectangle
    graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    // Export image to bmp file format.
    image.Save(outpath, saveOptions);
}
```

## Conclusion

Congratulations! You have successfully created elliptical shapes using Aspose.PSD for .NET. This tutorial covered the essential steps, from setting up the environment to drawing both dotted and continuous ellipse shapes.

## FAQ's

### Q1: Where can I find the documentation for Aspose.PSD for .NET?

A1: The documentation is available [here](https://reference.aspose.com/psd/net/).

### Q2: How do I download Aspose.PSD for .NET?

A2: You can download it from the release page [here](https://releases.aspose.com/psd/net/).

### Q3: Is there a free trial available?

A3: Yes, you can access the free trial [here](https://releases.aspose.com/).

### Q4: How can I get support for Aspose.PSD for .NET?

A4: Visit the support forum [here](https://forum.aspose.com/c/psd/34).

### Q5: Do I need a temporary license for testing?

A5: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
