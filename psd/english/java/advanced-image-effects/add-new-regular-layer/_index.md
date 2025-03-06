---
title: Add a New Regular Layer to PSD with Aspose.PSD for Java
linktitle: Add a New Regular Layer to PSD
second_title: Aspose.PSD Java API
description: Learn how to add a new regular layer to PSD files using Aspose.PSD for Java. Follow our step-by-step guide for seamless PSD manipulation.
weight: 11
url: /java/advanced-image-effects/add-new-regular-layer/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Add a New Regular Layer to PSD with Aspose.PSD for Java

## Introduction

Welcome to this comprehensive tutorial on using Aspose.PSD for Java to add a new regular layer to a PSD file. Aspose.PSD is a powerful Java library that allows developers to manipulate and work with PSD files efficiently. In this tutorial, we'll guide you through the process of adding a new regular layer to a PSD file, providing detailed steps and code examples.

## Prerequisites

Before diving into the tutorial, make sure you have the following prerequisites in place:

- Java Development Environment: Ensure that you have a Java development environment set up on your system.
- Aspose.PSD Library: Download and install the Aspose.PSD for Java library. You can find the library [here](https://releases.aspose.com/psd/java/).

## Import Packages

To get started, import the necessary packages into your Java project. These packages are essential for working with Aspose.PSD functionalities. Include the following lines at the beginning of your Java file:

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Step 1: Load PSD File

Load the PSD file you want to edit using the following code:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Step 2: Prepare Data Arrays and Rectangles

Prepare two int arrays and two Rectangle objects as follows:

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## Step 3: Initialize Layer Data

Initialize data arrays with a default value:

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## Step 4: Add Regular Layers

Add two regular layers to the PSD image:

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

## Step 5: Save PSD and PNG

Save the modified PSD and an additional PNG file:

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

Congratulations! You have successfully added a new regular layer to a PSD file using Aspose.PSD for Java.

## Conclusion

In this tutorial, we covered the process of adding a new regular layer to a PSD file using Aspose.PSD for Java. This powerful library simplifies PSD manipulation, making it accessible for Java developers. Experiment with different parameters and functionalities to explore the full potential of Aspose.PSD.

## FAQ's

### Q1: Is Aspose.PSD compatible with Java 8?

A1: Yes, Aspose.PSD supports Java 8 and later versions.

### Q2: Can I apply transformations to the added layers?

A2: Absolutely! Aspose.PSD provides a range of transformation options for layers.

### Q3: Where can I find additional Aspose.PSD documentation?

A3: You can refer to the documentation [here](https://reference.aspose.com/psd/java/).

### Q4: How can I obtain a temporary license for Aspose.PSD?

A4: Visit [this link](https://purchase.aspose.com/temporary-license/) for temporary license options.

### Q5: Are there any community forums for Aspose.PSD support?

A5: Yes, you can find support and discussions [here](https://forum.aspose.com/c/psd/34).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
