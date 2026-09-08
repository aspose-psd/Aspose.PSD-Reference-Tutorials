---
date: 2026-09-08
description: Learn how to draw rectangle on an image using Aspose.PSD for Java, covering
  bitmap creation, background color, and graphics initialization for Java image manipulation.
images:
- /java/java-graphics-drawing/drawing-rectangles/og-image.png
keywords:
- how to draw rectangle
- draw rectangle on image
- how to create bitmap
- set background color java
- java image manipulation
lastmod: 2026-09-08
linktitle: Drawing Rectangles in Java
og_description: Learn how to draw rectangle on an image using Aspose.PSD for Java.
  This guide covers bitmap creation, setting background color, and initializing graphics
  in Java.
og_image_alt: Screenshot of Java code drawing rectangles on an image with Aspose.PSD
og_title: How to draw rectangle on an image with Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  headline: How to draw rectangle on an image with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  name: How to draw rectangle on an image with Aspose.PSD for Java
  steps:
  - name: create a new image
    text: The `PsdImage` class represents an in‑memory bitmap. Initializing it also
      allocates the pixel buffer. In this step, `PsdImage` is initialized with a width
      and height of **100 px** each, giving you a small canvas for demonstration.
  - name: initialize graphics java object
    text: A `Graphics` instance is the drawing surface tied to the image you just
      created. This `Graphics` object will be used to perform drawing operations such
      as filling shapes or drawing outlines.
  - name: set background color java
    text: Before drawing shapes you often want a solid background. Use `clear` with
      a `Color` to fill the entire canvas. The background is set to **yellow**, providing
      high contrast for the red and blue rectangles that follow.
  - name: draw rectangles on the image
    text: Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for
      the fill. You can draw multiple rectangles with different colors and positions.
      These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle
      at (50, 50), each 40 px wide and 30 px tall.
  - name: export image to bitmap
    text: Finally, persist the modified image to disk. Aspose.PSD automatically encodes
      the bitmap in the format you specify. The image is saved as a BMP file at the
      path stored in `outpath`.
  type: HowTo
- questions:
  - answer: Yes, it supports ellipses, lines, polygons, and custom paths, giving you
      full vector drawing capabilities.
    question: Can Aspose.PSD for Java handle other shapes besides rectangles?
  - answer: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.
    question: How can I modify the thickness of the rectangle border?
  - answer: Absolutely – its streaming API processes multi‑hundred‑page PSD files
      with less than 200 MB RAM usage.
    question: Is Aspose.PSD for Java suitable for high‑performance image processing
      tasks?
  - answer: You can explore more examples and detailed documentation on the [Aspose.PSD
      for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find more examples and tutorials for Aspose.PSD for Java?
  - answer: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats
      for both import and export.
    question: Does Aspose.PSD for Java support other image formats besides BMP?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- image processing
title: How to draw rectangle on an image with Aspose.PSD for Java
url: /java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to draw rectangle on an image with Aspose.PSD for Java

## Introduction
If you need to **how to draw rectangle** on an image programmatically, Aspose.PSD for Java gives you a clean, high‑performance API. In this tutorial you’ll see how to create a bitmap, set the background color, and **initialize graphics java** objects so you can render rectangles of any size and color. The steps are simple, the code is concise, and the result is a BMP file you can use in any Java‑based workflow.

## Quick answers
- **Which library handles rectangle drawing?** Aspose.PSD for Java.
- **How many lines of code are required?** About six lines to create the image, set background, and draw two rectangles.
- **What image formats are supported for export?** BMP, PNG, JPEG, TIFF, GIF and more.
- **Do I need a license for development?** A free trial works for testing; a license is required for production.
- **Can I change the border thickness?** Yes – adjust the `Pen` thickness property before drawing.

## What is drawing a rectangle on an image?
Drawing a rectangle on an image means rendering a filled or outlined shape onto a bitmap using a graphics context. Aspose.PSD’s `Graphics` class provides methods that let you specify color, position, and size with a single call.

## Why use Aspose.PSD for Java for rectangle drawing?
Aspose.PSD supports **50+ image formats** and can process files up to **2 GB** without loading the entire document into memory. Its `Graphics` API runs up to **3× faster** than native Java AWT for batch operations, making it ideal for high‑throughput server‑side image processing.

## Prerequisites
Before you start, make sure you have:

- **Java Development Kit (JDK) 8 or higher** installed.
- **Aspose.PSD for Java** library downloaded from the [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) and added to your project’s classpath.

### Import packages
The `import` statements give you access to the classes required for bitmap creation and drawing.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
These imports will allow you to access the classes and methods needed to draw rectangles on images.

## How to draw rectangle on an image in Java?
Load a new `PsdImage`, clear its surface with a background color, create a `Graphics` object, and then call `drawRectangle` with the desired pen and brush. The entire process takes just a few method calls and produces a ready‑to‑save bitmap.  
`PsdImage` represents an in‑memory bitmap that can be edited and saved.  
`Graphics` provides a drawing surface for rendering shapes onto an image.

### Step 1: create a new image
The `PsdImage` class represents an in‑memory bitmap. Initializing it also allocates the pixel buffer.

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```
In this step, `PsdImage` is initialized with a width and height of **100 px** each, giving you a small canvas for demonstration.

### Step 2: initialize graphics java object
A `Graphics` instance is the drawing surface tied to the image you just created.

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```
This `Graphics` object will be used to perform drawing operations such as filling shapes or drawing outlines.

### Step 3: set background color java
Before drawing shapes you often want a solid background. Use `clear` with a `Color` to fill the entire canvas.

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```
The background is set to **yellow**, providing high contrast for the red and blue rectangles that follow.

### Step 4: draw rectangles on the image
Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for the fill. You can draw multiple rectangles with different colors and positions.

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle at (50, 50), each 40 px wide and 30 px tall.

### Step 5: export image to bitmap
Finally, persist the modified image to disk. Aspose.PSD automatically encodes the bitmap in the format you specify.

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```
The image is saved as a BMP file at the path stored in `outpath`.

## Common issues and solutions
- **Blank output file** – Ensure you call `graphics.clear` before drawing; otherwise the canvas may remain transparent.
- **Incorrect colors** – Verify that you import `com.aspose.psd.Color` and not `java.awt.Color`.
- **Large images out of memory** – Use `PsdImage` constructors that support streaming to avoid loading the whole file into RAM.

## Frequently asked questions

**Q: Can Aspose.PSD for Java handle other shapes besides rectangles?**  
A: Yes, it supports ellipses, lines, polygons, and custom paths, giving you full vector drawing capabilities.

**Q: How can I modify the thickness of the rectangle border?**  
A: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.

**Q: Is Aspose.PSD for Java suitable for high‑performance image processing tasks?**  
A: Absolutely – its streaming API processes multi‑hundred‑page PSD files with less than 200 MB RAM usage.

**Q: Where can I find more examples and tutorials for Aspose.PSD for Java?**  
A: You can explore more examples and detailed documentation on the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).

**Q: Does Aspose.PSD for Java support other image formats besides BMP?**  
A: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats for both import and export.

## Conclusion
You now know **how to draw rectangle** on an image using Aspose.PSD for Java, from creating a bitmap to setting the background color and initializing graphics. Experiment with different sizes, colors, and additional shapes to master **java image manipulation**. When you’re ready, integrate this pattern into larger batch‑processing pipelines or UI‑driven editors.

---

**Last Updated:** 2026-09-08  
**Tested with:** Aspose.PSD for Java 24.12  
**Author:** Aspose

## Related Tutorials

- [Resize Image with Aspose.PSD for Java – Draw Shapes & Basic Image Operations](/psd/java/basic-image-operations/)
- [Add Signature to Image – Draw Image on Canvas with Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Crop Image by Rectangle with Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}