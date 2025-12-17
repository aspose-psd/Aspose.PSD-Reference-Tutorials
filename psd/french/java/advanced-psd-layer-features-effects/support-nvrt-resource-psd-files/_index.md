---
date: 2025-12-17
description: Apprenez à charger des fichiers PSD en Java et à lire les calques PSD
  tout en prenant en charge la ressource Nvrt à l'aide d'Aspose.PSD.
linktitle: Support Nvrt Resource in PSD Files using Java
second_title: Aspose.PSD Java API
title: Comment charger des fichiers PSD et prendre en charge les ressources Nvrt avec
  Java
url: /fr/java/advanced-psd-layer-features-effects/support-nvrt-resource-psd-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Support Nvrt Resource in PSD Files using Java

## How to Load PSD Files in Java
When you need to **how to load psd** files programmatically, Java offers a robust ecosystem—especially with the Aspose.PSD library. Whether you're building a graphics editor, automating design pipelines, or extracting assets from Photoshop documents, mastering PSD handling is essential. In this tutorial we’ll walk through loading a PSD, reading its layers, and specifically supporting the Nvrt (Invert Adjustment) resource.

## Quick Answers
- **What library handles PSD files in Java?** Aspose.PSD for Java  
- **Can I read PSD layers?** Yes, the API provides full access to layer structures  
- **Is a license required for production?** Yes, a commercial license is needed  
- **Which JDK version is supported?** Java 8 and higher  
- **Where can I download the library?** From the official Aspose download page  

## Prerequisites
Before you start coding, make sure you have the following:

- **Java Development Kit (JDK)** installed (Java 8+ recommended)  
- **An IDE** such as IntelliJ IDEA, Eclipse, or VS Code  
- **Aspose.PSD for Java** library – download it from the official site: [Download Aspose.PSD for Java](https://releases.aspose.com/psd/java/)  
- **Basic Java knowledge** (classes, objects, exception handling)  

## Import Packages
Once your environment is ready, import the required classes. These give you access to PSD handling, layer traversal, and the Nvrt resource.

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.InvertAdjustmentLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.NvrtResource;
```

## Why Read PSD Layers?
Reading PSD layers lets you:

- Extract individual assets (e.g., icons, masks) for reuse  
- Analyze adjustment layers (like **Nvrt**) to understand image edits  
- Automate batch processing of design files  

## Step 1: Specify Your Source Directory
Set the folder that contains the PSD you want to work with.

```java
String sourceDir = "Your Source Directory";
String inPsdFilePath = sourceDir + "InvertAdjustmentLayer.psd";
```

Replace `"Your Source Directory"` with the actual path on your machine.

## Step 2: Load the PSD File
Now we actually **how to load psd** files using the Aspose API.

```java
PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);
```

The `Image.load()` method opens the file and prepares it for inspection.

## Step 3: Initialize the Nvrt Resource Variable
We’ll store the found Nvrt resource here.

```java
NvrtResource nvrtResource = null;
```

## Step 4: Search for Invert Adjustment Layer
Iterate through each layer, locate an `InvertAdjustmentLayer`, and then look for the `NvrtResource`.

```java
try {
    for (Layer layer : psdImage.getLayers()) {
        if (layer instanceof InvertAdjustmentLayer) {
            for (LayerResource layerResource : layer.getResources()) {
                if (layerResource instanceof NvrtResource) {
                    // The NvrtResource is found
                    nvrtResource = (NvrtResource)layerResource;
                    break;
                }
            }
        }
    }
} finally {
    psdImage.dispose();
}
```

The `finally` block guarantees that the PSD image is disposed, keeping memory usage clean.

## Step 5: Verify the Nvrt Resource
Confirm that the resource was successfully located.

```java
Assert.isNotNull(nvrtResource);
```

If the assertion passes, you’ve successfully read the PSD layers and extracted the Nvrt resource.

## Common Pitfalls & Tips
- **Null checks:** Always verify that `psdImage` and layer objects are not null before accessing them.  
- **Resource disposal:** Forgetting `psdImage.dispose()` can lead to memory leaks in long‑running applications.  
- **File path issues:** Use absolute paths or ensure your working directory is set correctly to avoid `FileNotFoundException`.  

## Conclusion
You now know **how to load psd** files, read their layers, and extract the Nvrt adjustment resource using Java and Aspose.PSD. This foundation lets you build powerful graphics automation tools, batch‑process design assets, or integrate Photoshop data into larger workflows.

## Frequently Asked Questions

**Q: What is Aspose.PSD for Java?**  
A: Aspose.PSD for Java is a library that enables developers to create, edit, convert, and render PSD files directly from Java code.

**Q: Can I use Aspose.PSD in commercial products?**  
A: Yes, a commercial license is required for production use. You can explore purchasing options [here](https://purchase.aspose.com/buy).

**Q: Where can I find the documentation for Aspose.PSD?**  
A: The complete documentation is available here: [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

**Q: Is there a free trial available?**  
A: Absolutely! You can get a free trial of Aspose.PSD for Java [here](https://releases.aspose.com/).

**Q: How can I get support for Aspose.PSD?**  
A: You can ask questions and get support on the Aspose forum: [Aspose Support](https://forum.aspose.com/c/psd/34).

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}