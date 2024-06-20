---
title: How to Add Stroke Layer Pattern in Java
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
description: Learn how to add a stroke layer pattern to PSD files using Aspose.PSD for Java. Follow this step-by-step guide to enhance your images easily.
type: docs
weight: 11
url: /java/java-graphics-drawing/add-stroke-layer-pattern/
---
## Introduction
Adding a stroke layer pattern to an image in Java might sound like a daunting task, but with Aspose.PSD for Java, it’s easier than you think. Whether you're designing graphics or working on photo editing applications, this guide will walk you through the process step-by-step. Ready to get started? Let's dive in!
## Prerequisites
Before you start, you'll need a few things:
- Java Development Kit (JDK): Make sure you have JDK installed on your system.
- Aspose.PSD for Java: Download the library from [here](https://releases.aspose.com/psd/java/) and include it in your project.
- An IDE: Use your favorite Integrated Development Environment (IDE) like IntelliJ IDEA or Eclipse.
## Import Packages
First things first, you need to import the necessary packages into your Java project. These packages are essential for working with Aspose.PSD.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
## Step 1: Load the PSD File
The first step in adding a stroke layer pattern is to load the PSD file you want to edit.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
By loading the PSD file, you can now access and manipulate its layers and effects.
## Step 2: Prepare New Pattern Data
Next, you need to prepare the new pattern data that you will apply to the stroke layer.
```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```
This pattern data will be used to create the new stroke effect.
## Step 3: Access the Stroke Effect
To modify the stroke effect, you need to access the specific layer and its blending options.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
This ensures you are working with the correct layer and effect.
## Step 4: Modify the Stroke Effect
Now, let's modify the stroke effect with the new pattern data.
### Update Stroke Effect Properties
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### Update the Pattern Resource
```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```
This code snippet updates the pattern resource with the new pattern data.
## Step 5: Apply the New Pattern
Finally, apply the new pattern to the stroke effect and save the changes.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
This ensures the new pattern is applied correctly and the file is saved with the changes.
## Step 6: Verify the Changes
To make sure everything worked correctly, load the file again and verify the changes.
```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```
This step verifies that the pattern data has been correctly applied to the stroke effect.
## Conclusion
And there you have it! You’ve successfully added a stroke layer pattern to a PSD file using Aspose.PSD for Java. By following these steps, you can customize and enhance your images with ease. Happy coding!
## FAQ's
### What is Aspose.PSD for Java?
Aspose.PSD for Java is a library that allows developers to create, edit, and convert PSD (Photoshop Document) files programmatically.
### Can I use Aspose.PSD for Java in a commercial project?
Yes, you can use it in commercial projects. You can purchase a license from [here](https://purchase.aspose.com/buy).
### Is there a free trial available for Aspose.PSD for Java?
Yes, you can download a free trial version from [here](https://releases.aspose.com/).
### How can I get support for Aspose.PSD for Java?
You can get support from the Aspose community forums [here](https://forum.aspose.com/c/psd/34).
### What are the system requirements for Aspose.PSD for Java?
You need JDK installed and an IDE for development. The library supports multiple operating systems including Windows, Linux, and macOS.
