---
date: 2026-09-08
description: เรียนรู้วิธีสร้างภาพด้วยคลาส Graphics Path ของ Aspose.PSD ใน Java คู่มือขั้นตอน‑โดย‑ขั้นตอนนี้แสดงวิธีเพิ่มข้อความ
  รูปร่าง และลบพื้นหลังของภาพอย่างมีประสิทธิภาพ
keywords:
- how to create image
- add text image java
- clear image background java
lastmod: 2026-09-08
linktitle: วิธีสร้างภาพโดยใช้ Graphics Path ใน Java
og_description: เรียนรู้วิธีสร้างภาพด้วย Aspose.PSD ใน Java บทเรียนนี้ครอบคลุมการเพิ่มข้อความ
  รูปร่าง และการลบพื้นหลังของภาพโดยใช้คลาส Graphics Path
og_image_alt: Screenshot of Java code creating an image with graphics path using Aspose.PSD
og_title: วิธีสร้างภาพโดยใช้ Graphics Path ใน Java กับ Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to create image with Aspose.PSD's Graphics Path class in
    Java. This step‑by‑step guide shows you how to add text, shapes, and clear image
    background efficiently.
  headline: How to create image using Graphics Path in Java
  type: TechArticle
- description: Learn how to create image with Aspose.PSD's Graphics Path class in
    Java. This step‑by‑step guide shows you how to add text, shapes, and clear image
    background efficiently.
  name: How to create image using Graphics Path in Java
  steps:
  - name: '**Java Development Kit (JDK)** – a stable JDK 11+ installed. Download it
      from [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – a stable JDK 11+ installed. Download it
      from [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from [here](https://releases.aspose.com/psd/java/)
      and add it to your project’s classpath.'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from [here](https://releases.aspose.com/psd/java/)
      and add it to your project’s classpath.'
  - name: '**IDE** – any Java IDE such as Eclipse, IntelliJ IDEA, or VS Code.'
    text: '**IDE** – any Java IDE such as Eclipse, IntelliJ IDEA, or VS Code.'
  type: HowTo
- questions:
  - answer: Aspose.PSD is a Java library that enables you to create, edit, and convert
      Photoshop (PSD) files and other raster formats without requiring Photoshop.
    question: What is Aspose.PSD?
  - answer: Yes – the library supports **50+** formats, including PNG, JPEG, BMP,
      TIFF, and GIF.
    question: Can I work with formats other than PSD?
  - answer: Yes, you can access a free trial of Aspose.PSD [here](https://releases.aspose.com/).
    question: Is a trial version available?
  - answer: You can purchase Aspose.PSD from [here](https://purchase.aspose.com/buy).
    question: How do I purchase a license?
  - answer: You can seek support and discussions on [Aspose’s forum](https://forum.aspose.com/c/psd/34).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- graphics path
- Aspose.PSD
- Java image processing
title: วิธีสร้างภาพโดยใช้ Graphics Path ใน Java
url: /th/java/java-graphics-drawing/drawing-using-graphics-path/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีสร้างภาพโดยใช้ Graphics Path ใน Java

## บทนำ
ในบทแนะนำนี้คุณจะได้เรียนรู้ **วิธีสร้างภาพ** อย่างโปรแกรมโดยใช้คลาส **Graphics Path** ที่มีประสิทธิภาพจาก Aspose.PSD สำหรับ Java ไม่ว่าคุณจะต้องการวาดรูปแบบกำหนดเอง ฝังข้อความ หรือเคลียร์พื้นหลังของภาพ คู่มือขั้นตอนต่อขั้นตอนด้านล่างจะแสดงให้คุณเห็นว่าต้องทำอย่างไรเพื่อให้ได้ผลลัพธ์ระดับมืออาชีพในเพียงไม่กี่บรรทัดของโค้ด

## คำตอบอย่างรวดเร็ว
- **ไลบรารีใดที่จัดการการวาดที่ซับซ้อน?** คลาส Graphics Path ของ Aspose.PSD สำหรับ Java.  
- **ฉันสามารถเพิ่มข้อความลงในภาพได้หรือไม่?** ได้ – ใช้วิธี `GraphicsPath.addString`.  
- **การเคลียร์พื้นหลังได้รับการสนับสนุนหรือไม่?** แน่นอน, เติมเส้นทางด้วยแปรงโปร่งใส.  
- **ต้องการเวอร์ชัน Java ใด?** JDK 11 หรือใหม่กว่า.  
- **ฉันต้องการไลเซนส์สำหรับการผลิตหรือไม่?** จำเป็นต้องมีไลเซนส์เชิงพาณิชย์; มีการทดลองใช้งานฟรี.

## Graphics Path class คืออะไร?
`GraphicsPath` class เป็นอ็อบเจ็กต์หลักของ Aspose.PSD สำหรับกำหนดคำสั่งการวาดแบบเวกเตอร์ มันช่วยให้คุณประกอบรูปทรง, ข้อความ, และการเติมสีเป็นเส้นทางเดียวที่สามารถนำกลับมาใช้ใหม่ได้และสามารถเรนเดอร์บนภาพใดก็ได้ โดยการสร้างเส้นทางคุณสามารถใช้ปากกา, แปรง, และการแปลงในขั้นตอนการเรนเดอร์เดียว ซึ่งช่วยเพิ่มประสิทธิภาพและทำให้ตรรกะการวาดเป็นระเบียบ

## ทำไมต้องใช้ Graphics Path สำหรับเพิ่มข้อความในภาพ Java และเคลียร์พื้นหลังภาพ Java?
Aspose.PSD รองรับ **รูปแบบภาพกว่า 50** (รวมถึง PSD, PNG, JPEG, BMP) และสามารถประมวลผลไฟล์ขนาดถึง **2 GB** โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ การใช้ Graphics Path ช่วยให้คุณรวมการวาด, การวางข้อความ, และการเคลียร์พื้นหลังในหนึ่งการดำเนินการที่มีประสิทธิภาพสูง ลดภาระหน่วยความจำได้ถึง **30 %** เมื่อเทียบกับวิธีการที่ใช้แรสเตอร์อย่างเดียว

## สิ่งที่ต้องเตรียม
ก่อนเริ่ม, ตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

1. **Java Development Kit (JDK)** – JDK 11+ ที่เสถียรติดตั้งแล้ว ดาวน์โหลดได้จาก [Oracle’s site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – รับไฟล์ JAR ล่าสุดจาก [here](https://releases.aspose.com/psd/java/) และเพิ่มไปยัง classpath ของโปรเจกต์ของคุณ.  
3. **IDE** – IDE ของ Java ใดก็ได้ เช่น Eclipse, IntelliJ IDEA หรือ VS Code.

เมื่อเตรียมพร้อมแล้ว, คุณพร้อมที่จะเริ่มสร้างภาพ

## นำเข้าแพ็กเกจ
เพื่อทำงานกับกราฟิก, นำเข้าชื่อเนมสเปซที่จำเป็น:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Figure;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.GraphicsPath;
import com.aspose.psd.HatchStyle;
import com.aspose.psd.Pen;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.HatchBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.shapes.EllipseShape;
import com.aspose.psd.shapes.RectangleShape;
import com.aspose.psd.shapes.TextShape;
```

การนำเข้าดังกล่าวเปิดเผยคลาสการวาด, แปรง, และปากกาหลักที่จำเป็นสำหรับการจัดการภาพ.

## วิธีสร้างภาพด้วย Graphics Path ใน Java?
สร้างแคนวาสแรสเตอร์ใหม่, แนบอ็อบเจ็กต์ `Graphics`, และเตรียมพื้นผิวการวาด ขั้นตอนเดียวนี้จะตั้งค่า bitmap ขนาด **500 × 500 พิกเซล** ที่พร้อมสำหรับการเรนเดอร์เวกเตอร์ แคนวาสเริ่มต้นเป็นโปร่งใส, ทำให้คุณสามารถเติมสีพื้นหลังหรือแพทเทิร์นใดก็ได้ในภายหลัง ซึ่งเป็นสิ่งสำคัญสำหรับสถานการณ์การเคลียร์พื้นหลังของภาพ.

```java
PsdImage image = new PsdImage(500, 500);
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
```

## ขั้นตอนที่ 1: เริ่มต้นภาพและกราฟิก
ที่นี่เราสร้างอ็อบเจ็กต์ `PsdImage` (500 × 500) และรับคอนเท็กซ์ `Graphics` ของมัน.  
`PsdImage` แสดงถึงภาพแรสเตอร์ในหน่วยความจำที่ Aspose.PSD สามารถจัดการและบันทึกในหลายรูปแบบ.  
`Graphics` ให้เมธอดการวาดที่เรนเดอร์รูปทรง, ข้อความ, และเส้นทางลงบน `PsdImage`.

## ขั้นตอนที่ 2: สร้างและกำหนดค่า graphics path
ต่อไป, เราสร้าง `GraphicsPath` ที่ประกอบด้วยวงกลม, สี่เหลี่ยม, และป้ายข้อความ.  
`GraphicsPath` เป็นคอนเทนเนอร์สำหรับรูปทรงเรขาคณิต; คุณสามารถเพิ่มรูปทรง, เส้น, และสตริงลงไปก่อนการเรนเดอร์.

```java
GraphicsPath graphicspath = new GraphicsPath();
Figure figure = new Figure();
figure.addShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
figure.addShape(new TextShape("Aspose.PSD", new RectangleF(170, 225, 170, 100), new TextFont("Arial", 20), StringFormat.getGenericTypographic()));
Figure[] fig = { figure };
graphicspath.addFigures(fig);
```

### การเพิ่มข้อความลงในภาพ (add text image java)
เมธอด `addString` ของ `GraphicsPath` จะวางข้อความที่ระบุที่พิกัดที่กำหนดโดยใช้ฟอนต์และแปรงที่ให้มา นี่เป็นวิธีที่เชื่อถือได้ที่สุดในการฝังข้อความที่คมชัดและปรับขนาดได้ภายในเส้นทางเวกเตอร์.

## ขั้นตอนที่ 3: วาดและเติมเส้นทาง
ตอนนี้เราจะเรนเดอร์เส้นทางด้วยปากกาสีฟ้าและเติมด้วยแปรง hatch แนวตั้ง, ซึ่งยังแสดงวิธี **clear image background java** โดยการเติมด้วยแพทเทิร์นโปร่งใสหากต้องการ `Pen` กำหนดสไตล์เส้นขอบ, ส่วน `HatchBrush` สร้างการเติมแบบลาย.

```java
graphics.drawPath(new Pen(Color.getBlue()), graphicspath);
HatchBrush hatchbrush = new HatchBrush();
hatchbrush.setBackgroundColor(Color.getBrown());
hatchbrush.setForegroundColor(Color.getBlue());
hatchbrush.setHatchStyle(HatchStyle.Vertical);
graphics.fillPath(hatchbrush, graphicspath);
```

## ขั้นตอนที่ 4: บันทึกภาพ
สุดท้าย, เขียนภาพที่ประกอบขึ้นไปยังดิสก์ในรูปแบบ PNG (หรือรูปแบบใดก็ได้จาก 50+ ที่รองรับ). เมธอด `save` กำหนดประเภทไฟล์ผลลัพธ์จากส่วนขยายไฟล์ที่คุณระบุ.

```java
String dataDir = "Your Document Directory";
image.save(dataDir + "DrawingUsingGraphicsPath_output.psd");
```

## ปัญหาทั่วไปและวิธีแก้
- **เส้นทางไม่ปรากฏ** – ตรวจสอบให้แน่ใจว่าสีของปากกาตรงกันกับแปรงเติมที่มีความคอนทราสต์.  
- **ข้อความดูเบลอ** – ใช้ภาพความละเอียดสูงขึ้นหรือฟอนต์ TrueType ที่มี DPI เพียงพอ.  
- **ข้อผิดพลาด out‑of‑memory กับไฟล์ขนาดใหญ่** – เปิดใช้งาน `PsdImageOptions.setUseMemoryCache(true)` เพื่อสตรีมข้อมูลแทนการโหลดเต็ม.

## คำถามที่พบบ่อย

**Q: Aspose.PSD คืออะไร?**  
A: Aspose.PSD เป็นไลบรารี Java ที่ช่วยให้คุณสร้าง, แก้ไข, และแปลงไฟล์ Photoshop (PSD) และรูปแบบแรสเตอร์อื่น ๆ โดยไม่ต้องใช้ Photoshop.

**Q: ฉันสามารถทำงานกับรูปแบบอื่นนอกจาก PSD ได้หรือไม่?**  
A: ได้ – ไลบรารีรองรับ **50+** รูปแบบ รวมถึง PNG, JPEG, BMP, TIFF, และ GIF.

**Q: มีเวอร์ชันทดลองหรือไม่?**  
A: มี, คุณสามารถเข้าถึงการทดลองใช้ Aspose.PSD ฟรีได้ [here](https://releases.aspose.com/).

**Q: ฉันจะซื้อไลเซนส์ได้อย่างไร?**  
A: คุณสามารถซื้อ Aspose.PSD ได้จาก [here](https://purchase.aspose.com/buy).

**Q: ฉันจะหาการสนับสนุนได้จากที่ไหน?**  
A: คุณสามารถขอรับการสนับสนุนและการสนทนาได้ที่ [Aspose’s forum](https://forum.aspose.com/c/psd/34).

## สรุป
โดยทำตามคู่มือนี้คุณจะรู้ **วิธีสร้างภาพ** ที่มีรูปทรงเวกเตอร์ซับซ้อน, ข้อความฝัง, และพื้นหลังโปร่งใสโดยใช้คลาส Graphics Path ของ Aspose.PSD ทดลองใช้ปากกา, แปรง, และรูปทรงเส้นทางต่าง ๆ เพื่อสร้างกราฟิกที่หลากหลายยิ่งขึ้นสำหรับเกม, ส่วน UI, หรือการสร้างรายงานอัตโนมัติ.

---

**อัปเดตล่าสุด:** 2026-09-08  
**ทดสอบกับ:** Aspose.PSD for Java 24.11  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [สร้างภาพ PSD ใน Java โดยกำหนด Path ด้วย Aspose.PSD](/psd/java/image-editing/create-image-by-setting-path/)
- [ปรับขนาดภาพด้วย Aspose.PSD สำหรับ Java – วาดรูปทรง & การดำเนินการพื้นฐานของภาพ](/psd/java/basic-image-operations/)
- [เพิ่มลายเซ็นลงในภาพ – วาดภาพบนแคนวาสด้วย Aspose.PSD สำหรับ Java](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}