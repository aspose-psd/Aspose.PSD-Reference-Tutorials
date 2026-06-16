---
date: 2026-05-19
description: เรียนรู้วิธีแปลง PSD เป็น JPEG และหมุนภาพ 270 องศาโดยใช้ Aspose.PSD for
  Java คู่มือนี้แสดงวิธีหมุนไฟล์ PSD, พลิกภาพ, และแปลง PSD เป็น JPEG.
keywords:
- convert psd to jpeg
- how to rotate psd
- flip image java
- rotate psd layer
- rotate image without photoshop
linktitle: หมุนภาพ 270 องศา
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  headline: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  name: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  steps:
  - name: Load the PSD File
    text: '`Image` is Aspose.PSD''s core class that represents a single PSD document
      in memory. Instantiating it reads only the header information, keeping memory
      usage low.'
  - name: Rotate the Image 270 Degrees
    text: '`rotateFlip` performs the specified rotation and optional flip on the image.
      `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise
      while leaving the image orientation unchanged. > **Pro tip:** If you also need
      to flip the image horizontally or vertically, choose a different `Ro'
  - name: Convert PSD to JPEG and Save
    text: '`JpegOptions` defines JPEG‑specific parameters such as compression quality.
      The `save` method writes the transformed image to disk in the desired format.
      The file `RotatedImage_out.jpg` now contains the original PSD content rotated
      270 degrees and saved as a JPEG.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other
      raster formats.
    question: Is Aspose.PSD compatible with different image formats?
  - answer: Absolutely! While `RotateFlipType` provides common angles, you can chain
      multiple calls or use transformation matrices for arbitrary angles.
    question: Can I apply custom rotations, not just predefined flips?
  - answer: Replace `JpegOptions` with `PngOptions` (or the appropriate options class)
      in the `save` method.
    question: How do I convert the rotated PSD to another format, such as PNG?
  - answer: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).
    question: Where can I find additional support or assistance?
  - answer: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: แปลง PSD เป็น JPEG และหมุน 270° ด้วย Aspose.PSD for Java
url: /th/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง PSD เป็น JPEG และหมุนภาพ 270 องศาด้วย Aspose.PSD for Java

## บทนำ

ใน **บทเรียนการประมวลผลภาพด้วย Java** นี้ คุณจะได้เรียนรู้วิธี **แปลง PSD เป็น JPEG** พร้อมกับการหมุนภาพ 270 องศาโดยใช้ Aspose.PSD for Java ไม่ว่าคุณจะสร้าง pipeline การประมวลผลแบบแบตช์, ตัวแก้ไขบนเว็บ, หรือยูทิลิตี้บนเดสก์ท็อป ไลบรารีนี้ช่วยให้คุณจัดการเลเยอร์ PSD ได้โดยไม่ต้องใช้ Photoshop เราจะครอบคลุมการพลิกภาพแบบเลือกได้และแสดงกระบวนการเต็มรูปแบบตั้งแต่การโหลดไฟล์ PSD จนถึงการบันทึกเป็น JPEG

## คำตอบอย่างรวดเร็ว
- **ไลบรารีที่จัดการการหมุนคืออะไร?** Aspose.PSD for Java  
- **มุมการหมุนที่ตัวอย่างใช้คืออะไร?** 270 องศา  
- **ฉันสามารถพลิกภาพได้หรือไม่?** ใช่ – ใช้ตัวเลือก `RotateFlipType` เช่น `Rotate90FlipX`  
- **ฉันบันทึกผลลัพธ์อย่างไร?** ในตัวอย่างเราบันทึกเป็น JPEG ด้วย `JpegOptions`  
- **ฉันต้องใช้ลิขสิทธิ์สำหรับการผลิตหรือไม่?** จำเป็นต้องมีลิขสิทธิ์ Aspose.PSD ที่ถูกต้องสำหรับการใช้งานเชิงพาณิชย์  

## การหมุนภาพ 270 องศาคืออะไร?
การหมุนภาพ 270 องศาหมายถึงการหมุนรูปภาพสามในสี่ของวงกลมเต็มหนึ่งรอบตามเข็มนาฬิกา (หรือ 90 องศาตรงข้ามเข็มนาฬิกา) การจัดแนวนี้มักใช้เพื่อคืนสภาพการจัดวางแนวตั้งเดิมหลังจากการแปลงก่อนหน้า และมักใช้เมื่อภาพถูกจับในโหมดแนวนอนแต่ต้องแสดงในแนวตั้ง ผลลัพธ์คือภาพที่มีการจัดแนวที่ถูกต้องโดยไม่สูญเสียคุณภาพ

## ทำไมต้องใช้ Aspose.PSD สำหรับงานนี้?
Aspose.PSD รองรับ **รูปแบบเข้าและออกกว่า 50 รูปแบบ** — รวมถึง PSD, JPEG, PNG, BMP, GIF, และ TIFF — และสามารถประมวลผลไฟล์ขนาด **ถึง 2 GB** โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ API ทำงานได้บน Java runtime ใดก็ได้ (JDK 8+) ไม่ต้องติดตั้ง Photoshop แบบเนทีฟ และให้คำสั่ง `rotateFlip` เพียงครั้งเดียวที่จัดการการหมุนและการพลิกในขั้นตอนเดียว

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำงาน โปรดตรวจสอบว่าคุณมี:

- **ไลบรารี Aspose.PSD for Java** ติดตั้งแล้ว คุณสามารถดาวน์โหลดและดูเอกสารอ้างอิง API ทั้งหมดได้ [ที่นี่](https://reference.aspose.com/psd/java/)  
- สภาพแวดล้อมการพัฒนา Java (JDK 8 หรือสูงกว่า)  
- ตัวอย่างไฟล์ PSD ที่ต้องการหมุน ปรับค่า `sourceFile` ในโค้ดให้ชี้ไปยังตำแหน่งไฟล์ของคุณ

## นำเข้าแพ็กเกจ

คลาส `Image`, `RotateFlipType` และ `JpegOptions` จำเป็นสำหรับการโหลด, แปลง, และบันทึกไฟล์  
`Image` เป็นคลาสหลักที่แทนเอกสาร PSD ในหน่วยความจำ  
`RotateFlipType` ระบุการหมุนและการพลิกที่รองรับ  
`JpegOptions` กำหนดการตั้งค่าการส่งออก JPEG เช่น คุณภาพ  

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## วิธีแปลง PSD เป็น JPEG หลังจากหมุน?

โหลดไฟล์ PSD ต้นฉบับ, ใช้การหมุน 270 องศา, แล้วบันทึกเป็น JPEG ทันที กระบวนการสามขั้นตอนนี้ใช้เวลาน้อยกว่าสองวินาทีสำหรับภาพ 10 MP ปกติบน CPU สมัยใหม่ ทำให้เหมาะกับงานแบตช์ที่ต้องประมวลผลจำนวนมาก โดยประมวลผลเฉพาะข้อมูลภาพที่จำเป็นเท่านั้น ทำให้การใช้หน่วยความจำน้อยลง และ JPEG ที่ได้ยังคงรักษาความคมชัดของภาพพร้อมลดขนาดไฟล์

### ขั้นตอน 1: โหลดไฟล์ PSD

`Image` เป็นคลาสหลักของ Aspose.PSD ที่แทนเอกสาร PSD หนึ่งไฟล์ในหน่วยความจำ การสร้างอินสแตนซ์จะอ่านเฉพาะข้อมูลส่วนหัว ทำให้การใช้หน่วยความจำต่ำ

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### ขั้นตอน 2: หมุนภาพ 270 องศา

`rotateFlip` ทำการหมุนตามที่ระบุและอาจพลิกภาพได้ตามต้องการ `RotateFlipType.Rotate270FlipNone` หมุนแคนวาส 270 องศาตามเข็มนาฬิกาโดยไม่เปลี่ยนการจัดแนวของภาพ

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **เคล็ดลับ:** หากต้องการพลิกภาพแนวนอนหรือแนวตั้งเพิ่มเติม ให้เลือก `RotateFlipType` อื่น เช่น `Rotate90FlipX` หรือ `Rotate180FlipY`

### ขั้นตอน 3: แปลง PSD เป็น JPEG และบันทึก

`JpegOptions` กำหนดพารามิเตอร์เฉพาะของ JPEG เช่น คุณภาพ การเรียกใช้เมธอด `save` จะเขียนภาพที่แปลงแล้วลงดิสก์ในรูปแบบที่ต้องการ

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

ไฟล์ `RotatedImage_out.jpg` ตอนนี้มีเนื้อหา PSD ดั้งเดิมที่หมุน 270 องศาและบันทึกเป็น JPEG แล้ว

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | วิธีแก้ |
|-------|----------|
| **ภาพปรากฏหัวกลับ** | ตรวจสอบว่าคุณใช้ `Rotate270FlipNone`. สำหรับการหมุน 90 องศาตามเข็มนาฬิกาให้ใช้ `Rotate90FlipNone`. |
| **ไฟล์ผลลัพธ์เสียหาย** | ตรวจสอบว่าโฟลเดอร์ปลายทางมีอยู่และคุณมีสิทธิ์เขียน. |
| **ข้อยกเว้นลิขสิทธิ์** | ติดตั้งลิขสิทธิ์ Aspose.PSD ชั่วคราวหรือถาวรก่อนโหลดภาพในสภาพการผลิต. |

## คำถามที่พบบ่อย

**Q: Aspose.PSD รองรับรูปแบบภาพต่าง ๆ หรือไม่?**  
A: ใช่, Aspose.PSD รองรับ PSD, JPEG, PNG, BMP, GIF, TIFF, และรูปแบบ raster อื่น ๆ อีกหลายรูปแบบ.

**Q: ฉันสามารถใช้การหมุนแบบกำหนดเองได้หรือไม่, ไม่ใช่แค่การพลิกที่กำหนดไว้ล่วงหน้า?**  
A: แน่นอน! แม้ว่า `RotateFlipType` จะให้มุมที่พบบ่อย, คุณสามารถเชื่อมต่อหลายคำสั่งหรือใช้เมทริกซ์การแปลงสำหรับมุมใดก็ได้.

**Q: ฉันจะแปลง PSD ที่หมุนแล้วเป็นรูปแบบอื่น เช่น PNG ได้อย่างไร?**  
A: เปลี่ยน `JpegOptions` เป็น `PngOptions` (หรือคลาส options ที่เหมาะสม) ในเมธอด `save`.

**Q: ฉันจะหาการสนับสนุนหรือความช่วยเหลือเพิ่มเติมได้จากที่ไหน?**  
A: สำหรับความช่วยเหลือจากชุมชน, เยี่ยมชม [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: มีการทดลองใช้งานฟรีหรือไม่?**  
A: ใช่, คุณสามารถสำรวจ Aspose.PSD ด้วย [free trial](https://releases.aspose.com/).

**Q: ฉันจะขอรับลิขสิทธิ์ชั่วคราวได้อย่างไร?**  
A: หากคุณต้องการลิขสิทธิ์ชั่วคราว, คุณสามารถรับได้จาก [ที่นี่](https://purchase.aspose.com/temporary-license/).

**อัปเดตล่าสุด:** 2026-05-19  
**ทดสอบกับ:** Aspose.PSD for Java 24.12  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง

- [แปลง PSD เป็นรูปแบบภาพ Raster ด้วย Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [แปลง PSD เป็น PNG และหมุนเลเยอร์ในไฟล์ PSD ด้วย Java](/psd/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/)
- [วิธีหมุนภาพใน Java ด้วย Aspose.PSD](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}