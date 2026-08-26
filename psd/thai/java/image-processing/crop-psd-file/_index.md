---
date: 2026-08-17
description: เรียนรู้วิธีการตัดไฟล์ psd ด้วย Java โดยใช้ Aspose.PSD for Java – วิธีที่เร็วและแม่นยำในการตัดเอกสาร
  Photoshop ในแอปพลิเคชัน Java ของคุณ
keywords:
- crop psd file java
- aspose.psd java
- java image cropping
lastmod: 2026-08-17
linktitle: ตัดไฟล์ PSD
og_description: ตัดไฟล์ psd ด้วย Java โดยใช้ Aspose.PSD for Java. คู่มือนี้แสดงขั้นตอน
  step‑by‑step วิธีการตัดไฟล์ Photoshop อย่างมีประสิทธิภาพ พร้อมคำอธิบาย code‑free
  และเคล็ดลับ best‑practice
og_image_alt: Guide showing how to crop a PSD file in Java using Aspose.PSD
og_title: ตัดไฟล์ psd ด้วย Java โดยใช้ Aspose.PSD – การตัดภาพที่เร็ว
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  headline: Crop psd file java using Aspose.PSD
  type: TechArticle
- description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  name: Crop psd file java using Aspose.PSD
  steps:
  - name: set document directory
    text: Replace “Your Document Directory” with the absolute or relative path that
      contains the PSD you want to process.
  - name: load PSD file
    text: The `RasterImage` class is Aspose.PSD’s entry point for raster‑based operations
      on a PSD file. Loading the file creates an in‑memory representation that you
      can manipulate.
  - name: define crop area
    text: '`Rectangle` defines the X and Y coordinates together with width and height
      of the region to keep. This class is part of the standard Java AWT package and
      is used by Aspose.PSD to specify cropping bounds.'
  - name: save cropped PSD
    text: After applying the crop, you can persist the result back to PSD format.
      The library writes only the cropped pixels, keeping the original color mode
      and bit depth.
  - name: save cropped image as PNG
    text: If you need a web‑friendly version, export the cropped raster to PNG. Aspose.PSD
      provides PNG save options that let you control compression level and interlacing.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles PSD cropping in Java?
  - answer: Two API calls after loading the image.
    question: How many lines of code are required for a basic crop?
  - answer: Yes, using the built‑in PNG save options.
    question: Can I export the cropped area as PNG?
  - answer: A commercial license is needed beyond the trial period.
    question: Is a license required for production use?
  - answer: Java 8 and later, including Java 11, 17, and 21.
    question: What Java versions are supported?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- crop psd
- aspose.psd
- java image processing
title: ตัดไฟล์ psd ด้วย Java โดยใช้ Aspose.PSD
url: /th/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตัดไฟล์ PSD ด้วย Java โดยใช้ Aspose.PSD

## บทนำ

หากคุณต้องการตัดเอกสาร Photoshop อย่างอัตโนมัติ, **crop psd file java** เป็นงานทั่วไปสำหรับนักพัฒนา Java ที่ทำงานกับกราฟิกพายป์ไลน์, พายป์ไลน์สินทรัพย์, หรือเวิร์กโฟลว์การออกแบบอัตโนมัติ Aspose.PSD for Java มี API เฉพาะที่ให้คุณกำหนดสี่เหลี่ยมและดึงส่วนที่ต้องการออกมาได้ในไม่กี่บรรทัดของโค้ด ในบทแนะนำนี้คุณจะได้เรียนรู้ว่าทำไมไลบรารีนี้จึงออกแบบมาสำหรับการตัดที่มีประสิทธิภาพสูง, วิธีตั้งค่าสภาพแวดล้อมของคุณ, และขั้นตอนที่แน่นอนเพื่อสร้างผลลัพธ์ทั้งในรูปแบบ PSD และ PNG.

## คำตอบอย่างรวดเร็ว
- **ไลบรารีใดจัดการการตัด PSD ใน Java?** Aspose.PSD for Java.
- **ต้องใช้กี่บรรทัดของโค้ดสำหรับการตัดพื้นฐาน?** Two API calls after loading the image.
- **ฉันสามารถส่งออกพื้นที่ที่ตัดเป็น PNG ได้หรือไม่?** Yes, using the built‑in PNG save options.
- **ต้องการใบอนุญาตสำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** A commercial license is needed beyond the trial period.
- **เวอร์ชัน Java ใดที่รองรับ?** Java 8 and later, including Java 11, 17, and 21.

## crop psd file java คืออะไร?

Crop psd file java หมายถึงกระบวนการตัดส่วนสี่เหลี่ยมออกจากเอกสาร Photoshop (.psd) อย่างอัตโนมัติด้วยโค้ด Java ด้วย Aspose.PSD คุณสามารถทำการดำเนินการนี้โดยไม่ต้องเปิด Photoshop ทำให้เหมาะสำหรับพายป์ไลน์ภาพบนเซิร์ฟเวอร์.

## ทำไมต้องใช้ Aspose.PSD for Java?

Aspose.PSD รองรับ **30+ รูปแบบการนำเข้าและส่งออก** และสามารถประมวลผลไฟล์ PSD ขนาดถึง **500 MB** โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ ด้วยสถาปัตยกรรมสตรีมมิ่ง ไลบรารีนี้รักษาชั้น, มาสก์, และโปรไฟล์สีไว้ ทำให้ผลลัพธ์ที่ตัดตรงกับผลลัพธ์ดั้งเดิมของ Photoshop ประสิทธิภาพที่วัดได้นี้ทำให้คุณจัดการงานแบตช์บนฮาร์ดแวร์ทั่วไปได้โดยใช้หน่วยความจำที่คาดการณ์ได้.

## ข้อกำหนดเบื้องต้น

- **สภาพแวดล้อมการพัฒนา Java** – JDK 8 หรือใหม่กว่า ติดตั้งและกำหนดค่าแล้ว.
- **Aspose.PSD for Java** – ดาวน์โหลด JAR ล่าสุดและเอกสาร [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).
- **ไฟล์ PSD ตัวอย่าง** – วางไฟล์ .psd ไว้ในไดเรกทอรีโครงการของคุณเพื่อให้โค้ดสามารถค้นหาได้.

## วิธีการตัดไฟล์ PSD ด้วย Java?

โหลดไฟล์ต้นฉบับ, กำหนดสี่เหลี่ยมที่ต้องการเก็บ, ทำการตัด, และสุดท้ายบันทึกผลลัพธ์ในรูปแบบที่ต้องการ กระบวนการทั้งหมดต้องการเพียงห้าขั้นตอนที่ง่ายต่อการทำตาม แต่ละขั้นตอนมีตัวอย่างโค้ดที่คุณจะต้องใส่โค้ดของคุณเอง.

### ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสาร

แทนที่ “Your Document Directory” ด้วยพาธแบบเต็มหรือแบบสัมพันธ์ที่บรรจุไฟล์ PSD ที่คุณต้องการประมวลผล.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

### ขั้นตอนที่ 2: โหลดไฟล์ PSD

คลาส `RasterImage` เป็นจุดเริ่มต้นของ Aspose.PSD สำหรับการดำเนินการแบบแรสเตอร์บนไฟล์ PSD การโหลดไฟล์จะสร้างการแสดงผลในหน่วยความจำที่คุณสามารถจัดการได้.

```java
String dataDir = "Your Document Directory";
```

### ขั้นตอนที่ 3: กำหนดพื้นที่การตัด

`Rectangle` กำหนดพิกัด X และ Y พร้อมกับความกว้างและความสูงของพื้นที่ที่ต้องการเก็บ คลาสนี้เป็นส่วนหนึ่งของแพ็กเกจ Java AWT มาตรฐานและถูกใช้โดย Aspose.PSD เพื่อระบุขอบเขตการตัด.

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

### ขั้นตอนที่ 4: บันทึก PSD ที่ตัดแล้ว

หลังจากทำการตัดแล้ว คุณสามารถบันทึกผลลัพธ์กลับเป็นรูปแบบ PSD ได้ ไลบรารีจะเขียนเฉพาะพิกเซลที่ตัดออกเท่านั้น รักษาโหมดสีและความลึกบิตเดิมไว้.

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

### ขั้นตอนที่ 5: บันทึกรูปภาพที่ตัดเป็น PNG

หากคุณต้องการเวอร์ชันที่เหมาะกับเว็บ ให้ส่งออกแรสเตอร์ที่ตัดเป็น PNG Aspose.PSD มีตัวเลือกการบันทึก PNG ที่ให้คุณควบคุมระดับการบีบอัดและการเชื่อมต่อระหว่างแถว.

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

## ปัญหาทั่วไปและวิธีแก้

- **พิกัดสี่เหลี่ยมไม่ถูกต้อง** – ตรวจสอบให้แน่ใจว่าค่า X/Y เริ่มที่ 0 ที่มุมซ้ายบน; ค่าติดลบจะทำให้เกิด `ArgumentException`.
- **การใช้หน่วยความจำพุ่งสูงในไฟล์ขนาดใหญ่** – ใช้ตัวเลือก `loadOptions.setLoadOnlyVisibleLayers(true)` เพื่อลดการใช้หน่วยความจำเมื่อไม่ต้องการชั้นที่ซ่อนอยู่.
- **การสูญเสียโปรไฟล์สี** – รักษา ICC profile ดั้งเดิมโดยเรียก `image.getColorProfile()` ก่อนการตัดและกำหนดใหม่หลังจากดำเนินการ.

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ Aspose.PSD for Java เพื่อตัดภาพในรูปแบบอื่นได้หรือไม่?

A1: Aspose.PSD มุ่งเน้นที่ไฟล์ PSD เป็นหลัก แต่ก็รองรับ BMP, GIF, JPEG, PNG, TIFF และรูปแบบแรสเตอร์อื่น ๆ อีกหลายรูปแบบสำหรับการนำเข้าและส่งออก.

### Q2: Aspose.PSD for Java เหมาะกับการประมวลผลภาพขนาดใหญ่หรือไม่?

A2: ใช่ สถาปัตยกรรมสตรีมมิ่งของไลบรารีสามารถประมวลผลไฟล์ PSD หลายร้อยหน้าโดยใช้หน่วยความจำต่ำกว่า 100 MB ทำให้เหมาะสำหรับงานแบตช์.

### Q3: มีข้อพิจารณาเรื่องใบอนุญาตในการใช้ Aspose.PSD for Java หรือไม่?

A3: จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานในสภาพแวดล้อมการผลิต รายละเอียดสามารถดูได้ที่ [Aspose.PSD for Java purchase page](https://purchase.aspose.com/buy).

### Q4: ฉันจะได้รับการสนับสนุนสำหรับปัญหาเกี่ยวกับ Aspose.PSD for Java อย่างไร?

A4: เยี่ยมชม [Aspose.PSD for Java forum](https://forum.aspose.com/c/psd/34) เพื่อถามคำถาม, แบ่งปันโค้ดสแนปช็อต, และรับความช่วยเหลือจากชุมชนและวิศวกรผลิตภัณฑ์.

### Q5: ฉันสามารถทดลองใช้ Aspose.PSD for Java ก่อนซื้อได้หรือไม่?

A5: ใช่, คุณสามารถดาวน์โหลดรุ่นทดลองใช้งานเต็มรูปแบบได้ที่ [Aspose.PSD free trial download](https://releases.aspose.com/).

{{< blocks/products/products-backtop-button >}}

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

## บทแนะนำที่เกี่ยวข้อง

- [ตัดภาพโดยสี่เหลี่ยมใน Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [ตัดภาพโดยการเลื่อนใน Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-shifts/)
- [วิธีการหมุนภาพใน Java ด้วย Aspose.PSD](/psd/java/advanced-image-manipulation/rotate-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}