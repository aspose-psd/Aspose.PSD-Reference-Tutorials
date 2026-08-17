---
date: 2026-03-07
description: เรียนรู้วิธีสร้างลายน้ำภาพในไฟล์ PSD ด้วย Aspose.PSD for Java – คู่มือสั้นสำหรับการประมวลผลภาพ
  PSD และการปกป้องกราฟิกของคุณ
linktitle: How to Create Image Watermark in PSD Files with Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: วิธีสร้างลายน้ำรูปภาพในไฟล์ PSD ด้วย Aspose.PSD สำหรับ Java
url: /th/java/modifying-converting-psd-images/add-watermark-psd-files/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เพิ่มลายน้ำให้ไฟล์ PSD ด้วย Aspose.PSD for Java

## Introduction
ลายน้ำเป็นวิธีที่ละเอียดอ่อนแต่มีประสิทธิภาพในการปกป้องภาพของคุณและสื่อสารความเป็นเจ้าของ ในบทเรียนนี้คุณจะได้เรียนรู้วิธี **สร้างลายน้ำภาพ** ในไฟล์ PSD ด้วย Aspose.PSD for Java ไม่ว่าคุณจะเป็นช่างภาพที่ต้องการแสดงผลงานพอร์ตโฟลิโอหรือเป็นนักออกแบบที่ต้องการนำเสนอผลงานล่าสุด การเพิ่มลายน้ำอาจเป็นสิ่งสำคัญในการรักษาอัตลักษณ์ของแบรนด์ ดังนั้นหยิบกาแฟมาสักแก้ว นั่งสบาย ๆ แล้วเริ่มกันเลย!

## Quick Answers
- **เป้าหมายหลักคืออะไร?** เพื่อสร้างลายน้ำภาพในไฟล์ PSD อย่างอัตโนมัติ.  
- **ไลบรารีที่ใช้คืออะไร?** Aspose.PSD for Java.  
- **ใช้เวลาการทำงานประมาณเท่าไหร่?** ประมาณ 10‑15 นาทีสำหรับลายน้ำพื้นฐาน.  
- **ข้อกำหนดเบื้องต้นคืออะไร?** Java JDK, ไลบรารี Aspose.PSD, และไฟล์ PSD ต้นฉบับ.  
- **ฉันสามารถส่งออกผลลัพธ์เป็น PNG ได้หรือไม่?** ได้ – ใช้เมธอด `save` พร้อม `PngOptions`.

## What is **create image watermark**?
การสร้างลายน้ำภาพหมายถึงการวางข้อความหรือกราฟิกที่มีความโปร่งแสงกึ่งครึ่งลงบนไฟล์ภาพโดยอัตโนมัติ เพื่อให้ข้อมูลความเป็นเจ้าของฝังอยู่ในเนื้อหาภาพโดยตรง

## Why use Aspose.PSD for Java for psd image processing?
Aspose.PSD มีชุด API ที่ครบครันสำหรับ **psd image processing** ช่วยให้คุณจัดการเลเยอร์, ใช้เอฟเฟกต์, และเรนเดอร์ภาพสุดท้ายโดยไม่ต้องใช้ Photoshop รองรับการเรนเดอร์ที่มีความละเอียดสูง, การทำงานเป็นชุด, และทำงานได้บนระบบปฏิบัติการหลักทั้งหมด

## Prerequisites
ก่อนจะลงมือเขียนโค้ด ให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1. **Java Development Kit (JDK)** – เวอร์ชันล่าสุดใดก็ได้ (8 หรือสูงกว่า)  
2. **Aspose.PSD for Java Library** – ดาวน์โหลดจาก [Aspose website](https://releases.aspose.com/psd/java/)  
3. **IDE** – Eclipse, IntelliJ IDEA หรือโปรแกรมแก้ไขใดก็ได้ที่คุณชอบ  
4. **PSD File** – ตัวอย่างไฟล์ชื่อ `layers.psd` ที่วางไว้ในไดเรกทอรีทำงานของคุณ  
5. **Basic Java knowledge** – ความคุ้นเคยกับคลาส, อ็อบเจ็กต์, และการทำ I/O ของไฟล์

## Import Packages
ตอนนี้คุณได้ตั้งค่าทุกอย่างเรียบร้อยแล้ว มา import แพ็กเกจที่จำเป็นกันดีกว่า Import ใน Java ช่วยให้คุณนำคลาสและฟังก์ชันจากไลบรารีต่าง ๆ มาใช้ได้อย่างมีประสิทธิภาพ ด้านล่างคือสิ่งที่คุณต้องใช้:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## How to **create image watermark** – Step‑by‑Step Guide

### Step 1: Set Up Your Directory
ขั้นแรก เราต้องกำหนดเส้นทางที่ไฟล์ PSD ของคุณอยู่ ซึ่งสำคัญมากเพราะ Java ต้องรู้ว่าจะหาไฟล์จากที่ไหน

```java
String dataDir = "Your Document Directory";
```

แทนที่ `Your Document Directory` ด้วยโฟลเดอร์จริงที่มี `layers.psd`

### Step 2: Load the PSD File
ต่อไปเราจะโหลดไฟล์ PSD และแคสท์เป็น `PsdImage` ขั้นตอนนี้ทำให้ไฟล์แปลงเป็นรูปแบบที่เราสามารถจัดการได้

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

คิดว่าเป็นการเปิดหนังสือเพื่อให้คุณเริ่มเขียนบนหน้าของมันได้

### Step 3: Create a Graphics Object
เมื่อไฟล์ PSD ถูกโหลดแล้ว เราต้องสร้างอ็อบเจ็กต์ `Graphics` เพื่อทำการวาด ซึ่งเปรียบเสมือนการหยิบแปรงสีมาวาดบนผ้าใบของคุณ

```java
Graphics graphics = new Graphics(psdImage);
```

### Step 4: Define the Font for Your Watermark
ต่อไปคือการกำหนดฟอนต์สำหรับลายน้ำ เราจะใช้ Arial ขนาด 20 คุณสามารถเปลี่ยนชื่อฟอนต์หรือขนาดให้ตรงกับสไตล์แบรนด์ของคุณได้ตามต้องการ

```java
Font font = new Font("Arial", 20.0f);
```

### Step 5: Create a Solid Brush for Watermarking
บรัชแบบทึบจะกำหนดสีและความโปร่งแสงของลายน้ำ เราจะตั้งค่า alpha เป็น 50 (จาก 255) เพื่อให้สีเทากึ่งโปร่งแสง

```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```

ที่นี่ `Color.fromArgb(50, 128, 128, 128)` สร้างสีเทาที่มีความโปร่งแสง 50% – เหมาะสำหรับลายเซ็นที่ละเอียดอ่อน

### Step 6: Set String Alignment for Your Watermark
เพื่อให้ลายน้ำอยู่ตรงกลางภาพ เราจะกำหนดตัวเลือกการจัดแนวข้อความ

```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
sf.setLineAlignment(StringAlignment.Center);
```

### Step 7: Draw the Watermark Using **java graphics drawstring**
ตอนนี้เรามาถึงส่วนที่น่าตื่นเต้นแล้ว ด้วยคอนเท็กซ์กราฟิกที่พร้อม เราจะวาดข้อความลายน้ำลงบนภาพโดยใช้ `java graphics drawstring`

```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, 0, psdImage.getWidth(), psdImage.getHeight()), sf);
```

แทนที่ `"Some watermark text"` ด้วยข้อความลายน้ำที่คุณต้องการให้ปรากฏบน PSD

### Step 8: **Save PSD as PNG** – **export psd png**
เมื่อลายน้ำถูกใส่ลงไปแล้ว เราจะ **save psd png** (คือส่งออก PSD เป็น PNG) เพื่อให้ผลลัพธ์สามารถดูได้ในเบราว์เซอร์หรือโปรแกรมดูรูปใด ๆ

```java
psdImage.save(dataDir + "AddWatermark_output.png", new PngOptions());
```

การรันบรรทัดนี้จะสร้างไฟล์ PNG ใหม่ที่มีลายน้ำของคุณอยู่

## Common Issues and Solutions
- **ลายน้ำไม่ปรากฏ?** ตรวจสอบค่า alpha ใน `Color.fromArgb()`; ค่าต่ำทำให้ลายน้ำโปร่งแสงมากขึ้น  
- **ขนาดไม่ตรง?** ตรวจสอบว่าคุณใช้ `psdImage.getWidth()` และ `psdImage.getHeight()` สำหรับสี่เหลี่ยมเพื่อให้ข้อความปรับขนาดตามภาพ  
- **ข้อยกเว้นใบอนุญาต?** ใบอนุญาตทดลองชั่วคราวใช้ได้สำหรับการทดสอบ แต่ต้องมีใบอนุญาตเต็มสำหรับการใช้งานจริง

## Frequently Asked Questions

**Q: ฉันสามารถปรับแต่งข้อความลายน้ำได้หรือไม่?**  
A: แน่นอน! เพียงเปลี่ยนสตริงในเมธอด `drawString` เป็นข้อความที่คุณต้องการ

**Q: ถ้าฉันต้องการฟอนต์อื่นล่ะ?**  
A: เปลี่ยนการสร้าง `Font` เป็นฟอนต์ที่ติดตั้งอยู่ใดก็ได้ เช่น `new Font("Times New Roman", 24.0f)`

**Q: มีวิธีปรับความโปร่งแสงได้หรือไม่?**  
A: มี – ปรับพารามิเตอร์แรกของ `Color.fromArgb(alpha, r, g, b)` ค่า `alpha` ที่ต่ำกว่าจะทำให้โปร่งแสงมากขึ้น

**Q: ฉันสามารถใช้รูปแบบภาพอื่นนอกจาก PNG ได้หรือไม่?**  
A: ได้เลย แทนที่ `new PngOptions()` ด้วย `new JpegOptions()` หรือ `new BmpOptions()` เพื่อ **save psd png** ในรูปแบบอื่น

**Q: จะหาความช่วยเหลือเพิ่มเติมได้จากที่ไหน?**  
A: สำหรับคำถามละเอียด สามารถเยี่ยมชม [Aspose forums](https://forum.aspose.com/c/psd/34) หรือดู [documentation](https://reference.aspose.com/psd/java/) ของพวกเขา

## Conclusion
คุณได้เรียนรู้วิธี **สร้างลายน้ำภาพ** ในไฟล์ PSD ด้วย Aspose.PSD for Java แล้ว เทคนิคนี้ไม่เพียงช่วยปกป้องเนื้อหาของคุณ แต่ยังเสริมสร้างการแสดงแบรนด์ในทุกสื่อภาพของคุณ ลองทดลองใช้ฟอนต์, สี, และระดับความโปร่งแสงต่าง ๆ เพื่อให้ตรงกับสไตล์ของคุณ และอย่าลืมว่าคุณสามารถ **save psd png** หรือ **export psd png** ไปยังรูปแบบใดก็ได้ที่ต้องการ

---

**Last Updated:** 2026-03-07  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}