---
date: 2026-02-25
description: เรียนรู้วิธีแปลง PSD เป็น TIFF และปรับความคอนทราสต์ของภาพโดยใช้ Aspose.PSD
  for Java ซึ่งเป็นไลบรารีการจัดการภาพ Java ชั้นนำ
linktitle: Convert PSD to TIFF and Adjust Contrast
second_title: Aspose.PSD Java API
title: วิธีแปลงไฟล์ PSD เป็น TIFF และปรับความคอนทราสต์ด้วย Aspose.PSD สำหรับ Java
url: /th/java/advanced-techniques/adjust-contrast/
weight: 22
---

- How to Adjust Contrast of an Image heading and description.

- Convert PSD to TIFF Using Aspose.PSD heading and description.

- Common Issues and Solutions heading and bullet list.

- Frequently Asked Questions heading and Q&A.

- Conclusion heading and paragraph.

- Last Updated, Tested With, Author lines.

All other content like shortcodes remain.

We need to keep markdown links unchanged.

Translate text but keep technical terms in English.

Let's translate.

Make sure to keep code block placeholders unchanged.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีแปลง PSD เป็น TIFF และปรับคอนทราสต์ด้วย Aspose.PSD for Java

## Introduction

หากคุณต้องการ **แปลง PSD เป็น TIFF** พร้อมกับการปรับคุณภาพภาพให้ดีขึ้น คุณมาถูกที่แล้ว ในบทแนะนำนี้เราจะเดินผ่านขั้นตอนทั้งหมดโดยใช้ Aspose.PSD for Java — ไลบรารี **java image manipulation** ที่แข็งแกร่ง คุณจะได้เรียนรู้วิธีเพิ่ม **image contrast adjustment**, แคชข้อมูล raster ขนาดใหญ่เพื่อประสิทธิภาพ, และสุดท้าย **save image as TIFF** สำหรับการประมวลผลต่อไป ไปดูกันเลย!

## Quick Answers
- **“adjust contrast” หมายถึงอะไร?** มันเปลี่ยนความแตกต่างระหว่างพิกเซลที่มืดที่สุดและสว่างที่สุด ทำให้รายละเอียดเด่นชัดขึ้น  
- **ไลบรารีใดจัดการเรื่องนี้?** Aspose.PSD for Java – ชุดเครื่องมือการประมวลผลภาพครบวงจร  
- **ต้องมีลิขสิทธิ์หรือไม่?** **temporary aspose license** ใช้สำหรับการทดสอบได้; ต้องมีลิขสิทธิ์เต็มสำหรับการใช้งานจริง  
- **ฉันสามารถ **convert PSD to TIFF** ได้หรือไม่?** แน่นอน – เราจะใช้ `TiffOptions` เพื่อส่งออกภาพที่ผ่านการปรับแล้ว  
- **โค้ดใช้เวลารันนานแค่ไหน?** ปกติภายในไม่กี่วินาทีสำหรับไฟล์ PSD ขนาดมาตรฐานบนฮาร์ดแวร์สมัยใหม่

## What is Image Contrast Adjustment?
การปรับคอนทราสต์จะเปลี่ยนช่วงโทนของภาพโดยขยายความแตกต่างระหว่างพื้นที่สว่างและมืด ซึ่งมีประโยชน์อย่างยิ่งเมื่อภาพดูแบนหลังการสแกนหรือเมื่อเตรียมกราฟิกสำหรับการพิมพ์

## Why Use Aspose.PSD for Java?
- **Rich format support** – เปิด, แก้ไข, และ **save image as TIFF**, PNG, JPEG และรูปแบบอื่น ๆ อีกมากมาย  
- **High performance** – การแคชและการปรับแต่ง raster‑image ลดภาระหน่วยความจำ, สำคัญสำหรับไฟล์ PSD ขนาดใหญ่  
- **Straight‑forward API** – การเรียกเมธอดแบบหนึ่งบรรทัดเช่น `adjustContrast` ทำให้โค้ดอ่านง่ายและบำรุงรักษาได้  
- **Comprehensive java image manipulation** ที่เหมาะกับสคริปต์ง่าย ๆ หรือแอปพลิเคชันระดับองค์กร

## Prerequisites

ก่อนเริ่ม, โปรดตรวจสอบว่าคุณมี:

- ความรู้พื้นฐานด้านการเขียนโปรแกรม Java  
- ไลบรารี Aspose.PSD for Java ติดตั้งแล้ว คุณสามารถดาวน์โหลดได้จาก [here](https://releases.aspose.com/psd/java/)

## Import Packages

เพิ่มการ import ที่จำเป็นลงในคลาส Java ของคุณ:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Step 1: Load the Image

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

เราจะโหลดไฟล์ PSD ต้นฉบับ (`sample.psd`) เข้าไปในอ็อบเจกต์ `Image` ซึ่งเป็นจุดเริ่มต้นสำหรับการประมวลผลต่อไปทั้งหมด

## Step 2: Cast to RasterImage and Cache Data

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

การแคสต์เป็น `RasterImage` ทำให้เราสามารถทำงานระดับพิกเซลได้ การแคชข้อมูลช่วยเพิ่มประสิทธิภาพ โดยเฉพาะไฟล์ขนาดใหญ่

## How to Adjust Contrast of an Image

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

เมธอด `adjustContrast` รับค่าจำนวนเต็มที่แทนเปอร์เซ็นต์การเปลี่ยนแปลง ในตัวอย่างนี้เราปรับคอนทราสต์เพิ่ม **50 %**

## Convert PSD to TIFF Using Aspose.PSD

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

ที่นี่เราตั้งค่า `TiffOptions` (bits per sample, photometric interpretation) และ **save image as TIFF** ขั้นตอนนี้ทำให้การ **convert PSD to TIFF** เสร็จสมบูรณ์

## Common Issues and Solutions
- **Image not cached:** ควรเรียก `cacheData()` เสมอสำหรับ PSD ขนาดใหญ่เพื่อหลีกเลี่ยง `OutOfMemoryError`  
- **Unexpected color shift:** ตรวจสอบว่า `setPhotometric` ตรงกับสีเป้าหมายของคุณ (RGB vs. CMYK)  
- **File not found:** ตรวจสอบให้แน่ใจว่า `dataDir` ชี้ไปยังโฟลเดอร์ที่ถูกต้องและชื่อไฟล์สะกดถูกต้อง

## Frequently Asked Questions

### Q1: Aspose.PSD รองรับรูปแบบภาพต่าง ๆ หรือไม่?

A1: ใช่, Aspose.PSD รองรับรูปแบบภาพหลายประเภท ให้ความยืดหยุ่นในโครงการของคุณ

### Q2: จะขอรับ temporary license สำหรับ Aspose.PSD ได้อย่างไร?

A2: คุณสามารถรับ temporary license ได้จาก [here](https://purchase.aspose.com/temporary-license/)

### Q3: จะหาเอกสารของ Aspose.PSD ได้จากที่ไหน?

A3: เอกสารพร้อมให้บริการที่ [here](https://reference.aspose.com/psd/java/)

### Q4: มีตัวเลือกการสนับสนุนอะไรบ้างสำหรับ Aspose.PSD?

A4: สำหรับการสนับสนุน, เยี่ยมชม [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)

### Q5: สามารถซื้อ Aspose.PSD ได้หรือไม่?

A5: ได้, คุณสามารถซื้อ Aspose.PSD ได้จาก [here](https://purchase.aspose.com/buy)

## Conclusion

ตอนนี้คุณรู้แล้วว่า **how to convert PSD to TIFF** และทำ **image contrast adjustment** ด้วย Aspose.PSD for Java ขั้นตอนเหล่านี้ให้การควบคุมคุณภาพภาพอย่างละเอียดพร้อมกับโค้ดที่สะอาดและบำรุงรักษาง่าย อย่าลังเลที่จะลองเมธอดการปรับอื่น ๆ เช่น `adjustBrightness` หรือ `adjustGamma` เพื่อให้ตรงกับความต้องการของคุณ

---

**Last Updated:** 2026-02-25  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}