---
title: Drawing Ellipses in Java
linktitle: Drawing Ellipses in Java
second_title: Aspose.PSD Java API
description: Learn how to draw ellipses in Java using Aspose.PSD for precise graphic design and image manipulation. Master step-by-step tutorials.
type: docs
weight: 15
url: /java/java-graphics-drawing/drawing-ellipses/
---
## Introduction
In this tutorial, you will learn how to draw ellipses using Aspose.PSD for Java. Aspose.PSD is a powerful library that allows Java developers to work with PSD files and manipulate images with ease. Drawing shapes like ellipses is a fundamental task in image processing and graphic design. By following this guide, you will gain hands-on experience in creating ellipses programmatically using Aspose.PSD.
## Prerequisites
Before you begin, ensure you have the following:
- Basic knowledge of Java programming.
- JDK (Java Development Kit) installed on your system.
- Integrated Development Environment (IDE) such as IntelliJ IDEA or Eclipse.
- Aspose.PSD for Java library. You can download it from [here](https://releases.aspose.com/psd/java/).
## Import Packages
First, you need to import necessary packages from Aspose.PSD:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
## Step 1: Set up your Java project
Before you start coding, make sure your Java project is set up correctly with Aspose.PSD included as a dependency.
## Step 2: Create an instance of PsdImage
Initialize a new instance of PsdImage with desired width and height.
```java
Image image = new PsdImage(100, 100);
```
## Step 3: Initialize Graphics object
Create and initialize an instance of Graphics to work with the image.
```java
Graphics graphics = new Graphics(image);
```
## Step 4: Clear the Graphics surface
Before drawing, clear the graphics surface with a specific color (optional).
```java
graphics.clear(Color.getYellow());
```
## Step 5: Draw a dotted ellipse
Use a Pen object with a red color and draw a dotted ellipse within a specified Rectangle.
```java
graphics.drawEllipse(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
```
## Step 6: Draw a continuous ellipse
Create a Pen object with a solid blue brush and draw a continuous ellipse within another Rectangle.
```java
graphics.drawEllipse(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
```
## Step 7: Save the image
Finally, save the generated image in BMP format to a specified path.
```java
String outputPath = "Your Document Directory/Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

## Conclusion
Congratulations! You have successfully learned how to draw ellipses programmatically using Aspose.PSD for Java. This tutorial covered setting up your project, initializing graphics, drawing dotted and continuous ellipses, and saving the resulting image. Now you can integrate these techniques into your Java applications for various graphic design and image manipulation tasks.
## FAQ's
### Can I use Aspose.PSD for free?
Aspose.PSD offers a free trial version, allowing you to evaluate its features before purchasing.
### Where can I find more examples and documentation?
Visit [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/) for comprehensive guides and examples.
### How can I get temporary licenses for Aspose.PSD?
Temporary licenses can be obtained from [Aspose.PSD Temporary License](https://purchase.aspose.com/temporary-license/).
### What formats can Aspose.PSD save images to?
Aspose.PSD supports saving images to various formats including BMP, PNG, JPEG, and PSD.
### Is Aspose.PSD suitable for enterprise use?
Yes, Aspose.PSD is designed for professional and enterprise-level image processing tasks.
