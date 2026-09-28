---
date: 2026-09-28
description: Learn how to draw ellipse in Java using Aspose.PSD, the leading Java
  image processing tutorial for creating ellipses and other shapes.
images:
- /java/java-graphics-drawing/drawing-ellipses/og-image.png
keywords:
- how to draw ellipse
- draw shapes java
- java image processing tutorial
- create ellipse image
- draw ellipses java
lastmod: 2026-09-28
linktitle: Drawing Ellipses in Java
og_description: Learn how to draw ellipse in Java using Aspose.PSD, the top Java image
  processing tutorial that lets you create ellipses, draw shapes, and generate bitmap
  images efficiently.
og_image_alt: Guide showing how to draw an ellipse in Java with Aspose.PSD
og_title: How to draw ellipse in Java using Aspose.PSD library
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to draw ellipse in Java using Aspose.PSD, the leading Java
    image processing tutorial for creating ellipses and other shapes.
  headline: How to draw ellipse in Java using Aspose.PSD library
  type: TechArticle
- questions:
  - answer: Aspose.PSD offers a fully functional trial that lets you evaluate all
      features before purchasing a license.
    question: Can I use Aspose.PSD for free?
  - answer: Visit [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides, API references, and sample projects.
    question: Where can I find more examples and documentation?
  - answer: Temporary licenses are available through the Aspose portal at [Aspose.PSD
      Temporary License](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  - answer: It supports BMP, PNG, JPEG, TIFF, GIF, and native PSD among others.
    question: What image formats can Aspose.PSD export to?
  - answer: Yes, the library is designed for high‑throughput server environments and
      includes features such as multi‑threaded processing and memory‑efficient streaming.
    question: Is Aspose.PSD suitable for enterprise‑level workloads?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- draw ellipse
- Aspose.PSD
- Java graphics
- image processing
title: How to draw ellipse in Java using Aspose.PSD library
url: /java/java-graphics-drawing/drawing-ellipses/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to draw ellipse in Java using Aspose.PSD library

## Introduction
In this tutorial you’ll learn **how to draw ellipse** in Java with the Aspose.PSD library. Aspose.PSD for Java is a robust API that lets you create, edit, and export PSD files without needing Adobe Photoshop. Drawing shapes such as ellipses is a core skill for any Java image‑processing project, and this guide walks you through every step—from project setup to saving the final bitmap.

## Quick answers
- **Which library is best for drawing ellipses in Java?** Aspose.PSD for Java.
- **How many lines of code are needed?** About ten lines plus a few setup statements.
- **Do I need a license for development?** A free trial works for testing; a commercial license is required for production.
- **Can I output to BMP, PNG, or JPEG?** Yes, Aspose.PSD supports BMP, PNG, JPEG, and PSD.
- **Is the API compatible with Java 8 and newer?** Fully supported on Java 8‑21.

## What is Aspose.PSD for Java?
Aspose.PSD for Java is a pure‑Java library that enables programmatic creation, manipulation, and conversion of Photoshop PSD files. It supports over 100 image formats and can handle files up to 2 GB without loading the entire document into memory.

## Why use Aspose.PSD for ellipse drawing?
Aspose.PSD delivers high performance, processing multi‑page documents in seconds, while supporting over 100 input and output formats such as BMP, PNG, JPEG and PSD. It operates entirely in Java, eliminating the need for native Photoshop and making it ideal for CI/CD pipelines and cloud‑based services.

## Prerequisites
Before you begin, make sure you have:
- Basic Java programming knowledge.
- JDK 8 or newer installed.
- An IDE such as IntelliJ IDEA or Eclipse.
- Aspose.PSD for Java library. You can download it from the [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).

## Import packages
First, import the classes you’ll need from the Aspose.PSD namespace.

## How to draw an ellipse in Java?
Load the Aspose.PSD library, create a blank PsdImage canvas, obtain a Graphics object, optionally clear the background, then use Pen objects with desired colours and styles to draw ellipses inside Rectangle bounds. Finally, save the image in BMP, PNG, or JPEG format. This process typically requires fewer than 15 lines of code.

## Step 1: set up your Java project
Before you start coding, ensure your project includes the Aspose.PSD JAR as a Maven/Gradle dependency or adds the JAR to the classpath.

## Step 2: create an instance of PsdImage
PsdImage represents an in‑memory Photoshop document and provides a canvas for drawing.

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

## Step 3: initialize graphics object
Graphics provides drawing methods to render shapes onto an image surface.

```java
Image image = new PsdImage(100, 100);
```

## Step 4: clear the graphics surface
Optionally clear the canvas with a background colour to ensure a clean drawing area.

```java
Graphics graphics = new Graphics(image);
```

## Step 5: draw a dotted ellipse
Pen defines the colour and style of the outline used when drawing shapes.

```java
graphics.clear(Color.getYellow());
```

## Step 6: draw a continuous ellipse
Pen with a solid‑blue brush creates a continuous outline for the second ellipse.

```java
graphics.drawEllipse(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
```

## Step 7: save the image
BmpOptions specifies BMP format settings for saving the image.

```java
graphics.drawEllipse(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
```

```java
String outputPath = "Your Document Directory/Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```



## Common issues and solutions
- **Image appears blank:** Ensure you called `graphics.clear()` with a visible colour before drawing.
- **Ellipse looks distorted:** Verify that the `Rectangle` dimensions match the image’s aspect ratio.
- **Out‑of‑memory errors on large files:** Use `PsdImage`’s streaming API to process sections of the file instead of loading the whole document.

## Frequently asked questions

**Q: Can I use Aspose.PSD for free?**  
A: Aspose.PSD offers a fully functional trial that lets you evaluate all features before purchasing a license.

**Q: Where can I find more examples and documentation?**  
A: Visit [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/) for comprehensive guides, API references, and sample projects.

**Q: How do I obtain a temporary license for testing?**  
A: Temporary licenses are available through the Aspose portal at [Aspose.PSD Temporary License](https://purchase.aspose.com/temporary-license/).

**Q: What image formats can Aspose.PSD export to?**  
A: It supports BMP, PNG, JPEG, TIFF, GIF, and native PSD among others.

**Q: Is Aspose.PSD suitable for enterprise‑level workloads?**  
A: Yes, the library is designed for high‑throughput server environments and includes features such as multi‑threaded processing and memory‑efficient streaming.

## Conclusion
You now have a complete, end‑to‑end example of **how to draw ellipse** in Java using Aspose.PSD. By setting up a `PsdImage`, using the `Graphics` API, and configuring `Pen` objects, you can render both dotted and solid ellipses and save the result in any of the supported bitmap formats. Integrate these steps into your own applications to generate dynamic graphics, thumbnails, or custom UI elements without relying on external graphics editors.

---

**Last Updated:** 2026-09-28  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose

## Related Tutorials

- [Draw and Save a Rectangle in a PSD using Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [Resize Image with Aspose.PSD for Java – Draw Shapes & Basic Image Operations](/psd/java/basic-image-operations/)
- [Add Signature to Image – Draw Image on Canvas with Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}