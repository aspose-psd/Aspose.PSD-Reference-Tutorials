---
title: ปรับขนาดรูปภาพตามสัดส่วนด้วย Aspose.PSD สำหรับ Java
linktitle: ปรับขนาดภาพตามสัดส่วน
second_title: Aspose.PSD Java API
description: ปรับปรุงแอปพลิเคชัน Java ของคุณด้วย Aspose.PSD ปฏิบัติตามคำแนะนำของเราเพื่อปรับขนาดรูปภาพตามสัดส่วนได้อย่างง่ายดาย เพิ่มความสามารถในการจัดการภาพของคุณวันนี้
weight: 17
url: /th/java/advanced-image-manipulation/resize-image-proportionally/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ปรับขนาดรูปภาพตามสัดส่วนด้วย Aspose.PSD สำหรับ Java

## การแนะนำ

ยินดีต้อนรับสู่คำแนะนำทีละขั้นตอนเกี่ยวกับการปรับขนาดรูปภาพตามสัดส่วนโดยใช้ Aspose.PSD สำหรับ Java หากคุณต้องการปรับปรุงแอปพลิเคชัน Java ของคุณด้วยความสามารถในการปรับขนาดรูปภาพที่มีประสิทธิภาพ คุณมาถูกที่แล้ว ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการโดยใช้ขั้นตอนที่ชัดเจนและกระชับ

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. สภาพแวดล้อม Java: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java บนระบบของคุณแล้ว
2.  ไลบรารี Aspose.PSD: ดาวน์โหลดและติดตั้งไลบรารี Aspose.PSD คุณสามารถค้นหาทรัพยากรที่จำเป็นได้[ที่นี่](https://releases.aspose.com/psd/java/).

## แพ็คเกจนำเข้า

เมื่อคุณเรียงลำดับข้อกำหนดเบื้องต้นแล้ว ให้นำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ ตรวจสอบให้แน่ใจว่าไลบรารี Aspose.PSD ได้รับการอ้างอิงอย่างถูกต้องในโปรเจ็กต์ของคุณ

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## ขั้นตอนที่ 1: โหลดรูปภาพ

เริ่มต้นด้วยการโหลดรูปภาพที่คุณต้องการปรับขนาดลงในแอปพลิเคชัน Java ของคุณ

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## ขั้นตอนที่ 2: ระบุความกว้างและความสูง

กำหนดความกว้างและความสูงใหม่สำหรับรูปภาพที่ปรับขนาดแล้ว ในตัวอย่างนี้ เราจะปรับขนาดรูปภาพให้เหลือครึ่งหนึ่งของขนาดดั้งเดิม

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## ขั้นตอนที่ 3: บันทึกภาพที่ปรับขนาดแล้ว

บันทึกรูปภาพที่ปรับขนาดแล้วไปยังตำแหน่งที่คุณต้องการ โดยระบุตัวเลือกรูปแบบ (PNG ในกรณีนี้)

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

และคุณก็ได้แล้ว! คุณปรับขนาดรูปภาพตามสัดส่วนได้สำเร็จโดยใช้ Aspose.PSD สำหรับ Java

## บทสรุป

ในบทช่วยสอนนี้ เราได้กล่าวถึงขั้นตอนสำคัญในการปรับขนาดรูปภาพตามสัดส่วนโดยใช้ไลบรารี Aspose.PSD สำหรับ Java ตอนนี้คุณสามารถรวมฟังก์ชันนี้เข้ากับแอปพลิเคชัน Java ของคุณได้อย่างง่ายดายเพื่อการจัดการรูปภาพที่ดียิ่งขึ้น

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD เข้ากันได้กับรูปแบบภาพทุกรูปแบบหรือไม่

 A1: Aspose.PSD รองรับรูปแบบภาพที่หลากหลาย รวมถึง PSD, PNG, JPEG และอื่นๆ ตรวจสอบ[เอกสารประกอบ](https://reference.aspose.com/psd/java/) สำหรับรายการที่ครอบคลุม

### คำถามที่ 2: ฉันสามารถใช้ Aspose.PSD สำหรับโครงการเชิงพาณิชย์ได้หรือไม่

 A2: ใช่คุณทำได้ เยี่ยมชม[หน้าซื้อ](https://purchase.aspose.com/buy) สำหรับรายละเอียดใบอนุญาต

### คำถามที่ 3: มีใบอนุญาตชั่วคราวสำหรับการทดสอบหรือไม่

 A3: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/) สำหรับการประเมินผล

### คำถามที่ 4: ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD ได้ที่ไหน

 A4: เยี่ยมชม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) สำหรับการสนับสนุนและช่วยเหลือชุมชน

### คำถามที่ 5: ฉันจะเข้าถึงเอกสาร Aspose.PSD ได้อย่างไร

 A5: โปรดดูเอกสารประกอบโดยละเอียด[ที่นี่](https://reference.aspose.com/psd/java/).
-
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
