---
title: Draw Red Rectangle with Aspose.PSD for Java
linktitle: Perform Simple Drawing
second_title: Aspose.PSD Java API
description: Learn how to draw red rectangle and other shapes in PSD files using Aspose.PSD for Java. This step‑by‑step guide covers creating documents, adding layers, and drawing with code examples.
weight: 10
url: /java/basic-image-operations/simple-drawing/
date: 2025-12-27
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Draw Red Rectangle with Aspose.PSD for Java

## Introduction

Welcome to this step‑by‑step guide on how to **draw red rectangle** using Aspose.PSD for Java! In this tutorial, we’ll walk through creating a new PSD document, adding a layer, and drawing shapes with custom colors. Whether you’re automating graphic assets or building a design‑tool backend, this tutorial gives you the essential building blocks.

## Quick Answers
- **What is the primary class to create a PSD file?** `PsdImage`
- **Which method clears a layer’s background color?** `Graphics.clear(Color)`
- **How do you draw a red rectangle?** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **Do I need a license for development?** A free trial works for testing; a license is required for production.
- **Can I manipulate existing PSD files with the same API?** Yes, Aspose.PSD supports full PSD editing.

## What is drawing a red rectangle in a PSD file?
Drawing a red rectangle means using the `Graphics` object to render a rectangular shape filled or outlined with the color red onto a specific layer of a PSD image. This operation is common for highlighting areas, creating placeholders, or adding simple graphics programmatically.

## Why use Aspose.PSD for Java to manipulate PSD files?
Aspose.PSD provides a pure‑Java API that lets you read, edit, and write Photoshop PSD files without needing Photoshop installed. It supports layer management, color manipulation, and vector drawing, making it ideal for server‑side image processing, automated asset pipelines, and custom graphic generation.

## Prerequisites

- Java Development Kit (JDK) installed on your machine.  
- Aspose.PSD for Java library. You can download it from the [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/).

## Import Packages

To start, import the required classes into your Java project:

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

First, create a fresh PSD document with the desired canvas size. This document will host the layer on which we’ll draw.

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

Next, add a new blank layer that spans the full width and height of the image. Layers are essential for separating drawing operations.

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## Step 3: Draw Shapes

We’ll use the `Graphics` class to manipulate the layer’s pixel data. Below are three examples that illustrate clearing the background and drawing rectangles with different colors.

### Clear Layer Color (set background to yellow)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### Draw a Red Rectangle (primary focus)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### Draw a Blue Rectangle (additional example)

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## Step 4: Save the Changes

Finally, write the modified PSD image to disk. The file will contain the new layer and the drawn shapes.

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## Common Issues and Solutions

- **Layer not visible after drawing:** Ensure the layer is added to the image **before** creating the `Graphics` object.
- **Colors appear incorrect:** Verify you are using `Color.getRed()` (or other static methods) rather than custom RGB values that may be out of range.
- **File not saved:** Confirm the `outputDir` path exists and the application has write permissions.

## Frequently Asked Questions

### Q1: Can I use Aspose.PSD for Java to manipulate existing PSD files?

A1: Yes, Aspose.PSD for Java provides extensive functionality to edit and manipulate existing PSD files.

### Q2: Where can I find support for Aspose.PSD for Java?

A2: You can visit the [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) for any support‑related queries.

### Q3: Is there a free trial available for Aspose.PSD for Java?

A3: Yes, you can access the free trial version [here](https://releases.aspose.com/).

### Q4: How can I purchase a license for Aspose.PSD for Java?

A4: You can buy a license from the [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy).

### Q5: Are temporary licenses available for Aspose.PSD for Java?

A5: Yes, you can obtain a temporary license from [here](https://purchase.aspose.com/temporary-license/).

## Additional Frequently Asked Questions

**Q: Can I draw other shapes besides rectangles?**  
A: Yes, the `Graphics` class also supports drawing ellipses, lines, and custom paths.

**Q: Does Aspose.PSD support transparency in drawn shapes?**  
A: Absolutely; you can use `SolidBrush` with an ARGB color to include alpha transparency.

**Q: Is it possible to edit the opacity of a layer?**  
A: Yes, each `Layer` object has an `setOpacity` method that accepts a value from 0 to 255.

**Q: How do I load an existing PSD file instead of creating a new one?**  
A: Use `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` before manipulating layers.

## Conclusion

You’ve now learned how to **draw red rectangle** and other basic shapes in a PSD file using Aspose.PSD for Java. By creating a document, adding a layer, clearing its background, and drawing with the `Graphics` API, you can automate many graphic‑design tasks. Explore further by experimenting with different brushes, layer effects, and file formats.

---

**Last Updated:** 2025-12-27  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}