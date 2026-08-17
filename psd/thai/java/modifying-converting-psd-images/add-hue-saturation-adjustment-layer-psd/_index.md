---
date: 2026-03-13
description: เรียนรู้วิธีเพิ่มเลเยอร์ปรับสีและความอิ่มตัวลงในไฟล์ PSD ด้วย Aspose.PSD
  สำหรับ Java คู่มือนี้ยังแสดงวิธีประมวลผลไฟล์ PSD เป็นชุดและสร้างเลเยอร์ปรับสีโดยอัตโนมัติ.
linktitle: Add Hue Saturation Layer to PSD
second_title: Aspose.PSD Java API
title: เพิ่มเลเยอร์ Hue Saturation ไปยังไฟล์ PSD ด้วย Aspose.PSD สำหรับ Java
url: /th/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
weight: 14
---

, preserve code block placeholders as separate lines.

Let's write translation.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เพิ่มเลเยอร์ Hue Saturation ไปยัง PSD

## Introduction
เมื่อพูดถึงการออกแบบกราฟิก การจัดการสีมีบทบาทสำคัญ—โดยเฉพาะการปรับค่า hue, saturation และ lightness สามารถเปลี่ยนบรรยากาศและคุณภาพของภาพได้อย่างมาก วิธีที่มีประสิทธิภาพหนึ่งคือการใช้ adjustment layer ใน Photoshop (ไฟล์ PSD) หากคุณต้องการ **add hue saturation layer** อย่างอัตโนมัติด้วย Java ไลบรารี Aspose.PSD พร้อมช่วยเหลือ! บทแนะนำนี้จะพาคุณผ่านขั้นตอนการเพิ่ม Hue Saturation Adjustment Layer ไปยังไฟล์ PSD ของคุณ ทำให้กระบวนการทำงานของคุณมีประสิทธิภาพและผลิตผลดีขึ้น

## Quick Answers
- **What library lets you add a hue saturation layer in Java?** Aspose.PSD for Java.  
- **Do I need Photoshop installed?** No, the library works independently of Photoshop.  
- **Can I batch process PSD files with this approach?** Yes—once you automate the steps you can apply them to many files.  
- **Which Java version is required?** JDK 8 or later.  
- **Is a license needed for production use?** Yes, a commercial license is required after the trial period.

## What is an “add hue saturation layer” operation?
การดำเนินการ **add hue saturation layer** สร้าง adjustment layer ที่ไม่ทำลายข้อมูลเดิม ทำให้คุณสามารถปรับค่า hue, saturation และ lightness ได้โดยไม่กระทบพิกเซลต้นฉบับ เหมาะสำหรับการปรับสีอย่างละเอียดทั่วทั้งคอมโพสชันหรือในช่วงสีเฉพาะ

## Why use Aspose.PSD for Java?
- **No Photoshop dependency** – works on any platform that runs Java.  
- **Full PSD fidelity** – preserves all layer information, masks, and effects.  
- **Batch‑ready** – you can loop through folders and apply the same adjustment to dozens of files.  
- **Performance‑focused** – optimized for large documents and server‑side automation.

## Prerequisites
ก่อนที่เราจะเริ่มเขียนโค้ด โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมใช้งาน:

1. **Java Development Kit (JDK):** Ensure you have JDK 8 or above installed on your machine. You can download it from the [Java SE Development Kit Downloads](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java Library:** You’ll need to have the Aspose.PSD library, which you can [download here](https://releases.aspose.com/psd/java/).  
3. **IDE:** A suitable Integrated Development Environment (IDE) like IntelliJ IDEA or Eclipse for Java development.  
4. **Basic Java Knowledge:** Familiarity with Java programming is a plus, but don’t worry—we’ll walk you through each line.

ตอนนี้เราได้เตรียมสิ่งจำเป็นเรียบร้อยแล้ว ไปที่ส่วนที่สนุกที่สุด—การเขียนโค้ดกันเถอะ!

## Import Packages
เพื่อเริ่มทำงานกับไลบรารี Aspose.PSD ขั้นตอนแรกคือการนำเข้าคลาสที่จำเป็น ดังนี้:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```

ตรวจสอบให้แน่ใจว่าคุณได้เพิ่มไลบรารีที่จำเป็นลงในโปรเจกต์แล้วเพื่อให้การ import ทำงานได้อย่างราบรื่น

## Step 1: Set Up Your Document Directory
ทุกโปรเจกต์ต้องมีจุดเริ่มต้นเช่นกัน เราต้องระบุโฟลเดอร์ที่เก็บไฟล์ PSD ของคุณ ซึ่งเป็นขั้นตอนสำคัญสำหรับการโหลดและบันทึกภาพอย่างถูกต้อง

```java
String dataDir = "Your Document Directory"; // Update this path to your actual directory
```

## Step 2: Load an Existing PSD File
เพื่อทำการปรับแต่งไฟล์ PSD ที่มีอยู่ เราต้องโหลดไฟล์นั้นเข้าสู่โปรแกรม ตัวอย่างโค้ดมีดังนี้:

```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

ในโค้ดนี้ให้เปลี่ยน `"HueSaturationAdjustmentLayer.psd"` เป็นชื่อไฟล์ PSD ที่คุณต้องการแก้ไข

## Step 3: Edit the Hue/Saturation Layer
ต่อไปเราจะวนลูปผ่านเลเยอร์ของภาพ PSD ที่โหลดมาเพื่อค้นหาและแก้ไขเลเยอร์ Hue/Saturation ที่มีอยู่ ขั้นตอนนี้เกี่ยวข้องกับการปรับค่า hue, saturation และ lightness

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

ในตัวอย่างนี้:  
- เราปรับค่า hue เป็น **-25**, saturation เป็น **-12**, และ lightness เป็น **+67**.  
- เมธอด `getRange(2)` ช่วยให้คุณปรับช่วงสีเฉพาะตามต้องการ

## Step 4: Save the Modified PSD File
หลังจากทำการปรับค่าเสร็จ ขั้นตอนต่อไปคือการบันทึกไฟล์ การบันทึกนี้เป็นส่วนสำคัญเพื่อให้การเปลี่ยนแปลงไม่หายไป

```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```

## Step 5: Add a New Hue/Saturation Layer
หากคุณต้องการ **create hue adjustment layer** ตั้งแต่ต้น คุณสามารถเพิ่มเลเยอร์ Hue/Saturation ใหม่ลงในไฟล์ PSD อื่นได้โดยใช้เมธอด `addHueSaturationAdjustmentLayer()`

```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```

## Step 6: Set New Hue/Saturation Values for the New Layer
เมื่อสร้างเลเยอร์ใหม่แล้ว ให้กำหนดค่า hue, saturation และ lightness ตามที่ต้องการเช่นเดียวกับขั้นตอนก่อนหน้า

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
สุดท้ายบันทึกไฟล์ PSD ที่มีเลเยอร์ Hue/Saturation เพิ่มเข้ามาเพื่อให้คุณเห็นการเปลี่ยนแปลง

```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```

ยินดีด้วย! คุณได้ทำการจัดการไฟล์ PSD ด้วย Aspose.PSD for Java อย่างสำเร็จแล้ว ตอนนี้คุณสามารถทดลองกับภาพต่าง ๆ และทำการปรับแต่งที่ลึกซึ้งยิ่งขึ้น เพื่อทำให้โครงการออกแบบกราฟิกของคุณมีชีวิตชีวาขึ้น

## How to batch process PSD files with hue adjustments
เนื่องจากโค้ดด้านบนสามารถสคริปต์ได้เต็มที่ คุณสามารถห่อขั้นตอนทั้งหมดไว้ในลูปที่วนผ่านไฟล์ `.psd` ทุกไฟล์ในโฟลเดอร์หนึ่งได้ วิธีนี้ทำให้คุณ **batch process psd files** และปรับค่า hue, saturation, lightness เดียวกันในครั้งเดียว—เหมาะสำหรับการอัปเดตแบรนด์ระดับใหญ่

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
การทำงานกับกราฟิกโดยอัตโนมัติเปิดโอกาสใหม่ ๆ ให้คุณใช้ Aspose.PSD for Java เพื่อ **add hue saturation layer** และ **create hue adjustment layer** ทำให้คุณมีความยืดหยุ่นและประสิทธิภาพที่ช่วยเร่งกระบวนการออกแบบ ไม่ว่าคุณจะปรับปรุงภาพสำหรับโครงการหรือสร้างคอนเทนต์ภาพที่สวยงาม การเชี่ยวชาญเครื่องมือเหล่านี้จะช่วยยกระดับผลลัพธ์ของคุณอย่างมาก

อย่าลังเลที่จะสำรวจฟังก์ชันเพิ่มเติมของ Aspose.PSD โดยอ่าน [documentation](https://reference.aspose.com/psd/java/) หรือพิจารณาใช้ [temporary license](https://purchase.aspose.com/temporary-license/) เพื่อทดสอบพลังเต็มของไลบรารี

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

---