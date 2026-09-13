---
date: 2026-09-13
description: เรียนรู้วิธีวาดรูปวงรีและรูปทรงอื่น ๆ ใน Java ด้วย Aspose.PSD. บทแนะนำกราฟิก
  Java แบบขั้นตอนนี้แสดงการเติมสีไล่ระดับ, การเติมรูปหลายเหลี่ยม, และการส่งออกภาพ.
keywords:
- how to draw ellipse
- draw shapes java
- how to create gradient
- java graphics tutorial
- fill polygon java
lastmod: 2026-09-13
linktitle: การวาดโดยใช้กราฟิกใน Java
og_description: เรียนรู้วิธีวาดรูปวงรีใน Java ด้วย Aspose.PSD. บทแนะนำกราฟิก Java
  นี้ครอบคลุมการวาดรูปทรง, การเติมสีไล่ระดับ, การเติมรูปหลายเหลี่ยม, และการส่งออกภาพ.
og_image_alt: Screenshot of Java code drawing an ellipse with Aspose.PSD
og_title: วิธีวาดรูปวงรีโดยใช้กราฟิกใน Java กับ Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-13'
  description: Learn how to draw an ellipse and other shapes in Java with Aspose.PSD.
    This step‑by‑step Java graphics tutorial shows gradient fills, polygon fills,
    and image export.
  headline: How to draw ellipse using graphics in Java with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Yes, it supports layer merging, channel adjustments, text rendering, and
      advanced masking in addition to shape drawing.
    question: Can Aspose.PSD handle complex image manipulations?
  - answer: Absolutely; the library is optimized for speed and can process a 10 MP
      image in under 2 seconds on a typical server.
    question: Is Aspose.PSD suitable for high‑performance applications?
  - answer: Visit the [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides and API references.
    question: Where can I find more examples and documentation?
  - answer: Yes, you can export to BMP, PNG, JPEG, TIFF, GIF, and PSD among others.
    question: Does Aspose.PSD support multiple image formats for export?
  - answer: Reach out to the Aspose.PSD community on the [support forum](https://forum.aspose.com/c/psd/34)
      or consider a [temporary license](https://purchase.aspose.com/temporary-license/)
      for priority assistance.
    question: How can I get support or assistance if I encounter issues?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- drawing shapes java
- gradient fill java
- initialize graphics java
title: วิธีวาดรูปวงรีโดยใช้กราฟิกใน Java กับ Aspose.PSD
url: /th/java/java-graphics-drawing/drawing-using-graphics/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีวาดวงรีโดยใช้กราฟิกใน Java กับ Aspose.PSD

## บทนำ
ในบทเรียนกราฟิก Java นี้คุณจะได้ค้นพบ **วิธีวาดวงรี** วัตถุและรูปทรงอื่น ๆ อย่างโปรแกรมโดยใช้ Aspose.PSD for Java ไม่ว่าคุณจะต้องการสร้างภาพย่อแบบไดนามิก, สร้างองค์ประกอบ UI ที่กำหนดเอง, หรืออัตโนมัติกระบวนการออกแบบ, การเชี่ยวชาญการวาดวงรีและการเติมไล่สีจะให้การควบคุมภาพที่แม่นยำ ขั้นตอนต่อไปนี้จะพาคุณผ่านการเริ่มต้นกราฟิก, การกำหนดค่า pen และ brush, และการส่งออกผลลัพธ์ในรูปแบบภาพที่เป็นที่นิยม

## คำตอบสั้น
- **ไลบรารีที่ต้องการคืออะไร?** Aspose.PSD for Java (ดาวน์โหลดจากเว็บไซต์อย่างเป็นทางการ).  
- **รูปร่างที่บทเรียนเน้นคืออะไร?** การวาดวงรีและการเติมพอลิกอน.  
- **ฉันสามารถส่งออกเป็นรูปแบบอื่นนอกจาก BMP ได้หรือไม่?** ใช่ – รองรับ PNG, JPEG, TIFF และอื่น ๆ อีกมาก.  
- **ฉันต้องใช้ไลเซนส์สำหรับการพัฒนาหรือไม่?** ไลเซนส์ชั่วคราวฟรีใช้ได้สำหรับการทดสอบ; จำเป็นต้องมีไลเซนส์เต็มสำหรับการผลิต.  
- **API นี้เหมาะกับภาพขนาดใหญ่หรือไม่?** Aspose.PSD ประมวลผลไฟล์ขนาดสูงสุด 500 MB โดยไม่ต้องโหลดบิตแมปทั้งหมดเข้าสู่หน่วยความจำ.

## วิธีวาดวงรีใน Java?
โหลด `PsdImage` ด้วยความกว้างและความสูงที่ต้องการ, สร้างอ็อบเจ็กต์ `Graphics`, ตั้งค่า `Pen`, และเรียก `drawEllipse` พร้อมสี่เหลี่ยมขอบเขต การดำเนินการทั้งหมดต้องการเพียงไม่กี่คำเรียกเมธอดและทำงานภายในเวลาไม่ถึงหนึ่งวินาทีสำหรับภาพ 800×600 ปกติบนฮาร์ดแวร์สมัยใหม่

## Aspose.PSD for Java คืออะไร?
Aspose.PSD for Java เป็น **ไลบรารี pure‑Java ที่ให้การแปลงรูปภาพกว่า 50 รูปแบบและความสามารถในการแก้ไข PSD อย่างเต็มรูปแบบ** โดยไม่ต้องใช้ Adobe Photoshop สามารถเรนเดอร์, แก้ไข, และส่งออกไฟล์หลายเลเยอร์พร้อมการใช้หน่วยความจำน้อย ทำให้เหมาะสำหรับการสร้างกราฟิกฝั่งเซิร์ฟเวอร์

## ทำไมต้องใช้ Aspose.PSD สำหรับการวาดรูปทรง?
Aspose.PSD มีประสิทธิภาพสูง, รองรับรูปแบบหลากหลาย, และการเรนเดอร์ที่แม่นยำ ทำให้เหมาะสำหรับการสร้างกราฟิกฝั่งเซิร์ฟเวอร์และการวาดรูปทรงที่ซับซ้อน

- **ประสิทธิภาพ:** จัดการภาพขนาดถึง 500 MB ด้วยการใช้หน่วยความจำ heap น้อยกว่า 150 MB (≈30 % ต่ำกว่าห้องสมุดอื่น).  
- **การสนับสนุนรูปแบบ:** มากกว่า 50 รูปแบบเข้าและออก รวมถึง BMP, PNG, JPEG, TIFF, และ PSD.  
- **ความแม่นยำ:** การเรนเดอร์ระดับซับพิกเซลทำให้วงรีคมชัดและไล่สีเรียบบนจอแสดงผลความละเอียดสูง.

## ข้อกำหนดเบื้องต้น
- ความรู้พื้นฐานการเขียนโปรแกรม Java.  
- ติดตั้ง Java Development Kit (JDK).  
- IDE เช่น IntelliJ IDEA หรือ Eclipse.  
- ไลบรารี Aspose.PSD for Java คุณสามารถดาวน์โหลดได้จาก [Aspose.PSD Java download](https://releases.aspose.com/psd/java/).

## นำเข้าแพ็กเกจ
เพื่อเริ่มต้น, ให้นำเข้าคลาส Aspose.PSD ที่จำเป็นและยูทิลิตี้มาตรฐานของ Java คลาสต่อไปนี้ให้ฟังก์ชันการวาดพื้นฐานและการจัดการสี:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Point;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.LinearGradientBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## ขั้นตอนที่ 1: สร้างอ็อบเจ็กต์ภาพ
`PsdImage` แสดงถึงแคนวาสเรสเตอร์ในหน่วยความจำที่สามารถวาดลงไปและบันทึกในรูปแบบต่าง ๆ
```java
String dataDir = "Your Document Directory";
PsdImage image = new PsdImage(500, 500);
```

## ขั้นตอนที่ 2: เริ่มต้นอ็อบเจ็กต์กราฟิก
`Graphics` เป็นพื้นผิวการวาดที่เชื่อมต่อกับ `PsdImage`, ทำให้สามารถทำงานเวกเตอร์เช่นการวาดรูปทรงได้
```java
Graphics graphics = new Graphics(image);
```

## ขั้นตอนที่ 3: ล้างพื้นผิวภาพ
`clear` เติมสีพื้นหลังเดียวทั่วทั้งแคนวาส
```java
graphics.clear(Color.getWhite());
```

## ขั้นตอนที่ 4: สร้างและกำหนดค่าอ็อบเจ็กต์ Pen
`Pen` กำหนดสีเส้น, ความกว้าง, และสไตล์ที่ใช้เมื่อวาดขอบ
```java
Pen pen = new Pen(Color.getBlue());
```

## ขั้นตอนที่ 5: วาดรูปทรง
`drawEllipse` วาดวงรีที่พอดีภายในสี่เหลี่ยมที่ระบุโดยใช้ pen ปัจจุบัน
```java
graphics.drawEllipse(pen, new Rectangle(10, 10, 150, 100));
```

## ขั้นตอนที่ 6: ใช้ Brush สำหรับการเติมสี
`LinearGradientBrush` สร้างการเติมไล่สีที่เปลี่ยนระหว่างสองสีในพื้นที่ที่กำหนด
```java
LinearGradientBrush linearGradientBrush = new LinearGradientBrush(image.getBounds(), Color.getRed(), Color.getWhite(), 45f);
Point[] points = { new Point(200, 200), new Point(400, 200), new Point(250, 350) };
graphics.fillPolygon(linearGradientBrush, points);
```

## ขั้นตอนที่ 7: บันทึกภาพที่แก้ไข
`save` เขียน `PsdImage` ลงดิสก์ในรูปแบบที่เลือก เช่น BMP หรือ PNG
```java
image.save(dataDir + "DrawingUsingGraphics_output.bmp", new BmpOptions());
```

## ข้อผิดพลาดทั่วไปและการแก้ไขปัญหา
- **NullPointerException บนกราฟิก:** ตรวจสอบให้แน่ใจว่า `PsdImage` ถูกสร้างเต็มที่ก่อนสร้างอ็อบเจ็กต์ `Graphics`.  
- **สีไม่ถูกต้อง:** ใช้ `Color.fromArgb` เพื่อระบุค่า ARGB ที่แน่นอนเมื่อพาเลตต์เริ่มต้นไม่ตรงกับที่คาดหวัง.  
- **ความล่าช้าของประสิทธิภาพบนภาพขนาดใหญ่:** เปิดใช้ `PsdImageOptions` กับ `compression = CompressionType.Rle` เพื่อลดภาระหน่วยความจำ.

## คำถามที่พบบ่อย

**ถาม: Aspose.PSD สามารถจัดการการปรับแต่งภาพที่ซับซ้อนได้หรือไม่?**  
ตอบ: ใช่, รองรับการรวมเลเยอร์, การปรับแชนแนล, การเรนเดอร์ข้อความ, และการมาสก์ขั้นสูงนอกเหนือจากการวาดรูปทรง.

**ถาม: Aspose.PSD เหมาะกับแอปพลิเคชันประสิทธิภาพสูงหรือไม่?**  
ตอบ: แน่นอน; ไลบรารีได้รับการปรับให้ทำงานเร็วและสามารถประมวลผลภาพ 10 MP ในเวลาน้อยกว่า 2 วินาทีบนเซิร์ฟเวอร์ทั่วไป.

**ถาม: ฉันจะหา ตัวอย่างและเอกสารเพิ่มเติมได้จากที่ไหน?**  
ตอบ: เยี่ยมชม [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/) เพื่อรับคู่มือและอ้างอิง API อย่างครบถ้วน.

**ถาม: Aspose.PSD รองรับหลายรูปแบบภาพสำหรับการส่งออกหรือไม่?**  
ตอบ: ใช่, คุณสามารถส่งออกเป็น BMP, PNG, JPEG, TIFF, GIF, และ PSD รวมถึงรูปแบบอื่น ๆ

**ถาม: ฉันจะขอรับการสนับสนุนหรือความช่วยเหลือหากพบปัญหาได้อย่างไร?**  
ตอบ: ติดต่อชุมชน Aspose.PSD ผ่าน [support forum](https://forum.aspose.com/c/psd/34) หรือพิจารณาใช้ [temporary license](https://purchase.aspose.com/temporary-license/) เพื่อรับการช่วยเหลือแบบเร่งด่วน.

---

**Last updated:** 2026-09-13  
**Tested with:** Aspose.PSD for Java 24.10  
**Author:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [ปรับขนาดภาพด้วย Aspose.PSD for Java – วาดรูปทรงและการดำเนินการภาพพื้นฐาน](/psd/java/basic-image-operations/)
- [วาดและบันทึกสี่เหลี่ยมใน PSD ด้วย Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [เพิ่มลายเซ็นลงในภาพ – วาดภาพบนแคนวาสด้วย Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}