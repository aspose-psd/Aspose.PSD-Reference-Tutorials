---
title: How to Add Stroke Layer Gradient in Java
linktitle: How to Add Stroke Layer Gradient in Java
second_title: Aspose.PSD Java API
description: Learn how to add and customize stroke layer gradients in PSD files using Aspose.PSD for Java with this comprehensive step-by-step tutorial.
type: docs
weight: 10
url: /java/java-graphics-drawing/add-stroke-layer-gradient/
---
## Introduction
Ever wondered how to add a stroke layer gradient to your images using Java? Well, you're in the right place! Today, we're diving into the world of Aspose.PSD for Java, a powerful library that helps you manipulate PSD files with ease. Whether you're a beginner or a seasoned developer, this step-by-step guide will walk you through the process of adding a stroke layer gradient to your PSD files. So, buckle up and get ready to enhance your graphic editing skills!
## Prerequisites
Before we get started, there are a few things you need to have in place. Make sure you have the following:
1. Java Development Kit (JDK): Ensure you have JDK installed on your system. You can download it from [Oracle's website](https://www.oracle.com/java/technologies/javase-downloads.html).
2. Aspose.PSD for Java Library: You can download it from the [Aspose.PSD download page](https://releases.aspose.com/psd/java/).
3. An Integrated Development Environment (IDE): Any IDE like IntelliJ IDEA, Eclipse, or NetBeans will work.
4. A valid license: You can get a [temporary license](https://purchase.aspose.com/temporary-license/) if you don't have a full one.
## Import Packages
First things first, let's import the necessary packages. These will enable us to use the classes and methods required for manipulating the PSD file.
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
Now, let's break down the example into multiple steps for better understanding.
## Step 1: Load the PSD File
First, we need to load the PSD file that we want to modify. We'll use the `PsdLoadOptions` to specify that we want to load the effects resources.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## Step 2: Access the Stroke Effect
Next, we need to access the stroke effect of the layer we're interested in. Here, we assume it's the third layer (index 2) in the PSD file.
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## Step 3: Verify Stroke Effect Properties
Before making any changes, let's verify the properties of the stroke effect to ensure we're modifying the correct settings.
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
Now, it's time to modify the gradient fill settings according to our requirements. We'll change the color, opacity, blend mode, and other properties.
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
Let's add new color and transparency points and modify the existing ones to achieve the desired gradient effect.
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
After making all the necessary modifications, we need to save the PSD file.
```java
im.save(exportPath);
```
## Step 7: Verify the Modifications
Finally, let's load the saved PSD file and verify that our changes have been applied correctly.
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
And there you have it! You now know how to add and manipulate stroke layer gradients in PSD files using Aspose.PSD for Java. This tutorial covered loading the PSD file, accessing and modifying stroke effects, and saving the changes. With these skills, you can create visually appealing gradients and customize your PSD files to suit your needs.
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
