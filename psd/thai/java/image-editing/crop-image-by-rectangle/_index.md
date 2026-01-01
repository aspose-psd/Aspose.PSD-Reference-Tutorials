---
date: 2026-01-01
description: สำรวจวิธีการครอบภาพใน Java ด้วย Aspose.PSD for Java. ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนของเราเพื่อโหลดไฟล์
  PSD, ครอบสี่เหลี่ยมภาพ, และแปลง PSD เป็น JPEG.
linktitle: Crop Image by Rectangle
second_title: Aspose.PSD Java API
title: 'ตัดรูปภาพ Java: ตัดรูปภาพด้วยสี่เหลี่ยมโดยใช้ Aspose.PSD'
url: /th/java/image-editing/crop-image-by-rectangle/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตัดรูปภาพด้วย Java: ตัดรูปภาพโดยใช้สี่เหลี่ยมกับ Aspose.PSD

## บทนำ

การจัดการกราฟิกเป็นส่วนที่ทำเป็นประจำของ **java image processing** และ Aspose.PSD for Java มอบ API ที่สะอาดและมีประสิทธิภาพสูงสำหรับทำงานกับไฟล์ PSD ในบทเรียนนี้คุณจะได้เรียนรู้ **วิธีการตัดรูปภาพ** ด้วยสี่เหลี่ยม, โหลดไฟล์ PSD, และสุดท้ายแปลงผลลัพธ์เป็น JPEG—ทั้งหมดด้วยเพียงไม่กี่บรรทัดของโค้ด Java

## คำตอบอย่างรวดเร็ว
- **What does “crop image java” mean?** หมายถึงการตัดภาพให้เป็นสี่เหลี่ยมที่กำหนดโดยใช้โค้ด Java.  
- **Which library handles the operation?** Aspose.PSD for Java provides the necessary classes.  
- **Do I need a license for testing?** มีรุ่นทดลองฟรี; จำเป็นต้องมีไลเซนส์สำหรับการใช้งานจริง.  
- **Can I convert the cropped PSD to JPEG?** ได้—ใช้ `JpegOptions` เมื่อบันทึก.  
- **How long does the implementation take?** โดยปกติใช้เวลาน้อยกว่า 10 นาทีสำหรับสถานการณ์พื้นฐาน.

## การตัดสี่เหลี่ยมภาพใน Java คืออะไร?

การตัดสี่เหลี่ยมภาพหมายถึงการเลือกพื้นที่เฉพาะ (กำหนดโดย X, Y, ความกว้าง, และความสูง) และละทิ้งทุกอย่างที่อยู่นอกพื้นที่นั้น การดำเนินการนี้มักใช้เมื่อคุณต้องการโฟกัสที่ส่วนใดส่วนหนึ่งของเอกสาร PSD ขนาดใหญ่

## ทำไมต้องใช้ Aspose.PSD สำหรับงานนี้?

- **No external dependencies** – ทำงานกับ Java แท้ ๆ.  
- **Supports PSD, PNG, JPEG, and many other formats** – คุณสามารถ **convert PSD to JPEG** ได้ทันที.  
- **High‑fidelity rendering** – รักษาข้อมูลเลเยอร์และโปรไฟล์สีระหว่างการตัด.

## ข้อกำหนดเบื้องต้น

- ติดตั้ง Java Development Kit (JDK) แล้ว.  
- Aspose.PSD for Java library – ดาวน์โหลดจาก [website](https://releases.aspose.com/psd/java/).  

## นำเข้าแพ็กเกจ

ตรวจสอบให้แน่ใจว่าได้รวมแพ็กเกจที่จำเป็นในโปรเจกต์ Java ของคุณเพื่อใช้ความสามารถของ Aspose.PSD for Java เพิ่มบรรทัด import ด้านล่างนี้ที่ส่วนต้นของไฟล์ Java ของคุณ:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

ตอนนี้เราจะแบ่งกระบวนการออกเป็นหลายขั้นตอนเพื่อแนะนำคุณในการตัดรูปภาพด้วยสี่เหลี่ยมโดยใช้ Aspose.PSD for Java

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสารของคุณ

```java
String dataDir = "Your Document Directory";
```

แทนที่ `"Your Document Directory"` ด้วยพาธจริงที่ไฟล์ PSD ของคุณอยู่

## ขั้นตอนที่ 2: ระบุไฟล์ต้นทางและไฟล์ปลายทาง

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

กำหนดพาธสำหรับไฟล์ PSD ต้นทางและไฟล์ JPEG ปลายทาง

## ขั้นตอนที่ 3: โหลดและแคชภาพ

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

ที่นี่เราจะ **load PSD file** เข้าไปในอินสแตนซ์ `RasterImage` และแคชข้อมูลเพื่อเพิ่มประสิทธิภาพ

## ขั้นตอนที่ 4: สร้างและกำหนดสี่เหลี่ยมตัด

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

สร้างอินสแตนซ์ของคลาส `Rectangle` ด้วยขนาดที่ต้องการสำหรับการตัด พารามิเตอร์แทนค่า **X**, **Y**, **width**, และ **height** ตามลำดับ

## ขั้นตอนที่ 5: ตัดและบันทึกภาพ

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

ทำการตัดโดยใช้สี่เหลี่ยมที่กำหนดและ **convert PSD to JPEG** โดยบันทึกผลลัพธ์ด้วย `JpegOptions`

ทำซ้ำขั้นตอนเหล่านี้ตามต้องการ ปรับพารามิเตอร์ให้สอดคล้องกับความต้องการเฉพาะของคุณ

## ปัญหาที่พบบ่อยและเคล็ดลับ

- **Rectangle outside image bounds** – ตรวจสอบให้แน่ใจว่าพิกัดของสี่เหลี่ยมอยู่ภายในขนาดของภาพต้นทาง.  
- **Memory consumption** – เรียก `rasterImage.dispose()` หลังใช้งานเสร็จเพื่อปล่อยทรัพยากรเนทีฟ.  
- **Quality control** – คุณสามารถตั้งค่า `JpegOptions.setQuality(int)` เพื่อควบคุมระดับการบีบอัดของ JPEG ที่ได้.

## สรุป

ในบทเรียนนี้เราได้อธิบายกระบวนการ **crop image java** ด้วยสี่เหลี่ยมโดยใช้ Aspose.PSD for Java โดยทำตามขั้นตอนเหล่านี้คุณสามารถผสานความสามารถการจัดการภาพที่ทรงพลัง—โหลดไฟล์ PSD, ตัดส่วนที่ต้องการ, และแปลงผลลัพธ์เป็น JPEG—เข้าไปในแอปพลิเคชัน Java ใดก็ได้

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ Aspose.PSD for Java กับเฟรมเวิร์ก Java อื่น ๆ ได้หรือไม่?

A1: ใช่, Aspose.PSD for Java สามารถผสานกับเฟรมเวิร์ก Java ต่าง ๆ ได้, ให้ความยืดหยุ่นในโครงการพัฒนาของคุณ

### Q2: มีรุ่นทดลองฟรีสำหรับ Aspose.PSD for Java หรือไม่?

A2: มี, คุณสามารถเข้าถึงรุ่นทดลองฟรีได้ [here](https://releases.aspose.com/)

### Q3: ฉันจะหาแหล่งสนับสนุนหรือความช่วยเหลือเพิ่มเติมได้จากที่ไหน?

A3: เยี่ยมชม [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) เพื่อรับการสนับสนุนจากชุมชนและการสนทนาต่าง ๆ

### Q4: ฉันจะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.PSD for Java ได้อย่างไร?

A4: คุณสามารถรับไลเซนส์ชั่วคราวได้ [here](https://purchase.aspose.com/temporary-license/)

### Q5: รูปแบบภาพที่รองรับสำหรับการตัดใน Aspose.PSD for Java มีอะไรบ้าง?

A5: Aspose.PSD for Java รองรับรูปแบบภาพหลายประเภท รวมถึง PSD, PNG, JPEG, และอื่น ๆ

---

**อัปเดตล่าสุด:** 2026-01-01  
**ทดสอบด้วย:** Aspose.PSD for Java 24.12  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}