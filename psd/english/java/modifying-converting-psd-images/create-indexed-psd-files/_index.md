---
title: How to Create PSD Files Using Aspose.PSD for Java
linktitle: Create Indexed PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
description: Learn how to create PSD files, generate PSD color palette and set PSD color mode using Aspose.PSD for Java in this step‑by‑step guide.
weight: 23
url: /java/modifying-converting-psd-images/create-indexed-psd-files/
date: 2026-03-15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to Create PSD Files Using Aspose.PSD for Java

## Introduction
If you’ve ever wondered **how to create PSD** files programmatically, you’re in the right place. Aspose.PSD for Java gives you full control over Photoshop documents, letting you generate, edit, and save PSD files without ever opening Photoshop. In this tutorial we’ll walk through creating an **indexed PSD** file, setting the PSD color mode, and generating a custom color palette—all with clear, step‑by‑step Java code. Whether you’re building a graphics pipeline, automating asset creation, or just experimenting, the concepts here will help you bring your visual ideas to life.

## Quick Answers
- **What library do I need?** Aspose.PSD for Java
- **Can I create an indexed PSD?** Yes, by setting the color mode to `Indexed`
- **Do I need Photoshop installed?** No, Aspose.PSD works independently
- **Which Java version is required?** JDK 8 or later
- **How large can the canvas be?** Any size; this example uses 500 × 500 px

## What is an Indexed PSD File?
An indexed PSD stores colors in a palette rather than full‑color values for each pixel. This reduces file size and is ideal for graphics with limited colors, such as icons or UI assets. By generating a custom palette you control exactly which colors appear in the final image.

## Why Generate a PSD Color Palette?
Creating a **PSD color palette** lets you:
- Keep file sizes small for web or mobile use  
- Ensure consistent branding by limiting colors to your corporate palette  
- Speed up rendering in applications that support indexed images  

## Prerequisites
Before we dive into the code, make sure you have the following:

1. **Basic Knowledge of Java** – you should be comfortable with classes, methods, and object creation.  
2. **Java Development Kit (JDK) 8+** – installed and configured in your IDE.  
3. **IDE (IntelliJ IDEA, Eclipse, etc.)** – optional but highly recommended for easier debugging.  
4. **Aspose.PSD for Java Library** – download it **[here](https://releases.aspose.com/psd/java/)** and add the JAR to your project’s classpath.  
5. **Fundamental Graphic Design Concepts** – understanding of color modes, palettes, and basic shapes will help you follow along.

## Import Packages
Before we proceed with the code, let’s make sure we have all the necessary packages imported into your Java application. Here’s what you’ll need:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdColorPalette;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

These imports will allow you to work with PSD options, colors, and graphics manipulation through Aspose.PSD.

Now, let’s break down the code step‑by‑step to **how to create PSD** files with an indexed color mode.

## Step 1: Set Up Your Document Directory
First, define where the generated PSD will be saved.

```java
String dataDir = "Your Document Directory";
```

Replace `"Your Document Directory"` with an absolute or relative path, e.g., `"/Users/YourName/Documents/"`.

## Step 2: Create an Instance of PsdOptions
`PsdOptions` holds all the settings for the file you are about to generate.

```java
PsdOptions createOptions = new PsdOptions();
```

## Step 3: Set Core Properties of PsdOptions
Here we specify the output location, the **set psd color mode** to `Indexed`, and the PSD version.

```java
createOptions.setSource(new FileCreateSource(dataDir + "Newsample_out.psd", false));
createOptions.setColorMode(ColorModes.Indexed);
createOptions.setVersion(5);
```

- **Source** – the full path of the new file.  
- **Color Mode** – `Indexed` tells Aspose.PSD to use a palette‑based image.  
- **Version** – PSD format version (5 works for most modern Photoshop versions).

## Step 4: Create a Color Palette (Generate PSD Color Palette)
Define the colors that will be available in the indexed image.

```java
Color[] palette = { Color.getRed(), Color.getGreen(), Color.getBlue(), Color.getYellow() };
createOptions.setPalette(new PsdColorPalette(palette));
createOptions.setCompressionMethod(CompressionMethod.RLE);
```

- The `palette` array holds up to 256 `Color` objects.  
- `CompressionMethod.RLE` provides efficient lossless compression for indexed images.

## Step 5: Create the PSD Image Canvas
Now we create a blank PSD with the dimensions we want.

```java
Image psd = Image.create(createOptions, 500, 500);
```

This creates a 500 × 500 pixel canvas that uses the palette defined earlier.

## Step 6: Draw Graphics on the PSD
Add visual content—here we draw a simple red ellipse on a white background.

```java
Graphics graphics = new Graphics(psd);
graphics.clear(Color.getWhite());
graphics.drawEllipse(new Pen(Color.getRed(), 6), new Rectangle(0, 0, 400, 400));
```

- `clear(Color.getWhite())` fills the background with white.  
- `drawEllipse` renders a red ellipse with a 6‑pixel stroke.

## Step 7: Save the PSD File
Finally, persist the image to disk.

```java
psd.save();
```

The file `Newsample_out.psd` will appear in the directory you specified earlier.

## Common Issues & Tips
- **Palette Size** – If you need more than 4 colors, simply add them to the `palette` array (up to 256).  
- **File Permissions** – Ensure the Java process has write access to `dataDir`.  
- **Incorrect Color Mode** – Forgetting `createOptions.setColorMode(ColorModes.Indexed)` will produce an RGB PSD instead of an indexed one.  

## Frequently Asked Questions

**Q: What is Aspose.PSD for Java?**  
A: Aspose.PSD for Java is a library that enables manipulation of PSD (Photoshop) files programmatically using Java.

**Q: Can I use Aspose.PSD for free?**  
A: Yes, you can access a free trial version of Aspose.PSD **[here](https://releases.aspose.com/)**.

**Q: Do I need to have Photoshop installed to work with Aspose.PSD?**  
A: No, you can create and manipulate PSD files without Photoshop, as Aspose.PSD handles all operations independently.

**Q: How do I obtain a temporary license for Aspose.PSD?**  
A: You can request a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.

**Q: Where can I get support for Aspose.PSD?**  
A: You can get support from the Aspose forum **[here](https://forum.aspose.com/c/psd/34)**.

## Conclusion
You’ve just learned **how to create PSD** files with an indexed color mode, generated a custom palette, and added simple graphics—all using Aspose.PSD for Java. With these building blocks you can expand to more complex drawings, layer management, and batch processing. For deeper exploration, check out the official API reference **[here](https://reference.aspose.com/psd/java/)** and keep experimenting with different palettes and drawing primitives.

---

**Last Updated:** 2026-03-15  
**Tested With:** Aspose.PSD for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}