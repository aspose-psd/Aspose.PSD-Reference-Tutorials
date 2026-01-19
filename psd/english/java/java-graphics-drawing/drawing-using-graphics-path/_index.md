---
title: "Create PSD Image Java – Drawing Using Graphics Path"
linktitle: Drawing Using Graphics Path in Java
second_title: Aspose.PSD Java API
description: "Learn how to create psd image java with Aspose.PSD and add text psd image using the Graphics Path class. Step‑by‑step guide for stunning results."
weight: 19
url: /java/java-graphics-drawing/drawing-using-graphics-path/
date: 2026-01-19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Create PSD Image Java – Drawing Using Graphics Path

## Introduction
In this tutorial, you'll learn how to **create PSD image java** using the powerful **Graphics Path** class provided by Aspose.PSD. We'll walk through each step—from setting up the environment to drawing shapes, adding text, and saving the final PSD file—so you can quickly start generating custom PSD images directly from Java code.

## Quick Answers
- **What can I create?** You can create a full‑featured PSD image programmatically.  
- **Which library is required?** Aspose.PSD for Java.  
- **Do I need a license?** A free trial works for evaluation; a commercial license is required for production.  
- **Can I add text?** Yes—use the `TextShape` class to **add text psd image** content.  
- **How long does it take?** With the steps below, you can have a PSD file ready in under 10 minutes.

## What is create psd image java?
Creating a PSD image in Java means generating a Photoshop‑compatible file (PSD) from scratch or by modifying existing layers. Aspose.PSD abstracts the low‑level PSD format details, letting you focus on drawing shapes, applying brushes, and inserting text—all through a clean, object‑oriented API.

## Why use Graphics Path to add text psd image?
The `GraphicsPath` class lets you combine multiple drawing primitives—such as ellipses, rectangles, and text—into a single path. This approach simplifies rendering, improves performance, and gives you fine‑grained control over fill styles and strokes. It’s especially handy when you need to **add text psd image** elements together with other graphics in one cohesive operation.

## Prerequisites
Before we jump into the coding part, ensure you have the following prerequisites:
1. Java Development Kit (JDK): A stable version of JDK installed on your machine. You can download it from [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. Aspose.PSD for Java Library: Download the Aspose.PSD for Java library from [here](https://releases.aspose.com/psd/java/). After downloading, add the JAR file to your project's classpath.  
3. Integrated Development Environment (IDE): Whether it’s Eclipse, IntelliJ IDEA, or any other, you need an IDE to write and run Java code.

With these prerequisites in place, let’s explore how to create visually engaging images using the Graphics Path class.

## Import Packages
To get started, you need to import the necessary packages:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Figure;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.GraphicsPath;
import com.aspose.psd.HatchStyle;
import com.aspose.psd.Pen;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.HatchBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.shapes.EllipseShape;
import com.aspose.psd.shapes.RectangleShape;
import com.aspose.psd.shapes.TextShape;
```

These imports provide access to the core functionality needed to create and manipulate PSD images using Aspose.PSD.

## Step 1: Initialize Image and Graphics
First, create a new PSD image and set up a graphics object that will be used for drawing:

```java
PsdImage image = new PsdImage(500, 500);
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
```

Here, we generate a 500 × 500 pixel canvas and clear it with a white background, preparing a clean drawing surface.

## Step 2: Create and Configure Graphics Path
Next, build a `GraphicsPath` that contains the shapes and text you want to render:

```java
GraphicsPath graphicspath = new GraphicsPath();
Figure figure = new Figure();
figure.addShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new TextShape("Aspose.PSD", new RectangleF(170, 225, 170, 100), new TextFont("Arial", 20), StringFormat.getGenericTypographic()));
Figure[] fig = { figure };
graphicspath.addFigures(fig);
```

In this step we add a circle, a rectangle, **and a text label** (“Aspose.PSD”)—demonstrating how to **add text psd image** content inside the same graphics path.

## Step 3: Draw and Fill Path
Now draw the outline of the path and fill it with a hatch brush:

```java
graphics.drawPath(new Pen(Color.getBlue()), graphicspath);
HatchBrush hatchbrush = new HatchBrush();
hatchbrush.setBackgroundColor(Color.getBrown());
hatchbrush.setForegroundColor(Color.getBlue());
hatchbrush.setHatchStyle(HatchStyle.Vertical);
graphics.fillPath(hatchbrush, graphicspath);
```

The blue pen renders the shapes’ borders, while the vertical hatch brush adds a textured fill.

## Step 4: Save the Image
Finally, write the PSD file to disk:

```java
String dataDir = "Your Document Directory";
image.save(dataDir + "DrawingUsingGraphicsPath_output.psd");
```

After this step, you’ll have a fully‑featured PSD file that includes vector shapes and embedded text.

## Conclusion
By following these steps, you now know how to **create PSD image java** projects that combine geometric shapes and text using Aspose.PSD’s `GraphicsPath`. This technique opens the door to automated graphic generation, custom watermarking, and dynamic design workflows directly from Java code.

## FAQ's
### What is Aspose.PSD?
Aspose.PSD is a library that allows developers to work with Photoshop files and manipulate image layers programmatically.

### Can I use Aspose.PSD for formats other than PSD?
As of this guide, Aspose.PSD specifically deals with PSD files but offers extensions to handle different image formats.

### Is a trial version available for Aspose.PSD?
Yes, you can access a free trial of Aspose.PSD [here](https://releases.aspose.com/).

### How can I purchase Aspose.PSD?
You can purchase Aspose.PSD from [here](https://purchase.aspose.com/buy).

### Where can I get support for Aspose.PSD?
You can seek support and discussions on [Aspose’s forum](https://forum.aspose.com/c/psd/34).

---

**Last Updated:** 2026-01-19  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}