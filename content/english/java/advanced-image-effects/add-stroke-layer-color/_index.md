---
title: Add Stroke Layer Color in Aspose.PSD for Java
linktitle: Add Stroke Layer Color
second_title: Aspose.PSD Java API
description: Explore the power of Aspose.PSD for Java with our step-by-step guide on adding stroke layer color. Elevate your graphic designs effortlessly.
type: docs
weight: 14
url: /java/advanced-image-effects/add-stroke-layer-color/
---
## Introduction

Unlock the potential of your Java application's graphic design with Aspose.PSD. In this tutorial, we'll delve into the fascinating world of adding stroke layer color using Aspose.PSD for Java. Enhance your graphics with strokes that pop, creating visually appealing designs effortlessly.

## Prerequisites

Before embarking on this creative journey, ensure you have the following prerequisites in place:

- Aspose.PSD Library: Download and set up the Aspose.PSD library by following the [documentation](https://reference.aspose.com/psd/java/).

- Java Development Kit (JDK): Make sure you have Java installed on your system.

- Integrated Development Environment (IDE): Choose an IDE of your preference; Eclipse or IntelliJ are popular choices.

## Import Packages

Let's start by importing the necessary packages to make the Aspose.PSD magic happen.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Step 1: Set Up Your Project

Begin by creating a new Java project in your preferred IDE. Ensure that the Aspose.PSD library is added to your project.

## Step 2: Load PSD File

Load the PSD file using Aspose.PSD, enabling the loading of effects resources.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Step 3: Access Stroke Layer

Access the stroke effect layer within the PSD file.

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## Step 4: Validate Stroke Properties

Ensure the stroke properties are as expected.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## Step 5: Set Color and Opacity

Modify the color and opacity of the stroke layer.

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## Step 6: Save the Modified PSD

Save the modified PSD file with the newly added stroke layer color.

```java
im.save(exportPath);
```

## Conclusion

Congratulations! You've successfully added stroke layer color to your PSD file using Aspose.PSD for Java. Experiment with different colors and settings to bring your graphic designs to life.

## FAQ's

### Q1: Can I use Aspose.PSD with other Java graphic libraries?

A1: Yes, Aspose.PSD can be integrated with other Java graphic libraries for enhanced functionality.

### Q2: Is Aspose.PSD compatible with the latest PSD file format?

A2: Absolutely! Aspose.PSD keeps pace with the latest PSD file format specifications, ensuring compatibility.

### Q3: How do I handle exceptions while using Aspose.PSD?

A3: Refer to the [support forum](https://forum.aspose.com/c/psd/34) for assistance in handling exceptions and troubleshooting.

### Q4: Can I try Aspose.PSD before purchasing?

A4: Certainly! Grab a [free trial](https://releases.aspose.com/) to explore the features of Aspose.PSD before making a commitment.

### Q5: Where can I get a temporary license for Aspose.PSD?

A5: Obtain a [temporary license](https://purchase.aspose.com/temporary-license/) for Aspose.PSD to evaluate its capabilities in your projects.
