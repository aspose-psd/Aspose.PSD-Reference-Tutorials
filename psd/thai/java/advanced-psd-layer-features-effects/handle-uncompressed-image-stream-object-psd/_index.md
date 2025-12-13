---
date: 2025-12-13
description: เรียนรู้วิธีสร้างอ็อบเจ็กต์กราฟิก PSD และจัดการชั้น PSD โดยการจัดการสตรีมภาพที่ไม่ได้บีบอัดด้วย
  Aspose.PSD for Java.
linktitle: Handle Uncompressed Image Stream Object in PSD - Java
second_title: Aspose.PSD Java API
title: สร้างอ็อบเจ็กต์กราฟิก PSD – สตรีมที่ไม่ได้บีบอัดใน Java
url: /th/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้างอ็อบเจ็กต์กราฟิก PSD – สตรีมที่ไม่ได้บีบอัดใน Java

## Introduction
ยินดีต้อนรับสู่โลกของการจัดการภาพใน Java! ในบทเรียนนี้คุณจะ **สร้างอ็อบเจ็กต์กราฟิก PSD** และจัดการกับสตรีมภาพที่ไม่ได้บีบอัดโดยใช้ Aspose.PSD for Java ไม่ว่าคุณจะเป็นนักออกแบบกราฟิกที่ต้องการทำงานอัตโนมัติหรือเป็นนักพัฒนาซอฟต์แวร์ที่ต้องการรวมความสามารถการประมวลผลภาพที่ทรงพลังเข้าไปในแอปพลิเคชันของคุณ คู่มือนี้ออกแบบมาเพื่อคุณโดยเฉพาะ เราจะเดินผ่านทุกขั้นตอนตั้งแต่ข้อกำหนดเบื้องต้นจนถึงบทสรุป เพื่อให้คุณเข้าใจอย่างถ่องแท้ว่าจะเริ่มต้นกับ Aspose.PSD อย่างไร

## Quick Answers
- **“สร้างอ็อบเจ็กต์กราฟิก PSD” หมายถึงอะไร?** หมายถึงการสร้างคอนเท็กซ์กราฟิกสำหรับไฟล์ PSD เพื่อให้คุณสามารถวาดหรือแก้ไขเนื้อหาได้  
- **ไลบรารีใดจัดการสตรีมที่ไม่ได้บีบอัด?** Aspose.PSD for Java ให้การสนับสนุนเต็มรูปแบบสำหรับข้อมูลภาพแบบ raw (ไม่ได้บีบอัด)  
- **ต้องใช้ไลเซนส์สำหรับการพัฒนาหรือไม่?** สามารถใช้รุ่นทดลองฟรีสำหรับการทดสอบได้; ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **ฉันสามารถจัดการเลเยอร์ของ PSD หลังจากสร้างอ็อบเจ็กต์กราฟิกได้หรือไม่?** ได้ – อินสแตนซ์ Graphics ให้คุณวาดบนเลเยอร์ใดก็ได้  

## Prerequisites
ก่อนที่เราจะกระโดดเข้าสู่โค้ด ให้ตรวจสอบว่าคุณมีทุกอย่างที่จำเป็นสำหรับการเริ่มต้นการเดินทางนี้ นี่คือข้อกำหนดเบื้องต้น:

### Java Development Kit (JDK)
ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนเครื่องของคุณแล้ว คุณสามารถดาวน์โหลดได้จากเว็บไซต์ของ Oracle หรือใช้ OpenJDK

### Aspose.PSD for Java
คุณต้องดาวน์โหลดและติดตั้งไลบรารี Aspose.PSD ไลบรารีที่ทรงพลังนี้ช่วยให้คุณจัดการไฟล์ PSD ได้อย่างง่ายดาย คุณสามารถรับเวอร์ชันล่าสุดได้จาก [ลิงก์นี้](https://releases.aspose.com/psd/java/)

### Integrated Development Environment (IDE)
แนะนำให้ใช้ IDE เพื่อเขียนและทดสอบโค้ด Java ของคุณ คุณสามารถใช้ IntelliJ IDEA, Eclipse หรือ IDE ใดก็ได้ที่คุณถนัด

### Basic Understanding of Java
ความคุ้นเคยกับการเขียนโปรแกรม Java จะทำให้กระบวนการนี้ราบรื่นยิ่งขึ้น ตรวจสอบให้แน่ใจว่าคุณเข้าใจพื้นฐานเช่น คลาส, เมธอด, และการจัดการข้อยกเว้น

เมื่อทุกอย่างพร้อมแล้ว มาเริ่มต้นทำความสนุกกับการเขียนโค้ดกันเถอะ!

## Import Packages
เพื่อเริ่มต้น เราต้องนำเข้าแพ็กเกจที่จำเป็นสำหรับการทำงานกับ Aspose.PSD ด้านล่างนี้คือรายการ import ที่คุณมักต้องใช้สำหรับการจัดการไฟล์ PSD

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

ตอนนี้เราจะทำการแบ่งโค้ดออกเป็นขั้นตอนย่อยเพื่อให้คุณตามได้ง่าย เราจะตั้งค่า, โหลดไฟล์ PSD, แก้ไข, และบันทึกผลลัพธ์

## Step 1: Define Your Document Directory
ก่อนเริ่มเขียนโค้ด คุณควรกำหนดตำแหน่งที่ไฟล์ PSD ของคุณอยู่ นี่คือการตั้งค่าพื้นฐานสำหรับโปรเจกต์ของคุณ

```java
String dataDir = "Your Document Directory";
```

เปลี่ยน `"Your Document Directory"` ให้เป็นพาธจริงที่ไฟล์ PSD (เช่น layers.psd) ของคุณอยู่ เพื่อให้โค้ดสามารถค้นหาไฟล์ได้โดยไม่มีปัญหา

## Step 2: Create a Byte Array Output Stream
คุณต้องมีที่เก็บภาพที่แก้ไขแล้วก่อนจะทำอะไรต่อไป `ByteArrayOutputStream` จะช่วยให้คุณจับข้อมูลภาพได้อย่างง่ายดาย

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

บรรทัดนี้จะสร้างอ็อบเจ็กต์ `ByteArrayOutputStream` ใหม่ชื่อ `ms` ซึ่งคุณจะใช้บันทึกภาพที่ไม่ได้บีบอัดของคุณ

## Step 3: Load the PSD File
ต่อไปเป็นการโหลดไฟล์ PSD จริง ๆ ที่นี่คือจุดเริ่มต้นของความมหัศจรรย์!

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

บรรทัดนี้จะโหลดไฟล์ PSD ของคุณเข้าสู่อ็อบเจ็กต์ `PsdImage` ตรวจสอบให้แน่ใจว่าพาธถูกต้อง มิฉะนั้นจะเกิดข้อผิดพลาดเช่นการสอบถามที่ไม่ได้ตรวจสอบ

## Step 4: Set Up the PsdOptions for Saving
คุณต้องระบุวิธีการบันทึกภาพของคุณ – แน่นอนว่าเป็นแบบไม่ได้บีบอัด!

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

ที่นี่คุณสร้างอ็อบเจ็กต์ `PsdOptions` และตั้งค่า `compressionMethod` เป็น `Raw` วิธีนี้จะทำให้ภาพคงคุณภาพเต็มที่และบันทึกโดยไม่มีการบีบอัด

## Step 5: Save the Image to the Output Stream
```java
psdImage.save(ms, saveOptions);
```

บรรทัดนี้จะบันทึกภาพที่แก้ไขแล้วลงใน `ByteArrayOutputStream` ที่คุณสร้างในขั้นตอน 2 โดยใช้ตัวเลือกที่กำหนดในขั้นตอน 4 เมธอด `save` จะจัดการการเข้ารหัสภาพตามการตั้งค่าของคุณ

## Step 6: Reset the Output Stream
หลังจากบันทึกแล้ว สตรีมของคุณจะอยู่ที่ตำแหน่งสุดท้าย คุณต้องรีเซ็ตเพื่ออ่านจากจุดเริ่มต้นอีกครั้ง

```java
ms.reset();
```

เมธอด `reset` นี้เตรียม `ByteArrayOutputStream` ของคุณให้พร้อมอ่านจากจุดเริ่มต้นอีกครั้ง เหมือนการรีวินด์เทปก่อนฟังเพลงโปรดของคุณ!

## Step 7: Load the Newly Created Image
```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

ที่นี่เราจะโหลดภาพกลับจาก `ByteArrayOutputStream` เข้าไปในอ็อบเจ็กต์ `PsdImage` ใหม่ ซึ่งคุณสามารถตรวจสอบผลลัพธ์ของการทำงานก่อนหน้าได้

## Step 8: Create Graphics Object
เพื่อทำการแก้ไขหรือเรนเดอร์ภาพต่อ คุณต้องสร้างอ็อบเจ็กต์กราฟิก

```java
Graphics graphics = new Graphics(psdImage);
```

บรรทัดนี้จะสร้างอ็อบเจ็กต์ `Graphics` โดยใช้ `psdImage` ของคุณ คุณสามารถใช้กราฟิกอ็อบเจ็กต์นี้เพื่อวาดหรือจัดการภาพตามที่ต้องการ เหมือนมีแปรงสีในมือของคุณ!

## Manipulate PSD Layers with Graphics Object
เมื่อคุณมีอินสแตนซ์ **Graphics** แล้ว คุณสามารถ **จัดการเลเยอร์ของ PSD** ได้ – เช่น วาดรูปทรง, เพิ่มข้อความ, หรือใช้ฟิลเตอร์บนเลเยอร์เฉพาะ กราฟิกคอนเท็กซ์ทำงานโดยตรงบนพิกเซลพื้นฐาน ให้คุณควบคุมลักษณะของแต่ละเลเยอร์ได้อย่างละเอียด

## Common Issues and Solutions
- **NullPointerException เมื่อโหลดไฟล์** – ตรวจสอบพาธ `dataDir` อีกครั้งและให้แน่ใจว่าไฟล์มีชื่อถูกต้อง  
- **ผลลัพธ์บีบอัดแม้ตั้งเป็น Raw** – ยืนยันว่าได้เรียก `saveOptions.setCompressionMethod(CompressionMethod.Raw);` ก่อนเมธอด `save`  
- **อ็อบเจ็กต์ Graphics แสดงเป็นสีขาว** – ตรวจสอบว่าคุณกำลังวาดบนอินสแตนซ์ `PsdImage` ที่ถูกต้อง (ใช้ตัวที่โหลดมา ไม่ใช่ตัวที่สร้างใหม่ เว้นแต่ต้องการ)

## FAQ's
### Aspose.PSD คืออะไร?
Aspose.PSD เป็นไลบรารี .NET ที่ช่วยให้นักพัฒนาสร้าง, แก้ไข, และจัดการไฟล์ Photoshop PSD รวมถึงรูปแบบภาพที่เกี่ยวข้องได้โดยโปรแกรม

### ฉันจะดาวน์โหลด Aspose.PSD for Java ได้จากที่ไหน?
คุณสามารถดาวน์โหลดได้จาก [หน้ารีลีส](https://releases.aspose.com/psd/java/)

### มีรุ่นทดลองฟรีสำหรับ Aspose.PSD หรือไม่?
มี – คุณสามารถรับรุ่นทดลองฟรีได้จาก [ที่นี่](https://releases.aspose.com/)

### ฉันสามารถขอรับการสนับสนุนสำหรับ Aspose.PSD ได้หรือไม่?
แน่นอน! คุณสามารถขอความช่วยเหลือได้ที่ [ฟอรั่มสนับสนุนของ Aspose](https://forum.aspose.com/c/psd/34)

### ฉันจะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร?
เพียงเยี่ยมชม [หน้าการขอไลเซนส์ชั่วคราว](https://purchase.aspose.com/temporary-license/) เพื่อเริ่มต้น

## Frequently Asked Questions

**Q: ฉันสามารถใช้กราฟิกอ็อบเจ็กต์เพื่อแก้ไขเฉพาะเลเยอร์เดียวได้หรือไม่?**  
A: ได้ หลังจากโหลด PSD แล้ว ให้เลือกเลเยอร์ที่ต้องการผ่าน `psdImage.getLayers().get_Item(index)` แล้วส่งอ็อบเจ็กต์นั้นไปยังคอนสตรัคเตอร์ของ `Graphics`

**Q: วิธีการบีบอัด Raw มีผลต่อขนาดไฟล์หรือไม่?**  
A: Raw จะเก็บข้อมูลพิกเซลโดยไม่มีการบีบอัด ดังนั้นไฟล์จะใหญ่กว่าการบีบอัดทั่วไป แต่คุณภาพภาพจะไม่เสียหาย

**Q: สามารถส่งออก PSD ที่แก้ไขแล้วเป็นรูปแบบอื่นได้หรือไม่ (เช่น PNG)?**  
A: แน่นอน ใช้เมธอด `Image.save` ที่รับ `PngOptions` หลังจากทำการแก้ไขเสร็จ

**Q: ต้องการ Java เวอร์ชันใด?**  
A: Aspose.PSD for Java รองรับ JDK 8 ขึ้นไป

**Q: ฉันควรปล่อยทรัพยากรหลังการประมวลผลอย่างไร?**  
A: เรียก `psdImage.dispose()` และปิดสตรีมใด ๆ เพื่อคืนทรัพยากรเนทีฟ

---  

**Last Updated:** 2025-12-13  
**Tested With:** Aspose.PSD for Java (latest release)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}