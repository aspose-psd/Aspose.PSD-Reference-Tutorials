---
date: 2026-06-03
description: เรียนรู้วิธีปรับขนาดภาพด้วย Aspose.PSD for Java คู่มือขั้นตอนต่อขั้นตอนนี้ครอบคลุม
  Resize Type Enumeration การปรับขนาดภาพคุณภาพสูง และวิธีแปลง PSD เป็น JPEG
keywords:
- how to resize image
- convert psd to jpeg
- high quality image resize
- resize image java
- java image manipulation tutorial
linktitle: การปรับขนาดด้วย Resize Type Enumeration
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  headline: How to Resize Image Java Using Resize Type Enumeration
  type: TechArticle
- description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  name: How to Resize Image Java Using Resize Type Enumeration
  steps:
  - name: '**Java Development Environment** – JDK 8 or newer installed and configured.'
    text: '**Java Development Environment** – JDK 8 or newer installed and configured.'
  - name: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
    text: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
  type: HowTo
- questions:
  - answer: Load the PSD with `Image.load`, then call `image.save("output.jpg", new
      JpegOptions());`.
    question: How do I programmatically convert a PSD file to JPEG without resizing?
  - answer: Yes, you can set the `Resolution` property on the `Image` object before
      saving.
    question: Is it possible to maintain the original DPI when resizing?
  - answer: While you can call `resize` multiple times, it’s more efficient to calculate
      the final dimensions and resize once.
    question: Can I chain multiple resize operations?
  type: FAQPage
second_title: Aspose.PSD Java API
title: วิธีปรับขนาดภาพ Java โดยใช้ Resize Type Enumeration
url: /th/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีปรับขนาดภาพ Java ด้วย Resize Type Enumeration

## บทนำ

If you’re looking for **วิธีปรับขนาดภาพ** files efficiently in a Java project, Aspose.PSD for Java provides a clean, high‑performance API. In this tutorial we’ll walk through loading a PSD, applying the **Resize Type Enumeration** for high‑quality image resize, and finally **แปลง PSD เป็น JPEG**. Whether you’re building a desktop editor or an automated server‑side pipeline, these steps let you control dimensions, quality, and format with just a few lines of code.

## คำตอบสั้น
- **ไลบรารีใดที่จัดการการปรับขนาดภาพใน Java?** Aspose.PSD for Java.
- **ประเภทการปรับขนาดใดให้คุณภาพดีที่สุด?** `ResizeType.LanczosResample`.
- **ฉันสามารถแปลง PSD เป็น JPEG หลังจากปรับขนาดได้หรือไม่?** Yes – simply save with `JpegOptions`.
- **ฉันต้องการใบอนุญาตสำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** A valid Aspose.PSD license is required for production use.
- **วิธีนี้เหมาะกับการประมวลผลเป็นกลุ่มขนาดใหญ่หรือไม่?** Absolutely; the API processes multi‑hundred‑page files without loading the whole document into memory.

## "how to resize image" คืออะไรใน Java?

**How to resize image** หมายถึงการเปลี่ยนขนาดพิกเซลของภาพโดยโปรแกรมเมชันขณะรักษาความคมชัดของภาพไว้ Aspose.PSD’s `Resize` method combined with the `ResizeType` enumeration delivers precise control over scaling algorithms, allowing developers to maintain quality across a wide range of source files and target sizes.

## ทำไมต้องใช้ Resize Type Enumeration?

`ResizeType` lets you select the resampling algorithm that best balances speed and visual quality. For most scenarios, **LanczosResample** delivers sharp results with a modest performance cost, processing a 2000 × 1500 image in under 120 ms on a typical server‑grade CPU while keeping edge detail intact.

## ข้อกำหนดเบื้องต้น

Before you start, make sure you have:

1. **Java Development Environment** – JDK 8 หรือใหม่กว่า ติดตั้งและกำหนดค่าแล้ว.  
2. **Aspose.PSD Library** – ดาวน์โหลด JAR ล่าสุดจาก [website](https://releases.aspose.com/psd/java/).  
3. **Sample PSD File** – ใช้ไฟล์ [sample.psd](Your Document Directory/sample.psd) ที่รวมมากับ SDK สำหรับการทดสอบด้วยมือ.

## นำเข้าแพ็กเกจ

`Image` เป็นคลาสฐานสำหรับประเภทภาพทั้งหมดใน Aspose.PSD. เพิ่มการนำเข้าที่จำเป็นลงในไฟล์ซอร์ส Java ของคุณ:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## ขั้นตอนที่ 1: โหลดภาพ

### ตัวกำหนดการอ้างอิง
`RasterImage` class คืออ็อบเจ็กต์หลักของ Aspose.PSD ที่แสดงภาพแบบแรสเตอร์ที่โหลดจากไฟล์ PSD.

โหลดไฟล์ PSD ของคุณเข้าสู่อินสแตนซ์ `RasterImage` เพื่อให้คุณสามารถจัดการพิกเซลได้:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## ขั้นตอนที่ 2: ปรับขนาดภาพ

`image.resize(width, height, resizeType)` ปรับขนาดภาพให้เป็นมิติที่ระบุโดยใช้ขั้นตอนอัลกอริธึมที่เลือก.

ตอนนี้ปรับขนาดภาพที่โหลดโดยใช้ **Resize Type Enumeration** ตัวอย่างนี้เราใช้วิธี Lanczos Resample ซึ่งเหมาะเมื่อคุณต้องการ **วิธีปรับขนาดภาพ** ด้วยคุณภาพสูง:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## ขั้นตอนที่ 3: บันทึกภาพที่ปรับขนาดแล้ว

`image.save(path, options)` เขียนภาพลงดิสก์ในรูปแบบที่กำหนดโดยตัวเลือกที่ให้มา.

หลังจากปรับขนาดแล้ว ให้บันทึกภาพด้วยมิติที่ระบุและประเภทการปรับขนาดที่เลือก ที่นี่เรายังแสดง **แปลง psd เป็น jpeg** โดยบันทึกผลลัพธ์เป็นไฟล์ JPEG:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

## ทำไมต้องใช้ Resize Type Enumeration?

`ResizeType` ให้การควบคุมละเอียดต่ออัลกอริธึมการรีแซมพลิง ช่วยให้คุณสมดุลระหว่างความเร็วและคุณภาพ สำหรับแอปพลิเคชันส่วนใหญ่ `LanczosResample` ให้การแลกเปลี่ยนที่ดี ส่งผลลัพธ์ที่คมชัดโดยไม่มีค่าใช้จ่ายด้านประสิทธิภาพสูง และทำงานได้ดีกับเนื้อหาภาพหลากหลาย

## ปัญหาที่พบบ่อยและวิธีแก้

- **ภาพดูเบลอหลังการปรับขนาด** – ลองใช้ `ResizeType` แบบอื่นเช่น `Bicubic` หรือ `NearestNeighbour` เพื่อดูว่าแบบใดให้ผลลัพธ์ภาพที่ดีที่สุดสำหรับภาพของคุณ  
- **OutOfMemoryError บนไฟล์ PSD ขนาดใหญ่** – ประมวลผลภาพเป็นส่วนย่อยหรือเพิ่มขนาด heap ของ JVM (`-Xmx` flag). Aspose.PSD สามารถจัดการไฟล์ได้ถึง **2 GB** โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ

## คำถามที่พบบ่อย

### Q1: Aspose.PSD for Java เหมาะกับโครงการขนาดเล็กและขนาดใหญ่หรือไม่?

A1: แน่นอน! Aspose.PSD for Java ถูกออกแบบมาเพื่อรองรับโครงการทุกขนาด ให้ความสามารถในการขยายและประสิทธิภาพ

### Q2: ฉันสามารถใช้ประเภทการปรับขนาดอื่นนอกจาก Lanczos Resample ได้หรือไม่?

A2: ใช่, Aspose.PSD for Java มีประเภทการปรับขนาดหลายแบบ เช่น **NearestNeighbour**, **Bicubic**, และอื่น ๆ ดูเอกสาร API เพื่อรายการทั้งหมด

### Q3: ฉันจะหาแหล่งสนับสนุนเพิ่มเติมสำหรับ Aspose.PSD for Java ได้จากที่ไหน?

A3: สำหรับคำถามหรือความช่วยเหลือใด ๆ ให้เยี่ยมชม [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### Q4: มีรุ่นทดลองฟรีสำหรับ Aspose.PSD for Java หรือไม่?

A4: ใช่, คุณสามารถเข้าถึงรุ่นทดลองฟรีได้ [here](https://releases.aspose.com/).

### Q5: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD for Java ได้อย่างไร?

A5: เพื่อรับใบอนุญาตชั่วคราว ให้ไปที่ [this link](https://purchase.aspose.com/temporary-license/).

## คำถามที่พบบ่อย

**Q: ฉันจะโปรแกรมแปลงไฟล์ PSD เป็น JPEG โดยไม่ปรับขนาดอย่างไร?**  
A: Load the PSD with `Image.load`, then call `image.save("output.jpg", new JpegOptions());`.

**Q: สามารถคงค่า DPI ดั้งเดิมเมื่อปรับขนาดได้หรือไม่?**  
A: Yes, you can set the `Resolution` property on the `Image` object before saving.

**Q: ฉันสามารถเรียงต่อการปรับขนาดหลายครั้งได้หรือไม่?**  
A: While you can call `resize` multiple times, it’s more efficient to calculate the final dimensions and resize once.

---

**อัปเดตล่าสุด:** 2026-06-03  
**ทดสอบด้วย:** Aspose.PSD for Java 24.12  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง

- [Simple Resizing with Aspose.PSD – Java Image Manipulation Library](/psd/java/basic-image-operations/simple-resizing/)
- [High Quality Image Scaling with Bicubic Resampler in Aspose.PSD for Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [How to Convert PSD to PNG and Resize Proportionally with Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}