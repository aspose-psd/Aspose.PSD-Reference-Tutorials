---
date: 2026-05-19
description: เรียนรู้วิธีการหมุนภาพตามมุมที่กำหนดใน Java ด้วย Aspose.PSD คู่มือนี้ครอบคลุม
  rotate image java, rotate image specific angle, การจัดการพื้นหลัง และอื่น ๆ
keywords:
- how to rotate image
- rotate image specific angle
- rotate image java
- rotate image background
- rotate image degrees
linktitle: วิธีการหมุนภาพตามมุมที่กำหนด
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to rotate image on a specific angle in Java using Aspose.PSD.
    The guide covers rotate image java, rotate image specific angle, background handling
    and more.
  headline: How to Rotate Image on a Specific Angle with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to rotate image on a specific angle in Java using Aspose.PSD.
    The guide covers rotate image java, rotate image specific angle, background handling
    and more.
  name: How to Rotate Image on a Specific Angle with Aspose.PSD for Java
  steps:
  - name: Define Your Document Directory
    text: Set the folder that holds the source PSD and where the output will be written.
      Using an absolute path or `System.getProperty("user.dir")` eliminates relative‑path
      surprises.
  - name: Specify Source and Destination File Paths
    text: Provide the full file names for the input PSD and the desired output format
      (e.g., PNG, JPEG, TIFF). Changing the extension in `destName` automatically
      selects the appropriate encoder.
  - name: Load the Image
    text: The `Image.load` method detects the file format and returns a concrete `RasterImage`
      instance ready for raster operations. The `Image` class is a factory that reads
      a file from disk and creates an in‑memory representation suitable for further
      processing. It supports automatic format detection for al
  - name: Cache Image Data (Optional but Recommended)
    text: Calling `image.cacheData()` stores pixel data in memory, dramatically speeding
      up subsequent transformations—especially for large PSD files that would otherwise
      trigger repeated disk I/O. The `cacheData()` method forces the image to be fully
      loaded into RAM, reducing the overhead of lazy loading dur
  - name: Rotate the Image
    text: 'Invoke `rotate` with three arguments: the rotation angle (float), a flag
      to expand the canvas, and the background color for the newly exposed corners.
      The `rotate` method rotates the image around its centre, optionally enlarging
      the canvas to accommodate the rotated bounds. The background `Color` fi'
  - name: Save the Result
    text: Choose an encoder (JPEG, PNG, etc.) and call `save`. `JpegOptions` lets
      you adjust quality, while `PngOptions` provides lossless output. The `save`
      method writes the transformed image to disk using the specified options object,
      ensuring that compression level and color depth are preserved as require
  type: HowTo
- questions:
  - answer: Yes. The library preserves alpha channels; omit an opaque background color
      to keep corners transparent.
    question: Can I rotate images with transparency using Aspose.PSD for Java?
  - answer: No. Aspose.PSD supports PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF,
      EMF, and 30+ additional formats.
    question: Are there any limitations on the image file formats supported for rotation?
  - answer: Absolutely. Pass a negative float to `rotate` (e.g., `-30f`) to rotate
      clockwise.
    question: Can I rotate images by a negative angle?
  - answer: The API is server‑side only. For live previews, render the rotated bitmap
      in a UI framework such as Swing or JavaFX and refresh the view.
    question: Does Aspose.PSD provide real‑time image preview during rotation?
  - answer: Yes, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) to
      ask questions and share experiences.
    question: Is there a community forum for Aspose.PSD where I can seek help?
  type: FAQPage
second_title: Aspose.PSD Java API
title: วิธีการหมุนภาพตามมุมที่กำหนดด้วย Aspose.PSD สำหรับ Java
url: /th/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีหมุนรูปภาพด้วยมุมเฉพาะด้วย Aspose.PSD for Java

หากคุณต้องการ **วิธีหมุนรูปภาพ** อย่างโปรแกรมในแอปพลิเคชัน Java, Aspose.PSD for Java มี API ที่สะอาดและมีประสิทธิภาพสูงซึ่งดูแลการทำงานหนักให้คุณ ไม่ว่าคุณจะกำลังสร้างโปรแกรมแก้ไขรูปภาพ, สร้างภาพย่อ, หรือเตรียมทรัพยากรสำหรับเว็บเซอร์วิส, การหมุนรูปภาพด้วยมุมที่แน่นอนเป็นความต้องการทั่วไป ในบทแนะนำนี้เราจะพาคุณผ่านกระบวนการทั้งหมด—ตั้งแต่การโหลดไฟล์ PSD จนถึงการบันทึกผลลัพธ์ที่หมุนแล้ว—พร้อมเน้นแนวปฏิบัติที่ดีที่สุด เช่น การแคชและการจัดการพื้นหลัง

## คำตอบสั้น ๆ
- **ห้องสมุดใดดีที่สุดสำหรับการหมุนรูปภาพใน Java?** Aspose.PSD for Java ให้เครื่องยนต์การหมุนที่เชื่อถือได้ที่สุด  
- **ฉันสามารถหมุนได้ทุกมุมหรือไม่?** ได้, เมธอด `rotate` รับค่า `float` เป็นมุม ไม่ว่าจะเป็นบวกหรือลบ  
- **ต้องใช้ไลเซนส์สำหรับการพัฒนาหรือไม่?** เวอร์ชันทดลองฟรีใช้สำหรับการทดสอบ; ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **รูปแบบไฟล์ภาพที่รองรับมีอะไรบ้าง?** PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF, และรูปแบบเพิ่มเติมกว่า 30 รูปแบบ  
- **จะตั้งค่าสีพื้นหลังสำหรับพื้นที่ว่างอย่างไร?** ส่งอ็อบเจ็กต์ `Color` ไปยังเมธอด `rotate`

## วิธีหมุนรูปภาพด้วยมุมเฉพาะด้วย Aspose.PSD for Java?

โหลดไฟล์ต้นฉบับ, เรียก `image.rotate(angle, true, backgroundColor)`, แล้วบันทึก—สามขั้นตอนสั้น ๆ ที่จัดการคณิตศาสตร์ที่ซับซ้อนให้คุณ Aspose.PSD รักษาชั้น, โปรไฟล์สี, และแชนแนลอัลฟาไว้พร้อมขยายขนาดแคนวาสเพื่อหลีกเลี่ยงการคลิป, ดังนั้นผลลัพธ์จะตรงตามที่คาดแม้สำหรับมุมเศษส่วนเช่น 12.5° วิธีนี้ทำงานได้กับไฟล์ตั้งแต่หลายกิโลไบต์จนถึง PSD หลายร้อยหน้าโดยไม่ทำให้หน่วยความจำหมด

## การหมุนภาพใน Java คืออะไร?

การหมุนภาพคือการแปลงเชิงเรขาคณิตที่หมุนเมทริกซ์พิกเซลรอบจุดศูนย์กลาง—โดยทั่วไปคือศูนย์กลางของภาพ—ตามมุมที่กำหนด ใน Java ธรรมดาคุณจะต้องจัดการกับอ็อบเจ็กต์ `Graphics2D`, คำนวณค่าไตรโกณมิติ, และจัดการพื้นหลังด้วยตนเอง Aspose.PSD แยกความซับซ้อนเหล่านี้ออก, จัดการความลึกสี, มาสก์ของชั้น, และรูปแบบไฟล์ต่าง ๆ โดยอัตโนมัติ

## ทำไมต้องใช้ Aspose.PSD สำหรับการหมุนภาพ?

Aspose.PSD รองรับ **รูปแบบเข้าและออกกว่า 30 รูปแบบ** และสามารถประมวลผล **ไฟล์ PSD ขนาด 500 หน้าในเวลาน้อยกว่า 5 วินาที** บนเซิร์ฟเวอร์คลาสทั่วไป ไลบรารีมีระบบแคชในตัว (`image.cacheData()`) ลดการใช้หน่วยความจำได้ถึง 60 % สำหรับทรัพยากรขนาดใหญ่, และเมธอด `rotate` ให้คุณระบุสีพื้นหลัง, รักษามุมโปร่งใสเมื่อจำเป็น ประโยชน์เชิงปริมาณเหล่านี้ทำให้เป็นตัวเลือกมาตรฐานอุตสาหกรรมสำหรับไพพ์ไลน์ภาพที่ต้องการประสิทธิภาพสูง

## ข้อกำหนดเบื้องต้น

ก่อนเริ่ม, โปรดตรวจสอบว่าคุณมี:

1. **Java Development Kit (JDK 8 หรือใหม่กว่า)** – IDE หรือสภาพแวดล้อมบรรทัดคำสั่งใดก็ได้  
2. **Aspose.PSD for Java** – ดาวน์โหลด JAR ล่าสุดจาก [หน้า Aspose.PSD Java](https://reference.aspose.com/psd/java/)  
3. **ไฟล์ PSD ตัวอย่าง** – เช่น `sample.psd` ที่วางไว้ในโฟลเดอร์ที่คุณสามารถอ้างอิงจากโค้ดได้

## นำเข้าแพ็กเกจ

คลาส `RasterImage` และยูทิลิตี้ที่เกี่ยวข้องเป็นหัวใจของเวิร์กโฟลว์การหมุน

คลาส `RasterImage` เป็นอ็อบเจ็กต์หลักของ Aspose.PSD สำหรับการจัดการภาพแบบแรสเตอร์ มันให้เมธอดสำหรับโหลด, แปลง, และบันทึกภาพแรสเตอร์พร้อมคงเมตาดาต้าไว้

## คู่มือขั้นตอนโดยละเอียด

### ขั้นตอนที่ 1: กำหนดไดเรกทอรีเอกสารของคุณ

ตั้งค่าโฟลเดอร์ที่เก็บ PSD ต้นฉบับและที่ที่ผลลัพธ์จะถูกเขียนออกไป การใช้พาธแบบเต็มหรือ `System.getProperty("user.dir")` จะช่วยหลีกเลี่ยงปัญหาเกี่ยวกับพาธสัมพัทธ์

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### ขั้นตอนที่ 2: ระบุพาธไฟล์ต้นทางและปลายทาง

ให้ชื่อไฟล์เต็มสำหรับ PSD อินพุตและรูปแบบผลลัพธ์ที่ต้องการ (เช่น PNG, JPEG, TIFF) การเปลี่ยนส่วนขยายใน `destName` จะเลือกตัวเข้ารหัสที่เหมาะสมโดยอัตโนมัติ

```java
String dataDir = "Your Document Directory";
```

### ขั้นตอนที่ 3: โหลดภาพ

เมธอด `Image.load` ตรวจจับรูปแบบไฟล์และคืนค่าอินสแตนซ์ `RasterImage` ที่พร้อมสำหรับการทำงานแรสเตอร์

คลาส `Image` เป็นฟactory ที่อ่านไฟล์จากดิสก์และสร้างการแสดงผลในหน่วยความจำที่เหมาะสำหรับการประมวลผลต่อไป มันรองรับการตรวจจับรูปแบบอัตโนมัติสำหรับรูปแบบที่สนับสนุนทั้งหมดกว่า 30 รูปแบบ

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

### ขั้นตอนที่ 4: แคชข้อมูลภาพ (ไม่บังคับแต่แนะนำ)

การเรียก `image.cacheData()` จะเก็บข้อมูลพิกเซลในหน่วยความจำ, เร่งความเร็วการแปลงต่อเนื่องอย่างมาก—โดยเฉพาะสำหรับไฟล์ PSD ขนาดใหญ่ที่หากไม่ทำอาจทำให้ต้องอ่านจากดิสก์หลายครั้ง

เมธอด `cacheData()` บังคับให้ภาพโหลดเต็มที่เข้าสู่ RAM, ลดค่าโอเวอร์เฮดของการโหลดแบบ lazy ระหว่างการทำงานหนัก

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

### ขั้นตอนที่ 5: หมุนภาพ

เรียก `rotate` พร้อมอาร์กิวเมนต์สามค่า: มุมการหมุน (float), ธงขยายแคนวาส, และสีพื้นหลังสำหรับมุมที่เปิดเผยใหม่

เมธอด `rotate` หมุนภาพรอบศูนย์กลาง, สามารถขยายแคนวาสเพื่อรองรับขอบเขตที่หมุนได้ สี `Color` จะเติมพื้นที่ว่าง, ป้องกันมุมโปร่งใสหรือสีดำ

- **20f** – มุมการหมุนเป็นองศา (float). เปลี่ยนค่าได้ตามต้องการ, เช่น `-45f` สำหรับการหมุนตามเข็มนาฬิกา  
- **true** – รักษาอัตราส่วนเดิมขณะขยายแคนวาส  
- **Color.getRed()** – สีพื้นหลังที่เติมมุมว่าง; สามารถเปลี่ยนเป็น `Color.getWhite()` หรือสีกำหนดเองอื่น ๆ ได้

```java
if (!image.isCached())
{
    image.cacheData();
}
```

### ขั้นตอนที่ 6: บันทึกผลลัพธ์

เลือกตัวเข้ารหัส (JPEG, PNG, ฯลฯ) แล้วเรียก `save`. `JpegOptions` ให้คุณปรับคุณภาพ, ส่วน `PngOptions` ให้ผลลัพธ์แบบไม่มีการสูญเสีย

เมธอด `save` เขียนภาพที่แปลงแล้วลงดิสก์โดยใช้วัตถุตัวเลือกที่ระบุ, ทำให้ระดับการบีบอัดและความลึกสีคงที่ตามที่ต้องการ

```java
image.rotate(20f, true, Color.getRed());
```

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|-----|
| **มุมสีขาวหลังการหมุน** | ไม่ได้ระบุสีพื้นหลัง | ส่ง `Color` (เช่น `Color.getWhite()`) ไปยัง `rotate` |
| **ข้อผิดพลาดหน่วยความจำเมื่อ PSD ขนาดใหญ่** | ไม่ได้แคชภาพ | เรียก `image.cacheData()` ก่อนทำการประมวลผล |
| **ทิศทางมุมไม่ถูกต้อง** | สับสนระหว่างค่าลบและบวก | ใช้ค่าลบสำหรับการหมุนตามเข็มนาฬิกา (หรือกลับกันตามระบบพิกัดของคุณ) |
| **การเปลี่ยนแปลงไม่ถูกบันทึก** | ลืมเรียก `save` | ตรวจสอบให้แน่ใจว่า `image.save(...)` ถูกเรียกหลังจากหมุน |

## คำถามที่พบบ่อย

**ถาม: ฉันสามารถหมุนภาพที่มีความโปร่งใสได้ด้วย Aspose.PSD for Java หรือไม่?**  
ตอบ: ได้. ไลบรารีคงอัลฟาแชนแนล; หากไม่ต้องการสีพื้นหลังให้ละเว้นการกำหนดสีอัปเปอร์

**ถาม: มีข้อจำกัดรูปแบบไฟล์ใดสำหรับการหมุนหรือไม่?**  
ตอบ: ไม่มี. Aspose.PSD รองรับ PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF, และรูปแบบเพิ่มเติมกว่า 30 รูปแบบ

**ถาม: ฉันสามารถหมุนภาพด้วยมุมลบได้หรือไม่?**  
ตอบ: แน่นอน. ส่งค่า float ลบให้กับ `rotate` (เช่น `-30f`) เพื่อหมุนตามเข็มนาฬิกา

**ถาม: Aspose.PSD มีการแสดงตัวอย่างภาพแบบเรียลไทม์ขณะหมุนหรือไม่?**  
ตอบ: API ทำงานบนเซิร์ฟเวอร์เท่านั้น. หากต้องการพรีวิวสด, ให้เรนเดอร์บิทแมปที่หมุนแล้วใน UI เช่น Swing หรือ JavaFX แล้วรีเฟรชวิว

**ถาม: มีฟอรั่มชุมชนสำหรับ Aspose.PSD ที่ฉันสามารถขอความช่วยเหลือได้หรือไม่?**  
ตอบ: มี, เยี่ยมชม [ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) เพื่อถามคำถามและแบ่งปันประสบการณ์

---

**อัปเดตล่าสุด:** 2026-05-19  
**ทดสอบกับ:** Aspose.PSD for Java 24.11 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
image.save(destName, new JpegOptions());
```

## บทแนะนำที่เกี่ยวข้อง

- [การปรับขนาดภาพคุณภาพสูงด้วย Bicubic Resampler ใน Aspose.PSD for Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Resize Image Java - การใช้ Resize Type Enumeration ใน Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [Blur Image Java ด้วย Aspose.PSD – เพิ่มเอฟเฟกต์เบลอร์](/psd/java/advanced-techniques/blur-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}