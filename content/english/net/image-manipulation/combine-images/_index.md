---
title: Combining Images in Aspose.PSD for .NET
linktitle: Combining Images
second_title: Aspose.PSD .NET API
description: Combine images effortlessly in .NET with Aspose.PSD. Follow our step-by-step tutorial for seamless image manipulation.
type: docs
weight: 10
url: /net/image-manipulation/combine-images/
---
## Introduction

Welcome to our step-by-step tutorial on combining images using Aspose.PSD for .NET! Aspose.PSD is a powerful .NET library that allows developers to work with Adobe Photoshop files seamlessly. In this tutorial, we'll guide you through the process of combining images using Aspose.PSD, providing you with practical examples and detailed steps.

## Prerequisites

Before we dive into the tutorial, make sure you have the following prerequisites in place:

- Aspose.PSD Library: Ensure that you have the Aspose.PSD library installed. You can download it from [here](https://releases.aspose.com/psd/net/).

Now, let's dive into the tutorial!

## Import Namespaces

Firstly, you need to import the necessary namespaces to work with Aspose.PSD. Add the following code snippet at the beginning of your .NET file:

```csharp
using Aspose.PSD.ImageOptions;
using Aspose.PSD.Sources;
```

## Step 1: Set Up the Environment

Begin by setting up the environment and specifying the directory for your images.

```csharp
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();
```

## Step 2: Create PsdOptions Instance

Create an instance of PsdOptions, setting its properties as needed.

```csharp
PsdOptions imageOptions = new PsdOptions();
```

## Step 3: Create FileCreateSource

Create an instance of FileCreateSource and assign it to the Source property of imageOptions.

```csharp
imageOptions.Source = new FileCreateSource(dataDir + "Two_images_result_out.psd", false);
```

## Step 4: Create Image Instance

Create an instance of Image and define the canvas size.

```csharp
using (var image = Image.Create(imageOptions, 600, 600))
```

## Step 5: Initialize Graphics and Draw Images

Initialize an instance of Graphics, clear the image surface with white color, and draw the images onto the canvas.

```csharp
var graphics = new Graphics(image);
graphics.Clear(Color.White);
graphics.DrawImage(Image.Load(dataDir + "example1.psd"), 0, 0, 300, 600);
graphics.DrawImage(Image.Load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

## Step 6: Save the Combined Image

Save the final combined image.

```csharp
image.Save();
```

Congratulations! You have successfully combined two images using Aspose.PSD for .NET.

## Conclusion

In this tutorial, we've walked you through the process of combining images using Aspose.PSD. With its intuitive API, Aspose.PSD empowers developers to manipulate Photoshop files seamlessly in their .NET applications.

## FAQ's

### Q1: Is Aspose.PSD compatible with all versions of .NET?

A1: Yes, Aspose.PSD is compatible with all versions of .NET, ensuring versatility in your development projects.

### Q2: Can I use Aspose.PSD for commercial purposes?

A2: Yes, Aspose.PSD can be used for both personal and commercial purposes. Check the licensing details [here](https://purchase.aspose.com/buy).

### Q3: How do I get support for Aspose.PSD?

A3: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community support or consider purchasing a support plan.

### Q4: Is there a free trial available for Aspose.PSD?

A4: Yes, you can access the free trial [here](https://releases.aspose.com/).

### Q5: Can I obtain a temporary license for Aspose.PSD?

A5: Yes, you can get a temporary license [here](https://purchase.aspose.com/temporary-license/).
