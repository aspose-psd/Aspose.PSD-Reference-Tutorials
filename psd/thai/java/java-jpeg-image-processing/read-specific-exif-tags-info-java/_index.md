---
date: 2026-10-08
description: เรียนรู้วิธีอ่านแท็ก EXIF ใน Java ด้วย Aspose.PSD for Java (asp) ผ่านบทเรียนแบบขั้นตอนต่อขั้นตอนของเรา
  และเพิ่มศักยภาพการประมวลผลภาพของคุณ
keywords:
- read exif tags java
- java exif tag extraction
- java image metadata extraction
lastmod: 2026-10-08
linktitle: อ่านข้อมูลแท็ก EXIF เฉพาะใน Java
og_description: อ่านแท็ก EXIF นักพัฒนา Java สามารถดึงข้อมูลเมตาดาต้าภาพได้อย่างรวดเร็วด้วย
  Aspose.PSD คู่มือนี้จะพาคุณผ่านขั้นตอนการโหลดไฟล์ PSD การค้นหาแหล่งข้อมูลรูปย่อ
  และการพิมพ์ฟิลด์ EXIF สำคัญ เช่น WhiteBalance และ ISO speed
og_image_alt: Guide showing how to read EXIF tags from PSD files in Java using Aspose.PSD
og_title: วิธีอ่านแท็ก EXIF ใน Java ด้วย Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-08'
  description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  headline: How to read EXIF tags in Java with Aspose.PSD
  type: TechArticle
- description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  name: How to read EXIF tags in Java with Aspose.PSD
  steps:
  - name: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
    text: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
  - name: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
    text: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
  - name: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
    text: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
  type: HowTo
- questions:
  - answer: Aspose.PSD (asp)
    question: What library reads EXIF data from PSD in Java?
  - answer: WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength,
      and more.
    question: Which tags can be extracted?
  - answer: Yes, a commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: The same API supports PNG, JPEG, TIFF via Java image metadata extraction.
    question: Can I use this with other image formats?
  - answer: About 10‑15 minutes for a basic read‑only scenario.
    question: How long does implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- read exif tags java
- Aspose.PSD
- java image metadata extraction
- EXIF extraction
- PSD processing
title: วิธีอ่านแท็ก EXIF ใน Java ด้วย Aspose.PSD
url: /th/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# อ่านข้อมูลแท็ก EXIF เฉพาะใน Java ด้วย Aspose (asp)

## บทนำ
หากคุณต้องการ **อ่านแท็ก EXIF ใน Java **, Aspose.PSD (asp) มี API แบบ pure‑Java ที่สะอาดและทำงานได้โดยไม่ต้องใช้ Photoshop ในบทแนะนำนี้คุณจะได้เรียนรู้วิธีสกัดข้อมูล EXIF จากภาพ PSD, เลือกเฉพาะแท็กที่คุณสนใจ, และพิมพ์ออกที่คอนโซล เราจะครอบคลุมตั้งแต่การตั้งค่าสภาพแวดล้อมการพัฒนาไปจนถึงการดึงเมตาดาต้าเช่น WhiteBalance, ISO speed, และ focal length มาเริ่มกันเลย!

## คำตอบอย่างรวดเร็ว
- **ไลบรารีใดที่อ่านข้อมูล EXIF จาก PSD ใน Java?** Aspose.PSD (asp)  
- **สามารถสกัดแท็กอะไรได้บ้าง?** WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength, และอื่น ๆ  
- **ต้องใช้ไลเซนส์สำหรับการผลิตหรือไม่?** ใช่, จำเป็นต้องมีไลเซนส์เชิงพาณิชย์; มีรุ่นทดลองฟรีให้ใช้  
- **สามารถใช้กับรูปแบบภาพอื่นได้หรือไม่?** API เดียวกันรองรับ PNG, JPEG, TIFF ผ่านการสกัดเมตาดาต้าภาพใน Java  
- **การนำไปใช้ใช้เวลานานเท่าไหร่?** ประมาณ 10‑15 นาทีสำหรับสถานการณ์อ่าน‑อย่างเดียวพื้นฐาน

## asp คืออะไร (Aspose.PSD for Java)?
Aspose.PSD for Java เป็นไลบรารี pure‑Java ที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Adobe Photoshop (PSD, PSB) โดยไม่ต้องติดตั้ง Photoshop มันให้การเข้าถึงโปรแกรมเมติกต่อเลเยอร์, ทรัพยากร, และเมตาดาต้า—including EXIF tags—ทำให้เหมาะสำหรับงาน **java image metadata extraction** 

## ทำไมต้องใช้ Aspose.PSD (asp) สำหรับการสกัด EXIF?
คุณสามารถสกัดแท็ก EXIF ใน Java ได้ด้วยเพียงสองการเรียกเมธอด และไลบรารีสามารถประมวลผลไฟล์ขนาดถึง 2 GB โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ รองรับ **30+ image formats** และคงค่าการตั้งค่ากล้องอย่างแม่นยำ ทำให้ได้ผลลัพธ์ที่สอดคล้องกันบน Windows, Linux, และ macOS

## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะลงลึกในโค้ด มีสิ่งที่คุณต้องเตรียมไว้ดังนี้:

1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนเครื่องของคุณแล้ว คุณสามารถดาวน์โหลดได้จาก [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html)  
2. Aspose.PSD for Java: ดาวน์โหลดไลบรารีจาก [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)  
3. Integrated Development Environment (IDE): IDE เช่น IntelliJ IDEA, Eclipse, หรือ NetBeans จะทำให้การเขียนโค้ดสะดวกยิ่งขึ้น  
4. PSD file: ไฟล์ PSD ที่มีข้อมูล EXIF คุณสามารถใช้ตัวอย่างที่ให้มาในบทแนะนำนี้หรือไฟล์ PSD ใด ๆ ที่มีแท็ก EXIF

## นำเข้าแพ็กเกจ
นำเข้าคลาส Aspose.PSD ที่จำเป็น เช่น Image, PsdImage, ThumbnailResource, และ JpegExifData เพื่อทำงานกับไฟล์ PSD  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## ขั้นตอนที่ 1: โหลดภาพ PSD
`Image.load()` โหลดไฟล์และคืนค่าอ็อบเจ็กต์ Image ที่แสดงข้อมูลภาพ  
`PsdImage` คือคลาส Aspose.PSD ที่ให้ฟังก์ชันเฉพาะสำหรับ PSD  
เมธอด `Image.load()` จะโหลดไฟล์ภาพที่รองรับใด ๆ ลงในหน่วยความจำและคืนค่าอ็อบเจ็กต์ `Image` ทั่วไปที่คุณสามารถแคสต์เป็นประเภทเฉพาะของ PSD ได้  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```

ในขั้นตอนนี้ เราโหลดไฟล์ PSD ด้วยเมธอด `Image.load()` คลาส `PsdImage` ถูกใช้เพื่อแทนภาพ PSD และเราจะแคสต์อ็อบเจ็กต์ที่โหลดมาเป็นคลาสนี้เพื่อเข้าถึงฟังก์ชันเฉพาะของ PSD

## ขั้นตอนที่ 2: วนลูปทรัพยากรภาพ
`PsdImage.getResources()` คืนคอลเลกชันของทรัพยากรที่ฝังอยู่ เช่น thumbnails และข้อมูล EXIF  
การเรียก `PsdImage.getResources()` จะให้คอลเลกชันของทรัพยากรที่ฝังอยู่ทั้งหมด โดยการวนลูปผ่านคอลเลกชันนี้คุณสามารถค้นหา thumbnail ที่มีเมตาดาต้า EXIF ได้  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Further processing will be done here
    }
}
```

เราวนลูปผ่านทรัพยากรของภาพด้วย `for` loop เป้าหมายคือระบุทรัพยากรที่เป็นอินสแตนซ์ของ `ThumbnailResource` หรือ `Thumbnail4Resource` เนื่องจากเป็นประเภทที่เก็บข้อมูล EXIF

## ขั้นตอนที่ 3: สกัดข้อมูล EXIF
`ThumbnailResource.getJpegOptions()` ให้การเข้าถึงตัวเลือก JPEG รวมถึงเมตาดาต้า EXIF  
`JpegExifData` เก็บค่าของแท็ก EXIF แต่ละรายการ  
เมธอด `ThumbnailResource.getJpegOptions()` ให้การเข้าถึงอ็อบเจ็กต์ `JpegExifData` ซึ่งเก็บแท็ก EXIF เช่น WhiteBalance, ISOSpeed, และ FocalLength  
```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
    if (exif != null) {
        System.out.println("Exif WhiteBalance: " + exif.getWhiteBalance());
        System.out.println("Exif PixelXDimension: " + exif.getPixelXDimension());
        System.out.println("Exif PixelYDimension: " + exif.getPixelYDimension());
        System.out.println("Exif ISOSpeed: " + exif.getISOSpeed());
        System.out.println("Exif FocalLength: " + exif.getFocalLength());
    }
}
```

เราใช้คำสั่ง `if` เพื่อตรวจสอบว่าทรัพยากรเป็นอินสแตนซ์ของ `ThumbnailResource` หรือไม่ หากใช่ เราจะแคสต์และดึง `JpegOptions` เพื่อเข้าถึง `ExifData` สุดท้ายพิมพ์แท็ก EXIF ต่าง ๆ เช่น WhiteBalance, Pixel Dimensions, ISOSpeed, และ FocalLength

## ปัญหาทั่วไปและเคล็ดลับ
- **Null EXIF data:** บางไฟล์ PSD อาจไม่มีทรัพยากร thumbnail ที่มีข้อมูล EXIF ตรวจสอบ `null` ก่อนเข้าถึงค่าแท็กเสมอ  
- **File path errors:** ใช้เส้นทางแบบ absolute หรือให้แน่ใจว่าไดเรกทอรีทำงานชี้ไปที่โฟลเดอร์ที่มีไฟล์ PSD ของคุณ  
- **License restrictions:** รุ่นทดลองจำกัดจำนวนหน้าที่สามารถประมวลผลได้; อัปเกรดเป็นไลเซนส์เต็มเพื่อใช้งานไม่จำกัด

## คำถามที่พบบ่อย

### EXIF คืออะไร?
EXIF (Exchangeable Image File Format) คือเมตาดาต้าที่ฝังอยู่ในไฟล์ภาพ ประกอบด้วยข้อมูลเช่นการตั้งค่ากล้อง, วันที่และเวลา, และขนาดภาพ

### ฉันสามารถแก้ไขข้อมูล EXIF ด้วย Aspose.PSD ได้หรือไม่?
ใช่, Aspose.PSD อนุญาตให้คุณอ่านและแก้ไขข้อมูล EXIF คุณสามารถอัปเดตแท็กและบันทึกการเปลี่ยนแปลงกลับไปยังไฟล์ภาพได้

### Aspose.PSD สำหรับ Java ฟรีหรือไม่?
Aspose.PSD มีรุ่นทดลองฟรีที่คุณสามารถดาวน์โหลดได้จาก [Aspose.PSD official releases page](https://releases.aspose.com/) สำหรับฟีเจอร์เต็มต้องซื้อไลเซนส์

### Aspose.PSD รองรับรูปแบบอื่นอะไรบ้าง?
Aspose.PSD รองรับรูปแบบไฟล์ Adobe Photoshop ต่าง ๆ รวมถึง PSD, PSB, และอื่น ๆ อีกทั้งยังมีตัวเลือกแปลงรูปแบบเหล่านี้เป็น PNG, JPEG, TIFF ฯลฯ

### ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD ได้อย่างไร?
คุณสามารถรับการสนับสนุนผ่าน [forum](https://forum.aspose.com/c/psd/34) ของ Aspose.PSD

### สิ่งนี้ช่วยกับ **java image metadata extraction** อย่างไร?
โดยใช้ `JpegExifData` คุณสามารถดึงแท็ก EXIF ใด ๆ ที่ต้องการได้โดยโปรแกรมเมติก ทำให้เป็นพื้นฐานที่มั่นคงสำหรับงานสกัดเมตาดาต้าขนาดใหญ่ในรูปแบบภาพต่าง ๆ

---

**อัปเดตล่าสุด:** 2026-10-08  
**ทดสอบกับ:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [อ่านและแก้ไขแท็ก Jpeg Exif ด้วย Java](/psd/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/)
- [การประมวลผลภาพ Jpeg ด้วย Java](/psd/java/java-jpeg-image-processing/)
- [วิธีหมุนภาพตามมุมที่กำหนดด้วย Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}