---
date: 2026-10-08
description: 'Java image processing tutorial: learn how to manipulate PSD files and
  save them as JPEGs using Aspose.PSD. Step‑by‑step guide with code examples for beginners
  and pros.'
images:
- /java/java-jpeg-image-processing/support-2-7-bits-jpeg-java/og-image.png
keywords:
- java image processing tutorial
- Aspose.PSD
- 2 bit JPEG
- 7 bit JPEG
lastmod: 2026-10-08
linktitle: Support for 2 and 7 Bits JPEG in Java
og_description: 'Java image processing tutorial: learn how to manipulate PSD files
  and save them as JPEGs using Aspose.PSD. Detailed steps, quick answers and troubleshooting
  for developers.'
og_image_alt: Guide to processing 2‑ and 7‑bit JPEG images in Java with Aspose.PSD
og_title: 'Java image processing tutorial: support 2‑ and 7‑bit JPEGs'
schemas:
- author: Aspose
  dateModified: '2026-10-08'
  description: 'Java image processing tutorial: learn how to manipulate PSD files
    and save them as JPEGs using Aspose.PSD. Step‑by‑step guide with code examples
    for beginners and pros.'
  headline: 'Java image processing tutorial: support 2‑ and 7‑bit JPEGs'
  type: TechArticle
- description: 'Java image processing tutorial: learn how to manipulate PSD files
    and save them as JPEGs using Aspose.PSD. Step‑by‑step guide with code examples
    for beginners and pros.'
  name: 'Java image processing tutorial: support 2‑ and 7‑bit JPEGs'
  steps:
  - name: '**Java Development Kit (JDK)** – version 8 or higher.'
    text: '**Java Development Kit (JDK)** – version 8 or higher.'
  - name: '**Aspose.PSD for Java library** – you can [download it here](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – you can [download it here](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
  - name: '**Sample PSD file** – any PSD you wish to convert.'
    text: '**Sample PSD file** – any PSD you wish to convert.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables creation, manipulation,
      and conversion of Photoshop PSD files directly from Java applications.
    question: What is Aspose.PSD for Java?
  - answer: You can download the library from the [website](https://releases.aspose.com/psd/java/)
      and add the JAR to your project’s build path or Maven/Gradle dependencies.
    question: How do I install Aspose.PSD for Java?
  - answer: Yes, you can load custom RGB or CMYK ICC profiles and assign them to the
      `JpegOptions` before saving.
    question: Can I use custom color profiles with Aspose.PSD for Java?
  - answer: It supports PSD, JPEG, PNG, BMP, TIFF, GIF, and over 20 additional raster
      formats.
    question: What image formats does Aspose.PSD for Java support?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library before purchasing a license.
    question: Is there a free trial available for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- Aspose.PSD
- JPEG conversion
title: 'Java image processing tutorial: support 2‑ and 7‑bit JPEGs'
url: /java/java-jpeg-image-processing/support-2-7-bits-jpeg-java/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java image processing tutorial: support 2‑ and 7‑bit JPEGs

## Introduction
In this **java image processing tutorial**, you’ll discover how to use the Aspose.PSD for Java library to load a PSD file and export it as a 2‑ or 7‑bit JPEG. Whether you’re building a batch‑conversion service or need fine‑grained control over image quality, the steps below walk you through everything from environment setup to saving the final JPEG. Let’s get started!

## Quick answers
- **Which library handles 2‑ and 7‑bit JPEGs?** Aspose.PSD for Java.  
- **Minimum Java version?** JDK 8 or later.  
- **Do I need a license for development?** A free trial works for evaluation; a commercial license is required for production.  
- **Can I change the color mode?** Yes – CMYK, YCCK, and other modes are supported via `JpegCompressionColorMode`.  
- **What file size reduction can I expect?** Using 2‑bit per channel can shrink the JPEG by up to 80 % compared with 8‑bit output.

## What is java image processing tutorial?
A java image processing tutorial is a step‑by‑step guide that teaches developers how to programmatically manipulate image data using Java. It covers loading various formats, applying transformations, adjusting color and compression settings, and saving the results, enabling you to build custom image‑handling workflows.

## Why use Aspose.PSD for Java?
Aspose.PSD for Java provides a comprehensive API for working with Photoshop files without requiring Photoshop itself. It supports over 30 image formats, handles files up to 2 GB by streaming data, and offers fine‑grained control over layers, channels, and color profiles, making it ideal for high‑performance server‑side processing.

## Prerequisites
Before you begin, verify that you have the following:

1. **Java Development Kit (JDK)** – version 8 or higher.  
2. **Aspose.PSD for Java library** – you can [download it here](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, or NetBeans.  
4. **Sample PSD file** – any PSD you wish to convert.  
5. **Basic Java knowledge** – familiarity with classes, objects, and exception handling.

## Import packages
First, add the Aspose.PSD JAR to your project’s classpath. Then import the required namespaces:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.jpeg.JpegCompressionColorMode;
import com.aspose.psd.fileformats.jpeg.JpegCompressionMode;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
```

## How to load a PSD image in Java?
To load a PSD file, call the static `load` method of the `Image` class and cast the result to `PsdImage`. This creates an in‑memory representation of the Photoshop document, giving you access to its layers, channels, masks, and metadata, which you can then manipulate or export to other formats.

`PsdImage` is Aspose.PSD's core class that represents a Photoshop document in memory, enabling read/write operations on its content.

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "PsdImage.psd");
```

## How to configure JPEG options for 2‑ or 7‑bit output?
Create a new `JpegOptions` instance and set its properties to match the desired output. Use `setColorType` to choose the appropriate `JpegCompressionColorMode` (e.g., CMYK or YCCK), and `setCompressionType` to select the compression algorithm. Finally, assign the `bitsPerChannel` value (2 or 7) to control the bit depth of each color channel.

```java
JpegOptions options = new JpegOptions();
options.setColorType(JpegCompressionColorMode.Cmyk);
options.setCompressionType(JpegCompressionMode.JpegLs);
```

## How to set bits per channel for low‑bit JPEGs?
`bitsPerChannel` specifies the number of bits used for each color channel in the output JPEG. Setting this property to 2 reduces each channel to two bits, producing a highly compressed image with noticeable banding, while a value of 7 retains more detail and yields a file size between the extreme low‑bit and standard 8‑bit outputs. Choose the value that balances quality and size for your use case.

```java
byte bpp = 2;
options.setBitsPerChannel(bpp);
```

## How to apply color profiles (optional)?
`ICCProfile` represents an International Color Consortium profile that describes the color characteristics of a device or working space. If you have a custom ICC file, load it with `ICCProfile.getInstance(path)` and assign it to the `jpegOptions` object's `iccProfile` property. Leaving the property null causes Aspose.PSD to use the default system profile, which works for most scenarios.

```java
options.setRgbColorProfile(null);
options.setCmykColorProfile(null);
```

## How to save the processed image as a JPEG?
The `save` method writes the image to a file using the provided options. Call it on the `PsdImage` instance, passing the target filename (including .jpg extension) and the configured `JpegOptions`. The library handles encoding, applying the selected bits‑per‑channel and color profile, and produces a JPEG that matches your specifications.

```java
image.save(dataDir + "2_7BitsJPEG_output.jpg", options);
```

## Common issues and solutions
- **File too large error** – Ensure you are using the latest Aspose.PSD version, which streams data and avoids loading the whole file into RAM.  
- **Unexpected colors** – Verify that the selected `JpegCompressionColorMode` matches your source image’s color space.  
- **Missing ICC profile** – If you need a specific profile, load it with `ICCProfile.getInstance(path)` and assign it to `JpegOptions`.

## Frequently asked questions

**Q: What is Aspose.PSD for Java?**  
A: Aspose.PSD for Java is a commercial library that enables creation, manipulation, and conversion of Photoshop PSD files directly from Java applications.

**Q: How do I install Aspose.PSD for Java?**  
A: You can download the library from the [website](https://releases.aspose.com/psd/java/) and add the JAR to your project’s build path or Maven/Gradle dependencies.

**Q: Can I use custom color profiles with Aspose.PSD for Java?**  
A: Yes, you can load custom RGB or CMYK ICC profiles and assign them to the `JpegOptions` before saving.

**Q: What image formats does Aspose.PSD for Java support?**  
A: It supports PSD, JPEG, PNG, BMP, TIFF, GIF, and over 20 additional raster formats.

**Q: Is there a free trial available for Aspose.PSD for Java?**  
A: Yes, you can download a [free trial](https://releases.aspose.com/) to evaluate the library before purchasing a license.

---

**Last Updated:** 2026-10-08  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose

## Related Tutorials

- [Image Processing Java – Support for JPEG-LS with CMYK](/psd/java/java-jpeg-image-processing/support-jpeg-ls-cmyk-java/)
- [Save PSD as JPEG and Support RGB Color with Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [How to Convert PSD to Raster Image Formats with Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}