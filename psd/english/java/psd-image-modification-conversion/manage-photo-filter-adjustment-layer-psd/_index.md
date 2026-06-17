---
title: How to Create Photo Filter Layer in PSD Using Java
linktitle: How to Create Photo Filter Layer in PSD Using Java
second_title: Aspose.PSD Java API
description: Learn how to create photo filter layer and add adjustment layer PSD files using Aspose.PSD for Java. Follow this guide for editing and adding filters effortlessly.
weight: 24
date: 2026-03-28
url: /java/psd-image-modification-conversion/manage-photo-filter-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Manage Photo Filter Adjustment Layer in PSD - Java

## Introduction
If you’re a Java developer looking to **create photo filter layer** objects inside PSD files, you’ve landed in the right spot. In this tutorial we’ll walk through using Aspose.PSD for Java to both edit existing Photo Filter Adjustment Layers and to add new ones. By the end, you’ll know exactly how to **create photo filter layer**, adjust its properties, and even **add adjustment layer PSD** files programmatically—speeding up your graphic‑design workflow.

## Quick Answers
- **Which library handles PSD layers in Java?** Aspose.PSD for Java  
- **Can I edit an existing Photo Filter layer?** Yes – load the PSD, locate the `PhotoFilterLayer`, then modify its properties.  
- **How do I add a new filter layer?** Use `addPhotoFilterLayer(Color)` on a `PsdImage` instance.  
- **Do I need a license for production?** A commercial license is required; a free trial is available.  
- **What Java version is supported?** JDK 8 or higher (JDK 11 recommended).  

## What is a Photo Filter Adjustment Layer?
A Photo Filter Adjustment Layer is a non‑destructive effect that tints the entire image with a chosen color, similar to applying a photographic filter. It lives on its own layer, allowing you to tweak color, density, and luminosity without altering the original pixels.

## Why use Aspose.PSD to create photo filter layer?
- **Full control** over PSD structure without Adobe Photoshop.  
- **Cross‑platform** Java API works on Windows, Linux, and macOS.  
- **No COM interop** – pure Java, ideal for server‑side processing.  
- **Supports PSD version 1‑8**, preserving layer effects and masks.

## Prerequisites
### Essential Software
1. Java Development Kit (JDK): Make sure you have a compatible version of JDK installed on your machine. You can download it from [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java: To manipulate PSD files, you’ll need the Aspose.PSD library. You can download it from the [Aspose releases page](https://releases.aspose.com/psd/java/). Don’t forget to check out the [Aspose documentation](https://reference.aspose.com/psd/java/) for more details.
3. IDE (Integrated Development Environment): A good IDE like IntelliJ IDEA or Eclipse will make your coding experience smoother.

### Understanding the Basics
Familiarity with Java programming and a basic understanding of how PSD files work will be beneficial. If you’re new to using libraries in Java, it’s a good idea to get accustomed to importing and utilizing frameworks.

## Import Packages
To get started, we need to import the necessary classes from the Aspose.PSD library. Here’s a simple import statement you’ll need at the beginning of your Java file:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PhotoFilterLayer;
```
Simply paste this at the top of your Java file, and you’re set to begin working with PSD images!

## Editing Existing Photo Filter Layer
### Step 1: Set Up the Data Directory
Firstly, you need to define the directory where your PSD files are stored. Replace `"Your Document Directory"` with the actual path. This is how you get everything organized:
```java
String dataDir = "Your Document Directory";
```

### Step 2: Load Your PSD File
Now, let’s load up the PSD file you want to edit. Make sure that `PhotoFilterAdjustmentLayer.psd` exists in your specified directory.
```java
String sourceFileName = dataDir + "PhotoFilterAdjustmentLayer.psd";
```

### Step 3: Initialize the Image Object
Using Aspose's built‑in functionality, we load the image into our project:
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### Step 4: Iterate Through the Layers
Next up, we’ll examine the layers within the PSD file. Our goal is to locate the `PhotoFilterLayer`:
```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof PhotoFilterLayer) {
        PhotoFilterLayer photoLayer = (PhotoFilterLayer) im.getLayers()[i];
        // Make changes to the layer
    }
}
```

### Step 5: Customize the Photo Filter Layer
Here's where the magic happens! You can modify the `Color` and `Density`. For example, we can set the color to a vibrant red and adjust the density:
```java
photoLayer.setColor(Color.fromArgb(255, 60, 60));
photoLayer.setDensity(78);
photoLayer.setPreserveLuminosity(false);
```

### Step 6: Save the Edited PSD File
Finally, save the changes to create a new PSD file with your adjustments:
```java
String psdPathAfterChange = dataDir + "PhotoFilterAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
You've just edited a Photo Filter Adjustment Layer in a PSD file.

## Adding a New Photo Filter Layer
### Step 1: Set Up Directory Path
As before, we begin with defining our data directory:
```java
String dataDir = "Your Document Directory";
```

### Step 2: Load the Source File
For this example, let’s load a different PSD file where we want to **add adjustment layer PSD**:
```java
String sourceFileName = dataDir + "PhotoExample.psd";
```

### Step 3: Initialize the Image Object Again
We must create a new `PsdImage` instance, so we load the file:
```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### Step 4: Add a Photo Filter Layer
Now, we can add a new Photo Filter layer with a customized color. Here’s how it’s done:
```java
PhotoFilterLayer layer = img.addPhotoFilterLayer(Color.fromArgb(25, 255, 35));
```

### Step 5: Save the New PSD File
Once again, it’s time to save our changes. Here's the line to do just that:
```java
String psdPathAfterChange = dataDir + "PhotoExampleAddedPhotoFilter.psd";
img.save(psdPathAfterChange);
```
You’ve successfully added a new photo filter layer to your PSD file.

## Common Issues and Solutions
- **`ClassCastException` when loading the image** – Ensure the file you load is a PSD; other formats require different classes.  
- **Color values appear incorrect** – Use `Color.fromArgb(alpha, red, green, blue)` where each component is 0‑255.  
- **Layer not found** – Verify that the source PSD actually contains a `PhotoFilterLayer`. Use `im.getLayers().length` to debug.

## Frequently Asked Questions
### What is Aspose.PSD?
Aspose.PSD is a .NET and Java library to create, edit, and convert PSD files.

### Can I try Aspose.PSD for free?
Yes, Aspose offers a free trial version. Check it out [here](https://releases.aspose.com/).

### Where can I find the documentation?
You can find complete documentation on [Aspose's reference page](https://reference.aspose.com/psd/java/).

### How can I purchase Aspose.PSD?
You can buy the software from [this link](https://purchase.aspose.com/buy).

### Is there support available for Aspose.PSD?
Absolutely! You can get support through the Aspose support forum [here](https://forum.aspose.com/c/psd/34).

---

**Last Updated:** 2026-03-28  
**Tested With:** Aspose.PSD for Java 24.11 (latest as of 2026)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}