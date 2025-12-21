---
date: 2025-12-21
description: เรียนรู้วิธีปรับความคอนทราสต์ของภาพโดยใช้ Aspose.PSD for Java ซึ่งเป็นไลบรารีการจัดการภาพ
  Java ชั้นนำ และแปลงไฟล์ PSD เป็น TIFF อย่างมีประสิทธิภาพ
linktitle: Adjust Contrast of an Image
second_title: Aspose.PSD Java API
title: วิธีปรับความคอนทราสต์ของภาพด้วย Aspose.PSD สำหรับ Java
url: /th/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีปรับความคอนทราสต์ของภาพด้วย Aspose.PSD สำหรับ Java

## Introduction

หากคุณกำลังมองหา **วิธีปรับความคอนทราสต์** ในโครงการ Java ของคุณ คุณมาถูกที่แล้ว Aspose.PSD for Java เป็น **ไลบรารีการจัดการภาพ java** ที่ทรงพลังซึ่งช่วยให้คุณปรับแต่งคุณสมบัติต่าง ๆ ของภาพ เช่น ความคอนทราสต์ ความสว่าง และอื่น ๆ อีกมาก ในบทเรียนนี้เราจะเดินผ่านขั้นตอนที่แน่นอนเพื่อเพิ่มความคอนทราสต์ของไฟล์ PSD แล้ว **แปลง PSD เป็น TIFF** สำหรับกระบวนการต่อไป

## Quick Answers
- **‘adjust contrast’ หมายถึงอะไร?** มันเปลี่ยนความแตกต่างระหว่างพิกเซลที่มืดที่สุดและสว่างที่สุด ทำให้รายละเอียดเด่นชัดขึ้น  
- **ไลบรารีที่ทำหน้าที่นี้คืออะไร?** Aspose.PSD for Java – ชุดเครื่องมือการประมวลผลภาพครบวงจร  
- **ฉันต้องการไลเซนส์หรือไม่?** ไลเซนส์ชั่วคราวใช้ได้สำหรับการทดสอบ; ไลเซนส์เต็มจำเป็นสำหรับการใช้งานจริง  
- **ฉันสามารถบันทึกผลลัพธ์เป็น TIFF ได้หรือไม่?** ได้ เราจะใช้ `TiffOptions` เพื่อส่งออกภาพที่ประมวลผลแล้ว  
- **โค้ดใช้เวลารันนานเท่าไหร่?** ปกติใช้เวลาน้อยกว่าวินาทีสำหรับไฟล์ PSD ขนาดมาตรฐาน  

## What is Contrast Adjustment?
การปรับความคอนทราสต์ทำการปรับช่วงโทนของภาพโดยเพิ่มความแตกต่างระหว่างพื้นที่สว่างและมืด ซึ่งมีประโยชน์อย่างยิ่งเมื่อภาพดูแบนหลังการสแกนหรือเมื่อเตรียมกราฟิกสำหรับการพิมพ์  

## Why Use Aspose.PSD for Java?
- **การสนับสนุนรูปแบบที่หลากหลาย** – เปิด แก้ไข และบันทึก PSD, TIFF, PNG, JPEG และอื่น ๆ อีกมากมาย  
- **ประสิทธิภาพสูง** – การแคชและการปรับแต่งภาพแรสเตอร์ช่วยลดการใช้หน่วยความจำ  
- **API ที่ใช้งานง่าย** – การเรียกเมธอดเดียวเช่น `adjustContrast` ทำให้โค้ดอ่านง่าย  

## Prerequisites

- ความรู้พื้นฐานการเขียนโปรแกรม Java  
- ไลบรารี Aspose.PSD for Java ติดตั้งแล้ว คุณสามารถดาวน์โหลดได้จาก [here](https://releases.aspose.com/psd/java/)  

## Import Packages

Add the required imports to your Java class:

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

เราจะโหลดไฟล์ PSD ต้นฉบับ (`sample.psd`) เข้าไปในอ็อบเจกต์ `Image` ซึ่งทำหน้าที่เป็นจุดเริ่มต้นสำหรับการประมวลผลต่อไปทั้งหมด  

## Step 2: Cast to RasterImage and Cache Data

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

การแคสต์เป็น `RasterImage` ทำให้เราสามารถเข้าถึงการดำเนินการระดับพิกเซลได้ การแคชช่วยเพิ่มประสิทธิภาพ โดยเฉพาะอย่างยิ่งสำหรับไฟล์ขนาดใหญ่  

## How to Adjust Contrast of an Image

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

เมธอด `adjustContrast` รับค่าเต็มจำนวนที่แสดงถึงการเปลี่ยนแปลงเป็นเปอร์เซ็นต์ ในตัวอย่างนี้เราจะเพิ่มความคอนทราสต์โดย **50 %**  

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

ที่นี่เราตั้งค่า `TiffOptions` (บิตต่อซัมพล์, การตีความโฟโทเมตริก) แล้วบันทึกภาพที่ปรับความคอนทราสต์แล้วเป็นไฟล์ TIFF  

## Common Issues and Solutions
- **ภาพไม่ได้แคช:** ควรเรียก `cacheData()` เสมอสำหรับ PSD ขนาดใหญ่เพื่อหลีกเลี่ยง `OutOfMemoryError`  
- **สีเปลี่ยนแปลงโดยไม่คาดคิด:** ตรวจสอบว่า `setPhotometric` ตรงกับสีเป้าหมายของคุณ (RGB vs. CMYK)  
- **ไม่พบไฟล์:** ตรวจสอบว่า `dataDir` ชี้ไปยังโฟลเดอร์ที่ถูกต้องและชื่อไฟล์สะกดถูกต้อง  

## Frequently Asked Questions

### Q1: Aspose.PSD รองรับรูปแบบภาพต่าง ๆ หรือไม่?
A1: ใช่, Aspose.PSD รองรับรูปแบบภาพหลายประเภท ให้ความยืดหยุ่นในโครงการของคุณ  

### Q2: ฉันจะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร?
A2: คุณสามารถรับไลเซนส์ชั่วคราวได้จาก [here](https://purchase.aspose.com/temporary-license/)  

### Q3: ฉันสามารถหาเอกสาร Aspose.PSD ได้ที่ไหน?
A3: เอกสารสามารถเข้าถึงได้จาก [here](https://reference.aspose.com/psd/java/)  

### Q4: ตัวเลือกการสนับสนุนสำหรับ Aspose.PSD มีอะไรบ้าง?
A4: สำหรับการสนับสนุน โปรดเยี่ยมชม [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)  

### Q5: ฉันสามารถซื้อ Aspose.PSD ได้หรือไม่?
A5: ใช่, คุณสามารถซื้อ Aspose.PSD ได้จาก [here](https://purchase.aspose.com/buy)  

## Conclusion

ตอนนี้คุณรู้แล้วว่า **วิธีปรับความคอนทราสต์** ของภาพ PSD ด้วย Aspose.PSD for Java และ **วิธีแปลง PSD เป็น TIFF** สำหรับการประมวลผลต่อไป ขั้นตอนเหล่านี้ให้การควบคุมคุณภาพภาพอย่างละเอียดพร้อมโค้ดที่สะอาดและดูแลได้ง่าย อย่าลังเลที่จะทดลองใช้เมธอดการปรับภาพอื่น ๆ เช่น `adjustBrightness` หรือ `adjustGamma` เพื่อให้ตรงกับความต้องการของคุณ  

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}