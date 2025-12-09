---
date: 2025-11-30
description: เรียนรู้วิธีเพิ่มเส้นขอบและเปลี่ยนสีเส้นขอบของ PSD ด้วย Aspose.PSD สำหรับ
  Java. ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนนี้เพื่อแก้ไขสีและความทึบของเลเยอร์เส้นขอบ.
linktitle: Add Stroke Layer Color
second_title: Aspose.PSD Java API
title: วิธีเพิ่มสีของเลเยอร์เส้นขอบใน Aspose.PSD สำหรับ Java
url: /th/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีเพิ่มสีเลเยอร์ Stroke ใน Aspose.PSD สำหรับ Java

## Introduction

หากคุณต้องการ **วิธีเพิ่มเส้นขอบ** ให้กับเอกสาร Photoshop ผ่านโปรแกรม, Aspose.PSD สำหรับ Java ทำให้เป็นเรื่องง่าย ในบทเรียนนี้เราจะอธิบายขั้นตอนการเพิ่มสีเลเยอร์ Stroke, ปรับความทึบแสง, และบันทึกผลลัพธ์ เมื่อเสร็จคุณจะเห็นวิธี **วิธีเปลี่ยนสีเส้นขอบ** (หรือ *เปลี่ยนสี Stroke ของ PSD*) สำหรับเลเยอร์ใด ๆ ที่มีอยู่, ให้คุณควบคุมการออกแบบได้เต็มที่จากโค้ด Java ของคุณ.

## Quick Answers
- **ไลบรารีที่ต้องการคืออะไร?** Aspose.PSD for Java (เวอร์ชันล่าสุด).  
- **ฉันสามารถเปลี่ยนสีเส้นขอบได้หรือไม่?** ใช่ – ใช้ `ColorFillSettings` เพื่อกำหนด `Color` ใดก็ได้.  
- **ฉันต้องการไลเซนส์หรือไม่?** ไลเซนส์ชั่วคราวใช้ได้สำหรับการประเมิน; ไลเซนส์เต็มจำเป็นสำหรับการใช้งานจริง.  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Java 8 หรือสูงกว่า.  
- **ใช้เวลานานเท่าไหร่ในการดำเนินการ?** ปกติใช้เวลาน้อยกว่า 10 นาทีสำหรับการเปลี่ยน Stroke พื้นฐาน.

## What is a Stroke Layer in a PSD?
เลเยอร์ Stroke คือเอฟเฟกต์เวกเตอร์ที่วาดเส้นขอบรอบเนื้อหาของเลเยอร์ สามารถปรับแต่งด้วยสี, ความหนา, ความทึบแสง, และโหมดผสม การแก้ไขเอฟเฟกต์นี้ผ่านโปรแกรมทำให้สามารถทำแบรนด์อัตโนมัติ, การประมวลผลเป็นชุด, หรือการสร้างกราฟิกแบบไดนามิกได้

## Why Use Aspose.PSD to Change Stroke Color?
- **ไม่ต้องใช้ Photoshop** – ทำงานทั้งหมดใน Java.  
- **สอดคล้องกับสเปค PSD เต็มรูปแบบ** – รองรับคุณสมบัติ PSD สมัยใหม่ทั้งหมด.  
- **ประสิทธิภาพสูง** – ประมวลผลไฟล์ขนาดใหญ่ได้อย่างรวดเร็ว.  
- **ข้ามแพลตฟอร์ม** – รันบน OS ใดก็ได้ที่มี JVM.

## Prerequisites

- **ไลบรารี Aspose.PSD** – ดาวน์โหลดจาก [เอกสารอย่างเป็นทางการ](https://reference.aspose.com/psd/java/).  
- **Java Development Kit (JDK)** – เวอร์ชัน 8 หรือใหม่กว่า.  
- **IDE** – Eclipse, IntelliJ IDEA, หรือเครื่องมือแก้ไขที่รองรับ Java ใดก็ได้.

## Import Packages

ก่อนอื่นให้ import คลาสที่จำเป็น นี่จะทำให้โปรเจกต์ของคุณเข้าถึง API การจัดการ PSD และเอฟเฟกต์ Stroke

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

## Step 1: Set Up Your Project

สร้างโปรเจกต์ Java ใหม่, เพิ่มไฟล์ JAR ของ Aspose.PSD ไปยัง build path, และตรวจสอบว่าลิบรารีโหลดโดยไม่มีข้อผิดพลาด.

## Step 2: Load the PSD File

เปิดใช้งานการโหลดทรัพยากรเอฟเฟกต์เพื่อให้ข้อมูล Stroke พร้อมใช้งาน.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Step 3: Access the Stroke Effect Layer

ดึงเอฟเฟกต์ Stroke ตัวแรกจากเลเยอร์ที่สอง (ดัชนี 1).

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## Step 4: Validate Stroke Properties

ยืนยันคุณสมบัติปัจจุบันก่อนทำการเปลี่ยนแปลง เพื่อหลีกเลี่ยงผลลัพธ์ที่ไม่คาดคิด.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## Step 5: Set Color and Opacity (How to Change Stroke Color)

ที่นี่เราจะ **เปลี่ยนสี Stroke ของ PSD** เป็นสีเหลืองและลดความทึบแสงลงเหลือ 50 % (127 / 255).

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## Step 6: Save the Modified PSD

เขียนภาพที่อัปเดตกลับไปยังดิสก์ ไฟล์ใหม่จะมี Stroke ที่แก้ไขแล้ว.

```java
im.save(exportPath);
```

## Common Pitfalls & Tips

- **การตรวจสอบค่า null** – ตรวจสอบเสมอว่า `getEffects()` คืนค่าเป็นอาเรย์ที่ไม่เป็น null ก่อนทำการแคส.  
- **ดัชนีเลเยอร์** – เลเยอร์ PSD เริ่มจากศูนย์; ตรวจสอบว่าคุณเลือกเลเยอร์ที่ถูกต้อง.  
- **รูปแบบสี** – `Color.getYellow()` เป็นเพียงตัวอย่าง; คุณสามารถสร้างสีกำหนดเองด้วย `new Color(r, g, b)`.  
- **ช่วงความทึบแสง** – ความทึบเป็นค่าไบต์ (0–255); ค่าที่มากกว่า 255 จะถูกจำกัด.

## Conclusion

คุณได้เรียนรู้ **วิธีเพิ่มเส้นขอบ** ให้กับไฟล์ PSD และ **วิธีเปลี่ยนสีเส้นขอบ** ด้วย Aspose.PSD สำหรับ Java แล้ว ทดลองใช้สี, โหมดผสม, และความทึบแสงต่าง ๆ เพื่อให้ได้สไตล์ภาพที่ต้องการสำหรับโครงการของคุณ.

## Frequently Asked Questions

**ถาม: ฉันสามารถใช้ Aspose.PSD ร่วมกับไลบรารีกราฟิก Java อื่นได้หรือไม่?**  
ตอบ: ใช่, Aspose.PSD สามารถรวมกับไลบรารีเช่น Apache Commons Imaging หรือ Java2D เพื่อเพิ่มฟังก์ชันการทำงาน.

**ถาม: Aspose.PSD รองรับรูปแบบไฟล์ PSD ล่าสุดหรือไม่?**  
ตอบ: แน่นอน. ไลบรารีนี้อัปเดตเป็นประจำเพื่อรองรับสเปค Photoshop ล่าสุด.

**ถาม: ฉันจะจัดการกับข้อยกเว้นเมื่อใช้ Aspose.PSD อย่างไร?**  
ตอบ: ดูที่ [ฟอรั่มสนับสนุน](https://forum.aspose.com/c/psd/34) สำหรับการแก้ปัญหาอย่างละเอียดและตัวอย่างโค้ดการจัดการข้อผิดพลาด.

**ถาม: ฉันสามารถทดลองใช้ Aspose.PSD ก่อนซื้อได้หรือไม่?**  
ตอบ: แน่นอน! ดาวน์โหลด [รุ่นทดลองฟรี](https://releases.aspose.com/) เพื่อสำรวจคุณสมบัติทั้งหมด.

**ถาม: ฉันจะได้ไลเซนส์ชั่วคราวสำหรับ Aspose.PSD จากที่ไหน?**  
ตอบ: รับ [ไลเซนส์ชั่วคราว](https://purchase.aspose.com/temporary-license/) เพื่อประเมินไลบรารีในสภาพแวดล้อมการพัฒนาของคุณ.

---

**Last Updated:** 2025-11-30  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}