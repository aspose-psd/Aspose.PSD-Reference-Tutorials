---
date: 2026-03-13
description: เรียนรู้วิธีสร้างภาพย่อ PSD ด้วย Java โดยใช้ Aspose.PSD. ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนของเราเพื่อสร้างภาพย่อจากไฟล์
  PSD อย่างรวดเร็ว.
linktitle: Create Thumbnails from PSD Files using Java
second_title: Aspose.PSD Java API
title: สร้างภาพย่อ PSD ด้วย Java – สร้างภาพย่อจากไฟล์ PSD
url: /th/java/modifying-converting-psd-images/create-thumbnails-psd-files/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้าง PSD Thumbnail Java – สร้างภาพย่อจาก PSD

## Introduction
หากคุณต้องการ **create PSD thumbnail Java** โค้ดที่ดึงภาพตัวอย่างจากไฟล์ Photoshop คุณมาถูกที่แล้ว ไม่ว่าคุณจะกำลังสร้างระบบจัดการสินทรัพย์ดิจิทัล, แกลเลอรีเว็บ, หรือไพพ์ไลน์การประมวลผลแบบแบตช์อัตโนมัติ การสร้างภาพย่อจากไฟล์ PSD สามารถปรับปรุงประสิทธิภาพและประสบการณ์ผู้ใช้ได้อย่างมาก ในบทแนะนำนี้เราจะเดินผ่านกระบวนการทั้งหมดด้วย Aspose.PSD for Java แสดงให้คุณเห็นวิธีโหลด PSD, ค้นหาแหล่งข้อมูลภาพย่อที่ฝังอยู่, และบันทึกเป็นไฟล์ภาพแยกต่างหาก

## Quick Answers
- **ไลบรารีที่ดีที่สุดสำหรับการสกัดภาพย่อ PSD คืออะไร?** Aspose.PSD for Java.  
- **การทำงานนี้ใช้เวลานานแค่ไหน?** ประมาณ 10‑15 นาทีสำหรับการตั้งค่าเบื้องต้น.  
- **ต้องติดตั้ง Photoshop ไหม?** ไม่จำเป็น, Aspose.PSD ทำงานได้โดยอิสระ.  
- **สามารถส่งออกภาพย่อเป็นฟอร์แมตใดได้บ้าง?** ฟอร์แมตใดก็ได้ที่ Aspose.PSD รองรับ (เช่น BMP, PNG, JPEG).  
- **ต้องมีลิขสิทธิ์สำหรับการใช้งานในโปรดักชันหรือไม่?** ใช่, จำเป็นต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานในโปรดักชัน.

## What is “create PSD thumbnail Java”?
การสร้าง PSD thumbnail ใน Java หมายถึงการอ่านภาพย่อที่เก็บไว้ภายในไฟล์ Photoshop Document (PSD) อย่างโปรแกรมเมติกและเขียนออกเป็นไฟล์ภาพแยกต่างหาก ซึ่งเป็นประโยชน์สำหรับการสร้างตัวอย่างอย่างรวดเร็วโดยไม่ต้องโหลดเนื้อหา PSD ที่มักมีขนาดใหญ่เต็มรูปแบบ

## Why use Aspose.PSD for this task?
- **ไม่มีการพึ่งพา Photoshop:** ทำงานบนแพลตฟอร์มใดก็ได้ที่มี JDK.  
- **รองรับ PSD อย่างเต็มรูปแบบ:** จัดการเวอร์ชันและแหล่งข้อมูล PSD ทั้งหมด รวมถึงภาพย่อ.  
- **API ที่เรียบง่าย:** เพียงไม่กี่บรรทัดของโค้ดก็สามารถสกัดและบันทึกภาพย่อได้.  
- **ประสิทธิภาพสูง:** จัดการหน่วยความจำอย่างมีประสิทธิภาพสำหรับไฟล์ขนาดใหญ่.

## Prerequisites
ก่อนที่เราจะลงลึกในรายละเอียดการสร้างภาพย่อ ให้ตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมใช้งาน

### Java Development Environment
- **Java JDK:** ตรวจสอบว่าคุณได้ติดตั้ง Java Development Kit (JDK) บนคอมพิวเตอร์ของคุณแล้ว คุณสามารถดาวน์โหลดได้จาก [ที่นี่](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
- **IDE:** Integrated Development Environment (IDE) เช่น IntelliJ IDEA, Eclipse หรือ NetBeans จะช่วยให้การเขียนโค้ดง่ายขึ้น

### Aspose.PSD Library
- คุณต้องรวมไลบรารี Aspose.PSD เข้าในโปรเจกต์ของคุณ คุณสามารถ [ดาวน์โหลดเวอร์ชันล่าสุดได้ที่นี่](https://releases.aspose.com/psd/java/)

### Basic Knowledge of Java
- ความคุ้นเคยกับพื้นฐานของ Java จะช่วยให้คุณเข้าใจโค้ดตัวอย่างได้ดีขึ้น แนวคิดเช่น คลาส, อ็อบเจ็กต์, และลูปจะถูกใช้บ่อยครั้ง

## Import Packages
เริ่มต้นด้วยการนำเข้าคลาสที่จำเป็นจากไลบรารี Aspose.PSD ขั้นตอนนี้สำคัญเพราะทำให้คุณสามารถใช้ฟังก์ชันของไลบรารีในโค้ดของคุณได้

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

เมื่อเตรียมความพร้อมเรียบร้อยแล้ว เรามาเริ่มขั้นตอนหลักกัน! การสร้างภาพย่อจากไฟล์ PSD มีขั้นตอนไม่กี่ขั้นตอนที่ง่ายดาย และฉันจะแบ่งให้คุณตามลำดับ

## How to create PSD thumbnail Java – Step‑by‑Step Guide

### Step 1: Set Up Your Environment
นี่คือวิธีเริ่มโปรเจกต์และเตรียมการสำหรับการสร้างภาพย่อ

1. **Create a Java Project**  
   - เปิด IDE ของคุณและสร้างโปรเจกต์ Java ใหม่  
   - ตั้งชื่ออย่างเช่น `"PsdThumbnailGenerator"`

2. **Include Aspose.PSD Library**  
   - เพิ่มไฟล์ JAR ของ Aspose.PSD ไปยัง build path ของโปรเจกต์  
   - หากคุณใช้ Maven ให้ใส่ลงใน `pom.xml` ของคุณ:

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-psd</artifactId>
    <version>your_version_here</version>
</dependency>
```

### Step 2: Load the PSD File
ต่อไปเราต้องโหลดไฟล์ PSD ที่ต้องการสร้างภาพย่อ

1. **Specify Your Document Directory**  
   กำหนดโฟลเดอร์ที่ไฟล์ PSD ของคุณอยู่

```java
String dataDir = "Your Document Directory"; // Replace with your path
```

2. **Load the PSD File**  
   ใช้คลาส `PsdImage` เพื่อโหลดไฟล์ PSD ของคุณ

```java
PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
```

> **Pro tip:** เก็บไฟล์ PSD ไว้ในโฟลเดอร์เฉพาะ (เช่น `src/main/resources`) เพื่อหลีกเลี่ยงปัญหาเกี่ยวกับพาธ

### Step 3: Iterate Over PSD Resources
เมื่อเราโหลดภาพ PSD แล้ว ขั้นตอนต่อไปคือการตรวจสอบแหล่งข้อมูลของมัน

1. **Get Resources Count**  
   เราจะวนลูปผ่านทุกแหล่งข้อมูลในไฟล์ PSD

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Processing resources
}
```

2. **Identify Thumbnail Resources**  
   ภายในลูปให้ตรวจสอบว่าแหล่งข้อมูลเป็นภาพย่อหรือไม่

```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    // Process the thumbnail
}
```

### Step 4: Process the Thumbnail
เมื่อเราตรวจพบแหล่งข้อมูลภาพย่อ เราจะต้องจัดการกับมันต่อไป

1. **Retrieve and Check Thumbnail Format**  
   หากแหล่งข้อมูลเป็นภาพย่อ ให้ดึงข้อมูลและตรวจสอบฟอร์แมตของมัน

```java
ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
    // Create and save the thumbnail
}
```

### Step 5: Create and Save the Thumbnail
นี่คือจุดที่ความมหัศจรรย์เกิดขึ้น! เราจะสร้างภาพใหม่จากข้อมูลภาพย่อและบันทึกมัน

1. **Create a New Image**  
   เราจะใช้ความกว้างและความสูงของแหล่งข้อมูลภาพย่อเพื่อสร้างบิทแมพใหม่

```java
PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
```

2. **Store Pixels in the New Image**  
   โอนข้อมูลพิกเซลจากภาพย่อไปยังภาพใหม่ที่สร้างขึ้น

```java
thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
```

3. **Save the Thumbnail Image**  
   สุดท้ายบันทึกภาพย่อลงในโฟลเดอร์เอกสารของคุณด้วยชื่อที่ไม่ซ้ำกัน

```java
thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
```

> **Common pitfall:** ลืมปิดอ็อบเจ็กต์ `PsdImage` สามารถทำให้เกิดการรั่วของหน่วยความจำได้ ควรห่อโค้ดการจัดการภาพด้วย `try‑with‑resources` หากคุณใช้ Java 7 ขึ้นไป

## Conclusion
โดยทำตามขั้นตอนเหล่านี้ คุณจะมีวิธีการ **create PSD thumbnail Java** ที่แข็งแรงและนำกลับมาใช้ใหม่ได้สำหรับการสกัดภาพตัวอย่างจากไฟล์ Photoshop ใด ๆ เทคนิคนี้สามารถนำไปผสานกับโปรเซสแบตช์, เว็บเซอร์วิส, หรือยูทิลิตี้เดสก์ท็อปเพื่อเร่งการจัดทำแคตาล็อกภาพและเพิ่มความตอบสนองของ UI ลองใช้กับคอลเลกชัน PSD ของคุณและดูว่าคุณสามารถสร้างภาพย่อที่เบาและรวดเร็วได้เร็วแค่ไหน!

## FAQ's
### What is Aspose.PSD?
Aspose.PSD เป็นไลบรารี Java ที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Photoshop ได้อย่างง่ายดายโดยโปรแกรมเมติก

### Can I use Aspose.PSD for free?
ใช่, Aspose มีรุ่นทดลองฟรีที่คุณสามารถใช้ทดสอบไลบรารีก่อนตัดสินใจซื้อ

### What formats can I save the thumbnails in?
ในตัวอย่างนี้เราบันทึกภาพย่อเป็นฟอร์แมต BMP แต่ Aspose.PSD รองรับฟอร์แมตอื่น ๆ อีกหลายรูปแบบ

### Do I need Photoshop installed to use Aspose.PSD?
ไม่จำเป็น, Aspose.PSD ทำงานได้โดยอิสระจาก Photoshop

### Where can I find more information about Aspose.PSD?
คุณสามารถดูรายละเอียดเพิ่มเติมใน [Aspose.PSD documentation](https://reference.aspose.com/psd/java/) เพื่อเรียนรู้เพิ่มเติมเกี่ยวกับบทเรียนและทรัพยากรอื่น ๆ

## Frequently Asked Questions

**Q: How do I extract thumbnails from a password‑protected PSD?**  
A: โหลด PSD ด้วย overload ของ `Image.load` ที่รับพารามิเตอร์รหัสผ่าน

**Q: Can I generate thumbnails in PNG instead of BMP?**  
A: แน่นอน เพียงเปลี่ยนนามสกุลไฟล์ในเมธอด `save` แล้ว Aspose.PSD จะทำการแปลงให้เอง

**Q: Is there a way to batch‑process multiple PSD files?**  
A: ห่อโค้ดภายในลูปที่วนผ่านไดเรกทอรีของไฟล์ PSD เพื่อใช้ตรรกะการสกัดภาพย่อซ้ำสำหรับแต่ละไฟล์

**Q: What Java version is required?**  
A: Aspose.PSD รองรับ Java 8 ขึ้นไป แนะนำให้ใช้ JDK เวอร์ชันล่าสุดเพื่อประสิทธิภาพและความปลอดภัย

**Q: Does the library handle large PSD files efficiently?**  
A: ใช่, Aspose.PSD ใช้การโหลดแบบ lazy และการจัดการหน่วยความจำที่ปรับแต่งเพื่อทำงานกับไฟล์ขนาดใหญ่โดยไม่ทำให้ heap เต็ม

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.PSD 24.11 for Java (latest at time of writing)  
**Author:** Aspose  

---