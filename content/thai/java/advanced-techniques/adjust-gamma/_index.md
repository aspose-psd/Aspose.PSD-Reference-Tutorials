---
title: ปรับแกมม่าของรูปภาพด้วย Aspose.PSD สำหรับ Java
linktitle: ปรับแกมม่าของรูปภาพ
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีปรับแกมมาของภาพได้อย่างง่ายดายโดยใช้ Aspose.PSD สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อให้ได้ผลลัพธ์ที่ดีที่สุด
type: docs
weight: 23
url: /th/java/advanced-techniques/adjust-gamma/
---
## การแนะนำ

ในขอบเขตของการประมวลผลภาพ การปรับแกมม่าของภาพเป็นขั้นตอนสำคัญในการเพิ่มความน่าดึงดูดทางสายตา Aspose.PSD สำหรับ Java นำเสนอโซลูชันอันทรงพลังสำหรับนักพัฒนา Java เพื่อจัดการแกมมาของภาพได้อย่างง่ายดาย ในบทช่วยสอนนี้ เราจะสำรวจวิธีปรับแกมม่าโดยใช้ Aspose.PSD โดยแจกแจงรายละเอียดแต่ละขั้นตอนเพื่อให้แน่ใจว่าการใช้งานจะราบรื่น

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าข้อกำหนดเบื้องต้นต่อไปนี้:

1. สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณมีสภาพแวดล้อมการพัฒนา Java ติดตั้งอยู่บนระบบของคุณ
2.  ไลบรารี Aspose.PSD: ดาวน์โหลดและรวมไลบรารี Aspose.PSD เข้ากับโปรเจ็กต์ Java ของคุณ คุณสามารถค้นหาทรัพยากรที่จำเป็นได้ใน[เอกสารประกอบ](https://reference.aspose.com/psd/java/).
3. รูปภาพตัวอย่าง: เตรียมรูปภาพ PSD ตัวอย่างที่คุณจะใช้การปรับแกมมา

## แพ็คเกจนำเข้า

หากต้องการเริ่มต้นกระบวนการ ให้นำเข้าแพ็คเกจที่จำเป็นในโปรเจ็กต์ Java ของคุณ นี่เป็นการปูทางสำหรับการใช้ฟังก์ชัน Aspose.PSD ได้อย่างราบรื่น

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## ขั้นตอนที่ 1: โหลดรูปภาพ

 เริ่มต้นด้วยการโหลดรูปภาพ PSD ตัวอย่างลงในอินสแตนซ์ของ`RasterImage` ระดับ. นี่คือรากฐานสำหรับการปรับแกมมาในภายหลัง

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// โหลดรูปภาพที่มีอยู่ลงในอินสแตนซ์ของคลาส RasterImage
Image image = Image.load(sourceFile);

// ส่งวัตถุของ Image ไปยัง RasterImage
RasterImage rasterImage = (RasterImage)image;

// ตรวจสอบว่าแคช RasterImage เพื่อประสิทธิภาพที่ดีขึ้นหรือไม่
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## ขั้นตอนที่ 2: ปรับแกมมา

 ตอนนี้ ปรับแกมม่าของภาพที่โหลดโดยใช้`adjustGamma` วิธี. ปรับแต่งค่าแกมมาอย่างละเอียดตามความต้องการของคุณ

```java
// ปรับแกมม่า
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## ขั้นตอนที่ 3: สร้าง TiffOptions

 สร้างอินสแตนซ์ของ`TiffOptions` สำหรับภาพที่ได้ ตั้งค่าคุณสมบัติต่างๆ เช่น บิตต่อตัวอย่างและตัวเลือกโฟโตเมตริก เพื่อปรับแต่งเอาต์พุตตามข้อกำหนดเฉพาะของคุณ

```java
// สร้างอินสแตนซ์ของ TiffOptions สำหรับรูปภาพผลลัพธ์
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## ขั้นตอนที่ 4: บันทึกรูปภาพผลลัพธ์

 บันทึกรูปภาพที่ปรับแต่งเป็นรูปแบบ TIFF โดยใช้รูปแบบที่กำหนดไว้ก่อนหน้านี้`TiffOptions`.

```java
// บันทึกรูปภาพผลลัพธ์เป็นรูปแบบ TIFF
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## บทสรุป

ยินดีด้วย! คุณได้ปรับแกมม่าของรูปภาพโดยใช้ Aspose.PSD สำหรับ Java สำเร็จแล้ว กระบวนการนี้ช่วยให้นักพัฒนาปรับปรุงคุณภาพของภาพได้อย่างง่ายดาย ส่งผลให้ผู้ใช้ได้รับประสบการณ์ที่น่าดึงดูดใจ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันจะหาเอกสาร Aspose.PSD ได้ที่ไหน

 A1: คุณสามารถเข้าถึงเอกสารได้ที่[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### คำถามที่ 2: ฉันจะดาวน์โหลด Aspose.PSD สำหรับ Java ได้อย่างไร

 A2: ดาวน์โหลดไลบรารี่จาก[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### คำถามที่ 3: ฉันจะซื้อ Aspose.PSD ได้ที่ไหน

 A3: เยี่ยมเลย[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) เพื่อซื้อ Aspose.PSD

### คำถามที่ 4: มีการทดลองใช้ฟรีหรือไม่?

 A4: ได้ คุณสามารถทดลองใช้ฟรีได้ที่[https://releases.aspose.com/](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะขอรับการสนับสนุนสำหรับ Aspose.PSD ได้ที่ไหน

 A5: สำหรับการสนับสนุน โปรดไปที่ฟอรัม Aspose.PSD ที่[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).