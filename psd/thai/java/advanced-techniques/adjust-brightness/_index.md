---
title: ปรับความสว่างของภาพด้วย Aspose.PSD สำหรับ Java
linktitle: ปรับความสว่างของภาพ
second_title: Aspose.PSD Java API
description: เพิ่มความสว่างของภาพใน Java ด้วย Aspose.PSD คำแนะนำทีละขั้นตอนในการปรับความสว่างของภาพโดยทางโปรแกรม
weight: 21
url: /th/java/advanced-techniques/adjust-brightness/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ปรับความสว่างของภาพด้วย Aspose.PSD สำหรับ Java

## การแนะนำ

การปรับปรุงรูปภาพเป็นข้อกำหนดทั่วไปในการออกแบบกราฟิกและการถ่ายภาพดิจิทัล Aspose.PSD สำหรับ Java มอบโซลูชันอันทรงพลังสำหรับการปรับความสว่างของภาพโดยทางโปรแกรม ในบทช่วยสอนนี้ เราจะสำรวจวิธีใช้ไลบรารี Aspose.PSD สำหรับ Java เพื่อปรับความสว่างของรูปภาพทีละขั้นตอน

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.PSD สำหรับ Java Library: ดาวน์โหลดและติดตั้งไลบรารีจาก[Aspose.PSD สำหรับเอกสาร Java](https://reference.aspose.com/psd/java/).

## แพ็คเกจนำเข้า

ในการเริ่มต้น ให้นำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ ในตัวอย่างนี้ เราจะใช้สิ่งต่อไปนี้:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

ตอนนี้ เรามาแบ่งขั้นตอนการปรับความสว่างของภาพออกเป็นขั้นตอนง่ายๆ กัน:

## ขั้นตอนที่ 1: โหลดรูปภาพ

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// โหลดรูปภาพที่มีอยู่ลงในอินสแตนซ์ของคลาส RasterImage
Image image = Image.load(sourceFile);
// ส่งวัตถุของ Image ไปยัง RasterImage
RasterImage rasterImage = (RasterImage) image;

// ตรวจสอบว่า RasterImage ถูกแคชและ Cache RasterImage เพื่อประสิทธิภาพที่ดีขึ้นหรือไม่
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 ในขั้นตอนนี้ เราจะโหลดภาพเป้าหมายและส่งไปที่`RasterImage` เพื่อนำไปแปรรูปต่อไป

## ขั้นตอนที่ 2: ปรับความสว่าง

```java
// ปรับความสว่าง
rasterImage.adjustBrightness(-50);
```

 ในที่นี้เราใช้.`adjustBrightness`วิธีการปรับความสว่างของภาพ ในตัวอย่างนี้ เราลดความสว่างลง 50 หน่วย แต่คุณปรับแต่งค่านี้ตามความต้องการของคุณได้

## ขั้นตอนที่ 3: ตั้งค่า TiffOptions

```java
int[] ushort = {8, 8, 8};
// สร้างอินสแตนซ์ของ TiffOptions สำหรับรูปภาพผลลัพธ์
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

 กำหนดค่า`TiffOptions` เพื่อบันทึกภาพที่ปรับแล้ว ปรับ`bitsPerSample` และ`photometric` คุณสมบัติตามความต้องการเฉพาะของคุณ

## ขั้นตอนที่ 4: บันทึกรูปภาพผลลัพธ์

```java
// บันทึกภาพที่ได้
rasterImage.save(destName, tiffOptions);
```

 สุดท้ายให้บันทึกภาพที่แก้ไขโดยใช้ที่ระบุ`TiffOptions`.

## บทสรุป

การปรับความสว่างของภาพโดยทางโปรแกรมทำได้ง่ายด้วย Aspose.PSD สำหรับ Java บทช่วยสอนนี้ได้ให้คำแนะนำที่ครอบคลุมเกี่ยวกับการใช้งานฟังก์ชันนี้ในแอปพลิเคชัน Java ของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถปรับความสว่างในรูปแบบภาพอื่นนอกเหนือจาก PSD ได้หรือไม่

ตอบ 1: ใช่ Aspose.PSD สำหรับ Java รองรับรูปแบบรูปภาพที่หลากหลาย เช่น JPEG, PNG และ TIFF

### คำถามที่ 2: ฉันจะจัดการกับข้อผิดพลาดระหว่างขั้นตอนการปรับแต่งภาพได้อย่างไร

A2: คุณสามารถใช้การจัดการข้อผิดพลาดโดยใช้บล็อก try-catch เพื่อจัดการข้อยกเว้นที่อาจเกิดขึ้น

### คำถามที่ 3: มีการจำกัดช่วงการปรับความสว่างหรือไม่?

A3: ช่วงของการปรับแต่งขึ้นอยู่กับเนื้อหาและรูปแบบของภาพ แต่ Aspose.PSD ให้ความยืดหยุ่นในการปรับแต่ง

### คำถามที่ 4: ฉันสามารถใช้ Aspose.PSD สำหรับ Java ในโครงการเชิงพาณิชย์ได้หรือไม่

 A4: ใช่ Aspose.PSD สำหรับ Java เป็นไลบรารีเชิงพาณิชย์ และคุณสามารถขอรับใบอนุญาตได้จาก[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 5: Aspose.PSD สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

 A5: ได้ คุณสามารถสำรวจห้องสมุดได้โดยทดลองใช้ฟรี[ที่นี่](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
