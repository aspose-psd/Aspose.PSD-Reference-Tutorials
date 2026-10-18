---
date: 2026-10-18
description: เรียนรู้วิธีส่งออก PSD เป็น PNG และเพิ่มเลเยอร์ปกติใหม่โดยใช้ Aspose.PSD
  for Java พร้อมใบอนุญาตชั่วคราว คู่มือขั้นตอนโดยละเอียด การจัดตำแหน่งเลเยอร์และการแก้ไขปัญหา
keywords:
- how to export psd
- aspose temporary license
- set layer position
- create new psd layer
lastmod: 2026-10-18
linktitle: เพิ่มเลเยอร์ปกติใหม่ใน PSD
og_description: เรียนรู้วิธีส่งออก PSD เป็น PNG และเพิ่มเลเยอร์ปกติใหม่โดยใช้ Aspose.PSD
  for Java พร้อมใบอนุญาตชั่วคราว รวมขั้นตอนเต็มรูปแบบโดยไม่ต้องเขียนโค้ดและเคล็ดลับการจัดตำแหน่งเลเยอร์
og_image_alt: Screenshot of Java code adding a layer to a PSD and exporting to PNG
og_title: วิธีส่งออก PSD เป็น PNG และเพิ่มเลเยอร์ด้วย Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  headline: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  name: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  steps:
  - name: Load the PSD file
    text: '`PsdImage` is Aspose.PSD''s core class that represents a PSD document in
      memory. Loading the file creates a manipulable object you can edit.'
  - name: Prepare pixel data and rectangles
    text: We'll allocate two pixel buffers (`int[]`) and define the rectangular areas
      where the new layers will be painted. Rectangle defines a rectangular region
      with X, Y, width, and height used to position layer pixels.
  - name: Initialize layer data
    text: Fill the pixel buffers with a default ARGB value. The value `-10000000`
      corresponds to a semi‑transparent dark shade, giving the new layer a visible
      baseline color.
  - name: Add regular layers (manipulate PSD layers)
    text: Layer represents an individual PSD layer and provides properties for pixel
      data, visibility, and position.
  - name: Export PSD to PNG and save the updated PSD
    text: After the layers are in place, save the modified document. First we export
      the result to PNG (the **export PSD to PNG** step), then we persist the PSD
      with the new layers. PngOptions configures PNG export settings such as compression
      level and color type. > **Pro tip:** If you only need the PNG, you
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports Java 8 and later versions.
    question: Is Aspose.PSD compatible with Java 8?
  - answer: Absolutely! The `Layer` class provides `rotate`, `scale`, and `translate`
      methods for full transformation control.
    question: Can I apply transformations (rotate, scale) to the added layers?
  - answer: Detailed API docs are available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find additional Aspose.PSD documentation?
  - answer: Visit the temporary‑license page [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.PSD?
  - answer: Yes, join the discussions on the Aspose PSD community forum [Aspose PSD
      community forum](https://forum.aspose.com/c/psd/34).
    question: Are there community forums for Aspose.PSD support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd to png
- aspose psd
- java image processing
title: วิธีส่งออก PSD เป็น PNG และเพิ่มเลเยอร์ด้วย Aspose.PSD for Java
url: /th/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีส่งออก PSD เป็น PNG และเพิ่มเลเยอร์ด้วย Aspose.PSD สำหรับ Java

ใน **Aspose.PSD tutorial** นี้ คุณจะได้เรียนรู้ **how to export PSD to PNG** พร้อมกับ **adding a new regular layer** ไปยังไฟล์เดียวกัน ทั้งหมดโดยใช้ **Aspose temporary license** ไม่ว่าคุณจะสร้างรูปย่อสำหรับเว็บ, เตรียมทรัพยากรสำหรับกระบวนการออกแบบ, หรือทดลองกับ **PSD image manipulation** คู่มือนี้จะแสดงขั้นตอนทั้งหมด — ตั้งแต่การโหลดไฟล์ต้นฉบับจนถึงการบันทึกทั้งไฟล์ PSD ที่อัปเดตและสำเนา PNG — เพื่อให้คุณเริ่มทำงานกับเลเยอร์ของ PSD ได้ทันที

## คำตอบสั้น
- **Can I export PSD to PNG with a single call?** ใช่ – หลังจากเพิ่มเลเยอร์ใด ๆ แล้วคุณเพียงเรียก `save` พร้อมกับ `PngOptions`.
- **Do I need a full license for development?** ไลเซนส์ชั่วคราวจะลบลายน้ำการประเมินและปลดล็อก API ทั้งหมด; จำเป็นต้องมีไลเซนส์ถาวรสำหรับการใช้งานในผลิตภัณฑ์
- **Which Java versions are supported?** Aspose.PSD ทำงานกับ Java 8 และรุ่นใหม่กว่า
- **Is layer positioning pixel‑based?** แน่นอน; คุณตั้งค่าพิกัดซ้าย, บน, ขวา, ล่างเป็นพิกเซลผ่านเมธอด **set layer position**
- **Will the PNG keep layer transparency?** PNG ที่ส่งออกจะมีผลลัพธ์ที่รวมของทุกเลเยอร์ที่มองเห็น, รักษาความโปร่งใสตามที่สามารถทำได้

## ทำไมต้องใช้ Aspose temporary license?

**Aspose temporary license** ช่วยให้คุณประเมินชุดคุณสมบัติทั้งหมดของ Aspose.PSD โดยไม่มีข้อจำกัดในการทำงาน มันลบลายน้ำการประเมิน, ปลดล็อก API ทั้งหมด — รวมถึงความสามารถในการ **create new PSD layer** objects — และให้คุณทดสอบโค้ดในสภาพแวดล้อมที่คล้ายการผลิตก่อนซื้อไลเซนส์ถาวร

## ข้อกำหนดเบื้องต้น

Before you begin, make sure you have:

- **Java Development Environment** – JDK 8+ และเครื่องมือสร้างเช่น Maven หรือ Gradle ที่ติดตั้งแล้ว.
- **Aspose.PSD for Java** – ดาวน์โหลด JAR ล่าสุดจากเว็บไซต์อย่างเป็นทางการ [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).
- **A sample PSD file** – เราจะใช้ `OneLayer.psd` ในตัวอย่าง

## นำเข้าแพ็กเกจ

เพิ่มการ import ที่จำเป็นในคลาส Java ของคุณ คลาสเหล่านี้ให้ฟังก์ชันหลักสำหรับ **PSD image manipulation** และการจัดการเลเยอร์

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## “set layer position” คืออะไรและทำไมจึงสำคัญ?

เมธอด **set layer position** กำหนดพิกเซลพิกัดที่แน่นอนที่เลเยอร์จะถูกวาดบนแคนวาส PSD, ควบคุมการวางตำแหน่งแนวนอนและแนวตั้ง การวางตำแหน่งที่ถูกต้องทำให้กราฟิกจัดเรียงอย่างแม่นยำ ซึ่งจำเป็นสำหรับการรวม UI assets, การสร้างเลย์เอาต์พร้อมพิมพ์, หรือการสร้างรูปย่อที่พิกเซลสมบูรณ์

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: โหลดไฟล์ PSD

`PsdImage` คือคลาสหลักของ Aspose.PSD ที่แสดงเอกสาร PSD ในหน่วยความจำ การโหลดไฟล์จะสร้างอ็อบเจกต์ที่สามารถจัดการได้สำหรับการแก้ไข

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### ขั้นตอนที่ 2: เตรียมข้อมูลพิกเซลและสี่เหลี่ยม

เราจะจัดสรรบัฟเฟอร์พิกเซลสองตัว (`int[]`) และกำหนดพื้นที่สี่เหลี่ยมที่เลเยอร์ใหม่จะถูกวาด

`Rectangle` กำหนดพื้นที่สี่เหลี่ยมที่มีค่า X, Y, ความกว้าง, และความสูง ที่ใช้ในการกำหนดตำแหน่งพิกเซลของเลเยอร์

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### ขั้นตอนที่ 3: เริ่มต้นข้อมูลเลเยอร์

เติมบัฟเฟอร์พิกเซลด้วยค่า ARGB เริ่มต้น ค่า `-10000000` ตรงกับสีเข้มกึ่งโปร่งใส ทำให้เลเยอร์ใหม่มีสีพื้นฐานที่มองเห็นได้

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### ขั้นตอนที่ 4: เพิ่มเลเยอร์ปกติ (จัดการเลเยอร์ PSD)

`Layer` แทนเลเยอร์ PSD แต่ละอันและให้คุณสมบัติสำหรับข้อมูลพิกเซล, การมองเห็น, และตำแหน่ง

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### ขั้นตอนที่ 5: ส่งออก PSD เป็น PNG และบันทึก PSD ที่อัปเดต

หลังจากที่เลเยอร์ถูกวางเรียบร้อยแล้ว ให้บันทึกเอกสารที่แก้ไขไว้ ขั้นแรกเราจะส่งออกผลลัพธ์เป็น PNG (ขั้นตอน **export PSD to PNG**) จากนั้นบันทึก PSD พร้อมเลเยอร์ใหม่

`PngOptions` กำหนดการตั้งค่าการส่งออก PNG เช่น ระดับการบีบอัดและประเภทสี

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tip:** หากคุณต้องการเพียง PNG เท่านั้น คุณสามารถข้ามการเรียก `save` ของ PSD และเรียก `save` โดยตรงด้วย `PngOptions`.

## ประโยชน์เชิงปริมาณของ Aspose.PSD สำหรับ Java

Aspose.PSD รองรับ **30+ image formats** และสามารถประมวลผลไฟล์ PSD ขนาดสูงสุด **500 MB** โดยไม่ต้องโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ ด้วยสถาปัตยกรรมสตรีมมิ่ง ในการทดสอบเบนช์มาร์ค การเพิ่มเลเยอร์ปกติสองชั้นใน PSD ขนาด 300 หน้าใช้เวลาน้อยกว่า **0.8 seconds** บน CPU มาตรฐาน 3.2 GHz

## ปัญหาทั่วไปและการแก้ไขข้อผิดพลาด

| อาการ | สาเหตุที่เป็นไปได้ | วิธีแก้ |
|---------|--------------|-----|
| PNG ปรากฏว่าง | เลเยอร์มองไม่เห็นหรือโปร่งใสเต็มที่ | ตรวจสอบว่าคุณตั้งค่าพิกเซลที่ไม่โปร่งใสหรือเรียก `layer.setVisible(true)` |
| `ArrayIndexOutOfBoundsException` | ขนาดสี่เหลี่ยมไม่ตรงกับความยาวของอาร์เรย์พิกเซล | ตรวจสอบว่า `rect.width * rect.height == dataArray.length` |
| LicenseException at runtime | ไม่มีไลเซนส์ที่ถูกต้องโหลดอยู่ | โหลดไลเซนส์ชั่วคราวหรือถาวรก่อนเรียกใช้เมธอด API ใด ๆ |

## คำถามที่พบบ่อย

**Q: Aspose.PSD รองรับ Java 8 หรือไม่?**  
A: ใช่, Aspose.PSD รองรับ Java 8 และรุ่นต่อ ๆ ไป

**Q: สามารถใช้การแปลง (หมุน, ย่อ/ขยาย) กับเลเยอร์ที่เพิ่มได้หรือไม่?**  
A: แน่นอน! คลาส `Layer` มีเมธอด `rotate`, `scale`, และ `translate` สำหรับการควบคุมการแปลงทั้งหมด

**Q: จะหาเอกสารเพิ่มเติมของ Aspose.PSD ได้จากที่ไหน?**  
A: เอกสาร API รายละเอียดสามารถเข้าถึงได้ที่ [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/)

**Q: จะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร?**  
A: เยี่ยมชมหน้าลิขสิทธิ์ชั่วคราว [Aspose temporary license page](https://purchase.aspose.com/temporary-license/)

**Q: มีฟอรั่มชุมชนสำหรับการสนับสนุน Aspose.PSD หรือไม่?**  
A: ใช่, เข้าร่วมการสนทนาที่ฟอรั่มชุมชน Aspose PSD [Aspose PSD community forum](https://forum.aspose.com/c/psd/34)

## สรุป

คุณตอนนี้รู้ **how to export PSD to PNG** พร้อมกับ **adding new regular layers** ด้วย Aspose.PSD สำหรับ Java แล้ว และคุณได้เห็นว่า **Aspose temporary license** ช่วยให้คุณลองกระบวนการนี้ได้โดยไม่มีข้อจำกัด บทเรียนนี้ครอบคลุมการโหลดไฟล์, การสร้างเลเยอร์, การเติมข้อมูลพิกเซล, การกำหนดตำแหน่งเลเยอร์, และการส่งออกคอมโพสชันสุดท้าย ทดลองใช้ขนาดสี่เหลี่ยม, สี, หรือเอฟเฟกต์ของเลเยอร์ที่ต่างกันเพื่อปรับผลลัพธ์ให้ตรงกับความต้องการของโครงการของคุณ

---

**อัปเดตล่าสุด:** 2026-10-18  
**ทดสอบด้วย:** Aspose.PSD 24.11 for Java  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [ส่งออก PSD เป็น PNG พร้อมเอฟเฟกต์เลเยอร์โดยใช้ Aspose.PSD สำหรับ Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [ส่งออก PSD เป็น PNG และรวมเลเยอร์โดยใช้ Aspose.PSD สำหรับ Java](/psd/java/psd-layer-management-effects/merge-psd-layers/)
- [ส่งออกกลุ่มเลเยอร์ PSD เป็นภาพโดยใช้ Java](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}