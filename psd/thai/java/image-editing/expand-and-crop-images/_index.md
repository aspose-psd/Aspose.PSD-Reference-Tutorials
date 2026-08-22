---
date: 2026-07-08
description: 'บทเรียนไลบรารีการแก้ไขรูปภาพ Java: เรียนรู้วิธีการตัดรูปภาพด้วย Aspose.PSD
  for Java, ปรับขนาด, ขยายแคนวาส, และแปลง PSD เป็น JPEG.'
keywords:
- java image editing library
- java image processing tutorial
- how to crop image java
lastmod: 2026-07-08
linktitle: ขยายและตัดรูปภาพ
og_description: บทเรียนไลบรารีการแก้ไขรูปภาพ Java แสดงวิธีการตัด, ขยายแคนวาส, และแปลง
  PSD เป็น JPEG ด้วย Aspose.PSD for Java ภายในไม่กี่นาที.
og_image_alt: 'Guide: Crop and expand images in Java with Aspose.PSD'
og_title: ไลบรารีการแก้ไขรูปภาพ Java – ตัดรูปภาพด้วย Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: 'Java image editing library tutorial: learn how to crop image java
    using Aspose.PSD for Java, resize, expand canvas, and convert PSD to JPEG.'
  headline: Java Image Editing Library – Crop Image with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles crop image java?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `JpegOptions` together with a cropping rectangle.
    question: Can I convert PSD to JPEG while cropping?
  - answer: Aspose.PSD supports Java 8 and newer versions.
    question: Is Java 8 supported?
  - answer: Typically under 10 minutes for a basic crop operation.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image editing
- Aspose.PSD
- image cropping
- PSD to JPEG
title: ไลบรารีการแก้ไขรูปภาพ Java – ตัดรูปภาพด้วย Aspose.PSD
url: /th/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ไลบรารีการแก้ไขรูปภาพ Java: การครอบรูปภาพ Java ด้วย Aspose.PSD

## บทนำ

ในบทแนะนำนี้คุณจะได้เรียนรู้วิธีใช้ **java image editing library**—โดยเฉพาะ Aspose.PSD for Java—to ครอบ, ขยาย, และแปลงไฟล์ PSD เป็น JPEG. ไม่ว่าคุณจะกำลังเตรียม assets สำหรับเว็บพอร์ทัลหรือทำการสร้าง thumbnail อัตโนมัติ ขั้นตอนด้านล่างจะให้ workflow ที่ทำซ้ำได้และพร้อมใช้งานใน production ที่คุณสามารถรวมเข้าในโปรเจกต์ Java 8+ ใดก็ได้.

## คำตอบอย่างรวดเร็ว
- **ไลบรารีใดที่จัดการการครอบรูปภาพ Java?** Aspose.PSD for Java.  
- **ฉันต้องมีใบอนุญาตสำหรับการพัฒนาหรือไม่?** ทดลองใช้ฟรีทำงานสำหรับการทดสอบ; จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานจริง.  
- **ฉันสามารถแปลง PSD เป็น JPEG ขณะครอบได้หรือไม่?** ได้, โดยใช้ `JpegOptions` ร่วมกับสี่เหลี่ยมครอบ.  
- **รองรับ Java 8 หรือไม่?** Aspose.PSD รองรับ Java 8 และรุ่นใหม่กว่า.  
- **การดำเนินการใช้เวลานานเท่าไหร่?** ปกติใช้เวลาน้อยกว่า 10 นาทีสำหรับการครอบพื้นฐาน.

## “crop image java” คืออะไร

การครอบรูปภาพ Java หมายถึงการเลือกพื้นที่สี่เหลี่ยมผืนผ้าของภาพต้นฉบับและละทิ้งทุกอย่างที่อยู่นอกพื้นที่นั้น. ด้วย Aspose.PSD, คุณสร้าง `Rectangle` ที่กำหนดพื้นที่, นำไปใช้กับ `RasterImage`, แล้วบันทึกผลลัพธ์ในรูปแบบที่รองรับเช่น JPEG.

## ทำไมต้องใช้ Aspose.PSD สำหรับการครอบรูปภาพ Java?

Aspose.PSD ให้ **java image editing library** ที่จัดการไฟล์ PSD ได้โดยตรง, รองรับคุณลักษณะของเลเยอร์มากกว่า 100 ชั้น, และสามารถประมวลผลภาพขนาดสูงสุด 10 000 × 10 000 พิกเซลโดยใช้งานหน่วยความจำต่ำกว่า 500 MB. นอกจากนี้ยังมีการแปลงในตัวเป็น JPEG, PNG, BMP ฯลฯ โดยไม่ต้องใช้เครื่องมือภายนอก ทำให้ไพป์ไลน์การประมวลผลเป็นชุดเร็ว, น่าเชื่อถือ, และง่ายต่อการบำรุงรักษา.

## ข้อกำหนดเบื้องต้น

1. **Java Development Kit (JDK)** – ต้องติดตั้ง Java 8 หรือใหม่กว่า.  
2. **Aspose.PSD for Java** – ดาวน์โหลดไลบรารีจากเว็บไซต์ทางการ **[here](https://releases.aspose.com/psd/java/)**.  

> **Pro tip:** เพิ่ม Aspose.PSD JAR ไปยัง classpath ของโปรเจกต์หรือ dependencies ของ Maven/Gradle เพื่อหลีกเลี่ยง `ClassNotFoundException`.

## นำเข้าแพ็กเกจ

เพิ่ม import ที่จำเป็นในไฟล์ซอร์ส Java ของคุณ. คลาสเหล่านี้ให้คุณเข้าถึงการโหลดภาพ, การจัดการ raster, การกำหนดสี่เหลี่ยม, และตัวเลือกการส่งออก JPEG.

## วิธีการครอบรูปภาพ Java ด้วย Aspose.PSD?

โหลด PSD ต้นฉบับด้วย `RasterImage`, กำหนด `Rectangle` ที่บรรยายพื้นที่ครอบ (ค่าพิกัดลบสามารถขยายแคนวาส), แล้วบันทึกผลลัพธ์ด้วย `JpegOptions`. กระบวนการสามขั้นตอนนี้จัดการทั้งการครอบและการแปลงรูปแบบในขั้นเดียว, ไม่ต้องสร้างไฟล์กลาง.

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสารของคุณ

ระบุโฟลเดอร์ที่มีไฟล์ PSD ต้นฉบับ. แทนที่ placeholder ด้วยพาธจริงบนเครื่องของคุณ.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## ขั้นตอนที่ 2: ระบุเส้นทางต้นทางและปลายทาง

กำหนดตำแหน่งที่จะอ่าน PSD และตำแหน่งที่จะเขียน JPEG ที่ครอบแล้ว.

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 3: โหลดและแคชภาพ

`RasterImage` แทนเวอร์ชัน rasterized ของไฟล์ PSD ในหน่วยความจำ.  
โหลด PSD เข้าไปในอ็อบเจ็กต์ `RasterImage`. การแคชช่วยเพิ่มประสิทธิภาพสำหรับการดำเนินการต่อไปเช่นการครอบ.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## ขั้นตอนที่ 4: สร้าง Rectangle สำหรับการครอบ

`Rectangle` กำหนดพิกัด X, Y และความกว้าง/สูงของพื้นที่ครอบ.  
สร้าง `Rectangle` ที่บรรยายพื้นที่ที่คุณต้องการเก็บ. พิกัดสามารถเป็นค่าลบเพื่อ **ขยาย** แคนวาสก่อนการครอบ, ซึ่งเป็นประโยชน์เมื่อต้องการเพิ่มขอบรอบภาพต้นฉบับ.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

> **ทำไมต้องใช้ค่าพิกัดลบ?**  
> ค่าลบของ X/Y จะเลื่อนพื้นที่ครอบไปทางซ้าย/บน, ทำให้เพิ่มพื้นที่ว่าง (ขยาย) รอบเนื้อหาเดิมก่อนการครอบสุดท้าย.

## ขั้นตอนที่ 5: บันทึกรูปภาพที่ครอบแล้ว

`JpegOptions` ระบุการตั้งค่าสำหรับผลลัพธ์ JPEG, เช่นคุณภาพและการบีบอัด.  
สุดท้ายบันทึกภาพที่ได้โดยใช้ `JpegOptions`. ขั้นตอนนี้ยังแสดง **convert psd jpeg** ขณะใช้สี่เหลี่ยมครอบด้วย.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **ผลลัพธ์:** `jpeg_out.jpg` ตอนนี้มีภาพขนาด 300 × 300 พิกเซลที่ขยายเพิ่ม 200 px ทุกด้านแล้วถูกครอบตามสี่เหลี่ยมที่กำหนด.

ขอแสดงความยินดี! คุณได้ทำ **java image cropping** สำเร็จ, ขยายแคนวาส, และแปลงไฟล์ PSD เป็น JPEG—ทั้งหมดในไม่กี่บรรทัดโค้ดสั้น ๆ.

## กรณีการใช้งานทั่วไป

- **เตรียม assets สำหรับเว็บ** – ครอบและปรับขนาด screenshot หรือดีไซน์ก่อนอัปโหลด.  
- **สร้าง thumbnails** – ดึงส่วนเฉพาะจาก PSD ขนาดใหญ่เพื่อใช้เป็นตัวอย่าง.  
- **ประมวลผลเป็นชุดอัตโนมัติ** – วนลูปผ่านโฟลเดอร์ของไฟล์ PSD, ใช้สี่เหลี่ยมครอบเดียวกันกับแต่ละไฟล์.

## การแก้ไขปัญหาและเคล็ดลับ

| ปัญหา | วิธีแก้แนะนำ |
|-------|----------------|
| `OutOfMemoryError` เมื่อโหลด PSD ขนาดใหญ่ | เรียก `rasterImage.cacheData()` ตั้งแต่ต้นและพิจารณาเพิ่มขนาด heap ของ JVM (`-Xmx`). |
| พื้นที่ที่ครอบอยู่ไม่ตรงกลาง | ตรวจสอบค่า offset X/Y ของสี่เหลี่ยม; จำไว้ว่าค่าลบจะขยายแคนวาส. |
| JPEG ที่ได้ดูเบลอ | ปรับค่าคุณภาพใน `JpegOptions` (เช่น `new JpegOptions { Quality = 90 }`). |

## คำถามที่พบบ่อย

### Q1: Aspose.PSD รองรับเวอร์ชัน Java ต่าง ๆ หรือไม่?

A1: ใช่, Aspose.PSD รองรับ Java 8, 11, 17, และเวอร์ชันใหม่กว่า, ทำให้เข้ากันได้กับสภาพแวดล้อมการพัฒนาต่าง ๆ อย่างกว้างขวาง.

### Q2: ฉันสามารถใช้ Aspose.PSD ในโครงการเชิงพาณิชย์ได้หรือไม่?

A2: แน่นอน, Aspose.PSD มีใบอนุญาตเชิงพาณิชย์สำหรับนักพัฒนา, สามารถใช้ได้ทั้งในแอปพลิเคชันส่วนบุคคลและเชิงพาณิชย์.

### Q3: มีข้อจำกัดใด ๆ เกี่ยวกับรูปแบบไฟล์ภาพที่รองรับหรือไม่?

A3: Aspose.PSD รองรับรูปแบบภาพกว่า 30 แบบ รวมถึง PSD, JPEG, PNG, BMP, TIFF ฯลฯ. ดูรายละเอียดเพิ่มเติมใน [documentation](https://reference.aspose.com/psd/java/).

### Q4: ฉันจะขอรับการสนับสนุนสำหรับคำถามเกี่ยวกับ Aspose.PSD ได้อย่างไร?

A4: เยี่ยมชม [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) เพื่อขอความช่วยเหลือจากชุมชนหรือทีมสนับสนุนของ Aspose.

### Q5: มีการทดลองใช้ฟรีหรือไม่?

A5: มี, คุณสามารถสำรวจ Aspose.PSD ด้วยการทดลองใช้ฟรี. ดาวน์โหลดได้ [here](https://releases.aspose.com/).

---

**อัปเดตล่าสุด:** 2026-07-08  
**ทดสอบกับ:** Aspose.PSD for Java 24.12  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

## การสอนที่เกี่ยวข้อง

- [Simple Resizing with Aspose.PSD – Java Image Manipulation Library](/psd/java/basic-image-operations/simple-resizing/)
- [How to Rotate Image 270 Degrees with Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rotate-image/)
- [How to Adjust Gamma in Java Image Processing with Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}