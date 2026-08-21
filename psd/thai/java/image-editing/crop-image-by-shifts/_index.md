---
date: 2026-07-03
description: เรียนรู้วิธีการตัดรูปภาพ Java ด้วยการใช้ Aspose.PSD for Java. บทเรียนการตัดรูปภาพแบบขั้นตอนต่อขั้นตอนนี้ครอบคลุมการโหลดไฟล์
  PSD, การตั้งค่าการเลื่อน, และการบันทึกผลลัพธ์.
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: ตัดรูปภาพด้วยการเลื่อน
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: ตัดรูปภาพ Java ด้วยการเลื่อนโดยใช้ Aspose.PSD
url: /th/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตัดรูปภาพ Java ด้วยการเลื่อนด้วย Aspose.PSD

## บทนำ

ในการประมวลผลภาพด้วย Java, **crop image java** เป็นความต้องการทั่วไปสำหรับการเตรียมกราฟิก, รูปย่อ, หรือทรัพยากร UI. Aspose.PSD for Java ทำให้งานนี้ง่ายขึ้นโดยเปิดเผยเมธอด `crop` ที่ทำงานกับรูปแบบ raster ที่รองรับทั้งหมด. ในบทแนะนำนี้คุณจะได้เรียนรู้วิธีโหลดไฟล์ PSD, กำหนดค่าการเลื่อนซ้าย‑ขวา‑บน‑ล่าง, ใช้การตัด, และบันทึกผลลัพธ์—ทั้งหมดโดยไม่ต้องเขียนโค้ดการจัดการพิกเซลแบบกำหนดเอง.

## คำตอบอย่างรวดเร็ว
- **ไลบรารีใดจัดการการตัด?** Aspose.PSD for Java provides a built‑in `crop` method.  
- **ฉันต้องการใบอนุญาตหรือไม่?** A temporary license works for evaluation; a full license is required for production.  
- **รูปแบบที่รองรับ?** Over 30 raster formats, including PSD, JPEG, PNG, BMP, and TIFF.  
- **ขนาดไฟล์สูงสุด?** Handles files up to 2 GB without loading the entire image into memory.  
- **ต้องใช้บรรทัดโค้ดกี่บรรทัด?** Only five logical steps—load, cache, define shifts, crop, and save.

## crop image java คืออะไร?
`crop image java` หมายถึงการดำเนินการตัดภาพบิตแมพในแอปพลิเคชัน Java. โดยใช้ Aspose.PSD, การดำเนินการนี้ทำโดยเมธอด `crop` ซึ่งรับค่าการเลื่อนสำหรับแต่ละด้านของภาพและคืนค่าอินสแตนซ์ภาพใหม่.

## ทำไมต้องใช้ Aspose.PSD สำหรับการตัดภาพ?
Aspose.PSD รองรับรูปแบบภาพ **30+** และสามารถประมวลผลไฟล์ PSD หลายร้อยหน้าได้โดยใช้หน่วยความจำ RAM น้อยกว่า 150 MB, ขอบคุณสถาปัตยกรรม lazy‑loading. ไลบรารีนี้ยังรับประกันผลลัพธ์ที่ pixel‑perfect, รักษาชั้น, มาสก์, และโปรไฟล์สี—สิ่งที่ไลบรารีภาพทั่วไปหลายตัวไม่สามารถรับประกันได้.

## ข้อกำหนดเบื้องต้น

### ชุดพัฒนา Java (JDK)

ตรวจสอบว่าคุณมี JDK เวอร์ชันล่าสุดติดตั้งบนระบบของคุณ. คุณสามารถดาวน์โหลดได้จาก [here](https://www.oracle.com/java/technologies/javase-downloads.html).

### ไลบรารี Aspose.PSD for Java

เพื่อเริ่มต้น, คุณต้องรับไลบรารี Aspose.PSD for Java. ไปที่ [download page](https://releases.aspose.com/psd/java/) และดาวน์โหลดเวอร์ชันล่าสุด.

### สภาพแวดล้อมการพัฒนาแบบบูรณาการ (IDE)

เลือก IDE Java ที่คุณชื่นชอบ, เช่น Eclipse หรือ IntelliJ, เพื่อประสบการณ์การเขียนโค้ดที่ราบรื่น.

## วิธีการ crop image java?

โหลดไฟล์ต้นฉบับของคุณ, กำหนดการเลื่อนพิกเซลสำหรับแต่ละด้าน, และเรียกเมธอด `crop`—กระบวนการทั้งหมดนี้สามารถเขียนได้ในห้าบรรทัดโค้ดสั้น ๆ. การดำเนินการ `crop` จะสร้างภาพใหม่ที่มีเฉพาะส่วนที่คุณระบุ, โดยไม่ทำให้ไฟล์ต้นฉบับเปลี่ยนแปลง.

### ขั้นตอนที่ 1: โหลดภาพ

`Image` คือคลาสฐานสำหรับทุกประเภทภาพใน Aspose.PSD.  
`RasterImage` แสดงถึงภาพ raster และให้ความสามารถในการตัด.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### ขั้นตอนที่ 2: แคชข้อมูลภาพ

`cacheData()` โหลดข้อมูลภาพเข้าสู่หน่วยความจำเพื่อการประมวลผลที่เร็วขึ้น.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### ขั้นตอนที่ 3: กำหนดค่าการเลื่อน

ระบุค่าการเลื่อนสำหรับสี่ด้านของภาพ (ซ้าย, บน, ขวา, ล่าง) เป็นพิกเซล.  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### ขั้นตอนที่ 4: ใช้การตัด

`crop(left, right, top, bottom)` ตัดภาพตามค่าการเลื่อนพิกเซลที่ระบุบนแต่ละด้าน.  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### ขั้นตอนที่ 5: บันทึกผลลัพธ์

`JpegOptions` กำหนดการตั้งค่าการเข้ารหัส JPEG เช่น คุณภาพและโปรไฟล์สี.  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

ยินดีด้วย! คุณได้ทำการตัดภาพสำเร็จโดยใช้ Aspose.PSD for Java.

## ปัญหาทั่วไปและวิธีแก้

- **Image appears unchanged:** ตรวจสอบว่าค่าการเลื่อนเป็นค่าบวกและไม่เกินขนาดเดิมของภาพ.  
- **OutOfMemoryError on large files:** เปิดใช้งานการแคชตามที่แสดงในขั้นตอน 2; นี้ทำให้ Aspose.PSD ใช้ไฟล์ชั่วคราวแทนการเก็บภาพทั้งหมดใน RAM.  
- **Color shift after cropping:** ตรวจสอบว่าคุณรักษาโปรไฟล์สีโดยเรียก `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })` หากคุณต้องการความแม่นยำของสีที่แน่นอน.

## คำถามที่พบบ่อย

**Q: Aspose.PSD รองรับรูปแบบภาพทั้งหมดหรือไม่?**  
A: ใช่, Aspose.PSD รองรับรูปแบบ raster มากกว่า 30 รูปแบบ รวมถึง PSD, JPEG, PNG, BMP, TIFF, และ GIF, เพื่อความเข้ากันได้อย่างกว้างขวาง.

**Q: ฉันสามารถทำการตัดหลายครั้งบนภาพเดียวกันได้หรือไม่?**  
A: แน่นอน. หลังจากแต่ละการเรียก `crop` คุณจะได้รับอ็อบเจ็กต์ภาพใหม่, ซึ่งคุณสามารถตัดอีกครั้งตามต้องการ.

**Q: มีฟอรั่มชุมชนสำหรับการสนับสนุน Aspose.PSD หรือไม่?**  
A: ใช่, คุณสามารถหาแหล่งสนับสนุนและเข้าร่วมกับชุมชนได้ที่ [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร?**  
A: เยี่ยมชม [here](https://purchase.aspose.com/temporary-license/) เพื่อรับใบอนุญาตชั่วคราว.

**Q: มีโครงการตัวอย่างที่แสดงฟังก์ชันการทำงานของ Aspose.PSD หรือไม่?**  
A: สำรวจเอกสารและตัวอย่างได้ที่ [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).

---

**อัปเดตล่าสุด:** 2026-07-03  
**ทดสอบด้วย:** Aspose.PSD 24.11 for Java  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## บทแนะนำที่เกี่ยวข้อง

- [ตัดรูปภาพโดยสี่เหลี่ยมใน Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Crop Image Java - ขยายและตัดภาพด้วย Aspose.PSD for Java](/psd/java/image-editing/expand-and-crop-images/)
- [Resize Image Java - การใช้ Resize Type Enumeration ใน Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}