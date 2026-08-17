---
date: 2026-03-13
description: Naučte se, jak přidat vrstvu odstínu a sytosti do souborů PSD pomocí
  Aspose.PSD pro Javu. Tento průvodce také ukazuje, jak hromadně zpracovávat soubory
  PSD a programově vytvářet vrstvu úpravy odstínu.
linktitle: Add Hue Saturation Layer to PSD
second_title: Aspose.PSD Java API
title: Přidat vrstvu odstínu a sytosti do PSD pomocí Aspose.PSD pro Javu
url: /cs/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Přidat vrstvu odstínu a sytosti do PSD

## Introduction
Když jde o grafický design, manipulace s barvami hraje klíčovou roli – konkrétně úprava odstínu, sytosti a jasu může zásadně změnit náladu a kvalitu jakéhokoli obrázku. Jedním účinným způsobem, jak toho dosáhnout, je použití úpravných vrstev ve Photoshopu (soubory PSD). Pokud chcete programově **add hue saturation layer** pomocí Javy, knihovna Aspose.PSD je zde, aby vám pomohla! Tento tutoriál vás provede kroky, jak přidat vrstvu úpravy Hue Saturation do vašich PSD souborů, což učiní váš pracovní postup produktivnějším a efektivnějším.

## Quick Answers
- **What library lets you add a hue saturation layer in Java?** Aspose.PSD for Java.  
- **Do I need Photoshop installed?** No, the library works independently of Photoshop.  
- **Can I batch process PSD files with this approach?** Yes—once you automate the steps you can apply them to many files.  
- **Which Java version is required?** JDK 8 or later.  
- **Is a license needed for production use?** Yes, a commercial license is required after the trial period.

## What is an “add hue saturation layer” operation?
An **add hue saturation layer** operation creates a non‑destructive adjustment layer that lets you modify hue, saturation, and lightness values without altering the original pixel data. This is ideal for fine‑tuning colors across an entire composition or specific color ranges.

## Why use Aspose.PSD for Java?
- **No Photoshop dependency** – works on any platform that runs Java.  
- **Full PSD fidelity** – preserves all layer information, masks, and effects.  
- **Batch‑ready** – you can loop through folders and apply the same adjustment to dozens of files.  
- **Performance‑focused** – optimized for large documents and server‑side automation.

## Prerequisites
Než se pustíme do kódu, ujistěte se, že máte připraveno následující:

1. **Java Development Kit (JDK):** Ensure you have JDK 8 or above installed on your machine. You can download it from the [Java SE Development Kit Downloads](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java Library:** You’ll need to have the Aspose.PSD library, which you can [download here](https://releases.aspose.com/psd/java/).  
3. **IDE:** A suitable Integrated Development Environment (IDE) like IntelliJ IDEA or Eclipse for Java development.  
4. **Basic Java Knowledge:** Familiarity with Java programming is a plus, but don’t worry—we’ll walk you through each line.

Now that we have our prerequisites sorted, let's move on to the fun part—coding!

## Import Packages
To start working with the Aspose.PSD library, the first step is to import the necessary classes. Here’s how you can do it in your Java file:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```

Make sure that you have the appropriate libraries added to your project so that these imports work seamlessly.

## Step 1: Set Up Your Document Directory
Every project needs a starting point, and ours is no exception. You need to specify a directory where your PSD files are stored. This is crucial for loading and saving images properly.

```java
String dataDir = "Your Document Directory"; // Update this path to your actual directory
```

## Step 2: Load an Existing PSD File
To manipulate an existing PSD file, we first need to load it into our program. Here’s how you can do that:

```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

In this code, update `"HueSaturationAdjustmentLayer.psd"` to the name of your existing PSD file that you want to edit.

## Step 3: Edit the Hue/Saturation Layer
Next, we’ll loop through the layers of our loaded PSD image to find and edit any existing Hue/Saturation layers. This step involves modifying the hue, saturation, and lightness values.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```

In this example:  
- We're adjusting the hue to **-25**, saturation to **-12**, and lightness to **+67**.  
- The `getRange(2)` method allows us to tweak specific color ranges as desired.

## Step 4: Save the Modified PSD File
After making adjustments, the next step is to save the file. This is a vital part of our process, ensuring that the changes we’ve made are not lost.

```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```

## Step 5: Add a New Hue/Saturation Layer
If you need to **create hue adjustment layer** from scratch, you can add a brand‑new Hue/Saturation adjustment layer to another PSD file. Follow the same loading pattern but use the `addHueSaturationAdjustmentLayer()` method.

```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```

## Step 6: Set New Hue/Saturation Values for the New Layer
Now that you’ve created this new layer, apply the desired hue, saturation, and lightness settings just like before.

```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```

## Step 7: Save the Updated PSD File
Finally, save the PSD file with the added Hue/Saturation layer so you can see your changes.

```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```

Congratulations! You’ve successfully manipulated PSD files using Aspose.PSD for Java. Now you can experiment with different images and deeper alterations, bringing your graphic design projects to life.

## How to batch process PSD files with hue adjustments
Because the code above is fully scriptable, you can wrap the entire sequence in a loop that iterates over every `.psd` file in a folder. This enables you to **batch process psd files** and apply the same hue, saturation, and lightness tweaks in a single run—perfect for large‑scale branding updates.

## Common Issues and Solutions
- **NullPointerException when loading a file:** Verify that `dataDir` ends with the appropriate file‑separator (`/` or `\`) and that the file name is correct.  
- **Adjustment values out of range:** Hue, saturation, and lightness accept values from -255 to 255. Keep your numbers within this range.  
- **Layer not found:** If the PSD has no Hue/Saturation layer, the `instanceof` check will skip the block. Use `addHueSaturationAdjustmentLayer()` to create one first.

## Frequently Asked Questions

**Q: What is a Hue Saturation Adjustment Layer?**  
A: It allows you to modify the color properties of an image without permanently altering the original pixels.

**Q: Do I need Photoshop installed to use Aspose.PSD?**  
A: No, Aspose.PSD is a standalone library that works independently of Photoshop.

**Q: Can I use Aspose.PSD for batch processing?**  
A: Yes, you can automate and batch process multiple PSD files with Aspose.PSD.

**Q: Is Aspose.PSD free?**  
A: Aspose.PSD offers a free trial, but a license is required for long‑term use. You can view pricing [here](https://purchase.aspose.com/buy).

## Conclusion
Working with graphics programmatically opens up a world of possibilities. Using Aspose.PSD for Java to **add hue saturation layer** and to **create hue adjustment layer** provides flexibility and efficiency that can streamline your design workflow. Whether you’re enhancing photos for a project or creating stunning visual content, mastering these tools can greatly improve your output.

Feel free to explore more functionalities of Aspose.PSD by diving into [documentation](https://reference.aspose.com/psd/java/) or consider snagging a [temporary license](https://purchase.aspose.com/temporary-license/) to test out the full power of the library.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose