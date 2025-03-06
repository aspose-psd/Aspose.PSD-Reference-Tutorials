---
title: Control Cache Reallocation in PSD Files
linktitle: Control Cache Reallocation in PSD Files
second_title: Aspose.PSD Java API
description: Manage cache reallocation in PSD files using Aspose.PSD for Java. Learn how to optimize memory and file handling efficiently—ideal for developers.
weight: 22
url: /java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Control Cache Reallocation in PSD Files

## Introduction
When working with images and Photoshop files programmatically, efficiency is a key factor. Aspose.PSD for Java offers robust features to manage and manipulate PSD files seamlessly. One of the fundamental aspects of optimizing performance is controlling cache reallocation. Cache management helps in maintaining the balance between memory and disk usage, ensuring your application runs smoothly, without unexpected crashes or slowdowns. 
## Prerequisites
Before we jump into the coding part, there are a few things you need to ensure so that everything runs smoothly:
1. Java Development Kit (JDK): Ensure that you have JDK installed on your machine. You can download it from [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java: You need to download the Aspose.PSD library. You can find the latest release [here](https://releases.aspose.com/psd/java/).
3. IDE Setup: An Integrated Development Environment (IDE) like IntelliJ IDEA or Eclipse will make it easier for you to manage your code.
4. Basic Understanding of Java: Familiarity with Java programming will help you understand the concepts and code snippets better.
5. Aspose License (Optional): If you wish to remove watermarks and gain full functionality, consider purchasing a license [here](https://purchase.aspose.com/buy) or trying the free trial [here](https://releases.aspose.com/).
## Import Packages
Before we start writing the code, let’s make sure we have the necessary packages imported. Below is a brief list of what to include at the beginning of your Java file:
```java
import com.aspose.psd.Cache;
import com.aspose.psd.CacheType;
import com.aspose.psd.Color;
import com.aspose.psd.ColorPalette;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.imageoptions.GifOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.MemoryStream;
```
## Step 1: Setting Up Your Data Directory
First things first, you’ll need to set up a directory where you want your cache files to be stored. This is essential for managing the cache effectively.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- String dataDir: Define the directory for your document cache.
- Cache.setCacheFolder(dataDir): This method sets the cache folder to the specified directory. Any cache created by Aspose will now be stored here instead of the default temporary directory.
## Step 2: Configuring Cache To Disk
Next, we’ll specify that we want our cache to be stored on disk only. This is particularly useful if your application uses large files and you want to ensure that memory remains free.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- Cache.setCacheType(CacheType.CacheOnDiskOnly): This option ensures that the cache is not held in memory, which is beneficial for handling large PSD files without consuming too much RAM.
## Step 3: Setting Maximum Disk and Memory Cache Size
Now, let's restrict our cache sizes. This is crucial because unlimited cache can lead to performance issues.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- Cache.setMaxDiskSpaceForCache(1073741824): This sets a limit of 1 GB for the cache on disk. You can adjust this size depending on your needs.
- Cache.setMaxMemoryForCache(1073741824): Similarly, this limits the in-memory cache, ensuring that your application does not use excessive memory.
## Step 4: Manage Cache Reallocation Strategy
Managing how cache is reallocated is essential for maintaining performance. Here’s how you can set it up.
```java
Cache.setExactReallocateOnly(false);
```

- Cache.setExactReallocateOnly(false): When set to false, this allows Aspose to manage cache reallocation more flexibly, which can lead to better performance.
## Step 5: Check Allocated Cache Size
This step is about monitoring how many bytes are currently allocated for the cache in memory or on disk. Let’s implement that:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- long l1: Stores the count of bytes allocated on the disk.
- long l2: Stores the count of bytes allocated in memory. 
You can check these values at any time to ensure your application is managing memory and disk usage as expected.
## Step 6: Creating a PSD Image
Now that we have our cache configurations set up, let’s create a simple PSD image.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- PsdOptions options: This object allows you to specify options when creating a Photoshop image.
- Color[] color: An array containing the colors that will be used in the image palette.
## Step 7: Saving Pixel Data to the Image
Now, let’s populate our image with pixel data and save it.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- Color[] pixels: This is an array of color objects. Here, we’re filling it with white pixels.
- image.savePixels(image.getBounds(), pixels): This method saves the pixel data to the image. It updates the image with the colors we've defined.
## Step 8: Monitoring Allocated Cache After Image Creation
After creating the image, it’s a good practice to check how many bytes are allocated for the cache again.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- long diskBytes: Captures the current allocation on the disk after the image creation.
- long memoryBytes: Captures the current allocation in memory. 
This step will help you determine how much cache is being consumed after your operations.
## Step 9: Check for Proper Disposal
Lastly, it's crucial to ensure that all Aspose.PSD objects were disposed of properly to avoid memory leaks.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- l1 and l2: These variables will help you check the final allocation. If they’re not zero, it indicates some objects haven’t been disposed of properly.
## Conclusion
Controlling cache reallocation in Aspose.PSD for Java can make a significant difference in your application’s performance. By following the steps outlined above, you can effectively manage the cache, minimize memory usage, and create beautiful PSD files efficiently. Embrace these techniques, and watch your applications thrive with optimal performance!
## FAQ's
### What is Aspose.PSD?
Aspose.PSD is a library for .NET and Java developers to create, manipulate, and convert Photoshop (PSD) files programmatically.
### How do I check allocated cache size?
Use methods like `Cache.getAllocatedDiskBytesCount()` and `Cache.getAllocatedMemoryBytesCount()` to monitor current cache usage.
### Can I set a custom directory for cache?
Yes, you can specify a different directory by using `Cache.setCacheFolder("Your Directory Path")`.
### Is Aspose.PSD free to use?
Aspose.PSD is a paid library, but you can start with a free trial available on their [website](https://releases.aspose.com/).
### What happens if I don’t dispose of objects?
Not disposing of objects can lead to memory leaks, causing your application to use more resources than necessary.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
