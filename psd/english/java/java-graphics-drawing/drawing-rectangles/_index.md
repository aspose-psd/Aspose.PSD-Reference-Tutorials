---
title: "Create Image Java – Drawing Rectangles with Aspose.PSD"
linktitle: "Create Image Java – Drawing Rectangles with Aspose.PSD"
second_title: "Aspose.PSD Java API"
description: "Learn how to create image java and draw rectangles on images using Aspose.PSD for Java. This step‑by‑step java image manipulation tutorial helps you draw shapes on image java efficiently."
weight: 17
url: /java/java-graphics-drawing/drawing-rectangles/
date: 2026-01-19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Create Image Java – Drawing Rectangles

## Introduction
If you need to **create image java** programmatically and add graphic elements such as rectangles, you’ve come to the right place. In many Java applications—reports, thumbnails, UI previews, or automated design pipelines—drawing shapes on an image is a routine requirement. Aspose.PSD for Java gives you a clean, high‑performance API to handle this task without dealing with low‑level pixel manipulation. In this tutorial we’ll walk through a complete, hands‑on example that shows you how to draw rectangles on a newly created image, step by step.

## Quick Answers
- **What does “create image java” mean?** It refers to generating a raster image (e.g., BMP, PNG) from Java code using an imaging library.  
- **Which library is best for drawing shapes?** Aspose.PSD for Java provides robust drawing primitives like `Graphics`, `Pen`, and `SolidBrush`.  
- **How many lines of code are needed?** About 30 lines, including imports, image setup, drawing, and saving.  
- **Can I change the output format?** Yes—swap `BmpOptions` for `PngOptions`, `JpegOptions`, etc.  
- **Do I need a license for production?** A commercial license is required for non‑evaluation use.

## What is **create image java**?
Creating an image in Java means instantiating an in‑memory bitmap (or PSD) object, drawing on its canvas with graphics primitives, and then persisting it to a file format of your choice. The Aspose.PSD API abstracts the low‑level details, letting you focus on the visual logic.

## Why use Aspose.PSD for Java to **draw shapes on image java**?
- **Full‑featured drawing API:** Supports rectangles, ellipses, lines, polygons, and custom paths.  
- **Cross‑format support:** Write BMP, PNG, JPEG, TIFF, GIF, and PSD without extra converters.  
- **Performance‑optimized:** Handles large images efficiently, ideal for batch processing.  
- **Simple licensing model:** Free trial for evaluation, straightforward commercial licensing.

## Prerequisites
Before you start, make sure you have:

- **Java Development Kit (JDK) 8+** installed and configured in your IDE or build tool.  
- **Aspose.PSD for Java** library. Download it from the [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) and add the JAR to your project’s classpath.  

## Import Packages
To work with graphics, import the following Aspose.PSD classes:

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

These imports give you access to color definitions, drawing primitives, and image‑saving options.

## Step 1: Create a New Image
First, set up a file path and configure the BMP output options. Then instantiate a `PsdImage` with the desired dimensions (100 × 100 px in this example).

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```

> **Pro tip:** Adjust the width and height to match the resolution you need for your specific use case.

## Step 2: Initialize Graphics Object
Create a `Graphics` object from the image. This object is the canvas on which you’ll draw.

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```

## Step 3: Clear Graphics Surface
Give the image a background color. Here we clear it to yellow, but any `Color` works.

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```

## Step 4: Draw Rectangles
Now draw two rectangles—one red, one blue—using `Pen` and `SolidBrush`. This demonstrates the **draw rectangle java** capability.

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```

You can experiment with different `Pen` widths, dash styles, or even fill the rectangle with a `SolidBrush`.

## Step 5: Export Image
Finally, save the modified image to disk. The `saveOptions` we prepared earlier ensure the output is a 32‑bit BMP.

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```

After running the code, you’ll find `Rectangle.bmp` in your data directory, showing a yellow canvas with a red and a blue rectangle.

## Common Issues and Tips
| Issue | Cause | Fix |
|-------|-------|-----|
| **Image appears blank** | `graphic.clear` not called before drawing | Ensure you clear or fill the background before drawing shapes. |
| **Rectangle size looks wrong** | Incorrect `Rectangle` parameters (x, y, width, height) | Double‑check the order of arguments; the third and fourth values are width and height, not x2/y2. |
| **File not saved** | Invalid output path or missing write permissions | Verify `outpath` points to an existing folder and that your application has write access. |
| **Colors look faded** | Using a low‑bit depth option | Use `BmpOptions.setBitsPerPixel(32)` or switch to PNG for lossless colors. |

## FAQ's
### Can Aspose.PSD for Java handle other shapes besides rectangles?
Aspose.PSD for Java supports drawing various shapes such as ellipses, lines, and polygons in addition to rectangles.

### How can I modify the thickness of the rectangle border?
You can adjust the thickness of the rectangle border by setting the `Pen` thickness property, e.g., `new Pen(Color.RED, 3)`.

### Is Aspose.PSD for Java suitable for high‑performance image processing tasks?
Yes, Aspose.PSD for Java is designed for high‑performance image processing with extensive features for both simple and complex operations.

### Where can I find more examples and tutorials for Aspose.PSD for Java?
You can explore more examples and detailed documentation on the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).

### Does Aspose.PSD for Java support other image formats besides BMP?
Yes, Aspose.PSD for Java supports a wide range of image formats including PNG, JPEG, TIFF, and GIF.

## Conclusion
By following this **create image java** guide, you now know how to set up an image canvas, clear it, draw rectangles, and export the result using Aspose.PSD for Java. Feel free to experiment with other drawing primitives, colors, and output formats to fit your project's needs. Happy coding!

---

**Last Updated:** 2026-01-19  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}