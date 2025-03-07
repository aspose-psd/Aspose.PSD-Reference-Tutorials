---
title: Support Length Record Data Properties in PSD - Java
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
description: Learn how to manipulate PSD files with length record data properties in Java using Aspose.PSD. Follow this step-by-step guide for all the details.
weight: 14
url: /java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Support Length Record Data Properties in PSD - Java

## Introduction
Have you ever worked with Photoshop files and wanted to manipulate layers or shapes programmatically? If so, you’ve stumbled upon the beauty of the Aspose.PSD for Java library. This powerful tool allows developers to interact with and modify PSD files seamlessly through Java code. In today’s article, we’ll be diving into how to support length record data properties in a PSD file using this library. 
Whether you’re a seasoned Java developer or just starting out, this guide will walk you through everything you need to know, step by step. By the end, you’ll be able to open a PSD file, modify its vector shape properties, and save your changes—all without leaving the comfort of your Java environment. Let's roll up our sleeves and jump in!
## Prerequisites
Before we get started, there are a few things you need to have ready. Ensuring you have everything in place makes the process smoother, and nobody likes a last-minute scramble! Here’s what you’ll need:
1. Java Development Kit (JDK): Make sure you have the JDK installed on your machine. You can download it from [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) or use a package manager.
2. Aspose.PSD for Java Library: You’ll need to download and include the Aspose.PSD for Java library in your project. Get it from the [Aspose releases page](https://releases.aspose.com/psd/java/).
3. IDE: Use an Integrated Development Environment (IDE) like IntelliJ IDEA, Eclipse, or any Java IDE of your choice for better code handling.
4. A PSD File: For this tutorial, you'll need a PSD file to work on. You can create one in Adobe Photoshop or download a sample PSD.
5. Basic Java Knowledge: Familiarity with Java syntax will help you follow along with ease.
## Import Packages
Now that you have all the prerequisites set up, the next step is to import the necessary packages. This step is crucial for gaining access to the classes and methods we'll be utilizing. Below is an example of how to import the required packages in your Java project:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```
With these imports, you’re all set to dive into manipulating PSD files!

## Step 1: Set Up Your Source and Output Directories
Before we load any files, let's designate where our input PSD file is coming from and where we want to save the modified file. Adjust the directory paths according to your local machine.
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```
## Step 2: Load the PSD File
Time to load the PSD file! For this, we’ll use the `Image.load` method from the Aspose.PSD library. This method allows us to open the PSD file and access its layers and resources.
```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```
It's like opening a book—you’ll be able to browse through its pages (layers and resources).
## Step 3: Locate the Vsms Resource in the Layer
Next up, we need to find the specific VsmsResource in our PSD file. These resources hold the data for vector shape layers. This is where the magic happens! In this snippet, we loop through the layer's resources to find this resource.
```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```
Like a treasure hunt, you're searching through layers to find the valuable vector data!
## Step 4: Access Length Records
Once we have the VsmsResource, we can extract the LengthRecord objects. Each LengthRecord represents a path within the vector shapes. Here, we access three LengthRecords to manipulate their properties.
```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```
It’s like choosing which parts of a painting you want to retouch!
## Step 5: Modify Path Operation Properties
Now comes the fun part—modifying the path properties! Here, the setPathOperations method allows for changing how the shapes interact with one another. We can set operations like excluding overlapping areas or subtracting the front shape from the back.
```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```
Picture it as adjusting the layers of a cake—each layer interacts differently based on how you slice it!
## Step 6: Save the Modified PSD File
After making the required changes, the next step is to save your modified PSD file. This is where all your hard work pays off. 
```java
psdImage.save(outPsdFilePath);
```
Your masterpiece is now packaged neatly for the world to see!
## Step 7: Clean Up Resources
Finally, it’s critical to dispose of the objects you’ve used to free up memory and resources.
```java
psdImage.dispose();
```
Think of it as cleaning up your workspace after an art project—ensuring everything is neat and tidy!
## Conclusion
There you have it! You’ve just completed a comprehensive tutorial on supporting length record data properties in PSD files using Aspose.PSD for Java. From loading the file to modifying shape properties and saving the final product—each step unveils the power of this library. Whether you're working on creative projects or automating graphic assets, Aspose.PSD opens up a whole new world of possibilities. Ready to get started? Dive into your PSD files and unleash your creativity!
## FAQ's
### What is Aspose.PSD for Java?
Aspose.PSD for Java is a library that allows developers to manipulate and work with Photoshop PSD files programmatically using Java.
### Can I use Aspose.PSD in a free project?
Yes, you can try the library for free using a trial version available on the Aspose website.
### What types of modifications can I make to PSD files?
You can manipulate layers, shapes, texts, path operations, and much more within PSD files.
### Is Aspose.PSD compatible with other programming languages?
Yes, Aspose offers various libraries for different programming languages, including .NET and Python.
### Where can I find the documentation for Aspose.PSD?
You can access the complete documentation [here](https://reference.aspose.com/psd/java/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
