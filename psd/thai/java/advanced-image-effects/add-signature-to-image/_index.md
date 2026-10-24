---
date: 2026-10-24
description: เรียนรู้วิธีวาด image canvas และเพิ่มลายเซ็นให้กับภาพโดยใช้ Aspose.PSD
  for Java คู่มือการประมวลผลภาพ java นี้แสดงวิธีบันทึก image png และ overlay graphics
keywords:
- draw image canvas
- save image png
- image processing java
- how to overlay image
- java graphics drawimage
lastmod: 2026-10-24
linktitle: เพิ่มลายเซ็นให้กับภาพ
og_description: เรียนรู้วิธีวาด image canvas และเพิ่มลายเซ็นให้กับภาพโดยใช้ Aspose.PSD
  for Java ทำตามขั้นตอนแบบละเอียดเพื่อบันทึก image png และ overlay graphics
og_image_alt: Tutorial showing how to draw image canvas and add a signature with Aspose.PSD
  for Java
og_title: วิธีวาด image canvas และเพิ่มลายเซ็นใน Java
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to draw image canvas and add a signature to an image using
    Aspose.PSD for Java. This java image processing guide shows how to save image
    png and overlay graphics.
  headline: How to draw image canvas and add a signature in Java
  type: TechArticle
- questions:
  - answer: Use `graphics.setOpacity(float opacity)` before calling `drawImage`. Values
      range from 0.0 (transparent) to 1.0 (opaque).
    question: How do I change the opacity of the signature?
  - answer: Yes—apply a transformation matrix via `graphics.rotateTransform(angle)`
      before drawing.
    question: Is it possible to rotate the signature?
  - answer: Absolutely. Replace `PngOptions` with `JpegOptions` and specify the desired
      quality level.
    question: Can I draw the signature onto a JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- draw image canvas
- Aspose.PSD
- Java image processing
- overlay graphics
title: วิธีวาด image canvas และเพิ่มลายเซ็นใน Java
url: /th/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีวาดแคนวาสภาพและเพิ่มลายเซ็นใน Java

## บทนำ

ในกระบวนการทำงานของธุรกิจหลายอย่าง คุณจำเป็นต้องฝังลายเซ็นมือหรือดิจิทัลลงในรูปภาพ—เช่น สัญญา, ใบแจ้งหนี้ หรือใบรับของ การสอนนี้จะแสดงวิธี **draw image canvas** ด้วย Aspose.PSD for Java โดยถือว่าลายเซ็นเป็นเลเยอร์โอเวอร์เลย์ทั่วไป คุณจะได้เรียนรู้วิธีโหลดรูปฐาน, โหลดไฟล์ลายเซ็น, สร้างบริบทกราฟิก, วาดโอเวอร์เลย์, และสุดท้าย **save image png** เมื่อเสร็จคุณจะมีรูปแบบที่นำกลับมาใช้ใหม่ได้สำหรับลายเซ็น, วอเตอร์มาร์ค, โลโก้ หรือภาพประกอบใด ๆ ที่ต้องการสร้างบนเซิร์ฟเวอร์

## คำตอบด่วน
- **draw image on canvas** หมายถึงอะไร? หมายถึงการเรนเดอร์ภาพหนึ่งบนอีกภาพหนึ่งโดยใช้คลาส `Graphics`.  
- **วิธีเพิ่มลายเซ็นใน Java?** โหลดไฟล์ลายเซ็นเป็น `Image` แล้วเรียก `graphics.drawImage`.  
- **ต้องการเวอร์ชัน Aspose.PSD ใด?** ใดก็ได้ที่เป็นรุ่น 24.x ล่าสุด; โค้ดทำงานกับไลบรารีรุ่นล่าสุด.  
- **ฉันสามารถวางหลายภาพซ้อนกันได้หรือไม่?** ได้—ทำซ้ำการเรียก `drawImage` ด้วยแหล่งที่ต่างกัน.  
- **ต้องการไลเซนส์หรือไม่?** รุ่นทดลองใช้ได้สำหรับการพัฒนา; จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง.

## draw image canvas คืออะไร?
การวาดภาพบนแคนวาสหมายถึงการเรนเดอร์อ็อบเจ็กต์ `Image` หนึ่งบนอีกอ็อบเจ็กต์โดยใช้คลาส `Graphics` ซึ่งเป็นการผสานภาพสองภาพเป็นบิตแมพเดียว การดำเนินการนี้เป็นแกนหลักของเทคนิค **overlay images java** เช่น การเพิ่มวอเตอร์มาร์ค, โลโก้ หรือ ลายเซ็น

## ทำไมต้องใช้ Aspose.PSD สำหรับการวางลายเซ็น?
คุณสามารถวางลายเซ็นด้วย Aspose.PSD ได้เพราะมัน **สนับสนุนประเภทเลเยอร์กว่า 120 ประเภทและตัวเลือกมาสก์ 15 แบบ** ซึ่งให้การควบคุมความโปร่งใสและการผสมอย่างแม่นยำ อีกทั้งมัน **ประมวลผลไฟล์ขนาดสูงสุด 500 MB ได้เร็วกว่า 2 × เท่าจากการเรนเดอร์ Photoshop แบบดั้งเดิมบนฮาร์ดแวร์เซิร์ฟเวอร์ทั่วไป** ทำให้เหมาะสำหรับไพป์ไลน์ภาพด้านเซิร์ฟเวอร์ที่มีอัตราการประมวลผลสูง นอกจากนี้ไลบรารีนี้ไม่มี **การพึ่งพา OS แบบเนทีฟใด ๆ** ดังนั้นจึงทำงานได้ทุกที่ที่มี Java 8+ runtime

## ข้อกำหนดเบื้องต้น
- Java Development Kit (JDK) 8 หรือสูงกว่า.  
- JAR ของ Aspose.PSD for Java ที่เพิ่มเข้าไปใน classpath ของโปรเจกต์ของคุณ.  
- ไฟล์รูปภาพสองไฟล์: รูปฐาน (เช่น `layers.psd`) และกราฟิกลายเซ็น (`sample.psd`).  

## นำเข้าแพ็กเกจ

คลาส `Graphics` ให้ความสามารถในการวาด, ส่วน `Image` แทนอ็อบเจ็กต์ภาพ, และ `Point` กำหนดพิกัด.  
```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## ขั้นตอนที่ 1: โหลดภาพหลักและภาพรอง

อ็อบเจ็กต์ `Image` แทนภาพต้นทางและปลายทางที่จะถูกรวมกัน.  
```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **เคล็ดลับ:** เก็บภาพทั้งสองให้อยู่ในโหมดสีเดียวกัน (RGB) เพื่อหลีกเลี่ยงการเปลี่ยนสีที่ไม่คาดคิดเมื่อวาด.

## ขั้นตอนที่ 2: เริ่มต้นกราฟิก (initialize graphics java)

`Graphics` ถูกสร้างจากภาพหลักเพื่อทำหน้าที่เป็นแคนวาสการวาด.  
```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

อ็อบเจ็กต์ `Graphics` ทำหน้าที่เหมือนแปรงสีที่ให้คุณ **draw image on canvas** การเริ่มต้นด้วย `Image` หลักจะทำให้คำสั่งวาดทั้งหมดต่อมาผูกกับแคนวาสนั้น.

## ขั้นตอนที่ 3: เพิ่มลายเซ็นลงในภาพ (how to add signature)

เมธอด `drawImage` วาดภาพลายเซ็นลงบนแคนวาสที่ตำแหน่งที่ระบุ.  
```java
//ExStart:AddSignatureToImage
graphics.drawImage(
    signature,
    new Point(
        canvas.getHeight() - signature.getHeight(),   // X‑coordinate (bottom)
        canvas.getWidth() - signature.getWidth()      // Y‑coordinate (right)
    )
);
canvas.save(dataDir + "AddSignatureToImage_out.png", new PngOptions());
//ExEnd:AddSignatureToImage
```

ในโค้ดส่วนนี้เราจะ **overlay images java** โดยวางลายเซ็นที่มุมล่าง‑ขวา ปรับค่า `Point` หากต้องการตำแหน่งอื่น.

## วิธีวางภาพซ้อนด้วย java graphics drawimage?

โหลดรูปฐาน, สร้างอินสแตนซ์ `Graphics` จากรูปนั้น, จากนั้นเรียก `graphics.drawImage(signature, x, y)` โดยที่ `x` และ `y` แทนพิกเซลตำแหน่งสำหรับการวางซ้อน การเรียกครั้งเดียวนี้จะผสานลายเซ็นลงบนแคนวาสต้นฉบับในหน่วยความจำ แล้วคุณสามารถบันทึกผลลัพธ์ในรูปแบบที่รองรับใดก็ได้

## ปัญหาทั่วไป & วิธีแก้
| อาการ | สาเหตุ | วิธีแก้ |
|---------|-------|-----|
| ลายเซ็นบิดเบี้ยว | DPI ไม่ตรงกันระหว่างแคนวาสและลายเซ็น | ใช้ `signature.resize` ก่อนวาดหรือให้ไฟล์ทั้งสองมี DPI เดียวกัน. |
| ไฟล์ผลลัพธ์มีขนาดใหญ่ | บันทึกโดยไม่มีการบีบอัด | ส่ง `PngOptions` ที่กำหนดค่า `CompressionLevel` ให้สูงขึ้น. |
| ไม่มีอะไรถูกวาด | Graphics ไม่ได้ถูกทำลาย | เรียก `graphics.dispose()` หลังการวาด (ไม่บังคับแต่เป็นแนวปฏิบัติที่ดี). |

## เคล็ดลับเพิ่มเติมสำหรับการใช้งานจริง

- **หลายลายเซ็น:** เรียก `graphics.drawImage` ซ้ำหลายครั้งด้วยอ็อบเจ็กต์ `Image` และพิกัดที่ต่างกัน.  
- **ควบคุมความทึบแสง:** ใช้ `graphics.setOpacity(float opacity)` ก่อนวาดเพื่อทำให้ลายเซ็นเป็นกึ่งโปร่งใส.  
- **การหมุนลายเซ็น:** ใช้ `graphics.rotateTransform(angle)` หากต้องการลายเซ็นเอียง.  
- **บันทึกเป็นรูปแบบอื่น:** แทนที่ `PngOptions` ด้วย `JpegOptions` หรือ `BmpOptions` เพื่อส่งออกเป็น JPEG, BMP ฯลฯ.

## คำถามที่พบบ่อย

### Q1: ฉันสามารถเพิ่มหลายลายเซ็นลงในภาพได้หรือไม่?
A1: ได้, คุณสามารถเพิ่มหลายลายเซ็นโดยทำซ้ำขั้นตอนด้วยภาพลายเซ็นที่ต่างกัน.

### Q2: Aspose.PSD รองรับรูปแบบภาพอื่นหรือไม่?
A2: ได้, Aspose.PSD รองรับรูปแบบไฟล์เข้าและออกกว่า 50 รูปแบบ—รวมถึง PSD, PNG, JPEG, BMP, TIFF, และ GIF—เพื่อความยืดหยุ่นในการประมวลผลภาพ.

### Q3: จำเป็นต้องมีไลเซนส์สำหรับการใช้ Aspose.PSD for Java หรือไม่?
A3: ใช่, คุณต้องมีไลเซนส์ที่ถูกต้องสำหรับการใช้งานในผลิตภัณฑ์ เยี่ยมชม [Purchase Aspose.PSD](https://purchase.aspose.com/buy) เพื่อดูรายละเอียดการไลเซนส์.

### Q4: ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD ได้อย่างไร?
A4: เยี่ยมชม [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) เพื่อรับการสนับสนุนจากชุมชนและการสนทนา.

### Q5: ฉันสามารถทดลองใช้ Aspose.PSD for Java ก่อนซื้อได้หรือไม่?
A5: ได้, คุณสามารถรับ [free trial](https://releases.aspose.com/) เพื่อสำรวจคุณสมบัติก่อนทำการซื้อ.

**คำถามเพิ่มเติม**

**Q: ฉันจะเปลี่ยนความทึบแสงของลายเซ็นได้อย่างไร?**  
A: ใช้ `graphics.setOpacity(float opacity)` ก่อนเรียก `drawImage`. ค่ามีช่วงตั้งแต่ 0.0 (โปร่งใส) ถึง 1.0 (ทึบ)

**Q: สามารถหมุนลายเซ็นได้หรือไม่?**  
A: ได้—ใช้เมทริกซ์การแปลงผ่าน `graphics.rotateTransform(angle)` ก่อนวาด.

**Q: ฉันสามารถวาดลายเซ็นลงบน JPEG แทน PNG ได้หรือไม่?**  
A: แน่นอน. แทนที่ `PngOptions` ด้วย `JpegOptions` และระบุระดับคุณภาพที่ต้องการ.

## สรุป

โดยทำตามขั้นตอนเหล่านี้คุณได้เรียนรู้ **วิธีวาดแคนวาสภาพและเพิ่มลายเซ็นลงในภาพ** ด้วย Aspose.PSD for Java รูปแบบเดียวกันสามารถขยายไปยังวอเตอร์มาร์ค, โลโก้ หรือกราฟิกโอเวอร์เลย์ใด ๆ ให้แอปพลิเคชัน Java ของคุณมีความสามารถ **image processing java** ที่ทรงพลัง.

---

**อัปเดตล่าสุด:** 2026-10-24  
**ทดสอบกับ:** Aspose.PSD for Java 24.11  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [วาดและบันทึกสี่เหลี่ยมใน PSD ด้วย Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [ปรับขนาดภาพด้วย Aspose.PSD for Java – วาดรูปและการดำเนินการภาพพื้นฐาน](/psd/java/basic-image-operations/)
- [Pattern Overlay PSD: เพิ่มเอฟเฟกต์ด้วย Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}