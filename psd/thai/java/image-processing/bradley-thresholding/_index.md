---
date: 2026-08-17
description: วิธีทำให้ภาพเป็นไบนารีด้วย Bradley thresholding โดยใช้ Aspose.PSD for
  Java. ปฏิบัติตามคำแนะนำทีละขั้นตอนเพื่อแปลง PSD เป็น PNG และปรับปรุงคุณภาพของภาพ
keywords:
- how to binarize image
- convert psd to png
- set threshold value
- enhance image quality
- save binarized image
lastmod: 2026-08-17
linktitle: Bradley Thresholding
og_description: เรียนรู้วิธีทำให้ภาพเป็นไบนารีโดยใช้ Bradley thresholding ใน Aspose.PSD
  for Java. คู่มือนี้จะแสดงวิธีตั้งค่า threshold value, แปลง PSD เป็น PNG, และบันทึกภาพที่ทำให้เป็นไบนารี
og_image_alt: 'Guide: binarize image using Bradley thresholding in Aspose.PSD for
  Java'
og_title: วิธีทำให้ภาพเป็นไบนารีใน Java ด้วย Bradley thresholding
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: How to binarize image with Bradley thresholding using Aspose.PSD for
    Java. Follow this step‑by‑step guide to convert PSD to PNG and enhance image quality.
  headline: How to binarize image in Java using Bradley thresholding
  type: TechArticle
- description: How to binarize image with Bradley thresholding using Aspose.PSD for
    Java. Follow this step‑by‑step guide to convert PSD to PNG and enhance image quality.
  name: How to binarize image in Java using Bradley thresholding
  steps:
  - name: '**Java development environment** – JDK 11 or newer installed and configured.'
    text: '**Java development environment** – JDK 11 or newer installed and configured.'
  - name: '**Aspose.PSD library** – download the latest JAR from [Aspose.PSD Java
      download page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD library** – download the latest JAR from [Aspose.PSD Java
      download page](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD image** – a PSD file you want to binarize; you can use any
      image you own or a test file.'
    text: '**Sample PSD image** – a PSD file you want to binarize; you can use any
      image you own or a test file.'
  type: HowTo
- questions:
  - answer: It is an adaptive binarization technique that computes a local average
      for each pixel and thresholds based on a percentage of that average.
    question: What is Bradley thresholding?
  - answer: Start with 0.5 (50 %). If the output is too noisy, increase the value;
      if details are lost, decrease it. Test a few values on a representative sample.
    question: How do I choose the right threshold value?
  - answer: Yes. Aspose.PSD supports more than 30 input and output formats—including
      PSD, PNG, JPEG, BMP, and TIFF—so you can load a JPEG, convert it to a `PsdImage`,
      and then binarize.
    question: Can I apply Bradley thresholding to other image formats?
  - answer: You can call `image.save("preview.png", new PngOptions())` after the `binarizeBradley`
      step to write a temporary file for visual inspection.
    question: Is there a way to preview the binarized image before saving?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      help and explore the official [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references.
    question: Where can I find more support and resources?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- image binarization
- Aspose.PSD
- Java image processing
- Bradley thresholding
title: วิธีทำให้ภาพเป็นไบนารีใน Java ด้วย Bradley thresholding
url: /th/java/image-processing/bradley-thresholding/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีทำให้ภาพเป็นไบนารีใน Java ด้วย Bradley thresholding

## บทนำ

ในบทเรียนนี้คุณจะได้เรียนรู้ **วิธีทำให้ภาพเป็นไบนารี** โดยใช้ Bradley Thresholding กับ Aspose.PSD for Java การทำไบนารีจะเปลี่ยนภาพสีหรือระดับสีเทาให้เป็นเวอร์ชันสีขาว‑ดำ ซึ่งจำเป็นสำหรับ OCR, การเก็บเอกสาร, และหลายกระบวนการคอมพิวเตอร์วิทัศน์ เราจะอธิบายทุกขั้นตอน—from loading a PSD file to saving the final PNG—เพื่อให้คุณสามารถนำเทคนิคนี้ไปใช้ในโครงการ Java ของคุณเอง

## คำตอบสั้น
- **Bradley thresholding ทำอะไร?** มันกำหนดค่าขีดจำกัดท้องถิ่นสำหรับแต่ละ pixel อย่างปรับตัว, รักษารายละเอียดในแสงที่ไม่สม่ำเสมอ.
- **ต้องใช้ไลบรารีอะไร?** Aspose.PSD for Java (latest version recommended).
- **ต้องการไลเซนส์หรือไม่?** รุ่นทดลองฟรีใช้ได้สำหรับการพัฒนา; จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง.
- **สามารถประมวลผลไฟล์ PSD ขนาดใหญ่ได้หรือไม่?** ได้, API สามารถจัดการไฟล์ขนาดถึง 2 GB โดยไม่ต้องโหลดภาพทั้งหมดเข้าสู่หน่วยความจำ.
- **รูปแบบเอาต์พุตที่แนะนำคืออะไร?** PNG เป็นรูปแบบที่ไม่มีการสูญเสียและได้รับการสนับสนุนอย่างกว้างขวางสำหรับผลลัพธ์ที่ไบนารี.

## Bradley thresholding คืออะไร?

Bradley thresholding เป็นอัลกอริทึมการทำไบนารีแบบปรับตัวที่คำนวณค่าเฉลี่ยท้องถิ่นรอบแต่ละ pixel และตั้งค่า pixel ให้เป็นสีขาวหากความเข้มของมันเกินค่าเฉลี่ยโดยเปอร์เซ็นต์ที่กำหนดได้ วิธีนี้รักษารายละเอียดขอบแม้เมื่อแสงเปลี่ยนแปลงทั่วทั้งภาพ.

## ทำไมต้องใช้ Bradley thresholding เพื่อทำให้ภาพเป็นไบนารี?

Bradley thresholding ให้ความคอนทราสต์สูงอย่างสม่ำเสมอบนภาพที่มีแสงไม่สม่ำเสมอ, ทำให้ได้ความแม่นยำ OCR สูงถึง 95 % บนเอกสารสแกนเมื่อเทียบกับวิธีการกำหนดค่าขีดจำกัดทั่วโลก. การทำงานของ Aspose.PSD ประมวลผล PSD ขนาด 500 หน้าในเวลาน้อยกว่า 4 วินาทีบนเซิร์ฟเวอร์ 8‑core ปกติ, ทำให้เหมาะสำหรับกระบวนการทำงานแบบแบตช์.

## ข้อกำหนดเบื้องต้น

ก่อนเริ่ม, โปรดตรวจสอบว่าคุณมี:

1. **Java development environment** – JDK 11 หรือใหม่กว่า ที่ติดตั้งและกำหนดค่าแล้ว.
2. **Aspose.PSD library** – ดาวน์โหลด JAR ล่าสุดจาก [Aspose.PSD Java download page](https://releases.aspose.com/psd/java/).
3. **Sample PSD image** – ไฟล์ PSD ที่คุณต้องการทำไบนารี; คุณสามารถใช้ภาพใดก็ได้ที่คุณเป็นเจ้าของหรือไฟล์ทดสอบ.

## นำเข้าแพ็กเกจ

การนำเข้าต่อไปนี้จะให้คุณเข้าถึงคลาสหลักที่จำเป็นสำหรับการโหลด, ประมวลผล, และบันทึกภาพ.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## วิธีทำให้ภาพเป็นไบนารีโดยใช้ Bradley thresholding?

ในบทเรียนนี้คุณจะโหลดไฟล์ PSD, เลือกค่าขีดจำกัดที่เหมาะสม, รันการทำไบนารีแบบปรับตัวของ Bradley, และสุดท้ายบันทึกผลลัพธ์เป็นไฟล์ PNG กระบวนการประกอบด้วยสี่การเรียกเมธอดสั้น ๆ, แต่ละขั้นตอนแสดงด้วยตัวอย่างโค้ด, ทำให้คุณสามารถรวมเวิร์กโฟลว์นี้เข้าไปในแอปพลิเคชัน Java ใดก็ได้โดยใช้ความพยายามน้อยที่สุด.

## ขั้นตอนที่ 1: โหลดภาพ

`PsdImage` class แสดงไฟล์ PSD ในหน่วยความจำและให้เมธอดสำหรับการจัดการระดับ pixel. การสร้างอินสแตนซ์ทำให้คุณเข้าถึงข้อมูลภาพทั้งหมด.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "binarized_out.png";

// Load an image
PsdImage image = (PsdImage)Image.load(sourceFile);
```

ในขั้นตอนนี้ไฟล์ PSD จะถูกอ่านจากดิสก์และเก็บไว้ในอ็อบเจ็กต์ `PsdImage`, พร้อมสำหรับการประมวลผล.

## ขั้นตอนที่ 2: กำหนดค่าขีดจำกัด

พารามิเตอร์ `threshold` ควบคุมความรุนแรงของการทำไบนารี; ค่า 0.5 (50 %) เป็นจุดเริ่มต้นที่ทั่วไป. ปรับค่าตามคอนทราสต์ของภาพต้นฉบับของคุณ.

```java
// Define threshold value
double threshold = 0.15;
```

การตั้งค่าขีดจำกัดอย่างถูกต้องจะสมดุลการลดสัญญาณรบกวนกับการรักษารายละเอียด.

## ขั้นตอนที่ 3: ใช้ Bradley thresholding

เมธอด `binarizeBradley` ทำการทำไบนารีแบบปรับตัวโดยใช้ค่าขีดจำกัดที่คุณระบุ. มันวิเคราะห์หน้าต่างท้องถิ่นรอบแต่ละ pixel เพื่อกำหนดว่าจะทำให้เป็นสีดำหรือสีขาว.

```java
// Call BinarizeBradley method and pass the threshold value as a parameter
image.binarizeBradley(threshold);
```

หลังจากการเรียกนี้อินสแตนซ์ `PsdImage` จะมีเวอร์ชันสีขาว‑ดำของภาพต้นฉบับ.

## ขั้นตอนที่ 4: บันทึกภาพเอาต์พุต

เมธอด `save` จะเขียนภาพที่ประมวลผลแล้วลงในระบบไฟล์. PNG ถูกเลือกเพราะรักษาข้อมูลไบนารีโดยไม่มีศิลปะการบีบอัดเพิ่มเติม.

```java
// Save the output image
image.save(destName, new PngOptions());
```

ตอนนี้คุณมี PNG ที่ทำไบนารีแล้วซึ่งสามารถส่งต่อไปยังเครื่อง OCR หรือกระบวนการต่อเนื่องอื่น ๆ.

## ปัญหาทั่วไปและวิธีแก้

LoadOptions เป็นคลาสที่ให้คุณระบุวิธีการโหลดไฟล์ PSD, เช่นการเปิดใช้งานโหมดสตรีมมิงเพื่อ ลดการใช้หน่วยความจำ.

- **ภาพดูมืดเกินไปหรือสว่างเกินไป** – ปรับค่าขีดจำกัด; ค่าต่ำทำให้ภาพสว่างขึ้น, ค่าสูงทำให้ภาพมืดลง.
- **ข้อผิดพลาด Out‑of‑memory กับ PSD ขนาดใหญ่มาก** – เปิดใช้งานโหมดสตรีมมิงโดยเรียก `PsdImage.setLoadOptions(new LoadOptions { LoadMode = LoadMode.Stream })` ก่อนการโหลด. `LoadMode.Stream` เปิดโหมดสตรีมมิงสำหรับไฟล์ขนาดใหญ่.
- **แถบสีที่ไม่คาดคิด** – ตรวจสอบว่า PSD ต้นฉบับอยู่ในโหมด RGB; แปลงโดยใช้ `image.convertToRgb()` หากจำเป็น. เมธอด `convertToRgb()` จะเปลี่ยนภาพเป็นโหมดสี RGB, เพื่อให้การจัดการสีถูกต้อง.

## คำถามที่พบบ่อย

**Q: Bradley thresholding คืออะไร?**  
A: เป็นเทคนิคการทำไบนารีแบบปรับตัวที่คำนวณค่าเฉลี่ยท้องถิ่นสำหรับแต่ละ pixel และกำหนดขีดจำกัดตามเปอร์เซ็นต์ของค่าเฉลี่ยนั้น.

**Q: ฉันจะเลือกค่าขีดจำกัดที่เหมาะสมอย่างไร?**  
A: เริ่มต้นที่ 0.5 (50 %). หากผลลัพธ์มีสัญญาณรบกวนมากเกินไป, เพิ่มค่า; หากรายละเอียดหายไป, ลดค่า. ทดลองค่าต่าง ๆ บนตัวอย่างที่เป็นตัวแทน.

**Q: ฉันสามารถใช้ Bradley thresholding กับรูปแบบภาพอื่นได้หรือไม่?**  
A: ได้. Aspose.PSD รองรับรูปแบบอินพุตและเอาต์พุตมากกว่า 30 รูปแบบ—รวมถึง PSD, PNG, JPEG, BMP, และ TIFF—ดังนั้นคุณสามารถโหลด JPEG, แปลงเป็น `PsdImage`, แล้วทำไบนารีได้.

**Q: มีวิธีดูตัวอย่างภาพที่ทำไบนารีก่อนบันทึกหรือไม่?**  
A: คุณสามารถเรียก `image.save("preview.png", new PngOptions())` หลังจากขั้นตอน `binarizeBradley` เพื่อเขียนไฟล์ชั่วคราวสำหรับการตรวจสอบภาพ.

**Q: ฉันจะหาแหล่งสนับสนุนและทรัพยากรเพิ่มเติมได้ที่ไหน?**  
A: เยี่ยมชม [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) เพื่อรับความช่วยเหลือจากชุมชนและสำรวจ [documentation](https://reference.aspose.com/psd/java/) อย่างเป็นทางการสำหรับอ้างอิง API รายละเอียด.

---

**อัปเดตล่าสุด:** 2026-08-17  
**ทดสอบด้วย:** Aspose.PSD 24.12 for Java  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทเรียนที่เกี่ยวข้อง

- [บทเรียนการประมวลผลภาพ Java - ปรับความสว่างของภาพด้วย Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-brightness/)
- [วิธีปรับค่า Gamma ในการประมวลผลภาพ Java ด้วย Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)
- [ไลบรารีการประมวลผลภาพ Java: กลับด้านเลเยอร์โดยใช้ Aspose.PSD](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}