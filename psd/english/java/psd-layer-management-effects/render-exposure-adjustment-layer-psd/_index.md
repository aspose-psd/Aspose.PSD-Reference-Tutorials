---
title: Render Exposure Adjustment Layer in PSD Files - Java
linktitle: Render Exposure Adjustment Layer in PSD Files - Java
second_title: Aspose.PSD Java API
description: Learn how to render and adjust exposure layers in PSD files using Aspose.PSD for Java. Step-by-step guide with code examples for modifying and adding exposure layers.
weight: 15
url: /java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Render Exposure Adjustment Layer in PSD Files - Java

## Introduction

Are you working with Photoshop PSD files and need to adjust the exposure or add an exposure adjustment layer programmatically? Whether you're tweaking existing layers or adding new ones, Aspose.PSD for Java provides a powerful and intuitive way to handle these tasks. In this guide, we'll walk through how to use Aspose.PSD for Java to render and modify exposure adjustment layers in PSD files. By the end of this tutorial, you'll know how to adjust exposure settings in existing layers and add new exposure adjustment layers to your PSD files. Let's dive in!

## Prerequisites

Before we jump into the tutorial, make sure you have the following prerequisites:

1. Java Development Kit (JDK): You need to have JDK installed on your machine. This guide assumes you have at least JDK 8.
2. Aspose.PSD for Java: You need the Aspose.PSD library to work with PSD files. You can download it from [here](https://releases.aspose.com/psd/java/).
3. Basic Knowledge of Java: Familiarity with Java programming will help you follow along easily.
4. IDE or Text Editor: Use any IDE like IntelliJ IDEA, Eclipse, or a text editor of your choice to write and run Java code.

## Import Packages

First things first, let's import the necessary packages from Aspose.PSD for Java. This step ensures that our code can utilize the library’s features for manipulating PSD files.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## Step 1: Load the PSD File

To begin, you need to load your PSD file into the application. Here’s how you can do it:

```java
String dataDir = "Your Document Directory";  // Define your document directory
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  // Source PSD file path

PsdImage im = (PsdImage) Image.load(sourceFileName);  // Load the PSD file
```

In this code snippet, replace `"Your Document Directory"` with the path where your PSD files are located. The `Image.load()` method loads the PSD file into an instance of `PsdImage`, which allows you to manipulate its layers.

## Step 2: Edit Existing Exposure Adjustment Layer

Once the PSD file is loaded, you can access and modify existing layers. If the file contains an exposure adjustment layer, you can adjust its properties:

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  // Adjust the exposure level
        expLayer.setOffset(-0.25f);  // Set the offset
        expLayer.setGammaCorrection(0.5f);  // Adjust the gamma correction
    }
}
```

In this loop, we iterate over all layers of the PSD file. If we find an `ExposureLayer`, we modify its `Exposure`, `Offset`, and `GammaCorrection` properties. This allows you to fine-tune the visual output of the exposure adjustment layer.

## Step 3: Save the Modified PSD File

After making changes, you need to save the updated PSD file:

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  // Path to save the modified PSD file

im.save(psdPathAfterChange);  // Save the changes to the PSD file
```

This line saves the modified PSD file to the specified path, preserving your exposure adjustments.

## Step 4: Export as PNG

To export the updated PSD file as a PNG, follow these steps:

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // Path to save the PNG file

PngOptions saveOptions = new PngOptions();  // Create PNG options
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

im.save(pngExportPath, saveOptions);  // Save as PNG
```

Here, `PngOptions` is used to configure the PNG export settings. `PngColorType.TruecolorWithAlpha` ensures that the PNG file retains color depth and transparency.

## Step 5: Add a New Exposure Adjustment Layer

If you want to add a new exposure adjustment layer to an existing PSD file, you can do so with the following code:

```java
String sourceFileName = dataDir + "PhotoExample.psd";  // Source PSD file path

PsdImage img = (PsdImage) Image.load(sourceFileName);  // Load the PSD file

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  // Add new exposure adjustment layer

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  // Path to save the modified PSD file
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // Path to save the PNG file

img.save(psdPathAfterChange);  // Save the changes to the PSD file

PngOptions options = new PngOptions();  // Create PNG options
options.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

img.save(pngExportPath, options);  // Save as PNG
```

In this step, a new exposure adjustment layer is added to the PSD file with specified exposure, offset, and gamma correction values. The updated PSD and PNG files are then saved.

## Conclusion

And there you have it! You've learned how to render and adjust exposure layers in PSD files using Aspose.PSD for Java. We covered how to modify existing exposure layers, add new ones, and export your work as PNG files. Whether you're tweaking photos or preparing design assets, these skills will enhance your ability to manage PSD files programmatically. Happy coding!

## FAQ's

### What is Aspose.PSD for Java?

Aspose.PSD for Java is a library that allows you to create, edit, and convert PSD files programmatically using Java. It provides comprehensive functionality for working with Photoshop documents.

### Can I use Aspose.PSD for Java to manipulate other types of layers?

Yes, Aspose.PSD for Java supports various types of layers, including text layers, adjustment layers, and image layers, allowing extensive manipulation of PSD files.

### How do I get started with Aspose.PSD for Java?

You can start by downloading the library from the [website](https://releases.aspose.com/psd/java/) and referring to the [documentation](https://reference.aspose.com/psd/java/) for detailed guides and examples.

### Is there a free trial available for Aspose.PSD for Java?

Yes, a free trial is available. You can download it [here](https://releases.aspose.com/).

### How can I get support for Aspose.PSD for Java?

For support, you can visit the [Aspose support forum](https://forum.aspose.com/c/psd/34) where you can ask questions and get help from the community.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
