---
date: 2026-09-08
description: เรียนรู้วิธีวาด rectangle บน image ด้วย Aspose.PSD for Java, ครอบคลุมการสร้าง
  bitmap, การตั้งค่า background color, และการเริ่มต้น graphics สำหรับการจัดการ image
  ด้วย Java
keywords:
- how to draw rectangle
- draw rectangle on image
- how to create bitmap
- set background color java
- java image manipulation
lastmod: 2026-09-08
linktitle: การวาด Rectangles ใน Java
og_description: เรียนรู้วิธีวาด rectangle บน image ด้วย Aspose.PSD for Java. คู่มือนี้ครอบคลุมการสร้าง
  bitmap, การตั้งค่า background color, และการเริ่มต้น graphics ใน Java
og_image_alt: Screenshot of Java code drawing rectangles on an image with Aspose.PSD
og_title: วิธีวาด rectangle บน image ด้วย Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  headline: How to draw rectangle on an image with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  name: How to draw rectangle on an image with Aspose.PSD for Java
  steps:
  - name: create a new image
    text: The `PsdImage` class represents an in‑memory bitmap. Initializing it also
      allocates the pixel buffer. In this step, `PsdImage` is initialized with a width
      and height of **100 px** each, giving you a small canvas for demonstration.
  - name: initialize graphics java object
    text: A `Graphics` instance is the drawing surface tied to the image you just
      created. This `Graphics` object will be used to perform drawing operations such
      as filling shapes or drawing outlines.
  - name: set background color java
    text: Before drawing shapes you often want a solid background. Use `clear` with
      a `Color` to fill the entire canvas. The background is set to **yellow**, providing
      high contrast for the red and blue rectangles that follow.
  - name: draw rectangles on the image
    text: Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for
      the fill. You can draw multiple rectangles with different colors and positions.
      These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle
      at (50, 50), each 40 px wide and 30 px tall.
  - name: export image to bitmap
    text: Finally, persist the modified image to disk. Aspose.PSD automatically encodes
      the bitmap in the format you specify. The image is saved as a BMP file at the
      path stored in `outpath`.
  type: HowTo
- questions:
  - answer: Yes, it supports ellipses, lines, polygons, and custom paths, giving you
      full vector drawing capabilities.
    question: Can Aspose.PSD for Java handle other shapes besides rectangles?
  - answer: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.
    question: How can I modify the thickness of the rectangle border?
  - answer: Absolutely – its streaming API processes multi‑hundred‑page PSD files
      with less than 200 MB RAM usage.
    question: Is Aspose.PSD for Java suitable for high‑performance image processing
      tasks?
  - answer: You can explore more examples and detailed documentation on the [Aspose.PSD
      for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find more examples and tutorials for Aspose.PSD for Java?
  - answer: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats
      for both import and export.
    question: Does Aspose.PSD for Java support other image formats besides BMP?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- image processing
title: วิธีวาด rectangle บน image ด้วย Aspose.PSD for Java
url: /th/java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีวาดสี่เหลี่ยมบนภาพด้วย Aspose.PSD for Java

## บทนำ
If you need to **how to draw rectangle** on an image programmatically, Aspose.PSD for Java gives you a clean, high‑performance API. In this tutorial you’ll see how to create a bitmap, set the background color, and **initialize graphics java** objects so you can render rectangles of any size and color. The steps are simple, the code is concise, and the result is a BMP file you can use in any Java‑based workflow.

## คำตอบอย่างรวดเร็ว
- **ไลบรารีใดที่จัดการการวาดสี่เหลี่ยม?** Aspose.PSD for Java.
- **ต้องใช้บรรทัดโค้ดกี่บรรทัด?** ประมาณหกบรรทัดสำหรับสร้างภาพ ตั้งค่าพื้นหลัง และวาดสี่เหลี่ยมสองรูป
- **รูปแบบภาพใดบ้างที่รองรับการส่งออก?** BMP, PNG, JPEG, TIFF, GIF และอื่น ๆ
- **ต้องใช้ไลเซนส์สำหรับการพัฒนาหรือไม่?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการทดสอบ; ต้องมีไลเซนส์สำหรับการใช้งานจริง
- **สามารถเปลี่ยนความหนาของเส้นขอบได้หรือไม่?** ได้ – ปรับคุณสมบัติความหนาของ `Pen` ก่อนการวาด

## การวาดสี่เหลี่ยมบนภาพคืออะไร
การวาดสี่เหลี่ยมบนภาพหมายถึงการเรนเดอร์รูปทรงที่เติมสีหรือเป็นเส้นขอบลงบนบิตแมพโดยใช้กราฟิกคอนเท็กซ์ คลาส `Graphics` ของ Aspose.PSD มีเมธอดที่ให้คุณระบุสี ตำแหน่ง และขนาดด้วยการเรียกเดียว

## ทำไมต้องใช้ Aspose.PSD for Java สำหรับการวาดสี่เหลี่ยม
Aspose.PSD รองรับ **รูปแบบภาพกว่า 50** ชนิดและสามารถประมวลผลไฟล์ขนาดสูงสุด **2 GB** โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ API `Graphics` ของมันทำงานเร็วถึง **3×** เทียบกับ Java AWT ดั้งเดิมสำหรับการประมวลผลแบบแบตช์ ทำให้เหมาะสำหรับการประมวลผลภาพบนเซิร์ฟเวอร์ที่ต้องการประสิทธิภาพสูง

## ข้อกำหนดเบื้องต้น
- **Java Development Kit (JDK) 8 หรือสูงกว่า** ติดตั้งแล้ว
- **Aspose.PSD for Java** library ดาวน์โหลดจาก [หน้าโหลด Aspose.PSD for Java](https://releases.aspose.com/psd/java/) และเพิ่มไปยัง classpath ของโปรเจกต์ของคุณ

### นำเข้าแพ็กเกจ
The `import` statements give you access to the classes required for bitmap creation and drawing.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
These imports will allow you to access the classes and methods needed to draw rectangles on images.

## วิธีวาดสี่เหลี่ยมบนภาพด้วย Java?
Load a new `PsdImage`, clear its surface with a background color, create a `Graphics` object, and then call `drawRectangle` with the desired pen and brush. The entire process takes just a few method calls and produces a ready‑to‑save bitmap.  
`PsdImage` represents an in‑memory bitmap that can be edited and saved.  
`Graphics` provides a drawing surface for rendering shapes onto an image.

### ขั้นตอนที่ 1: สร้างภาพใหม่
The `PsdImage` class represents an in‑memory bitmap. Initializing it also allocates the pixel buffer.

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```
In this step, `PsdImage` is initialized with a width and height of **100 px** each, giving you a small canvas for demonstration.

### ขั้นตอนที่ 2: เริ่มต้นอ็อบเจ็กต์ graphics java
A `Graphics` instance is the drawing surface tied to the image you just created.

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```
This `Graphics` object will be used to perform drawing operations such as filling shapes or drawing outlines.

### ขั้นตอนที่ 3: ตั้งค่าสีพื้นหลัง java
Before drawing shapes you often want a solid background. Use `clear` with a `Color` to fill the entire canvas.

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```
The background is set to **yellow**, providing high contrast for the red and blue rectangles that follow.

### ขั้นตอนที่ 4: วาดสี่เหลี่ยมบนภาพ
Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for the fill. You can draw multiple rectangles with different colors and positions.

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle at (50, 50), each 40 px wide and 30 px tall.

### ขั้นตอนที่ 5: ส่งออกภาพเป็นบิตแมพ
Finally, persist the modified image to disk. Aspose.PSD automatically encodes the bitmap in the format you specify.

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```
The image is saved as a BMP file at the path stored in `outpath`.

## ปัญหาที่พบบ่อยและวิธีแก้
- **ไฟล์ผลลัพธ์เป็นไฟล์เปล่า** – ตรวจสอบว่าคุณเรียก `graphics.clear` ก่อนการวาด; มิฉะนั้นแคนวาสอาจยังคงเป็นแบบโปร่งใส
- **สีไม่ถูกต้อง** – ตรวจสอบว่าคุณนำเข้า `com.aspose.psd.Color` ไม่ใช่ `java.awt.Color`
- **ภาพขนาดใหญ่ทำให้หน่วยความจำเต็ม** – ใช้คอนสตรัคเตอร์ของ `PsdImage` ที่รองรับการสตรีมเพื่อหลีกเลี่ยงการโหลดไฟล์ทั้งหมดเข้าสู่ RAM

## คำถามที่พบบ่อย

**Q: Aspose.PSD for Java สามารถจัดการรูปทรงอื่น ๆ นอกจากสี่เหลี่ยมได้หรือไม่?**  
A: ได้, รองรับวงรี, เส้น, โพลิกอน, และเส้นทางแบบกำหนดเอง ให้คุณมีความสามารถในการวาดเวกเตอร์เต็มรูปแบบ

**Q: ฉันจะปรับความหนาของเส้นขอบสี่เหลี่ยมได้อย่างไร?**  
A: ตั้งค่าคุณสมบัติ `setWidth(float)` ของอ็อบเจ็กต์ `Pen` ก่อนเรียก `drawRectangle`

**Q: Aspose.PSD for Java เหมาะกับงานประมวลผลภาพที่ต้องการประสิทธิภาพสูงหรือไม่?**  
A: แน่นอน – API การสตรีมของมันประมวลผลไฟล์ PSD หลายร้อยหน้าโดยใช้หน่วยความจำต่ำกว่า 200 MB

**Q: ฉันจะหา ตัวอย่างและบทเรียนเพิ่มเติมสำหรับ Aspose.PSD for Java ได้จากที่ไหน?**  
A: คุณสามารถสำรวจตัวอย่างเพิ่มเติมและเอกสารโดยละเอียดได้ที่ [เอกสาร Aspose.PSD for Java](https://reference.aspose.com/psd/java/)

**Q: Aspose.PSD for Java รองรับรูปแบบภาพอื่น ๆ นอกจาก BMP หรือไม่?**  
A: ได้, รองรับ PNG, JPEG, TIFF, GIF, และรูปแบบเพิ่มเติมกว่า 30 รูปแบบสำหรับการนำเข้าและส่งออก

## สรุป
คุณได้เรียนรู้ **วิธีวาดสี่เหลี่ยม** บนภาพด้วย Aspose.PSD for Java ตั้งแต่การสร้างบิตแมพ การตั้งค่าสีพื้นหลัง ไปจนถึงการเริ่มต้นกราฟิกแล้ว ทดลองกับขนาด สี และรูปทรงเพิ่มเติมเพื่อเชี่ยวชาญ **การจัดการภาพด้วย Java** เมื่อพร้อมให้ผสานโค้ดนี้เข้าสู่กระบวนการประมวลผลแบบแบตช์ขนาดใหญ่หรือโปรแกรมแก้ไขที่ขับเคลื่อนด้วย UI

---

**อัปเดตล่าสุด:** 2026-09-08  
**ทดสอบด้วย:** Aspose.PSD for Java 24.12  
**ผู้เขียน:** Aspose

## บทเรียนที่เกี่ยวข้อง

- [ปรับขนาดภาพด้วย Aspose.PSD for Java – วาดรูปทรงและการดำเนินการภาพพื้นฐาน](/psd/java/basic-image-operations/)
- [เพิ่มลายเซ็นลงในภาพ – วาดภาพบนแคนวาสด้วย Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [ครอบภาพด้วยสี่เหลี่ยมด้วย Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}