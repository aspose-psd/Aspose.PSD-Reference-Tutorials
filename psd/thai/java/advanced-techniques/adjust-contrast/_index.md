---
date: 2026-02-25
description: เรียนรู้วิธีแปลง PSD เป็น TIFF และปรับความคอนทราสต์ของภาพโดยใช้ Aspose.PSD
  for Java ซึ่งเป็นไลบรารีการจัดการภาพ Java ชั้นนำ
linktitle: Convert PSD to TIFF and Adjust Contrast
second_title: Aspose.PSD Java API
title: วิธีแปลงไฟล์ PSD เป็น TIFF และปรับความคอนทราสต์ด้วย Aspose.PSD สำหรับ Java
url: /th/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีแปลง PSD เป็น TIFF และปรับคอนทราสต์ด้วย Aspose.PSD for Java

## การแนะนำ

** แปลง PSD เป็น TIFF** ฟังก์ชั่นนี้จำเป็นต้องใช้ภาพคุณภาพที่คุณมาถูกที่แล้วในบทแนะนำนี้เราจะใช้ขั้นตอนทั้งหมดส่วนประกอบ Aspose.PSD สำหรับ Java — ไลบรารี **java image manipulation** คุณจะได้ฟังเพิ่ม **การปรับความคมชัดของภาพ**, แคชข้อมูล raster ขนาดใหญ่เพื่อประสิทธิภาพ, และสุดท้าย **บันทึกภาพเป็น TIFF** สำหรับการทำงานร่วมกันต่อไป!

## คำตอบด่วน
- **“ปรับคอนทราสต์” ส่วนอะไร?** มันเปลี่ยนระหว่างส่วนมืดที่มืดที่สุดและสว่างที่สุดการควบคุมรายละเอียดขึ้น
- **ไลบรารี่ใดๆ ในเรื่องนั้น?** Aspose.PSD for Java – บทความวิจัยภาพรวมของภาพ
- **ต้องมีลิขสิทธิ์หรือไม่** **ใบอนุญาตชั่วคราว** การทดสอบได้; ต้องลิขสิทธิ์เต็มๆเลยจริง
- **การ **แปลง PSD เป็น TIFF** ทำได้ใช่ไหม** แน่นอนว่า – ใช้ `TiffOptions` เพื่อส่งออกภาพในการปรับแล้ว
- **โค้ดทดสอบประสิทธิภาพ?** อีกครั้งภายในสำหรับไฟล์ PSD ขนาดมาตรฐานบนฮาร์ดแวร์ที่ทันสมัย

## การปรับคอนทราสต์ของภาพคืออะไร?
เพื่อให้คอนทราสต์เปลี่ยนช่วงโทนของภาพโดยการขยายพื้นที่ระหว่างพื้นที่สว่างและมืดซึ่งจะมีประโยชน์เมื่อภาพดูแบนด์สแกนหลังหรือเมื่อเตรียมกราฟิกสำหรับการพิมพ์

## เหตุใดจึงต้องใช้ Aspose.PSD สำหรับ Java
- **รองรับรูปแบบ Rich** – เปิด, การแสดง, และ **บันทึกภาพเป็น TIFF**, PNG, JPEG และรูปแบบอื่นๆ ของภาพเคลื่อนไหว
- **ประสิทธิภาพสูง** – การแคชและข้อมูลแรสเตอร์-รูปภาพลดความเสถียร, สำคัญสำหรับไฟล์ PSD ขนาดใหญ่
- **Straight‑forward API** – การเรียกเมธอดแบบหนึ่งบรรทัดเช่น `adjustContrast` เพื่อให้อ่านโค้ดของการบำรุงรักษาได้
- **การจัดการภาพ Java ที่ครอบคลุม** สามารถเข้ากันได้ง่าย ๆ หรือแอปพลิเคชันระดับองค์กร

## ข้อกำหนดเบื้องต้น

ก่อนเริ่ม, กรุณาตรวจสอบคุณ:

- ความรู้พื้นฐานด้าน Java
- ไลบรารี Aspose.PSD สำหรับ Java ดาวน์โหลดแล้วดาวน์โหลดดาวน์โหลด [ที่นี่](https://releases.aspose.com/psd/java/)

## แพคเกจนำเข้า

เพิ่มการ import ที่จำเป็นลงในคลาส Java ของคุณ:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## ขั้นตอนที่ 1: โหลดภาพ

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

เราจะโหลดไฟล์ PSD ต้นฉบับ (`sample.psd`) เข้าไปในอ็อบเจกต์ `Image` ซึ่งเป็นจุดเริ่มต้นสำหรับการประมวลผลต่อไปทั้งหมด

## ขั้นตอนที่ 2: แปลงเป็น RasterImage และแคชข้อมูล

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

การแคสต์เป็น `RasterImage` ทำให้เราสามารถทำงานระดับพิกเซลได้ การแคชข้อมูลช่วยเพิ่มประสิทธิภาพ โดยเฉพาะไฟล์ขนาดใหญ่

## วิธีการปรับความคมชัดของภาพ

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

เมธอด `adjustContrast` รับค่าจำนวนเต็มที่แทนเปอร์เซ็นต์การเปลี่ยนแปลง ในตัวอย่างนี้เราปรับคอนทราสต์เพิ่ม **50 %**

## แปลง PSD เป็น TIFF โดยใช้ Aspose.PSD

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

ที่นี่เราตั้งค่า `TiffOptions` (bits per sample, photometric interpretation) และ **save image as TIFF** ขั้นตอนนี้ทำให้การ **convert PSD to TIFF** เสร็จสมบูรณ์

## ปัญหาทั่วไปและแนวทางแก้ไข
- **รูปภาพไม่ถูกแคช:** โดยทั่วไปเรียก `cacheData()` เสมอสำหรับ PSD ขนาดใหญ่ตลอด `OutOfMemoryError`
- **การเปลี่ยนสีที่ไม่คาดคิด:** คอนโซล `setPhotometric` สีทึบสีเป้าหมายของคุณ (RGB เทียบกับ CMYK)
- **ไม่พบไฟล์:** แผงควบคุมสำหรับ `dataDir` ชี้ไปยังความถูกต้องและชื่อไฟล์สะกดถูกต้อง

## คำถามที่พบบ่อย

### Q1: Aspose.PSD รองรับรูปแบบภาพที่แตกต่างกันอย่างมาก?

คำตอบที่ 1: จริง, Aspose.PSD นำเสนอรูปแบบภาพที่แสดงถึงข้อมูลของคุณ

### คำถามที่ 2: จะต้องขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร?

A2: ไม่เคยได้รับใบอนุญาตชั่วคราวจาก [ที่นี่](https://purchase.aspose.com/temporary-license/)

### Q3: เอกสารของ Aspose.PSD จากที่ไหน?

A3: เอกสารพร้อมให้บริการที่ [ที่นี่](https://reference.aspose.com/psd/java/)

### Q4: คุณต้องการอะไรบ้างสำหรับ Aspose.PSD?

A4: สำหรับความต้องการของคุณอีกครั้ง [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)

### Q5: ยังคง Aspose.PSD ได้หรือไม่?

A5: ได้อีกต่อไปแล้ว Aspose.PSD ได้จาก [ที่นี่](https://purchase.aspose.com/buy)

## บทสรุป

ตอนนี้คุณรู้แล้วว่า **how to convert PSD to TIFF** และทำ **image contrast adjustment** ด้วย Aspose.PSD for Java ขั้นตอนเหล่านี้ให้การควบคุมคุณภาพภาพอย่างละเอียดพร้อมกับโค้ดที่สะอาดและบำรุงรักษาง่าย อย่าลังเลที่จะลองเมธอดการปรับอื่น ๆ เช่น `adjustBrightness` หรือ `adjustGamma` เพื่อให้ตรงกับความต้องการของคุณ

---

**Last Updated:** 2026-02-25  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}