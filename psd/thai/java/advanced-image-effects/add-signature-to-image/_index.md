---
date: 2026-04-28
description: เรียนรู้วิธีเพิ่มลายเซ็นลงในภาพโดยการวาดภาพบนแคนวาสด้วย Aspose.PSD for
  Java บทเรียนการประมวลผลภาพด้วย Java นี้แสดงวิธีบันทึกภาพเป็น PNG และวางกราฟิกทับกัน.
keywords:
- add signature to image
- draw image on canvas
- save image as png
- java image processing
- add watermark java
linktitle: เพิ่มลายเซ็นลงในภาพ
second_title: Aspose.PSD Java API
title: เพิ่มลายเซ็นลงในภาพ – วาดภาพบนแคนวาสด้วย Aspose.PSD สำหรับ Java
url: /th/java/advanced-image-effects/add-signature-to-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เพิ่มลายเซ็นลงในภาพ – วาดภาพบนแคนวาสด้วย Aspose.PSD สำหรับ Java

## บทนำ

การเพิ่มลายเซ็นที่เขียนด้วยมือหรือดิจิทัล **add signature to image** เป็นความต้องการทั่วไปสำหรับสัญญา ใบแจ้งหนี้ หรือเอกสารใด ๆ ที่ต้องการหลักฐานความถูกต้อง ในบทเรียนนี้คุณจะได้เห็นว่า Aspose.PSD สำหรับ Java ทำให้คุณสามารถ **draw image on canvas** และถือว่าลายเซ็นเป็นเพียงเลเยอร์โอเวอร์เลย์อีกชั้นหนึ่ง เราจะอธิบายขั้นตอนการโหลดรูปภาพฐาน การโหลดไฟล์ลายเซ็น การเริ่มต้นกราฟิกคอนเท็กซ์ การวาดโอเวอร์เลย์ และสุดท้าย **save image as PNG** เมื่อเสร็จคุณจะมีรูปแบบที่นำกลับมาใช้ได้สำหรับสถานการณ์ **java image processing** ใด ๆ ไม่ว่าจะเป็นลายเซ็น, ลายน้ำ หรือโลโก้

## คำตอบสั้น

- **draw image on canvas** หมายถึงอะไร? หมายถึงการเรนเดอร์ภาพหนึ่งบนอีกภาพหนึ่งโดยใช้คลาส `Graphics`  
- **How to add a signature in Java?** โหลดไฟล์ลายเซ็นเป็น `Image` แล้วใช้ `Graphics.drawImage`  
- **Which Aspose.PSD version is required?** ต้องใช้เวอร์ชัน Aspose.PSD 24.x ล่าสุด; โค้ดทำงานกับไลบรารีล่าสุด  
- **Can I overlay multiple images?** ได้—ทำซ้ำการเรียก `drawImage` ด้วยแหล่งที่มาที่ต่างกัน  
- **Do I need a license?** รุ่นทดลองทำงานสำหรับการพัฒนา; จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานจริง  

## Draw Image on Canvas คืออะไร?

ในคำศัพท์ของ Aspose.PSD การวาดภาพบนแคนวาสหมายถึงการทาสีอ็อบเจ็กต์ `Image` หนึ่งลงบนอีกอ็อบเจ็กต์หนึ่งโดยใช้คอนเท็กซ์ `Graphics` การดำเนินการนี้เป็นหัวใจของเทคนิค **overlay images java** เช่น การเพิ่มลายน้ำ, โลโก้ หรือ ลายเซ็น

## ทำไมต้องใช้ Aspose.PSD สำหรับการวางลายเซ็นทับ?

- **Full PSD support** – ทำงานกับเลเยอร์, มาสก์, และความโปร่งใส  
- **No native OS dependencies** – pure Java, เหมาะสำหรับการประมวลผลบนเซิร์ฟเวอร์  
- **High‑performance rendering** – ปรับให้ทำงานได้อย่างมีประสิทธิภาพกับไฟล์ขนาดใหญ่และการประกอบที่ซับซ้อน  

## ข้อกำหนดเบื้องต้น

- Java Development Kit (JDK) 8 หรือสูงกว่า  
- เพิ่ม JAR ของ Aspose.PSD for Java ไปยัง classpath ของโปรเจคของคุณ  
- ไฟล์รูปภาพสองไฟล์: รูปภาพฐาน (เช่น `layers.psd`) และกราฟิกลายเซ็น (`sample.psd`)  

## นำเข้าแพ็กเกจ

```java
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Point;

import com.aspose.psd.imageoptions.PngOptions;
```

## ขั้นตอนที่ 1: โหลดภาพหลักและภาพรอง

```java
//ExStart:LoadImages
String dataDir = "Your Document Directory";

// Load the primary image (the canvas)
Image canvas = Image.load(dataDir + "layers.psd");

// Load the secondary image containing the signature graphics
Image signature = Image.load(dataDir + "sample.psd");
//ExEnd:LoadImages
```

> **เคล็ดลับ:** เก็บภาพทั้งสองให้อยู่ในโหมดสีเดียวกัน (RGB) เพื่อหลีกเลี่ยงการเปลี่ยนสีที่ไม่คาดคิดเมื่อทำการวาด  

## ขั้นตอนที่ 2: เริ่มต้น Graphics (initialize graphics java)

```java
//ExStart:InitializeGraphics
Graphics graphics = new Graphics(canvas);
//ExEnd:InitializeGraphics
```

อ็อบเจ็กต์ `Graphics` ทำหน้าที่เหมือนแปรงสีที่ให้คุณ **draw image on canvas** การเริ่มต้นด้วย `Image` หลักจะทำให้คำสั่งการวาดทั้งหมดต่อมาถูกผูกกับแคนวาสนั้น  

## ขั้นตอนที่ 3: เพิ่มลายเซ็นลงในภาพ (how to add signature)

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

ในโค้ดตัวอย่างนี้เราจะ **overlay images java** โดยวางลายเซ็นที่มุมล่าง‑ขวา ปรับค่า `Point` หากต้องการตำแหน่งอื่น  

## ปัญหาที่พบบ่อยและวิธีแก้

| อาการ | สาเหตุ | วิธีแก้ |
|---------|-------|-----|
| ลายเซ็นแสดงผิดรูป | DPI ไม่ตรงกันระหว่างแคนวาสและลายเซ็น | ใช้ `signature.resize` ก่อนวาดหรือให้แน่ใจว่าไฟล์ทั้งสองมี DPI เดียวกัน |
| ไฟล์ผลลัพธ์มีขนาดใหญ่ | บันทึกโดยไม่มีการบีบอัด | ส่ง `PngOptions` ที่กำหนดค่า `CompressionLevel` ให้สูงขึ้น |
| ไม่มีการวาดอะไร | Graphics ไม่ได้ถูกทำลาย | เรียก `graphics.dispose()` หลังการวาด (เป็นทางเลือก แต่เป็นแนวปฏิบัติที่ดี) |

## เคล็ดลับเพิ่มเติมสำหรับการใช้งานจริง

- **Multiple signatures:** เรียก `graphics.drawImage` ซ้ำหลายครั้งด้วย `Image` และพิกัดที่ต่างกัน  
- **Opacity control:** ใช้ `graphics.setOpacity(float opacity)` ก่อนวาดเพื่อทำให้ลายเซ็นกึ่งโปร่งใส  
- **Rotating the signature:** ใช้ `graphics.rotateTransform(angle)` หากต้องการลายเซ็นเอียง  
- **Saving to other formats:** แทนที่ `PngOptions` ด้วย `JpegOptions` หรือ `BmpOptions` เพื่อบันทึกเป็น JPEG, BMP ฯลฯ  

## คำถามที่พบบ่อย

### Q1: สามารถเพิ่มลายเซ็นหลายลายลงในภาพได้หรือไม่?

A1: ได้ คุณสามารถเพิ่มลายเซ็นหลายลายได้โดยทำซ้ำขั้นตอนด้วยภาพลายเซ็นที่ต่างกัน  

### Q2: Aspose.PSD รองรับรูปแบบภาพอื่น ๆ หรือไม่?

A2: รองรับ Aspose.PSD รองรับรูปแบบภาพหลายประเภท ทำให้มีความยืดหยุ่นในการประมวลผลภาพ  

### Q3: จำเป็นต้องมีใบอนุญาตสำหรับการใช้ Aspose.PSD for Java หรือไม่?

A3: ใช่ คุณต้องมีใบอนุญาตที่ถูกต้องสำหรับการใช้ Aspose.PSD เยี่ยมชม [ซื้อ Aspose.PSD](https://purchase.aspose.com/buy) สำหรับรายละเอียดการรับใบอนุญาต  

### Q4: จะขอรับการสนับสนุนสำหรับ Aspose.PSD ได้อย่างไร?

A4: เยี่ยมชม [ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) เพื่อรับการสนับสนุนจากชุมชนและการสนทนา  

### Q5: สามารถทดลองใช้ Aspose.PSD for Java ก่อนซื้อได้หรือไม่?

A5: ได้ คุณสามารถรับ [ทดลองใช้ฟรี](https://releases.aspose.com/) เพื่อสำรวจคุณลักษณะก่อนทำการซื้อ  

**Additional FAQs**

**Q: จะเปลี่ยนความโปร่งใสของลายเซ็นได้อย่างไร?**  
A: ใช้ `graphics.setOpacity(float opacity)` ก่อนเรียก `drawImage` ค่าอยู่ระหว่าง 0.0 (โปร่งใส) ถึง 1.0 (ทึบ)

**Q: สามารถหมุนลายเซ็นได้หรือไม่?**  
A: ได้—ใช้เมทริกซ์การแปลงโดย `graphics.rotateTransform(angle)` ก่อนวาด  

**Q: สามารถวาดลายเซ็นลงใน JPEG แทน PNG ได้หรือไม่?**  
A: แน่นอน แทนที่ `PngOptions` ด้วย `JpegOptions` และระบุระดับคุณภาพที่ต้องการ  

## สรุป

โดยทำตามขั้นตอนเหล่านี้คุณได้เรียนรู้ **how to add signature to image** โดย **drawing an image on canvas** ด้วย Aspose.PSD for Java รูปแบบเดียวกันนี้สามารถขยายไปใช้กับลายน้ำ, โลโก้ หรือกราฟิกโอเวอร์เลย์ใด ๆ ทำให้แอปพลิเคชัน Java ของคุณมีความสามารถ **java image processing** ที่ทรงพลัง

---

**Last Updated:** 2026-04-28  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}