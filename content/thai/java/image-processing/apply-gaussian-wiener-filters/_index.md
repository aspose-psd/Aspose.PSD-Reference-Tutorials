---
title: ใช้ตัวกรอง Gaussian และ Wiener ใน Aspose.PSD สำหรับ Java
linktitle: ใช้ตัวกรอง Gaussian และ Wiener
second_title: Aspose.PSD Java API
description: ปรับปรุงการประมวลผลภาพ Java ของคุณด้วย Aspose.PSD เรียนรู้การใช้ฟิลเตอร์ Gaussian และ Wiener ทีละขั้นตอนเพื่อให้ได้ผลลัพธ์ภาพที่น่าทึ่ง
type: docs
weight: 10
url: /th/java/image-processing/apply-gaussian-wiener-filters/
---
## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนที่ครอบคลุมของเราเกี่ยวกับการใช้ตัวกรอง Gaussian และ Wiener ใน Aspose.PSD สำหรับ Java! ในคู่มือนี้ เราจะแนะนำคุณตลอดกระบวนการปรับปรุงรูปภาพของคุณโดยใช้ฟิลเตอร์อันทรงพลังเหล่านี้ Aspose.PSD สำหรับ Java มอบชุดคุณสมบัติที่มีประสิทธิภาพสำหรับการประมวลผลภาพ และด้วยการใช้ตัวกรอง Gaussian และ Wiener คุณจะได้ภาพที่นุ่มนวลและละเอียดยิ่งขึ้น

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java บนเครื่องของคุณ

- Aspose.PSD สำหรับไลบรารี Java: ดาวน์โหลดและติดตั้ง Aspose.PSD สำหรับไลบรารี Java คุณสามารถค้นหาลิงค์ดาวน์โหลด[ที่นี่](https://releases.aspose.com/psd/java/).

## แพ็คเกจนำเข้า

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าแพ็คเกจที่จำเป็นสำหรับ Aspose.PSD ต่อไปนี้คือตัวอย่างคำสั่งนำเข้าเพื่อช่วยคุณเริ่มต้น:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

ตอนนี้ เราจะแจกแจงตัวอย่างออกเป็นหลายขั้นตอนเพื่อใช้ตัวกรอง Gaussian และ Wiener

## ขั้นตอนที่ 1: โหลดรูปภาพ

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);
RasterImage rasterImage = (RasterImage)image;
```

ในขั้นตอนนี้ เราจะโหลดไฟล์รูปภาพ PSD จากไดเร็กทอรีที่ระบุ

## ขั้นตอนที่ 2: ตรวจสอบภาพแรสเตอร์

```java
if (rasterImage == null) {
    return;
}
```

ตรวจสอบให้แน่ใจว่าภาพที่โหลดนั้นเป็นภาพแรสเตอร์ที่ถูกต้อง มิฉะนั้น กระบวนการจะยุติลง

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกตัวกรอง

```java
GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
options.setGrayscale(true);
```

สร้างอินสแตนซ์ของ GaussWienerFilterOptions ตั้งค่าขนาดรัศมี ค่าที่ราบรื่น และระบุว่าคุณต้องการใช้ตัวกรองในระดับสีเทาหรือไม่

## ขั้นตอนที่ 4: ใช้ตัวกรองและบันทึก

```java
rasterImage.filter(image.getBounds(), options);
String destName = dataDir + "gauss_wiener_out.gif";
image.save(destName, new GifOptions());
```

สุดท้าย ใช้ตัวกรอง Gaussian และ Wiener ที่กำหนดค่าไว้กับ RasterImage และบันทึกภาพที่ได้ในรูปแบบ GIF

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีใช้ตัวกรอง Gaussian และ Wiener โดยใช้ Aspose.PSD สำหรับ Java เรียบร้อยแล้ว ทดลองใช้พารามิเตอร์ต่างๆ เพื่อให้ได้การปรับปรุงภาพที่ต้องการ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ตัวกรองเหล่านี้กับรูปภาพในรูปแบบอื่นที่ไม่ใช่ PSD ได้หรือไม่

A1: ใช่ Aspose.PSD สำหรับ Java รองรับรูปแบบรูปภาพที่หลากหลายนอกเหนือจาก PSD

### คำถามที่ 2: Aspose.PSD สำหรับ Java เวอร์ชันทดลองมีข้อจำกัดใดๆ หรือไม่

A2: เวอร์ชันทดลองใช้มีข้อจำกัด และคุณสามารถสำรวจความสามารถทั้งหมดได้โดยการได้รับใบอนุญาตที่ถูกต้อง

### คำถามที่ 3: ฉันจะได้รับการสนับสนุนสำหรับ Aspose.PSD สำหรับ Java ได้อย่างไร

 A3: เยี่ยมชม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) สำหรับการสนับสนุนและการอภิปรายของชุมชน

### คำถามที่ 4: มีใบอนุญาตชั่วคราวสำหรับการทดสอบหรือไม่

 A4: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 5: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose.PSD สำหรับ Java ได้ที่ไหน

 A5: โปรดดูที่[เอกสารประกอบ](https://reference.aspose.com/psd/java/) เพื่อข้อมูลเชิงลึก