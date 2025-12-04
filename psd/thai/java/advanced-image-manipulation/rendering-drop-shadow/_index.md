---
date: 2025-12-04
description: เรียนรู้วิธีบันทึกไฟล์ PSD เป็น PNG และใช้เงาตกแบบเรนเดอร์ด้วย Aspose.PSD
  สำหรับ Java คู่มือนี้ครอบคลุมวิธีเพิ่มเงา, แปลง PSD เป็น PNG, และใช้เงาตกใน Java
language: th
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: บันทึก PSD เป็น PNG และเพิ่มเงาตกด้วย Aspose.PSD Java
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึก PSD เป็น PNG และเพิ่มเงาตกกับ Aspose.PSD Java

## บทนำ

หากคุณทำงานกับไฟล์ Photoshop ใน Java, **saving PSD as PNG** พร้อมกับการเพิ่มเงาตกที่ดูเป็นมืออาชีพเป็นความต้องการทั่วไป Aspose.PSD ทำให้งานนี้ง่ายขึ้น โดยให้คุณ **convert PSD to PNG** และ **apply drop shadow Java** เพียงไม่กี่บรรทัดของโค้ด ในบทแนะนำนี้เราจะพาคุณผ่านกระบวนการทั้งหมด ตั้งแต่การโหลดไฟล์ PSD จนถึงการส่งออก PNG สุดท้ายพร้อมเอฟเฟกต์เงาที่เรนเดอร์แล้ว.

## คำตอบด่วน
- **What does “save PSD as PNG” mean?** มันแปลงไฟล์ Photoshop แบบหลายชั้นเป็นภาพ PNG แบบแบนเดียว โดยคงความโปร่งใสไว้.  
- **Can I add a drop shadow while converting?** ใช่—Aspose.PSD ให้คุณแก้ไขเอฟเฟกต์ของเลเยอร์ก่อนการส่งออก.  
- **Do I need a license to run the code?** ต้องการไลเซนส์เพื่อรันโค้ดหรือไม่? การทดลองใช้ฟรีใช้ได้สำหรับการประเมิน; จำเป็นต้องมีไลเซนส์สำหรับการใช้งานจริง.  
- **Which Java version is supported?** เวอร์ชัน Java ที่รองรับคืออะไร? Java 8 หรือสูงกว่า.  
- **Is the drop‑shadow effect customizable?** เอฟเฟกต์เงาตกสามารถปรับแต่งได้หรือไม่? แน่นอน—คุณสามารถปรับสี, ความทึบ, ระยะทาง, ขนาด, มุม และอื่น ๆ ได้.

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม, โปรดตรวจสอบว่าคุณมี:

- **Java Development Environment** – ติดตั้ง JDK 8 หรือใหม่กว่า.  
- **Aspose.PSD Library** – ดาวน์โหลด JAR ล่าสุดจากเว็บไซต์ทางการ [here](https://releases.aspose.com/psd/java/).  
- **A PSD file** – ไฟล์ที่มีอย่างน้อยหนึ่งเลเยอร์ที่คุณต้องการเพิ่มเงา.  

## วิธีบันทึก PSD เป็น PNG พร้อมเงาตกใน Java?

ด้านล่างเป็นคำแนะนำแบบขั้นตอนต่อขั้นตอน แต่ละขั้นตอนรวมคำอธิบายสั้น ๆ ตามด้วยโค้ดที่ต้องคัดลอก.

### ขั้นตอนที่ 1: นำเข้าแพ็กเกจที่จำเป็น

เราเริ่มโดยการนำเข้าคลาสที่ให้การโหลดภาพ, การจัดการเอฟเฟกต์, และความสามารถในการส่งออก PNG

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

### ขั้นตอนที่ 2: กำหนดไดเรกทอรีเอกสาร

ตั้งค่าโฟลเดอร์ที่ไฟล์ PSD ต้นฉบับและ PNG ที่ได้จะถูกจัดเก็บ

```java
String dataDir = "Your Document Directory";
```

### ขั้นตอนที่ 3: ตั้งค่าเส้นทางไฟล์ PSD และ PNG

ระบุเส้นทางเต็มสำหรับ PSD อินพุตและ PNG เอาต์พุต

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### ขั้นตอนที่ 4: โหลดไฟล์ PSD พร้อมเปิดใช้งานเอฟเฟกต์

การเปิดใช้งาน **loadEffectsResource** จะทำให้แน่ใจว่าเอฟเฟกต์ของเลเยอร์ (เช่นเงา) สามารถจัดการได้

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### ขั้นตอนที่ 5: เข้าถึงเอฟเฟกต์เงาตก

ที่นี่เราดึงเอฟเฟกต์แรกที่ใช้กับเลเยอร์ที่สอง (ดัชนี 1) ซึ่งเป็นที่ที่เราจะอ่านหรือแก้ไขพารามิเตอร์ของเงา

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### ขั้นตอนที่ 6: ตรวจสอบคุณสมบัติของเอฟเฟกต์เงา (ไม่บังคับแต่เป็นประโยชน์)

การตรวจสอบคุณสมบัติปัจจุบันช่วยให้คุณตัดสินใจว่าต้องการเปลี่ยนแปลงอะไรหรือไม่ การยืนยันด้านล่างตรวจสอบค่าดีฟอลต์

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

> **เคล็ดลับ:** หากคุณต้องการ **how to add shadow** ด้วยการตั้งค่าที่กำหนดเอง, ให้แก้ไขคุณสมบัติบน `shadowEffect` ก่อนบันทึก (เช่น `shadowEffect.setColor(Color.getRed());`).

### ขั้นตอนที่ 7: บันทึกรูปภาพที่แก้ไขเป็น PNG

สุดท้ายเราส่งออก PSD (พร้อมเงาที่เรนเดอร์แล้ว) ไปเป็นไฟล์ PNG ตัวเลือก `TruecolorWithAlpha` จะคงความโปร่งใส

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

และนี่คือทั้งหมด—กระบวนการ **convert PSD to PNG** ที่สมบูรณ์พร้อมกับ **apply drop shadow java** ในหนึ่งขั้นตอน.

## ทำไมต้องใช้ Aspose.PSD สำหรับงานนี้?

- **No native Photoshop required** – ทำงานบนแพลตฟอร์มใดก็ได้ที่รองรับ Java.  
- **Full PSD fidelity** – ข้อมูลเลเยอร์, มาสก์, และเอฟเฟกต์ทั้งหมดจะถูกคงไว้.  
- **Fine‑grained control** – ปรับทุกพารามิเตอร์ของเงาตกก่อนการส่งออก.  
- **High performance** – ถูกปรับให้เหมาะกับไฟล์ขนาดใหญ่และการประมวลผลเป็นชุด.

## ปัญหาทั่วไปและการแก้ไขข้อผิดพลาด

| อาการ | สาเหตุที่เป็นไปได้ | วิธีแก้ |
|---------|-------------------|----------|
| `NullPointerException` on `shadowEffect` | เลเยอร์เป้าหมายไม่มีเอฟเฟกต์หรือดัชนีผิดพลาด. | ตรวจสอบดัชนีของเลเยอร์ (`im.getLayers()[i]`) และให้แน่ใจว่าเอฟเฟกต์มีอยู่. |
| PNG ที่ส่งออกเป็นสีขาวเปล่า | ตัวเลือก PNG ไม่ได้ตั้งค่าอย่างถูกต้องหรือภาพไม่ได้บันทึก. | ใช้ `PngColorType.TruecolorWithAlpha` และยืนยันว่าเส้นทาง `im.save()` สามารถเขียนได้. |
| สีเงาไม่ปรากฏ | ความทึบของเงาตั้งเป็น 0 หรือสีตรงกับพื้นหลัง. | ตั้งค่า `shadowEffect.setOpacity(255);` และเลือกสีที่ตัดกัน. |

## คำถามที่พบบ่อย

**Q: ฉันสามารถใช้เงาตกกับหลายเลเยอร์พร้อมกันได้หรือไม่?**  
A: ใช่. วนลูปผ่าน `im.getLayers()` และแก้ไข `DropShadowEffect` ของแต่ละเลเยอร์ตามต้องการ.

**Q: พารามิเตอร์ ‘Spread’ ทำหน้าที่อะไร?**  
A: มันควบคุมความคมของการเปลี่ยนจากเงาที่ทึบเต็มจนถึงโปร่งใส. Spread ที่สูงกว่าจะทำให้ขอบเงาแข็งแรงขึ้น.

**Q: Aspose.PSD รองรับเวอร์ชัน Photoshop ทั้งหมดหรือไม่?**  
A: มันรองรับหลายเวอร์ชันของ PSD ตั้งแต่รุ่นแรกจนถึงไฟล์ Photoshop CC ล่าสุด.

**Q: ฉันจะขอความช่วยเหลือเมื่อเจอปัญหาได้อย่างไร?**  
A: เยี่ยมชม [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) เพื่อรับการสนับสนุนจากชุมชนและความช่วยเหลืออย่างเป็นทางการ.

**Q: ฉันสามารถทดลองใช้ Aspose.PSD ก่อนซื้อได้หรือไม่?**  
A: ได้เลย. ดาวน์โหลดเวอร์ชันทดลองฟรีจาก [Aspose website](https://releases.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**อัปเดตล่าสุด:** 2025-12-04  
**ทดสอบด้วย:** Aspose.PSD 24.12 for Java  
**ผู้เขียน:** Aspose