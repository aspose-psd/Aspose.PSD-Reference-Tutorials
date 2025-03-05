---
title: ปรับคอนทราสต์ของรูปภาพด้วย Aspose.PSD สำหรับ Java
linktitle: ปรับคอนทราสต์ของรูปภาพ
second_title: Aspose.PSD Java API
description: สำรวจโลกแห่งการปรับคอนทราสต์ของภาพใน Java ด้วย Aspose.PSD ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการปรับแต่งภาพที่ราบรื่น
type: docs
weight: 22
url: /th/java/advanced-techniques/adjust-contrast/
---
## การแนะนำ

ในขอบเขตของการประมวลผลภาพด้วย Java Aspose.PSD โดดเด่นในฐานะเครื่องมืออันทรงพลัง ท่ามกลางคุณสมบัติมากมาย การปรับคอนทราสต์ของภาพถือเป็นข้อกำหนดทั่วไป บทช่วยสอนนี้จะแนะนำคุณตลอดขั้นตอนการปรับคอนทราสต์ของภาพโดยใช้ Aspose.PSD สำหรับ Java ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเพิ่งเริ่มต้น คู่มือนี้จะช่วยให้คุณเชี่ยวชาญด้านที่จำเป็นของการปรับแต่งภาพ

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- ความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม Java
-  ติดตั้ง Aspose.PSD สำหรับไลบรารี Java แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/psd/java/).

## แพ็คเกจนำเข้า

ในการเริ่มต้น คุณต้องนำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ เพิ่มบรรทัดต่อไปนี้ลงในโค้ดของคุณ:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## ขั้นตอนที่ 1: โหลดรูปภาพ

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// โหลดรูปภาพที่มีอยู่ลงในอินสแตนซ์ของคลาส RasterImage
Image image = Image.load(sourceFile);
```

 ในขั้นตอนนี้ เราจะโหลดรูปภาพตัวอย่าง ("sample.psd") โดยใช้`Image.load` วิธี.

## ขั้นตอนที่ 2: ส่งไปยัง RasterImage และ Cache Data

```java
// ส่งวัตถุของ Image ไปยัง RasterImage
RasterImage rasterImage = (RasterImage)image;

// ตรวจสอบว่า RasterImage ถูกแคชและ Cache RasterImage เพื่อประสิทธิภาพที่ดีขึ้นหรือไม่
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 ที่นี่เราโยนเรื่องทั่วไป`Image` คัดค้านก`RasterImage` เพื่อการประมวลผลโดยเฉพาะ การแคชข้อมูลรูปภาพช่วยปรับปรุงประสิทธิภาพ

## ขั้นตอนที่ 3: ปรับความคมชัด

```java
// ปรับคอนทราสต์
rasterImage.adjustContrast(50);
```

 ที่`adjustContrast`ใช้สำหรับแก้ไขคอนทราสต์ของภาพ ในตัวอย่างนี้ ความคมชัดจะเพิ่มขึ้น 50%

## ขั้นตอนที่ 4: สร้าง TiffOptions และบันทึก

```java
// สร้างอินสแตนซ์ของ TiffOptions สำหรับรูปภาพผลลัพธ์
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// บันทึกรูปภาพผลลัพธ์เป็นรูปแบบ TIFF
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

 นี่เราจัดให้`TiffOptions` สำหรับภาพที่ส่งออก โดยระบุรูปแบบและคุณสมบัติอื่นๆ ภาพสุดท้ายจะถูกบันทึกลงในไฟล์ TIFF

## บทสรุป

ยินดีด้วย! คุณได้ปรับคอนทราสต์ของรูปภาพโดยใช้ Aspose.PSD สำหรับ Java สำเร็จแล้ว บทช่วยสอนนี้ครอบคลุมขั้นตอนที่สำคัญ ตั้งแต่การนำเข้าแพ็คเกจไปจนถึงการบันทึกอิมเมจที่ประมวลผล

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD เข้ากันได้กับรูปแบบรูปภาพที่แตกต่างกันหรือไม่

ตอบ 1: ใช่ Aspose.PSD รองรับรูปแบบภาพที่หลากหลาย ทำให้โปรเจ็กต์ของคุณมีความยืดหยุ่น

### คำถามที่ 2: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร

 A2: คุณสามารถรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 3: ฉันจะหาเอกสารประกอบ Aspose.PSD ได้ที่ไหน

A3: มีเอกสารประกอบให้[ที่นี่](https://reference.aspose.com/psd/java/).

### คำถามที่ 4: Aspose.PSD มีตัวเลือกการสนับสนุนใดบ้าง

 A4: สำหรับการสนับสนุน โปรดไปที่[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34).

### คำถามที่ 5: ฉันสามารถซื้อ Aspose.PSD ได้หรือไม่

 A5: ได้ คุณสามารถซื้อ Aspose.PSD ได้[ที่นี่](https://purchase.aspose.com/buy).