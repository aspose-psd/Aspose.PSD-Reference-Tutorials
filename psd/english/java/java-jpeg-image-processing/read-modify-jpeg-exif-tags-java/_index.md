---
date: 2026-10-03
description: Learn how to java read image metadata and modify JPEG EXIF tags with
  Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
  image metadata efficiently.
images:
- /java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/og-image.png
keywords:
- java read image metadata
- read EXIF tags Java
- modify JPEG metadata Java
- Aspose.PSD Java
lastmod: 2026-10-03
linktitle: Read and Modify JPEG EXIF Tags in Java
og_description: Learn how to java read image metadata and modify JPEG EXIF tags with
  Aspose.PSD for Java. This guide shows step‑by‑step code for extracting and updating
  EXIF information.
og_image_alt: Guide showing how to java read image metadata and edit JPEG EXIF tags
  using Aspose.PSD for Java
og_title: How to java read image metadata and modify JPEG EXIF tags
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  headline: How to java read image metadata and modify JPEG EXIF tags
  type: TechArticle
- description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  name: How to java read image metadata and modify JPEG EXIF tags
  steps:
  - name: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
    text: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
  type: HowTo
- questions:
  - answer: EXIF (Exchangeable Image File Format) metadata stores camera settings,
      timestamps, GPS coordinates, and other information embedded in JPEG and other
      image files.
    question: What is EXIF data?
  - answer: You can get a free trial from the [Aspose releases page](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for Java for free?
  - answer: Aspose.PSD for Java supports Java SE 7 and above.
    question: Is Aspose.PSD for Java compatible with all versions of Java?
  - answer: Check out the [documentation](https://reference.aspose.com/psd/java/)
      for more details.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: You can get support from the [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).
    question: How do I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- exif tags
- aspose psd
- jpeg metadata
- java tutorial
title: How to java read image metadata and modify JPEG EXIF tags
url: /java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Read and modify JPEG EXIF tags in Java

## Introduction
If you need to **java read image metadata** from JPEG files and change it programmatically, you’ve landed in the right spot. In this tutorial we’ll walk through extracting and updating EXIF tags using Aspose.PSD for Java. By the end you’ll be able to pull camera details, orientation, and custom fields, then write them back to the file—all without a graphical editor.

## Quick answers
- **Which library handles JPEG EXIF in Java?** Aspose.PSD for Java.
- **How many lines of code to read EXIF?** About three lines after loading the image.
- **Can you modify EXIF tags?** Yes, you can change any standard or custom tag and save the result.
- **Supported image formats?** Over 150 formats, including PSD, JPEG, PNG, TIFF, and BMP.
- **Minimum Java version?** Java 7 or higher.

## Why use Aspose.PSD for Java?
Aspose.PSD supports **150+ image formats** and can process files up to **2 GB** without loading the entire document into memory, giving you fast, low‑memory metadata operations on large photo collections. It also provides a simple API for reading and writing EXIF, IPTC, and XMP data, making batch processing of thousands of images efficient and reliable.

## Prerequisites
1. **Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.  
4. **Basic Java knowledge** – you should be comfortable with creating projects and adding external JARs.

## What is Java read image metadata?
Java read image metadata refers to the process of programmatically accessing embedded information such as EXIF, IPTC, and XMP stored inside image files using Java code. This metadata can include camera settings, timestamps, GPS coordinates, copyright notices, and user comments, enabling applications to organize, search, and manipulate images based on their descriptive data.

## Import packages
First, add the Aspose.PSD JAR to your project’s classpath and import the required classes.

The `com.aspose.psd` package provides the core API for loading images and accessing their resources.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## How to read image metadata from JPEG files in Java?
Load the JPEG with `PsdImage.load("image.jpg")`, locate the thumbnail resource that holds EXIF data, and then call `ExifData.read()` to obtain a populated `ExifData` object. This single‑step approach gives you full access to all standard EXIF fields and any custom tags you may have added.

## Step 1: Load the PSD image
PsdImage is the Aspose.PSD class representing a PSD file and provides methods to access its resources and metadata.  
In this step, we’ll load the PSD image from which we want to read the EXIF data. Make sure your image is in the correct directory.

```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Step 2: Iterate over image resources
ThumbnailResource represents a thumbnail image stored in a PSD file, often containing embedded EXIF data.  
Once the image is loaded, the next step is to iterate over its resources to find the thumbnail resource, which typically contains the EXIF data.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Proceed to next step
    }
}
```

## Step 3: Extract EXIF data
JpegExifData is the class that holds EXIF information extracted from a JPEG image, allowing you to read and modify individual tags.  
Now that we have the thumbnail resource, we can extract the EXIF data from it. EXIF data includes valuable information like the camera owner’s name, aperture value, orientation, and more.

```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```

## Step 4: Modify EXIF data
After reading the EXIF data, you might want to modify some of its fields. Here’s how you can do it:

```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```

## Step 5: Save the changes
Finally, after modifying the EXIF data, save the changes to a new PSD file.

```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Common issues and solutions
- **Missing thumbnail resource** – Some JPEGs store EXIF directly in the main image header. If the thumbnail resource is absent, use `image.getExifData()` instead.  
- **Large files cause OutOfMemoryError** – Ensure you run the JVM with enough heap (`-Xmx2g`) or process the image in streaming mode using `PsdImage.load(inputStream, loadOptions)`.  
- **Unsupported tag types** – Aspose.PSD supports all standard EXIF tags; custom tags may require manual byte‑level handling.

## Frequently asked questions

**Q: What is EXIF data?**  
A: EXIF (Exchangeable Image File Format) metadata stores camera settings, timestamps, GPS coordinates, and other information embedded in JPEG and other image files.

**Q: Can I use Aspose.PSD for Java for free?**  
A: You can get a free trial from the [Aspose releases page](https://releases.aspose.com/).

**Q: Is Aspose.PSD for Java compatible with all versions of Java?**  
A: Aspose.PSD for Java supports Java SE 7 and above.

**Q: Where can I find more documentation on Aspose.PSD for Java?**  
A: Check out the [documentation](https://reference.aspose.com/psd/java/) for more details.

**Q: How do I get support for Aspose.PSD for Java?**  
A: You can get support from the [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).

## Conclusion
By following these steps you can **java read image metadata** from any JPEG, adjust the EXIF fields you need, and write the updated data back to the file—all with a few lines of clean Java code. Aspose.PSD’s rich API makes metadata handling reliable and performant, so you can integrate it into batch processing pipelines, photo‑management tools, or any application that needs to work with image information.

---

**Last Updated:** 2026-10-03  
**Tested With:** Aspose.PSD for Java 24.5  
**Author:** Aspose

## Related Tutorials

- [Read Specific EXIF Tags Information in Java with Aspose (asp)](/psd/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/)
- [Create XMP Metadata in PSD Files Using Aspose.PSD for Java](/psd/java/image-editing/create-xmp-metadata/)
- [Resize Image with Aspose.PSD for Java – Draw Shapes & Basic Image Operations](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}