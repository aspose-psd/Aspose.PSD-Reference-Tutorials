---
title: Convert AI to JPG in Java
linktitle: Convert AI to JPG in Java
second_title: Aspose.PSD Java API
description: Convert AI files to JPG in Java effortlessly with Aspose.PSD. Follow our step-by-step guide for high-quality image conversion.
type: docs
weight: 11
url: /java/java-ai-to-image-format-conversion/convert-ai-to-jpg/
---
## Introduction
Are you looking to convert AI (Adobe Illustrator) files to JPG format using Java? Look no further! In this comprehensive guide, we'll walk you through the entire process using Aspose.PSD for Java, a powerful and flexible library that makes image manipulation a breeze. Whether you're a seasoned developer or just starting, this tutorial will provide you with everything you need to know.
## Prerequisites
Before diving into the code, let's ensure you have everything set up and ready to go. Here’s what you need:
1. Java Development Kit (JDK): Make sure you have JDK 8 or above installed.
2. Aspose.PSD for Java: Download the library from [here](https://releases.aspose.com/psd/java/).
3. Development Environment: An IDE like IntelliJ IDEA, Eclipse, or any text editor of your choice.
4. AI File: An Adobe Illustrator file (.ai) you wish to convert.
5. Basic Java Knowledge: Familiarity with Java programming basics.
## Import Packages
First things first, we need to import the necessary packages to handle our image conversion task. Here’s how you do it:
```java
import com.aspose.psd.Image;
import com.aspose.psd.ImageOptionsBase;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.ai.AiImage;
import com.aspose.psd.imageoptions.JpegOptions;
```
These imports bring in the essential classes for loading AI files and saving them as JPGs.
Let's break down the conversion process into simple, manageable steps. Follow along to transform your AI files into JPGs effortlessly.
## Step 1: Set Up Your Environment
Before we start coding, ensure that your development environment is set up correctly. Make sure you have the Aspose.PSD for Java library added to your project.
- Download and Install JDK: If you haven't already, download and install the JDK from the [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).
- Download Aspose.PSD: Get the library from the [Aspose releases page](https://releases.aspose.com/psd/java/).
- Add Aspose.PSD to Your Project: Include the JAR files in your project's build path.
## Step 2: Load Your AI File
The first step in our code is to load the AI file using the `AiImage` class. This class allows us to work with Adobe Illustrator files seamlessly.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "34992OStroke.ai";
AiImage image = (AiImage) Image.load(sourceFileName);
```
Here, `dataDir` is the directory where your AI file is stored, and `sourceFileName` is the full path to your AI file.
## Step 3: Set JPG Options
Next, we need to set the options for our JPG output. The `JpegOptions` class helps us configure the quality and other settings for the JPG file.
```java
JpegOptions options = new JpegOptions();
options.setQuality(85); // Set the quality of the JPG
```
In this example, we've set the quality to 85, which balances file size and image quality. You can adjust this value based on your requirements.
## Step 4: Save the AI File as JPG
Finally, it's time to save the loaded AI file as a JPG. We use the `save` method of the `AiImage` class for this purpose.
```java
String outFileName = dataDir + "34992OStroke.jpg";
image.save(outFileName, options);
```
This line of code saves the image to the specified directory with the desired quality settings.
## Step 5: Run Your Program
With everything set up, you can now run your Java program. Ensure your IDE or command line points to the correct file paths and class names.
```java
public class AiToJpgConverter {
    public static void main(String[] args) {
        String dataDir = "Your Document Directory";
        String sourceFileName = dataDir + "34992OStroke.ai";
        String outFileName = dataDir + "34992OStroke.jpg";
        AiImage image = (AiImage) Image.load(sourceFileName);
        JpegOptions options = new JpegOptions();
        options.setQuality(85);
        image.save(outFileName, options);
        System.out.println("AI file converted to JPG successfully!");
    }
}
```
Run this class, and you should see your AI file converted to a JPG in the specified directory.
## Conclusion
Converting AI files to JPG in Java is straightforward with the Aspose.PSD library. By following the steps outlined in this guide, you can easily achieve this conversion while controlling the quality of the output image. Aspose.PSD for Java is a powerful tool that offers extensive features for image manipulation, making it a valuable addition to any developer's toolkit.
## FAQ's
### What is Aspose.PSD for Java?
Aspose.PSD for Java is a Java API for working with Photoshop and Illustrator files, offering a wide range of features for manipulating images.
### Can I set different quality levels for the output JPG?
Yes, you can adjust the quality setting in `JpegOptions` to control the output JPG's quality and size.
### Is Aspose.PSD for Java free to use?
Aspose.PSD offers a free trial, but you will need to purchase a license for full functionality. You can obtain a free trial [here](https://releases.aspose.com/).
### Do I need Adobe Illustrator installed to use this library?
No, you do not need Adobe Illustrator installed. Aspose.PSD handles the file formats independently.
### Where can I find more documentation on Aspose.PSD for Java?
You can find comprehensive documentation [here](https://reference.aspose.com/psd/java/).
