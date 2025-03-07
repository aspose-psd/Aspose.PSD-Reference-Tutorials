---
title: เบลอภาพโดยใช้ Aspose.PSD สำหรับ Java
linktitle: เบลอภาพ
second_title: Aspose.PSD Java API
description: เรียนรู้การเบลอภาพใน Java ด้วย Aspose.PSD ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อผลลัพธ์ระดับมืออาชีพ
weight: 24
url: /th/java/advanced-techniques/blur-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เบลอภาพโดยใช้ Aspose.PSD สำหรับ Java

## การแนะนำ

ในโลกของการพัฒนา Java การปรับปรุงและการจัดการอิมเมจถือเป็นข้อกำหนดทั่วไป หากคุณต้องการเพิ่มเอฟเฟกต์เบลอให้กับรูปภาพของคุณโดยทางโปรแกรม Aspose.PSD สำหรับ Java เป็นเครื่องมืออันทรงพลังที่ทำให้กระบวนการง่ายขึ้น บทช่วยสอนนี้จะแนะนำคุณตลอดขั้นตอนการเบลอภาพโดยใช้ Aspose.PSD เพื่อให้มั่นใจว่าคุณจะได้ผลลัพธ์ระดับมืออาชีพได้อย่างง่ายดาย

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- ติดตั้ง Java Development Kit (JDK) บนระบบของคุณ
-  Aspose.PSD สำหรับไลบรารี Java คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/psd/java/).
- ความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม Java

## แพ็คเกจนำเข้า

เริ่มต้นด้วยการนำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ ซึ่งรวมถึงคลาส Aspose.PSD สำหรับการประมวลผลภาพ

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussianBlurFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

ตอนนี้ เรามาแบ่งกระบวนการทำให้ภาพเบลอออกเป็นหลายขั้นตอนกัน

## ขั้นตอนที่ 1: กำหนดเส้นทางไฟล์

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "BlurAnImage_out.gif";
```

## ขั้นตอนที่ 2: โหลดรูปภาพ

```java
// โหลดรูปภาพที่มีอยู่ลงในอินสแตนซ์ของคลาส RasterImage
Image image = Image.load(sourceFile);
```

## ขั้นตอนที่ 3: แปลงเป็น RasterImage

```java
// แปลงภาพให้เป็น RasterImage
RasterImage rasterImage = (RasterImage)image;
```

## ขั้นตอนที่ 4: ใช้ตัวกรองเบลอ

```java
//ส่ง Bounds[rectangle] ของรูปภาพและอินสแตนซ์ GaussianBlurFilterOptions ไปยังวิธี Filter
rasterImage.filter(rasterImage.getBounds(), new GaussianBlurFilterOptions(15, 15));
```

## ขั้นตอนที่ 5: บันทึกผลลัพธ์

```java
// บันทึกผลลัพธ์ในรูปแบบ GIF
rasterImage.save(destName, new GifOptions());
```

เมื่อทำตามขั้นตอนเหล่านี้ คุณจะใช้เอฟเฟกต์เบลอกับรูปภาพของคุณโดยใช้ Aspose.PSD สำหรับ Java ได้สำเร็จ

## บทสรุป

Aspose.PSD สำหรับ Java ทำให้งานการประมวลผลภาพง่ายขึ้น ทำให้นักพัฒนาสามารถบรรลุผลลัพธ์ระดับมืออาชีพได้อย่างง่ายดาย การเบลอภาพโดยทางโปรแกรมเป็นเพียงตัวอย่างหนึ่งของคุณสมบัติอันทรงพลังที่ไลบรารีนี้มีให้

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.PSD สำหรับ Java เหมาะสำหรับนักพัฒนามือใหม่หรือไม่

A1: แน่นอน! Aspose.PSD มาพร้อมกับเอกสารที่ครอบคลุมเพื่อเป็นแนวทางแก่นักพัฒนาทุกระดับทักษะ

### คำถามที่ 2: ฉันสามารถใช้ Aspose.PSD สำหรับโครงการเชิงพาณิชย์ได้หรือไม่

 A2: ใช่คุณทำได้ เยี่ยม[ที่นี่](https://purchase.aspose.com/buy) เพื่อสำรวจตัวเลือกการออกใบอนุญาต

### คำถามที่ 3: มีการทดลองใช้ฟรีหรือไม่?

 A3: ใช่ คุณสามารถทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD สำหรับ Java ได้ที่ไหน

 A4: เยี่ยมชม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) สำหรับคำถามที่เกี่ยวข้องกับการสนับสนุน

### คำถามที่ 5: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร

 A5: คุณสามารถรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
