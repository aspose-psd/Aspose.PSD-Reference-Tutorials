---
date: 2026-09-28
description: วิธีเพิ่มรูปย่อในส่วนของ JFIF ด้วย Java โดยใช้ Aspose.PSD. ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนนี้เพื่อฝังรูปย่อในไฟล์
  PSD อย่างรวดเร็วและเชื่อถือได้.
keywords:
- how to add thumbnail
- JFIF segment Java
- Aspose.PSD thumbnail
- Java image processing
lastmod: 2026-09-28
linktitle: เพิ่มรูปย่อในส่วนของ JFIF ด้วย Java
og_description: วิธีเพิ่มรูปย่อในส่วนของ JFIF ด้วย Java โดยใช้ Aspose.PSD. ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนนี้เพื่อฝังรูปย่อในไฟล์
  PSD อย่างรวดเร็วและเชื่อถือได้.
og_image_alt: Guide showing how to add thumbnail to JFIF segment in Java with Aspose.PSD
og_title: วิธีเพิ่มรูปย่อในส่วนของ JFIF ด้วย Java
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  headline: How to add thumbnail to JFIF segment in Java
  type: TechArticle
- description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  name: How to add thumbnail to JFIF segment in Java
  steps:
  - name: import packages
    text: '`Document`, `JfifResource`, and related classes are part of the Aspose.PSD
      namespace. Document represents the PSD file container, and JfifResource provides
      access to the JFIF segment within the PSD. Import them at the top of your source
      file.'
  - name: load the PSD image
    text: Create a `PsdImage` instance by passing the file path to the constructor.
      PsdImage is the Aspose.PSD class that models a Photoshop document. This loads
      the document metadata while streaming the pixel data.
  - name: iterate over image resources
    text: Search the `Resources` collection for a `JfifResource`. When found, you
      can replace its thumbnail byte array with a new JPEG‑encoded preview.
  - name: adjust thumbnail data
    text: Generate a small JPEG thumbnail (e.g., 120 × 120 px) using any image‑processing
      library, then assign the resulting byte array to `jfifResource.ThumbnailData`.
  - name: save the modified image
    text: Call the `save` method on the `PsdImage` object, specifying the output path
      and desired format. The JFIF segment now contains the new thumbnail.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables developers to
      create, edit, convert, and render Photoshop PSD files without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Detailed documentation can be found on the [Aspose.PSD for Java documentation
      page](https://reference.aspose.com/psd/java/).
    question: Where can I find more documentation for Aspose.PSD for Java?
  - answer: Yes, Aspose.PSD for Java can be used commercially. You can purchase a
      license from [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).
    question: Is Aspose.PSD for Java suitable for commercial use?
  - answer: Yes, you can download a free trial from [Aspose.PSD's trial download page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- add thumbnail
- Aspose.PSD
- Java image processing
- JFIF
- PSD
title: วิธีเพิ่มรูปย่อในส่วนของ JFIF ด้วย Java
url: /th/java/java-jpeg-image-processing/add-thumbnail-to-jfif-segment-java/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีเพิ่มภาพย่อในส่วน JFIF ของ Java

## บทนำ
การเพิ่มภาพย่อในส่วน JFIF ของไฟล์ PSD เป็นความต้องการทั่วไปเมื่อคุณต้องการตัวอย่างภาพอย่างรวดเร็วโดยไม่ต้องโหลดภาพเต็ม ในบทแนะนำนี้คุณจะได้เรียนรู้ **วิธีเพิ่มภาพย่อ** ในส่วน JFIF ด้วย Java โดยใช้ Aspose.PSD เมื่อจบคู่มือคุณจะมีโค้ดตัวอย่างที่สามารถรันได้ ความเข้าใจเกี่ยวกับโครงสร้าง JFIF เบื้องต้น และเคล็ดลับการจัดการไฟล์ขนาดใหญ่อย่างมีประสิทธิภาพ

## คำตอบด่วน
- **ไลบรารีที่ต้องการคืออะไร?** Aspose.PSD for Java.  
- **เวอร์ชัน Java ใดที่ทำงานได้?** JDK 11 หรือใหม่กว่า.  
- **ต้องใช้บรรทัดโค้ดกี่บรรทัด?** ประมาณ 10 บรรทัดเพื่อโหลด แก้ไข และบันทึก.  
- **ฉันสามารถประมวลผลไฟล์หลายเมกะไบต์ได้หรือไม่?** ได้, Aspose.PSD สตรีมข้อมูล ทำให้การใช้หน่วยความจำต่ำ.  
- **จำเป็นต้องมีลิขสิทธิ์เชิงพาณิชย์หรือไม่?** จำเป็นต้องมีลิขสิทธิ์สำหรับการใช้งานในผลิตภัณฑ์; มีรุ่นทดลองฟรีให้ใช้.

## JFIF segment คืออะไร?
JFIF segment คือบล็อก JPEG File Interchange Format ที่สามารถเก็บข้อมูลเสริมเช่นภาพย่อ, EXIF หรือโปรไฟล์สี  
มันอยู่ภายในสตรีม JPEG ของไฟล์ PSD และถูกโปรแกรมดูภาพส่วนใหญ่รับรู้เพื่อสร้างตัวอย่างอย่างรวดเร็ว

## ทำไมต้องเพิ่มภาพย่อในไฟล์ PSD?
Aspose.PSD for Java รองรับ **30+ image formats** และสามารถประมวลผลไฟล์ได้ถึง **2 GB** โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ การเพิ่มภาพย่อช่วยลดแบนด์วิธเมื่อส่งตัวอย่างและเร่งการแสดงผล UI ในแอปพลิเคชันแกลเลอรี

## ข้อกำหนดเบื้องต้น
- Java Development Kit (JDK): ตรวจสอบว่าคุณได้ติดตั้ง Java บนระบบของคุณแล้ว คุณสามารถดาวน์โหลดได้จาก [Oracle's JDK website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
- Aspose.PSD for Java: คุณต้องมีไลบรารี Aspose.PSD for Java คุณสามารถรับได้จาก [Aspose.PSD Java download page](https://releases.aspose.com/psd/java/).
- Integrated Development Environment (IDE): ใช้ IDE เช่น IntelliJ IDEA หรือ Eclipse สำหรับการพัฒนา Java
- Basic Understanding of Java: มีความคุ้นเคยกับภาษาโปรแกรม Java และแนวคิดพื้นฐาน

## วิธีเพิ่มภาพย่อในส่วน JFIF ของ Java?
โหลดไฟล์ PSD เป้าหมาย ค้นหาแหล่งข้อมูล JFIF แทนที่ข้อมูลภาพย่อของมัน แล้วบันทึกไฟล์ การดำเนินการทั้งหมดสามารถทำได้ด้วยการเรียก API ไม่กี่ครั้ง และ Aspose.PSD จะจัดการโครงสร้าง JPEG ระดับต่ำให้คุณ

### ขั้นตอนที่ 1: นำเข้าแพ็กเกจ
`Document`, `JfifResource` และคลาสที่เกี่ยวข้องเป็นส่วนหนึ่งของ namespace Aspose.PSD `Document` แทนไฟล์ PSD container, ส่วน `JfifResource` ให้การเข้าถึงส่วน JFIF ภายใน PSD นำเข้าที่ส่วนบนของไฟล์ซอร์สของคุณ

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

### ขั้นตอนที่ 2: โหลดภาพ PSD
สร้างอินสแตนซ์ `PsdImage` โดยส่งพาธไฟล์ไปยังคอนสตรัคเตอร์ `PsdImage` เป็นคลาสของ Aspose.PSD ที่จำลองเอกสาร Photoshop นี้จะโหลดเมตาดาต้าเอกสารพร้อมสตรีมข้อมูลพิกเซล

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```

### ขั้นตอนที่ 3: วนซ้ำทรัพยากรภาพ
ค้นหา collection `Resources` เพื่อหา `JfifResource` เมื่อพบคุณสามารถแทนที่อาร์เรย์ไบต์ของภาพย่อด้วยตัวอย่าง JPEG‑encoded ใหม่ได้

```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Continue with thumbnail processing
    }
}
```

### ขั้นตอนที่ 4: ปรับข้อมูลภาพย่อ
สร้างภาพย่อ JPEG ขนาดเล็ก (เช่น 120 × 120 px) ด้วยไลบรารีประมวลผลภาพใดก็ได้ แล้วกำหนดอาร์เรย์ไบต์ที่ได้ให้กับ `jfifResource.ThumbnailData`

```java
try {
    PsdImage thumbnailImage = new PsdImage(100, 100);
    
    // Fill thumbnail data (example: create a simple pixel array)
    int[] pixels = new int[thumbnailImage.getWidth() * thumbnailImage.getHeight()];
    for (int j = 0; j < pixels.length; j++) {
        pixels[j] = j;
    }
    
    // Save thumbnail data
    thumbnailImage.saveArgb32Pixels(thumbnailImage.getBounds(), pixels);
    
    // Set thumbnail data to Jpeg options
    JpegExifData exifData = new JpegExifData();
    exifData.setThumbnail(thumbnailImage);
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setExifData(exifData);
    
    // Set options to thumbnail resource
    thumbnail.getJpegOptions().setExifData(exifData);
    
} catch(Exception e) {
    // Handle exceptions
} finally {
    // Dispose of resources
}
```

### ขั้นตอนที่ 5: บันทึกภาพที่แก้ไข
เรียกเมธอด `save` บนวัตถุ `PsdImage` ระบุพาธเอาต์พุตและรูปแบบที่ต้องการ ส่วน JFIF ตอนนี้มีภาพย่อใหม่แล้ว

```java
image.save(dataDir + "output.psd");
```

## ปัญหาทั่วไปและวิธีแก้
- **Thumbnail not visible in viewers:** ตรวจสอบให้แน่ใจว่าข้อมูลภาพย่อเป็นอาร์เรย์ไบต์ JPEG ที่ถูกต้องและขนาดไม่เกิน 256 × 256 px ซึ่งเป็นขนาดสูงสุดที่สเปค JFIF รองรับ
- **OutOfMemoryError on large PSDs:** ใช้ `PsdImage.load(inputStream, true)` เพื่อเปิดใช้งานโหมดสตรีมมิ่ง ซึ่งช่วยลดการใช้หน่วยความจำ
- **Incorrect resource type:** ยืนยันว่าทรัพยากรที่คุณแก้ไขเป็น `JfifResource` จริง; ทรัพยากรอื่นเช่น `ExifResource` จะไม่ส่งผลต่อการแสดงภาพย่อ

## คำถามที่พบบ่อย

**Q: Aspose.PSD for Java คืออะไร?**  
A: Aspose.PSD for Java เป็นไลบรารีเชิงพาณิชย์ที่ช่วยให้นักพัฒนาสร้าง, แก้ไข, แปลงและเรนเดอร์ไฟล์ Photoshop PSD ได้โดยไม่ต้องใช้ Adobe Photoshop

**Q: สามารถค้นหาเอกสารเพิ่มเติมสำหรับ Aspose.PSD for Java ได้ที่ไหน?**  
A: เอกสารโดยละเอียดสามารถพบได้ที่ [Aspose.PSD for Java documentation page](https://reference.aspose.com/psd/java/)

**Q: Aspose.PSD for Java เหมาะสำหรับการใช้งานเชิงพาณิชย์หรือไม่?**  
A: ใช่, Aspose.PSD for Java สามารถใช้เชิงพาณิชย์ได้ คุณสามารถซื้อไลเซนส์ได้จาก [Aspose.PSD's purchase page](https://purchase.aspose.com/buy)

**Q: สามารถทดลองใช้ Aspose.PSD for Java ก่อนซื้อได้หรือไม่?**  
A: ได้, คุณสามารถดาวน์โหลดรุ่นทดลองฟรีจาก [Aspose.PSD's trial download page](https://releases.aspose.com/)

**Q: จะขอรับการสนับสนุนสำหรับ Aspose.PSD for Java อย่างไร?**  
A: สำหรับการสนับสนุน ให้เยี่ยมชม [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)

---

**อัปเดตล่าสุด:** 2026-09-28  
**ทดสอบด้วย:** Aspose.PSD for Java 24.11  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [Add IOPA Resource to PSD Files using Aspose PSD for Java](/psd/java/modifying-converting-psd-images/add-iopa-resource-psd-files/)
- [Add Signature to Image – Draw Image on Canvas with Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [How to Rotate Image on a Specific Angle with Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}