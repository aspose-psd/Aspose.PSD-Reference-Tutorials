---
date: 2026-09-28
description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
  grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
images:
- /java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/og-image.png
keywords:
- export psd as png
- how to convert psd to png
- 16-bit grayscale java
lastmod: 2026-09-28
linktitle: Export PSD as PNG – 16-bit Grayscale – Java
og_description: Export PSD as PNG with 16‑bit grayscale using Aspose.PSD for Java.
  Follow this step‑by‑step tutorial to preserve 65,536 gray shades.
og_image_alt: Guide showing how to export PSD as PNG with 16-bit grayscale using Aspose.PSD
  Java
og_title: Export PSD as PNG with 16‑bit grayscale in Java – Aspose.PSD Guide
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  headline: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  type: TechArticle
- description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  name: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
    text: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
  - name: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
    text: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
  - name: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
    text: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
  type: HowTo
- questions:
  - answer: It provides 65 536 shades of gray, delivering far more tonal detail than
      the standard 8‑bit (256 shades).
    question: What is 16‑bit grayscale color mode?
  - answer: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other
      color modes.
    question: Can I use Aspose.PSD for non‑grayscale images?
  - answer: Yes, you can try a free trial version of Aspose.PSD. Just head to the
      [Aspose download page](https://releases.aspose.com/).
    question: Is there a trial version of Aspose.PSD?
  - answer: Check the official [documentation](https://reference.aspose.com/psd/java/)
      for in‑depth tutorials, API references, and sample projects.
    question: Where can I find more Aspose.PSD examples?
  - answer: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
title: How to export PSD as PNG with 16‑bit grayscale color mode in Java
url: /java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export PSD as PNG with 16‑bit grayscale color mode in Java

## Introduction
Exporting PSD as PNG while keeping a 16‑bit grayscale color mode gives you the depth of a professional photograph and the universal compatibility of PNG. In this guide you’ll learn how to **set the PSD color mode to 16‑bit grayscale** and then **export the PSD as PNG** using Aspose.PSD for Java. The tutorial covers everything from prerequisites to troubleshooting, so you can integrate the workflow into any Java‑based image pipeline.

## Quick answers
- **What does “export PSD as PNG” involve?** Load a PSD, optionally change its color mode, and save it as a PNG file.  
- **Which Aspose class handles the conversion?** `PsdImage` loads the PSD and `PngOptions` defines PNG output settings.  
- **Do I need a license for production?** Yes – a trial works for testing, but a paid license is required for commercial use.  
- **Can the 16‑bit depth be retained in PNG?** Absolutely, by using `PngColorType.GrayscaleWithAlpha`.  
- **Which IDEs are supported?** Any Java IDE – IntelliJ IDEA, Eclipse, VS Code, or NetBeans.

## What is export PSD as PNG?
Export PSD as PNG is the process of converting an Adobe Photoshop document (PSD) into a Portable Network Graphics (PNG) file while preserving the image’s pixel data and color depth. This conversion is commonly used to share high‑quality grayscale assets on the web without losing tonal detail.

## Why export PSD as PNG with 16‑bit grayscale?
Exporting to PNG while keeping 16‑bit grayscale preserves 65 536 shades of gray, which provides far more tonal richness than 8‑bit images. PNG’s universal support ensures the files can be displayed in browsers, mobile apps, and desktop editors without loss, while the lossless compression of Aspose.PSD guarantees no artifacts are introduced.

## Prerequisites
Before we start, make sure you have the following items ready:

1. **Java Development Kit (JDK)** – Install the latest JDK from [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – Download the JAR from the [Aspose download page](https://releases.aspose.com/psd/java/).  
3. **An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.  
4. **Basic Java knowledge** – You should be comfortable creating classes, handling exceptions, and working with file paths.  
5. **A sample PSD file** – Create one in Adobe Photoshop or grab a free sample online.

## How to export PSD as PNG step by step

## How do you set the PSD color mode to 16‑bit grayscale?
PsdImage is the Aspose.PSD class that loads and represents a PSD file in memory.  
ColorMode is an enumeration that defines the color mode of a PSD image.  

Load the PSD with `PsdImage`, change its color mode using the `ColorMode` property, and then save the modified file. This operation runs entirely in memory, eliminating the need for intermediate files and ensuring the conversion is fast and efficient.

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

These imports give you access to the functionalities you’ll use to manipulate PSD files, set the color mode, and export the result as PNG.

## How do you define source and output directories?
`File` is a java.io class that represents a file or directory path on the file system.  

You need to tell the program where to read the original PSD and where to write the converted PNG. Using absolute or relative paths works, but keep them consistent across environments to avoid path resolution errors.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Replace the placeholder strings with the actual paths on your machine.

## How do you encapsulate the conversion logic in a reusable method?
`convertPsdToPng` is a custom method that encapsulates all steps required to convert a PSD file to PNG with optional settings.  

Creating a dedicated method lets you reuse the same conversion steps for multiple files or different settings. Pass parameters such as source path, destination folder, and optional compression level, making the workflow flexible and maintainable.

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

This method lets you **set PSD color mode** and then **export PSD as PNG** in a single flow.

## How do you load the PSD and apply the 16‑bit grayscale mode?
PsdImage is the Aspose.PSD class that loads a PSD file into memory.  
ColorMode.GRAYSCALE_16 is an enumeration value that sets the image to 16‑bit grayscale.  
`channelBitsCount` is a property that specifies the number of bits per channel.  

Inside the conversion method, build the full file paths, instantiate `PsdImage`, and change its `ColorMode` to `ColorMode.GRAYSCALE_16`. The `channelBitsCount` property must be set to 16 to keep the high‑bit depth, ensuring the image retains all tonal information.

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

The `postfix` helps you keep track of the settings used for each exported file.

## How do you draw a subtle border on the image (optional step)?
`Graphics` is a class that provides drawing capabilities on a `PsdImage` canvas.  

You can optionally draw a gray rectangle around the image to make the output more visible during testing. This step demonstrates how to work with layers and graphics objects, and the rectangle is calculated dynamically so it stays centered regardless of image size.

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

The rectangle is calculated dynamically so it stays centered regardless of image size.

## How do you save the modified PSD with the new color mode?
`PsdOptions` is a class that controls how a PSD file is saved, including color mode and bit depth settings.  

After drawing (or skipping that step), call `save` on the `PsdImage` instance, passing a `PsdOptions` object that preserves the 16‑bit grayscale configuration. This ensures the saved PSD retains the desired color mode without any data loss.

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## How do you convert the PSD to PNG while preserving 16‑bit depth?
`PngOptions` is a class that defines PNG output settings such as color type and compression level.  
`PngColorType.GrayscaleWithAlpha` is an enumeration value that stores 16‑bit grayscale data with an alpha channel.  

Load the newly saved PSD, configure `PngOptions` with `PngColorType.GrayscaleWithAlpha`, and call `save`. This retains the 16‑bit grayscale data inside the PNG file, providing a lossless, high‑quality image suitable for further processing or distribution.

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

Now you have successfully **exported PSD as PNG** while keeping the high‑quality 16‑bit grayscale data.

## Common issues and solutions
| Issue | Why it happens | Fix |
|-------|----------------|-----|
| **“Unsupported color type” exception** | Trying to save a PSD with an unsupported channel configuration. | Ensure `channelBitsCount` matches the actual bit depth (16) and `channelsCount` is correct for grayscale (1). |
| **File not found** | Incorrect source directory path. | Double‑check the `sourceDir` string and verify the PSD file exists at that location. |
| **Output PNG appears black** | PNG saved without proper alpha handling. | Use `PngColorType.GrayscaleWithAlpha` as shown above. |
| **Memory overflow on large PSDs** | Loading the entire file into memory. | Enable streaming mode via `PsdImage.load(inputStream, new LoadOptions())` to process large files efficiently. |

## Frequently asked questions

**Q: What is 16‑bit grayscale color mode?**  
A: It provides 65 536 shades of gray, delivering far more tonal detail than the standard 8‑bit (256 shades).

**Q: Can I use Aspose.PSD for non‑grayscale images?**  
A: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other color modes.

**Q: Is there a trial version of Aspose.PSD?**  
A: Yes, you can try a free trial version of Aspose.PSD. Just head to the [Aspose download page](https://releases.aspose.com/).

**Q: Where can I find more Aspose.PSD examples?**  
A: Check the official [documentation](https://reference.aspose.com/psd/java/) for in‑depth tutorials, API references, and sample projects.

**Q: How do I purchase a license for Aspose.PSD?**  
A: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).

---

**Last Updated:** 2026-09-28  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose

## Related Tutorials

- [Convert PSD to PNG with Specified Bit Depth Using Aspose.PSD for Java](/psd/java/optimizing-png-files/specify-png-bit-depth/)
- [Export PSD to PNG with Layer Effects using Aspose.PSD for Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Save PSD as JPEG and Support RGB Color with Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}