---
title: ครอบตัดรูปภาพตามสี่เหลี่ยมผืนผ้าใน Aspose.PSD สำหรับ Java
linktitle: ครอบตัดรูปภาพตามสี่เหลี่ยมผืนผ้า
second_title: Aspose.PSD Java API
description: สำรวจความสามารถในการครอบตัดภาพที่ราบรื่นใน Java ด้วย Aspose.PSD ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อครอบตัดรูปภาพอย่างง่ายดายโดยใช้ Aspose.PSD สำหรับ Java
weight: 15
url: /th/java/image-editing/crop-image-by-rectangle/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ครอบตัดรูปภาพตามสี่เหลี่ยมผืนผ้าใน Aspose.PSD สำหรับ Java

## การแนะนำ

ในโลกของการพัฒนา Java การจัดการรูปภาพเป็นงานทั่วไป และ Aspose.PSD สำหรับ Java มอบโซลูชันอันทรงพลังสำหรับการประมวลผลรูปภาพ ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการครอบตัดรูปภาพตามสี่เหลี่ยมโดยใช้ Aspose.PSD สำหรับ Java ทำตามขั้นตอนด้านล่างเพื่อให้บรรลุเป้าหมายนี้อย่างง่ายดาย

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- ติดตั้ง Java Development Kit (JDK) บนเครื่องของคุณแล้ว
- Aspose.PSD สำหรับไลบรารี Java คุณสามารถดาวน์โหลดได้จาก[เว็บไซต์](https://releases.aspose.com/psd/java/).

## แพ็คเกจนำเข้า

ตรวจสอบให้แน่ใจว่าได้รวมแพ็คเกจที่จำเป็นในโปรเจ็กต์ Java ของคุณเพื่อใช้ประโยชน์จากความสามารถของ Aspose.PSD สำหรับ Java เพิ่มคำสั่งนำเข้าต่อไปนี้ที่จุดเริ่มต้นของไฟล์ Java ของคุณ:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

ตอนนี้ เรามาแบ่งกระบวนการออกเป็นหลายขั้นตอนเพื่อแนะนำคุณเกี่ยวกับการครอบตัดรูปภาพตามสี่เหลี่ยมโดยใช้ Aspose.PSD สำหรับ Java

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสารของคุณ

```java
String dataDir = "Your Document Directory";
```

 แทนที่`"Your Document Directory"` ด้วยเส้นทางจริงที่มีไฟล์ PSD ของคุณอยู่

## ขั้นตอนที่ 2: ระบุไฟล์ต้นทางและปลายทาง

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

กำหนดเส้นทางสำหรับไฟล์ PSD ต้นทางและไฟล์ JPEG ปลายทาง

## ขั้นตอนที่ 3: โหลดและแคชรูปภาพ

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 โหลดภาพ PSD ลงในไฟล์`RasterImage` อินสแตนซ์และแคชข้อมูล

## ขั้นตอนที่ 4: สร้างและกำหนดสี่เหลี่ยมครอบตัด

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

 สร้างอินสแตนซ์ของ`Rectangle` คลาสที่มีขนาดที่ต้องการสำหรับการครอบตัด

## ขั้นตอนที่ 5: ครอบตัดและบันทึกรูปภาพ

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

ดำเนินการครอบตัดโดยใช้สี่เหลี่ยมที่ระบุและบันทึกผลลัพธ์เป็นไฟล์ JPEG

ทำซ้ำขั้นตอนเหล่านี้ตามความจำเป็น โดยปรับพารามิเตอร์ตามความต้องการเฉพาะของคุณ

## บทสรุป

ในบทช่วยสอนนี้ เราได้อธิบายขั้นตอนการครอบตัดรูปภาพตามสี่เหลี่ยมโดยใช้ Aspose.PSD สำหรับ Java ด้วยการทำตามขั้นตอนเหล่านี้ คุณสามารถรวมความสามารถในการจัดการรูปภาพอันทรงพลังเข้ากับแอปพลิเคชัน Java ของคุณได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.PSD สำหรับ Java กับเฟรมเวิร์ก Java อื่นได้หรือไม่

ตอบ 1: ได้ Aspose.PSD สำหรับ Java สามารถรวมเข้ากับเฟรมเวิร์ก Java ต่างๆ ได้ ซึ่งให้ความยืดหยุ่นในโครงการพัฒนาของคุณ

### คำถามที่ 2: Aspose.PSD สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

 A2: ได้ คุณสามารถเข้าถึงเวอร์ชันทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะรับการสนับสนุนหรือความช่วยเหลือเพิ่มเติมได้จากที่ไหน

 A3: เยี่ยมชม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) สำหรับการสนับสนุนและการอภิปรายของชุมชน

### คำถามที่ 4: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD สำหรับ Java ได้อย่างไร

 A4: คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 5: รูปแบบรูปภาพที่รองรับสำหรับการครอบตัดใน Aspose.PSD สำหรับ Java คืออะไร

A5: Aspose.PSD สำหรับ Java รองรับรูปแบบรูปภาพที่หลากหลาย รวมถึง PSD, PNG, JPEG และอื่นๆ
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
