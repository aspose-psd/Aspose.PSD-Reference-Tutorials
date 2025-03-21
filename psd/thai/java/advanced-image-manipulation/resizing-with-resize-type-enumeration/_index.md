---
title: การปรับขนาดด้วยการแจงนับประเภทการปรับขนาดใน Aspose.PSD สำหรับ Java
linktitle: การปรับขนาดด้วยการแจงนับประเภทการปรับขนาด
second_title: Aspose.PSD Java API
description: การปรับขนาดรูปภาพหลักใน Java ด้วย Aspose.PSD คำแนะนำทีละขั้นตอนโดยใช้การแจงนับประเภทการปรับขนาด
weight: 18
url: /th/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การปรับขนาดด้วยการแจงนับประเภทการปรับขนาดใน Aspose.PSD สำหรับ Java

## การแนะนำ

ในภูมิทัศน์การพัฒนา Java ที่เปลี่ยนแปลงตลอดเวลา การประมวลผลภาพที่มีประสิทธิภาพเป็นสิ่งสำคัญที่นักพัฒนามักต้องเผชิญ Aspose.PSD สำหรับ Java กลายเป็นโซลูชันที่ทรงพลัง โดยมอบประสบการณ์ที่ราบรื่นในการปรับขนาดรูปภาพ พร้อมข้อดีเพิ่มเติมของการแจงนับประเภทการปรับขนาด ในบทช่วยสอนนี้ เราจะเจาะลึกความซับซ้อนของการปรับขนาดรูปภาพโดยใช้ Aspose.PSD สำหรับ Java โดยแจกแจงแต่ละขั้นตอนเพื่อให้แน่ใจว่ามีความเข้าใจที่ครอบคลุม

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเริ่มบทช่วยสอนนี้ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java บนเครื่องของคุณ

2. ไลบรารี Aspose.PSD: ดาวน์โหลดและติดตั้งไลบรารี Aspose.PSD จากไฟล์[เว็บไซต์](https://releases.aspose.com/psd/java/).

3.  ไฟล์ PSD ตัวอย่าง: เตรียมไฟล์ PSD ตัวอย่างให้พร้อมสำหรับการทดลอง คุณสามารถใช้[example.psd](ไดเรกทอรีเอกสารของคุณ/sample.psd) สำหรับบทช่วยสอนนี้

## แพ็คเกจนำเข้า

ในการเริ่มต้น ให้นำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## ขั้นตอนที่ 1: โหลดรูปภาพ

 เริ่มต้นด้วยการโหลดรูปภาพที่มีอยู่ลงในอินสแตนซ์ของ`RasterImage` ระดับ. ใช้ข้อมูลโค้ดต่อไปนี้:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// โหลดรูปภาพที่มีอยู่ลงในอินสแตนซ์ของคลาส RasterImage
Image image = Image.load(sourceFile);
```

## ขั้นตอนที่ 2: ปรับขนาดรูปภาพ

ตอนนี้ ปรับขนาดภาพที่โหลดโดยใช้ Resize Type Enumeration ในตัวอย่างนี้ เราใช้วิธี Lanczos Resample:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## ขั้นตอนที่ 3: บันทึกภาพที่ปรับขนาดแล้ว

หลังจากปรับขนาดแล้ว ให้บันทึกรูปภาพตามขนาดที่ระบุและประเภทการปรับขนาดที่เลือก ที่นี่เราบันทึกเป็นไฟล์ JPEG:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

และคุณก็ได้แล้ว! คุณปรับขนาดรูปภาพได้สำเร็จโดยใช้ Resize Type Enumeration ใน Aspose.PSD สำหรับ Java

โดยสรุป Aspose.PSD สำหรับ Java มอบแพลตฟอร์มที่แข็งแกร่งสำหรับการจัดการรูปภาพ และการแจงนับประเภทการปรับขนาดจะเพิ่มชั้นของความยืดหยุ่นให้กับกระบวนการนี้ ไม่ว่าคุณจะทำงานในโครงการขนาดเล็กหรือแอปพลิเคชันขนาดใหญ่ การทำตามขั้นตอนเหล่านี้ให้เชี่ยวชาญจะช่วยให้คุณจัดการกับการปรับขนาดรูปภาพได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD สำหรับ Java เหมาะสำหรับทั้งโปรเจ็กต์ขนาดเล็กและขนาดใหญ่หรือไม่

A1: แน่นอน! Aspose.PSD สำหรับ Java ได้รับการออกแบบมาเพื่อรองรับโปรเจ็กต์ทุกขนาด โดยให้ความสามารถในการปรับขนาดและประสิทธิภาพ

### คำถามที่ 2: ฉันสามารถใช้การปรับขนาดประเภทอื่นนอกเหนือจาก Lanczos Resample ได้หรือไม่

ตอบ 2: ใช่ Aspose.PSD สำหรับ Java มีประเภทการปรับขนาดที่หลากหลาย เช่น Nearest Neighbour, Bicubic และอื่นๆ อีกมากมาย สำรวจเอกสารเพื่อดูรายการที่ครอบคลุม

### คำถามที่ 3: ฉันจะรับการสนับสนุนเพิ่มเติมสำหรับ Aspose.PSD สำหรับ Java ได้ที่ไหน

 A3: หากมีข้อสงสัยหรือความช่วยเหลือ โปรดไปที่[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34).

### คำถามที่ 4: Aspose.PSD สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

 A4: ได้ คุณสามารถเข้าถึงเวอร์ชันทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD สำหรับ Java ได้อย่างไร

 A5: หากต้องการขอรับใบอนุญาตชั่วคราว โปรดไปที่[ลิงค์นี้](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
