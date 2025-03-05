---
title: Add Level Adjustment Layer in PSD
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
description: Learn how to effectively add a Level Adjustment Layer in your PSD files using Aspose.PSD for Java. Elevate your image editing skills.
type: docs
weight: 16
url: /java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---
## Introduction
When it comes to image editing, managing levels can make a world of difference in the vibrancy and clarity of your photos. One handy tool in the Photoshop arsenal is the "Level Adjustment Layer," which allows you to tweak the tonal range and color balance of your images. In this guide, we'll walk you through how to implement a Level Adjustment Layer in a PSD file using Aspose.PSD for Java. So, grab your Java IDE.
## Prerequisites
Before you jump into the world of level adjustments, you’ll need to set up a few things to ensure a smooth ride:
1. Java Development Kit (JDK): Make sure you have the JDK installed on your machine. If you don’t have it, you can grab it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) or use OpenJDK.
2. Aspose.PSD for Java Library: To manipulate PSD files, you'll need to download the Aspose.PSD library. You can get the latest version from this [download link](https://releases.aspose.com/psd/java/) and ensure you have included the JAR in your project’s library.
3. Basic Knowledge of Java: Having a fundamental understanding of Java programming will help, as we’ll be diving into code snippets throughout this tutorial.
4. IDE Setup: You can use any Java IDE you prefer—like IntelliJ IDEA, Eclipse, or NetBeans—to write and run your code. Just make sure you have set up your Java project and added the Aspose.PSD library.

## Import Packages
Before we start writing our code, we need to import the necessary packages from the Aspose.PSD library. Here’s how you can do it:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
By importing these packages, we’ll have access to the classes necessary for loading, modifying, and saving our PSD files.

Now, let's break down the process into digestible steps. Follow along as we walk through loading a PSD file, adjusting the levels, and then saving your changes. 
## Step 1: Set Up Your File Paths
The first step is to define where our PSD file is located and where we want to save the modified output. You can customize the directory path to suit your needs.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
Here, replace `"Your Document Directory"` with the actual path on your system where your PSD file is stored. This sets the stage for everything we will do next.
## Step 2: Load the PSD File
Now, let’s load the PSD file using the `PsdImage` class. This step is essential as it allows us to access and manipulate the layers.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
When you call `Image.load()`, it will read the PSD file and create an instance of `PsdImage` that you can work with.
## Step 3: Iterate Through the Layers
Since we want to adjust a Level Adjustment Layer, we'll need to loop through each layer in our PSD file. This helps us find the specific layer we want to modify.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
In this loop, `instanceof LevelsLayer` checks if the current layer is a Levels Adjustment Layer. If it is, we can proceed to tweak its properties.
## Step 4: Adjust the Level Channel Settings
Once we identify the correct layer, we can modify its input and output levels. This is where the magic happens! Adjust different parameters to see how they affect the image.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
Here’s what each parameter does:
- Input Midtone Level: Adjusts the mid-tones.
- Input Shadow Level: Tweaks the darker areas of the image.
- Input Highlight Level: Alters the bright areas of the image.
- Output Shadow Level: Sets how dark shadows will appear.
- Output Highlight Level: Sets how light highlights will appear.
Feel free to experiment with different values!
## Step 5: Save the Modified PSD File
Now that we’ve made our adjustments, it’s time to save the modified PSD file. This step is crucial to ensure that your changes are applied and stored.
```java
im.save(psdPathAfterChange);
```
You can now find your adjusted PSD file at the specified `psdPathAfterChange`. 
## Conclusion
You’ve just learned how to add a Level Adjustment Layer to a PSD file using Aspose.PSD for Java! By following this guide, you can adjust the tonal quality of your images effortlessly, paving the way for a more vibrant and visually appealing output. Remember, practice makes perfect, so feel free to tweak the adjustments and explore different PSD files to see the effects of your changes.
## FAQ's
### What is a Level Adjustment Layer?
A Level Adjustment Layer allows you to correct the tonal range in your images, balancing shadows, midtones, and highlights.
### Can I use Aspose.PSD without a purchase?
Yes! Aspose offers a free trial to test the library before purchasing.
### Where can I find documentation for Aspose.PSD?
You can find the documentation [here](https://reference.aspose.com/psd/java/).
### Is there any community support for Aspose products?
Absolutely! You can ask questions and get support in the [Aspose forum](https://forum.aspose.com/c/psd/34).
### How can I get a temporary license for Aspose.PSD?
You can apply for a temporary license [here](https://purchase.aspose.com/temporary-license/).
