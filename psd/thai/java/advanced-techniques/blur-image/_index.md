---
date: 2026-08-01
description: เรียนรู้วิธีการเบลอรูปภาพ Java ด้วย Aspose.PSD for Java, ใช้ฟิลเตอร์
  Gaussian blur และแปลง PSD เป็น GIF ในไม่กี่ขั้นตอนง่าย ๆ
keywords:
- blur image java
- apply gaussian blur
- convert psd to gif
- aspose psd conversion
lastmod: 2026-08-01
linktitle: เบลอรูปภาพ
og_description: เบลอรูปภาพ Java อย่างรวดเร็วด้วย Aspose.PSD. เรียนรู้การใช้ Gaussian
  blur, เพิ่มเอฟเฟกต์เบลอ, และแปลง PSD เป็น GIF ในบทเรียน Java สั้น ๆ
og_image_alt: Guide showing Java code to blur an image and convert PSD to GIF using
  Aspose.PSD
og_title: เบลอรูปภาพ Java – เพิ่มเอฟเฟกต์ Gaussian Blur ด้วย Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to blur image java using Aspose.PSD for Java, apply gaussian
    blur filter and convert PSD to GIF in a few simple steps.
  headline: Blur Image Java with Aspose.PSD – Add Blur Effect
  type: TechArticle
- description: Learn how to blur image java using Aspose.PSD for Java, apply gaussian
    blur filter and convert PSD to GIF in a few simple steps.
  name: Blur Image Java with Aspose.PSD – Add Blur Effect
  steps:
  - name: Define File Paths
    text: Set the source PSD file and the destination GIF file. Using absolute or
      correctly resolved relative paths prevents “File not found” errors.
  - name: Load the Image
    text: The `Image` class represents any image format that Aspose.PSD can read.
      Loading a PSD returns a concrete subclass that gives you access to layers and
      raster data.
  - name: Convert to RasterImage
    text: '`RasterImage` is the raster‑based representation required by most filters,
      including Gaussian blur. Casting the loaded image ensures the blur algorithm
      works on pixel data rather than vector information.'
  - name: Apply Blur Filter
    text: '`GaussianBlurFilter` applies a Gaussian kernel with a configurable radius.
      In this example we use a radius of 15 pixels on both the X and Y axes, which
      yields a smooth, natural‑looking blur.'
  - name: Save the Result
    text: '`GifOptions` tells Aspose.PSD to encode the final raster image as a GIF.
      The library handles color quantisation automatically, so the output file size
      stays small without manual tweaking. By following these five steps, you have
      successfully **blurred an image** using Aspose.PSD for Java and saved th'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java.
    question: What library can blur images in Java?
  - answer: Gaussian blur filter.
    question: Which filter creates a smooth blur?
  - answer: Yes – use `GifOptions`.
    question: Can I output to GIF after blurring?
  - answer: A free trial works for testing; a license is required for production.
    question: Do I need a license for development?
  - answer: About 10‑15 minutes for a basic blur.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- blur image java
- Aspose.PSD
- Java image processing
- gaussian blur
- PSD to GIF
title: เบลอรูปภาพ Java ด้วย Aspose.PSD – เพิ่มเอฟเฟกต์เบลอ
url: /th/java/advanced-techniques/blur-image/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เบลอรูปภาพ Java ด้วย Aspose.PSD – เพิ่มเอฟเฟกต์เบลอ

## บทนำ

หากคุณต้องการ **blur image java** อย่างรวดเร็วและเชื่อถือได้ Aspose.PSD for Java จะมอบ API ที่ง่ายต่อการเพิ่มเอฟเฟกต์เบลอให้กับไฟล์ PSD ใด ๆ คำแนะนำ **java image processing tutorial** นี้จะพาคุณผ่านขั้นตอนการ **apply gaussian blur**, การ **convert psd to gif**, และเหตุผลที่คุณอาจต้องการใช้เบลอสำหรับเอฟเฟกต์พื้นหลังในแอปพลิเคชัน Java ขั้นตอนต่าง ๆ ถูกอธิบายด้วยภาษาง่าย ๆ เพื่อให้คุณสามารถทำตามได้แม้จะเป็นมือใหม่กับไลบรารีการประมวลผลภาพ คุณยังสามารถสำรวจไลบรารี Aspose อื่น ๆ ได้ที่ [here](https://releases.aspose.com/).

## คำตอบด่วน
- **ไลบรารีใดที่สามารถเบลอรูปภาพใน Java?** Aspose.PSD for Java.  
- **ฟิลเตอร์ใดที่สร้างการเบลอที่เรียบเนียน?** Gaussian blur filter.  
- **ฉันสามารถส่งออกเป็น GIF หลังจากเบลอได้หรือไม่?** Yes – use `GifOptions`.  
- **ฉันต้องการใบอนุญาตสำหรับการพัฒนาหรือไม่?** A free trial works for testing; a license is required for production.  
- **การทำงานนี้ใช้เวลานานเท่าไหร่?** About 10‑15 minutes for a basic blur.

## blur image java คืออะไร?

การเบลอรูปภาพใน Java หมายถึงการใช้การคอนโวลูชันที่ทำให้รายละเอียดอ่อนลงโดยการเฉลี่ยพิกเซลใกล้เคียง ซึ่งมักใช้เคอร์เนล Gaussian การดำเนินการนี้ลดข้อมูลความถี่สูง ทำให้ได้ลักษณะที่เรียบและดูโฟกัสออก มักใช้สำหรับเอฟเฟกต์พื้นหลัง, การปกปิดความเป็นส่วนตัว, หรือการสไตล์ศิลปะ และสามารถนำไปใช้กับเลเยอร์แรสเตอร์ใด ๆ ภายในไฟล์ PSD

## ทำไมต้องใช้ Aspose.PSD สำหรับงานนี้?

Aspose.PSD มีการทำงาน Gaussian blur ที่พร้อมใช้และมีประสิทธิภาพสูงซึ่งทำงานบนเลเยอร์แรสเตอร์ใด ๆ ภายในไฟล์ PSD ไลบรารีนี้รองรับ **120+ image formats**, สามารถประมวลผลไฟล์ PSD ขนาดสูงสุด **2 GB** โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ และทำงานบนระบบปฏิบัติการใด ๆ ที่รองรับ Java 8+ นอกจากนี้ยังมีการแปลงด้วยคลิกเดียวเป็น GIF, PNG, JPEG และรูปแบบอื่น ๆ อีกมากมาย ทำให้ไม่จำเป็นต้องใช้ไลบรารีภาพเพิ่มเติม

## ข้อกำหนดเบื้องต้น

- ติดตั้ง Java Development Kit (JDK).  
- ไลบรารี Aspose.PSD for Java. คุณสามารถดาวน์โหลดได้จาก [here](https://releases.aspose.com/psd/java/).  
- มีความคุ้นเคยพื้นฐานกับไวยากรณ์ Java.

## นำเข้าแพ็กเกจ

แพ็กเกจ `com.aspose.psd` ให้คลาสหลักสำหรับการโหลด, แก้ไข, และบันทึกเอกสาร Photoshop ก่อนเริ่มเขียนโค้ดให้ทำการนำเข้าคลาสที่จำเป็น

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussianBlurFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: กำหนดเส้นทางไฟล์  
กำหนดไฟล์ PSD ต้นทางและไฟล์ GIF ปลายทาง การใช้เส้นทางแบบเต็มหรือเส้นทางสัมพัทธ์ที่แก้ไขอย่างถูกต้องจะป้องกันข้อผิดพลาด “File not found”

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "BlurAnImage_out.gif";
```

### ขั้นตอนที่ 2: โหลดภาพ  
คลาส `Image` แสดงถึงรูปแบบภาพใด ๆ ที่ Aspose.PSD สามารถอ่านได้ การโหลด PSD จะคืนค่าชั้นย่อยที่เป็นคอนกรีตซึ่งให้คุณเข้าถึงเลเยอร์และข้อมูลแรสเตอร์

```java
// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

### ขั้นตอนที่ 3: แปลงเป็น RasterImage  
`RasterImage` เป็นการแสดงผลแบบแรสเตอร์ที่จำเป็นสำหรับฟิลเตอร์ส่วนใหญ่ รวมถึง Gaussian blur การแคสท์ภาพที่โหลดไว้ทำให้แน่ใจว่าอัลกอริทึมเบลอทำงานบนข้อมูลพิกเซลแทนข้อมูลเวกเตอร์

```java
// Convert the image into RasterImage
RasterImage rasterImage = (RasterImage)image;
```

### ขั้นตอนที่ 4: ใช้ฟิลเตอร์เบลอ  
`GaussianBlurFilter` ใช้เคอร์เนล Gaussian ที่มีรัศมีที่กำหนดได้ ในตัวอย่างนี้เราใช้รัศมี 15 พิกเซลทั้งแกน X และ Y ซึ่งให้ผลการเบลอที่เรียบและดูเป็นธรรมชาติ

```java
// Pass Bounds[rectangle] of the image and GaussianBlurFilterOptions instance to the Filter method
rasterImage.filter(rasterImage.getBounds(), new GaussianBlurFilterOptions(15, 15));
```

### ขั้นตอนที่ 5: บันทึกผลลัพธ์  
`GifOptions` บอกให้ Aspose.PSD เข้ารหัสภาพแรสเตอร์สุดท้ายเป็น GIF ไลบรารีจัดการการควอนไทซ์สีโดยอัตโนมัติ ทำให้ขนาดไฟล์ผลลัพธ์เล็กลงโดยไม่ต้องปรับด้วยตนเอง

```java
// Save the results in GIF format
rasterImage.save(destName, new GifOptions());
```

โดยทำตามขั้นตอนห้าขั้นตอนนี้ คุณได้ **blurred an image** อย่างสำเร็จโดยใช้ Aspose.PSD for Java และบันทึกผลลัพธ์เป็น GIF.

## ทำไมเรื่องนี้ถึงสำคัญ

การเบลอรูปภาพไม่ใช่เพียงการปรับแต่งเชิงสุนทรียะ; มันสามารถปรับปรุงความอ่านง่ายของ UI, ปกป้องข้อมูลที่ละเอียดอ่อน, และสร้างเอฟเฟกต์ความลึกของสนามระดับมืออาชีพ การใช้ Gaussian blur กับ Aspose.PSD ใช้เวลาน้อยกว่า 200 ms สำหรับภาพขนาด 1920×1080 บน CPU 3.0 GHz ปกติ ทำให้เหมาะสำหรับสถานการณ์พรีวิวแบบเรียลไทม์ในแอปพลิเคชันเดสก์ท็อปหรือเว็บ

## กรณีการใช้งานทั่วไป

1. **User‑interface overlays** – ใช้เบลอเบา ๆ เพื่อลดความสว่างของพื้นหลังเมื่อแสดงไดอะล็อกโมดัล  
2. **Privacy protection** – ปิดบังใบหน้า หรือป้ายทะเบียนในภาพก่อนแชร์  
3. **Artistic filters** – รวมหลายรอบการเบลอเพื่อให้ได้ลุคแบบฝัน

## ปัญหาและเคล็ดลับทั่วไป

- **Incorrect file path** – ตรวจสอบให้แน่ใจว่า `dataDir` ลงท้ายด้วยตัวคั่น (`/` หรือ `\`) ที่เหมาะกับ OS ของคุณ  
- **Unsupported image format** – ฟิลเตอร์เบลอทำงานได้เฉพาะบนภาพแรสเตอร์; เลเยอร์เวกเตอร์ต้องแรสเตอร์ไก่อน  
- **Performance** – ภาพขนาดใหญ่กว่าอาจใช้เวลานานขึ้น; พิจารณาปรับขนาดภาพก่อนใช้ฟิลเตอร์หากความเร็วเป็นสิ่งสำคัญ  
- **Memory consumption** – หลังการประมวลผล ให้เรียก `System.gc()` หรือปิดสตรีมหากคุณจัดการหลายภาพในลูป  

## คำถามที่พบบ่อย

### Q1: Aspose.PSD for Java เหมาะกับนักพัฒนามือใหม่หรือไม่?
**A:** แน่นอน! Aspose.PSD มาพร้อมกับเอกสารที่ครอบคลุมและ API ที่ใช้งานง่ายซึ่งช่วยแนะนำนักพัฒนาทุกระดับ

### Q2: ฉันสามารถใช้ Aspose.PSD สำหรับโครงการเชิงพาณิชย์ได้หรือไม่?
**A:** ใช่, คุณสามารถทำได้. เยี่ยมชม [here](https://purchase.aspose.com/buy) เพื่อสำรวจตัวเลือกการให้สิทธิ์

### Q3: มีการทดลองใช้ฟรีหรือไม่?
**A:** มี, คุณสามารถรับการทดลองใช้ฟรีได้ที่ [here](https://releases.aspose.com/)

### Q4: ฉันจะหาแหล่งสนับสนุนสำหรับ Aspose.PSD for Java ได้จากที่ไหน?
**A:** เยี่ยมชม [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) สำหรับคำถามที่เกี่ยวกับการสนับสนุน

### Q5: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD อย่างไร?
**A:** คุณสามารถรับใบอนุญาตชั่วคราวได้ที่ [here](https://purchase.aspose.com/temporary-license/)

## สรุป

Aspose.PSD for Java ทำให้การทำงาน **blur image java** เป็นเรื่องง่าย ไม่ว่าคุณต้องการ **apply gaussian blur**, **add blur effect**, หรือ **convert PSD to GIF**, ไลบรารีจะจัดการทุกอย่างให้ คุณสามารถทดลองกับรัศมีเบลอที่ต่างกัน, ลองรวมฟิลเตอร์, และสำรวจว่า **blur background java** สามารถเพิ่มประสิทธิภาพให้แอปพลิเคชันของคุณได้อย่างไร

---

**อัปเดตล่าสุด:** 2026-08-01  
**ทดสอบด้วย:** Aspose.PSD for Java 24.11  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [แปลง PSD เป็น GIF - ใช้ Gaussian และ Wiener Filters สำหรับภาพสีด้วย Aspose.PSD for Java](/psd/java/image-processing/apply-gaussian-wiener-filters-color-image/)
- [ฟิลเตอร์ขั้นตอนต่อขั้นตอน - ใช้ Motion Wiener Filters ด้วย Aspose.PSD for Java](/psd/java/image-processing/apply-motion-wiener-filters/)
- [วิธีใช้ Gradient Effects ใน Aspose.PSD for Java](/psd/java/advanced-image-effects/add-gradient-effects/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}