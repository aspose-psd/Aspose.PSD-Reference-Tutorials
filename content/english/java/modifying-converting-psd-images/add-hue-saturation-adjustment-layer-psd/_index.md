---
title: Add Hue Saturation Adjustment Layer to PSD
linktitle: Add Hue Saturation Adjustment Layer to PSD
second_title: Aspose.PSD Java API
description: Learn how to add hue saturation adjustment layers to PSD using Aspose.PSD for Java in this comprehensive, step-by-step tutorial. Enhance your graphic design workflow.
type: docs
weight: 14
url: /java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---
## Introduction
When it comes to graphic design, color manipulation plays a pivotal role—specifically, tweaking hue, saturation, and lightness can drastically transform the mood and quality of any image. One effective way to achieve this is through the use of adjustment layers in Photoshop (PSD files). If you're looking to enhance your PSD files programmatically using Java, the Aspose.PSD library is here to help! This tutorial will take you through the steps to add a Hue Saturation Adjustment Layer to your PSD files, making your workflows more productive and efficient.
In this guide, we’ll cover everything from importing necessary packages to the nitty-gritty details of the code examples.
## Prerequisites
Before we jump into the code, make sure you have the following in place:
1. Java Development Kit (JDK): Ensure you have JDK 8 or above installed on your machine. You can download it from the [Java SE Development Kit Downloads](https://www.oracle.com/java/technologies/javase-downloads.html).
2. Aspose.PSD for Java Library: You’ll need to have the Aspose.PSD library, which you can [download here](https://releases.aspose.com/psd/java/). 
3. IDE: A suitable Integrated Development Environment (IDE) like IntelliJ IDEA or Eclipse for Java development.
4. Basic Java Knowledge: Familiarity with Java programming is a plus, but don’t worry; we’ll walk you through the code step by step.
Now that we have our prerequisites sorted, let's move on to the fun part—coding!
## Import Packages
To start working with the Aspose.PSD library, the first step is to import the necessary classes. Here’s how you can do it in your Java file:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
Make sure that you have the appropriate libraries added to your project so that these imports work seamlessly.
## Step 1: Set Up Your Document Directory
Every project needs a starting point, and ours is no exception. You need to specify a directory where your PSD files are stored. This is crucial for loading and saving images properly.
```java
String dataDir = "Your Document Directory"; // Update this path to your actual directory
```
## Step 2: Load an Existing PSD File
To manipulate an existing PSD file, we first need to load it into our program. Here’s how you can do that:
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
In this code, update `"HueSaturationAdjustmentLayer.psd"` to the name of your existing PSD file that you want to edit.
## Step 3: Edit the Hue/Saturation Layer
Next, we’ll loop through the layers of our loaded PSD image to find and edit any existing Hue/Saturation layers. This step involves modifying the hue, saturation, and lightness values.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```
In this example:
- We're adjusting the hue to -25, saturation to -12, and lightness to +67.
- The `getRange(2)` method allows us to tweak specific color ranges as desired.
## Step 4: Save the Modified PSD File
After making adjustments, the next step is to save the file. This is a vital part of our process, ensuring that the changes we’ve made are not lost.
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## Step 5: Add a New Hue/Saturation Layer
Next, you may want to add a new Hue/Saturation adjustment layer to another PSD file. Just follow the same approach you used earlier but with different PSD files.
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## Step 6: Set New Hue/Saturation Values for the New Layer
Now that you’ve created this new layer, apply the desired hue, saturation, and lightness settings just like before.
```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```
## Step 7: Save the Updated PSD File
Finally, save the PSD file with the added Hue/Saturation layer so you can see your changes.
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
Congratulations! You’ve successfully manipulated PSD files using Aspose.PSD for Java. Now, you can experiment with different images and deeper alterations, bringing your graphic design projects to life.
## Conclusion
Working with graphics programmatically opens up a world of possibilities. Using Aspose.PSD for Java to add and modify Hue Saturation Adjustment Layers provides flexibility and efficiency that can streamline your design workflow. Whether you’re enhancing photos for a project or creating stunning visual content, mastering these tools can greatly improve your output.
Feel free to explore more functionalities of Aspose.PSD by diving into [documentation](https://reference.aspose.com/psd/java/) or consider snagging a [temporary license](https://purchase.aspose.com/temporary-license/) to test out the full power of the library.
## FAQ's
### What is a Hue Saturation Adjustment Layer?
A Hue Saturation Adjustment Layer allows you to modify the color properties of an image without permanently altering the original pixels.
### Do I need Photoshop installed to use Aspose.PSD?
No, Aspose.PSD is a standalone library that works independently of Photoshop.
### Can I use Aspose.PSD for batch processing?
Yes, you can automate and batch process multiple PSD files with Aspose.PSD.
### Is Aspose.PSD free?
Aspose.PSD offers a free trial, but a license is required for long-term use. You can view pricing [here](https://purchase.aspose.com/buy).
