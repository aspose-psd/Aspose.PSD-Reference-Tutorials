---
date: 2026-02-12
description: เรียนรู้วิธีการหมุนภาพและวิธีการหมุนภาพ 270 องศาโดยใช้ Aspose.PSD สำหรับ
  Java คู่มือนี้ครอบคลุมการหมุนไฟล์ PSD, การพลิกภาพ, และการแปลง PSD เป็น JPEG โดยไม่ต้องใช้
  Photoshop.
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
title: วิธีหมุนภาพ 270 องศาด้วย Aspose.PSD สำหรับ Java
url: /th/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# หมุนภาพ 270 องศาด้วย Aspose.PSD for Java

## บทนำ

ใน **java image processing tutorial** นี้ คุณจะได้ค้นพบ **how to rotate image** 270 degrees อย่างรวดเร็วและเชื่อถือได้โดยใช้ Aspose.PSD for Java ไม่ว่าคุณจะกำลังสร้างเครื่องมือแก้ไขภาพ, ทำการแปลงเป็นชุดอัตโนมัติ, หรือเพียงต้องการปรับทิศทางของเลเยอร์ PSD ไลบรารีทำให้การทำงานนี้ง่ายดาย เราจะกล่าวถึงเทคนิค **flip image java** และการแปลง PSD ที่หมุนแล้วเป็น JPEG เพื่อให้คุณได้กระบวนการทำงานแบบครบวงจรโดยไม่ต้องใช้ Photoshop.

## คำตอบอย่างรวดเร็ว
- **ไลบรารีใดที่จัดการการหมุน?** Aspose.PSD for Java  
- **มุมการหมุนที่ตัวอย่างใช้คืออะไร?** 270 degrees  
- **ฉันสามารถพลิกภาพได้หรือไม่?** Yes – use `RotateFlipType` options like `Rotate90FlipX`  
- **ฉันจะบันทึกผลลัพธ์อย่างไร?** In the example we save as JPEG using `JpegOptions`  
- **ฉันต้องการไลเซนส์สำหรับการใช้งานในเชิงพาณิชย์หรือไม่?** A valid Aspose.PSD license is required for commercial use  

## “rotate image 270 degrees” คืออะไร?
การหมุนภาพ 270 degrees หมายถึงการหมุนรูปภาพเป็นสามในสี่ของวงกลมเต็มตามเข็มนาฬิกา (หรือ 90 degrees ทวนเข็มนาฬิกา) ในหลายสถานการณ์การแก้ไขกราฟิก การจัดแนวนี้จะตรงกับเค้าโครงแนวตั้งต้นฉบับหลังจากการแปลงหลายขั้นตอน.

## ทำไมต้องใช้ Aspose.PSD สำหรับงานนี้?
- **Full PSD support** – ทำงานกับเลเยอร์, มาสก์, และวัตถุปรับแต่ง  
- **No native Photoshop required** – สามารถทำงานบน Java runtime ใดก็ได้  
- **Simple API** – การเรียกเมธอดเดียว (`rotateFlip`) จัดการการหมุนและการพลิก  
- **Easy format conversion** – ส่งออกโดยตรงเป็น JPEG, PNG หรือรูปแบบทั่วไปอื่น ๆ  

## วิธีการหมุนภาพด้วย Aspose.PSD for Java
ด้านล่างนี้คุณจะพบคู่มือขั้นตอนต่อขั้นตอนที่นำคุณผ่านการโหลด PSD, ใช้การหมุน 270°, เลือกพลิกภาพได้ตามต้องการ, และสุดท้ายบันทึกผลลัพธ์เป็น JPEG.

### ข้อกำหนดเบื้องต้น

ก่อนเริ่ม, ตรวจสอบว่าคุณมี:

- **Aspose.PSD for Java** library installed. คุณสามารถดาวน์โหลดและดูเอกสารอ้างอิง API เต็มรูปแบบได้ที่ [ที่นี่](https://reference.aspose.com/psd/java/).  
- สภาพแวดล้อมการพัฒนา Java (JDK 8 หรือสูงกว่า).  
- ไฟล์ PSD ตัวอย่างที่คุณต้องการหมุน. อัปเดตตัวแปร `sourceFile` ในโค้ดให้เป็นพาธที่ถูกต้องของไฟล์ของคุณ.

### นำเข้าแพ็กเกจ

เริ่มต้นด้วยการนำเข้าคลาสที่จำเป็นจากแพ็กเกจ Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

### ขั้นตอน 1: โหลดภาพ

สร้างอินสแตนซ์ `Image` ที่ชี้ไปยังไฟล์ PSD แหล่งของคุณ:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### ขั้นตอน 2: หมุนภาพ 270 องศา

ใช้เมธอด `rotateFlip` พร้อม `RotateFlipType.Rotate270FlipNone` เพื่อทำการหมุน 270 องศาโดยไม่มีการพลิกภาพ:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Pro tip:** หากคุณต้องการพลิกภาพในแนวนอนหรือแนวตั้งด้วย, เลือก `RotateFlipType` ที่แตกต่างเช่น `Rotate90FlipX` หรือ `Rotate180FlipY`. นี่เป็นวิธีที่พบบ่อยที่สุดสำหรับการดำเนินการ **flip image java**.

### ขั้นตอน 3: แปลง PSD เป็น JPEG และบันทึก

หลังจากหมุนแล้ว, คุณสามารถ **convert PSD to JPEG** (หรือรูปแบบอื่นที่รองรับ) โดยใช้คลาส options ที่เหมาะสม:

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

ไฟล์ `RotatedImage_out.jpg` ตอนนี้มีเนื้อหา PSD ดั้งเดิมที่หมุน 270 องศาและบันทึกเป็น JPEG.

## ทำไมเรื่องนี้สำคัญ – กรณีการใช้งานจริง
- **Batch processing of product catalogs** – หมุน PSD หลายสิบไฟล์ให้มีการจัดแนวเดียวกันก่อนเผยแพร่.  
- **Automated thumbnail generation** – สร้างตัวอย่างภาพขนาดเล็กที่จัดแนวถูกต้องสำหรับแกลเลอรีเว็บโดยไม่ต้องเปิด Photoshop.  
- **Mobile app back‑ends** – ปรับทิศทางไฟล์ PSD ที่ผู้ใช้อัปโหลดบนเซิร์ฟเวอร์โดยใช้ Java อย่างเดียว.

## ปัญหาที่พบบ่อยและการแก้ไข

| Issue | Solution |
|-------|----------|
| **ภาพแสดงหัวกลับ** | ตรวจสอบว่าคุณใช้ `Rotate270FlipNone`. สำหรับการหมุน 90‑องศาตามเข็มนาฬิกาให้ใช้ `Rotate90FlipNone`. |
| **ไฟล์ผลลัพธ์เสียหาย** | ตรวจสอบให้แน่ใจว่าโฟลเดอร์ปลายทางมีอยู่และคุณมีสิทธิ์เขียน. |
| **ข้อยกเว้นไลเซนส์** | ติดตั้งไลเซนส์ Aspose.PSD ชั่วคราวหรือถาวรก่อนโหลดภาพในสภาพการผลิต. |
| **ต้องการหมุนภาพโดยไม่ใช้ Photoshop** | API นี้ทำการหมุนภาพทั้งหมดในโค้ด, ลบการพึ่งพา Photoshop ออก. |
| **ต้องการพลิกภาพเป็นส่วนหนึ่งของการดำเนินการเดียว** | ใช้ค่า `RotateFlipType` อื่น ๆ เช่น `Rotate90FlipX` (ครอบคลุม **how to flip image**). |

## คำถามที่พบบ่อย

**Q:** Aspose.PSD รองรับรูปแบบภาพต่าง ๆ หรือไม่?  
**A:** ใช่, Aspose.PSD รองรับ PSD, JPEG, PNG, BMP, GIF และรูปแบบแรสเตอร์อื่น ๆ อีกหลายรูปแบบ.

**Q:** ฉันสามารถใช้การหมุนแบบกำหนดเองได้หรือไม่, ไม่ใช่แค่การพลิกที่กำหนดไว้ล่วงหน้า?  
**A:** แน่นอน! แม้ว่า `RotateFlipType` จะให้มุมที่พบบ่อย, คุณสามารถรวมหลายการเรียกหรือใช้เมทริกซ์การแปลงสำหรับมุมใดก็ได้.

**Q:** ฉันจะแปลง PSD ที่หมุนแล้วเป็นรูปแบบอื่น เช่น PNG ได้อย่างไร?  
**A:** แทนที่ `JpegOptions` ด้วย `PngOptions` (หรือคลาส options ที่เหมาะสม) ในเมธอด `save`.

**Q:** ฉันสามารถหาการสนับสนุนหรือความช่วยเหลือเพิ่มเติมได้ที่ไหน?  
**A:** For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q:** มีการทดลองใช้ฟรีหรือไม่?  
**A:** Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).

**Q:** ฉันจะขอรับไลเซนส์ชั่วคราวได้อย่างไร?  
**A:** If you need a temporary license, you can obtain one [here](https://purchase.aspose.com/temporary-license/).

**Q:** วิธีนี้ทำงานบนเซิร์ฟเวอร์แบบไม่มี UI (headless) หรือไม่?  
**A:** ใช่, Aspose.PSD for Java ทำงานในสภาพแวดล้อม JVM มาตรฐานใด ๆ ทำให้เหมาะสำหรับ pipeline CI/CD หรือฟังก์ชันคลาวด์.

## สรุป

คุณได้เรียนรู้ **how to rotate image** 270 degrees ด้วย Aspose.PSD for Java, วิธี **flip image** เมื่อจำเป็น, และวิธีส่งออกผลลัพธ์เป็น JPEG แล้ว กระบวนการทำงานที่ง่ายนี้สามารถรวมเข้ากับ pipeline การประมวลผลภาพด้วย Java ขนาดใหญ่ได้, ให้คุณควบคุมการจัดการ PSD อย่างเต็มที่โดยไม่ต้องพึ่งพา Photoshop.

---

**Last Updated:** 2026-02-12  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}