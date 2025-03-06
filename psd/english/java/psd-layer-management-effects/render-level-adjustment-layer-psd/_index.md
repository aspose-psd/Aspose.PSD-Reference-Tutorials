---
title: Render Level Adjustment Layer in PSD Files - Java
linktitle: Render Level Adjustment Layer in PSD Files - Java
second_title: Aspose.PSD Java API
description: Learn how to effortlessly enhance image contrast and vibrancy using Aspose.PSD for Java. Master Levels Adjustment Layers with this step-by-step guide.
weight: 17
url: /java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Render Level Adjustment Layer in PSD Files - Java

## Introduction

Have you ever opened a PSD file only to find the image lacking contrast or vibrancy? Fear not, image editing warriors! Aspose.PSD for Java comes to the rescue with its powerful Levels Adjustment Layer manipulation capabilities. This guide will equip you with the knowledge to fine-tune your images using Levels in a breeze. 

## Prerequisites

- Java Development Kit (JDK): Make sure you have a recent version of JDK installed on your system. You can download it from the Oracle website ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).
- Aspose.PSD for Java Library:  Download the Aspose.PSD for Java library from the download page ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). You'll need a valid license to use the full features, but a free trial is available to get you started ([https://releases.aspose.com/](https://releases.aspose.com/)).

## Import Packages

Before diving into the code, we need to import the necessary Aspose.PSD classes to interact with PSD files. Here's what you'll need:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

The `com.aspose.psd` package provides access to PSD manipulation functionalities, while `com.aspose.psd.imaging.PngOptions` allows us to define options when saving the image as a PNG.

Now, let's embark on our Levels adjustment adventure:

## Step 1: Setting Up File Paths:

- Define variables for your document directory (`dataDir`), source PSD file name (`sourceFileName`), target PSD file name after modification (`psdPathAfterChange`), and the final PNG export path (`pngExportPath`). Consider using descriptive names to improve code readability.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## Step 2: Loading the PSD Image:

- Use the `Image.load` method to open the source PSD file and store it in a `PsdImage` object (`im`). Aspose.PSD automatically detects the file format.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Step 3: Iterating Through Layers:

- We need to find the Levels Adjustment Layer within your PSD. Aspose provides a convenient way to iterate through all layers using a loop.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (code to check for Levels Layer will be added here)
}
```

## Step 4: Identifying the Levels Layer:

- Inside the loop, check if the current layer (`im.getLayers()[i]`) is an instance of the `LevelsLayer` class using the `instanceof` operator. 
- If it is, cast the layer to a `LevelsLayer` object for further manipulation.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (code to adjust levels will be added here)
   }
}
```
## Step 5: Fine-Tuning Levels (Continued):

- Adjust the output levels using `setOutputShadowLevel` and `setOutputHighlightLevel` to control the darkness and lightness of the resulting image. These values determine the range of input levels that will be mapped to the output range.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Adjust Input Levels (0-255):
	   channel.setInputShadowLevel((short) 10); // Darken shadows slightly
	   channel.setInputMidtoneLevel(2.0f);     // Increase midtones
	   channel.setInputHighlightLevel((short) 230); // Reduce highlights

	   // Adjust Output Levels (0-255):
	   channel.setOutputShadowLevel((short) 20); // Darken shadows further
	   channel.setOutputHighlightLevel((short) 200); // Brighten highlights
   }
}
```

## Step 6: Saving the Modified PSD:

- Use the `save` method of the `PsdImage` object to save the modified image to the specified path (`psdPathAfterChange`).

```java
im.save(psdPathAfterChange);
```

## Step 7: Exporting as PNG (Optional):

- If you need a PNG version of the adjusted image, create a `PngOptions` object and set the color type to `TruecolorWithAlpha`. Then, use the `save` method again with the PNG export path and options.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

And there you have it! You've successfully adjusted the Levels Adjustment Layer in your PSD file using Aspose.PSD for Java. By understanding these steps and experimenting with different values, you can enhance the contrast and overall appearance of your images.

## Conclusion

Aspose.PSD for Java empowers you to take control of your image editing process. By mastering the Levels Adjustment Layer, you can breathe new life into your photos and designs. Remember, practice makes perfect, so don't hesitate to experiment and explore the full potential of this powerful tool.
 
## FAQ's

### Can I adjust individual color channels (RGB) separately? 
Yes, you can access each color channel using the `getChannel` method of the `LevelsLayer` object and modify its levels independently.

### How do I handle multiple Levels Adjustment Layers in a PSD?
The code iterates through all layers, so it will automatically process any additional Levels layers found in the image.

### Are there other ways to adjust image contrast besides Levels?
Absolutely! Aspose.PSD offers various image adjustment tools like Curves, Brightness/Contrast, and more.

### Can I automate this process for multiple images? 
Yes, you can incorporate this code into a loop or batch processing script to efficiently process multiple PSD files.

### Where can I find more information and support?
Aspose provides extensive documentation ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) and a support forum ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) for any questions or issues you may encounter.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
