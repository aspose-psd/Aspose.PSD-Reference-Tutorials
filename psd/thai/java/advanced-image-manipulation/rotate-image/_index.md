---
title: หมุนรูปภาพใน Aspose.PSD สำหรับ Java
linktitle: หมุนรูปภาพ
second_title: Aspose.PSD Java API
description: สำรวจการหมุนภาพใน Java ได้อย่างง่ายดายด้วย Aspose.PSD หมุน พลิก และบันทึกไฟล์ PSD ได้อย่างง่ายดาย
weight: 19
url: /th/java/advanced-image-manipulation/rotate-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# หมุนรูปภาพใน Aspose.PSD สำหรับ Java

## การแนะนำ

Aspose.PSD สำหรับ Java มอบชุดคุณสมบัติอันทรงพลังสำหรับการทำงานกับรูปภาพ ช่วยให้นักพัฒนาจัดการและประมวลผลไฟล์ PSD ได้อย่างมีประสิทธิภาพ ในบทช่วยสอนนี้ เราจะเน้นไปที่งานเฉพาะอย่างหนึ่ง นั่นคือ การหมุนรูปภาพ ไม่ว่าคุณกำลังสร้างแอปพลิเคชันแก้ไขรูปภาพหรือเพียงแค่ต้องปรับการวางแนวของรูปภาพ Aspose.PSD จะทำให้กระบวนการนี้ตรงไปตรงมา

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.PSD สำหรับไลบรารี Java: ตรวจสอบให้แน่ใจว่าคุณได้ดาวน์โหลดและติดตั้ง Aspose.PSD สำหรับไลบรารี Java แล้ว คุณสามารถค้นหาห้องสมุดและเอกสารรายละเอียดได้[ที่นี่](https://reference.aspose.com/psd/java/).

- สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java บนเครื่องของคุณ

-  ไฟล์ PSD ตัวอย่าง: เตรียมไฟล์ PSD ตัวอย่างที่คุณต้องการหมุน ปรับ`sourceFile` ตัวแปรในโค้ดตัวอย่างพร้อมเส้นทางไปยังไฟล์ PSD ของคุณ

## แพ็คเกจนำเข้า

เริ่มต้นด้วยการนำเข้าแพ็คเกจที่จำเป็นเพื่อใช้ประโยชน์จากความสามารถของ Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## ขั้นตอนที่ 1: โหลดรูปภาพ

 โหลดรูปภาพที่มีอยู่ลงในอินสแตนซ์ของ`Image` ระดับ:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## ขั้นตอนที่ 2: หมุนภาพ

 หมุนภาพโดยใช้`rotateFlip` วิธี. ในตัวอย่างนี้ เราหมุนรูปภาพ 270 องศา:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## ขั้นตอนที่ 3: บันทึกภาพที่หมุนแล้ว

 บันทึกภาพที่หมุนโดยใช้`save` และระบุรูปแบบเอาต์พุต (JPEG ในกรณีนี้):

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## บทสรุป

ยินดีด้วย! คุณได้หมุนรูปภาพโดยใช้ Aspose.PSD สำหรับ Java สำเร็จแล้ว ไลบรารีที่เรียบง่ายแต่ทรงพลังนี้เปิดโลกแห่งความเป็นไปได้สำหรับการจัดการรูปภาพในแอปพลิเคชัน Java ของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD เข้ากันได้กับรูปแบบรูปภาพที่แตกต่างกันหรือไม่

A1: ใช่ Aspose.PSD รองรับรูปแบบภาพที่หลากหลาย รวมถึง PSD, JPEG, PNG และอื่นๆ

### คำถามที่ 2: ฉันสามารถใช้การหมุนแบบกำหนดเอง ไม่ใช่แค่การพลิกที่กำหนดไว้ล่วงหน้าได้หรือไม่

A2: แน่นอน! Aspose.PSD มอบความยืดหยุ่นในการใช้การหมุนเวียนแบบกำหนดเองเพื่อให้ตรงตามความต้องการเฉพาะของคุณ

### คำถามที่ 3: ฉันจะรับการสนับสนุนหรือความช่วยเหลือเพิ่มเติมได้จากที่ไหน

 A3: สำหรับข้อสงสัยหรือปัญหาใดๆ โปรดไปที่[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) เพื่อสนับสนุนชุมชน

### คำถามที่ 4: มีการทดลองใช้ฟรีหรือไม่?

 A4: ใช่ คุณสามารถสำรวจ Aspose.PSD ได้ด้วย[ทดลองใช้ฟรี](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะขอรับใบอนุญาตชั่วคราวได้อย่างไร

 A5: หากคุณต้องการใบอนุญาตชั่วคราว คุณสามารถขอรับได้[ที่นี่](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
