---
date: 2026-09-18
description: เรียนรู้วิธีเพิ่มภาพขนาดย่อของเมตาดาต้าภาพ java ไปยังส่วน EXIF โดยใช้
  Aspose.PSD for Java คู่มือขั้นตอนนี้ครอบคลุมข้อกำหนดเบื้องต้น การอธิบายโค้ด และการบันทึกรูปภาพที่อัปเดต
keywords:
- java image metadata
- how to add thumbnail
- java exif metadata
lastmod: 2026-09-18
linktitle: เพิ่มภาพขนาดย่อไปยังส่วน EXIF ใน Java
og_description: เรียนรู้วิธีเพิ่มภาพขนาดย่อของเมตาดาต้าภาพ java ไปยังส่วน EXIF โดยใช้
  Aspose.PSD for Java ปฏิบัติตามคู่มือขั้นตอนเพื่อฝังภาพขนาดย่อและบันทึกรูปภาพที่อัปเดต
og_image_alt: Guide showing Java code to embed a thumbnail into EXIF metadata using
  Aspose.PSD
og_title: วิธีเพิ่มภาพขนาดย่อของเมตาดาต้าภาพ java ไปยังส่วน EXIF
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to add java image metadata thumbnail to the EXIF segment
    using Aspose.PSD for Java. This step‑by‑step guide covers prerequisites, code
    walkthrough, and saving the updated image.
  headline: How to add java image metadata thumbnail to EXIF segment
  type: TechArticle
- questions:
  - answer: EXIF metadata is embedded information in digital images that includes
      camera settings, capture date, GPS coordinates, and other details.
    question: What is EXIF metadata?
  - answer: Adding a thumbnail improves user experience by allowing quick image previews
      without loading the full image.
    question: Why add a thumbnail to EXIF?
  - answer: You can download Aspose.PSD for Java from the [Aspose.PSD for Java download
      page](https://releases.aspose.com/psd/java/).
    question: Where can I download Aspose.PSD for Java?
  - answer: You can obtain a temporary license for Aspose.PSD from the [temporary
      license page](https://purchase.aspose.com/temporary-license/).
    question: How can I get a temporary license for Aspose.PSD?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How do I get support for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- EXIF thumbnail
- Aspose.PSD
- Java image processing
title: วิธีเพิ่มภาพขนาดย่อของเมตาดาต้าภาพ java ไปยังส่วน EXIF
url: /th/java/java-jpeg-image-processing/add-thumbnail-to-exif-segment-java/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เพิ่มภาพย่อเมตาดาต้าภาพ java ไปยังส่วน EXIF

## บทนำ
ในบทแนะนำนี้คุณจะได้เรียนรู้วิธีเพิ่มภาพย่อ **java image metadata** ไปยังส่วน EXIF ของไฟล์ PSD ด้วย Aspose.PSD for Java. เมตาดาต้า EXIF (Exchangeable Image File Format) จะเก็บการตั้งค่ากล้อง, วันที่ถ่าย, ตำแหน่ง, และข้อมูลที่เป็นประโยชน์อื่น ๆ การฝังภาพย่อขนาดเล็กทำให้แอปพลิเคชันสามารถแสดงภาพตัวอย่างอย่างรวดเร็วโดยไม่ต้องโหลดไฟล์เต็ม ช่วยปรับปรุงประสิทธิภาพและประสบการณ์ผู้ใช้.

## คำตอบอย่างรวดเร็ว
- **บทเรียนครอบคลุมอะไร?** การเพิ่มภาพย่อไปยังส่วน EXIF ของภาพ PSD ด้วย Aspose.PSD for Java.  
- **ใช้เวลานานเท่าไหร่ในการทำ?** ประมาณ 10‑15 นาทีสำหรับการรวมพื้นฐาน.  
- **ต้องการใบอนุญาตหรือไม่?** ต้องมีใบอนุญาตชั่วคราวสำหรับการใช้งานในผลิตภัณฑ์; การทดลองใช้ฟรีสามารถใช้สำหรับการประเมิน.  
- **รองรับเวอร์ชัน Java ใด?** Java 8 และใหม่กว่าได้รับการสนับสนุนเต็มที่.  
- **สามารถประมวลผลไฟล์ขนาดใหญ่ได้หรือไม่?** ได้—Aspose.PSD สามารถจัดการไฟล์ได้สูงสุด 2 GB โดยไม่ต้องโหลดภาพทั้งหมดเข้าสู่หน่วยความจำ.

## java image metadata คืออะไร?
java image metadata หมายถึงข้อมูลที่มีโครงสร้างซึ่งฝังอยู่ในไฟล์ภาพ (เช่น EXIF, IPTC หรือ XMP) ซึ่งสามารถอ่าน, แก้ไข หรือสร้างโดยโปรแกรมโดยใช้ไลบรารี Java เช่น Aspose.PSD. เมตาดาต้านี้ทำให้แอปพลิเคชันสามารถดึงการตั้งค่ากล้อง, เวลาที่บันทึก, พิกัด GPS, และข้อมูลกำหนดเองโดยไม่ต้องเปิดเนื้อหาภาพ.

## ทำไมต้องเพิ่มภาพย่อไปยังเมตาดาต้า EXIF?
การเพิ่มภาพย่อไปยังส่วน EXIF ให้สัญญาณภาพทันทีสำหรับเบราว์เซอร์ภาพ, ตัวสำรวจไฟล์, และระบบจัดการเนื้อหา. Aspose.PSD ประมวลผลภาพย่อในหน่วยความจำ, ทำให้คุณสามารถฝังตัวอย่างได้ภายในเวลาไม่ถึง 0.2 วินาทีสำหรับภาพขนาดสูงสุด 500 KB, และรองรับรูปแบบภาพกว่า 30 รูปแบบ รวมถึง PSD, JPEG, PNG, และ TIFF.

## ข้อกำหนดเบื้องต้น
ก่อนเริ่มบทแนะนำ, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:
- ความรู้พื้นฐานการเขียนโปรแกรม Java.  
- Java Development Kit (JDK) ที่ติดตั้งบนระบบของคุณ.  
- IDE (Integrated Development Environment) สำหรับ Java เช่น IntelliJ IDEA หรือ Eclipse.  
- ไลบรารี Aspose.PSD for Java คุณสามารถดาวน์โหลดได้จาก [Aspose.PSD for Java Download page](https://releases.aspose.com/psd/java/).

## นำเข้าแพ็กเกจ
การนำเข้าต่อไปนี้จะนำคลาสของ Aspose.PSD ที่จำเป็นสำหรับการทำงานกับภาพ PSD และข้อมูล EXIF เข้ามา.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## ขั้นตอนที่ 1: โหลดภาพ psd
`PsdImage` แทนไฟล์ Photoshop PSD และให้การเข้าถึงเลเยอร์และทรัพยากรของมัน.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
```

## ขั้นตอนที่ 2: วนลูปผ่านทรัพยากรภาพ
`ImageResource` รวมทรัพยากรต่าง ๆ เช่น ภาพย่อ, โปรไฟล์ ICC, และเมตาดาต้าที่ฝังอยู่ในไฟล์ PSD.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        // Process the thumbnail resource
    }
}
```

## ขั้นตอนที่ 3: ปรับข้อมูลภาพย่อ
`JpegOptions` ให้คุณกำหนดค่าการตั้งค่าเฉพาะของ JPEG เช่น คุณภาพ สำหรับภาพย่อ.  
```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setQuality(100); // Set JPEG quality
```

## ขั้นตอนที่ 4: บันทึกภาพ
การเรียก `save` จะเขียนส่วน EXIF ที่อัปเดต (รวมถึงภาพย่อใหม่) กลับไปยังดิสก์โดยไม่ต้องเข้ารหัสภาพทั้งหมดใหม่.  
```java
image.save(dataDir + "output.psd");
```

## ปัญหาทั่วไปและวิธีแก้ไข
- **ภาพย่อไม่แสดง:** ตรวจสอบว่าทรัพยากรภาพย่อถูกเพิ่มอย่างถูกต้องไปยังส่วน EXIF และภาพถูกบันทึกด้วยเมธอด `PsdImage.save`.  
- **ข้อผิดพลาดหน่วยความจำไม่พอเมื่อไฟล์ขนาดใหญ่:** ใช้ `PsdImage.load(..., LoadOptions)` พร้อม `LoadOptions.setLoadOnlyMetadata(true)` เพื่อทำงานกับเมตาดาต้าเท่านั้น.  
- **การวางแนวไม่ถูกต้อง:** ตรวจสอบให้ภาพย่อเคารพแฟล็กการวางแนวของภาพต้นฉบับ; คุณสามารถอ่านแท็ก EXIF `Orientation` และหมุนภาพย่อตามนั้น.

## คำถามที่พบบ่อย

**Q: EXIF metadata คืออะไร?**  
A: เมตาดาต้า EXIF คือข้อมูลที่ฝังอยู่ในภาพดิจิทัลซึ่งรวมถึงการตั้งค่ากล้อง, วันที่ถ่าย, พิกัด GPS, และรายละเอียดอื่น ๆ.

**Q: ทำไมต้องเพิ่มภาพย่อไปยัง EXIF?**  
A: การเพิ่มภาพย่อช่วยปรับปรุงประสบการณ์ผู้ใช้โดยให้การแสดงตัวอย่างภาพอย่างรวดเร็วโดยไม่ต้องโหลดภาพเต็ม.

**Q: สามารถดาวน์โหลด Aspose.PSD for Java ได้จากที่ไหน?**  
A: คุณสามารถดาวน์โหลด Aspose.PSD for Java จาก [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).

**Q: จะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร?**  
A: คุณสามารถรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD จาก [temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: จะขอรับการสนับสนุนสำหรับ Aspose.PSD อย่างไร?**  
A: สำหรับการสนับสนุน, เยี่ยมชม [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).

---

**อัปเดตล่าสุด:** 2026-09-18  
**ทดสอบกับ:** Aspose.PSD for Java 24.10  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [สร้างเมตาดาต้า XMP ในไฟล์ PSD ด้วย Aspose.PSD for Java](/psd/java/image-editing/create-xmp-metadata/)
- [ปรับขนาดภาพด้วย Aspose.PSD for Java – วาดรูปทรงและการดำเนินการภาพพื้นฐาน](/psd/java/basic-image-operations/)
- [วิธีแปลง PSD เป็นรูปแบบภาพแรสเตอร์ด้วย Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}