---
date: 2026-03-04
description: เรียนรู้วิธีสร้างวัตถุกราฟิกใน Java และเพิ่มลายน้ำแนวทแยงมุมลงในไฟล์
  PSD ด้วย Aspose.PSD คู่มือแบบขั้นตอนนี้ครอบคลุมการใช้งานไลบรารีลายน้ำรูปภาพใน Java.
linktitle: Add Diagonal Watermark to PSD Files with Java
second_title: Aspose.PSD Java API
title: สร้างวัตถุกราฟิกใน Java – ลายน้ำแนวทแยงสำหรับ PSD
url: /th/java/modifying-converting-psd-images/add-diagonal-watermark-psd-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เพิ่มลายน้ำแนวทแยงมุมในไฟล์ PSD ด้วย Java

## Introduction
ในบทเรียนนี้คุณจะ **create graphics object java** และใช้เพื่อเพิ่มลายน้ำแนวทแยงมุมในไฟล์ PSD ไม่ว่าคุณจะเป็นนักออกแบบที่ต้องการปกป้องผลงานศิลปะของคุณหรือเป็นนักการตลาดที่ต้องการใส่แบรนด์ลงบนภาพ ลายน้ำที่เรียบง่ายสามารถทำให้งานของคุณดูเป็นมืออาชีพและปลอดภัย เราจะอธิบายแต่ละขั้นตอนอย่างชัดเจน เพื่อให้คุณสามารถนำเทคนิคนี้ไปใช้ในโปรเจกต์ของคุณได้อย่างรวดเร็ว

## Quick Answers
- **ต้องใช้ไลบรารีอะไร?** Aspose.PSD for Java (ไลบรารี java image watermark ที่แข็งแรง)  
- **คีย์เวิร์ดหลักของบทเรียนนี้คืออะไร?** create graphics object java.  
- **ต้องมีลิขสิทธิ์หรือไม่?** ทดลองใช้งานฟรีได้สำหรับการทดสอบ; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **สามารถเปลี่ยนข้อความและสไตล์ของลายน้ำได้หรือไม่?** ได้ – คุณสามารถปรับฟอนต์, สี, ความทึบ, และการหมุนได้  
- **รองรับรูปแบบไฟล์เอาต์พุตอะไรบ้าง?** ตัวอย่างบันทึกเป็น PNG, แต่ Aspose.PSD สามารถส่งออกเป็น PSD, JPEG, BMP และอื่น ๆ อีกมากมาย

## What is a Graphics Object in Java?
อ็อบเจ็กต์ **Graphics** แสดงถึงพื้นผิวการวาดสำหรับภาพ โดยการสร้าง graphics object คุณจะเข้าถึงเมธอดที่ให้คุณวาดข้อความ, รูปร่าง, และองค์ประกอบภาพอื่น ๆ ลงบนบิตแมปหรือแคนวาส PSD ได้โดยตรง นี่คือแนวคิดหลักของคีย์เวิร์ด **create graphics object java**  

## Why Use Aspose.PSD for Watermarking?
Aspose.PSD เป็น **java image watermark library** เฉพาะที่ทำงานโดยไม่ต้องใช้ Adobe Photoshop ให้คุณควบคุมเลเยอร์, การเรนเดอร์ข้อความ, และการแปลงภาพได้อย่างเต็มที่ เหมาะสำหรับการประมวลผลบนเซิร์ฟเวอร์หรือการทำงานเป็นชุด

## Prerequisites
ก่อนที่เราจะลงลึกในโค้ด โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมแล้ว:

### 1. Java Development Environment
ติดตั้ง JDK เวอร์ชันล่าสุดจาก [Java website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)

### 2. Aspose.PSD Library
ดาวน์โหลดไลบรารีจาก [Aspose Downloads page](https://releases.aspose.com/psd/java/) แล้วเพิ่ม JAR ไปยังโปรเจกต์ของคุณผ่าน Maven, Gradle หรือการเพิ่มคลาสพาธด้วยตนเอง

### 3. Basic Understanding of Java
ความคุ้นเคยกับคลาส, อ็อบเจ็กต์, และการทำ I/O กับไฟล์จะช่วยให้คุณตามขั้นตอนได้อย่างราบรื่น

### 4. IDE Setup
ใช้ IntelliJ IDEA, Eclipse หรือ NetBeans เพื่อประสบการณ์การเขียนโค้ดที่สะดวกสบาย

## Import Packages
เพื่อจัดการไฟล์ PSD ให้นำเข้าคลาส Aspose.PSD ที่จำเป็นดังนี้:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Matrix;
import com.aspose.psd.PointF;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

ตอนนี้เรามีสิ่งที่ต้องเตรียมพร้อมและได้ทำการนำเข้าชุดแพ็กเกจที่จำเป็นแล้ว เราจะไปดูขั้นตอนการเพิ่มลายน้ำแนวทแยงมุมในไฟล์ PSD กันต่อ

## Step 1: Set Up Your Directory
```java
String dataDir = "Your Document Directory";
```
แทนที่ `"Your Document Directory"` ด้วยเส้นทางโฟลเดอร์ที่เก็บไฟล์ PSD ต้นฉบับของคุณ

## Step 2: Load the PSD File
```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```
เมธอด `Image.load` จะอ่านไฟล์และแคสต์เป็น `PsdImage` เพื่อให้เราสามารถใช้ฟีเจอร์เฉพาะของ PSD ได้

## Step 3: Create a Graphics Object
```java
Graphics graphics = new Graphics(psdImage);
```
ที่นี่เราจะ **create graphics object java** — แคนวาสที่เราจะวาดลายน้ำลงไป

## Step 4: Create a Font for the Watermark
```java
Font font = new Font("Arial", 20.0f);
```
เลือกฟอนต์ที่ติดตั้งไว้ใดก็ได้; ขนาดฟอนต์จะกำหนดความเด่นของลายน้ำ

## Step 5: Create a Brush for the Watermark
```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```
ค่าพารามิเตอร์ `alpha` (พารามิเตอร์แรก) กำหนดความโปร่งแสง ค่า alpha 50 จะให้ลายน้ำดูอ่อนละมุนและกึ่งโปร่งใส

## Step 6: Set Up the Transform Matrix
```java
graphics.setTransform(new Matrix());
graphics.getTransform().rotateAt(45, new PointF(psdImage.getWidth() / 2, psdImage.getHeight() / 2));
```
เราจะหมุนพื้นผิวการวาด 45° รอบศูนย์กลางของภาพ เพื่อสร้างเอฟเฟกต์แนวทแยงมุม

## Step 7: Define String Alignment
```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
```
การจัดตำแหน่งแบบศูนย์กลางทำให้ลายน้ำอยู่ตรงกลางของสี่เหลี่ยมที่หมุนแล้วอย่างสวยงาม

## Step 8: Draw the Watermark
```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, psdImage.getHeight() / 2, psdImage.getWidth(), psdImage.getHeight() / 2), sf);
```
แทนที่ `"Some watermark text"` ด้วยชื่อแบรนด์หรือข้อความลิขสิทธิ์ของคุณ สี่เหลี่ยมกำหนดตำแหน่งที่ข้อความจะถูกเรนเดอร์

## Step 9: Save the Image
```java
psdImage.save(dataDir + "AddDiagnolWatermark_output.png", new PngOptions());
```
ผลลัพธ์จะถูกบันทึกเป็น PNG, แต่คุณสามารถเลือกฟอร์แมตใดก็ได้ที่ Aspose.PSD รองรับ

## Common Use Cases
- **Brand protection:** เพิ่มโลโก้กึ่งโปร่งใสเพื่อป้องกันการนำไปใช้โดยไม่ได้รับอนุญาต  
- **Batch processing:** ทำงานอัตโนมัติในการใส่ลายน้ำสำหรับไลบรารีภาพขนาดใหญ่บนเซิร์ฟเวอร์  
- **Creative previews:** แสดงร่างที่มีลายน้ำให้ลูกค้าเห็นในขณะที่ไฟล์ต้นฉบับยังคงไม่ถูกแก้ไข

## Troubleshooting & Tips
- **Transparency not visible?** เพิ่มค่า alpha (เช่น `100`) เพื่อทำให้ลายน้ำเด่นชัดขึ้น  
- **Watermark appears off‑center?** ตรวจสอบว่าจุดหมุนใช้ค่าความกว้าง/ความสูงของภาพที่หารด้วยสองอย่างแม่นยำ  
- **Performance concerns:** ใช้อ็อบเจ็กต์ `Graphics` เดียวกันซ้ำเมื่อประมวลผลหลายภาพในลูป

## FAQ's
### What is Aspose.PSD?
Aspose.PSD เป็นไลบรารี Java ที่ใช้สำหรับทำงานและจัดการไฟล์ PSD โดยไม่ต้องอาศัย Adobe Photoshop

### Can I use other fonts for watermarking?
ได้, คุณสามารถเลือกฟอนต์ใดก็ได้ที่ติดตั้งบนระบบของคุณสำหรับการใส่ลายน้ำ

### Is there a way to customize the watermark's transparency?
แน่นอน! คุณสามารถปรับค่า alpha ใน SolidBrush เพื่อเปลี่ยนความโปร่งแสงของลายน้ำได้

### Can I add multiple watermarks?
ได้, คุณสามารถเรียกเมธอด `drawString` หลายครั้งพร้อมพารามิเตอร์ที่แตกต่างกันเพื่อเพิ่มลายน้ำหลายชิ้น

### Where can I find more information about Aspose.PSD?
คุณสามารถดูเอกสารเพิ่มเติมได้ที่ [here](https://reference.aspose.com/psd/java/)

---

**Last Updated:** 2026-03-04  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}