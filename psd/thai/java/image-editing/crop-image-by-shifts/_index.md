---
date: 2026-01-01
description: เชี่ยวชาญการประมวลผลภาพด้วย Java โดยเรียนรู้วิธีการตัดภาพด้วย Aspose.PSD
  สำหรับ Java. บทเรียนที่ครอบคลุมเพื่อการจัดการภาพอย่างราบรื่น.
linktitle: Crop Image by Shifts
second_title: Aspose.PSD Java API
title: การประมวลผลภาพด้วย Java – การครอบภาพโดยการเลื่อนด้วย Aspose.PSD
url: /th/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การประมวลผลภาพ Java – การตัดภาพโดยการเลื่อนด้วย Aspose.PSD

## บทนำ

หากคุณกำลังทำงานกับ **java image processing** คุณจะพบว่า การตัดภาพอย่างแม่นยำเป็นพื้นฐานสำคัญสำหรับกระบวนการกราฟิกใด ๆ ไม่ว่าจะต้องการตัดขอบ, ลบพื้นหลังที่ไม่ต้องการ, หรือเตรียมทรัพยากรสำหรับการส่งบนเว็บ การรู้ **how to crop image** ด้วยโปรแกรมช่วยประหยัดเวลามนุษย์เป็นจำนวนมาก ในบทเรียนนี้เราจะอธิบายวิธีการตัดภาพแรสเตอร์โดยระบุค่าการเลื่อนสำหรับแต่ละด้าน ด้วยไลบรารี **Aspose.PSD for Java** ที่ทรงพลัง เมื่อจบคุณจะสามารถ **use the crop method** ได้อย่างมั่นใจและแม้กระทั่ง **optimize image cropping** เพื่อประสิทธิภาพที่ดียิ่งขึ้น

## คำตอบอย่างรวดเร็ว
- **ไลบรารีใดที่จัดการการประมวลผลภาพ java?** Aspose.PSD for Java  
- **เมธอดใดที่ใช้ตัดภาพแรสเตอร์?** `RasterImage.crop(left, right, top, bottom)`  
- **ต้องแคชข้อมูลก่อนหรือไม่?** ใช่ – การแคชช่วยเพิ่มความเร็วสำหรับไฟล์ PSD ขนาดใหญ่  
- **สามารถตั้งค่าขอบเขตการตัดแบบกำหนดเองได้หรือไม่?** แน่นอน – ระบุการเลื่อน left, right, top, และ bottom  
- **รูปแบบไฟล์เอาต์พุตที่รองรับมีอะไรบ้าง?** JPEG, PNG, BMP, และอื่น ๆ อีกหลายรูปแบบผ่าน `ImageOptions`

## Java image processing คืออะไร?
Java image processing หมายถึงการจัดการกราฟิกบิตแมพและเวกเตอร์โดยใช้ API ที่พัฒนาด้วย Java งานต่าง ๆ รวมถึงการปรับขนาด, การกรอง, การแปลงรูปแบบ, และการปรับ **image cropping margins** ทั้งหมดนี้สามารถทำอัตโนมัติในแอปพลิเคชันฝั่งเซิร์ฟเวอร์หรือเดสก์ท็อปได้

## ทำไมต้องใช้ Aspose.PSD สำหรับการประมวลผลภาพ java?
Aspose.PSD ให้โซลูชันแบบ pure‑Java ที่เข้าใจไฟล์ PSD ที่เข้ากันได้กับ Photoshop, ชั้น, ช่องสี, และมาสก์ มันขจัดความจำเป็นในการใช้ไลบรารีเนทีฟ ทำงานข้ามแพลตฟอร์ม และมี API **crop raster image** ที่เรียบง่ายและผสานรวมกับโปรเจกต์ Java ได้อย่างราบรื่น

## ข้อกำหนดเบื้องต้น

- **Java Development Kit (JDK)** – ดาวน์โหลดเวอร์ชันล่าสุดจาก [here](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Aspose.PSD for Java Library** – รับรุ่นใหม่ที่สุดจาก [download page](https://releases.aspose.com/psd/java/).  
- **Integrated Development Environment (IDE)** – Eclipse, IntelliJ IDEA, หรือโปรแกรมแก้ไขใด ๆ ที่คุณชอบ

## นำเข้าแพ็กเกจ

ในโปรเจกต์ Java ของคุณ ให้นำเข้าคลาสที่จำเป็นเพื่อเริ่มกระบวนการตัดภาพ:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: โหลดภาพ (how to crop image)

แรกเริ่มให้โหลดไฟล์ PSD ต้นฉบับเข้าสู่อินสแตนซ์ `RasterImage` ซึ่งจะให้การเข้าถึงระดับพิกเซลโดยตรง

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### ขั้นตอนที่ 2: แคชข้อมูลภาพ (optimize image cropping)

การแคชข้อมูลภาพในหน่วยความจำช่วยลดภาระ I/O เมื่อทำหลาย ๆ การดำเนินการเช่นการตัดภาพ

```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### ขั้นตอนที่ 3: กำหนดขอบเขตการตัดภาพ (image cropping margins)

ระบุจำนวนพิกเซลที่ต้องการตัดออกจากแต่ละด้าน ปรับค่าตาม **image cropping margins** ที่คุณต้องการ

```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### ขั้นตอนที่ 4: ใช้การตัด (use crop method)

จากนั้นเรียกเมธอด `crop` พร้อมค่าการเลื่อน การดำเนินการ **crop raster image** นี้จะเปลี่ยนแปลงบิตแมพพื้นฐาน

```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

### ขั้นตอนที่ 5: บันทึกผลลัพธ์ (how to crop image to a new format)

สุดท้ายให้เขียนภาพที่ถูกตัดลงดิสก์ ตัวอย่างนี้ใช้ JPEG แต่คุณสามารถใช้รูปแบบใดก็ได้ที่ Aspose.PSD รองรับ

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

ขอแสดงความยินดี! คุณได้ **cropped an image by shifts** ด้วย Aspose.PSD for Java สำเร็จแล้ว ซึ่งเป็นทักษะสำคัญในชุดเครื่องมือ **java image processing** ใด ๆ

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | วิธีแก้ |
|-------|----------|
| **`OutOfMemoryError` on large PSD files** | ตรวจสอบให้แน่ใจว่าคุณเรียก `cacheData()` (ขั้นตอน 2) และพิจารณาเพิ่มขนาด heap ของ JVM (`-Xmx`). |
| **Unexpected transparent borders** | ตรวจสอบว่าค่าการเลื่อนของคุณสอดคล้องกับขอบเขตที่ต้องการ; ค่าลบอาจทำให้ขยายแทนการตัด. |
| **Saving in the wrong format** | ใช้คลาสย่อย `ImageOptions` ที่เหมาะสม (เช่น `PngOptions`) เมื่อเรียก `save`. |

## คำถามที่พบบ่อย

**Q: Aspose.PSD รองรับรูปแบบภาพทั้งหมดหรือไม่?**  
A: ใช่, Aspose.PSD รองรับรูปแบบแรสเตอร์และเวกเตอร์หลากหลาย ทำให้คุณมีความยืดหยุ่นในโครงการของคุณ

**Q: สามารถทำการตัดหลายครั้งบนภาพเดียวกันได้หรือไม่?**  
A: แน่นอน คุณสามารถเรียก `crop` ซ้ำได้; แต่ละครั้งจะทำงานบนสถานะปัจจุบันของภาพ

**Q: มีฟอรั่มชุมชนสำหรับการสนับสนุน Aspose.PSD หรือไม่?**  
A: มี, คุณสามารถหาการสนับสนุนและเข้าร่วมชุมชนได้ที่ [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34)

**Q: จะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร?**  
A: เยี่ยมชม [here](https://purchase.aspose.com/temporary-license/) เพื่อรับใบอนุญาตชั่วคราว

**Q: มีตัวอย่างโปรเจกต์ที่แสดงการทำงานของ Aspose.PSD หรือไม่?**  
A: สำรวจเอกสารและตัวอย่างได้ที่ [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/)

## สรุป

ในคู่มือนี้เราได้ครอบคลุมทุกอย่างที่คุณต้องรู้เพื่อ **crop raster image** ด้วยการระบุค่าการเลื่อน ซึ่งเป็นเทคนิคที่จำเป็นสำหรับ **java image processing** ที่ละเอียดอ่อน ตอนนี้คุณมีพื้นฐานที่มั่นคงเพื่อผสานการตัดภาพเข้ากับกระบวนการทำงานที่ใหญ่ขึ้น ไม่ว่าจะเป็นการเตรียมทรัพยากรสำหรับเว็บ, การสร้างภาพย่อ, หรือการทำความสะอาดเอกสารสแกน

---

**Last Updated:** 2026-01-01  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}