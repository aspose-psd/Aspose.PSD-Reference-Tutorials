---
date: 2025-12-19
description: เรียนรู้วิธีปรับความสว่างของภาพโดยใช้ Aspose.PSD สำหรับ Java. บทแนะนำการจัดการภาพด้วย
  Java นี้ให้คำแนะนำแบบทีละขั้นตอน.
linktitle: Adjust Brightness of an Image
second_title: Aspose.PSD Java API
title: วิธีปรับความสว่างของภาพด้วย Aspose.PSD สำหรับ Java
url: /th/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ปรับความสว่างของภาพด้วย Aspose.PSD for Java

## บทนำ

If you need to **learn how to adjust brightness** of a picture directly from Java code, you’re in the right place. Brightness tweaking is a frequent task for graphic designers, photographers, and anyone building image‑processing pipelines. In this **java image manipulation tutorial** we’ll walk through the complete workflow—loading a PSD/TIFF, applying a brightness offset, and saving the result—using the Aspose.PSD for Java library.

## คำตอบอย่างรวดเร็ว
- **ไลบรารีที่จัดการความสว่างคืออะไร?** Aspose.PSD for Java  
- **เมธอดที่เปลี่ยนความสว่างคืออะไร?** `RasterImage.adjustBrightness()`  
- **ฉันสามารถทำงานกับไฟล์ PSD และ TIFF ได้หรือไม่?** ใช่, API รองรับทั้งสองรูปแบบ.  
- **ต้องการไลเซนส์สำหรับการใช้งานจริงหรือไม่?** จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานที่ไม่ใช่การประเมิน.  
- **ใช้เวลานานเท่าไหร่ในการทำงานนี้?** ปกติใช้เวลาน้อยกว่า 10 นาทีสำหรับการปรับพื้นฐาน.

## การปรับความสว่างของภาพคืออะไร?

Image brightness adjustment changes the overall lightness of every pixel in an image. Increasing brightness makes dark areas lighter, while decreasing it darkens the entire picture. This operation is useful for correcting underexposed photos, preparing assets for print, or creating visual effects in applications.

## ทำไมต้องใช้ Aspose.PSD for Java?

- **การสนับสนุนรูปแบบเต็ม** – PSD, TIFF, JPEG, PNG, และอื่น ๆ.  
- **ไม่มีการพึ่งพาเนทีฟภายนอก** – Java แท้, ง่ายต่อการรวม.  
- **แคชประสิทธิภาพสูง** – ข้อมูลแรสเตอร์สามารถแคชเพื่อการทำงานซ้ำที่เร็วขึ้น.  
- **API ที่ครบครัน** – เมธอดสำหรับการแก้สี, เลเยอร์, มาสก์, และการแก้ไขขั้นสูงอื่น ๆ.

## ข้อกำหนดเบื้องต้น

Before diving into the tutorial, ensure you have the following prerequisites:

- Aspose.PSD for Java Library: ดาวน์โหลดและติดตั้งไลบรารีจาก [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).

## นำเข้าแพ็กเกจ

To begin, import the necessary packages into your Java project. In this example, we'll use the following:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Now, let's break down the process of adjusting the brightness of an image into simple steps:

## วิธีปรับความสว่างโดยใช้ Aspose.PSD

### ขั้นตอนที่ 1: โหลดภาพ

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

ในขั้นตอนนี้ เราโหลดภาพเป้าหมายและแคสต์เป็น `RasterImage` เพื่อการประมวลผลต่อไป.

### ขั้นตอนที่ 2: ปรับความสว่าง

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

ที่นี่ เราใช้เมธอด `adjustBrightness` เพื่อปรับความสว่างของภาพ ในตัวอย่างนี้ เราลดความสว่างลง 50 หน่วย แต่คุณสามารถปรับค่าตามความต้องการของคุณได้.

### ขั้นตอนที่ 3: ตั้งค่า TiffOptions

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

กำหนดค่า `TiffOptions` สำหรับการบันทึกภาพที่ปรับแล้ว ปรับคุณสมบัติ `bitsPerSample` และ `photometric` ตามความต้องการของคุณ.

### ขั้นตอนที่ 4: บันทึกภาพผลลัพธ์

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

สุดท้าย บันทึกภาพที่แก้ไขโดยใช้ `TiffOptions` ที่ระบุ.

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|----------|
| **`ClassCastException` เมื่อทำการแคสต์ Image** | ไฟล์ไม่ใช่ภาพแรสเตอร์ (เช่น PSD เวกเตอร์). | ตรวจสอบรูปแบบไฟล์ต้นทางหรือใช้ `image instanceof RasterImage` ก่อนทำการแคสต์. |
| **การเปลี่ยนแปลงความสว่างไม่มีผล** | ภาพไม่ได้ถูกแคชก่อนการปรับ. | เรียก `rasterImage.cacheData()` ตามที่แสดงในขั้นตอน 1. |
| **ไฟล์ที่บันทึกดูเหมือนเสียหาย** | การกำหนดค่า `TiffOptions` ไม่ถูกต้อง. | ตรวจสอบให้แน่ใจว่า `bitsPerSample` ตรงกับความลึกของภาพต้นทาง (โดยทั่วไป 8‑บิตต่อช่อง). |

## คำถามที่พบบ่อย

### Q1: ฉันสามารถปรับความสว่างในรูปแบบภาพอื่น ๆ นอกจาก PSD ได้หรือไม่?

A1: ใช่, Aspose.PSD for Java รองรับรูปแบบภาพหลายประเภทเช่น JPEG, PNG, และ TIFF.

### Q2: ฉันจะจัดการข้อผิดพลาดระหว่างกระบวนการปรับภาพอย่างไร?

A2: คุณสามารถทำการจัดการข้อผิดพลาดโดยใช้บล็อก try‑catch เพื่อจัดการกับข้อยกเว้นที่อาจเกิดขึ้น.

### Q3: มีขอบเขตจำกัดสำหรับการปรับความสว่างหรือไม่?

A3: ขอบเขตการปรับขึ้นอยู่กับเนื้อหาและรูปแบบของภาพ, แต่ Aspose.PSD ให้ความยืดหยุ่นในการปรับแต่ง.

### Q4: ฉันสามารถใช้ Aspose.PSD for Java ในโครงการเชิงพาณิชย์ได้หรือไม่?

A4: ใช่, Aspose.PSD for Java เป็นไลบรารีเชิงพาณิชย์, และคุณสามารถรับไลเซนส์ได้จาก [here](https://purchase.aspose.com/buy).

### Q5: มีการทดลองใช้งานฟรีสำหรับ Aspose.PSD for Java หรือไม่?

A5: ใช่, คุณสามารถสำรวจไลบรารีด้วยการทดลองใช้งานฟรีจาก [here](https://releases.aspose.com/).

### Q6: เมธอด `adjustBrightness` มีผลต่อการมองเห็นเลเยอร์หรือไม่?

A6: เมธอดทำงานบนภาพคอมโพสิตที่แรสเตอร์แล้ว, ดังนั้นการมองเห็นเลเยอร์จะได้รับการเคารพในระหว่างการแรสเตอร์.

### Q7: ฉันสามารถเชื่อมต่อการปรับหลายอย่าง (เช่น คอนทราสต์, ความอิ่มตัว) เข้าด้วยกันได้หรือไม่?

A7: แน่นอน. หลังจากปรับความสว่าง, คุณสามารถเรียก `adjustContrast`, `adjustSaturation` ฯลฯ บนอินสแตนซ์ `RasterImage` เดียวกัน.

**อัปเดตล่าสุด:** 2025-12-19  
**ทดสอบกับ:** Aspose.PSD for Java 24.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}