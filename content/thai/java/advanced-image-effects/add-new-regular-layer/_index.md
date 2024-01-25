---
title: เพิ่มเลเยอร์ปกติใหม่ให้กับ PSD ด้วย Aspose.PSD สำหรับ Java
linktitle: เพิ่มเลเยอร์ปกติใหม่ให้กับ PSD
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีเพิ่มเลเยอร์ปกติใหม่ให้กับไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการจัดการ PSD ที่ราบรื่น
type: docs
weight: 11
url: /th/java/advanced-image-effects/add-new-regular-layer/
---
## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนที่ครอบคลุมเกี่ยวกับการใช้ Aspose.PSD สำหรับ Java เพื่อเพิ่มเลเยอร์ปกติใหม่ให้กับไฟล์ PSD Aspose.PSD เป็นไลบรารี Java ที่ทรงพลังซึ่งช่วยให้นักพัฒนาจัดการและทำงานกับไฟล์ PSD ได้อย่างมีประสิทธิภาพ ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการเพิ่มเลเยอร์ปกติใหม่ให้กับไฟล์ PSD โดยให้ขั้นตอนโดยละเอียดและตัวอย่างโค้ด

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java บนระบบของคุณ
-  ไลบรารี Aspose.PSD: ดาวน์โหลดและติดตั้ง Aspose.PSD สำหรับไลบรารี Java คุณสามารถค้นหาห้องสมุด[ที่นี่](https://releases.aspose.com/psd/java/).

## แพ็คเกจนำเข้า

ในการเริ่มต้น ให้นำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ แพ็คเกจเหล่านี้จำเป็นสำหรับการทำงานกับฟังก์ชัน Aspose.PSD รวมบรรทัดต่อไปนี้ไว้ที่จุดเริ่มต้นของไฟล์ Java ของคุณ:

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## ขั้นตอนที่ 1: โหลดไฟล์ PSD

โหลดไฟล์ PSD ที่คุณต้องการแก้ไขโดยใช้รหัสต่อไปนี้:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## ขั้นตอนที่ 2: เตรียมอาร์เรย์ข้อมูลและสี่เหลี่ยม

เตรียมอาร์เรย์ int สองตัวและวัตถุสี่เหลี่ยมผืนผ้าสองชิ้นดังนี้:

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## ขั้นตอนที่ 3: เริ่มต้นข้อมูลเลเยอร์

เริ่มต้นอาร์เรย์ข้อมูลด้วยค่าเริ่มต้น:

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## ขั้นตอนที่ 4: เพิ่มเลเยอร์ปกติ

เพิ่มเลเยอร์ปกติสองชั้นให้กับรูปภาพ PSD:

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

## ขั้นตอนที่ 5: บันทึก PSD และ PNG

บันทึก PSD ที่แก้ไขและไฟล์ PNG เพิ่มเติม:

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

ยินดีด้วย! คุณได้เพิ่มเลเยอร์ปกติใหม่ลงในไฟล์ PSD สำเร็จแล้วโดยใช้ Aspose.PSD สำหรับ Java

## บทสรุป

ในบทช่วยสอนนี้ เราได้กล่าวถึงกระบวนการเพิ่มเลเยอร์ปกติใหม่ให้กับไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java ไลบรารีอันทรงพลังนี้ทำให้การจัดการ PSD ง่ายขึ้น ทำให้นักพัฒนา Java สามารถเข้าถึงได้ ทดลองใช้พารามิเตอร์และฟังก์ชันต่างๆ เพื่อสำรวจศักยภาพทั้งหมดของ Aspose.PSD

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD เข้ากันได้กับ Java 8 หรือไม่

A1: ใช่ Aspose.PSD รองรับ Java 8 และเวอร์ชันที่ใหม่กว่า

### คำถามที่ 2: ฉันสามารถใช้การแปลงกับเลเยอร์ที่เพิ่มเข้ามาได้หรือไม่

A2: แน่นอน! Aspose.PSD มีตัวเลือกการเปลี่ยนแปลงมากมายสำหรับเลเยอร์

### คำถามที่ 3: ฉันจะหาเอกสารประกอบ Aspose.PSD เพิ่มเติมได้จากที่ไหน

 A3: คุณสามารถดูเอกสารประกอบได้[ที่นี่](https://reference.aspose.com/psd/java/).

### คำถามที่ 4: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร

 A4: เยี่ยมเลย[ลิงค์นี้](https://purchase.aspose.com/temporary-license/) สำหรับตัวเลือกใบอนุญาตชั่วคราว

### คำถามที่ 5: มีฟอรัมชุมชนสำหรับการสนับสนุน Aspose.PSD หรือไม่

 A5: ใช่ คุณสามารถค้นหาการสนับสนุนและการสนทนาได้[ที่นี่](https://forum.aspose.com/c/psd/34).