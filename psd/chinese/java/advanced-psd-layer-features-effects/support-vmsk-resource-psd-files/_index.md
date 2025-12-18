---
date: 2025-12-18
description: 学习如何使用 Aspose.PSD for Java 在 PSD 文件中创建矢量蒙版（Vmsk 资源）。本分步教程展示了如何添加矢量蒙版、将
  PSD 转换为 PNG 等操作。
linktitle: Create Vector Mask (Vmsk Resource) in PSD Files with Java
second_title: Aspose.PSD Java API
title: 使用 Java 在 PSD 文件中创建矢量蒙版（Vmsk 资源）
url: /zh/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Java 在 PSD 文件中创建矢量蒙版 (Vmsk 资源)

## Introduction
如果您需要在 Photoshop (PSD) 文件中 **创建矢量蒙版** (Vmsk) 资源，Aspose.PSD for Java 为您提供了一种简洁的编程方式。无论是构建设计自动化工具，还是为现有图形流水线添加自定义蒙版支持，本教程都会一步步演示——加载 PSD、读取 Vmsk 资源、修改属性并保存结果。完成后，您将能够熟练处理矢量蒙版、将 PSD 转换为 PNG，以及在文件中扩展其他矢量数据。

## Quick Answers
- **What is a Vmsk resource?** It’s the vector mask data stored inside a PSD file, defining complex vector shapes for a layer.  
- **Which library supports it?** Aspose.PSD for Java provides full read/write access to Vmsk resources.  
- **Do I need a license?** A free trial is available; a commercial license is required for production use.  
- **Can I convert the edited PSD to PNG?** Yes—once saved, you can load the PSD and export to PNG with the same API.  
- **Is Maven support available?** Absolutely; Aspose.PSD can be added as a Maven dependency (see “aspose psd maven” keyword).

## What is a Vector Mask (Vmsk Resource)?
A vector mask (Vmsk) is a non‑pixel‑based mask that uses Bézier curves and path records to define transparent and opaque regions on a layer. Because it’s vector‑based, it scales without quality loss—perfect for high‑resolution graphics.

## Why Create a Vector Mask with Aspose.PSD?
- **Automation:** Programmatically add or modify masks without opening Photoshop.  
- **Consistency:** Ensure every PSD you generate follows the same mask rules.  
- **Cross‑platform:** Works on any OS that supports Java.  
- **Integration:** Combine with other Aspose APIs (e.g., convert PSD → PNG) for end‑to‑end workflows.

## Prerequisites
Before we dive into the code, make sure you have the following:

### What You Need
- Java Development Kit (JDK): Make sure you have JDK installed on your machine. If not, you can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).
- Aspose.PSD for Java Library: This is a powerful library for managing PSD files. You can download it from the [Aspose release page](https://releases.aspose.com/psd/java/). For those who want to try before they buy, you can also start with the [free trial](https://releases.aspose.com/).
- An IDE: Any IDE for Java (like IntelliJ IDEA, Eclipse, etc.) will work for this project.

### Setting Up Your Workspace
1. **Create a New Java Project** – Open your preferred IDE and start a fresh project。  
2. **Add the Aspose Library** – After downloading the Aspose JAR, add it to your project’s build path so you can access all the PSD‑related classes。

With the environment ready, let’s jump into the actual implementation。

## How to create vector mask in PSD files with Java
Below is a step‑by‑step guide. The code blocks are unchanged from the original tutorial; we only added explanatory text to make each step crystal clear。

## Import Packages
Before we can work on PSD files, we need to import the necessary classes from the Aspose.PSD library。

```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```

Now that we’ve set the stage, let’s walk through each operation。

## Step 1: Load Your PSD File
The first thing you want to do is load your PSD file. This is where all the magic begins。

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- We set the `dataDir` to the directory of your PSD file。  
- We create a string for the `sourceFileName`, combining the directory with the PSD file's name。  
- Finally, we load the PSD file into a `PsdImage` object using `Image.load()`。

## Step 2: Retrieve the Vmsk Resource
Now that we have our PSD image loaded, let's fetch the Vmsk resource。

```java
VmskResource resource = getVmskResource(im);
```

- We call the `getVmskResource()` method which handles searching and retrieving the Vmsk resource from the image。

## Step 3: Validate Vmsk Resource Properties
Before proceeding with modifications, it’s essential to validate that our Vmsk resource is in the expected state。

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Here, we’re checking various properties of the Vmsk resource. We want to ensure it’s not disabled, inverted, or not linked, and that it has the right number of paths。

## Step 4: Access Each Path and Validate
Let’s dig a little deeper and inspect the paths within the Vmsk resource。

```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- We’re extracting three specific path records and validating their types and properties to ensure they meet our criteria。

## Step 5: Edit the Vmsk Resource
Now we’re getting into the modification part! You can tweak the properties of the Vmsk resource as needed。

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- In this block, we’re toggling various properties of the Vmsk resource. By setting them to `true`, we can control how the mask behaves in the PSD file。

## Step 6: Modify the Bezier Knot Points
Bezier knots are critical for vector paths. Let’s change some values here。

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- We’re accessing specific `BezierKnotRecord` paths and changing their points to potentially reshape the vector mask。

## Step 7: Save the Modified PSD File
Once all edits are completed, it’s time to save the modified PSD file。

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- We set the path for the exported PSD file and then call `im.save()` to write the changes to this new file。

## Step 8: Clean Up Resources
Finally, we need to ensure that we properly dispose of the image to free up resources。

```java
im.dispose();
```

- It’s always a good practice to dispose of any resources once you’re done. This helps to avoid memory leaks in your applications。

## Conclusion
Congratulations! You’ve just stepped through a detailed process of **creating vector mask** (Vmsk) resources in PSD files using Aspose.PSD for Java. From loading the image, retrieving and validating the Vmsk resource, editing its properties, to saving your modified PSD, you now have a solid foundation for automating vector mask workflows. Use these techniques to enrich your design pipelines, integrate with other Aspose APIs (like converting PSD to PNG), or build custom graphics tools。

## FAQ's
### What is a Vmsk resource?
A Vmsk resource is a vector mask in a PSD file that allows for complex vector shapes and editing features。

### Can I use Aspose.PSD in a Maven project?
Yes, you can include Aspose.PSD as a dependency in your Maven project using its coordinates from the repository。

### What format can I save my modified PSD files in?
You can save them back as PSD files or export them to other formats like PNG, JPEG, etc。

### Is there a free trial available for Aspose.PSD?
Yes, you can access a free trial of Aspose.PSD to test its features. Visit the [free trial link](https://releases.aspose.com/)。

### How can I get support for Aspose.PSD?
You can join the [Aspose forum](https://forum.aspose.com/c/psd/34) for support and troubleshooting help。

## Frequently Asked Questions
**Q: How do I add a new vector mask to an existing layer?**  
A: Create a `VmskResource`, populate it with the required path records (e.g., `BezierKnotRecord`), and attach it to the layer’s resources collection。

**Q: Can I convert the edited PSD directly to PNG without opening Photoshop?**  
A: Yes—after saving the PSD, load it again with `Image.load()` and call `im.save("output.png")` specifying the PNG format。

**Q: Is there a way to automate this in a CI/CD pipeline?**  
A: Absolutely. Since the process is pure Java, you can embed it in Maven/Gradle builds, Docker containers, or any CI system that supports Java。

**Q: What versions of Aspose.PSD are compatible with Java 11+?**  
A: All recent releases (2024‑2025) support Java 8 and above, including Java 11, 17, and newer LTS versions。

**Q: Do I need a license for development builds?**  
A: A free evaluation license works for development and testing. For production deployments, a commercial license is required。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

---