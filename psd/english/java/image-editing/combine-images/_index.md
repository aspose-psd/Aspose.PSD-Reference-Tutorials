---
title: How to create PSD file Java – Combine Images with Aspose.PSD
linktitle: Combine Images
second_title: Aspose.PSD Java API
description: Learn how to create PSD file Java by combining two images using Aspose.PSD. Follow our step‑by‑step guide to merge images into a PSD file quickly.
date: 2025-12-30
weight: 11
url: /java/image-editing/combine-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Create PSD file Java – Combine Images using Aspose.PSD

## Introduction

If you need to **create a PSD file in Java** by merging several pictures, Aspose.PSD makes the job straightforward. In this tutorial we’ll walk through combining two images into a single PSD canvas, explain why this approach is useful, and give you ready‑to‑run code. By the end you’ll be able to **combine two images Java** style and generate a professional‑looking layered file.

## Quick Answers
- **What library is best for merging images into PSD?** Aspose.PSD for Java.
- **How long does the implementation take?** About 10‑15 minutes for a basic combine.
- **Do I need a license?** A free trial works for testing; a commercial license is required for production.
- **Can I add more than two images?** Yes – repeat the `drawImage` calls for each additional layer.
- **Which Java version is supported?** Java 8 and newer.

## Prerequisites

Before diving in, ensure you have the following:

1. **Aspose.PSD Library** – download it from [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit (JDK)** – Java 8+ is recommended.  
3. **Document Directory** – a folder on your machine where the source images and the resulting PSD will be stored.

## Import Packages

Start by importing the required Aspose.PSD classes into your project:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## Step‑by‑Step Guide

### Step 1: Create PSD Options (prepare the file)

We first create a `PsdOptions` instance that will hold the output settings.

```java
PsdOptions imageOptions = new PsdOptions();
```

### Step 2: Set the FileCreateSource (define where the PSD will be saved)

Assign a `FileCreateSource` to the options, pointing to the desired result file.

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

### Step 3: Create Image Instance (initialize canvas size)

Create an `Image` object with the options and specify a canvas of 600 × 600 pixels.

```java
Image image = Image.create(imageOptions, 600, 600);
```

### Step 4: Initialize Graphics and draw the first picture

A `Graphics` object lets us paint on the canvas. We clear the background to white and draw the first source image on the left half.

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

### Step 5: Draw the second picture (complete the combine)

Now we place the second image on the right half of the same canvas.

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

### Step 6: Save the resulting PSD file

Finally, persist the combined canvas to disk.

```java
image.save();
```

Congratulations! You have successfully **merge images into PSD** and created a PSD file in Java.

## Why combine images with Aspose.PSD?

- **Layer‑aware** – each `drawImage` call adds a separate layer you can edit later.  
- **Format flexibility** – supports PSD, PNG, JPEG, BMP, and more.  
- **No native dependencies** – pure Java, works on any OS that runs the JDK.  

## Common Issues and Solutions

| Issue | Cause | Fix |
|-------|-------|-----|
| `File not found` error when loading source images | Incorrect `dataDir` path | Verify `dataDir` points to the folder containing `example1.psd` and `example2.psd`. |
| Output PSD is blank | `graphics.clear` called after drawing | Ensure `graphics.clear(Color.getWhite())` is executed **before** any `drawImage` calls. |
| License exception at runtime | Missing or expired Aspose.PSD license | Apply a valid license using `License license = new License(); license.setLicense("Aspose.PSD.lic");` before any API call. |

## Frequently Asked Questions

### Q1: Is Aspose.PSD compatible with all image formats?
A1: Aspose.PSD primarily focuses on PSD file format. However, it supports various other formats for input and output.

### Q2: Can I perform additional modifications on the combined image?
A2: Absolutely! After combining images, you can further manipulate the resulting PSD using Aspose.PSD's extensive features.

### Q3: Are there any licensing requirements for using Aspose.PSD?
A3: Yes, a valid license is required for commercial use. Obtain it from [here](https://purchase.aspose.com/buy).

### Q4: Is there a free trial available for Aspose.PSD?
A4: Yes, you can explore Aspose.PSD with a free trial [here](https://releases.aspose.com/).

### Q5: Where can I find support for Aspose.PSD-related queries?
A5: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community support and discussions.

---

**Last Updated:** 2025-12-30  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}