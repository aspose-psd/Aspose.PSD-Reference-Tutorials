---
date: 2026-04-08
description: เรียนรู้วิธีสร้างเอฟเฟกต์ไล่สีแบบรัศมีในภาพ Java ด้วย Aspose.PSD. ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนนี้เพื่อการผสานรวมที่ราบรื่น.
keywords:
- create radial gradient
- gradient overlay effect
- Aspose.PSD Java
linktitle: เพิ่มเอฟเฟกต์ไล่สี
second_title: Aspose.PSD Java API
title: วิธีสร้างเอฟเฟกต์ไล่สีรัศมีใน Aspose.PSD สำหรับ Java
url: /th/java/advanced-image-effects/add-gradient-effects/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีสร้างเอฟเฟกต์การไล่สีแบบรัศมีใน Aspose.PSD สำหรับ Java

## บทนำ

Welcome to the tutorial on **วิธีสร้างการไล่สีแบบรัศมี** effects in Aspose.PSD for Java! If you're looking to enhance your images with stunning gradient overlays, you're in the right place. In this guide we'll walk you through the process using Aspose.PSD, a powerful Java library for image processing. By the end of this tutorial you’ll be comfortable adding, customizing, and saving radial gradient overlays programmatically.

## คำตอบอย่างรวดเร็ว
- **What can I achieve?** Add, edit, and blend radial gradient overlays on PSD layers.  
- **Which library is required?** Aspose.PSD for Java (latest version).  
- **Do I need a license?** A free trial works for development; a commercial license is required for production.  
- **How long does implementation take?** Roughly 10‑15 minutes for a basic radial gradient overlay.  
- **Is it compatible with Java 8+?** Yes, the API supports Java 8 and newer runtimes.

## ข้อกำหนดเบื้องต้น

Before we dive into the tutorial, make sure you have the following prerequisites in place:

1. **Aspose.PSD for Java Library** – Ensure you have downloaded and installed the Aspose.PSD for Java library. You can find the library and its documentation [ที่นี่](https://reference.aspose.com/psd/java/).  
2. **Java Development Environment** – Set up a Java development environment on your machine (JDK 8 or higher, IDE of your choice).

Now that you have everything set up, let's proceed with the step‑by‑step guide.

## นำเข้าแพ็กเกจ

Start by importing the necessary packages in your Java project. This ensures that you have access to the Aspose.PSD functionality. Here's a basic example:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.*;
import com.aspose.psd.fileformats.psd.layers.layereffects.GradientOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Gradient Overlay Effect คืออะไร?

A **gradient overlay effect** is a layer‑style that paints a smooth transition between two or more colors across a selected area. In Photoshop (and therefore in PSD files), this effect can be blended, colored, and positioned to create sophisticated visual designs. Aspose.PSD exposes this effect through the `GradientOverlayEffect` class, allowing you to read and modify its properties programmatically.

## วิธีสร้างเอฟเฟกต์การไล่สีแบบรัศมี

Below we break the implementation into clear, numbered steps. Each step includes a short explanation followed by the original code block (unchanged).

### ขั้นตอนที่ 1: โหลดไฟล์ PSD และเข้าถึง Gradient Overlay

```javaString dataDir = "Your Document Directory";

// Gradient overlay effect. Example
String sourceFileName = dataDir + "GradientOverlay.psd";
String exportPath = dataDir + "GradientOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlay = (GradientOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

In this step, we load a PSD file and retrieve the first `GradientOverlayEffect` from the second layer (index 1). The `loadOptions.setLoadEffectsResource(true)` call ensures that effect resources are available for editing.

### ขั้นตอนที่ 2: ตรวจสอบการตั้งค่าเริ่มต้น

```java
// Verify initial settings
Assert.areEqual(BlendMode.Normal, gradientOverlay.getBlendMode());
Assert.areEqual(255, gradientOverlay.getOpacity());
Assert.areEqual(true, gradientOverlay.isVisible());
// ... (additional verifications)
```

Before making changes, it’s a good practice to confirm the current blend mode, opacity, and visibility. This helps you understand the baseline state of the gradient overlay.

### ขั้นตอนที่ 3: ปรับแต่งการตั้งค่า Gradient

```java
// Modify gradient settings
settings.setColor(Color.getGreen());
gradientOverlay.setOpacity((byte)193);
gradientOverlay.setBlendMode(BlendMode.Lighten);
// ... (additional modifications)
```

Here you can customize the gradient’s color, opacity, and blend mode. The example changes the color to green, reduces opacity to 193 (out of 255), and switches the blend mode to **Lighten**. Feel free to experiment with other `BlendMode` values such as `Multiply`, `Screen`, or `Overlay`.

### ขั้นตอนที่ 4: บันทึกภาพที่แก้ไขแล้ว

```java
// Save the edited image
im.save(exportPath);
```

After applying your modifications, persist the changes by saving the PSD to a new file. This step ensures the original file remains untouched.

### ขั้นตอนที่ 5: ตรวจสอบการเปลี่ยนแปลง

```java
// Verify changes after editing
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlayEffect = (GradientOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];
// ... (additional verifications)
```

Reload the saved file (or the original, depending on your workflow) and re‑inspect the gradient overlay to confirm that your changes were applied correctly.

## ทำไมต้องสร้าง Radial Gradient Overlays?

Radial gradients add depth and focus to designs, making elements appear three‑dimensional or spotlighted. They’re ideal for:

- **Background fills** that draw the eye toward a central subject.  
- **Button or icon highlights** where a subtle glow is needed.  
- **Creative photo effects** like vignettes or light bursts.  

Using Aspose.PSD lets you automate these effects across many files, saving hours of manual Photoshop work.

## ปัญหาที่พบบ่อยและเคล็ดลับ

- **Effect Not Visible:** Ensure `gradientOverlay.isVisible()` returns `true`. Some PSD files hide effects by default.  
- **Incorrect Layer Index:** Layers are zero‑based; double‑check you are targeting the correct layer (`im.getLayers()[1]` refers to the second layer).  
- **Opacity Casting:** The `setOpacity` method expects a `byte`. Passing an `int` will cause a compilation error; cast explicitly as shown.  
- **Resource Loading:** If you encounter `null` when accessing effects, verify that `loadOptions.setLoadEffectsResource(true)` is set before loading the image.

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้เอฟเฟกต์ไล่สีหลายแบบบนภาพเดียวได้หรือไม่?

A1: Yes, you can apply multiple gradient effects by repeating the modification steps for each effect.

### Q2: มีเอฟเฟกต์อื่น ๆ ที่ฉันสามารถรวมกับ gradient overlays ได้หรือไม่?

A2: Aspose.PSD provides a variety of effects, including shadows, glows, and more. Explore the documentation for more options.

### Q3: ฉันจะแก้ไขปัญหาเมื่อเอฟเฟกต์ไม่แสดงผลอย่างถูกต้องได้อย่างไร?

A3: Check the documentation and community forums at [Aspose.PSD Support](https://forum.aspose.com/c/psd/34) for assistance.

### Q4: มีเวอร์ชันทดลองสำหรับ Aspose.PSD for Java หรือไม่?

A4: Yes, you can get a free trial [ที่นี่](https://releases.aspose.com/).

### Q5: ฉันจะซื้อไลเซนส์สำหรับ Aspose.PSD for Java ได้จากที่ไหน?

A5: Visit the [purchase page](https://purchase.aspose.com/buy) for licensing information.

## คำถามเพิ่มเติม

**Q: ฉันสามารถเปลี่ยนทิศทางของ gradient ได้โดยโปรแกรมหรือไม่?**  
A: Yes. Use the `GradientOverlayEffect.setAngle(float angle)` method to set the gradient angle in degrees.

**Q: Aspose.PSD รองรับ radial gradients หรือไม่?**  
A: Absolutely. Set the gradient style to `GradientStyle.Radial` via the `GradientOverlayEffect` properties.

**Q: Gradient overlays จะคงอยู่เมื่อแปลง PSD ไปเป็นรูปแบบอื่น (เช่น PNG) หรือไม่?**  
A: When you rasterize the PSD (e.g., save as PNG), the visual result of the gradient overlay is retained, but the effect itself becomes part of the pixel data.

**Q: ฉันจะลบ gradient overlay จากเลเยอร์ได้อย่างไร?**  
A: Retrieve the layer’s `BlendingOptions`, locate the `GradientOverlayEffect` in the `Effects` collection, and remove it using `remove(effect)`.

**Q: สามารถทำให้ gradient เปลี่ยนแปลงแบบอนิเมชันได้หรือไม่?**  
A: While Aspose.PSD does not directly handle animation, you can generate a sequence of PSD files with varying gradient parameters and then assemble them into a video or GIF using another library.

## สรุป

Congratulations! You've learned **วิธีสร้างการไล่สีแบบรัศมี** effects to your images using Aspose.PSD for Java. By following the steps above, you can programmatically add, modify, and save gradient overlays, giving you full creative control over PSD assets. Experiment with different colors, blend modes, and opacity values to achieve the visual impact you need.

---

**Last Updated:** 2026-04-08  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}