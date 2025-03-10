---
title: ไบนารี่ที่มีเกณฑ์คงที่ใน Aspose.PSD สำหรับ Java
linktitle: ไบนารี่ที่มีเกณฑ์คงที่
second_title: Aspose.PSD Java API
description: สำรวจการแบ่งไบนารีด้วยเกณฑ์คงที่ใน Aspose.PSD สำหรับ Java แปลงรูปภาพได้อย่างราบรื่นด้วยคำแนะนำทีละขั้นตอนของเรา
weight: 14
url: /th/java/image-processing/binarization-fixed-threshold/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ไบนารี่ที่มีเกณฑ์คงที่ใน Aspose.PSD สำหรับ Java

## การแนะนำ

ในขอบเขตของการพัฒนา Java Aspose.PSD พิสูจน์แล้วว่าเป็นเครื่องมือที่ทรงพลังสำหรับงานประมวลผลภาพ การดำเนินการที่สำคัญอย่างหนึ่งคือ Binarization ซึ่งเป็นเทคนิคที่ทำให้ภาพง่ายขึ้นโดยการแปลงเป็นรูปแบบไบนารี บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการเพื่อให้ได้ไบนาไรเซชันด้วยเกณฑ์คงที่โดยใช้ Aspose.PSD สำหรับ Java รัดเข็มขัดในขณะที่เราสำรวจขั้นตอนที่เกี่ยวข้องในเส้นทางการประมวลผลภาพที่เปลี่ยนแปลงไปนี้

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- ความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม Java
-  ติดตั้ง Aspose.PSD สำหรับไลบรารี Java แล้ว คุณสามารถค้นหาแพ็คเกจที่จำเป็นได้[ที่นี่](https://releases.aspose.com/psd/java/).

## แพ็คเกจนำเข้า

ในการเริ่มต้น ให้นำเข้าแพ็คเกจที่จำเป็นลงในโปรเจ็กต์ Java ของคุณ ตรวจสอบให้แน่ใจว่าคุณมีไลบรารี Aspose.PSD ที่รวมอยู่ในโครงสร้างโปรเจ็กต์ของคุณ

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterCachedImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## ขั้นตอนที่ 1: ตั้งค่าโครงการของคุณ

เริ่มต้นด้วยการตั้งค่าโปรเจ็กต์ Java และรวมไลบรารี Aspose.PSD ตรวจสอบให้แน่ใจว่าคุณมีไดเร็กทอรีเอกสารของคุณพร้อม

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: โหลดอิมเมจต้นฉบับ

ระบุไฟล์ PSD ต้นฉบับและโหลดลงในออบเจ็กต์รูปภาพ

```java
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
RasterCachedImage rasterCachedImage = (RasterCachedImage)image;
```

## ขั้นตอนที่ 3: แคชรูปภาพ

ตรวจสอบว่ารูปภาพถูกแคชไว้แล้วหรือไม่ และหากไม่เป็นเช่นนั้น ให้แคชรูปภาพนั้น

```java
if (!rasterCachedImage.isCached()) {
    rasterCachedImage.cacheData();
}
```

## ขั้นตอนที่ 4: แปลงภาพเป็นสองเท่า

ดำเนินการกระบวนการไบนาไรเซชันด้วยเกณฑ์คงที่ที่กำหนดไว้ล่วงหน้า (ในกรณีนี้คือ 100)

```java
rasterCachedImage.binarizeFixed((byte)100);
```

## ขั้นตอนที่ 5: บันทึกภาพที่ได้

บันทึกภาพแบบไบนารี่ด้วยรูปแบบเอาต์พุตที่ต้องการ (ในกรณีนี้คือ JPEG)

```java
String destName = dataDir + "BinarizationWithFixedThreshold_out.jpg";
rasterCachedImage.save(destName, new JpegOptions());
```

แค่นั้นแหละ! คุณใช้ Binarization ด้วยเกณฑ์คงที่โดยใช้ Aspose.PSD สำหรับ Java สำเร็จแล้ว

## บทสรุป

ในบทช่วยสอนนี้ เราได้เจาะลึกเข้าไปในโลกแห่งการประมวลผลภาพด้วย Aspose.PSD สำหรับ Java โดยเน้นไปที่การทำให้เป็นไบนารี่ด้วยเกณฑ์คงที่โดยเฉพาะ ด้วยการทำตามขั้นตอนเหล่านี้ คุณสามารถปรับปรุงแอปพลิเคชัน Java ของคุณด้วยความสามารถในการแปลงรูปภาพอันทรงพลัง

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Binarization กับรูปแบบรูปภาพอื่นนอกเหนือจาก PSD ได้หรือไม่

A1:ใช่ Aspose.PSD รองรับรูปแบบรูปภาพที่หลากหลาย ทำให้ Binarization ใช้ได้กับรูปภาพหลากหลายประเภท

### คำถามที่ 2: มีใบอนุญาตชั่วคราวสำหรับการทดสอบหรือไม่

 A2: แน่นอน! คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/) เพื่อการทดสอบและประเมินผล

### คำถามที่ 3: ฉันจะรับการสนับสนุนเพิ่มเติมหรือการสนทนาในชุมชนได้จากที่ไหน

 A3: เยี่ยมชม[ฟอรั่ม Aspose.PSD](https://forum.aspose.com/c/psd/34) สำหรับการสนับสนุนจากชุมชนและการอภิปรายเกี่ยวกับข้อสงสัยใด ๆ ที่คุณอาจมี

### คำถามที่ 4: ฉันจะซื้อไลบรารี Aspose.PSD ได้อย่างไร

 A4: คุณสามารถซื้อไลบรารี Aspose.PSD ได้[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 5: มีเวอร์ชันทดลองใช้งานฟรีหรือไม่

 A5: ได้ คุณสามารถสำรวจความสามารถของ Aspose.PSD ได้ด้วยเวอร์ชันทดลองใช้ฟรี[ที่นี่](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
