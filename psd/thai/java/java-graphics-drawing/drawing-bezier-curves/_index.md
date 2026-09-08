---
date: 2026-09-08
description: เรียนรู้วิธีวาดเส้นโค้งเบเซียร์ใน Java ด้วย Aspose.PSD for Java ทำตามคำแนะนำขั้นตอนต่อขั้นตอน
  ข้อกำหนดเบื้องต้น และตัวอย่างที่ไม่ต้องเขียนโค้ด
keywords:
- how to draw bezier
- how to use pen
- bezier curve example java
- java graphics draw curve
lastmod: 2026-09-08
linktitle: การวาดเส้นโค้งเบเซียร์ใน Java
og_description: วิธีวาดเส้นโค้งเบเซียร์ใน Java ด้วย Aspose.PSD คู่มือนี้ครอบคลุมข้อกำหนดเบื้องต้น
  การวาดขั้นตอนต่อขั้นตอน และเคล็ดลับสำหรับภาพความละเอียดสูง
og_image_alt: Screenshot of a Java application rendering a Bezier curve with Aspose.PSD
og_title: วิธีวาดเส้นโค้งเบเซียร์ใน Java ด้วยไลบรารี Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw bezier curves in Java using Aspose.PSD for Java.
    Follow step‑by‑step instructions, prerequisites, and code‑free examples.
  headline: How to draw bezier curves in Java with Aspose.PSD library
  type: TechArticle
- description: Learn how to draw bezier curves in Java using Aspose.PSD for Java.
    Follow step‑by‑step instructions, prerequisites, and code‑free examples.
  name: How to draw bezier curves in Java with Aspose.PSD library
  steps:
  - name: create an image instance
    text: 'The `PsdImage` class is Aspose.PSD''s top‑level object that represents
      a single PSD file in memory. First, you need to create an instance of the `PsdImage`
      class, which represents a PSD image in memory. Explanation: - `PsdImage` is
      instantiated with width and height parameters (100 × 100 pixels in th'
  - name: initialize graphics context
    text: 'The `Graphics` class provides drawing capabilities on a `PsdImage`. Next,
      initialize an instance of the `Graphics` class to perform drawing operations
      on the image. Explanation: - `Graphics` object is initialized with the `image`
      instance, allowing drawing operations.'
  - name: clear the graphics surface
    text: 'The `clear()` method sets the background colour of the graphics surface.
      Clear the graphics surface using a specific background colour, here `Color.getYellow()`.
      Explanation: - `clear()` method sets the background colour of the graphics surface.'
  - name: initialize pen for drawing
    text: 'The `Pen` object defines stroke attributes such as colour and width. Set
      up a `Pen` object with properties like colour and width to define how the curve
      will be drawn. Explanation: - `Pen` is initialized with black colour and 3‑pixel
      width.'
  - name: define bezier curve parameters
    text: 'Control points determine the curvature. Specify the control points and
      end points for the Bezier curve. Explanation: - `startX`, `startY`: Starting
      point of the curve. - `controlX1`, `controlY1`: First control point. - `controlX2`,
      `controlY2`: Second control point. - `endX`, `endY`: Ending point of'
  - name: draw the bezier curve
    text: 'The `drawBezier()` method renders the curve using the supplied `Pen` and
      points. Use the `drawBezier()` method to draw the Bezier curve onto the image
      using the previously defined `Pen` and control points. Explanation: - `drawBezier()`
      method draws the curve with specified parameters using the `blac'
  - name: save the image
    text: Saving the image persists the drawing to disk. Save the drawn image to a
      BMP file format.
  type: HowTo
- questions:
  - answer: Yes, repeat the `drawBezier()` call inside a loop, updating the control
      points for each curve.
    question: Can I draw multiple Bezier curves in the same image?
  - answer: Modify the `Pen` object's colour property (`Color.getBlack()` in the example)
      before invoking `drawBezier()`.
    question: How can I change the colour of the Bezier curve?
  - answer: Yes, Aspose.PSD for Java supports high‑resolution images with efficient
      memory management, handling files larger than 500 MB without loading the entire
      file into memory.
    question: Is Aspose.PSD for Java suitable for high‑resolution images?
  - answer: Yes, Aspose.PSD for Java supports exporting to PNG, JPEG, TIFF, and many
      other raster formats.
    question: Can I export the image to formats other than BMP?
  - answer: Visit the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides and code samples.
    question: Where can I find more examples and documentation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- drawing bezier
- Aspose.PSD
- Java graphics
- curve drawing
title: วิธีวาดเส้นโค้งเบเซียร์ใน Java ด้วยไลบรารี Aspose.PSD
url: /th/java/java-graphics-drawing/drawing-bezier-curves/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีวาดเส้นโค้งเบเซียร์ใน Java ด้วยไลบรารี Aspose.PSD

## บทนำ
ถ้าคุณต้องการทราบ **วิธีวาดเบเซียร์** รูปทรงในแอปพลิเคชัน Java บนเดสก์ท็อปหรือเซิร์ฟเวอร์, Aspose.PSD for Java จะมอบ API ที่สะอาดและใช้หน่วยความจำอย่างมีประสิทธิภาพ ในบทแนะนำนี้คุณจะเห็นขั้นตอนที่แน่นอนในการสร้างแคนวาส PSD, กำหนดปากกาวาด, นิยามจุดควบคุม, และเรนเดอร์เส้นโค้งเบเซียร์ที่เรียบเนียน — ทั้งหมดโดยไม่ต้องเขียนโค้ดการจัดการพิกเซลระดับต่ำ

## คำตอบอย่างรวดเร็ว
- **ไลบรารีใดที่จัดการการวาด?** Aspose.PSD for Java.
- **ต้องใช้บรรทัดโค้ดกี่บรรทัด?** About ten concise statements.
- **ฉันสามารถเปลี่ยนสีของเส้นโค้งได้หรือไม่?** Yes, by adjusting the `Pen` colour property.
- **รองรับการส่งออกความละเอียดสูงหรือไม่?** Yes, up to 500 MB files without full memory load.
- **ฉันต้องการใบอนุญาตเชิงพาณิชย์หรือไม่?** A free trial works for development; a license is required for production.

## เส้นโค้งเบเซียร์คืออะไร?
เส้นโค้งเบเซียร์เป็นเส้นเรียบที่กำหนดโดยคณิตศาสตร์ซึ่งควบคุมโดยสองจุดหรือมากกว่า มักใช้ในกราฟิกเวกเตอร์, แอนิเมชัน, และการออกแบบ UI เพื่อสร้างรูปทรงที่สวยงามและปรับขนาดได้ รูปร่างของเส้นโค้งจะกำหนดโดยจุดเริ่มต้น, จุดสิ้นสุด, และหนึ่งหรือหลายจุดควบคุมที่มีผลต่อความโค้งของเส้น ทำให้ผู้ออกแบบสามารถสร้างเส้นทางที่ซับซ้อนได้ด้วยพารามิเตอร์ง่าย ๆ

## ทำไมต้องใช้ Aspose.PSD สำหรับการวาดเส้นโค้งเบเซียร์?
Aspose.PSD รองรับ **30+ รูปแบบภาพ** และสามารถประมวลผล **ไฟล์ PSD หลายร้อยหน้า** ได้โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่ RAM วิธี `drawBezier()` ของไลบรารีจะจัดการการทำ anti‑aliasing และการจัดการสีโดยอัตโนมัติ ส่งผลลัพธ์ที่พิกเซล‑เพอร์เฟ็กต์ในเวลาน้อยกว่า หนึ่งวินาทีสำหรับแคนวาสขนาดทั่วไป 100 × 100

## ข้อกำหนดเบื้องต้น
ก่อนเริ่ม, ตรวจสอบว่าคุณมีข้อกำหนดต่อไปนี้:
1. **Java Development Kit (JDK)** – เวอร์ชันล่าสุดใดก็ได้ (8 หรือใหม่กว่า) ที่ติดตั้งและกำหนดค่าไว้
2. **Aspose.PSD for Java JAR** – ดาวน์โหลดไลบรารี Aspose.PSD for Java จาก [Aspose.PSD Java download](https://releases.aspose.com/psd/java/) แล้วเพิ่มลงใน classpath ของโปรเจกต์ของคุณ
3. **Integrated Development Environment (IDE)** – เช่น Eclipse, IntelliJ IDEA, หรือ NetBeans ที่ตั้งค่ากับ JDK

## นำเข้าแพ็กเกจ
การนำเข้าต่อไปนี้จะนำเข้าคลาสของ Aspose.PSD ที่จำเป็นสำหรับการสร้างภาพและการวาด
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## วิธีวาดเส้นโค้งเบเซียร์ใน Java?
โหลด `PsdImage` ว่าง, สร้างอ็อบเจ็กต์ `Graphics`, กำหนดค่า `Pen`, นิยามจุดเริ่มต้น, จุดควบคุม, และจุดสิ้นสุด, เรียก `drawBezier()`, และสุดท้ายบันทึกภาพ ลำดับนี้จะสร้างเส้นโค้งเรียบด้วยการเรียกเมธอดเดียวและไม่ต้องคำนวณพิกเซลด้วยตนเอง

### ขั้นตอนที่ 1: สร้างอินสแตนซ์ของภาพ
คลาส `PsdImage` เป็นอ็อบเจ็กต์ระดับบนของ Aspose.PSD ที่แทนไฟล์ PSD เดียวในหน่วยความจำ ก่อนอื่นคุณต้องสร้างอินสแตนซ์ของคลาส `PsdImage` ซึ่งแทนภาพ PSD ในหน่วยความจำ
```java
String dataDir = "Your Document Directory";
Image image = new PsdImage(100, 100);
```
- `PsdImage` ถูกสร้างด้วยพารามิเตอร์ความกว้างและความสูง (100 × 100 พิกเซลในตัวอย่างนี้)

### ขั้นตอนที่ 2: เริ่มต้นบริบทกราฟิก
คลาส `Graphics` ให้ความสามารถในการวาดบน `PsdImage` ต่อไปนี้ให้เริ่มต้นอินสแตนซ์ของคลาส `Graphics` เพื่อทำการวาดบนภาพ
```java
Graphics graphics = new Graphics(image);
```
- อ็อบเจ็กต์ `Graphics` ถูกเริ่มต้นด้วยอินสแตนซ์ `image` ทำให้สามารถทำการวาดได้

### ขั้นตอนที่ 3: ล้างพื้นผิวกราฟิก
เมธอด `clear()` ตั้งค่าสีพื้นหลังของพื้นผิวกราฟิก ล้างพื้นผิวกราฟิกโดยใช้สีพื้นหลังเฉพาะ, ในที่นี้คือ `Color.getYellow()`.
```java
graphics.clear(Color.getYellow());
```
- เมธอด `clear()` ตั้งค่าสีพื้นหลังของพื้นผิวกราฟิก

### ขั้นตอนที่ 4: เริ่มต้นปากกาสำหรับการวาด
อ็อบเจ็กต์ `Pen` กำหนดคุณลักษณะของเส้นเช่นสีและความกว้าง ตั้งค่าอ็อบเจ็กต์ `Pen` ด้วยคุณสมบัติเช่นสีและความกว้างเพื่อกำหนดวิธีการวาดเส้นโค้ง
```java
Pen blackPen = new Pen(Color.getBlack(), 3);
```
- `Pen` ถูกสร้างด้วยสีดำและความกว้าง 3 พิกเซล

### ขั้นตอนที่ 5: กำหนดพารามิเตอร์ของเส้นโค้งเบเซียร์
จุดควบคุมกำหนดความโค้ง ระบุจุดควบคุมและจุดสิ้นสุดสำหรับเส้นโค้งเบเซียร์
```java
float startX = 10, startY = 25;
float controlX1 = 20, controlY1 = 5;
float controlX2 = 55, controlY2 = 10;
float endX = 90, endY = 25;
```
- `startX`, `startY`: จุดเริ่มต้นของเส้นโค้ง  
- `controlX1`, `controlY1`: จุดควบคุมแรก  
- `controlX2`, `controlY2`: จุดควบคุมที่สอง  
- `endX`, `endY`: จุดสิ้นสุดของเส้นโค้ง

### ขั้นตอนที่ 6: วาดเส้นโค้งเบเซียร์
เมธอด `drawBezier()` จะเรนเดอร์เส้นโค้งโดยใช้ `Pen` และจุดที่ระบุ ใช้เมธอด `drawBezier()` เพื่อวาดเส้นโค้งเบเซียร์ลงบนภาพโดยใช้ `Pen` และจุดควบคุมที่กำหนดไว้ก่อนหน้า
```java
graphics.drawBezier(blackPen, startX, startY, controlX1, controlY1, controlX2, controlY2, endX, endY);
```
- เมธอด `drawBezier()` วาดเส้นโค้งด้วยพารามิเตอร์ที่ระบุโดยใช้ `blackPen`

### ขั้นตอนที่ 7: บันทึกภาพ
การบันทึกภาพทำให้การวาดถูกบันทึกลงดิสก์ บันทึกภาพที่วาดเป็นรูปแบบไฟล์ BMP
```java
String outpath = dataDir + "Bezier.bmp";
BmpOptions saveOptions = new BmpOptions();
image.save(outpath, saveOptions);
```

## ปัญหาทั่วไปและวิธีแก้
- **เส้นโค้งดูแบน** – ตรวจสอบว่าจุดควบคุมไม่ได้อยู่บนเส้นเดียวกับจุดเริ่มต้นและจุดสิ้นสุด ให้เลื่อนตำแหน่งจุดควบคุมเล็กน้อยเพื่อสร้างความโค้ง
- **สีไม่เปลี่ยน** – ตรวจสอบว่าคุณได้แก้ไขสีของ `Pen` ก่อนเรียก `drawBezier()`
- **ข้อผิดพลาด out‑of‑memory บนแคนวาสขนาดใหญ่** – ใช้คอนสตรัคเตอร์ของ `PsdImage` ที่เปิดใช้งานการสตรีมมิ่ง หรือแบ่งการวาดเป็นหลายส่วน

## คำถามที่พบบ่อย

**ถาม: ฉันสามารถวาดหลายเส้นโค้งเบเซียร์ในภาพเดียวได้หรือไม่?**  
ตอบ: ได้, ให้เรียกเมธอด `drawBezier()` ซ้ำภายในลูป และอัปเดตจุดควบคุมสำหรับแต่ละเส้นโค้ง

**ถาม: ฉันจะเปลี่ยนสีของเส้นโค้งเบเซียร์ได้อย่างไร?**  
ตอบ: แก้ไขคุณสมบัติ colour ของอ็อบเจ็กต์ `Pen` (`Color.getBlack()` ในตัวอย่าง) ก่อนเรียก `drawBezier()`

**ถาม: Aspose.PSD for Java เหมาะกับภาพความละเอียดสูงหรือไม่?**  
ตอบ: ใช่, Aspose.PSD for Java รองรับภาพความละเอียดสูงด้วยการจัดการหน่วยความจำที่มีประสิทธิภาพ, สามารถจัดการไฟล์ที่ใหญ่กว่า 500 MB โดยไม่ต้องโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ

**ถาม: ฉันสามารถส่งออกภาพเป็นรูปแบบอื่นนอกจาก BMP ได้หรือไม่?**  
ตอบ: ใช่, Aspose.PSD for Java รองรับการส่งออกเป็น PNG, JPEG, TIFF, และรูปแบบแรสเตอร์อื่น ๆ อีกหลายรูปแบบ

**ถาม: ฉันจะหา ตัวอย่างและเอกสารเพิ่มเติมได้จากที่ไหน?**  
ตอบ: เยี่ยมชม [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) เพื่อดูคู่มือและตัวอย่างโค้ดอย่างครบถ้วน

---

**อัปเดตล่าสุด:** 2026-09-08  
**ทดสอบด้วย:** Aspose.PSD for Java 24.11  
**ผู้เขียน:** Aspose

## บทเรียนที่เกี่ยวข้อง

- [ปรับขนาดภาพด้วย Aspose.PSD for Java – วาดรูปทรงและการดำเนินการภาพพื้นฐาน](/psd/java/basic-image-operations/)
- [วาดและบันทึกสี่เหลี่ยมใน PSD ด้วย Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [วิธีเปลี่ยนสีเส้นขอบใน Java ด้วย Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}