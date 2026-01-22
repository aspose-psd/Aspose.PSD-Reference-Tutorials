---
title: "Create PSD Image Java – Drawing Using Graphics with Aspose.PSD"
linktitle: Drawing Using Graphics in Java
second_title: Aspose.PSD Java API
description: Learn how to create PSD image Java using Aspose.PSD, draw graphics, fill polygon, and export PSD to BMP. A complete java image manipulation tutorial.
weight: 18
url: /java/java-graphics-drawing/drawing-using-graphics/
date: 2026-01-22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Drawing Using Graphics in Java

## Introduction
In this **java image manipulation tutorial** we’ll show you how to **create PSD image java** programmatically with Aspose.PSD. Whether you need to generate graphics on the fly, fill polygons, or export your work to BMP, this guide walks you through every step—from setting up the environment to saving the final file.

## Quick Answers
- **What library lets me create PSD images in Java?** Aspose.PSD for Java.
- **Can I draw shapes and fill polygons?** Yes, using the Graphics and Brush classes.
- **How do I export a PSD to BMP?** Call `image.save(..., new BmpOptions())`.
- **Do I need a license for development?** A free temporary license is available for evaluation.
- **What Java version is required?** JDK 8 or higher.

## Prerequisites
Before diving into this tutorial, ensure you have the following prerequisites:
- Basic knowledge of Java programming.
- Java Development Kit (JDK) installed on your system.
- Integrated Development Environment (IDE) such as IntelliJ IDEA or Eclipse.
- Aspose.PSD for Java library. You can download it from [here](https://releases.aspose.com/psd/java/).

## How to draw graphics Java with Aspose.PSD
To begin, import the necessary packages from Aspose.PSD for Java and other standard Java libraries:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Point;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.LinearGradientBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Step 1: Create an Image Object
First, instantiate a `PsdImage` object with specific dimensions:

```java
String dataDir = "Your Document Directory";
PsdImage image = new PsdImage(500, 500);
```

## Step 2: Initialize Graphics Object
Next, initialize a `Graphics` object using the `PsdImage`:

```java
Graphics graphics = new Graphics(image);
```

## Step 3: Clear the Image Surface
Clear the image surface with a specified color (white in this example):

```java
graphics.clear(Color.getWhite());
```

## Step 4: Create and Configure Pen Object
Create a `Pen` object to define the stroke properties (color, thickness, etc.):

```java
Pen pen = new Pen(Color.getBlue());
```

## Step 5: Draw Shapes – How to draw graphics Java
Draw an ellipse on the image using the `Pen` object and a bounding rectangle:

```java
graphics.drawEllipse(pen, new Rectangle(10, 10, 150, 100));
```

## Fill Polygon Java Graphics
Define and use a `LinearGradientBrush` to fill a polygon with a gradient:

```java
LinearGradientBrush linearGradientBrush = new LinearGradientBrush(image.getBounds(), Color.getRed(), Color.getWhite(), 45f);
Point[] points = { new Point(200, 200), new Point(400, 200), new Point(250, 350) };
graphics.fillPolygon(linearGradientBrush, points);
```

## Export PSD to BMP
Finally, save the modified image to a specified location and format (BMP in this example):

```java
image.save(dataDir + "DrawingUsingGraphics_output.bmp", new BmpOptions());
```

## Conclusion
By following this **java image manipulation tutorial**, you now know how to **create PSD image java**, draw shapes, apply gradients, fill polygons, and **export PSD to BMP** using Aspose.PSD. Experiment with different brushes, colors, and geometries to enrich your Java applications with powerful graphics capabilities.

## Frequently Asked Questions

**Q: Can Aspose.PSD handle complex image manipulations?**  
A: Yes, Aspose.PSD supports a wide range of operations including layer manipulation, color adjustments, and text rendering.

**Q: Is Aspose.PSD suitable for high‑performance applications?**  
A: Absolutely, Aspose.PSD is optimized for performance and memory efficiency.

**Q: Where can I find more examples and documentation?**  
A: Visit the [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/) for comprehensive guides and API references.

**Q: Does Aspose.PSD support multiple image formats for export?**  
A: Yes, Aspose.PSD can export to BMP, PNG, JPEG, TIFF, and other popular formats.

**Q: How can I get support or assistance if I encounter issues?**  
A: Reach out to the Aspose.PSD community on the [support forum](https://forum.aspose.com/c/psd/34) or consider a [temporary license](https://purchase.aspose.com/temporary-license/) for priority support.

---

**Last Updated:** 2026-01-22  
**Tested With:** Aspose.PSD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}