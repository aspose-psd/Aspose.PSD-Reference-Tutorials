---
date: 2026-04-22
description: เรียนรู้วิธีเปลี่ยนสีเส้นขอบใน Java ด้วย Aspose.PSD for Java ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนนี้เพื่อแก้ไขสีของเลเยอร์เส้นขอบ
  ความทึบแสง และอื่น ๆ อีกมากมาย.
keywords:
- change stroke color java
- modify stroke opacity
- apply stroke effect
- psd stroke tutorial
- add stroke layer psd
linktitle: เพิ่มสีของชั้นเส้นขอบ
second_title: Aspose.PSD Java API
title: วิธีเปลี่ยนสีเส้นขอบใน Java ด้วย Aspose.PSD
url: /th/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีเปลี่ยนสีเส้นขอบใน Java ด้วย Aspose.PSD

## บทนำ

หากคุณต้องการ **change stroke color java** ในเอกสาร Photoshop อย่างโปรแกรมมิ่ง Aspose.PSD for Java ทำให้เรื่องนี้ง่ายขึ้น ในบทแนะนำนี้เราจะอธิบายขั้นตอนการเพิ่มเลเยอร์เส้นขอบ, การเปลี่ยนสี, การปรับความทึบแสง, และการบันทึกผลลัพธ์ เมื่อเสร็จคุณจะเห็นวิธีแก้ไขเส้นขอบของเลเยอร์ที่มีอยู่แล้ว, ให้คุณควบคุมการสร้างสรรค์ทั้งหมดจากโค้ด Java ของคุณ.

## คำตอบสั้น
- **ไลบรารีที่ต้องการคืออะไร?** Aspose.PSD for Java (latest version).  
- **ฉันสามารถเปลี่ยนสีเส้นขอบได้หรือไม่?** Yes – use `ColorFillSettings` to set any `Color`.  
- **ฉันต้องการใบอนุญาตหรือไม่?** A temporary license works for evaluation; a full license is required for production.  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Java 8 or higher.  
- **การดำเนินการใช้เวลานานเท่าไหร่?** Typically under 10 minutes for a basic stroke change.

## Stroke Layer คืออะไรใน PSD?
Stroke layer เป็นเอฟเฟกต์เวกเตอร์ที่วาดเส้นขอบรอบเนื้อหาของเลเยอร์ สามารถปรับแต่งด้วยสี, ความหนา, ความทึบแสง, และโหมดผสม การแก้ไขเอฟเฟกต์นี้โดยโปรแกรมมิ่งทำให้สามารถทำแบรนด์อัตโนมัติ, การประมวลผลเป็นชุด, หรือการสร้างกราฟิกแบบไดนามิกได้

## ทำไมต้องใช้ Aspose.PSD เพื่อเปลี่ยนสีเส้นขอบ?
- **ไม่ต้องใช้ Photoshop** – ทำงานทั้งหมดใน Java.  
- **รองรับสเปค PSD เต็มรูปแบบ** – รองรับคุณลักษณะ PSD สมัยใหม่ทั้งหมด.  
- **ประสิทธิภาพสูง** – ประมวลผลไฟล์ขนาดใหญ่ได้อย่างรวดเร็ว.  
- **ข้ามแพลตฟอร์ม** – ทำงานบน OS ใดก็ได้ที่มี JVM.

## วิธีเปลี่ยนสีเส้นขอบใน Java อย่างโปรแกรมมิ่ง
ด้านล่างเป็นขั้นตอนสั้น ๆ ที่แสดงอย่างชัดเจนว่าจะแก้ไขสีเส้นขอบโดยใช้ Aspose.PSD for Java อย่างไร แต่ละขั้นตอนมีคำอธิบายสั้น ๆ ตามด้วยบล็อกโค้ดต้นฉบับ (ไม่เปลี่ยนแปลง)

### ข้อกำหนดเบื้องต้น

- **Aspose.PSD Library** – download from the [official documentation](https://reference.aspose.com/psd/java/).  
- **Java Development Kit (JDK)** – version 8 or newer.  
- **IDE** – Eclipse, IntelliJ IDEA, or any Java‑compatible editor.

### นำเข้าแพ็กเกจ

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

### ขั้นตอนที่ 3: เข้าถึงเลเยอร์เอฟเฟกต์เส้นขอบ

Retrieve the first stroke effect from the second layer (index 1).

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

### ขั้นตอนที่ 4: ตรวจสอบคุณสมบัติของเส้นขอบ

Confirm the existing properties before making changes. This helps avoid unexpected results.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

### ขั้นตอนที่ 5: ตั้งค่าสีและความทึบแสง (วิธีเปลี่ยนสีเส้นขอบ)

Here we **change stroke color** to yellow and reduce opacity to 50 % (127 / 255).

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

## วิธีแก้ไขความทึบของเส้นขอบ

If you only need to adjust the opacity while keeping the original color, change the `setOpacity` value (0‑255). For example, `colorStroke.setOpacity((byte)200);` will make the stroke roughly 78 % opaque.

## วิธีใช้เอฟเฟกต์เส้นขอบ

To add a new stroke effect to a layer that doesn’t already have one, create a `StrokeEffect` instance, configure its `ColorFillSettings`, and attach it to the layer’s `BlendingOptions`. The same `setColor` and `setOpacity` methods are used to define appearance.

## บทเรียน PSD Stroke: เพิ่มเลเยอร์เส้นขอบลงใน PSD

The steps above illustrate adding a stroke to an existing layer. For a brand‑new stroke layer, duplicate the target layer, then apply the `StrokeEffect`. This approach is useful when you want to keep the original layer untouched.

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
A: Yes, Aspose.PSD can be combined with libraries such as Apache Commons Imaging or Java2D for extended functionality.

**Q: Aspose.PSD รองรับรูปแบบไฟล์ PSD ล่าสุดหรือไม่?**  
A: Absolutely. The library is regularly updated to support the newest Photoshop specifications.

**Q: ฉันจะจัดการกับข้อยกเว้นขณะใช้ Aspose.PSD อย่างไร?**  
A: Refer to the [support forum](https://forum.aspose.com/c/psd/34) for detailed troubleshooting and sample error‑handling code.

**Q: ฉันสามารถลองใช้ Aspose.PSD ก่อนซื้อได้หรือไม่?**  
A: Certainly! Grab a [free trial](https://releases.aspose.com/) to explore all features.

**Q: ฉันจะได้ใบอนุญาตชั่วคราวสำหรับ Aspose.PSD จากที่ไหน?**  
A: Obtain a [temporary license](https://purchase.aspose.com/temporary-license/) to evaluate the library in your development environment.

---

**Last Updated:** 2026-04-22  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}