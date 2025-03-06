---
title: Auto Correct JPEG Image Orientation in Java
linktitle: Auto Correct JPEG Image Orientation in Java
second_title: Aspose.PSD Java API
description: Learn to automatically correct JPEG image orientation in Java using Aspose.PSD. Enhance your image processing skills effortlessly.
weight: 12
url: /java/java-jpeg-image-processing/auto-correct-jpeg-image-orientation-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Auto Correct JPEG Image Orientation in Java

## Introduction
In today's digital age, manipulating and optimizing images programmatically has become a crucial task for developers across various domains. Aspose.PSD for Java empowers developers with robust tools to handle PSD, JPEG, and other image formats efficiently. This tutorial dives into a specific task: automatically correcting JPEG image orientation using Aspose.PSD for Java. Whether you're building a photo editing app, managing image resources in a content management system, or automating image processing workflows, this guide will equip you with the necessary knowledge to seamlessly integrate this functionality into your Java applications.
## Prerequisites
Before diving into this tutorial, ensure you have the following prerequisites set up:
- Java Development Environment: Make sure you have Java Development Kit (JDK) installed on your system.
- Aspose.PSD for Java JAR: Download the Aspose.PSD for Java library from [here](https://releases.aspose.com/psd/java/).
- Integrated Development Environment (IDE): Use IntelliJ IDEA, Eclipse, or any IDE of your choice for Java development.
- Basic Understanding of Java and Image Processing: Familiarity with Java programming and basic concepts of image processing will be beneficial.

## Import Packages
Before starting with the example, make sure to import the necessary packages from Aspose.PSD for Java:
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```
## Step 1: Load the PSD Image
Firstly, load the PSD image that contains the JPEG thumbnail whose orientation needs correction:
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
Replace `"Your Document Directory"` with the actual directory path where your PSD file is located.
## Step 2: Iterate Over Image Resources
Next, iterate through the image resources to find the JPEG thumbnail resource:
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Find thumbnail resource. Typically they are in the Jpeg file format.
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Adjust thumbnail data.
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null && exifData.getThumbnail() != null) {
            // If there is a thumbnail stored, auto-rotate it.
            PsdImage jpegImage = (PsdImage) exifData.getThumbnail();
            if (jpegImage != null) {
                jpegImage.autoRotate();
            }
        }
    }
}
```
## Step 3: Save the Image
Finally, save the corrected image after applying the auto-rotation:
```java
image.save();
```
This step ensures that the changes made to the image are persisted.

## Conclusion
In conclusion, using Aspose.PSD for Java provides a powerful solution for automatically correcting JPEG image orientations within PSD files. By following the steps outlined in this tutorial, developers can enhance their image processing workflows, ensuring images are correctly displayed across various platforms and devices.
## FAQ's
### What is Aspose.PSD for Java?
Aspose.PSD for Java is a powerful library that allows Java developers to work with PSD, JPEG, and other image formats programmatically.
### How can I download Aspose.PSD for Java?
You can download the library from [here](https://releases.aspose.com/psd/java/).
### Does Aspose.PSD for Java support image manipulation?
Yes, it supports various image manipulation tasks such as resizing, cropping, and adjusting orientation.
### Where can I find documentation for Aspose.PSD for Java?
Comprehensive documentation is available [here](https://reference.aspose.com/psd/java/).
### Can I try Aspose.PSD for Java for free?
Yes, you can get a free trial from [here](https://releases.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
