---
date: 2026-03-18
description: Dowiedz się, jak konwertować pliki PSD na PNG, zmieniając przy tym głębię
  bitową PNG przy użyciu Aspose.PSD for Java – przewodnik krok po kroku z przykładami
  kodu.
linktitle: Specify PNG Bit Depth in Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Jak przekonwertować PSD na PNG o określonej głębi bitowej przy użyciu Aspose.PSD
  dla Javy
url: /pl/java/optimizing-png-files/specify-png-bit-depth/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konwertuj PSD do PNG z określoną głębokością bitową przy użyciu Aspose.PSD for Java

## Introduction
If you need to **convert psd to png** and control the exact PNG bit depth, you’re in the right place. In this tutorial we’ll walk through how to change png bit depth while saving a PSD file as a PNG image with Aspose.PSD for Java. Whether you’re building a batch‑processing tool, a web service, or a desktop utility, being able to **save png with options** such as grayscale color type and custom bit depth gives you fine‑grained control over image quality and file size.

## Quick Answers
- **Can I change the PNG bit depth?** Yes – use `PngOptions.setBitDepth()` to specify 1, 2, 4, 8, or 16 bits.  
- **Which color types are supported?** Grayscale, TrueColor, Indexed, and others via `PngColorType`.  
- **Do I need a license for Aspose.PSD?** A free trial works for development; a commercial license is required for production.  
- **What Java version is required?** Java 8+ (the library is compatible with newer JDKs).  
- **Is the code runnable as‑is?** Yes – just replace the placeholder path with your own folder.

## What is “convert psd to png” with custom bit depth?
Converting a Photoshop PSD file to a PNG image is a common task when you need a web‑friendly format. Adding the ability to **adjust png quality** by setting the bit depth lets you balance visual fidelity against file size, which is especially useful for thumbnails, icons, or when bandwidth is limited.

## Why use Aspose.PSD for Java?
Aspose.PSD for Java provides a high‑level API that abstracts the complexity of the PSD format. It lets you **create grayscale png**, **save png with options**, and handle color profiles without dealing with low‑level byte manipulation. The library is fully managed, cross‑platform, and receives regular updates.

## Prerequisites
Before we dive into the code, make sure you have the following:

1. **Java Development Kit (JDK)** – download it from [Oracle’s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – obtain the latest JAR from [this link](https://releases.aspose.com/psd/java/).  
3. **Basic Java knowledge** – you should be comfortable with classes, methods, and exception handling.  
4. **An IDE** such as IntelliJ IDEA or Eclipse (optional but recommended).  
5. **A sample PSD file** – place it in a folder you’ll reference in the code.

Got everything? Great – let’s import the necessary packages.

## Import Packages
Now that we have our prerequisites covered, it’s time to get our environment set up by importing the relevant packages in our Java application. Start your coding environment and add the following import statements at the top of your Java file:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

These statements import the classes that we’ll be using throughout the tutorial, enabling us to load PSD files and save them as PNG images with the specified bit depth.

## Step 1: Set Up Your Document Directory
Before diving into image processing, let’s define a directory where our images will be stored. This is like creating a folder for your art supplies before starting a craft project.

```java
String dataDir = "Your Document Directory";
```

## Step 2: Load the PSD Image
Next up, we need to load the PSD image file you want to convert. Think of this as opening up a canvas where you’ll do all your work.

```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
```

Here, we are making use of the `Image.load()` method to read our sample PSD file and cast it to `PsdImage` to access PSD‑specific properties.

## Step 3: Create PNG Options
Once we have our canvas open, we need a set of options for how we want to save our image. This is essentially choosing your colors and brush styles before you start painting.

```java
PngOptions options = new PngOptions();
```

In this step, we’re initializing an instance of `PngOptions`, which allows us to specify the parameters for our PNG output.

## Step 4: Set the Desired Color Type
Now we decide what kind of colors we want in our final PNG image. Are you going for a colorful palette or a monochromatic style? Let’s make that decision!

```java
options.setColorType(PngColorType.Grayscale);
```

In this example, we set the color type to grayscale. You could also choose `PngColorType.TrueColor` if you want a full‑color image. This is the part where we **create grayscale png**.

## Step 5: Specify the Bit Depth
Next, let’s specify the bit depth. This is similar to telling your printer how finely it should print your image – the more bits, the more detail!

```java
options.setBitDepth((byte)1);
```

Here, we set the bit depth to **1 bit**, which is suitable for simple grayscale images. You can change the value to 2, 4, 8, or 16 depending on your quality requirements – a classic example of how to **change png bit depth**.

## Step 6: Save the PNG Image
Finally, it's time to save your masterpiece! This step concludes our project as we effectively transfer our artwork from the editing canvas to a gallery wall.

```java
psdImage.save(dataDir + "SpecifyBitDepth_out.png", options);
```

Using the `save()` method of `PsdImage`, we save the converted file, applying the options we defined. Voila! Our image is now saved with the custom bit depth.

## Common Issues and Solutions
- **`NullPointerException` when loading the PSD** – double‑check that `dataDir` points to the correct folder and that `sample.psd` exists.  
- **Unsupported bit depth** – Aspose.PSD supports 1, 2, 4, 8, and 16 bits for PNG. Using any other value will throw an `IllegalArgumentException`.  
- **Color type mismatch** – if you set a bit depth that isn’t compatible with the chosen `PngColorType`, the library will automatically adjust to the nearest supported setting.

## Frequently Asked Questions

**Q: What is Aspose.PSD for Java?**  
A: Aspose.PSD for Java is a library for working with PSD files in Java applications, allowing you to manipulate and convert images.

**Q: How do I specify different bit depths?**  
A: You can set the bit depth by using the `options.setBitDepth((byte)n)` method, replacing `n` with your desired depth.

**Q: Can I use Aspose.PSD for free?**  
A: Yes, you can try out the library with a free trial which you can find [here](https://releases.aspose.com/).

**Q: Where can I get a support license for Aspose?**  
A: For a temporary license, you can apply [here](https://purchase.aspose.com/temporary-license/).

**Q: What type of images can I convert?**  
A: Aspose.PSD primarily deals with PSD files, but it supports conversion to various formats like PNG, JPEG, and TIFF.

## Conclusion
You’ve now learned how to **convert psd to png** while controlling the PNG bit depth using Aspose.PSD for Java. By tweaking the `PngOptions`, you can **adjust png quality**, create **grayscale png**, and fine‑tune file size for any scenario. Experiment with different color types and bit depths to find the perfect balance for your application.

---

**Last Updated:** 2026-03-18  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}