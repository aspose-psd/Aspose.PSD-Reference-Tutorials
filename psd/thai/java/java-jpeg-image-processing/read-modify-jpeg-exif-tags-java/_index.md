---
date: 2026-10-03
description: เรียนรู้วิธีการอ่านเมตาดาต้าภาพด้วย Java และแก้ไขแท็ก JPEG EXIF ด้วย
  Aspose.PSD for Java ในคู่มือขั้นตอนต่อขั้นตอนนี้ เหมาะสำหรับนักพัฒนาที่จัดการเมตาดาต้าภาพอย่างมีประสิทธิภาพ
keywords:
- java read image metadata
- read EXIF tags Java
- modify JPEG metadata Java
- Aspose.PSD Java
lastmod: 2026-10-03
linktitle: อ่านและแก้ไขแท็ก JPEG EXIF ด้วย Java
og_description: เรียนรู้วิธีการอ่านเมตาดาต้าภาพด้วย Java และแก้ไขแท็ก JPEG EXIF ด้วย
  Aspose.PSD for Java. คู่มือนี้แสดง step‑by‑step code สำหรับการสกัดและอัปเดตข้อมูล
  EXIF
og_image_alt: Guide showing how to java read image metadata and edit JPEG EXIF tags
  using Aspose.PSD for Java
og_title: วิธีการอ่านเมตาดาต้าภาพด้วย Java และแก้ไขแท็ก JPEG EXIF
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  headline: How to java read image metadata and modify JPEG EXIF tags
  type: TechArticle
- description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  name: How to java read image metadata and modify JPEG EXIF tags
  steps:
  - name: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
    text: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
  type: HowTo
- questions:
  - answer: EXIF (Exchangeable Image File Format) metadata stores camera settings,
      timestamps, GPS coordinates, and other information embedded in JPEG and other
      image files.
    question: What is EXIF data?
  - answer: You can get a free trial from the [Aspose releases page](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for Java for free?
  - answer: Aspose.PSD for Java supports Java SE 7 and above.
    question: Is Aspose.PSD for Java compatible with all versions of Java?
  - answer: Check out the [documentation](https://reference.aspose.com/psd/java/)
      for more details.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: You can get support from the [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).
    question: How do I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- exif tags
- aspose psd
- jpeg metadata
- java tutorial
title: วิธีการอ่านเมตาดาต้าภาพด้วย Java และแก้ไขแท็ก JPEG EXIF
url: /th/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# อ่านและแก้ไขแท็ก EXIF ของ JPEG ใน Java

## บทนำ
หากคุณต้องการ **java read image metadata** จากไฟล์ JPEG และเปลี่ยนแปลงโดยโปรแกรม คุณมาถูกที่แล้ว ในบทเรียนนี้เราจะอธิบายการดึงและอัปเดตแท็ก EXIF ด้วย Aspose.PSD for Java เมื่อเสร็จคุณจะสามารถดึงรายละเอียดกล้อง, การจัดแนว, และฟิลด์กำหนดเอง แล้วเขียนกลับไปยังไฟล์ — ทั้งหมดโดยไม่ต้องใช้โปรแกรมแก้ไขกราฟิก

## คำตอบอย่างรวดเร็ว
- **ไลบรารีใดที่จัดการ JPEG EXIF ใน Java?** Aspose.PSD for Java.
- **ต้องใช้บรรทัดโค้ดกี่บรรทัดเพื่ออ่าน EXIF?** ประมาณสามบรรทัดหลังจากโหลดภาพ.
- **สามารถแก้ไขแท็ก EXIF ได้หรือไม่?** ใช่ คุณสามารถเปลี่ยนแท็กมาตรฐานหรือกำหนดเองใด ๆ แล้วบันทึกผลลัพธ์.
- **รูปแบบภาพที่รองรับ?** มากกว่า 150 รูปแบบ รวมถึง PSD, JPEG, PNG, TIFF, และ BMP.
- **เวอร์ชัน Java ขั้นต่ำ?** Java 7 หรือสูงกว่า.

## ทำไมต้องใช้ Aspose.PSD for Java?
Aspose.PSD รองรับ **150+ รูปแบบภาพ** และสามารถประมวลผลไฟล์ได้ถึง **2 GB** โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ ทำให้คุณทำการดำเนินการเมตาดาต้าอย่างรวดเร็วและใช้หน่วยความจำน้อยบนคอลเลกชันภาพขนาดใหญ่ นอกจากนี้ยังมี API ที่ง่ายต่อการอ่านและเขียนข้อมูล EXIF, IPTC, และ XMP ทำให้การประมวลผลแบบแบตช์ของภาพหลายพันรูปมีประสิทธิภาพและเชื่อถือได้.

## ข้อกำหนดเบื้องต้น
1. **Java Development Kit (JDK)** – ตรวจสอบให้แน่ใจว่าคุณมี JDK 11 หรือใหม่กว่า คุณสามารถดาวน์โหลดได้จาก [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – รับไฟล์ JAR ล่าสุดจาก [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse หรือโปรแกรมแก้ไขใด ๆ ที่คุณชอบ.  
4. **Basic Java knowledge** – คุณควรคุ้นเคยกับการสร้างโปรเจกต์และเพิ่ม JAR ภายนอก.

## Java read image metadata คืออะไร?
Java read image metadata หมายถึงกระบวนการเข้าถึงข้อมูลที่ฝังอยู่ในไฟล์ภาพ เช่น EXIF, IPTC, และ XMP โดยใช้โค้ด Java อย่างโปรแกรมเมติก ข้อมูลเมตาดาต้านี้อาจรวมถึงการตั้งค่ากล้อง, เวลาที่บันทึก, พิกัด GPS, หมายเหตุลิขสิทธิ์, และความคิดเห็นของผู้ใช้ ทำให้แอปพลิเคชันสามารถจัดระเบียบ, ค้นหา, และจัดการภาพตามข้อมูลอธิบายได้.

## นำเข้าชุดแพ็กเกจ
ขั้นแรก ให้เพิ่มไฟล์ JAR ของ Aspose.PSD ไปยัง classpath ของโปรเจกต์และนำเข้าคลาสที่จำเป็น

แพ็กเกจ `com.aspose.psd` ให้ API หลักสำหรับการโหลดภาพและเข้าถึงทรัพยากรของมัน.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## วิธีอ่านเมตาดาต้าภาพจากไฟล์ JPEG ใน Java?
โหลดไฟล์ JPEG ด้วย `PsdImage.load("image.jpg")`, ค้นหาแหล่งข้อมูล thumbnail ที่เก็บข้อมูล EXIF, แล้วเรียก `ExifData.read()` เพื่อรับอ็อบเจกต์ `ExifData` ที่เต็มไปด้วยข้อมูล วิธีการขั้นตอนเดียวนี้ทำให้คุณเข้าถึงฟิลด์ EXIF มาตรฐานทั้งหมดและแท็กกำหนดเองใด ๆ ที่คุณอาจเพิ่มได้.

## ขั้นตอนที่ 1: โหลดภาพ PSD
PsdImage คือคลาสของ Aspose.PSD ที่แทนไฟล์ PSD และให้เมธอดสำหรับเข้าถึงทรัพยากรและเมตาดาต้าของมัน  
ในขั้นตอนนี้ เราจะโหลดภาพ PSD ที่ต้องการอ่านข้อมูล EXIF ตรวจสอบให้แน่ใจว่าภาพของคุณอยู่ในไดเรกทอรีที่ถูกต้อง.

```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## ขั้นตอนที่ 2: วนลูปผ่านทรัพยากรภาพ
ThumbnailResource แทนภาพย่อที่เก็บในไฟล์ PSD ซึ่งมักมีข้อมูล EXIF ฝังอยู่  
เมื่อโหลดภาพแล้ว ขั้นตอนต่อไปคือการวนลูปผ่านทรัพยากรเพื่อค้นหา ThumbnailResource ซึ่งโดยปกติจะมีข้อมูล EXIF.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Proceed to next step
    }
}
```

## ขั้นตอนที่ 3: ดึงข้อมูล EXIF
JpegExifData คือคลาสที่เก็บข้อมูล EXIF ที่ดึงจากภาพ JPEG ทำให้คุณสามารถอ่านและแก้ไขแท็กแต่ละรายการได้  
ตอนนี้เรามี ThumbnailResource แล้ว เราสามารถดึงข้อมูล EXIF จากมันได้ ข้อมูล EXIF ประกอบด้วยข้อมูลสำคัญเช่น ชื่อเจ้าของกล้อง, ค่า aperture, การจัดแนว, และอื่น ๆ.

```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```

## ขั้นตอนที่ 4: แก้ไขข้อมูล EXIF
หลังจากอ่านข้อมูล EXIF แล้ว คุณอาจต้องการแก้ไขฟิลด์บางส่วน นี่คือตัวอย่างวิธีทำ:

```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```

## ขั้นตอนที่ 5: บันทึกการเปลี่ยนแปลง
สุดท้าย หลังจากแก้ไขข้อมูล EXIF แล้ว ให้บันทึกการเปลี่ยนแปลงไปยังไฟล์ PSD ใหม่.

```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## ปัญหาทั่วไปและวิธีแก้
- **Missing thumbnail resource** – JPEG บางไฟล์เก็บ EXIF ไว้โดยตรงในส่วนหัวของภาพหลัก หากไม่มี ThumbnailResource ให้ใช้ `image.getExifData()` แทน.  
- **Large files cause OutOfMemoryError** – ตรวจสอบให้แน่ใจว่าคุณรัน JVM ด้วย heap เพียงพอ (`-Xmx2g`) หรือประมวลผลภาพในโหมดสตรีมโดยใช้ `PsdImage.load(inputStream, loadOptions)`.  
- **Unsupported tag types** – Aspose.PSD รองรับแท็ก EXIF มาตรฐานทั้งหมด; แท็กกำหนดเองอาจต้องจัดการระดับไบต์ด้วยตนเอง.

## คำถามที่พบบ่อย

**Q: EXIF data คืออะไร?**  
A: EXIF (Exchangeable Image File Format) เป็นเมตาดาต้าที่เก็บการตั้งค่ากล้อง, เวลาที่บันทึก, พิกัด GPS, และข้อมูลอื่น ๆ ที่ฝังอยู่ในไฟล์ JPEG และไฟล์ภาพอื่น ๆ.

**Q: ฉันสามารถใช้ Aspose.PSD for Java ได้ฟรีหรือไม่?**  
A: คุณสามารถรับรุ่นทดลองฟรีจาก [Aspose releases page](https://releases.aspose.com/).

**Q: Aspose.PSD for Java รองรับทุกเวอร์ชันของ Java หรือไม่?**  
A: Aspose.PSD for Java รองรับ Java SE 7 ขึ้นไป.

**Q: ฉันจะหาเอกสารเพิ่มเติมเกี่ยวกับ Aspose.PSD for Java ได้จากที่ไหน?**  
A: ดูที่ [documentation](https://reference.aspose.com/psd/java/) เพื่อดูรายละเอียดเพิ่มเติม.

**Q: ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD for Java ได้อย่างไร?**  
A: คุณสามารถรับการสนับสนุนจาก [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).

## สรุป
โดยทำตามขั้นตอนเหล่านี้ คุณสามารถ **java read image metadata** จาก JPEG ใดก็ได้ ปรับฟิลด์ EXIF ที่ต้องการ และเขียนข้อมูลที่อัปเดตกลับไปยังไฟล์ — ทั้งหมดด้วยไม่กี่บรรทัดของโค้ด Java ที่สะอาด Aspose.PSD มี API ที่ครอบคลุมทำให้การจัดการเมตาดาต้าเป็นเรื่องเชื่อถือได้และมีประสิทธิภาพ ดังนั้นคุณสามารถนำไปผสานในไพรไลน์การประมวลผลแบบแบตช์, เครื่องมือจัดการรูปภาพ, หรือแอปพลิเคชันใด ๆ ที่ต้องทำงานกับข้อมูลภาพ

---

**Last Updated:** 2026-10-03  
**Tested With:** Aspose.PSD for Java 24.5  
**Author:** Aspose

## บทเรียนที่เกี่ยวข้อง

- [อ่านข้อมูลแท็ก EXIF เฉพาะใน Java ด้วย Aspose (asp)](/psd/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/)
- [สร้างเมตาดาต้า XMP ในไฟล์ PSD ด้วย Aspose.PSD for Java](/psd/java/image-editing/create-xmp-metadata/)
- [ปรับขนาดภาพด้วย Aspose.PSD for Java – วาดรูปและการดำเนินการพื้นฐานของภาพ](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}