---
date: 2026-06-13
description: เรียนรู้วิธีการแทนที่ฟอนต์ในไฟล์ PSD ด้วย Aspose.PSD for Java, แปลง PSD
  เป็น PNG, และจัดการฟอนต์ที่หายไปอย่างมีประสิทธิภาพ
keywords:
- how to replace fonts
- convert psd to png
- handle missing fonts psd
linktitle: การตั้งค่าสำหรับการแทนที่ฟอนต์ที่หายไป
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to replace fonts in PSD files using Aspose.PSD for Java,
    convert PSD to PNG, and handle missing fonts efficiently.
  headline: How to Replace Fonts in PSD Files with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: '`PsdImage` is the core class that represents a PSD document in memory.'
    question: What is the primary class for loading PSD files?
  - answer: Use `PsdLoadOptions.setDefaultFontName("Arial")`.
    question: Which option sets a default replacement font?
  - answer: Yes—call `psdImage.save("output.png", new PngOptions())`.
    question: Can I save the result as PNG?
  - answer: A temporary license works for testing; a full license is required for
      production.
    question: Do I need a license for development?
  - answer: Aspose.PSD for Java supports Java 8 and later.
    question: What Java version is supported?
  type: FAQPage
second_title: Aspose.PSD Java API
title: วิธีการแทนที่ฟอนต์ในไฟล์ PSD ด้วย Aspose.PSD for Java
url: /th/java/advanced-techniques/settings-replacing-missing-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีการแทนที่ฟอนต์ในไฟล์ PSD ด้วย Aspose.PSD สำหรับ Java

ในการพัฒนา Java สมัยใหม่, **วิธีการแทนที่ฟอนต์** ในไฟล์ Photoshop (PSD) เป็นความท้าทายทั่วไปที่อาจทำให้การจัดวางภาพของคุณเสียหาย Aspose.PSD for Java มี API ที่แข็งแกร่งซึ่งทำการแทนที่ฟอนต์โดยอัตโนมัติ ช่วยให้คุณรักษาภาพให้ดูเหมือนตามที่ตั้งใจ คู่มือนี้จะพาคุณผ่านทุกขั้นตอน—ตั้งแต่การตั้งค่าสภาพแวดล้อมจนถึงการบันทึก PNG สุดท้าย—เพื่อให้คุณจัดการฟอนต์ที่หายไปในไฟล์ PSD ได้อย่างมั่นใจ

## คำตอบสั้น
- **อะไรคือคลาสหลักสำหรับการโหลดไฟล์ PSD?** `PsdImage` เป็นคลาสหลักที่แสดงเอกสาร PSD ในหน่วยความจำ.  
- **ตัวเลือกใดที่ตั้งค่าฟอนต์แทนที่เริ่มต้น?** ใช้ `PsdLoadOptions.setDefaultFontName("Arial")`.  
- **ฉันสามารถบันทึกผลลัพธ์เป็น PNG ได้หรือไม่?** ใช่—เรียก `psdImage.save("output.png", new PngOptions())`.  
- **ฉันต้องการไลเซนส์สำหรับการพัฒนาหรือไม่?** ไลเซนส์ชั่วคราวใช้ได้สำหรับการทดสอบ; ไลเซนส์เต็มจำเป็นสำหรับการใช้งานจริง.  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Aspose.PSD for Java รองรับ Java 8 และรุ่นต่อไป.

## วิธีการแทนที่ฟอนต์ในไฟล์ PSD ด้วย Aspose.PSD for Java?

โหลดไฟล์ PSD ต้นฉบับด้วย `PsdLoadOptions` ที่ระบุฟอนต์สำรอง, จากนั้นบันทึกภาพในรูปแบบที่ต้องการ API จะทำการแทนที่ glyph ที่หายไปโดยอัตโนมัติด้วยฟอนต์เริ่มต้นที่คุณกำหนด, ทำให้ข้อผิดพลาดการเรนเดอร์หายไปโดยไม่ต้องแก้ไขด้วยมือ วิธีการแบบขั้นตอนเดียวนี้ทำงานกับไฟล์ทุกขนาดและคงรักษาเลเยอร์, มาสก์, และเอฟเฟกต์ไว้

## `PsdLoadOptions` คืออะไร?

`PsdLoadOptions` เป็นอ็อบเจ็กต์การกำหนดค่าที่ควบคุมวิธีที่ Aspose.PSD วิเคราะห์ไฟล์ PSD. มันให้คุณระบุฟอนต์แทนที่เริ่มต้น, ควบคุมพฤติกรรมการโหลดเลเยอร์, และตั้งค่าตัวเลือกสำหรับการจัดการทรัพยากรที่หายไป. ด้วยการปรับคุณสมบัติเหล่านี้, นักพัฒนาสามารถรับประกันการเรนเดอร์ข้อความและองค์ประกอบอื่น ๆ อย่างสม่ำเสมอในสภาพแวดล้อมต่าง ๆ และหลีกเลี่ยงข้อผิดพลาดรันไทม์ที่เกิดจากฟอนต์ที่ไม่พร้อมใช้งาน.

## ทำไมต้องแทนที่ฟอนต์ที่หายไปในไฟล์ PSD?

Aspose.PSD รองรับ **รูปแบบเข้าและออกกว่า 50+** และสามารถประมวลผลไฟล์ PSD หลายร้อยหน้าโดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ. การแทนที่ฟอนต์ที่หายไปช่วยป้องกันเลเยอร์ข้อความที่เสียหาย, ลดเวลาการแก้ไขด้วยมือได้ถึง **80%**, และรับประกันว่า PNG ที่ส่งออกจะคงความแม่นยำของการออกแบบต้นฉบับ.

## ข้อกำหนดเบื้องต้น

1. **Aspose.PSD Library** – ดาวน์โหลดและติดตั้งไลบรารี Aspose.PSD for Java จาก [releases page](https://releases.aspose.com/psd/java/).  
2. **Java Development Environment** – Java 8+ JDK และ IDE ที่คุณชื่นชอบ (Eclipse, IntelliJ IDEA, เป็นต้น).  

เมื่อทุกอย่างพร้อมแล้ว, มาเริ่มลงมือทำการดำเนินการกัน.

## นำเข้าแพ็กเกจ

นำเข้าชื่อเนมสเปซที่จำเป็นเพื่อให้คอมไพเลอร์สามารถค้นหาคลาสของ Aspose.PSD ได้.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสารของคุณ

กำหนดโฟลเดอร์ที่บรรจุไฟล์ PSD ต้นฉบับและที่ที่ผลลัพธ์จะถูกเขียน. เส้นทางนี้จะใช้โดยตัวโหลดและตัวบันทึก.

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: ระบุไฟล์ต้นทางและไฟล์ปลายทาง

ระบุเส้นทางแบบเต็มหรือแบบสัมพันธ์สำหรับ PSD ต้นฉบับและ PNG ปลายทาง. การใช้แนวทางตั้งชื่อที่ชัดเจนช่วยหลีกเลี่ยงการเขียนทับไฟล์.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## ขั้นตอนที่ 3: กำหนดค่าการแทนที่ฟอนต์

สร้างอินสแตนซ์ของ `PsdLoadOptions` และตั้งค่าฟอนต์แทนที่เริ่มต้นเป็น **Arial** (หรือฟอนต์ใดก็ได้ที่ติดตั้งบนระบบของคุณ). สิ่งนี้บอกเอนจินว่าจะใช้ฟอนต์ใดเมื่อไม่พบฟอนต์ต้นฉบับ.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setDefaultReplacementFont("Arial");
```

## ขั้นตอนที่ 4: โหลดภาพ PSD และแทนที่ฟอนต์

โหลด PSD ด้วยตัวเลือกที่กำหนดไว้. Aspose.PSD จะทำการแทนที่ฟอนต์ที่หายไปโดยอัตโนมัติในระหว่างกระบวนการโหลด, ดังนั้นไม่จำเป็นต้องเขียนโค้ดเพิ่มเติม.

```java
Image image = Image.load(sourceFile, loadOptions);
PsdImage psdImage = (PsdImage) image;
```

## ขั้นตอนที่ 5: บันทึกภาพที่แก้ไขแล้ว

เลือก `PngOptions` เพื่อส่งออกภาพเป็น PNG true‑color พร้อมแชนแนลอัลฟา. ไฟล์ที่ได้จะแสดงฟอนต์ที่แทนที่อย่างถูกต้อง.

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
psdImage.save(destName, options);
```

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|-----|
| ข้อความแสดงเป็นอักขระผิดรูป | ฟอนต์แทนที่ไม่มี glyph ที่จำเป็น | เลือกฟอนต์ที่มีช่วง Unicode กว้างขึ้น (เช่น **Arial Unicode MS**). |
| ข้อผิดพลาดไฟล์ไม่พบ | เส้นทางไม่ถูกต้องในขั้นตอนที่ 1 หรือ 2 | ตรวจสอบสตริงของไดเรกทอรีและใช้ `File.separator` เพื่อความเข้ากันได้ข้ามแพลตฟอร์ม. |
| ข้อยกเว้นไลเซนส์ | ทำงานโดยไม่มีไลเซนส์ที่ถูกต้อง | ใช้ไลเซนส์ชั่วคราวสำหรับการทดสอบหรือซื้อไลเซนส์เต็มสำหรับการใช้งานจริง. |

## คำถามที่พบบ่อย

### Q1: Aspose.PSD รองรับเวอร์ชันไฟล์ PSD ทั้งหมดหรือไม่?
A1: Aspose.PSD รองรับเวอร์ชัน PSD ตั้งแต่ **4.0** จนถึงรุ่น Photoshop ล่าสุด, ทำให้เข้ากันได้อย่างกว้างขวางทั้งในงานออกแบบเก่าและใหม่.

### Q2: ฉันสามารถใช้ฟอนต์กำหนดเองสำหรับการแทนที่ใน Aspose.PSD ได้หรือไม่?
A2: ได้, คุณสามารถระบุฟอนต์ TrueType หรือ OpenType ใดก็ได้ที่ติดตั้งบนเซิร์ฟเวอร์โดยส่งชื่อฟอนต์ไปยัง `setDefaultFontName`. สิ่งนี้ให้คุณควบคุมผลลัพธ์ด้านภาพได้อย่างเต็มที่.

### Q3: มีตัวเลือกไลเซนส์สำหรับ Aspose.PSD หรือไม่?
A3: สำรวจตัวเลือกไลเซนส์ [ที่นี่](https://purchase.aspose.com/buy) เพื่อเลือกแผนที่เหมาะสมที่สุดสำหรับองค์กรของคุณ, รวมถึงไลเซนส์สำหรับนักพัฒนา, เว็บไซต์, และ OEM.

### Q4: มีฟอรั่มชุมชนสำหรับการสนับสนุน Aspose.PSD หรือไม่?
A4: มี, เยี่ยมชม [ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) เพื่อรับความช่วยเหลือจากชุมชน, ตัวอย่างโค้ด, และเคล็ดลับการแก้ปัญหาจากนักพัฒนาคนอื่น.

### Q5: ฉันจะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร?
A5: รับไลเซนส์ชั่วคราว [ที่นี่](https://purchase.aspose.com/temporary-license/) สำหรับการประเมิน, การทดสอบ, หรือโครงการ proof‑of‑concept โดยไม่มีค่าใช้จ่าย.

---

**อัปเดตล่าสุด:** 2026-06-13  
**ทดสอบกับ:** Aspose.PSD 24.12 for Java  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง

- [แปลง PSD เป็น PNG พร้อมการทับสี – Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rendering-color-effect/)
- [วิธีแปลง PSD เป็น PNG และปรับขนาดสัดส่วนอย่างเหมาะสมด้วย Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)
- [แปลง PSD เป็นรูปแบบภาพ Raster ด้วย Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}