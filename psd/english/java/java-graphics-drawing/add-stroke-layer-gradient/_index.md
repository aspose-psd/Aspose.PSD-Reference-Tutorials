---
title: How to Create Gradient Stroke Layer in Java
linktitle: How to Create Gradient Stroke Layer in Java
second_title: Aspose.PSD Java API
description: Learn how to create gradient stroke layer and customize stroke gradients in PSD files using Aspose.PSD for Java with this step‑by‑step tutorial.
weight: 10
url: /java/java-graphics-drawing/add-stroke-layer-gradient/
date: 2026-01-14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to Create Gradient Stroke Layer in Java

## Introduction
Ever wondered how to **create gradient stroke layer** in your PSD files using Java? You’re in the right place! Today we’ll dive into Aspose.PSD for Java—a powerful library that lets you manipulate PSD files effortlessly. Whether you’re new to graphics programming or looking to fine‑tune existing designs, this guide will walk you through adding and customizing stroke gradients step by step.

## Quick Answers
- **What is the primary goal?** Create a gradient stroke layer on a PSD file.  
- **Which library is required?** Aspose.PSD for Java.  
- **Do I need a license?** Yes, a valid (or temporary) license is required for production.  
- **What Java version works?** Java 8 or higher.  
- **How long does implementation take?** Roughly 10‑15 minutes for a basic gradient stroke.

## What is a Gradient Stroke Layer?
A gradient stroke layer is a vector outline around a shape or text that transitions smoothly between colors. Using Aspose.PSD you can programmatically define the colors, opacity, angle, and type (linear, radial, etc.) of the stroke.

## Why use Aspose.PSD for Java?
- **Full PSD support** – read, edit, and write PSD files without Photoshop.  
- **Rich effect API** – access stroke, shadow, glow, and many other layer effects.  
- **Cross‑platform** – works on any OS that supports Java.  
- **No native dependencies** – pure Java, easy to integrate into CI pipelines.

## Prerequisites
1. **Java Development Kit (JDK)** – Install the latest JDK from [Oracle's website](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java** – Download the library from the [Aspose.PSD download page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, or NetBeans.  
4. **License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/) if you don’t have a full one.

## Import Packages
First, import the classes we’ll need for loading the PSD, accessing effects, and configuring gradient fills.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

Now let’s break the process into clear steps.

## Step 1: Load the PSD File
We load the source PSD and enable effect resources so the stroke effect is available.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## Step 2: Access the Stroke Effect
Assuming the stroke we want to modify belongs to the third layer (index 2), we retrieve its `StrokeEffect`.

```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```

## Step 3: Verify Stroke Effect Properties
Before making changes, we confirm the existing settings so we know exactly what we’re updating.

```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```

## Step 4: Modify the Gradient Fill Settings
Here we change the color, opacity, blend mode, and other properties to achieve the desired look.

```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```

## Step 5: Add and Modify Color and Transparency Points
We add new color and transparency points, then adjust the existing ones to shape the gradient.

```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```

## Step 6: Save the Modified PSD File
After all adjustments, we write the updated file back to disk.

```java
im.save(exportPath);
```

## Step 7: Verify the Modifications
Load the saved file and assert that every property reflects the changes we applied.

```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Check transparency points
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```

## Conclusion
You now know how to **create gradient stroke layer** effects in PSD files using Aspose.PSD for Java. By loading a PSD, accessing the stroke effect, tweaking gradient fill settings, and saving the result, you can programmatically produce professional‑grade graphics without ever opening Photoshop.

## FAQ's
### What is Aspose.PSD for Java?
Aspose.PSD for Java is a library that allows developers to work with PSD files in Java applications, providing features to create, manipulate, and convert PSD files.

### Do I need a license to use Aspose.PSD for Java?
Yes, you need a valid license to use Aspose.PSD for Java. You can get a [temporary license](https://purchase.aspose.com/temporary-license/) for evaluation purposes.

### Can I use Aspose.PSD for Java to create PSD files from scratch?
Absolutely! Aspose.PSD for Java provides comprehensive APIs to create and manipulate PSD files programmatically.

### Is it possible to apply other effects using Aspose.PSD for Java?
Yes, you can apply various effects like shadow, glow, and more using Aspose.PSD for Java.

### Where can I find the documentation for Aspose.PSD for Java?
You can find the documentation [here](https://reference.aspose.com/psd/java/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-14  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose