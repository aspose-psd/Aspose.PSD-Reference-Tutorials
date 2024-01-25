---
title: ปรับภาพให้เป็นสีเทาโดยใช้ Aspose.PSD สำหรับ Java
linktitle: ระดับสีเทาของรูปภาพ
second_title: Aspose.PSD Java API
description: สำรวจ Aspose.PSD สำหรับ Java และเรียนรู้วิธีทำให้ภาพเป็นระดับสีเทาอย่างง่ายดายด้วยบทช่วยสอนทีละขั้นตอนของเรา
type: docs
weight: 10
url: /th/java/advanced-techniques/grayscale-image/
---
## การแนะนำ

ในขอบเขตของการประมวลผลภาพ การแปลงภาพเป็นระดับสีเทาถือเป็นการดำเนินการขั้นพื้นฐาน Aspose.PSD สำหรับ Java มอบโซลูชันอันทรงพลังสำหรับนักพัฒนา Java เพื่อให้บรรลุเป้าหมายนี้ได้อย่างราบรื่น ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการปรับขนาดสีเทาของรูปภาพโดยใช้ Aspose.PSD เพื่อให้มั่นใจว่าแม้แต่ผู้เริ่มต้นก็สามารถทำตามได้อย่างง่ายดาย

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java บนระบบของคุณ
2.  Aspose.PSD สำหรับ Java: ดาวน์โหลดและติดตั้งไลบรารี Aspose.PSD สำหรับ Java จาก[ที่นี่](https://releases.aspose.com/psd/java/).

## แพ็คเกจนำเข้า

เริ่มต้นด้วยการนำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ ขั้นตอนนี้ช่วยให้แน่ใจว่าคุณสามารถเข้าถึงฟังก์ชัน Aspose.PSD ในโค้ดของคุณได้ เพิ่มบรรทัดต่อไปนี้ที่จุดเริ่มต้นของไฟล์ Java ของคุณ:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterCachedImage;

import com.aspose.psd.imageoptions.JpegOptions;
import java.io.FileNotFoundException;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสารของคุณ

กำหนดไดเร็กทอรีซึ่งเป็นที่ตั้งของไฟล์ PSD ของคุณและตำแหน่งที่จะบันทึกเอาต์พุตระดับสีเทา:

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: โหลดอิมเมจต้นฉบับ

โหลดรูปภาพ PSD ต้นฉบับลงในโค้ดโดยใช้ตัวอย่างต่อไปนี้:

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "Grayscaling_out.jpg";

Image image = Image.load(sourceFile);
```

## ขั้นตอนที่ 3: ตรวจสอบและแคชอิมเมจ

ตรวจสอบให้แน่ใจว่ารูปภาพที่โหลดถูกแคชไว้ โดยปรับความเร็วการประมวลผลให้เหมาะสม:

```java
RasterCachedImage rasterCachedImage = (RasterCachedImage)image;
if (!rasterCachedImage.isCached())
{
    rasterCachedImage.cacheData();
}
```

## ขั้นตอนที่ 4: แปลงเป็นโทนสีเทา

แปลงรูปภาพให้เป็นการแสดงระดับสีเทา:

```java
rasterCachedImage.grayscale();
```

## ขั้นตอนที่ 5: บันทึกรูปภาพผลลัพธ์

บันทึกภาพที่มีระดับสีเทาโดยใช้ชื่อปลายทางที่ระบุและตัวเลือก JPEG:

```java
rasterCachedImage.save(destName, new JpegOptions());
```

ทำซ้ำขั้นตอนเหล่านี้สำหรับรูปภาพเพิ่มเติมที่คุณต้องการให้เป็นโทนสีเทา

## บทสรุป

ยินดีด้วย! คุณปรับภาพให้เป็นสีเทาได้สำเร็จโดยใช้ Aspose.PSD สำหรับ Java กระบวนการที่เรียบง่ายแต่ทรงพลังนี้สามารถรวมเข้ากับแอปพลิเคชันต่างๆ ได้ ช่วยเพิ่มความสามารถในการประมวลผลภาพของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.PSD สำหรับ Java สำหรับโปรเจ็กต์เชิงพาณิชย์ได้หรือไม่

A1: ใช่ Aspose.PSD สำหรับ Java พร้อมให้ใช้งานเชิงพาณิชย์แล้ว คุณสามารถซื้อใบอนุญาตได้[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 2: มี Aspose.PSD สำหรับ Java เวอร์ชันทดลองใช้ฟรีหรือไม่

 ตอบ 2: ได้ คุณสามารถสำรวจคุณสมบัติของ Aspose.PSD สำหรับ Java ได้ด้วยการทดลองใช้ฟรี ดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะหาเอกสารสำหรับ Aspose.PSD สำหรับ Java ได้ที่ไหน

 A3: โปรดดูเอกสารประกอบ[ที่นี่](https://reference.aspose.com/psd/java/).

### คำถามที่ 4: ฉันจะรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD สำหรับ Java ได้อย่างไร

 A4: รับใบอนุญาตชั่วคราว[ที่นี่](https://purchase.aspose.com/temporary-license/).

### Q5: ต้องการความช่วยเหลือหรือมีคำถาม?

 A5: ไปที่ฟอรัม Aspose.PSD[ที่นี่](https://forum.aspose.com/c/psd/34).