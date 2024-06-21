---
title: กำลังโหลดรูปภาพจากสตรีมด้วย Aspose.PSD สำหรับ Java
linktitle: กำลังโหลดภาพจากสตรีม
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีโหลดรูปภาพ PSD ได้อย่างราบรื่นใน Java โดยใช้ Aspose.PSD ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการประมวลผลภาพที่มีประสิทธิภาพ
type: docs
weight: 11
url: /th/java/advanced-techniques/loading-images-from-stream/
---
## การแนะนำ

Aspose.PSD สำหรับ Java เป็นไลบรารี่ที่มีฟีเจอร์มากมายที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ PSD ได้อย่างราบรื่น โดยทำหน้าที่ประมวลผลภาพต่างๆ ในบทช่วยสอนนี้ เราจะเน้นไปที่ขั้นตอนสำคัญในการโหลดรูปภาพจากสตรีมโดยใช้ Aspose.PSD สำหรับ Java

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- ความรู้พื้นฐานเกี่ยวกับการเขียนโปรแกรม Java
-  ติดตั้ง Aspose.PSD สำหรับไลบรารี Java แล้ว คุณสามารถดาวน์โหลดได้จาก[เว็บไซต์กำหนด](https://releases.aspose.com/psd/java/).

## แพ็คเกจนำเข้า

ในการเริ่มต้น ให้นำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ แพ็คเกจเหล่านี้ประกอบด้วย:

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.system.io.FileMode;
import com.aspose.psd.system.io.FileStream;
import com.aspose.psd.system.io.MemoryStream;
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสารของคุณ

ตรวจสอบให้แน่ใจว่าคุณมีไดเร็กทอรีที่กำหนดไว้สำหรับเอกสารของคุณ แทนที่ "Your Document Directory" ในโค้ดด้วยเส้นทางจริง

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: กำหนดเส้นทางต้นทางและปลายทาง

ระบุเส้นทางของไฟล์ PSD ของคุณเป็นแหล่งที่มาและเส้นทางเอาต์พุตที่ต้องการสำหรับภาพที่ได้

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## ขั้นตอนที่ 3: สร้างอินพุตสตรีมและโหลดรูปภาพ

เริ่มต้น FileInputStream และโหลดไฟล์ PSD ลงในวัตถุ Image

```java
FileInputStream inputStream = new FileInputStream(sourceFile);
Image image = Image.load(inputStream);
```

## ขั้นตอนที่ 4: แปลงรูปภาพเป็น PsdImage

หากภาพที่โหลดไม่ใช่ภาพ PSD ให้แปลงเป็น PsdImage

```java
PsdImage psdImage = (PsdImage)image;
```

## ขั้นตอนที่ 5: บันทึกภาพเพื่อสตรีมด้วยตัวเลือก PNG

สร้าง FileOutputStream และบันทึก PsdImage ไปยังปลายทางที่ต้องการโดยใช้ตัวเลือก PNG

```java
FileOutputStream outputStream = new FileOutputStream(destName);
psdImage.save(outputStream, new PngOptions());
```

ยินดีด้วย! คุณโหลดรูปภาพจากสตรีมโดยใช้ Aspose.PSD สำหรับ Java สำเร็จแล้ว

## บทสรุป

 Aspose.PSD สำหรับ Java ช่วยให้นักพัฒนาสามารถจัดการไฟล์ PSD ได้อย่างง่ายดาย บทช่วยสอนนี้ให้คำแนะนำโดยย่อเกี่ยวกับการโหลดภาพจากสตรีม สำรวจ[เอกสารประกอบ](https://reference.aspose.com/psd/java/) เพื่อดูรายละเอียดและความสามารถเพิ่มเติม

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD สำหรับ Java เหมาะสำหรับการประมวลผลภาพเป็นชุดหรือไม่

A1: แน่นอน! Aspose.PSD สำหรับ Java เป็นเลิศในงานประมวลผลภาพเป็นชุด โดยให้ประสิทธิภาพและความน่าเชื่อถือ

### คำถามที่ 2: ฉันสามารถลองใช้ Aspose.PSD สำหรับ Java ก่อนซื้อได้หรือไม่

 A2: ได้ คุณสามารถทดลองใช้เวอร์ชันทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD สำหรับ Java ได้ที่ไหน

 A3: เข้าร่วมชุมชนที่[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) เพื่อขอความช่วยเหลือและหารือ

### คำถามที่ 4: ฉันจำเป็นต้องมีใบอนุญาตชั่วคราวเพื่อการทดสอบหรือไม่

 A4: รับใบอนุญาตชั่วคราว[ที่นี่](https://purchase.aspose.com/temporary-license/) สำหรับการทดสอบ Aspose.PSD สำหรับ Java

### คำถามที่ 5: ฉันจะซื้อ Aspose.PSD สำหรับ Java ได้ที่ไหน

 A5: เยี่ยมชม[หน้าซื้อ](https://purchase.aspose.com/buy) เพื่อรับ Aspose.PSD สำหรับ Java