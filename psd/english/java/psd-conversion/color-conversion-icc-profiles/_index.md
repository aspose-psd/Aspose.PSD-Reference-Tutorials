---
title: How to Use ICC Profiles for Color Conversion in Aspose.PSD
linktitle: Color Conversion using ICC Profiles
second_title: Aspose.PSD Java API
description: Learn how to use ICC profiles to convert color profiles, apply ICC profile settings, and set RGB profile when creating PSD images with Aspose.PSD for Java.
weight: 12
url: /java/psd-conversion/color-conversion-icc-profiles/
date: 2026-03-21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to Use ICC Profiles for Color Conversion in Aspose.PSD

## Introduction
If you’re looking to **how to use icc** profiles to guarantee accurate colors across devices, you’ve come to the right place. In this tutorial we’ll walk through converting a color profile, applying an ICC profile, and setting an RGB profile while **creating a PSD image** with Aspose.PSD for Java. Whether you’re building a batch‑processing pipeline or a single‑image editor, the steps below will give you a solid, production‑ready foundation.

## Quick Answers
- **What is the primary purpose of an ICC profile?** It defines how colors should be interpreted on a specific device or color space.  
- **Which class represents a PSD image in Aspose.PSD?** `PsdImage`.  
- **Can I change both RGB and CMYK profiles?** Yes – use `setRgbColorProfile` and `setCmykColorProfile`.  
- **Do I need a license for development?** A free trial works for testing; a license is required for production.  
- **What output format supports YCCK?** JPEG with `JpegCompressionColorMode.Ycck`.

## What is ICC Color Conversion?
ICC (International Color Consortium) profiles are standardized data sets that describe the color characteristics of devices (monitors, printers, scanners). By **convert color profile** from one space to another, you ensure that the visual appearance remains consistent, no matter where the image is viewed.

## Why Use ICC Profiles with Aspose.PSD?
- **Accurate color reproduction** – essential for branding and print workflows.  
- **Cross‑platform consistency** – the same image looks the same on Windows, macOS, and mobile.  
- **Built‑in API support** – Aspose.PSD lets you **apply icc profile** and **set rgb profile** with just a few lines of Java.

## Prerequisites
Before you start, make sure you have the following:

1. **Aspose.PSD for Java** – download the latest library from the [releases](https://releases.aspose.com/psd/java/) page.  
2. **Java Development Environment** – JDK 8+ and your favorite IDE.  
3. **ICC Profiles** – for this example we’ll use `eciRGB_v2.icc` (RGB) and `ISOcoated_v2_FullGamut4.icc` (CMYK). You can obtain them from reputable color‑management sources.

## Import Packages
Add the required Aspose.PSD namespaces to your project. These imports give you access to image handling, JPEG options, and stream sources.

```java
import com.aspose.psd.Color;
import com.aspose.psd.fileformats.jpeg.JpegCompressionColorMode;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
import com.aspose.psd.sources.StreamSource;
import java.io.File;
import java.io.FileInputStream;
import java.io.FileNotFoundException;
```

## How to Use ICC Profiles for Color Conversion
Below is a step‑by‑step guide that shows **how to convert color** using ICC profiles while **creating a PSD image**.

### Step 1: Create a New Image (Create PSD Image)
First, instantiate a blank `PsdImage`. This gives you a canvas you can fill with pixel data.

```java
String dataDir = "Your Document Directory";
PsdImage image = new PsdImage(500, 500);
```

### Step 2: Fill Image Data
Populate the image with raw ARGB pixel values. In a real‑world scenario you might load pixel data from another source, but here we simply illustrate the process.

```java
int count = image.getWidth() * image.getHeight();
int[] pixels = new int[count];
int r = 0, g = 0, b = 0, channel = 0;
for (int i = 0; i < count; i++) {
    // Fill pixels with color values.
    // ...
}
// Save the newly created pixels.
image.saveArgb32Pixels(image.getBounds(), pixels);
```

### Step 3: Save Image with Default ICC Profiles
Saving at this point writes the image using the library’s default color profiles. This step helps you see the difference after applying custom profiles later.

```java
image.save(dataDir + "Default_profiles.jpg");
```

### Step 4: Update Color Profiles (Apply ICC Profile & Set RGB Profile)
Load the external ICC files and assign them to the image. This is where we **apply icc profile** and **set rgb profile**.

```java
File rgbFile = new File(dataDir + "eciRGB_v2.icc");
FileInputStream rgbInputStream = new FileInputStream(rgbFile);
StreamSource rgbprofile = new StreamSource(rgbInputStream);
File cmykFile = new File(dataDir + "ISOcoated_v2_FullGamut4.icc");
FileInputStream cmykInputStream = new FileInputStream(cmykFile);
StreamSource cmykprofile = new StreamSource(cmykInputStream);
image.setRgbColorProfile(rgbprofile);
image.setCmykColorProfile(cmykprofile);
```

### Step 5: Save Image with New YCCK Profiles
Finally, export the image as a JPEG using the YCCK color mode, which respects the CMYK profile we just set.

```java
JpegOptions options = new JpegOptions();
options.setColorType(JpegCompressionColorMode.Ycck);
image.save(dataDir + "Ycck_profiles.jpg", options);
```

By following these steps you have **converted the color profile** of a PSD image, **applied ICC profiles**, and **set the RGB profile** for accurate rendering.

## Common Issues and Solutions
| Issue | Reason | Fix |
|-------|--------|-----|
| Colors look washed out after conversion | Wrong profile assigned or missing profile data | Verify that the ICC files correspond to the source image’s color space. |
| `FileNotFoundException` when loading ICC files | Incorrect `dataDir` path | Use an absolute path or ensure the files are placed in the specified directory. |
| JPEG saved without YCCK colors | `JpegOptions` not set to `Ycck` | Call `options.setColorType(JpegCompressionColorMode.Ycck)` before saving. |

## Frequently Asked Questions
**Q: Can I use custom ICC profiles with Aspose.PSD for Java?**  
A: Yes, simply replace the provided ICC files with your own and point the `StreamSource` to the new files.

**Q: How can I handle color differences in the resulting images?**  
A: Fine‑tune the ICC profiles or use Aspose.PSD’s color‑adjustment APIs to tweak brightness, contrast, or gamma after conversion.

**Q: Is Aspose.PSD suitable for batch processing of images?**  
A: Absolutely. You can loop through a folder of PSD files, apply the same profile logic, and save the results efficiently.

**Q: Where can I find more ICC profiles for color management?**  
A: Look at the ICC website, Adobe’s color resource page, or vendor‑specific libraries that provide device‑specific profiles.

**Q: What are the benefits of using ICC profiles in color conversion?**  
A: They guarantee consistent color across different devices, simplify workflow automation, and reduce manual color‑matching effort.

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Last Updated:** 2026-03-21  
**Tested With:** Aspose.PSD for Java (latest)  
**Author:** Aspose