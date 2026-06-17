---
title: Create Graphics Object Java – Diagonal Watermark for PSD
linktitle: Add Diagonal Watermark to PSD Files with Java
second_title: Aspose.PSD Java API
description: Learn how to create graphics object java and add a diagonal watermark to PSD files using Aspose.PSD. This step‑by‑step guide covers java image watermark library usage.
weight: 12
url: /java/modifying-converting-psd-images/add-diagonal-watermark-psd-files/
date: 2026-03-04
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Add Diagonal Watermark to PSD Files with Java

## Introduction
In this tutorial you’ll **create graphics object java** and use it to add a diagonal watermark to PSD files. Whether you’re a designer protecting your artwork or a marketer branding images, a clean watermark can make your work look professional and secure. We’ll walk through each step with clear explanations, so you can quickly apply the technique in your own projects.

## Quick Answers
- **What library do I need?** Aspose.PSD for Java (a robust java image watermark library).  
- **Which primary keyword does this tutorial cover?** create graphics object java.  
- **Do I need a license?** A free trial works for testing; a commercial license is required for production.  
- **Can I change the watermark text and style?** Yes – you can customize font, color, opacity, and rotation.  
- **What output formats are supported?** The example saves as PNG, but Aspose.PSD can export to PSD, JPEG, BMP, and more.

## What is a Graphics Object in Java?
A **Graphics** object represents a drawing surface for an image. By creating a graphics object, you gain access to methods that let you render text, shapes, and other visual elements directly onto the bitmap or PSD canvas. This is the core concept behind the primary keyword **create graphics object java**.

## Why Use Aspose.PSD for Watermarking?
Aspose.PSD is a dedicated **java image watermark library** that works without Adobe Photoshop. It gives you full control over layers, text rendering, and image transformations, making it ideal for server‑side processing or batch operations.

## Prerequisites
Before we dive into the code, make sure you have the following:

### 1. Java Development Environment
Install the latest JDK from the [Java website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### 2. Aspose.PSD Library
Download the library from the [Aspose Downloads page](https://releases.aspose.com/psd/java/). Add the JAR to your project via Maven, Gradle, or manual classpath inclusion.

### 3. Basic Understanding of Java
Familiarity with classes, objects, and file I/O will help you follow along smoothly.

### 4. IDE Setup
Use IntelliJ IDEA, Eclipse, or NetBeans for a comfortable coding experience.

## Import Packages
To manipulate PSD files, import the required Aspose.PSD classes:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Matrix;
import com.aspose.psd.PointF;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

Now that we have our prerequisites sorted and the necessary packages imported, let’s walk through the steps to add a diagonal watermark to a PSD file.

## Step 1: Set Up Your Directory
```java
String dataDir = "Your Document Directory";
```
Replace `"Your Document Directory"` with the folder path that holds your PSD source file.

## Step 2: Load the PSD File
```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```
The `Image.load` method reads the file and casts it to a `PsdImage` so we can work with PSD‑specific features.

## Step 3: Create a Graphics Object
```java
Graphics graphics = new Graphics(psdImage);
```
Here we **create graphics object java**—the canvas on which we’ll draw the watermark.

## Step 4: Create a Font for the Watermark
```java
Font font = new Font("Arial", 20.0f);
```
Pick any installed font; the size controls how prominent the watermark appears.

## Step 5: Create a Brush for the Watermark
```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```
The `alpha` value (first parameter) sets transparency. An alpha of 50 gives a subtle, semi‑transparent look.

## Step 6: Set Up the Transform Matrix
```java
graphics.setTransform(new Matrix());
graphics.getTransform().rotateAt(45, new PointF(psdImage.getWidth() / 2, psdImage.getHeight() / 2));
```
We rotate the drawing surface 45° around the image center, creating the diagonal effect.

## Step 7: Define String Alignment
```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
```
Center alignment ensures the watermark sits nicely in the middle of the rotated rectangle.

## Step 8: Draw the Watermark
```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, psdImage.getHeight() / 2, psdImage.getWidth(), psdImage.getHeight() / 2), sf);
```
Replace `"Some watermark text"` with your brand name or copyright notice. The rectangle defines where the text is rendered.

## Step 9: Save the Image
```java
psdImage.save(dataDir + "AddDiagnolWatermark_output.png", new PngOptions());
```
The output is saved as PNG, but you can choose any format supported by Aspose.PSD.

## Common Use Cases
- **Brand protection:** Add a semi‑transparent logo to prevent unauthorized reuse.  
- **Batch processing:** Automate watermarking for large image libraries on a server.  
- **Creative previews:** Show watermarked drafts to clients while keeping the original files untouched.

## Troubleshooting & Tips
- **Transparency not visible?** Increase the alpha value (e.g., `100`) for a stronger watermark.  
- **Watermark appears off‑center?** Verify the rotation point uses the image’s exact width/height division.  
- **Performance concerns:** Reuse the same `Graphics` object when processing multiple images in a loop.

## FAQ's
### What is Aspose.PSD?
Aspose.PSD is a Java library used for working with and manipulating PSD files without requiring Adobe Photoshop.

### Can I use other fonts for watermarking?
Yes, you can choose any font that is installed on your system for watermarking.

### Is there a way to customize the watermark's transparency?
Absolutely! You can adjust the alpha value in the SolidBrush to change the transparency.

### Can I add multiple watermarks?
Yes, you can call the `drawString` method multiple times with different parameters to add more watermarks.

### Where can I find more information about Aspose.PSD?
You can check the documentation [here](https://reference.aspose.com/psd/java/).

---

**Last Updated:** 2026-03-04  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}