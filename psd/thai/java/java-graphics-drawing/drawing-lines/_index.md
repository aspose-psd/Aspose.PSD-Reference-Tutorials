---
date: 2026-09-08
description: เรียนรู้วิธี java graphics draw line ในไฟล์ PSD ด้วย Aspose.PSD for Java
  คู่มือฉบับนี้แสดง draw lines java พร้อมขั้นตอนที่ชัดเจนและตัวอย่างโค้ด
keywords:
- java graphics draw line
- draw lines java
- how to draw lines java
lastmod: 2026-09-08
linktitle: การวาดเส้นใน Java
og_description: ค้นพบวิธี java graphics draw line ใน Java ด้วย Aspose.PSD ทำตามคำแนะนำขั้นตอนต่อขั้นตอนเพื่อ
  draw lines java ในไฟล์ PSD อย่างรวดเร็ว
og_image_alt: Screenshot of Java code drawing lines in a PSD file using Aspose.PSD
og_title: วิธี java graphics draw line ใน Java ด้วย Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to java graphics draw line in PSD files using Aspose.PSD
    for Java. This guide shows draw lines java with clear steps and code examples.
  headline: How to java graphics draw line in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library is required?
  - answer: java graphics draw line.
    question: Which primary keyword does this tutorial target?
  - answer: Yes – a free trial license is available.
    question: Do I need a license to try it?
  - answer: The library works on Windows, Linux, and macOS.
    question: Can I run this on any OS?
  - answer: About 10‑15 minutes for a basic line drawing.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- PSD line drawing
- Java image processing
title: วิธี java graphics draw line ใน Java
url: /th/java/java-graphics-drawing/drawing-lines/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การวาดเส้นใน Java

## บทนำ
ในบทแนะนำนี้คุณจะได้เรียนรู้วิธี **java graphics draw line** ในไฟล์ PSD ด้วย Aspose.PSD for Java การวาดเส้นโดยโปรแกรมช่วยให้คุณอัตโนมัติการสร้างกราฟิก เพิ่มคำอธิบาย หรือสร้างสินทรัพย์การออกแบบโดยไม่ต้องเปิด Photoshop เมื่อจบคู่มือคุณจะสามารถวาดเส้นแบบจุดและเส้นทึบได้ด้วยเพียงไม่กี่บรรทัดของโค้ด Java

## คำตอบอย่างรวดเร็ว
- **ต้องการไลบรารีอะไร?** Aspose.PSD for Java.  
- **คีย์เวิร์ดหลักที่บทแนะนำนี้มุ่งเป้า?** java graphics draw line.  
- **ต้องการใบอนุญาตเพื่อทดลองหรือไม่?** Yes – a free trial license is available.  
- **สามารถรันบนระบบปฏิบัติการใดก็ได้หรือไม่?** The library works on Windows, Linux, and macOS.  
- **ใช้เวลานานเท่าไหร่ในการทำงานนี้?** About 10‑15 minutes for a basic line drawing.

## java graphics draw line คืออะไร?
คำว่า `java graphics draw line` หมายถึงกระบวนการใช้ API กราฟิกที่พัฒนาด้วย Java เพื่อวาด primitive เส้นตรงบนแคนวาสของภาพ ในบทแนะนำนี้ไลบรารี Aspose.PSD จะให้คลาส `Graphics` ซึ่งมีเมธอด `drawLine` ที่รับพารามิเตอร์ `Pen` และค่าพิกัดเพื่อสร้างเส้น

## ทำไมต้องใช้ Aspose.PSD สำหรับการวาดเส้น?
Aspose.PSD มีเอนจินที่แข็งแรงและใช้หน่วยความจำน้อยสำหรับจัดการไฟล์ Photoshop โดยตรงจากโค้ด Java รองรับรูปภาพและเอกสารมากกว่า 70 รูปแบบ สามารถทำงานกับไฟล์ PSD ขนาดถึง 2 GB โดยไม่ต้องโหลดเต็มไฟล์ และให้การดำเนินการวาดที่มีประสิทธิภาพสูง ทำให้เหมาะสำหรับการประมวลผลแบบแบตช์และการสร้างกราฟิกอัตโนมัติ

## ข้อกำหนดเบื้องต้น
- ความรู้พื้นฐานของภาษาโปรแกรม Java.  
- JDK (Java Development Kit) ติดตั้งบนระบบของคุณ.  
- ไลบรารี Aspose.PSD for Java ดาวน์โหลดและตั้งค่าในสภาพแวดล้อมการพัฒนาของคุณ.

## นำเข้าแพ็กเกจ
การนำเข้าต่อไปนี้จะนำเข้าคลาส Aspose.PSD ที่จำเป็นสำหรับการสร้างภาพ การจัดการกราฟิก และการจัดการสี.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Point;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## ขั้นตอนที่ 1: ตั้งค่าโปรเจกต์ของคุณ
เริ่มต้นด้วยการสร้างโปรเจกต์ Java ใหม่ใน IDE ของคุณและเพิ่ม Aspose.PSD for Java ลงใน dependencies ของคุณ คุณสามารถดาวน์โหลดไลบรารีได้จาก [Aspose.PSD for Java Download](https://releases.aspose.com/psd/java/).

## ขั้นตอนที่ 2: เริ่มต้นภาพ PSD
คลาส `PsdImage` แทนเอกสาร Photoshop และให้คุณสร้างแคนวาส PSD ว่างใหม่ด้วยขนาดที่กำหนด.
```java
String dataDir = "Your Document Directory";
String outpath = dataDir + "Lines.psd";
Image image = new PsdImage(100, 100);
```

## ขั้นตอนที่ 3: เริ่มต้นอ็อบเจ็กต์กราฟิก
`Graphics` คือคลาสหลักของ Aspose.PSD สำหรับการวาดรูปทรง, ข้อความ, และเส้นบนแคนวาส PSD.  
สร้างอินสแตนซ์ของคลาส Graphics และล้างพื้นผิวกราฟิก:
```java
Graphics graphic = new Graphics(image);
graphic.clear(Color.getYellow());
```

## วิธีการ java graphics draw line ใน Java?
โหลดหรือสร้างแคนวาส PSD, รับอ็อบเจ็กต์ `Graphics` ของมัน, แล้วเรียกเมธอด `drawLine` พร้อมกับ `Pen` ที่กำหนดค่า วิธีนี้ทำให้วาดเส้นตรงได้ทันทีโดยอัตโนมัติจัดการ anti‑aliasing และการผสมสี คุณสามารถเรียกซ้ำด้วยพิกัดต่าง ๆ เพื่อสร้างหลายเส้น

## ขั้นตอนที่ 4: วาดเส้นจุดทแยงมุม
อ็อบเจ็กต์ `Pen` กำหนดสี, ความกว้าง, และรูปแบบ dash ของเส้น และถูกส่งไปยังเมธอด `drawLine` เพื่อวาดเส้น.
```java
graphic.drawLine(new Pen(Color.getBlue()), 9, 9, 90, 90);
graphic.drawLine(new Pen(Color.getBlue()), 9, 90, 90, 9);
```

## ขั้นตอนที่ 5: วาดเส้นต่อเนื่อง
`SolidBrush` ให้สีเติมเต็มแบบทึบสำหรับ pen ทำให้คุณตั้งค่าสีของเส้นได้ง่าย.
```java
graphic.drawLine(new Pen(new SolidBrush(Color.getRed())), new Point(9, 9), new Point(9, 90));
graphic.drawLine(new Pen(new SolidBrush(Color.getAqua())), new Point(9, 90), new Point(90, 90));
graphic.drawLine(new Pen(new SolidBrush(Color.getBlack())), new Point(90, 90), new Point(90, 9));
graphic.drawLine(new Pen(new SolidBrush(Color.getWhite())), new Point(90, 9), new Point(9, 9));
```

## ขั้นตอนที่ 6: บันทึกภาพ
การเรียกเมธอด `save` บนอ็อบเจ็กต์ `Image` จะบันทึกไฟล์ PSD ที่แก้ไขแล้วไปยังพาธที่ระบุบนดิสก์.
```java
image.save(outpath);
```

## สรุป
โดยทำตามขั้นตอนเหล่านี้ คุณได้วาดเส้นภายในไฟล์ PSD ด้วย Aspose.PSD for Java อย่างสำเร็จ บทแนะนำนี้ครอบคลุมการเริ่มต้นภาพ PSD, การตั้งค่ากราฟิก, การวาดเส้นหลายประเภท, และการบันทึกภาพที่ได้ คุณมีพื้นฐานที่มั่นคงสำหรับการอัตโนมัติการสร้างกราฟิกใน Java

## คำถามที่พบบ่อย
### Aspose.PSD for Java คืออะไร?
Aspose.PSD for Java เป็นไลบรารี Java ที่ทรงพลังสำหรับทำงานกับไฟล์ PSD ผ่านโปรแกรม

### ฉันจะหาเอกสารสำหรับ Aspose.PSD for Java ได้จากที่ไหน?
คุณสามารถหาเอกสารได้ที่หน้าอ้างอิง API ของ Aspose.PSD Java [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

### ฉันสามารถทดลอง Aspose.PSD for Java ก่อนซื้อได้หรือไม่?
ใช่, คุณสามารถรับการทดลองใช้งานฟรีได้จากหน้า releases ของ Aspose [Aspose releases page](https://releases.aspose.com/).

### ฉันจะรับการสนับสนุนทางเทคนิคสำหรับ Aspose.PSD for Java อย่างไร?
สำหรับการสนับสนุนทางเทคนิค, เยี่ยมชม [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

### ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD for Java ได้จากที่ไหน?
คุณสามารถขอรับใบอนุญาตชั่วคราวได้จากพอร์ทัลการซื้อของ Aspose [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).

---

**อัปเดตล่าสุด:** 2026-09-08  
**ทดสอบด้วย:** Aspose.PSD for Java 24.12  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [ปรับขนาดภาพด้วย Aspose.PSD for Java – วาดรูปทรงและการดำเนินการภาพพื้นฐาน](/psd/java/basic-image-operations/)
- [วาดและบันทึกสี่เหลี่ยมใน PSD ด้วย Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [เพิ่มลายเซ็นลงในภาพ – วาดภาพบนแคนวาสด้วย Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}