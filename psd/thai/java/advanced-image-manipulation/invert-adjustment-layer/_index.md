---
title: สลับเลเยอร์การปรับใน Aspose.PSD สำหรับ Java
linktitle: สลับเลเยอร์การปรับ
second_title: Aspose.PSD Java API
description: สำรวจ Invert Adjustment Layer ใน Aspose.PSD สำหรับ Java ไลบรารี Java ที่ทรงพลังสำหรับการจัดการไฟล์ PSD ได้อย่างราบรื่น
weight: 14
url: /th/java/advanced-image-manipulation/invert-adjustment-layer/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สลับเลเยอร์การปรับใน Aspose.PSD สำหรับ Java

## การแนะนำ

ยินดีต้อนรับสู่คำแนะนำทีละขั้นตอนของเราเกี่ยวกับการใช้ Invert Adjustment Layer ใน Aspose.PSD สำหรับ Java ในบทช่วยสอนนี้ เราจะสำรวจคุณสมบัติอันทรงพลังของ Aspose.PSD ซึ่งเป็นไลบรารี Java ที่ช่วยให้จัดการไฟล์ PSD ได้อย่างราบรื่น ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเป็นมือใหม่ในการประมวลผลภาพ บทช่วยสอนนี้ออกแบบมาเพื่อช่วยให้คุณเข้าใจและใช้งาน Invert Adjustment Layer ได้อย่างมีประสิทธิภาพ

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. ไลบรารี Aspose.PSD: ตรวจสอบให้แน่ใจว่าคุณได้ดาวน์โหลดและติดตั้งไลบรารี Aspose.PSD แล้ว คุณสามารถค้นหาลิงค์ดาวน์โหลด[ที่นี่](https://releases.aspose.com/psd/java/).

2. สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java บนระบบของคุณ

ตอนนี้เรามาเริ่มต้นใช้งานกันดีกว่า

## แพ็คเกจนำเข้า

เริ่มต้นด้วยการนำเข้าแพ็คเกจที่จำเป็นในแอปพลิเคชัน Java ของคุณ แพ็คเกจเหล่านี้จำเป็นสำหรับการทำงานกับฟังก์ชัน Aspose.PSD

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสาร

เริ่มต้นไดเร็กทอรีที่มีไฟล์ PSD ของคุณอยู่

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: โหลดไฟล์ PSD

โหลดไฟล์ PSD โดยใช้ไลบรารี Aspose.PSD

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## ขั้นตอนที่ 3: เพิ่มเลเยอร์การปรับกลับด้าน

ใช้ Invert Adjustment Layer บนรูปภาพ PSD ที่โหลด

```java
im.addInvertAdjustmentLayer();
```

## ขั้นตอนที่ 4: บันทึกผลลัพธ์

บันทึกรูปภาพ PSD ที่แก้ไขด้วย Invert Adjustment Layer ที่ใช้

```java
im.save(outputPath);
```

ยินดีด้วย! คุณใช้งาน Invert Adjustment Layer โดยใช้ Aspose.PSD สำหรับ Java สำเร็จแล้ว รู้สึกอิสระที่จะสำรวจคุณสมบัติและฟังก์ชันการทำงานเพิ่มเติมของ Aspose.PSD เพื่อเพิ่มความสามารถในการประมวลผลภาพของคุณ

## บทสรุป

ในบทช่วยสอนนี้ เราได้กล่าวถึงกระบวนการทีละขั้นตอนในการรวม Invert Adjustment Layer เข้ากับไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java ไลบรารีอเนกประสงค์นี้ช่วยให้นักพัฒนาจัดการรูปภาพได้อย่างง่ายดาย เปิดโลกแห่งความเป็นไปได้สำหรับโปรเจ็กต์สร้างสรรค์

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD เข้ากันได้กับ Java เวอร์ชันทั้งหมดหรือไม่

A1: Aspose.PSD รองรับ Java 6.0 และเวอร์ชันที่ใหม่กว่า

### คำถามที่ 2: ฉันสามารถใช้การปรับหลายชั้นในการดำเนินการครั้งเดียวได้หรือไม่

ตอบ 2: ได้ คุณสามารถซ้อนเลเยอร์การปรับหลายชั้นเข้าด้วยกันเพื่อให้ได้การปรับแต่งภาพที่ซับซ้อน

### คำถามที่ 3: ฉันจะหาเอกสารเพิ่มเติมสำหรับ Aspose.PSD ได้ที่ไหน

 A3: โปรดดูเอกสารประกอบ[ที่นี่](https://reference.aspose.com/psd/java/) เพื่อข้อมูลที่ครบถ้วน

### คำถามที่ 4: Aspose.PSD มีรุ่นทดลองใช้ฟรีหรือไม่

 A4: ได้ คุณสามารถทดลองใช้งานฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร

A5: คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
