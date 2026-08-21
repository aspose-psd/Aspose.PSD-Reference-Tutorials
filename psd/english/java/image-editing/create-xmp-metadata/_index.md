---
title: 'Create XMP Metadata in PSD Files Using Aspose.PSD for Java'
linktitle: Create XMP Metadata
second_title: Aspose.PSD Java API
description: Learn how to manipulate image metadata and add author metadata using Aspose.PSD for Java – step‑by‑step guide to create XMP metadata.
weight: 12
url: /java/image-editing/create-xmp-metadata/
date: 2026-07-03
keywords:
- manipulate image metadata
- add author metadata
- Aspose.PSD Java
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Create XMP Metadata with Aspose.PSD for Java

**XMP metadata** is a standardized format for embedding descriptive information directly within image files.

## Introduction

In modern Java applications, the ability to **manipulate image metadata** is essential for digital asset management, automated publishing, and compliance workflows. With Aspose.PSD for Java you can programmatically create, edit, and embed XMP metadata—such as author, copyright, and keywords—into PSD files without ever opening Photoshop. This tutorial walks you through the complete process, from setting up the environment to saving the final image.

## Quick Answers
- **What does this tutorial cover?** Creating and embedding XMP metadata in a PSD using Aspose.PSD for Java.  
- **How many steps are involved?** Twelve clear steps, each with a concise code placeholder.  
- **Do I need a license?** A free trial works for development; a commercial license is required for production.  
- **Which Java version is supported?** Java 8 and above.  
- **Can I add author information?** Yes—see the “add author metadata” section for details.

## What is XMP metadata?
XMP (Extensible Metadata Platform) is an ISO‑standard XML format that stores metadata inside image files. It enables consistent sharing of information like creator, description, and usage rights across different applications. It can store information such as creator, title, rights, and custom tags, and is recognized by most image editing and cataloging software. By embedding XMP directly, the metadata travels with the file, ensuring consistent identification across platforms.

## Why use Aspose.PSD for Java to manipulate image metadata?
Aspose.PSD supports **30+ image formats** and can process files up to **2 GB** while keeping memory usage below **200 MB**. The library works entirely in code—no Photoshop installation is required—making it ideal for server‑side automation and batch processing. It also provides a simple API for reading and writing XMP, Photoshop, and IPTC blocks, allowing developers to integrate metadata handling into automated pipelines without third‑party tools.

## Prerequisites

- **Java Development Environment** – Java 8+ installed and a basic familiarity with Java programming.  
- **Aspose.PSD Library** – Download and set up the Aspose.PSD library for Java. You can find the library and detailed documentation on the [Aspose.PSD for Java documentation page](https://reference.aspose.com/psd/java/).  
- **Document Directory** – Define the folder where your PSD files will be read from and saved to.

## How to manipulate image metadata with Aspose.PSD for Java?
`XmpMetadata` is a class that represents XMP data structures and provides methods to set standard and custom metadata fields. Load your target PSD file, create an `XmpMetadata` object, populate the desired fields (e.g., author, title, keywords), and then attach the metadata back to the image before saving. This end‑to‑end flow lets you **manipulate image metadata** in just a few lines of Java code, without manual file editing.

## Import Packages

```java
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.system.io.MemoryStream;
import com.aspose.psd.xmp.XmpHeaderPi;
import com.aspose.psd.xmp.XmpMeta;
import com.aspose.psd.xmp.XmpPacketWrapper;
import com.aspose.psd.xmp.XmpTrailerPi;
import com.aspose.psd.xmp.schemas.dublincore.DublinCorePackage;
import com.aspose.psd.xmp.schemas.photoshop.ColorMode;
import com.aspose.psd.xmp.schemas.photoshop.PhotoshopPackage;
```

## Step 1: specify image size

```java
// Specify the size of the image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## Step 2: create a new image

```java
// Create a brand new image for sample purposes
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## Step 3: create XMP header

```java
// Create an instance of XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## Step 4: create XMP trailer

```java
// Create an instance of Xmp-TrailerPi 
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Step 5: create XMP metadata

```java
// Create an instance of XMPmeta class to set different attributes
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Step 6: create XMP packet wrapper

```java
// Create an instance of XmpPacketWrapper that contains all metadata
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Step 7: set photoshop attributes

```java
// Create an instance of Photoshop package and set Photoshop attributes
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## Step 8: add photoshop package to XMP metadata

```java
// Add Photoshop package into XMP metadata
xmpData.addPackage(photoshopPackage);
```

## Step 9: set dublinCore attributes

```java
// Create an instance of DublinCore package and set DublinCore attributes
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## Step 10: add dublinCore package to XMP metadata

```java
// Add DublinCore Package into XMP metadata
xmpData.addPackage(dublinCorePackage);
```

## Step 11: update XMP metadata into image

```java
// Update XMP metadata into the image
image.setXmpData(xmpData);
```

## Step 12: save image

```java
// Save the image on the disk or in a memory stream
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## How to add author metadata to XMP?
Use the `XmpMetadata` API to set the `dc:creator` property, which stores the author name. After assigning the author, the metadata is written back to the PSD when you call `image.save()`. This approach ensures the author information is permanently embedded and searchable by any XMP‑aware tool.

## Common issues and solutions

- **Metadata not appearing after save** – Verify that you called `image.updateXmpMetadata(xmpMetadata)` before invoking `image.save()`.  
- **Large files cause OutOfMemoryError** – Enable streaming mode by setting `PsFileFormatOptions.setUseMemoryCache(true)` to keep memory usage low.  
- **Author name shows as empty** – Ensure the Unicode string is correctly encoded; use `new String("Your Name".getBytes("UTF-8"), "UTF-8")` when assigning.

## Frequently asked questions

**Q: Is Aspose.PSD compatible with different image formats?**  
A: Yes, Aspose.PSD supports over 30 raster and vector formats, allowing you to work with PSD, JPEG, PNG, TIFF, and more.

**Q: Can I manipulate existing metadata using Aspose.PSD?**  
A: Absolutely. You can read, modify, and rewrite any XMP or Photoshop‑specific metadata block within an image.

**Q: Are there any limitations on the image size Aspose.PSD can handle?**  
A: The library can process images up to 2 GB in size, and it uses a streaming architecture to keep RAM consumption modest.

**Q: Is there a trial version available for Aspose.PSD?**  
A: Yes, you can explore the capabilities of Aspose.PSD by obtaining a free trial from the [Aspose.PSD free trial download](https://releases.aspose.com/).

**Q: Where can I seek support for Aspose.PSD-related queries?**  
A: For any assistance or queries, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

---

**Last Updated:** 2026-07-03  
**Tested With:** Aspose.PSD for Java 24.10  
**Author:** Aspose

## Related Tutorials

- [Create Image using Stream in Aspose.PSD for Java](/psd/java/image-editing/create-image-using-stream/)
- [How to Rotate Image in Java with Aspose.PSD](/psd/java/advanced-image-manipulation/rotate-image/)
- [Java Image Manipulation - Add Effects at Runtime with Aspose.PSD for Java](/psd/java/advanced-techniques/add-effects-runtime/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}