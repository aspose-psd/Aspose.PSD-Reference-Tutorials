---
date: 2026-03-21
description: เรียนรู้วิธีแปลงไฟล์ PSD เป็น PNG และตัดไฟล์ PSD ด้วย Aspose.PSD สำหรับ
  Java คู่มือนี้แสดงการประมวลผลภาพแบบขั้นตอนต่อขั้นตอนในแอปพลิเคชัน Java
linktitle: Cropping PSD when Converting to PNG
second_title: Aspose.PSD Java API
title: วิธีแปลงไฟล์ PSD เป็น PNG พร้อมการครอปด้วย Aspose.PSD สำหรับ Java
url: /th/java/psd-conversion/cropping-psd-converting-png/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีแปลง PSD เป็น PNG พร้อมการครอปด้วย Aspose.PSD for Java

## บทนำ
ในโลกที่เปลี่ยนแปลงอย่างรวดเร็วของการพัฒนา Java การเชี่ยวชาญการประมวลผลภาพอย่างมีประสิทธิภาพเป็นสิ่งสำคัญ ในบทแนะนำนี้คุณจะได้เรียนรู้ **วิธีแปลง PSD เป็น PNG** และครอปภาพในขั้นตอนเดียวโดยใช้ไลบรารี Aspose.PSD for Java ที่ทรงพลัง เมื่อทำตามคำแนะนำแบบขั้นตอนนี้เสร็จแล้ว คุณจะสามารถเพิ่มการครอปที่แม่นยำให้กับการส่งออก PNG ของคุณและทำให้แอปพลิเคชัน Java ของคุณจัดการไฟล์ PSD ได้อย่างมั่นใจ

## คำตอบสั้น
- **โค้ดทำอะไร?** โหลดไฟล์ PSD, ครอปสี่เหลี่ยม, แล้วบันทึกเป็น PNG.  
- **ต้องใช้ไลบรารีอะไร?** Aspose.PSD for Java (เวอร์ชันล่าสุด).  
- **ต้องมีลิขสิทธิ์หรือไม่?** ใช่, จำเป็นต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานในโปรดักชัน.  
- **กำหนดพื้นที่ครอปได้หรือไม่?** ได้เลย – คุณสามารถตั้งค่า X, Y, ความกว้างและความสูงตามที่ต้องการ.  
- **วิธีนี้เร็วพอสำหรับไฟล์ขนาดใหญ่หรือไม่?** ใช่, Aspose.PSD ถูกออกแบบให้ทำงานประมวลผลด้วยประสิทธิภาพสูง.

## การแปลง PSD เป็น PNG คืออะไร?
การแปลง PSD เป็น PNG หมายถึงการนำเอกสาร Photoshop ที่มีหลายเลเยอร์มาทำให้เป็นภาพ PNG แบบไม่มีการสูญเสียข้อมูล รูปแบบนี้เหมาะสำหรับการส่งบนเว็บ, รูปย่อ, หรือสถานการณ์ใด ๆ ที่ต้องการภาพราสเตอร์โดยไม่ต้องการเลเยอร์ต้นฉบับ

## ทำไมต้องครอป PSD ก่อนแปลงเป็น PNG?
การครอปช่วยให้คุณดึงเฉพาะส่วนของการออกแบบที่ต้องการออกมา ลดขนาดไฟล์และเน้นเนื้อหาภาพที่สำคัญ เหมาะอย่างยิ่งสำหรับการสร้างรูปย่อ, สินทรัพย์ UI, หรือการเตรียมภาพสำหรับเลย์เอาต์ที่ตอบสนองต่อขนาดหน้าจอ

## ข้อกำหนดเบื้องต้น
ก่อนเริ่มทำตามบทแนะนำนี้ ให้ตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมใช้งาน:
- ความรู้พื้นฐานด้านการเขียนโปรแกรม Java.  
- Java Development Kit (JDK) ติดตั้งบนเครื่องของคุณ.  
- ไลบรารี Aspose.PSD for Java ดาวน์โหลดและเพิ่มเข้าไปในโปรเจกต์ของคุณ.  
- ไฟล์ PSD ตัวอย่างสำหรับการทดลอง.

## นำเข้าแพ็กเกจ
ในโปรเจกต์ Java ของคุณ ให้แน่ใจว่าได้นำเข้าแพ็กเกจที่จำเป็นสำหรับการใช้ฟังก์ชันของ Aspose.PSD:
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;
import com.aspose.psd.imageoptions.PngOptions;
```

## ขั้นตอนที่ 1: ตั้งค่าโปรเจกต์ของคุณ
เริ่มต้นด้วยการสร้างโปรเจกต์ Java และเพิ่มไลบรารี Aspose.PSD for Java ลงใน classpath ของโปรเจกต์ นั่นจะทำให้คุณเข้าถึงคลาสการประมวลผลภาพทั้งหมดที่ต้องการ

## ขั้นตอนที่ 2: โหลดภาพ PSD
```java
String dataDir = "Your Document Directory";
String srcPath = dataDir + "sample.psd";
// Load an existing PSD image
RasterImage image = (RasterImage)Image.load(srcPath);
```
*ที่นี่เราจะโหลดไฟล์ PSD ต้นฉบับเข้าสู่วัตถุ `RasterImage` ซึ่งให้การดำเนินการแบบราสเตอร์ เช่น การครอป*

## ขั้นตอนที่ 3: กำหนดพื้นที่ครอป
```java
// Create an instance of Rectangle class by passing x, y, width, and height
Rectangle cropRegion = new Rectangle(0, 0, 350, 450);
```
*อ็อบเจ็กต์ `Rectangle` กำหนดพื้นที่ที่คุณต้องการเก็บ ปรับค่า `x`, `y`, `width` และ `height` ให้ตรงกับการออกแบบของคุณ ขั้นตอนนี้ตอบคำถาม “กำหนดพื้นที่ครอป” โดยตรง*

## ขั้นตอนที่ 4: ครอปภาพ PSD
```java
// Call the crop method of Image class and pass the Rectangle instance
image.crop(cropRegion);
```
*การเรียก `crop` จะทำการแก้ไขภาพในหน่วยความจำโดยตัดส่วนที่อยู่นอกสี่เหลี่ยมที่กำหนดออก*

## ขั้นตอนที่ 5: ตั้งค่าการส่งออก PNG
```java
// Create an instance of PngOptions class
PngOptions pngOptions = new PngOptions();
```
*`PngOptions` ให้คุณควบคุมการตั้งค่าเฉพาะของ PNG เช่น ระดับการบีบอัด, ประเภทสี, และอื่น ๆ*

## ขั้นตอนที่ 6: บันทึกภาพที่ครอปเป็น PNG
```java
// Provide output path and PngOptions to convert the PSD file to PNG and save the output
String destName = dataDir + "export.png";
image.save(destName, pngOptions);
```
*เมธอด `save` ทำการ **แปลง PSD เป็น PNG** พร้อมคงการครอปที่คุณกำหนดไว้*

## ข้อผิดพลาดทั่วไป & เคล็ดลับ
- **ขนาดสี่เหลี่ยมไม่ถูกต้อง:** ตรวจสอบให้แน่ใจว่าความกว้างและความสูงไม่เกินขนาดของภาพต้นฉบับ มิฉะนั้นจะเกิดข้อยกเว้น.  
- **การใช้หน่วยความจำกับ PSD ขนาดใหญ่:** ปล่อยวัตถุ `RasterImage` (`image.dispose()`) หลังจากบันทึกเพื่อคืนทรัพยากรเนทีฟ.  
- **ไม่ได้ตั้งค่าลิขสิทธิ์:** หากรันโค้ดโดยไม่มีลิขสิทธิ์ที่ถูกต้อง จะมีลายน้ำปรากฏบน PNG ที่ได้.

## คำถามที่พบบ่อย
### ฉันสามารถครอปไฟล์ PSD ด้วยรูปทรงที่ไม่เป็นสี่เหลี่ยมได้หรือไม่โดยใช้ Aspose.PSD for Java?
ได้, Aspose.PSD for Java อนุญาตให้คุณกำหนดพื้นที่ครอปแบบกำหนดเอง ทำให้คุณสามารถครอปภาพเป็นรูปทรงต่าง ๆ ได้

### Aspose.PSD for Java เหมาะกับงานประมวลผลภาพขนาดใหญ่หรือไม่?
แน่นอน! Aspose.PSD ถูกออกแบบให้จัดการกับภาพขนาดใหญ่ได้อย่างมีประสิทธิภาพ เหมาะสำหรับโครงการที่ต้องการการประมวลผลภาพจำนวนมาก

### ฉันต้องมีลิขสิทธิ์สำหรับ Aspose.PSD for Java หรือไม่?
ใช่, จำเป็นต้องมีลิขสิทธิ์ที่ถูกต้องสำหรับการใช้งานเชิงพาณิชย์ คุณสามารถรับได้จาก [Aspose Purchase](https://purchase.aspose.com/buy)

### ฉันจะขอความช่วยเหลือหรือรายงานปัญหากับ Aspose.PSD for Java ได้อย่างไร?
เยี่ยมชม [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) เพื่อขอคำแนะนำ, แบ่งปันประสบการณ์, และรายงานปัญหาที่พบ

### ฉันสามารถลองใช้ Aspose.PSD for Java ก่อนซื้อได้หรือไม่?
ได้เลย! สำรวจคุณลักษณะของไลบรารีด้วยการทดลองใช้ฟรีที่ [here](https://releases.aspose.com/)

---

**อัปเดตล่าสุด:** 2026-03-21  
**ทดสอบด้วย:** Aspose.PSD for Java 24.12 (เวอร์ชันล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}