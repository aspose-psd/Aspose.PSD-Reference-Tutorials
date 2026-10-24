---
date: 2026-10-24
description: เรียนรู้วิธีสร้างเลเยอร์เส้นขอบใน Java ด้วย Aspose.PSD for Java คู่มือขั้นตอนนี้จะแสดงวิธีเพิ่มเลเยอร์เส้นขอบ,
  เปลี่ยนสี, ปรับความโปร่งแสง, และบันทึกไฟล์ PSD
keywords:
- create stroke layer java
- change stroke color java
- modify stroke opacity
- apply stroke effect
- psd stroke tutorial
lastmod: 2026-10-24
linktitle: เพิ่มสีเลเยอร์เส้นขอบ
og_description: สร้างเลเยอร์เส้นขอบใน Java ด้วย Aspose.PSD for Java. ปฏิบัติตามบทแนะนำสั้นนี้เพื่อเพิ่มเลเยอร์เส้นขอบ,
  เปลี่ยนสี, ปรับความโปร่งแสง, และส่งออกไฟล์ PSD
og_image_alt: Screenshot of a Java IDE showing Aspose.PSD code that creates and modifies
  a stroke layer in a PSD file
og_title: สร้างเลเยอร์เส้นขอบใน Java ด้วย Aspose.PSD – คู่มือเร็ว
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to create stroke layer Java with Aspose.PSD for Java. This
    step‑by‑step guide shows you how to add a stroke layer, change its color, adjust
    opacity, and save the PSD.
  headline: How to create stroke layer Java using Aspose.PSD
  type: TechArticle
- description: Learn how to create stroke layer Java with Aspose.PSD for Java. This
    step‑by‑step guide shows you how to add a stroke layer, change its color, adjust
    opacity, and save the PSD.
  name: How to create stroke layer Java using Aspose.PSD
  steps:
  - name: set up your project
    text: Create a new Java project, add the Aspose.PSD JAR to the build path, and
      verify the library loads without errors.
  - name: load the PSD file
    text: Enable loading of effect resources so the stroke information is available.
  - name: access the stroke effect layer
    text: '`StrokeEffect` is Aspose.PSD’s class that represents a vector outline applied
      to a layer. Retrieve the first stroke effect from the second layer (index 1).'
  - name: validate stroke properties
    text: '`ColorFillSettings` holds the color and opacity values for a stroke. Confirm
      the existing properties before making changes to avoid unexpected results.'
  - name: set color and opacity (how to change stroke color)
    text: Here we **change stroke color** to yellow and reduce opacity to 50 % (127
      / 255). `ColorFillSettings` also lets you specify blend mode and size.
  - name: save the modified PSD
    text: Write the updated image back to disk. The new file now contains the modified
      stroke.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD can be combined with libraries such as Apache Commons
      Imaging or Java2D for extended functionality.
    question: Can I use Aspose.PSD with other Java graphic libraries?
  - answer: Absolutely. The library supports the newest Photoshop specifications and
      over 150 PSD features.
    question: Is Aspose.PSD compatible with the latest PSD file format?
  - answer: Wrap your code in try‑catch blocks and consult the [support forum](https://forum.aspose.com/c/psd/34)
      for detailed troubleshooting examples.
    question: How do I handle exceptions while using Aspose.PSD?
  - answer: Certainly! Grab a [free trial](https://releases.aspose.com/) to explore
      all features.
    question: Can I try Aspose.PSD before purchasing?
  - answer: Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      to evaluate the library in your development environment.
    question: Where can I get a temporary license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create stroke layer
- Aspose.PSD
- Java image processing
title: วิธีสร้างเลเยอร์เส้นขอบใน Java ด้วย Aspose.PSD
url: /th/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีสร้างชั้นเส้นขอบใน Java ด้วย Aspose.PSD

## บทนำ

หากคุณต้องการ **create stroke layer Java** ในเอกสาร Photoshop อย่างอัตโนมัติ Aspose.PSD for Java จะมอบวิธีการที่สะอาดและเน้นโค้ดเป็นหลัก ในบทเรียนนี้คุณจะได้เรียนรู้วิธีเพิ่มชั้นเส้นขอบใหม่, เปลี่ยนสี, ปรับความทึบแสง, และบันทึกผลลัพธ์—ทั้งหมดโดยไม่ต้องเปิด Photoshop เมื่อเสร็จสิ้นคุณจะทราบวิธีแก้ไขเส้นขอบของชั้นที่มีอยู่แล้ว ทำให้คุณควบคุมการสร้างสรรค์ได้เต็มที่จากแอปพลิเคชัน Java ของคุณ

## คำตอบอย่างรวดเร็ว
- **ไลบรารีที่ต้องการคืออะไร?** Aspose.PSD for Java (latest version).  
- **ฉันสามารถเปลี่ยนสีเส้นขอบได้หรือไม่?** Yes – use `ColorFillSettings` to set any `Color`.  
- **ฉันต้องการใบอนุญาตหรือไม่?** A temporary license works for evaluation; a full license is required for production.  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Java 8 or higher.  
- **การดำเนินการใช้เวลานานเท่าไหร่?** Typically under 10 minutes for a basic stroke change.

## ชั้นเส้นขอบใน PSD คืออะไร

ชั้นเส้นขอบเป็นเอฟเฟกต์เวกเตอร์ที่วาดเส้นรอบขอบของเนื้อหาในชั้นหนึ่ง สามารถปรับแต่งได้ด้วยสี, ความหนา, ความทึบแสง, และโหมดการผสม การแก้ไขเอฟเฟกต์นี้โดยโปรแกรมช่วยให้ทำแบรนด์อัตโนมัติ, การประมวลผลเป็นชุด, หรือการสร้างกราฟิกแบบไดนามิกได้

## ทำไมต้องใช้ Aspose.PSD เพื่อเปลี่ยนสีเส้นขอบ

Aspose.PSD รองรับ **150+** ฟีเจอร์ของ PSD—including vector masks, smart objects, and layer effects—while processing multi‑hundred‑page files without loading the entire document into memory. ไลบรารีทำงานบน OS ใดก็ได้ที่มี JVM, ให้ประสิทธิภาพระดับใต้หนึ่งวินาทีสำหรับแอสเซ็ตทั่วไป, และไม่ต้องติดตั้ง Photoshop

## วิธีสร้างชั้นเส้นขอบใน Java?

โหลด PSD, เพิ่มเอฟเฟกต์เส้นขอบ, กำหนดลักษณะการแสดงผล, แล้วบันทึกไฟล์—ทั้งหมดในไม่กี่บรรทัดที่เรียบง่าย คำตอบด้านล่างบอกคุณอย่างชัดเจนก่อนที่เราจะลงลึกในขั้นตอนทีละขั้นตอน

**Direct answer (40‑70 words):**  
`PsdImage` represents a PSD document and provides methods to load and save files. Start by loading your PSD with `PsdImage.load("input.psd", loadOptions)`. Create a new `StrokeEffect`, set its `ColorFillSettings` to the desired `Color`, adjust opacity and size, then attach the effect to the target layer’s `BlendingOptions`. Finally, call `psd.save("output.psd", SaveFormat.PSD)`. This sequence creates a stroke layer in Java with Aspose.PSD.

### ข้อกำหนดเบื้องต้น

- **Aspose.PSD library** – ดาวน์โหลดจาก [เอกสารอย่างเป็นทางการ](https://reference.aspose.com/psd/java/).  
- **Java Development Kit (JDK)** – version 8 or newer.  
- **IDE** – Eclipse, IntelliJ IDEA, or any Java‑compatible editor.

### นำเข้าชุดแพ็กเกจ

First, import the classes you’ll need. This gives your project access to the PSD handling and stroke‑effect APIs.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

### ขั้นตอนที่ 1: ตั้งค่าโปรเจกต์ของคุณ

Create a new Java project, add the Aspose.PSD JAR to the build path, and verify the library loads without errors.

### ขั้นตอนที่ 2: โหลดไฟล์ PSD

Enable loading of effect resources so the stroke information is available.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### ขั้นตอนที่ 3: เข้าถึงชั้นเอฟเฟกต์เส้นขอบ

`StrokeEffect` is Aspose.PSD’s class that represents a vector outline applied to a layer. Retrieve the first stroke effect from the second layer (index 1).

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

### ขั้นตอนที่ 4: ตรวจสอบคุณสมบัติของเส้นขอบ

`ColorFillSettings` holds the color and opacity values for a stroke. Confirm the existing properties before making changes to avoid unexpected results.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

### ขั้นตอนที่ 5: ตั้งค่าสีและความทึบแสง (วิธีเปลี่ยนสีเส้นขอบ)

Here we **change stroke color** to yellow and reduce opacity to 50 % (127 / 255). `ColorFillSettings` also lets you specify blend mode and size.

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

### ขั้นตอนที่ 6: บันทึก PSD ที่แก้ไขแล้ว

Write the updated image back to disk. The new file now contains the modified stroke.

```java
im.save(exportPath);
```

## วิธีเปลี่ยนสีเส้นขอบใน Java?

`Color` represents an ARGB color value. Load your PSD, locate the target layer, update the `ColorFillSettings` with a new `Color`, and save the file. This operation requires only a few lines of code and completes in under a second for typical assets, making it fast and efficient.

**Direct answer (40‑70 words):**  
Use `layer.getEffects().getStrokeEffect()` to obtain the existing stroke, call `stroke.getColorFillSettings().setColor(Color.getRed())` (or any `Color` you need), optionally adjust `setOpacity((byte)200)` for 78 % opacity, then save the PSD with `psd.save("output.psd", SaveFormat.PSD)`. The change is applied instantly without re‑rendering the whole document.

## วิธีแก้ไขความทึบแสงของเส้นขอบ

If you only need to adjust the opacity while keeping the original color, change the `setOpacity` value (0‑255) on the `ColorFillSettings`. For example, `colorStroke.setOpacity((byte)200);` will make the stroke roughly 78 % opaque. Adjusting opacity lets you create subtle outlines or fully solid strokes, depending on your design requirements.

**Direct answer (40‑70 words):**  
Retrieve the `StrokeEffect` from the desired layer, then call `stroke.getColorFillSettings().setOpacity((byte)desiredValue)`, where `desiredValue` ranges from 0 (transparent) to 255 (fully opaque). Save the PSD and the new opacity is reflected immediately. This approach works for any existing stroke, regardless of its original color.

## วิธีใช้เอฟเฟกต์เส้นขอบ

To add a new stroke effect to a layer that doesn’t already have one, create a `StrokeEffect` instance, configure its `ColorFillSettings`, and attach it to the layer’s `BlendingOptions`. The same `setColor` and `setOpacity` methods are used to define appearance overall.

**Direct answer (40‑70 words):**  
Instantiate `StrokeEffect newStroke = new StrokeEffect(); newStroke.getColorFillSettings().setColor(Color.getBlue()); newStroke.getColorFillSettings().setOpacity((byte)255); layer.getBlendingOptions().setEffect(newStroke);`. After attaching the effect, save the PSD. This adds a fresh, fully‑customizable stroke layer to any existing layer in your document.

## กรณีการใช้งานทั่วไปสำหรับการเปลี่ยนสีเส้นขอบ
- **Branding automation:** Apply a corporate color to logos across hundreds of PSD assets in a single batch run.  
- **Dynamic UI generation:** Change stroke colors on the fly based on user‑selected themes in a web‑based design tool.  
- **Pre‑flight preparation:** Ensure all stroke colors meet print specifications before sending files to a press.

## ข้อผิดพลาดทั่วไปและเคล็ดลับ

- **Null checks** – always verify that `getEffects()` returns a non‑null array before casting.  
- **Layer index** – PSD layers are zero‑based; ensure you target the correct layer.  
- **Color format** – `Color.getYellow()` is just an example; you can create custom colors with `new Color(r, g, b)`.  
- **Opacity range** – opacity is a byte (0–255); values above 255 will be clamped.  
- **Resource loading** – forgetting `loadOptions.setLoadEffectsResource(true)` will result in a `null` effects array.

## คำถามที่พบบ่อย

**Q: ฉันสามารถใช้ Aspose.PSD กับไลบรารีกราฟิก Java อื่นได้หรือไม่?**  
**A:** Yes, Aspose.PSD can be combined with libraries such as Apache Commons Imaging or Java2D for extended functionality.

**Q: Aspose.PSD รองรับรูปแบบไฟล์ PSD ล่าสุดหรือไม่?**  
**A:** Absolutely. The library supports the newest Photoshop specifications and over 150 PSD features.

**Q: ฉันจะจัดการกับข้อยกเว้นขณะใช้ Aspose.PSD อย่างไร?**  
**A:** Wrap your code in try‑catch blocks and consult the [ฟอรั่มสนับสนุน](https://forum.aspose.com/c/psd/34) for detailed troubleshooting examples.

**Q: ฉันสามารถลองใช้ Aspose.PSD ก่อนซื้อได้หรือไม่?**  
**A:** Certainly! Grab a [ทดลองใช้ฟรี](https://releases.aspose.com/) to explore all features.

**Q: ฉันจะได้รับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้จากที่ไหน?**  
**A:** Obtain a [temporary license](https://purchase.aspose.com/temporary-license/) to evaluate the library in your development environment.

---

**อัปเดตล่าสุด:** 2026-10-24  
**ทดสอบด้วย:** Aspose.PSD 24.11 for Java  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [วิธีเปลี่ยนสีเส้นขอบใน Java ด้วย Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)
- [วิธีเพิ่มเงาใน PSD ด้วย Java – เอฟเฟกต์ชั้นขั้นสูง](/psd/java/advanced-psd-layer-features-effects/)
- [Pattern Overlay PSD: เพิ่มเอฟเฟกต์ด้วย Aspose.PSD สำหรับ Java](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}