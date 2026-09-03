---
date: 2026-09-03
description: Learn how to java graphics draw arc using Aspose.PSD for Java. Step‑by‑step
  guide with code snippets for creating arcs in PSD files.
images:
- /java/java-graphics-drawing/drawing-arcs/og-image.png
keywords:
- java graphics draw arc
- how to draw arcs java
- Aspose.PSD arc drawing
lastmod: 2026-09-03
linktitle: Drawing Arcs in Java
og_description: Learn how to java graphics draw arc with Aspose.PSD for Java. This
  tutorial shows prerequisites, code steps, and tips for creating arcs in PSD files.
og_image_alt: Screenshot of a Java program drawing an arc using Aspose.PSD
og_title: How to java graphics draw arc in Java – Aspose.PSD guide
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to java graphics draw arc using Aspose.PSD for Java. Step‑by‑step
    guide with code snippets for creating arcs in PSD files.
  headline: How to java graphics draw arc in Java
  type: TechArticle
- description: Learn how to java graphics draw arc using Aspose.PSD for Java. Step‑by‑step
    guide with code snippets for creating arcs in PSD files.
  name: How to java graphics draw arc in Java
  steps:
  - name: set up your Java project
    text: Create a new Java project in your favourite IDE and add the Aspose.PSD JAR
      to the build path. Ensure the JAR is referenced correctly so the compiler can
      locate the library classes.
  - name: import required packages
    text: 'To begin, import the necessary packages from Aspose.PSD for Java: The `Pen`
      class defines the colour, width, and style of the line used to draw the arc.
      These imports expose the `PsdImage`, `Graphics`, `Pen`, and colour classes needed
      for arc drawing.'
  - name: initialise image and graphics objects
    text: 'Create an instance of `PsdImage` and obtain a `Graphics` object to draw
      on: Replace `"Your Document Directory"` with the folder where you want the output
      files saved.'
  - name: define arc parameters
    text: 'Set the geometry and style of the arc—its bounding rectangle, start angle,
      sweep angle, colour, and thickness: Adjust the values to match the visual design
      you need; for example, a 200 px radius arc starting at 45° and sweeping 270°.'
  - name: draw the arc and save the image
    text: 'Invoke `drawArc` on the `Graphics` object and persist the PSD (or export
      to another format): The `drawArc` method of the `Graphics` class renders an
      arc defined by a bounding rectangle, start angle, and sweep angle using the
      specified `Pen`. The snippet draws the arc on the canvas and saves it as a '
  type: HowTo
- questions:
  - answer: Yes, the library can draw rectangles, ellipses, lines, polygons, and custom
      paths using the same `Graphics` API.
    question: Can Aspose.PSD for Java handle other shapes besides arcs?
  - answer: Create a `Pen` with the desired `Color` and width, then pass that `Pen`
      instance to `drawArc`.
    question: How do I change the arc colour and thickness?
  - answer: Absolutely. Aspose.PSD supports PNG, JPEG, TIFF, GIF and many more – just
      change the file extension in the `save` method.
    question: Is it possible to export the PSD to a format other than BMP?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for tutorials,
      code samples, and assistance from other developers.
    question: Where can I find more examples and community support?
  - answer: Yes, it can process files up to 2 GB and render arcs without loading the
      entire document into memory, thanks to its streaming architecture.
    question: Does the library work with large PSD files?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- arc drawing
- PSD manipulation
title: How to java graphics draw arc in Java
url: /java/java-graphics-drawing/drawing-arcs/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to Java graphics draw arc in Java

## Introduction
In this tutorial you’ll discover how to **java graphics draw arc** using the Aspose.PSD for Java library. Drawing arcs programmatically is a common requirement for custom UI components, data visualisations, and graphic‑rich reports. Aspose.PSD for Java gives you full control over PSD (Photoshop Document) files, letting you create, edit, and export images without Photoshop installed.

## Quick answers
- **Which library supports arc drawing in Java?** Aspose.PSD for Java.
- **Do I need a license for production use?** Yes, a commercial license is required for non‑trial deployments.
- **What file formats can I export to?** BMP, PNG, JPEG, TIFF, GIF and more.
- **Can I change arc thickness and colour?** Yes, via the `Pen` object passed to `drawArc`.
- **Is the API compatible with Java 8 and later?** Fully compatible with Java 8‑21.

## What is Java graphics draw arc?
`java graphics draw arc` refers to the process of rendering a curved line segment—an arc—onto a graphics surface using Java’s drawing APIs. In the context of Aspose.PSD, the operation is performed on a `Graphics` object that represents a layer inside a PSD file.

## Why use Aspose.PSD for Java to draw arcs?
Aspose.PSD supports **50+** image and document formats, can handle PSD files with **up to 2 GB** size, and processes multi‑hundred‑page documents without loading the entire file into memory. This quantified performance makes it ideal for server‑side graphics generation where speed and memory usage matter.

## Prerequisites
1. **Java Development Environment** – Install Java from [Oracle's website](https://www.oracle.com/java/).  
2. **Aspose.PSD for Java Library** – Download the latest JAR from the [download page](https://releases.aspose.com/psd/java/). Follow the provided instructions to add the JAR to your project’s classpath.

## How to Java graphics draw arc in Java?
Load a new `PsdImage`, obtain its `Graphics` surface, configure a `Pen` with the desired colour and thickness, and call `drawArc`. This concise sequence creates the arc and saves the result in a single method chain. By adjusting the bounding rectangle and angle parameters you can control the size, position, and sweep of the arc to fit your design requirements.

### Step 1: set up your Java project
Create a new Java project in your favourite IDE and add the Aspose.PSD JAR to the build path. Ensure the JAR is referenced correctly so the compiler can locate the library classes.

### Step 2: import required packages
To begin, import the necessary packages from Aspose.PSD for Java:
The `Pen` class defines the colour, width, and style of the line used to draw the arc.
```java
import com.aspose.psd.Color;
import static com.aspose.psd.ColorAdjustType.Pen;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```  
These imports expose the `PsdImage`, `Graphics`, `Pen`, and colour classes needed for arc drawing.

### Step 3: initialise image and graphics objects
Create an instance of `PsdImage` and obtain a `Graphics` object to draw on:
```java
String dataDir = "Your Document Directory";
// Initialize PsdImage object
PsdImage image = new PsdImage(100, 100);
// Initialize Graphics object and clear surface
Graphics graphics = new Graphics(image);
graphics.clear(Color.getYellow());
```  
Replace `"Your Document Directory"` with the folder where you want the output files saved.

### Step 4: define arc parameters
Set the geometry and style of the arc—its bounding rectangle, start angle, sweep angle, colour, and thickness:
```java
int width = 100;
int height = 200;
int startAngle = 45;
int sweepAngle = 270;
```  
Adjust the values to match the visual design you need; for example, a 200 px radius arc starting at 45° and sweeping 270°.

### Step 5: draw the arc and save the image
Invoke `drawArc` on the `Graphics` object and persist the PSD (or export to another format):
The `drawArc` method of the `Graphics` class renders an arc defined by a bounding rectangle, start angle, and sweep angle using the specified `Pen`.
```java
// Draw arc with specified Pen object (black color) and parameters
graphics.drawArc(new Pen(Color.getBlack()), 0, 0, width, height, startAngle, sweepAngle);
// Save the image in BMP format
String outputPath = dataDir + "Arc.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```  
The snippet draws the arc on the canvas and saves it as a BMP file. Change the file extension in `outputPath` to export to PNG, JPEG, or TIFF.

## Common pitfalls and troubleshooting
- **Incorrect angle units** – Aspose.PSD expects angles in degrees, not radians. Supplying radians will produce unexpected results.
- **Pen thickness too large** – Very thick pens may cause the arc to exceed the image bounds; reduce the thickness or enlarge the canvas.
- **File path issues** – Use absolute paths or ensure the working directory has write permissions to avoid `IOException`.

## Frequently asked questions

**Q: Can Aspose.PSD for Java handle other shapes besides arcs?**  
A: Yes, the library can draw rectangles, ellipses, lines, polygons, and custom paths using the same `Graphics` API.

**Q: How do I change the arc colour and thickness?**  
A: Create a `Pen` with the desired `Color` and width, then pass that `Pen` instance to `drawArc`.

**Q: Is it possible to export the PSD to a format other than BMP?**  
A: Absolutely. Aspose.PSD supports PNG, JPEG, TIFF, GIF and many more – just change the file extension in the `save` method.

**Q: Where can I find more examples and community support?**  
A: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for tutorials, code samples, and assistance from other developers.

**Q: Does the library work with large PSD files?**  
A: Yes, it can process files up to 2 GB and render arcs without loading the entire document into memory, thanks to its streaming architecture.

---

**Last Updated:** 2026-09-03  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## Related Tutorials

- [Draw and Save a Rectangle in a PSD using Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [Resize Image with Aspose.PSD for Java – Draw Shapes & Basic Image Operations](/psd/java/basic-image-operations/)
- [How to Change Stroke Color Java Using Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}