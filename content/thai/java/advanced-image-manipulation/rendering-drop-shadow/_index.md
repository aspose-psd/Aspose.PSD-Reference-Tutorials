---
title: ใช้ Rendering Drop Shadow ใน Aspose.PSD สำหรับ Java
linktitle: ใช้การเรนเดอร์เงาตกกระทบ
second_title: Aspose.PSD Java API
description: สำรวจคำแนะนำทีละขั้นตอนในการใช้การเรนเดอร์เงาใน Aspose.PSD สำหรับ Java ซึ่งจะช่วยเสริมทักษะการประมวลผลภาพของคุณได้อย่างง่ายดาย
type: docs
weight: 16
url: /th/java/advanced-image-manipulation/rendering-drop-shadow/
---
## การแนะนำ

หากคุณกำลังสนใจในการประมวลผลภาพด้วย Java Aspose.PSD คือเครื่องมือที่คุณนำไปใช้ได้จริงสำหรับการจัดการไฟล์ PSD ได้อย่างราบรื่นและมีประสิทธิภาพ ในบทช่วยสอนนี้ เราจะสำรวจกระบวนการใช้เงาตกกระทบในการเรนเดอร์โดยใช้ Aspose.PSD สำหรับ Java รัดเข็มขัดในขณะที่เราแจกแจงขั้นตอนต่างๆ ให้กับคุณ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้นการเดินทางครั้งนี้ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java บนเครื่องของคุณแล้ว
- ไลบรารี Aspose.PSD: ดาวน์โหลดและตั้งค่าไลบรารี Aspose.PSD คุณสามารถค้นหาห้องสมุด[ที่นี่](https://releases.aspose.com/psd/java/).
- ไฟล์ PSD: เตรียมไฟล์ PSD ที่มีเลเยอร์ที่คุณต้องการใช้วางเงา

## แพ็คเกจนำเข้า

มาเริ่มกันด้วยการนำเข้าแพ็คเกจที่จำเป็น ขั้นตอนนี้ช่วยให้แน่ใจว่าคุณมีเครื่องมือที่จำเป็นเพื่อการใช้งานโค้ดที่ราบรื่น

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

ตอนนี้เรามาดูรายละเอียดแต่ละขั้นตอนกัน

## ขั้นตอนที่ 1: กำหนดไดเร็กทอรีเอกสาร

เริ่มต้นด้วยการระบุไดเร็กทอรีที่มีไฟล์ PSD ของคุณ

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: ตั้งค่าเส้นทางไฟล์ PSD และ PNG

กำหนดเส้นทางสำหรับไฟล์ PSD ต้นทางและไฟล์ PNG ปลายทาง

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

## ขั้นตอนที่ 3: โหลดไฟล์ PSD พร้อมเอฟเฟกต์

โหลดไฟล์ PSD เพื่อให้สามารถโหลดทรัพยากรเอฟเฟกต์ได้

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## ขั้นตอนที่ 4: เข้าถึงเอฟเฟกต์ Drop Shadow

ดึงเอฟเฟกต์เงาจากเลเยอร์ที่ระบุ

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

## ขั้นตอนที่ 5: ตรวจสอบคุณสมบัติของเอฟเฟกต์เงา

ตรวจสอบให้แน่ใจว่าคุณสมบัติเอฟเฟกต์เงาตกกระทบตรงตามความคาดหวังของคุณ

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

## ขั้นตอนที่ 6: บันทึกเป็น PNG

บันทึกภาพที่แก้ไขเป็นไฟล์ PNG

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

และคุณก็เข้าใจแล้ว—คำแนะนำทีละขั้นตอนในการใช้การเรนเดอร์เงาตกหล่นใน Aspose.PSD สำหรับ Java

## บทสรุป

การเรียนรู้การจัดการภาพใน Java กลายเป็นเรื่องง่ายด้วย Aspose.PSD คุณเพิ่งไขความลับในการแสดงเงาตกกระทบ ซึ่งเป็นการเปิดโลกแห่งความเป็นไปได้ที่สร้างสรรค์

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้เงาตกกระทบกับหลายเลเยอร์พร้อมกันได้หรือไม่

A1: ได้ คุณสามารถวนซ้ำเลเยอร์ต่างๆ และใช้เงาตกกระทบได้ตามต้องการ

### คำถามที่ 2: พารามิเตอร์ 'Spread' มีความสำคัญอย่างไรในเงาตกกระทบ

A2: พารามิเตอร์ 'Spread' ควบคุมการเปลี่ยนระหว่างพื้นที่เงาและพื้นที่ที่ไม่ใช่เงา

### คำถามที่ 3: Aspose.PSD เข้ากันได้กับไฟล์ Photoshop ทุกเวอร์ชันหรือไม่

A3: Aspose.PSD ให้ความเข้ากันได้กับไฟล์ PSD เวอร์ชันต่างๆ มากมาย จึงมั่นใจได้ถึงความอเนกประสงค์

### คำถามที่ 4: ฉันจะรายงานปัญหาหรือขอความช่วยเหลือจาก Aspose.PSD ได้อย่างไร

 A4: ตรงไปที่[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) เพื่อการสนับสนุนอย่างครอบคลุม

### คำถามที่ 5: ฉันสามารถทดสอบ Aspose.PSD ก่อนตัดสินใจซื้อได้หรือไม่

 A5: แน่นอน ใช้[ทดลองใช้ฟรี](https://releases.aspose.com/) เพื่อสำรวจความสามารถก่อนตัดสินใจซื้อ