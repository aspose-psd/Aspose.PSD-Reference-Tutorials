---
title: Apply Stroke Effect with Color Fill in PSD - Java
linktitle: Apply Stroke Effect with Color Fill in PSD - Java
second_title: Aspose.PSD Java API
description: Learn how to apply a stroke effect with color fill to your PSD files using Aspose.PSD for Java. Follow this step-by-step guide to enhance your images with ease.
type: docs
weight: 21
url: /java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
---
## Introduction

In this guide, we’ll walk you through the process of applying a stroke effect with a color fill to your PSD files using Aspose.PSD for Java. Whether you're a seasoned developer or just starting, this step-by-step tutorial will make it easy for you to get the job done. We’ll cover everything from setting up your environment to saving the final image with the applied effects.

## Prerequisites

Before we begin, let's ensure you have everything you need to follow along with this tutorial:

1. Java Development Kit (JDK) Installed: Make sure you have JDK 8 or higher installed on your system.
2. Aspose.PSD for Java Library: You’ll need the Aspose.PSD for Java library. You can download it from the [website](https://releases.aspose.com/psd/java/).
3. Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse, or any other of your choice.
4. Sample PSD File: A sample PSD file to which you can apply the stroke effect. If you don’t have one, you can create a simple PSD file in Photoshop or download one from the internet.
5. Basic Knowledge of Java: While this tutorial is beginner-friendly, having some basic knowledge of Java will be beneficial.

Once you have these prerequisites in place, you're all set to start applying the stroke effect with color fill to your PSD files.

## Import Packages

To start working with Aspose.PSD for Java, you’ll need to import the necessary packages into your Java project. Here’s how you can do it:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

These imports bring in all the necessary classes you'll need to work with PSD files, apply effects, and save the images in your desired format.

## Step 1: Load the PSD File

The first step in our process is loading the PSD file that you want to modify. Aspose.PSD for Java makes this incredibly simple with its `PsdImage` class. Here’s how you can do it:

### 1.1 Set the Directory Path

First, define the directory path where your PSD files are stored:

```java
String dataDir = "Your Document Directory";
```

Replace `"Your Document Directory"` with the actual path where your PSD file is located.

### 1.2 Load the PSD Image

Now, load the PSD file using the `PsdLoadOptions` and `PsdImage` classes:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

Here, the `PsdLoadOptions` is configured to load the effects resources, ensuring that any existing effects within the PSD are accessible.

## Step 2: Apply Stroke Effect with Color Fill

With the PSD file loaded, the next step is to apply the stroke effect to the layers of the image. This is where the real magic happens.

Each PSD file may contain multiple layers, and you'll need to apply the effect to each one. Here's how to do it:

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    settings.setColor(Color.getDeepPink());
}
```

In this loop:

- `im.getLayers()`: Retrieves all layers in the PSD file.
- `StrokeEffect effect`: Extracts the stroke effect applied to the layer.
- `ColorFillSettings settings`: Modifies the fill settings for the stroke effect.
- `settings.setColor(Color.getDeepPink())`: Sets the stroke color to deep pink. You can change this to any color you prefer.

## Step 3: Save the Modified PSD and Export as PNG

Once you've applied the stroke effect, it's time to save the changes and export the image.

### 3.1 Save the PSD File

To save the modified PSD file, use the following code:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

This saves the file with the applied stroke effect to the specified path.

### 3.2 Export as PNG

To make the image more accessible, you might want to export it as a PNG file. Here’s how:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

This code snippet saves the image as a PNG with true color and alpha transparency, making it ready for use in web applications or other platforms.

## Conclusion

Applying a stroke effect with a color fill to your PSD files using Aspose.PSD for Java is not only straightforward but also incredibly powerful. With just a few lines of code, you can automate complex image processing tasks, saving you both time and effort.

Whether you're working on a large batch of images or just need to tweak a few files, this method provides a flexible and efficient solution. Now that you have the basics down, you can start experimenting with different effects and customizations to make your images truly stand out.

Ready to try it out? Grab your sample PSD file and start adding those stunning effects today!

## FAQ's

### Can I apply multiple effects to a single layer using Aspose.PSD for Java?
Yes, you can apply multiple effects to a single layer by accessing the layer's blending options and adding the desired effects.

### Is it possible to automate the process for a batch of PSD files?
Absolutely! You can loop through a directory of PSD files, apply the stroke effect, and save the results automatically.

### How can I revert changes made to a PSD file using Aspose.PSD for Java?
To revert changes, you would need to reload the original PSD file before saving any modifications. There’s no direct undo feature in Aspose.PSD.

### Can I customize the stroke width and position?
Yes, Aspose.PSD for Java allows you to customize the stroke width, position, and other properties through the `StrokeEffect` class.

### Is the Aspose.PSD for Java library free to use?
Aspose.PSD for Java offers a free trial, but for full access to all features, you would need to purchase a license. You can explore the [buy options](https://purchase.aspose.com/buy) on their website.
