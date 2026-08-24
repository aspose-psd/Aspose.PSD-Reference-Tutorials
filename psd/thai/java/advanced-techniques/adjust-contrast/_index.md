---
date: 2026-07-27
description: เรียนรู้วิธีแปลง PSD เป็น TIFF และทำการปรับความคอนทราสต์ของภาพโดยใช้
  Aspose.PSD สำหรับ Java ซึ่งเป็นไลบรารี image manipulation library ของ Java ชั้นนำ
keywords:
- convert psd to tiff
- java image processing
- improve image contrast
lastmod: 2026-07-27
linktitle: แปลง PSD เป็น TIFF และปรับความคอนทราสต์
og_description: แปลง PSD เป็น TIFF พร้อมการปรับความคอนทราสต์โดยใช้ Aspose.PSD สำหรับ
  Java คู่มือนี้แสดง code ขั้นตอนต่อขั้นตอน, performance tips, และ export options
  สำหรับ high‑quality TIFF output
og_image_alt: 'Guide: Convert PSD to TIFF and adjust contrast using Aspose.PSD for
  Java'
og_title: แปลง PSD เป็น TIFF & ปรับความคอนทราสต์ – Aspose.PSD Java
schemas:
- author: Aspose
  dateModified: '2026-07-27'
  description: Learn how to convert PSD to TIFF and perform image contrast adjustment
    using Aspose.PSD for Java, a leading java image manipulation library.
  headline: Convert PSD to TIFF and Adjust Contrast with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: It changes the difference between the darkest and brightest pixels, making
      details pop.
    question: What does “adjust contrast” mean?
  - answer: Aspose.PSD for Java – a full‑featured image processing toolkit.
    question: Which library handles this?
  - answer: A **temporary Aspose license** works for testing; a full license is required
      for production.
    question: Do I need a license?
  - answer: Absolutely – we’ll use `TiffOptions` to export the processed image.
    question: Can I convert PSD to TIFF?
  - answer: For a typical 30 MB PSD the whole pipeline runs under one second on a
      modern CPU.
    question: How fast is the conversion?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image manipulation
- tiff export options
title: แปลง PSD เป็น TIFF และปรับความคอนทราสต์ด้วย Aspose.PSD สำหรับ Java
url: /th/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีแปลง PSD เป็น TIFF และปรับความคอนทราสต์ด้วย Aspose.PSD for Java

## บทนำ

หากคุณต้องการ **แปลง PSD เป็น TIFF** พร้อมกับปรับแต่งคุณภาพภาพกราฟิกของคุณให้ดีขึ้น คุณมาถูกที่แล้ว ในบทแนะนำนี้เราจะพาคุณผ่านขั้นตอนการทำงานทั้งหมดโดยใช้ Aspose.PSD for Java—ไลบรารี **java image manipulation** ที่แข็งแกร่ง คุณจะได้เรียนรู้วิธีเพิ่ม **การปรับความคอนทราสต์ของภาพ**, แคชข้อมูลเรสเตอร์ขนาดใหญ่เพื่อประสิทธิภาพ, และสุดท้าย **บันทึกภาพเป็น TIFF** สำหรับการประมวลผลต่อไป มาเริ่มกันเลย!

## คำตอบอย่างรวดเร็ว
- **การปรับความคอนทราสต์หมายถึงอะไร?** มันเปลี่ยนความแตกต่างระหว่างพิกเซลที่มืดที่สุดและสว่างที่สุด ทำให้รายละเอียดเด่นชัดขึ้น.  
- **ไลบรารีใดที่จัดการเรื่องนี้?** Aspose.PSD for Java – ชุดเครื่องมือการประมวลผลภาพแบบครบวงจร.  
- **ฉันต้องการไลเซนส์หรือไม่?** **temporary Aspose license** ใช้ได้สำหรับการทดสอบ; จำเป็นต้องมีไลเซนส์เต็มสำหรับการใช้งานจริง.  
- **ฉันสามารถแปลง PSD เป็น TIFF ได้หรือไม่?** แน่นอน – เราจะใช้ `TiffOptions` เพื่อส่งออกภาพที่ประมวลผลแล้ว.  
- **การแปลงเร็วแค่ไหน?** สำหรับ PSD ขนาดประมาณ 30 MB กระบวนการทั้งหมดทำงานภายในหนึ่งวินาทีบน CPU สมัยใหม่.

## การปรับความคอนทราสต์ของภาพคืออะไร?
การปรับความคอนทราสต์ทำการเปลี่ยนแปลงช่วงโทนของภาพโดยขยายความแตกต่างระหว่างพื้นที่สว่างและมืด ซึ่งมีประโยชน์อย่างยิ่งเมื่อภาพดูแบนหลังจากสแกนหรือเมื่อเตรียมกราฟิกสำหรับการพิมพ์ มันทำงานโดยการยืดหรือบีบฮิสโตแกรมของความเข้มของพิกเซล ทำให้เงาลึกขึ้นและไฮไลท์สว่างขึ้น ซึ่งเพิ่มความลึกและรายละเอียดที่รับรู้ได้.

## ทำไมต้องใช้ Aspose.PSD for Java?
Aspose.PSD ให้เครื่องยนต์ประสิทธิภาพสูงและเต็มคุณสมบัติที่สามารถจัดการ **50+ รูปแบบเรสเตอร์และเวกเตอร์**, ประมวลผลไฟล์ขนาดถึง 500 MB โดยไม่ต้องโหลดเต็มหน่วยความจำ, และส่งออกเป็น TIFF ด้วยการควบคุมที่แม่นยำต่อบิตต่อซัมพล์และการตีความโฟโตเมตริก ความสามารถที่วัดได้เหล่านี้ทำให้เป็นตัวเลือกอันดับต้น ๆ สำหรับไพป์ไลน์ภาพระดับองค์กร.

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำงาน โปรดตรวจสอบว่าคุณมี:

- ความรู้พื้นฐานด้านการเขียนโปรแกรม Java.  
- ไลบรารี Aspose.PSD for Java ติดตั้งแล้ว คุณสามารถดาวน์โหลดได้จาก [here](https://releases.aspose.com/psd/java/).

## นำเข้าแพ็กเกจ

เพิ่มการนำเข้าที่จำเป็นลงในคลาส Java ของคุณ:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## ขั้นตอนที่ 1: โหลดภาพ

คลาส `Image` เป็นจุดเริ่มต้นของ Aspose.PSD ที่แสดงถึงภาพเรสเตอร์ที่รองรับใด ๆ ในหน่วยความจำ.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

เราจะโหลดไฟล์ PSD ต้นฉบับ (`sample.psd`) ลงในอ็อบเจ็กต์ `Image` ซึ่งทำหน้าที่เป็นจุดเริ่มต้นสำหรับการประมวลผลต่อไปทั้งหมด.

## ขั้นตอนที่ 2: แคสต์เป็น RasterImage และแคชข้อมูล

`RasterImage` ให้การเข้าถึงระดับพิกเซลโดยตรงและเปิดใช้งานการแคชสำหรับไฟล์ขนาดใหญ่.  
```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

การแคสต์เป็น `RasterImage` ทำให้เราสามารถทำงานระดับพิกเซลได้ การแคชช่วยปรับปรุงประสิทธิภาพ โดยเฉพาะอย่างยิ่งสำหรับไฟล์ขนาดใหญ่.

## วิธีปรับความคอนทราสต์ของภาพ

เมธอด `adjustContrast` เป็นการเรียก API อย่างง่ายที่เปลี่ยนความคอนทราสต์ของภาพตามค่าร้อยละ.  
```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

เมธอด `adjustContrast` รับจำนวนเต็มที่แสดงถึงการเปลี่ยนแปลงเป็นเปอร์เซ็นต์ ในตัวอย่างนี้เราจะเพิ่มความคอนทราสต์ **50 %**.

## แปลง PSD เป็น TIFF ด้วย Aspose.PSD

`TiffOptions` ให้คุณกำหนดค่าที่เฉพาะเจาะจงของ TIFF เช่น บิตต่อซัมพล์, ประเภทการบีบอัด, และการตีความโฟโตเมตริก.  
```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

ที่นี่เราตั้งค่า `TiffOptions` (บิตต่อซัมพล์, การตีความโฟโตเมตริก) และ **บันทึกภาพเป็น TIFF** ขั้นตอนนี้ทำให้เวิร์กโฟลว์ **แปลง PSD เป็น TIFF** เสร็จสมบูรณ์.

## ปัญหาทั่วไปและวิธีแก้
- **Image not cached:** ควรเรียก `cacheData()` เสมอสำหรับ PSD ขนาดใหญ่เพื่อหลีกเลี่ยง `OutOfMemoryError`.  
- **Unexpected color shift:** ตรวจสอบว่า `setPhotometric` ตรงกับสีเป้าหมายของคุณ (RGB vs. CMYK).  
- **File not found:** ตรวจสอบให้แน่ใจว่า `dataDir` ชี้ไปยังโฟลเดอร์ที่ถูกต้องและชื่อไฟล์สะกดถูกต้อง.

## คำถามที่พบบ่อย

### Q1: Aspose.PSD รองรับรูปแบบภาพต่าง ๆ หรือไม่?
A1: ใช่, Aspose.PSD รองรับ **50+ รูปแบบการนำเข้าและส่งออก**, รวมถึง PSD, TIFF, PNG, JPEG, BMP, และ GIF, ให้ความยืดหยุ่นในการทำงานหลายโครงการ.

### Q2: ฉันจะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร?
A2: คุณสามารถรับไลเซนส์ชั่วคราวได้จาก [here](https://purchase.aspose.com/temporary-license/).

### Q3: ฉันจะหาเอกสารของ Aspose.PSD ได้จากที่ไหน?
A3: เอกสารพร้อมให้บริการที่ [here](https://reference.aspose.com/psd/java/).

### Q4: มีตัวเลือกการสนับสนุนสำหรับ Aspose.PSD อย่างไรบ้าง?
A4: สำหรับการสนับสนุน, เยี่ยมชม [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### Q5: ฉันสามารถซื้อ Aspose.PSD ได้หรือไม่?
A5: ได้, คุณสามารถซื้อ Aspose.PSD ได้จาก [here](https://purchase.aspose.com/buy).

## สรุป

คุณได้เรียนรู้ **วิธีแปลง PSD เป็น TIFF** และทำ **การปรับความคอนทราสต์ของภาพ** ด้วย Aspose.PSD for Java ขั้นตอนเหล่านี้ให้การควบคุมระดับละเอียดต่อคุณภาพภาพในขณะที่รักษาโค้ดให้สะอาดและดูแลได้ง่าย อย่าลังเลที่จะทดลองเมธอดการปรับอื่น ๆ เช่น `adjustBrightness` หรือ `adjustGamma` เพื่อให้ตรงกับความต้องการของคุณ.

**อัปเดตล่าสุด:** 2026-07-27  
**ทดสอบด้วย:** Aspose.PSD for Java 24.12  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [Java Image Processing Tutorial - Adjust Brightness of an Image with Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-brightness/)
- [How to Adjust Gamma in Java Image Processing with Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)
- [Convert PSD to Raster Image Formats with Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}