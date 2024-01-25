---
title: ใช้ตัวกรอง Median และ Wiener ด้วย Aspose.PSD สำหรับ Java
linktitle: ใช้ตัวกรองค่ามัธยฐานและ Wiener
second_title: Aspose.PSD Java API
description: สำรวจพลังของการประมวลผลภาพใน Java ด้วย Aspose.PSD เรียนรู้วิธีใช้ตัวกรอง Median และ Wiener ทีละขั้นตอน เพิ่มคุณภาพของภาพได้อย่างง่ายดาย
type: docs
weight: 12
url: /th/java/image-processing/apply-median-wiener-filters/
---
## การแนะนำ

ในขอบเขตของการเขียนโปรแกรม Java Aspose.PSD โดดเด่นในฐานะเครื่องมืออันทรงพลังสำหรับการจัดการและประมวลผลภาพ หนึ่งในฟังก์ชันหลักที่มีให้คือการใช้ฟิลเตอร์ Median และ Wiener ซึ่งมีบทบาทสำคัญในการปรับปรุงคุณภาพของภาพและลดสัญญาณรบกวน คำแนะนำทีละขั้นตอนนี้จะแนะนำคุณตลอดกระบวนการใช้ตัวกรองเหล่านี้โดยใช้ Aspose.PSD สำหรับ Java

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1.  Aspose.PSD สำหรับ Java Library: ดาวน์โหลดและติดตั้งไลบรารีจาก[ที่นี่](https://releases.aspose.com/psd/java/).
2. สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java ไว้ในระบบของคุณ

## แพ็คเกจนำเข้า

เริ่มต้นด้วยการนำเข้าแพ็คเกจที่จำเป็นเพื่อใช้ประโยชน์จากฟังก์ชันการทำงานของ Aspose.PSD ภายในโปรเจ็กต์ Java ของคุณ:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.MedianFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

## การใช้ตัวกรองค่ามัธยฐาน

### ขั้นตอนที่ 1: โหลดรูปภาพ

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

//โหลดภาพต้นฉบับ
Image image = Image.load(sourceFile);
```

### ขั้นตอนที่ 2: ส่งภาพลงใน RasterImage

```java
// ส่งภาพไปที่ RasterImage
RasterImage rasterImage = (RasterImage)image;
if (rasterImage == null) {
    return;
}
```

### ขั้นตอนที่ 3: สร้างอินสแตนซ์ MedianFilterOptions

```java
// สร้างอินสแตนซ์ของคลาส MedianFilterOptions และตั้งค่าขนาดตัวกรอง
MedianFilterOptions options = new MedianFilterOptions(4);
```

### ขั้นตอนที่ 4: ใช้ตัวกรองค่ามัธยฐาน

```java
// ใช้ตัวกรอง MedianFilterOptions กับวัตถุ RasterImage
rasterImage.filter(image.getBounds(), options);
```

### ขั้นตอนที่ 5: บันทึกรูปภาพผลลัพธ์

```java
String destName = dataDir + "median_test_denoise_out.gif";
// บันทึกภาพที่ได้เป็น GIF
image.save(destName, new GifOptions());
```

การทำตามขั้นตอนเหล่านี้ แสดงว่าคุณใช้ตัวกรองค่ามัธยฐานกับรูปภาพของคุณโดยใช้ Aspose.PSD สำหรับ Java ได้สำเร็จ

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจกระบวนการใช้ตัวกรองค่ามัธยฐานและ Wiener โดยใช้ Aspose.PSD สำหรับ Java ตัวกรองเหล่านี้จำเป็นสำหรับการปรับปรุงคุณภาพของภาพและลดสัญญาณรบกวนในแอปพลิเคชัน Java ของคุณ ด้วยการใช้ประโยชน์จากพลังของ Aspose.PSD คุณสามารถรวมฟิลเตอร์เหล่านี้เข้ากับขั้นตอนการประมวลผลภาพของคุณได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ฟิลเตอร์เหล่านี้กับรูปภาพทุกรูปแบบได้หรือไม่

ตอบ 1: ใช่ Aspose.PSD รองรับรูปแบบภาพที่หลากหลาย ทำให้ใช้งานได้หลากหลายสำหรับโปรเจ็กต์ต่างๆ

### คำถามที่ 2: Aspose.PSD สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

 A2: ได้ คุณสามารถทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะได้รับการสนับสนุนสำหรับ Aspose.PSD สำหรับ Java ได้อย่างไร

 A3: เยี่ยมชม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) เพื่อสนับสนุนชุมชน

### คำถามที่ 4: ฉันจะหาเอกสารสำหรับ Aspose.PSD สำหรับ Java ได้ที่ไหน

 A4: โปรดดูเอกสารประกอบ[ที่นี่](https://reference.aspose.com/psd/java/).

### คำถามที่ 5: ฉันจะซื้อ Aspose.PSD สำหรับ Java ได้อย่างไร

 A5: คุณสามารถซื้อผลิตภัณฑ์ได้[ที่นี่](https://purchase.aspose.com/buy).