---
title: Working with Timeline in Aspose.PSD for .NET
linktitle: Working with Timeline
second_title: Aspose.PSD .NET API
description: Enhance PSD image manipulation with Aspose.PSD for .NET Timeline class. Control frame properties, layer states, and unleash creative possibilities effortlessly.
type: docs
weight: 16
url: /net/psd-file-manipulation/timeline/
---
## Introduction
In the dynamic world of graphic design and image manipulation, the ability to control and manipulate the timeline of images is crucial. Aspose.PSD for .NET provides a powerful solution with its Timeline class. This high-level feature enables users to make changes to the timeline of PsdImage, such as altering frame delay, editing layer states on specific frames, and more.
## Prerequisites
Before diving into the exciting possibilities that the Timeline class offers, make sure you have the following prerequisites in place:
- Aspose.PSD for .NET Library: Ensure that you have the Aspose.PSD for .NET library installed. You can download it from the [Aspose.PSD for .NET documentation](https://reference.aspose.com/psd/net/).
- Document and Output Directories: Define the paths for your document and output directories in the code. Adjust the `baseDir` and `outputDir` variables according to your project structure.
Now, let's explore how to utilize the Timeline class step by step.
## Import Namespaces
To start working with the Timeline class, import the necessary namespaces in your code:
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.Animation;
```
## Step 1: Load PSD Image
Begin by loading the PSD image from the specified source file. Ensure that the source file path is correctly set:
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    // Your code for further operations goes here
}
```
## Step 2: Access the Timeline
Once the PSD image is loaded, access the Timeline using the following code:
```csharp
Timeline timeline = psdImage.Timeline;
```
## Step 3: Change Dispose Method
Manipulate the dispose method of a specific frame. In this example, we change the dispose method of frame 1:
```csharp
timeline.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;
```
## Step 4: Adjust Frame Delay
Modify the delay of a particular frame. Here, we change the delay of frame 2 to 15:
```csharp
timeline.Frames[1].Delay = 15;
```
## Step 5: Edit Layer State
Change the opacity of 'Layer 1' on a specific frame. In this instance, we set the opacity to 50 on frame 2:
```csharp
LayerState layerState11 = timeline.Frames[1].LayerStates[1];
layerState11.Opacity = 50;
```
## Step 6: Move Layer
Move 'Layer 1' to the left-bottom corner on a specific frame (frame 3 in this example):
```csharp
LayerState layerState21 = timeline.Frames[2].LayerStates[1];
layerState21.PositionOffset = new Point(-50, 230);
```
## Step 7: Add New Frame
Add a new frame to the timeline:
```csharp
List<Frame> frames = new List<Frame>(timeline.Frames);
frames.Add(new Frame());
timeline.Frames = frames.ToArray();
```
## Step 8: Change Blend Mode
Alter the blend mode of 'Layer 1' on a specific frame (frame 4 in this case):
```csharp
LayerState layerState31 = timeline.Frames[3].LayerStates[1];
layerState31.BlendMode = BlendMode.Dissolve;
```
## Step 9: Save Changes
Apply the changes back to the PsdImage instance and save the modified PSD image:
```csharp
psdImage.Save(outputPsd);
```
## Step 10: Clean Up
Finally, clean up by deleting the temporary output file:
```csharp
File.Delete(outputPsd);
```
## Conclusion

In conclusion, the Timeline class in Aspose.PSD for .NET empowers developers to have granular control over the timeline of PSD images. Through a series of simple steps, you can manipulate frame properties, layer states, and more, opening up a realm of creative possibilities.

## FAQ's

### Q1: Is Aspose.PSD for .NET suitable for beginners?

A1: Absolutely! Aspose.PSD for .NET provides a user-friendly interface and comprehensive documentation, making it accessible for both beginners and seasoned developers.

### Q2: Can I apply timeline changes to GIF images?

A2: The Timeline class is specifically designed for PSD images. For GIF manipulation, refer to Aspose.GIF for .NET.

### Q3: Where can I find additional support or discuss issues?

A3: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community support and issue discussions.

### Q4: How can I obtain a temporary license for Aspose.PSD for .NET?

A4: Acquire a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q5: What are the key benefits of using Aspose.PSD for .NET?

A5: Aspose.PSD for .NET offers advanced image processing capabilities, PSD file manipulation, and high-performance rendering.
