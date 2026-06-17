---
title: Support Length Record Properties – Modify PSD Vector Shapes (Java)
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
description: Learn how to support length record properties and batch process PSD files using Aspose.PSD for Java. Step‑by‑step guide with code examples.
weight: 14
url: /java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
date: 2026-02-20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Support Length Record Properties – Modify PSD Vector Shapes (Java)

## Introduction
If you need to **modify PSD vector shapes** programmatically, the Aspose.PSD for Java library gives you full control over Photoshop files right from your Java code. In this tutorial we’ll walk through everything you need to know to **support length record properties**—an essential step when you want to edit vector shape layers. By the end, you’ll be able to open a PSD, tweak its vector shape properties, and save the updated file without ever leaving your IDE. Let’s dive in!

## Quick Answers
- **What does “modify PSD vector shapes” mean?** Adjusting the geometry, path operations, or other properties of vector‑based layers inside a PSD file.  
- **Which library handles this?** Aspose.PSD for Java.  
- **Do I need a license?** A free trial works for evaluation; a commercial license is required for production.  
- **How long does the implementation take?** Around 10‑15 minutes for a basic shape‑modification script.  
- **What are the main prerequisites?** Java JDK, Aspose.PSD for Java, and a sample PSD file.

## What is “support length record properties”?
Supporting length record properties means accessing and updating the `LengthRecord` objects that describe each vector path inside a PSD. Changing these records lets you control how shapes combine, intersect, or subtract from one another.

## Why use Aspose.PSD for Java to support length record properties?
- **No Photoshop required** – work directly with PSD files on any server.  
- **Rich API** – access layers, resources, and vector data with strongly typed classes.  
- **Cross‑platform** – run on Windows, Linux, or macOS with any JDK.  
- **Performance‑focused** – efficient memory handling and fast save operations.  

## Prerequisites
1. **Java Development Kit (JDK)** – download from [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) or use your preferred package manager.  
2. **Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.  
4. **A PSD file** – create one in Photoshop or grab a sample PSD to experiment with.  
5. **Basic Java knowledge** – familiarity with classes, objects, and exception handling.

## Import Packages
First, import the classes you’ll need to work with PSD files and vector shape resources.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Step 1: Set Up Your Source and Output Directories
Define where the original PSD lives and where you want the modified file to be saved.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Step 2: Load the PSD File
Use `Image.load` to open the file and cast it to `PsdImage` for PSD‑specific features.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Step 3: Locate the Vsms Resource in the Layer
Vector shape data lives inside a `VsmsResource`. Loop through the second layer’s resources to find it.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Step 4: Access Length Records
Each `LengthRecord` represents a distinct vector path. Grab the ones you intend to modify.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Step 5: Modify Path Operation Properties
Now you can **modify PSD vector shapes** by changing their `PathOperations`. This determines how shapes interact (e.g., exclusion, intersection, subtraction).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Step 6: Save the Modified PSD File
Persist your changes to a new file.

```java
psdImage.save(outPsdFilePath);
```

## Step 7: Clean Up Resources
Dispose of the `PsdImage` to free memory.

```java
psdImage.dispose();
```

## How to batch process PSD files with support length record properties
If you need to apply the same vector‑shape adjustments to many PSDs, wrap the code above in a loop that iterates over a directory of files. Update `inPsdFilePath` and `outPsdFilePath` for each iteration, and you’ll be able to **batch process PSD files** efficiently.

## Common Pitfalls & Tips
- **Null checks** – always verify `resource` isn’t `null` before accessing paths.  
- **Path index bounds** – ensure the indices you use (`[2]`, `[7]`, `[11]`) exist for the specific PSD you’re editing.  
- **License** – running without a valid license will embed a watermark in the saved PSD.  

## Conclusion
You now have a complete, end‑to‑end example of how to **modify PSD vector shapes** by supporting length record properties with Aspose.PSD for Java. Whether you’re automating asset pipelines or building a custom design tool, these APIs give you the flexibility to manipulate vector layers without manual Photoshop work. Explore further by experimenting with other `PathOperations` or combining multiple `LengthRecord` edits for complex shapes.

## Frequently Asked Questions

**Q: How do I handle a PSD that contains no vector shape layers?**  
A: The `VsmsResource` will be absent, so `resource` will stay `null`. Add a check and skip the modification step or inform the user.

**Q: Can I change other properties like fill color or stroke width?**  
A: Yes, `LengthRecord` provides additional setters for fill, stroke, and opacity. Refer to the API docs for full details.

**Q: Is it possible to batch‑process multiple PSD files?**  
A: Absolutely. Wrap the code inside a loop that iterates over a directory of PSD files, adjusting the input and output paths each time.

**Q: Do I need to close streams manually when loading from a file path?**  
A: The `Image.load` method handles file streams internally, but if you load from an `InputStream`, remember to close it after use.

**Q: What version of Aspose.PSD is required for these APIs?**  
A: The `LengthRecord` and `PathOperations` classes are available since Aspose.PSD 20.10. Using the latest version is recommended.

---

**Last Updated:** 2026-02-20  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}