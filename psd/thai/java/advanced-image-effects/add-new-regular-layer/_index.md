---
date: 2026-04-08
description: เรียนรู้วิธีส่งออกไฟล์ PSD เป็น PNG และสร้างเลเยอร์ PSD ใหม่ด้วย Aspose.PSD
  สำหรับ Java โดยใช้ใบอนุญาตชั่วคราวของ Aspose บทเรียนทีละขั้นตอนนี้ครอบคลุมการจัดการภาพ
  PSD และการตั้งตำแหน่งเลเยอร์
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: เพิ่มเลเยอร์ปกติใหม่ใน PSD
second_title: Aspose.PSD Java API
title: ส่งออก PSD เป็น PNG และเพิ่มเลเยอร์ปกติใหม่โดยใช้ Aspose.PSD สำหรับ Java –
  ใบอนุญาตชั่วคราวของ Aspose
url: /th/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก PSD เป็น PNG และเพิ่มเลเยอร์ปกติใหม่โดยใช้ Aspose.PSD สำหรับ Java

## บทนำ

ใน **aspose psd tutorial** นี้คุณจะได้เรียนรู้วิธี **export PSD to PNG** พร้อมกับ **creating a new regular layer** ภายในไฟล์เดียวกันโดย **using an aspose temporary license** สำหรับการพัฒนา ไม่ว่าคุณจะต้องการสร้างภาพย่อพร้อมใช้งานบนเว็บ, เตรียมทรัพยากรสำหรับกระบวนการออกแบบ, หรือเพียงแค่ทดลอง **psd image manipulation** Aspose.PSD สำหรับ Java จะให้การควบคุมแบบโปรแกรมเต็มรูปแบบ เราจะเดินผ่านทุกขั้นตอน—from loading the source file to saving both the updated PSD and a PNG copy—เพื่อให้คุณเริ่มจัดการเลเยอร์ PSD ได้ทันที

## คำตอบอย่างรวดเร็ว
- **ฉันสามารถส่งออก PSD เป็น PNG ด้วยการเรียกหนึ่งครั้งได้หรือไม่?** ใช่, หลังจากเพิ่มเลเยอร์คุณสามารถเรียก `save` พร้อมกับ `PngOptions`.
- **ฉันต้องการใบอนุญาตสำหรับการพัฒนาหรือไม่?** ใบอนุญาตชั่วคราวทำงานสำหรับการทดสอบ; ใบอนุญาตเต็มจำเป็นสำหรับการใช้งานจริง.
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Aspose.PSD ทำงานกับ Java 8 และใหม่กว่า.
- **การกำหนดตำแหน่งเลเยอร์เป็นแบบพิกเซลหรือไม่?** ใช่, คุณตั้งค่าพิกัด left, top, right, bottom เป็นพิกเซลโดยใช้วิธี **set layer position**.
- **PNG จะคงความโปร่งใสของเลเยอร์หรือไม่?** PNG จะมีผลลัพธ์ที่ผสานของทุกเลเยอร์ที่มองเห็น.

## ทำไมต้องใช้ใบอนุญาตชั่วคราวของ aspose?

**aspose temporary license** ช่วยให้คุณประเมินคุณสมบัติเต็มของ Aspose.PSD โดยไม่มีข้อจำกัดการทำงาน มันลบลายน้ำการประเมิน, ปลดล็อก API ทั้งหมด—including ความสามารถในการ **create new psd layer** objects—และให้คุณทดสอบโค้ดในสภาพแวดล้อมคล้ายการผลิตก่อนซื้อใบอนุญาตถาวร

## ข้อกำหนดเบื้องต้น

ก่อนเริ่ม, ตรวจสอบว่าคุณมี:

- **Java Development Environment** – JDK 8+ และเครื่องมือสร้าง (Maven/Gradle) ที่ติดตั้งแล้ว
- **Aspose.PSD for Java** – ดาวน์โหลด JAR ล่าสุดจากเว็บไซต์ทางการ [here](https://releases.aspose.com/psd/java/)
- **A sample PSD file** – เราจะใช้ไฟล์ `OneLayer.psd` ในตัวอย่าง

## นำเข้าชุดแพ็กเกจ

เพิ่มการนำเข้าที่จำเป็นในคลาส Java ของคุณ คลาสเหล่านี้ให้ฟังก์ชันหลักสำหรับ **psd image manipulation** และการจัดการเลเยอร์

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## อะไรคือ “set layer position” และทำไมจึงสำคัญ?

เมื่อคุณเพิ่มเลเยอร์ใหม่, คุณต้องกำหนดตำแหน่งที่มันปรากฏบนแคนวาส วิธี `setLeft`, `setTop`, `setRight`, และ `setBottom` **set layer position** ในพิกัดพิกเซล การกำหนดตำแหน่งที่ถูกต้องทำให้กราฟิกของคุณจัดเรียงตรงตามที่คาดหวัง ซึ่งสำคัญสำหรับการคอมโพสท์ UI หรือการเตรียมไฟล์พร้อมพิมพ์

## คู่มือทีละขั้นตอน

### ขั้นตอนที่ 1: โหลดไฟล์ PSD

เริ่มต้นโดยโหลดไฟล์ PSD ที่มีอยู่ที่คุณต้องการแก้ไข ซึ่งจะให้คุณได้อ็อบเจ็กต์ `PsdImage` ที่สามารถทำงานได้

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### ขั้นตอนที่ 2: เตรียมข้อมูลพิกเซลและสี่เหลี่ยม

เราจะสร้างบัฟเฟอร์พิกเซลสองชุด (`int[]`) และกำหนดพื้นที่สี่เหลี่ยมที่เลเยอร์ใหม่จะถูกวาด นี่เป็นพื้นฐานสำหรับ **creating a new psd layer**

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### ขั้นตอนที่ 3: เริ่มต้นข้อมูลเลเยอร์

เติมบัฟเฟอร์พิกเซลด้วยค่า ARGB เริ่มต้น ค่า `-10000000` แทนสีเข้มกึ่งโปร่งใส

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### ขั้นตอนที่ 4: เพิ่มเลเยอร์ปกติ (จัดการเลเยอร์ PSD)

ตอนนี้เราจะ **add regular layers** ไปยังภาพ PSD และ **set layer position** ด้วยคุณสมบัติ left, top, right, bottom ซึ่งแสดงให้เห็นวิธี **manipulate PSD layers** ด้วยโปรแกรม

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

หลังจากเลเยอร์ถูกวางไว้แล้ว, บันทึกเอกสารที่แก้ไข เราจะส่งออกผลลัพธ์เป็น PNG (ขั้นตอน **export psd to png**) แล้วบันทึก PSD พร้อมเลเยอร์ใหม่

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **เคล็ดลับ:** หากคุณต้องการเพียง PNG เท่านั้น, คุณสามารถข้ามการเรียก `save` ของ PSD และเรียก `save` โดยตรงด้วย `PngOptions`.

## ปัญหาทั่วไปและการแก้ไขปัญหา

| อาการ | สาเหตุที่เป็นไปได้ | วิธีแก้ |
|---------|--------------|-----|
| PNG ปรากฏเป็นสีขาว | เลเยอร์ไม่มองเห็นหรือโปร่งใสเต็มที่ | ตรวจสอบให้แน่ใจว่าคุณตั้งค่าพิกเซลที่ไม่โปร่งใสหรือเรียก `layer.setVisible(true)` |
| `ArrayIndexOutOfBoundsException` | ขนาดสี่เหลี่ยมไม่ตรงกับความยาวอาร์เรย์พิกเซล | ตรวจสอบว่า `rect.width * rect.height == dataArray.length` |
| LicenseException ที่ runtime | ไม่มีใบอนุญาตที่ถูกต้องโหลด | โหลดใบอนุญาตชั่วคราวหรือถาวรก่อนเรียกใช้เมธอด API ใด ๆ |

## คำถามที่พบบ่อย

**Q: Aspose.PSD รองรับ Java 8 หรือไม่?**  
A: ใช่, Aspose.PSD รองรับ Java 8 และเวอร์ชันต่อมา

**Q: ฉันสามารถใช้การแปลง (หมุน, ย่อ/ขยาย) กับเลเยอร์ที่เพิ่มได้หรือไม่?**  
A: แน่นอน! คลาส `Layer` มีเมธอดเช่น `rotate`, `scale`, และ `translate` สำหรับการควบคุมการแปลงเต็มรูปแบบ

**Q: ฉันจะหาเอกสารเพิ่มเติมของ Aspose.PSD ได้จากที่ไหน?**  
A: เอกสาร API รายละเอียดมีให้ [here](https://reference.aspose.com/psd/java/)

**Q: ฉันจะขอใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร?**  
A: เยี่ยมชมหน้าลิขสิทธิ์ชั่วคราว [here](https://purchase.aspose.com/temporary-license/)

**Q: มีฟอรั่มชุมชนสำหรับการสนับสนุน Aspose.PSD หรือไม่?**  
A: มี, เข้าร่วมการสนทนาที่ฟอรั่ม Aspose [here](https://forum.aspose.com/c/psd/34)

## สรุป

คุณได้เรียนรู้วิธี **export PSD to PNG** พร้อมกับ **adding new regular layers** โดยใช้ Aspose.PSD สำหรับ Java และเห็นว่า **aspose temporary license** ช่วยให้คุณลองเวิร์กโฟลว์นี้ได้โดยไม่มีข้อจำกัด บทเรียนนี้แสดงความสามารถหลักของ **psd image manipulation**: โหลดไฟล์, สร้างเลเยอร์, เติมข้อมูลพิกเซล, และส่งออกคอมโพสชันสุดท้าย อย่าลังเลที่จะทดลองขนาดสี่เหลี่ยม, สีพิกเซล, หรือเอฟเฟกต์เลเยอร์ต่าง ๆ เพื่อให้ผลลัพธ์ตรงกับความต้องการของโครงการของคุณ

---

**Last Updated:** 2026-04-08  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}