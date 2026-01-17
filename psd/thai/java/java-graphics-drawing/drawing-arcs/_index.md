---
date: 2026-01-17
description: เรียนรู้วิธีการวาดส่วนโค้งด้วยกราฟิก Java โดยใช้ Aspose.PSD สำหรับ Java
  คู่มือแบบทีละขั้นตอนพร้อมตัวอย่างโค้ดสำหรับแอปพลิเคชันกราฟิก
linktitle: Java Graphics Draw Arc with Aspose.PSD
second_title: Aspose.PSD Java API
title: Java Graphics วาดส่วนโค้งด้วย Aspose.PSD – คู่มือแบบทีละขั้นตอน
url: /th/java/java-graphics-drawing/drawing-arcs/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Graphics Draw Arc ด้วย Aspose.PSD

## Introduction
ในบทแนะนำนี้คุณจะได้เรียนรู้วิธี **java graphics draw arc** ด้วยไลบรารี Aspose.PSD for Java การวาดส่วนโค้ง (arc) ด้วยโปรแกรมเป็นประโยชน์สำหรับส่วนประกอบ UI ที่กำหนดเอง การแสดงผลข้อมูล หรือกราฟิกใด ๆ ที่ต้องการการควบคุมเส้นโค้งอย่างแม่นยำ เราจะเดินผ่านทุกขั้นตอน—from การตั้งค่าโปรเจกต์จนถึงการเรนเดอร์ส่วนโค้งและบันทึกผลลัพธ์—เพื่อให้คุณสามารถเพิ่มความสามารถนี้ลงในแอปพลิเคชัน Java ของคุณได้ทันที

## Quick Answers
- **ไลบรารีใดที่ทำให้ Java วาดส่วนโค้งได้ง่าย?** Aspose.PSD for Java.  
- **ต้องใช้ลิขสิทธิ์สำหรับการพัฒนาหรือไม่?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการทดสอบ; ต้องมีลิขสิทธิ์สำหรับการใช้งานจริง.  
- **รูปแบบผลลัพธ์ที่รองรับมีอะไรบ้าง?** BMP, PNG, JPEG, TIFF, GIF และอื่น ๆ.  
- **สามารถเปลี่ยนความหนาหรือสีของส่วนโค้งได้หรือไม่?** ได้—ปรับคุณสมบัติของอ็อบเจกต์ `Pen`.  
- **โค้ดนี้เข้ากันได้กับ Java 8+ หรือไม่?** แน่นอน, API รองรับ Java 8 และใหม่กว่า.

## What is “java graphics draw arc”?
วลีนี้หมายถึงการใช้โค้ด Java เพื่อวาดส่วนโค้ง (arc) บนแคนวาสกราฟิก ด้วย Aspose.PSD คุณจะได้คลาสระดับสูง `Graphics` ที่ทำให้การวาดง่ายขึ้น จัดการสี การทำ anti‑aliasing และการส่งออกไฟล์โดยอัตโนมัติ

## Why use Aspose.PSD for arc drawing?
- **Full PSD support** – สร้างหรือแก้ไขไฟล์ Photoshop ได้โดยไม่ต้องติดตั้ง Photoshop.  
- **Rich drawing API** – เมธอดเช่น `drawArc` ให้คุณระบุขนาด มุม และสไตล์ในคำสั่งเดียว.  
- **Cross‑format export** – บันทึกส่วนโค้งของคุณเป็น BMP, PNG, JPEG ฯลฯ เพียงไม่กี่บรรทัดโค้ด.  
- **Performance‑focused** – ปรับให้ทำงานได้เร็วกับภาพขนาดใหญ่และการประมวลผลแบบแบตช์.

## Prerequisites
1. **Java Development Environment** – ติดตั้ง Java (JDK 8 หรือใหม่กว่า) ดาวน์โหลดจาก [Oracle's website](https://www.oracle.com/java/).  
2. **Aspose.PSD for Java** – รับไลบรารีจาก [download page](https://releases.aspose.com/psd/java/) แล้วเพิ่มไฟล์ JAR ไปยัง classpath ของโปรเจกต์ของคุณ.

## Import Packages
ก่อนอื่นให้นำเข้าคลาส Aspose.PSD ที่จำเป็น:

```java
import com.aspose.psd.Color;
import static com.aspose.psd.ColorAdjustType.Pen;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

การนำเข้าต่าง ๆ นี้ทำให้คุณเข้าถึงการกำหนดสี เครื่องมือวาด ภาพคอนเทนเนอร์ และตัวเลือกการบันทึกไฟล์

## Step‑by‑Step Guide

### Step 1: Set Up Your Java Project
สร้างโปรเจกต์ Maven หรือ Gradle ใหม่ เพิ่มไฟล์ JAR ของ Aspose.PSD แล้วตรวจสอบว่า IDE สามารถ resolve การนำเข้าได้โดยไม่มีข้อผิดพลาด

### Step 2: Initialize Image and Graphics Objects
สร้างแคนวาส `PsdImage` ว่างและอ็อบเจกต์ `Graphics` เพื่อวาด:

```java
String dataDir = "Your Document Directory";
// Initialize PsdImage object
PsdImage image = new PsdImage(100, 100);
// Initialize Graphics object and clear surface
Graphics graphics = new Graphics(image);
graphics.clear(Color.getYellow());
```

แทนที่ `"Your Document Directory"` ด้วยโฟลเดอร์ที่คุณต้องการบันทึกไฟล์ผลลัพธ์

### Step 3: Define Arc Parameters
กำหนดขนาดและมุมที่ทำให้เกิดส่วนโค้ง:

```java
int width = 100;
int height = 200;
int startAngle = 45;
int sweepAngle = 270;
```

คุณสามารถปรับตัวเลขเหล่านี้ให้เข้ากับสไตล์ที่ต้องการได้ตามใจชอบ

### Step 4: Draw and Save the Arc
ใช้เมธอด `drawArc` แล้วส่งออกภาพ:

```java
// Draw arc with specified Pen object (black color) and parameters
graphics.drawArc(new Pen(Color.getBlack()), 0, 0, width, height, startAngle, sweepAngle);
// Save the image in BMP format
String outputPath = dataDir + "Arc.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

โค้ดนี้จะวาดส่วนโค้งสีดำบนพื้นหลังสีเหลืองและบันทึกผลลัพธ์เป็น `Arc.bmp` เปลี่ยน `outputPath` และ `BmpOptions` หากต้องการฟอร์แมตหรือคุณภาพอื่น

## Common Issues & Solutions
- **File not found error** – ตรวจสอบให้แน่ใจว่า `dataDir` ลงท้ายด้วยตัวคั่นเส้นทาง (`/` หรือ `\\`) และโฟลเดอร์มีอยู่จริง.  
- **Arc appears as a line** – ยืนยันว่า `width` และ `height` มากกว่า 0 และ `sweepAngle` ไม่เป็นหลายของ 360° (ซึ่งจะทำให้เป็นวงรีเต็ม).  
- **Color not applied** – ใช้ `new Pen(Color.getRed())` หรือกำหนด `pen.setWidth(2)` เพื่อให้เห็นผลชัดเจนขึ้น.

## Frequently Asked Questions

**Q: Aspose.PSD for Java สามารถจัดการรูปทรงอื่น ๆ นอกจากส่วนโค้งได้หรือไม่?**  
A: ได้, รองรับสี่เหลี่ยม, วงรี, เส้นตรง และพาธที่กำหนดเองผ่าน `Graphics` API เดียวกัน.

**Q: จะเปลี่ยนความหนาหรือสีของส่วนโค้งอย่างไร?**  
A: สร้าง `Pen` ด้วย `Color` และ `Width` ที่ต้องการ (เช่น `new Pen(Color.getBlue(), 3)`) แล้วส่งให้ `drawArc`.

**Q: สามารถส่งออกส่วนโค้งเป็นฟอร์แมตอื่น ๆ นอกจาก BMP ได้หรือไม่?**  
A: แน่นอน. ใช้ `PngOptions`, `JpegOptions`, `TiffOptions` ฯลฯ แทน `BmpOptions`.

**Q: จะหา ตัวอย่างและการสนับสนุนเพิ่มเติมได้จากที่ไหน?**  
A: เยี่ยมชม [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) เพื่อรับความช่วยเหลือจากชุมชน, เอกสารอย่างเป็นทางการ, และโค้ดตัวอย่าง.

## Conclusion
คุณมีตัวอย่างครบถ้วนพร้อมใช้งานสำหรับการ **java graphics draw arc** ด้วย Aspose.PSD for Java แล้ว โดยการปรับพารามิเตอร์, การตั้งค่า Pen, และตัวเลือกการส่งออก คุณสามารถผสานส่วนโค้งที่กำหนดเองเข้าไปในเวิร์กโฟลว์กราฟิกของ Java ใด ๆ ได้อย่างง่ายดาย

---

**Last Updated:** 2026-01-17  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}