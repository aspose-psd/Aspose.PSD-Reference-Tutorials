---
title: Handling PSD Image Timeline in Aspose.PSD for .NET
linktitle: Handling PSD Image Timeline
second_title: Aspose.PSD .NET API
description: Learn to handle PSD image timelines effortlessly using Aspose.PSD for .NET. Add frames, switch seamlessly, and enhance your image editing skills.
type: docs
weight: 17
url: /net/psd-file-manipulation/psd-image-timeline/
---
## Introduction
In the dynamic world of image processing, Aspose.PSD for .NET stands out as a powerful toolkit, providing robust solutions for handling PSD image timelines. Whether you're a seasoned developer or a coding enthusiast, this tutorial will guide you through the process of utilizing Aspose.PSD to manipulate image timelines with ease.
## Prerequisites
Before diving into the tutorial, make sure you have the following prerequisites in place:
- Basic knowledge of C# and .NET framework.
- Aspose.PSD for .NET installed. You can download the latest version [here](https://releases.aspose.com/psd/net/).
- A code editor like Visual Studio for seamless implementation.
## Import Namespaces
In your C# project, ensure you import the necessary namespaces to access the Aspose.PSD functionalities:
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.Animation;
```
## Step 1: Set Up Your Project
Begin by creating a new C# project in your preferred development environment. Ensure that Aspose.PSD for .NET is referenced.
## Step 2: Define Your Directories
Set up the directories for your source PSD file and the output directory where the manipulated image will be saved.
```csharp
string baseDir = "Your Document Directory";
string outputDir = "Your Output Directory";
```
## Step 3: Load and Manipulate the PSD Image
Use the following code snippet to load a PSD file, add a new frame to the timeline, switch to a specific frame, and save the manipulated image.
```csharp
string sourceFile = Path.Combine(baseDir, "4_animated.psd");
string outputFile = Path.Combine(outputDir, "output_edited.psd");
using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    Timeline timeline = psdImage.Timeline;
    // Add one more frame
    List<Frame> frames = new List<Frame>(timeline.Frames);
    frames.Add(new Frame());
    timeline.Frames = frames.ToArray();
    timeline.SwitchActiveFrame(4);
    psdImage.Save(outputFile);
}
```
## Step 4: Clean Up
Delete the temporary file after manipulation.
```csharp
File.Delete(outputFile);
```
## Step 5: Verify Execution
Finally, confirm the successful execution of the code.
```csharp
Console.WriteLine("SupportOfPsdImageTimelineProperty executed successfully");
```
## Conclusion
Congratulations! You've successfully navigated through the intricacies of handling PSD image timelines using Aspose.PSD for .NET. This tutorial empowers you to add frames, switch between them, and save your edited image effortlessly.
## FAQ's

### Q1: Can I use Aspose.PSD for .NET with other programming languages?

A1: No, Aspose.PSD is specifically designed for .NET applications.

### Q2: Is a license required for using Aspose.PSD?

A2: Yes, you need a valid license. Get it [here](https://purchase.aspose.com/buy).

### Q3: Can I try Aspose.PSD for free before purchasing a license?

A3: Yes, you can access the free trial [here](https://releases.aspose.com/).

### Q4: Where can I find detailed documentation for Aspose.PSD?

A4: Refer to the documentation [here](https://reference.aspose.com/psd/net/).

### Q5: Need assistance or have questions?

A5: Visit the Aspose.PSD community forum [here](https://forum.aspose.com/c/psd/34).
