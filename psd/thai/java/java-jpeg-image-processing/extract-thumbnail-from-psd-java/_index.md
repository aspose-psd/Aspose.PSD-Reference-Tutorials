---
date: 2026-10-03
description: เรียนรู้วิธีดึงรูปย่อจากไฟล์ PSD ใน Java ด้วย Aspose.PSD คู่มือขั้นตอนนี้ครอบคลุมการตั้งค่า
  ตัวอย่างโค้ด และการบันทึกรูปย่อเป็นภาพ JPEG
keywords:
- extract thumbnail from psd
- java aspose psd
- psd thumbnail extraction
lastmod: 2026-10-03
linktitle: ดึงรูปย่อจากไฟล์ PSD ใน Java
og_description: เรียนรู้วิธีดึงรูปย่อจากไฟล์ PSD ใน Java ด้วย Aspose.PSD คู่มือนี้จะพาคุณผ่านการตั้งค่า
  การโหลดไฟล์ การดึงรูปย่อ และการบันทึกเป็นภาพ JPEG
og_image_alt: Screenshot showing Java code extracting a thumbnail from a PSD file
  using Aspose.PSD
og_title: ดึงรูปย่อจากไฟล์ PSD ใน Java ด้วย Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to extract thumbnail from PSD in Java using Aspose.PSD. This
    step‑by‑step guide covers setup, code snippets, and saving the thumbnail as a
    JPEG image.
  headline: Extract thumbnail from PSD in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is a Java library that enables programmatic creation, manipulation,
      and conversion of PSD and other raster image formats without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD?
  - answer: You can refer to the [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references and examples.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library’s capabilities.
    question: Can I try Aspose.PSD for free before purchasing?
  - answer: Temporary licenses are available from the [temporary license](https://purchase.aspose.com/temporary-license/)
      page.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Yes, Aspose.PSD can be used in both personal and commercial projects under
      its licensing terms.
    question: Is Aspose.PSD suitable for commercial use?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose.psd
- thumbnail extraction
title: ดึงรูปย่อจากไฟล์ PSD ใน Java
url: /th/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ดึงภาพย่อจากไฟล์ PSD ด้วย Java

## บทนำ
การดึงภาพย่อจากไฟล์ PSD ช่วยให้คุณสร้างภาพตัวอย่างอย่างรวดเร็วโดยไม่ต้องโหลดภาพความละเอียดเต็ม ใน Java, Aspose.PSD ทำให้กระบวนการนี้ง่ายและมีประสิทธิภาพ ในบทแนะนำนี้คุณจะได้เรียนรู้วิธีตั้งค่าห้องสมุด, ค้นหาแหล่งข้อมูลภาพย่อ, และบันทึกเป็นไฟล์ JPEG — ทั้งหมดด้วยเพียงไม่กี่บรรทัดของโค้ด

## คำตอบอย่างรวดเร็ว
- **ไลบรารีที่จัดการภาพย่อ PSD คืออะไร?** Aspose.PSD for Java.  
- **ต้องใช้กี่บรรทัดของโค้ด?** ประมาณห้าบรรทัดสำหรับการโหลด, ดึง, และบันทึก.  
- **ฉันสามารถดึงภาพย่อจากไฟล์ PSD ขนาดใหญ่ได้หรือไม่?** ได้, Aspose.PSD ประมวลผลไฟล์ขนาดสูงสุด 500 MB โดยไม่ต้องโหลดข้อมูลทั้งหมดเข้าสู่หน่วยความจำ.  
- **ต้องใช้ไลเซนส์สำหรับการพัฒนาหรือไม่?** สามารถใช้รุ่นทดลองฟรีสำหรับการประเมิน; จำเป็นต้องมีไลเซนส์สำหรับการใช้งานจริง.  
- **รูปแบบไฟล์ผลลัพธ์ที่รองรับคืออะไร?** ภาพย่อที่ดึงออกมาสามารถบันทึกเป็น JPEG, PNG หรือ BMP.  

## การดึงภาพย่อจาก PSD คืออะไร?
การดึงภาพย่อจาก PSD คือกระบวนการอ่านภาพตัวอย่างขนาดเล็กที่ฝังอยู่ภายในเอกสาร Photoshop (PSD) ตัวอย่างนี้ถูกจัดเก็บเป็นทรัพยากรและสามารถบันทึกแยกออกมาเพื่อการจัดทำแคตาล็อกหรือการแสดงผล ภาพย่อมักเป็นการแสดงผลความละเอียดต่ำที่แอปพลิเคชันใช้เพื่อแสดงสรุปภาพอย่างรวดเร็วโดยไม่ต้องโหลดภาพเต็มขนาด

## ทำไมต้องใช้ Aspose.PSD สำหรับงานนี้?
Aspose.PSD รองรับ **รูปแบบภาพกว่า 30 ประเภท** และสามารถจัดการไฟล์ PSD ขนาดถึง **500 MB** พร้อมรักษาการใช้หน่วยความจำน้อย เนื่องจากอ่านทรัพยากรตามความต้องการ API ยังให้การจัดการข้อผิดพลาดที่แข็งแรง ทำให้คุณสามารถดึงภาพย่อได้อย่างเชื่อถือแม้จากไฟล์ที่เสียหาย

## ข้อกำหนดเบื้องต้น
- ติดตั้ง Java Development Kit (JDK) แล้ว
- ดาวน์โหลดไลบรารี Aspose.PSD for Java จาก [Aspose.PSD for Java download](https://releases.aspose.com/psd/java/).
- มีความคุ้นเคยพื้นฐานกับไวยากรณ์ Java และการตั้งค่าโปรเจกต์

## วิธีดึงภาพย่อจากไฟล์ PSD ด้วย Java?
โหลดไฟล์ PSD ด้วย `PsdImage`, ค้นหา `ThumbnailResource`, และบันทึกข้อมูลภาพเป็น JPEG. Aspose.PSD ทำหน้าที่แยกการวิเคราะห์ระดับต่ำออก, ดังนั้นคุณเพียงเรียก `getResources()` แล้วตามด้วย `save()` บนภาพที่ดึงออก วิธีนี้ทำงานกับไฟล์ PSD ใด ๆ ที่มีภาพย่อ ไม่ว่าจะมีขนาดไฟล์เท่าใด

## นำเข้าแพ็กเกจ
`Image` is the base class for loading images. `PsdImage` represents a PSD document. `ThumbnailResource` and `Thumbnail4Resource` represent thumbnail resources. `JpegOptions` specifies JPEG save options.

```text
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
```

## ขั้นตอนที่ 1: โหลดไฟล์ PSD
ขั้นแรก, สร้างอินสแตนซ์ `PsdImage` ที่ชี้ไปยังไฟล์ PSD ของคุณ ตัวสร้างจะอ่านเฉพาะส่วนหัวและทรัพยากรที่จำเป็น ทำให้การใช้หน่วยความจำน้อยที่สุด

```text
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
```

Replace `"Your_Document_Directory/"` with the directory path where your PSD file is located, and `"your_file.psd"` with the name of your PSD file.

## ขั้นตอนที่ 2: วนลูปทรัพยากรภาพ
Aspose.PSD เก็บภาพย่อเป็นอ็อบเจ็กต์ `ThumbnailResource` ภายในคอลเลกชันทรัพยากรของภาพ. วนลูปผ่านคอลเลกชัน, ตรวจสอบประเภทของทรัพยากร, และจับภาพย่อแรกที่พบ

```text
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```
```

## ขั้นตอนที่ 3: บันทึกภาพย่อที่ดึงออกมา
เมื่อคุณมีภาพย่อแล้ว, เรียกเมธอด `save` ของมันเพื่อบันทึกลงดิสก์. คุณสามารถเลือก JPEG, PNG หรือ BMP; JPEG เป็นรูปแบบที่นิยมที่สุดสำหรับภาพตัวอย่างบนเว็บ

## ขั้นตอนที่ 4: จัดการกับประเภทภาพย่อที่แตกต่างกัน
หากไฟล์ PSD มีหลายรูปแบบของภาพย่อ, เช่น `Thumbnail4Resource`, ให้ขยายตรรกะการวนลูปเพื่อเช็คแต่ละประเภท. API มีคลาสแยกต่างหากสำหรับแต่ละทรัพยากร, ทำให้คุณเลือกความละเอียดที่ต้องการได้

## ปัญหาทั่วไปและวิธีแก้ไข
- **ไม่พบภาพย่อ:** ไม่ใช่ไฟล์ PSD ทุกไฟล์จะฝังตัวอย่าง. ตรวจสอบไฟล์ต้นทางใน Photoshop ที่เมนู “File → File Info”
- **ข้อผิดพลาดรูปแบบที่ไม่รองรับ:** ตรวจสอบว่าคุณใช้เวอร์ชันล่าสุดของ Aspose.PSD; รุ่นเก่าอาจไม่มีประเภททรัพยากรภาพย่อใหม่
- **หน่วยความจำเต็มเมื่อไฟล์ใหญ่:** ใช้ `PsdImage.load(..., LoadOptions)` พร้อม `LoadOptions.setLoadResourcesOnly(true)` เพื่อหลีกเลี่ยงการโหลดข้อมูลภาพเต็มเมื่อคุณต้องการเฉพาะภาพย่อ

## คำถามที่พบบ่อย

**Q: Aspose.PSD คืออะไร?**  
A: Aspose.PSD เป็นไลบรารี Java ที่ช่วยให้สามารถสร้าง, แก้ไข, และแปลงไฟล์ PSD และรูปแบบภาพราสเตอร์อื่น ๆ ได้โดยไม่ต้องใช้ Adobe Photoshop.

**Q: ฉันสามารถหาข้อมูลเอกสารเพิ่มเติมเกี่ยวกับ Aspose.PSD for Java ได้ที่ไหน?**  
A: คุณสามารถอ้างอิงที่ [documentation](https://reference.aspose.com/psd/java/) สำหรับรายละเอียด API และตัวอย่าง.

**Q: ฉันสามารถทดลองใช้ Aspose.PSD ฟรีก่อนซื้อได้หรือไม่?**  
A: ได้, คุณสามารถดาวน์โหลด [free trial](https://releases.aspose.com/) เพื่อประเมินความสามารถของไลบรารี.

**Q: ฉันจะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร?**  
A: ไลเซนส์ชั่วคราวมีให้ที่หน้า [temporary license](https://purchase.aspose.com/temporary-license/).

**Q: Aspose.PSD เหมาะสำหรับการใช้งานเชิงพาณิชย์หรือไม่?**  
A: ใช่, Aspose.PSD สามารถใช้ได้ทั้งในโครงการส่วนบุคคลและเชิงพาณิชย์ตามเงื่อนไขการให้ไลเซนส์.

---

**Last Updated:** 2026-10-03  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [วิธีแปลง PSD เป็นรูปแบบภาพราสเตอร์ด้วย Aspose.PSD for Java](/psd/java/advanced-techniques/convert-psd-to-raster-forms/)
- [บันทึก PSD เป็น JPEG และรองรับสี RGB ด้วย Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [ปรับขนาดภาพด้วย Aspose.PSD for Java – วาดรูปและการดำเนินการพื้นฐานของภาพ](/psd/java/basic-image-operations/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}