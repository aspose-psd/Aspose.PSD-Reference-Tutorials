---
title: Perform Simple Drawing with Aspose.PSD for Java
linktitle: Perform Simple Drawing
second_title: Aspose.PSD Java API
description: Learn how to draw shapes in PSD files using Aspose.PSD for Java. This step-by-step guide covers creating, adding layers, and drawing with code examples.
type: docs
weight: 10
url: /java/basic-image-operations/simple-drawing/
---
## Introduction

Welcome to this step-by-step guide on performing simple drawing using Aspose.PSD for Java! In this tutorial, we will explore the basics of creating a new PSD document, adding layers, and drawing shapes with different colors. Aspose.PSD for Java is a powerful library that enables you to manipulate PSD files programmatically, providing extensive functionality for graphic design tasks.

## Prerequisites

Before diving into the tutorial, make sure you have the following prerequisites in place:

- Java Development Kit (JDK) installed on your machine.
- Aspose.PSD for Java library. You can download it from the [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/).

## Import Packages

To get started, import the necessary packages into your Java project. Include the following code at the beginning of your Java file:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## Step 1: Create a New Document

Let's start by creating a new PSD document with a specified width and height:

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## Step 2: Add a Layer

Now, let's add a layer to the document using the no-argument constructor:

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## Step 3: Draw Shapes

In this step, we will use the Graphics class to draw shapes on the created layer:

### Draw a Rectangle with a Yellow Color

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Draw a Red Rectangle

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### Draw a Blue Rectangle

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Step 4: Save the Changes

Finally, save a copy of the loaded PSD file including the changes:

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## Conclusion

Congratulations! You've successfully performed simple drawing using Aspose.PSD for Java. This tutorial covered creating a new document, adding layers, and drawing rectangles with different colors. Feel free to explore more advanced features offered by the library for your graphic design needs.

## FAQ's

### Q1: Can I use Aspose.PSD for Java to manipulate existing PSD files?

A1: Yes, Aspose.PSD for Java provides extensive functionality to edit and manipulate existing PSD files.

### Q2: Where can I find support for Aspose.PSD for Java?

A2: You can visit the [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) for any support-related queries.

### Q3: Is there a free trial available for Aspose.PSD for Java?

A3: Yes, you can access the free trial version [here](https://releases.aspose.com/).

### Q4: How can I purchase a license for Aspose.PSD for Java?

A4: You can buy a license from the [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy).

### Q5: Are temporary licenses available for Aspose.PSD for Java?

A5: Yes, you can obtain a temporary license from [here](https://purchase.aspose.com/temporary-license/).
