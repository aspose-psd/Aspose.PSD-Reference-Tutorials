---
date: 2026-07-17
description: บทแนะนำการประมวลผลภาพด้วย Java โดยใช้ Aspose.PSD เรียนรู้วิธีการใช้ตัวกรอง
  Gaussian และ Wiener อย่างเป็นขั้นตอนเพื่อผลลัพธ์ภาพที่น่าตื่นตาตื่นใจ
keywords:
- java image processing tutorial
- export png java
- gaussian filter java
- wiener filter java
lastmod: 2026-07-17
linktitle: ใช้ตัวกรอง Gaussian และ Wiener
og_description: บทแนะนำการประมวลผลภาพด้วย Java แสดงการใช้ตัวกรอง Gaussian และ Wiener
  ด้วย Aspose.PSD สำหรับ Java รวมถึงการส่งออกเป็น PNG และรูปแบบอื่น ๆ
og_image_alt: 'Developer guide: Apply Gaussian and Wiener filters to images in Java
  using Aspose.PSD'
og_title: บทแนะนำการประมวลผลภาพด้วย Java – ใช้ตัวกรอง Gaussian & Wiener
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Java image processing tutorial using Aspose.PSD learn how to apply
    Gaussian and Wiener filters step‑by‑step for stunning visual results.
  headline: Java Image Processing Tutorial – Apply Gaussian & Wiener Filters
  type: TechArticle
- questions:
  - answer: It smooths an image by averaging neighboring pixels, reducing high‑frequency
      noise.
    question: What does the Gaussian filter do?
  - answer: It performs adaptive smoothing, preserving edges while diminishing noise.
    question: What is the Wiener filter?
  - answer: Aspose.PSD for Java provides built‑in support for both filters.
    question: Which library is used?
  - answer: A trial works for testing, but a commercial license is required for production.
    question: Do I need a license?
  - answer: Yes—Aspose.PSD supports PNG, JPEG, BMP, and many more.
    question: Can I output formats other than GIF?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- Aspose.PSD
- gaussian filter
- wiener filter
- export png java
title: บทแนะนำการประมวลผลภาพด้วย Java – ใช้ตัวกรอง Gaussian & Wiener
url: /th/java/image-processing/apply-gaussian-wiener-filters/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บทแนะนำการประมวลผลภาพด้วย Java – ใช้ตัวกรอง Gaussian และ Wiener กับ Aspose.PSD

## บทนำ

ยินดีต้อนรับสู่ **java image processing tutorial** ของเรา ที่จะแสดงวิธีการใช้ตัวกรอง Gaussian และ Wiener ด้วย Aspose.PSD for Java ไม่ว่าคุณจะต้องการทำความสะอาดภาพที่มีสัญญาณรบกวนหรือเตรียมกราฟิกสำหรับการส่งบนเว็บ ตัวกรองเหล่านี้จะให้ผลลัพธ์ที่เรียบเนียนและดูเป็นมืออาชีพ ในไม่กี่นาทีต่อไปคุณจะได้เห็นขั้นตอนการทำงานเต็มรูปแบบ — ตั้งแต่การโหลดไฟล์ PSD ไปจนถึงการบันทึกผลลัพธ์ที่ผ่านการกรองเป็น GIF

## คำตอบอย่างรวดเร็ว
- **ตัวกรอง Gaussian ทำอะไร?** ตัวกรองนี้ทำให้ภาพเรียบเนียนโดยการเฉลี่ยพิกเซลใกล้เคียง ลดสัญญาณรบกวนความถี่สูง  
- **ตัวกรอง Wiener คืออะไร?** ตัวกรองนี้ทำการเรียบเนียนแบบปรับตัวได้ รักษาขอบภาพไว้ขณะลดสัญญาณรบกวน  
- **ใช้ไลบรารีอะไร?** Aspose.PSD for Java มีการสนับสนุนในตัวสำหรับทั้งสองตัวกรอง  
- **ต้องมีลิขสิทธิ์หรือไม่?** สามารถใช้รุ่นทดลองเพื่อทดสอบได้ แต่ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **สามารถส่งออกเป็นรูปแบบอื่นนอกจาก GIF ได้หรือไม่?** ได้ — Aspose.PSD รองรับ PNG, JPEG, BMP และรูปแบบอื่น ๆ อีกมากมาย

## Java Image Processing Tutorial คืออะไร?

Java image processing tutorial จะพัฒนาให้ผู้พัฒนาผ่านขั้นตอนสำคัญของการโหลดภาพ, การประยุกต์การแปลงเช่นการกรองหรือการปรับขนาด, และสุดท้ายการบันทึกผลลัพธ์ในรูปแบบที่ต้องการ โดยให้ตัวอย่างโค้ดและคำอธิบายที่ชัดเจน ช่วยให้คุณรวมความสามารถในการจัดการภาพเข้าไปในแอปพลิเคชัน Java ได้โดยตรง ลดความจำเป็นในการใช้เครื่องมือภายนอก

## ทำไมต้องใช้ตัวกรอง Gaussian และ Wiener?

โหลดภาพของคุณ, ใช้ตัวกรอง Gaussian‑Wiener ร่วมกัน, แล้วคุณจะเห็นการลดเม็ดสีอย่างชัดเจนในขณะที่ขอบสำคัญยังคงคมชัด — เหมาะสำหรับการเตรียมกราฟิกสำหรับเว็บหรือการสแกนเพื่อเก็บรักษา ส่วน Gaussian จะกำจัดสัญญาณรบกวนความถี่สูง, ส่วน Wiener จะปรับให้เข้ากับความแปรปรวนท้องถิ่น, รักษารายละเอียดที่สำคัญที่สุด

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม, โปรดตรวจสอบว่าคุณมี:

- สภาพแวดล้อมการพัฒนา Java (JDK 8 หรือใหม่กว่า)  
- ไลบรารี Aspose.PSD for Java คุณสามารถดาวน์โหลดได้ **[ที่นี่](https://releases.aspose.com/psd/java/)**  
- ความคุ้นเคยพื้นฐานกับไวยากรณ์ Java และแนวคิดเชิงวัตถุ

## นำเข้าแพ็กเกจ

คำสั่ง import จะนำคลาสของ Aspose.PSD เข้ามาในสโคป เพื่อให้คุณทำงานกับภาพ raster, ตัวเลือกการกรอง, และรูปแบบการส่งออกได้

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

การ import เหล่านี้ให้คุณเข้าถึงการโหลดภาพ, การจัดการ raster, ตัวเลือกการกรอง, และรูปแบบการส่งออก

## ขั้นตอนที่ 1: โหลดภาพ

คลาส `RasterImage` แทนภาพแบบ raster ที่สามารถประมวลผลพิกเซลต่อพิกเซลได้

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);
RasterImage rasterImage = (RasterImage)image;
```

เราจะโหลดไฟล์ PSD จากไดเรกทอรีที่ระบุและแคสต์เป็น `RasterImage` เพื่อให้สามารถทำงานกับข้อมูลพิกเซลได้

## ขั้นตอนที่ 2: ตรวจสอบ RasterImage

การตรวจสอบความปลอดภัยจะยืนยันว่าไฟล์ที่โหลดเป็นแบบ raster; หากไม่เป็นเช่นนั้น โปรแกรมจะออกอย่างเรียบร้อย

```java
if (rasterImage == null) {
    return;
}
```

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการกรอง

คลาส `GaussWienerFilterOptions` ให้คุณปรับแต่งพารามิเตอร์ของ Gaussian และ Wiener ในอ็อบเจกต์เดียว

```java
GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
options.setGrayscale(true);
```

- อาร์กิวเมนต์แรก (`12`) กำหนดขนาดรัศมีของ kernel Gaussian  
- อาร์กิวเมนต์ที่สอง (`3`) กำหนดค่าความเรียบที่ใช้โดยอัลกอริทึม Wiener  
- `setGrayscale(true)` บอกตัวกรองให้ทำงานในโหมดสีเทา ซึ่งมักให้ผลลัพธ์การลดสัญญาณรบกวนที่สะอาดกว่า

## ขั้นตอนที่ 4: ใช้ตัวกรองและบันทึก

เมธอด `filter` จะประยุกต์การผสม Gaussian‑Wiener ที่กำหนดไว้กับขอบเขตภาพทั้งหมด สุดท้ายเราจะบันทึกภาพที่ผ่านการประมวลผลเป็น GIF ด้วย `GifOptions` คุณสามารถเปลี่ยน `GifOptions` เป็น `PngOptions`, `JpegOptions` ฯลฯ เพื่อ **export PNG Java** หรือรูปแบบอื่น ๆ

```java
rasterImage.filter(image.getBounds(), options);
String destName = dataDir + "gauss_wiener_out.gif";
image.save(destName, new GifOptions());
```

## ปัญหาและเคล็ดลับทั่วไป

- **Null RasterImage:** ตรวจสอบให้แน่ใจว่าไฟล์ต้นทางเป็น PSD หรือรูปแบบที่รองรับ raster อื่น ๆ  
- **ประสิทธิภาพ:** ภาพขนาดใหญ่อาจใช้เวลานาน; พิจารณาลดรัศมีหรือประมวลผลสำเนาที่ลดขนาดลงก่อน  
- **สี vs. สีเทา:** หากต้องการคงสี, ตั้งค่า `options.setGrayscale(false)`

## คำถามที่พบบ่อย

**Q1: สามารถใช้ตัวกรองเหล่านี้กับภาพในรูปแบบอื่นนอกจาก PSD ได้หรือไม่?**  
A1: ได้, Aspose.PSD for Java รองรับรูปแบบภาพหลายรูปแบบนอกเหนือจาก PSD เช่น PNG, JPEG, BMP, และ GIF

**Q2: มีข้อจำกัดอะไรในรุ่นทดลองของ Aspose.PSD for Java หรือไม่?**  
A2: รุ่นทดลองจำกัดขนาดการส่งออกและเพิ่มลายน้ำ เพื่อเปิดใช้งานความสามารถเต็มรูปแบบต้องได้รับลิขสิทธิ์ที่ถูกต้อง

**Q3: จะขอรับการสนับสนุนสำหรับ Aspose.PSD for Java ได้อย่างไร?**  
A3: เยี่ยมชม **[Aspose.PSD Forum](https://forum.aspose.com/c/psd/34)** เพื่อรับความช่วยเหลือจากชุมชนและการตอบจากทีมอย่างเป็นทางการ

**Q4: มีลิขสิทธิ์ชั่วคราวสำหรับการทดสอบหรือไม่?**  
A4: มี, คุณสามารถรับลิขสิทธิ์ชั่วคราว **[ที่นี่](https://purchase.aspose.com/temporary-license/)**

**Q5: จะหาเอกสารรายละเอียดของ Aspose.PSD for Java ได้จากที่ไหน?**  
A5: ดู **[documentation](https://reference.aspose.com/psd/java/)** เพื่ออ้างอิง API อย่างละเอียดและตัวอย่างเพิ่มเติม

## สรุป

คุณได้ทำ **java image processing tutorial** ครบถ้วนที่แสดงวิธี **apply Gaussian** และ Wiener filters ด้วย Aspose.PSD for Java แล้ว ทดลองปรับค่ารัศมีและความเรียบ, สลับโหมดสีเทา, และลองรูปแบบการส่งออกอื่น ๆ เช่น PNG เพื่อดูว่าตัวกรองมีผลต่อภาพของคุณอย่างไร ขอให้สนุกกับการเขียนโค้ด!

---

**Last Updated:** 2026-07-17  
**Tested With:** Aspose.PSD for Java 23.12 (latest at time of writing)  
**Author:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [Step by Step Filter - Apply Motion Wiener Filters using Aspose.PSD for Java](/psd/java/image-processing/apply-motion-wiener-filters/)
- [Step by Step Filter - Apply Median & Wiener Filters (Java)](/psd/java/image-processing/apply-median-wiener-filters/)
- [How to Filter PNG Files in Aspose.PSD for Java](/psd/java/optimizing-png-files/apply-filters-png-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}