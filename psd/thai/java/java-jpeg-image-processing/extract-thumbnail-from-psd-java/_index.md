---
date: 2026-01-25
description: เรียนรู้วิธีดึงภาพย่อจากไฟล์ PSD ด้วย Aspose.PSD for Java. ทำตามคู่มือขั้นตอนต่อขั้นตอนนี้เพื่อโหลด
  ดึง และบันทึกภาพย่ออย่างรวดเร็ว.
linktitle: Extract Thumbnail from PSD in Java
second_title: Aspose.PSD Java API
title: สกัดรูปย่อจาก PSD ด้วย Java
url: /th/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ดึง Thumbnail จาก PSD ด้วย Java

## Introduction
ในบทเรียนนี้ คุณจะได้เรียนรู้ **วิธีดเล็กที่ฝังอยู่ในเอกสาร PSD และการดึงออกมาช่วยให้คุณสร้างตัวอย่างอย่างรวดเร็ว สร้างแกลเลอรีภาพ หรือประหยัดพื้นที่จัดเก็บเมื่อคุณต้องการเพียงภาพตัวแทนขนาดเล็กของงานต้นฉบับ เราจะเดินผ่านทุกขั้นตอนตั้งแต่การตั้งค่าโปรเจกต์จนถึงการบันทึก thumbnail ที่ดึงออกมาเป็นไฟล์ภาพมาตรฐาน

## Quick Answers
- **บทเรียนนี้ครอบคลุมอะไร?** การดึงและบันทึกภาพ thumbnail จากไฟล์ PSD ด้วย Aspose.PSD สำหรับ Java.  
- **ต้องใช้ไลบรารีอะไร?** Aspose.PSD สำหรับ Java (ดาวน์โหลดได้จากเว็บไซต์ทางการของ Aspose).  
- **ต้องมีลิขสิทธิ์หรือไม่?** จำเป็นต้องมีลิขสิทธิ์ชั่วคราวหรือเต็มสำหรับการใช้งานในผลิตภัณฑ์; มีรุ่นทดลองฟรีให้ใช้.  
- **รูปแบบผลลัพธ์ที่ใช้คืออะไร?** ตัวอย่างบันทึก thumbnail เป็นไฟล์ JPEG, แต่คุณสามารถเลือกใช้รูปแบบที่รองรับอื่นได้.  
- **ใช้เวลานานเท่าไหร่ในการทำงาน?** ประมาณ 5‑10 นาทีสำหรับนักพัฒนาที่คุ้นเคยกับแนวคิดพื้นฐานของ Java.

## What is “extract thumbnail from PSD”?
การดึง thumbnail จาก PSD หมายถึงการอ่านภาพตัวอย่างขนาดเล็กที่ Photoshop เก็บไว้ในส่วน resources ของไฟล์ ภาพตัวอย่างนี้มักเป็นเวอร์ชันความละเอียดต่ำของแคนวาสเต็มรูปแบบ ทำให้เหมาะสำหรับการโหลดอย่างรวดเร็วในตัวจัดการไฟล์หรือแกลเลอรีเว็บ

## Why extract thumbnails with Aspose.PSD?
- **Speed:** ไม่ต้องเปิด PSD เต็มรูปแบบในโปรแกรมแก้ไขกราฟิก; thumbnail มีอยู่แล้วในไฟล์.  
- **Automation:** เหมาะสำหรับการประมวลผลเป็นชุดของไลบรารีภาพขนาดใหญ่.  
- **Cross‑platform:** ทำงานบนระบบปฏิบัติการใดก็ได้ที่รองรับ Java, ไม่ต้องใช้ Photoshop.  
- **Format flexibility:** แปลง thumbnail เป็น JPEG, PNG, หรือรูปแบบใดก็ได้ที่ Aspose.PSD รองรับ.

## Prerequisites
ก่อนเริ่มทำงาน ตรวจสอบให้แน่ใจว่าคุณได้เตรียมสิ่งต่อไปนี้ไว้:
- Java Development Kit (JDK) ที่ติดตั้งบนระบบของคุณ.  
- ไลบรารี Aspose.PSD สำหรับ Java. คุณสามารถดาวน์โหลดได้จาก [here](https://releases.aspose.com/psd/java/).  
- ความรู้พื้นฐานด้านการเขียนโปรแกรม Java.

## Import Packages
เพื่อเริ่มต้น ให้รวมแพ็คเกจ Aspose.PSD ที่จำเป็นในคลาส Java ของคุณ:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```

## How to extract thumbnail from PSD using Aspose.PSD for Java
ด้านล่างเป็นคำแนะนำแบบขั้นตอนต่อขั้นตอน แต่ละขั้นตอนมีคำอธิบายสั้น ๆ ตามด้วยโค้ดที่ต้องคัดลอกใช้

### Step 1: Load the PSD File
แรกสุดให้โหลดไฟล์ PSD ที่มี thumbnail ที่คุณต้องการดึงออกมา
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
เปลี่ยน `"Your_Document_Directory/"` ให้เป็นพาธไดเรกทอรีที่เก็บไฟล์ PSD ของคุณ, และ `"your_file.psd"` ให้เป็นชื่อไฟล์ PSD ของคุณ

### Step 2: Iterate Over Image Resources
วนลูปผ่าน image resources เพื่อค้นหา resource ของ thumbnail
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

### Step 3: Save the Extracted Thumbnail
โค้ดในขั้นตอนก่อนหน้านี้ได้บันทึก thumbnail เป็นไฟล์ JPEG ชื่อ `extracted_thumbnail.jpg` ในไดเรกทอรีเดียวกันแล้ว คุณสามารถเปลี่ยนชื่อไฟล์หรือรูปแบบได้โดยปรับพารามิเตอร์ของเมธอด `save`

### Step 4: Handling Different Thumbnail Types
หากไฟล์ PSD ของคุณอาจมีหลายประเภทของ thumbnail เช่น `Thumbnail4Resource` คุณสามารถขยายตรรกะเพื่อจัดการกรณีนั้นได้โดยเพิ่มการตรวจสอบ `instanceof Thumbnail4Resource` ภายในลูปและประมวลผลด้วยรูปแบบเดียวกัน

## Common Issues and Solutions
- **ไม่พบ thumbnail:** ไม่ใช่ทุกไฟล์ PSD จะมี resource ของ thumbnail ตรวจสอบไฟล์ต้นฉบับใน Photoshop (File → Export → Thumbnail) หรือใช้ PSD ที่มีตัวอย่างภาพแนบ.  
- **เกิดข้อผิดพลาดรูปแบบภาพที่ไม่รองรับ:** ตรวจสอบว่าคุณใช้เวอร์ชันล่าสุดของ Aspose.PSD ที่รองรับรูปแบบเป้าหมาย.  
- **ข้อผิดพลาดการอนุญาตเมื่อบันทึก:** ยืนยันว่าแอปพลิเคชันมีสิทธิ์เขียนในไดเรกทอรีปลายทาง.

## Frequently Asked Questions

**Q: Aspose.PSD คืออะไร?**  
A: Aspose.PSD เป็นไลบรารี Java ที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ PSD และรูปแบบภาพอื่น ๆ ได้โดยโปรแกรมมิ่ง

**Q: จะหาเอกสารเพิ่มเติมเกี่ยวกับ Aspose.PSD สำหรับ Java ได้จากที่ไหน?**  
A: คุณสามารถอ้างอิง [documentation](https://reference.aspose.com/psd/java/) เพื่อดูรายละเอียด API และตัวอย่างต่าง ๆ

**Q: สามารถทดลองใช้ Aspose.PSD ฟรีก่อนซื้อได้หรือไม่?**  
A: ได้, คุณสามารถดาวน์โหลด [free trial](https://releases.aspose.com/) เพื่อประเมินความสามารถของไลบรารี

**Q: จะขอรับลิขสิทธิ์ชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร?**  
A: สามารถขอรับลิขสิทธิ์ชั่วคราวได้จาก [here](https://purchase.aspose.com/temporary-license/)

**Q: Aspose.PSD เหมาะกับการใช้งานเชิงพาณิชย์หรือไม่?**  
A: ใช่, Aspose.PSD สามารถใช้ได้ทั้งในโครงการส่วนบุคคลและเชิงพาณิชย์ตามเงื่อนไขการให้ลิขสิทธิ์

## Conclusion
ในบทเรียนนี้ เราได้สำรวจวิธี **ดึง thumbnail จากไฟล์ PSD** ด้วย Aspose.PSD สำหรับ Java โดยทำตามขั้นตอนที่อธิบายไว้ด้านบน คุณจะสามารถดึงและบันทึก thumbnail ที่ฝังอยู่ในเอกสาร PSD ของคุณได้อย่างมีประสิทธิภาพ ทำให้การแสดงตัวอย่างเร็วขึ้นและกระบวนการทำงานกับภาพเป็นไปอย่างราบรื่น

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-25  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose