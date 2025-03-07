---
title: Adding Stroke Layer with Solid Color in Aspose.PSD for .NET
linktitle: Adding Stroke Layer with Solid Color
second_title: Aspose.PSD .NET API
description: Enhance your .NET image manipulation skills with Aspose.PSD. Learn to add stroke layers with solid colors step by step.
weight: 11
url: /net/layer-effects/adding-stroke-layer-solid-color/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Adding Stroke Layer with Solid Color in Aspose.PSD for .NET

## Introduction

In the realm of .NET development, creating visually appealing images is a common requirement. Aspose.PSD for .NET provides a powerful set of tools to manipulate and enhance images seamlessly. One of the essential features is adding a stroke layer with a solid color, which brings vibrancy and depth to your images. In this tutorial, we will guide you through the process step by step using Aspose.PSD for .NET.

## Prerequisites

Before diving into the tutorial, make sure you have the following prerequisites:

- Basic knowledge of .NET development.
- Visual Studio installed on your machine.
- Aspose.PSD for .NET library. You can download it from the [website](https://releases.aspose.com/psd/net/).

## Import Namespaces

Start by importing the necessary namespaces to leverage the functionality of Aspose.PSD for .NET:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
```

## Step 1: Load the PSD File

Begin by loading the PSD file that you want to enhance with a stroke layer. Ensure you have the correct file path:

```csharp
string dataDir = "Your Document Directory";
string sourceFileName = dataDir + "Stroke.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // Code for further steps will be added here
}
```

## Step 2: Access Stroke Effect Properties

Retrieve the properties of the stroke effect from the PSD file:

```csharp
var colorStroke = (StrokeEffect)im.Layers[1].BlendingOptions.Effects[0];

if ((colorStroke.BlendMode != BlendMode.Normal) ||
    (colorStroke.Opacity != 255) ||
    (colorStroke.IsVisible != true))
{
    throw new Exception("Color stroke effect was read wrong");
}
```

## Step 3: Adjust Stroke Settings

Modify the stroke settings according to your preferences. In this example, we change the color to yellow, set opacity to 127, and use the Color blend mode:

```csharp
var fillSettings = (ColorFillSettings)colorStroke.FillSettings;

if ((fillSettings.Color != Color.Black) || (fillSettings.FillType != FillType.Color))
{
    throw new Exception("Color stroke effect settings were read wrong");
}

fillSettings.Color = Color.Yellow;
colorStroke.Opacity = 127;
colorStroke.BlendMode = BlendMode.Color;
```

## Step 4: Save the Edited Image

Save the image after applying the stroke layer changes:

```csharp
string exportPath = dataDir + "StrokeGradientChanged.psd";
im.Save(exportPath);
```

## Step 5: Verify the Changes

Ensure the changes are correctly applied by loading and inspecting the edited image:

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    // Code to verify changes will be added here
}
```

Repeat these steps for additional adjustments or experiment with different stroke effects to achieve the desired visual impact.

## Conclusion

Congratulations! You've successfully learned how to add a stroke layer with a solid color using Aspose.PSD for .NET. This powerful feature opens up a world of possibilities for enhancing your images in the .NET environment.

## FAQs

### Q1: Is Aspose.PSD for .NET compatible with the latest .NET framework versions?

A1: Yes, Aspose.PSD for .NET is regularly updated to ensure compatibility with the latest .NET framework versions.

### Q2: Can I use Aspose.PSD for .NET for commercial projects?

A2: Absolutely! Aspose.PSD for .NET is a commercial product, and you can use it in your projects by purchasing a license.

### Q3: Where can I find more examples and documentation for Aspose.PSD for .NET?

A3: Explore the [documentation](https://reference.aspose.com/psd/net/) for comprehensive examples and guidance.

### Q4: Is there a free trial available for Aspose.PSD for .NET?

A4: Yes, you can get a free trial from the [releases page](https://releases.aspose.com/).

### Q5: How can I get support for Aspose.PSD for .NET?

A5: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) to seek assistance and connect with the community.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
