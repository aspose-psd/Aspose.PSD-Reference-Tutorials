---
date: 2025-12-30
description: เรียนรู้วิธีสร้างไฟล์ PSD ด้วย Java โดยการรวมสองภาพด้วย Aspose.PSD ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนของเราเพื่อรวมภาพเป็นไฟล์
  PSD อย่างรวดเร็ว.
linktitle: Combine Images
second_title: Aspose.PSD Java API
title: วิธีสร้างไฟล์ PSD ด้วย Java – รวมภาพด้วย Aspose.PSD
url: /th/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้างไฟล์ PSD ด้วย Java – รวมรูปภาพโดยใช้ Aspose.PSD

## บทนำ

หากคุณต้อง **สร้างไฟล์ PSD ด้วย Java** โดยการรวมรูปหลายรูป Aspose.PSD ทำให้การทำงานนี้ง่ายดาย ในบทแนะนำนี้เราจะอธิบายขั้นตอนการรวมรูปสองรูปเข้ากับแคนวาส PSD เดียว, ทำไมวิธีนี้จึงมีประโยชน์, และให้โค้ดที่พร้อมรันแล้ว เมื่อเสร็จสิ้นคุณจะสามารถ **รวมรูปสองรูปในสไตล์ Java** และสร้างไฟล์เลเยอร์ที่ดูเป็นมืออาชีพได้

## คำตอบสั้น
- **ไลบรารีที่ดีที่สุดสำหรับการรวมรูปเป็น PSD คืออะไร?** Aspose.PSD for Java  
- **ใช้เวลานานเท่าไหร่ในการทำงานนี้?** ประมาณ 10‑15 นาทีสำหรับการรวมพื้นฐาน  
- **ต้องมีลิขสิทธิ์หรือไม่?** สามารถใช้รุ่นทดลองฟรีสำหรับการทดสอบ; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **สามารถเพิ่มรูปมากกว่าสองรูปได้หรือไม่?** ได้ – เพียงทำซ้ำการเรียก `drawImage` สำหรับแต่ละเลเยอร์เพิ่มเติม  
- **รองรับเวอร์ชัน Java ใด?** Java 8 ขึ้นไป

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำงาน, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

1. **Aspose.PSD Library** – ดาวน์โหลดได้จาก [here](https://releases.aspose.com/psd/java/)  
2. **Java Development Kit (JDK)** – แนะนำให้ใช้ Java 8+  
3. **Document Directory** – โฟลเดอร์บนเครื่องของคุณที่เก็บรูปต้นฉบับและไฟล์ PSD ที่จะสร้าง

## นำเข้าแพ็กเกจ

เริ่มต้นด้วยการนำเข้าคลาส Aspose.PSD ที่จำเป็นเข้าสู่โปรเจกต์ของคุณ:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## คู่มือแบบขั้นตอน

### ขั้นตอนที่ 1: สร้าง PSD Options (เตรียมไฟล์)

เราจะสร้างอินสแตนซ์ `PsdOptions` ที่จะเก็บการตั้งค่าเอาต์พุต

```java
PsdOptions imageOptions = new PsdOptions();
```

### ขั้นตอนที่ 2: ตั้งค่า FileCreateSource (กำหนดตำแหน่งบันทึก PSD)

กำหนด `FileCreateSource` ให้กับ options โดยระบุตำแหน่งไฟล์ผลลัพธ์ที่ต้องการ

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

### ขั้นตอนที่ 3: สร้าง Image Instance (กำหนดขนาดแคนวาส)

สร้างอ็อบเจ็กต์ `Image` ด้วย options และกำหนดแคนวาสขนาด 600 × 600 พิกเซล

```java
Image image = Image.create(imageOptions, 600, 600);
```

### ขั้นตอนที่ 4: เริ่มต้น Graphics และวาดรูปแรก

อ็อบเจ็กต์ `Graphics` ช่วยให้เราวาดบนแคนวาส เราจะเคลียร์พื้นหลังเป็นสีขาวและวาดรูปต้นฉบับแรกทางด้านซ้าย

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

### ขั้นตอนที่ 5: วาดรูปที่สอง (ทำการรวมให้เสร็จ)

ต่อไปเราจะวางรูปที่สองบนครึ่งขวาของแคนวาสเดียวกัน

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

### ขั้นตอนที่ 6: บันทึกไฟล์ PSD ที่ได้

สุดท้ายบันทึกแคนวาสที่รวมแล้วลงดิสก์

```java
image.save();
```

ยินดีด้วย! คุณได้ **รวมรูปภาพเป็น PSD** และสร้างไฟล์ PSD ด้วย Java อย่างสำเร็จแล้ว

## ทำไมต้องรวมรูปภาพด้วย Aspose.PSD?

- **รองรับเลเยอร์** – การเรียก `drawImage` แต่ละครั้งจะเพิ่มเลเยอร์แยกที่สามารถแก้ไขต่อไปได้  
- **ความยืดหยุ่นของฟอร์แมต** – รองรับ PSD, PNG, JPEG, BMP และอื่น ๆ อีกมาก  
- **ไม่มีการพึ่งพาเนทีฟ** – เป็น Java แท้ ๆ ทำงานได้บนทุก OS ที่รัน JDK  

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|--------|
| เกิดข้อผิดพลาด `File not found` ขณะโหลดรูปต้นฉบับ | เส้นทาง `dataDir` ไม่ถูกต้อง | ตรวจสอบให้ `dataDir` ชี้ไปยังโฟลเดอร์ที่มี `example1.psd` และ `example2.psd` |
| PSD ผลลัพธ์เป็นสีขาวเปล่า | เรียก `graphics.clear` หลังจากวาดรูป | ให้แน่ใจว่า `graphics.clear(Color.getWhite())` ถูกเรียก **ก่อน** การเรียก `drawImage` ใด ๆ |
| เกิดข้อยกเว้น License ขณะรัน | ไม่มีหรือหมดอายุลิขสิทธิ์ Aspose.PSD | ใช้ลิขสิทธิ์ที่ถูกต้องด้วย `License license = new License(); license.setLicense("Aspose.PSD.lic");` ก่อนเรียก API ใด ๆ |

## คำถามที่พบบ่อย

### Q1: Aspose.PSD รองรับฟอร์แมตรูปภาพทั้งหมดหรือไม่?
A1: Aspose.PSD เน้นที่ฟอร์แมต PSD เป็นหลัก อย่างไรก็ตามยังรองรับฟอร์แมตอื่น ๆ สำหรับการนำเข้าและส่งออกหลายรูปแบบ

### Q2: สามารถทำการแก้ไขเพิ่มเติมบนรูปที่รวมแล้วได้หรือไม่?
A2: แน่นอน! หลังจากรวมรูปแล้ว คุณสามารถปรับแต่ง PSD ที่ได้ต่อด้วยฟีเจอร์หลากหลายของ Aspose.PSD

### Q3: มีข้อกำหนดด้านลิขสิทธิ์สำหรับการใช้ Aspose.PSD หรือไม่?
A3: มี, จำเป็นต้องมีลิขสิทธิ์ที่ถูกต้องสำหรับการใช้งานเชิงพาณิชย์ สามารถรับได้จาก [here](https://purchase.aspose.com/buy)

### Q4: มีรุ่นทดลองฟรีสำหรับ Aspose.PSD หรือไม่?
A4: มี, คุณสามารถทดลองใช้ Aspose.PSD ได้ฟรีที่ [here](https://releases.aspose.com/)

### Q5: จะหาการสนับสนุนสำหรับคำถามเกี่ยวกับ Aspose.PSD ได้จากที่ไหน?
A5: เยี่ยมชม [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) เพื่อรับการสนับสนุนจากชุมชนและการสนทนา

---

**อัปเดตล่าสุด:** 2025-12-30  
**ทดสอบด้วย:** Aspose.PSD 24.11 for Java  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}