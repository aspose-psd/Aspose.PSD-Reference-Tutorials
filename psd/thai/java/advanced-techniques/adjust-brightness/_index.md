---
date: 2026-09-28
description: บทเรียนการประมวลผลภาพด้วย Java แสดงวิธีปรับความสว่างของภาพโดยใช้ Aspose.PSD
  for Java. ทำตามโค้ดทีละขั้นตอนเพื่อโหลด, แก้ไข และบันทึกไฟล์ PSD หรือ TIFF.
keywords:
- java image processing
- aspose psd java
- java image manipulation
- adjust brightness java
lastmod: 2026-09-28
linktitle: ปรับความสว่างของภาพ
og_description: บทเรียนการประมวลผลภาพด้วย Java แสดงวิธีปรับความสว่างของภาพโดยใช้ Aspose.PSD
  for Java. ทำตามโค้ดทีละขั้นตอนเพื่อโหลด, แก้ไข และบันทึกไฟล์ PSD หรือ TIFF.
og_image_alt: Guide to adjusting image brightness in Java using Aspose.PSD
og_title: 'การประมวลผลภาพด้วย Java: ปรับความสว่างด้วย Aspose.PSD'
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  headline: 'Java image processing: adjust brightness with Aspose.PSD'
  type: TechArticle
- description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  name: 'Java image processing: adjust brightness with Aspose.PSD'
  steps:
  - name: Load the image
    text: The `RasterImage` class represents a rasterized version of a PSD or TIFF
      file in memory. It provides direct pixel access for color‑correction operations.
      In this step, we load the target image and cast it to a `RasterImage` for further
      processing.
  - name: Adjust brightness
    text: '`adjustBrightness(int value)` changes the lightness of every pixel by the
      specified integer value. Positive numbers brighten the image; negative numbers
      darken it. The method processes the image in‑place, so no additional object
      creation is required. Here, we use the `adjustBrightness` method to mod'
  - name: Set TiffOptions
    text: '`TiffOptions` specifies the encoding parameters for TIFF output, such as
      bits per sample and photometric interpretation. It lets you control how the
      resulting file is encoded. Configure the `TiffOptions` for saving the adjusted
      image. Adjust the `bitsPerSample` and `photometric` properties based on '
  - name: Save the resultant image
    text: Calling `save` writes the processed raster data to a file using the previously
      defined options. The operation is atomic and guarantees that the output file
      is a valid TIFF image. Finally, save the modified image using the specified
      `TiffOptions`.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports JPEG, PNG, BMP, GIF, and many other
      raster formats in addition to PSD and TIFF.
    question: Can I adjust brightness in other image formats besides PSD?
  - answer: Wrap the processing code in a try‑catch block and catch `IOException`
      or `ImageProcessingException` to manage file‑access and raster‑operation errors.
    question: How can I handle errors during the image adjustment process?
  - answer: The method accepts integer values from –255 to +255; values outside this
      range are clamped to the nearest limit.
    question: Is there a limit to the range of brightness adjustment?
  - answer: Yes, a commercial license is required for production use. Purchase a license
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial projects?
  - answer: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose psd
- java image manipulation
title: 'การประมวลผลภาพด้วย Java: ปรับความสว่างด้วย Aspose.PSD'
url: /th/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ปรับความสว่างของภาพด้วย Aspose.PSD for Java

## บทนำ

ในบทแนะนำ **java image processing** นี้ คุณจะได้เรียนรู้วิธีปรับความสว่างของรูปภาพโดยตรงจากโค้ด Java การปรับความสว่างเป็นงานที่ทำบ่อยสำหรับนักออกแบบกราฟิก, ช่างภาพ, และผู้ที่สร้าง pipeline การประมวลผลภาพ ในนำทาง **java image manipulation** นี้ เราจะเดินผ่านขั้นตอนทั้งหมด—การโหลด PSD/TIFF, การใช้ค่าออฟเซ็ตความสว่าง, และการบันทึกผลลัพธ์—โดยใช้ไลบรารี Aspose.PSD for Java

## คำตอบอย่างรวดเร็ว
- **ไลบรารีใดจัดการความสว่าง?** Aspose.PSD for Java.  
- **เมธอดใดเปลี่ยนความสว่าง?** `RasterImage.adjustBrightness()`.  
- **ฉันสามารถทำงานกับไฟล์ PSD และ TIFF ได้หรือไม่?** Yes, the API supports both formats and 10+ additional image types.  
- **ฉันต้องการไลเซนส์สำหรับการใช้งานจริงหรือไม่?** A commercial license is required for non‑evaluation use.  
- **การดำเนินการใช้เวลานานเท่าไหร่?** Typically under 10 minutes for a basic adjustment.

## java image processing คืออะไร?
`Java image processing` หมายถึงชุดเทคนิคที่ทำให้คุณสามารถอ่าน, แปลง, และเขียนข้อมูลภาพโดยใช้ Java อย่างโปรแกรมเมติก การปรับความสว่างเป็นหนึ่งในการดำเนินการหลักที่เปลี่ยนความสว่างโดยรวมของพิกเซลแต่ละจุด ทำให้พื้นที่มืดสว่างขึ้นหรือพื้นที่สว่างมืดลง

## ทำไมต้องใช้ Aspose.PSD for Java?
Aspose.PSD for Java ให้โซลูชันที่ครอบคลุมและเป็น pure‑Java ที่รองรับรูปแบบ raster และ vector มากมาย, ขจัดการพึ่งพา native, และให้การแคชประสิทธิภาพสูงสำหรับไฟล์ขนาดใหญ่ API ที่กว้างขวางของมันทำให้นักพัฒนาสามารถทำการแก้ไขการปรับสีและการแก้ไขแบบชั้นได้อย่างซับซ้อนด้วยโค้ดน้อย ทำให้เหมาะสำหรับการปรับเล็กน้อยและ pipeline การประมวลผลภาพขั้นสูง
- **รองรับรูปแบบ raster และ vector มากกว่า 10 แบบ** – PSD, TIFF, JPEG, PNG, BMP, GIF, and more.  
- **การทำงานแบบ Pure‑Java** – no native DLLs or external dependencies, so it works on any JVM.  
- **การแคชประสิทธิภาพสูง** – raster data can be cached, enabling up to 2× faster repeated edits on large files.  
- **API ครอบคลุม** – over 150 methods for color correction, layer handling, masks, and compositing.

## ข้อกำหนดเบื้องต้น

ก่อนจะเริ่มบทแนะนำนี้ โปรดตรวจสอบว่าคุณมีข้อกำหนดต่อไปนี้:
- Aspose.PSD for Java Library: ดาวน์โหลดและติดตั้งไลบรารีจาก [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).  
- Java Development Kit (JDK) 8 หรือสูงกว่า ที่ติดตั้งบนเครื่องของคุณ.  
- สภาพแวดล้อมการพัฒนา (IDE) เช่น IntelliJ IDEA, Eclipse, หรือ VS Code.

## นำเข้าแพ็กเกจ

เพื่อเริ่มต้น ให้นำเข้าแพ็กเกจที่จำเป็นเข้าสู่โครงการ Java ของคุณ ในตัวอย่างนี้ เราจะใช้ดังต่อไปนี้:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

ต่อไปนี้ เราจะแบ่งกระบวนการปรับความสว่างของภาพออกเป็นขั้นตอนง่าย ๆ:

## วิธีปรับความสว่างโดยใช้ Aspose.PSD?

โหลดภาพต้นฉบับของคุณ, ใช้ค่าออฟเซ็ตความสว่าง, กำหนดตัวเลือกการบันทึก, และเขียนผลลัพธ์ลงดิสก์—ทั้งหมดในสี่ขั้นตอนสั้น ๆ ส่วนต่อไปนี้ให้คำแนะนำที่ชัดเจนแบบขั้นตอนต่อขั้นตอนที่คุณสามารถคัดลอกไปใช้ในโปรเจกต์ของคุณ วิธีนี้ทำให้แต่ละการดำเนินการทำอย่างมีประสิทธิภาพและภาพสุดท้ายคงคุณภาพเดิมพร้อมแสดงการเปลี่ยนแปลงความสว่างที่ต้องการ

### ขั้นตอนที่ 1: โหลดภาพ

`RasterImage` class แสดงเวอร์ชัน raster ของไฟล์ PSD หรือ TIFF ที่อยู่ในหน่วยความจำ มันให้การเข้าถึงพิกเซลโดยตรงสำหรับการดำเนินการแก้สี

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

ในขั้นตอนนี้ เราโหลดภาพเป้าหมายและแคสต์เป็น `RasterImage` เพื่อดำเนินการต่อ

### ขั้นตอนที่ 2: ปรับความสว่าง

`adjustBrightness(int value)` เปลี่ยนความสว่างของพิกเซลทุกจุดตามค่าจำนวนเต็มที่ระบุ ตัวเลขบวกทำให้ภาพสว่างขึ้น; ตัวเลขลบทำให้มืดลง เมธอดนี้ประมวลผลภาพในที่เดียวจึงไม่ต้องสร้างอ็อบเจกต์เพิ่มเติม

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

ที่นี่ เราใช้เมธอด `adjustBrightness` เพื่อปรับความสว่างของภาพ ในตัวอย่างนี้ เราลดความสว่างลง 50 หน่วย แต่คุณสามารถปรับค่าตามความต้องการของคุณ

### ขั้นตอนที่ 3: ตั้งค่า TiffOptions

`TiffOptions` กำหนดพารามิเตอร์การเข้ารหัสสำหรับการส่งออกเป็น TIFF เช่น bits per sample และ photometric interpretation มันให้คุณควบคุมวิธีการเข้ารหัสไฟล์ผลลัพธ์

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

กำหนดค่า `TiffOptions` เพื่อบันทึกภาพที่ปรับแล้ว ปรับค่า `bitsPerSample` และ `photometric` ตามความต้องการของคุณ

### ขั้นตอนที่ 4: บันทึกภาพที่ได้

การเรียก `save` จะเขียนข้อมูล raster ที่ประมวลผลแล้วลงไฟล์โดยใช้ตัวเลือกที่กำหนดไว้ก่อนหน้านี้ การดำเนินการนี้เป็นแบบ atomic และรับประกันว่าไฟล์ผลลัพธ์เป็นภาพ TIFF ที่ถูกต้อง

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|----------|
| **`ClassCastException` เมื่อทำการแคสต์ Image** | ไฟล์ไม่ใช่ภาพ raster (เช่น PSD แบบเวกเตอร์) | ตรวจสอบรูปแบบไฟล์ต้นฉบับหรือใช้ `image instanceof RasterImage` ก่อนทำการแคสต์. |
| **การเปลี่ยนความสว่างไม่มีผล** | ภาพไม่ได้ถูกแคชก่อนการปรับความสว่าง. | เรียก `rasterImage.cacheData()` ตามที่แสดงในขั้นตอน 1. |
| **ไฟล์ที่บันทึกดูเหมือนเสียหาย** | การกำหนดค่า `TiffOptions` ไม่ถูกต้อง. | ตรวจสอบให้แน่ใจว่า `bitsPerSample` ตรงกับความลึกของภาพต้นฉบับ (โดยปกติ 8‑บิตต่อช่อง). |

## คำถามที่พบบ่อย

**Q: ฉันสามารถปรับความสว่างในรูปแบบภาพอื่น ๆ นอกจาก PSD ได้หรือไม่?**  
A: ใช่, Aspose.PSD for Java รองรับ JPEG, PNG, BMP, GIF, และรูปแบบ raster อื่น ๆ มากมาย นอกเหนือจาก PSD และ TIFF.

**Q: ฉันจะจัดการข้อผิดพลาดระหว่างกระบวนการปรับภาพอย่างไร?**  
A: ห่อโค้ดการประมวลผลด้วยบล็อก try‑catch และจับ `IOException` หรือ `ImageProcessingException` เพื่อจัดการข้อผิดพลาดการเข้าถึงไฟล์และการดำเนินการ raster.

**Q: มีขอบเขตจำกัดสำหรับการปรับความสว่างหรือไม่?**  
A: เมธอดรับค่าจำนวนเต็มตั้งแต่ –255 ถึง +255; ค่าที่อยู่นอกช่วงนี้จะถูกจำกัดให้อยู่ที่ขอบเขตที่ใกล้ที่สุด.

**Q: ฉันสามารถใช้ Aspose.PSD for Java ในโครงการเชิงพาณิชย์ได้หรือไม่?**  
A: ใช่, จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานในผลิตภัณฑ์ ซื้อไลเซนส์ได้จาก [here](https://purchase.aspose.com/buy).

**Q: มีการทดลองใช้ฟรีหรือไม่?**  
A: มี, คุณสามารถทดลองใช้ไลบรารีได้จาก [here](https://releases.aspose.com/).

**Q: เมธอด `adjustBrightness` มีผลต่อการมองเห็นของเลเยอร์หรือไม่?**  
A: เมธอดทำงานบนภาพคอมโพสิตที่ rasterized ดังนั้นเลเยอร์ที่ซ่อนจะถูกละเว้นระหว่างการ rasterization ทำให้ผลลัพธ์ภาพตามที่ต้องการยังคงอยู่.

**Q: ฉันสามารถเชื่อมต่อการปรับหลายอย่างต่อเนื่อง (เช่น คอนทราสต์, ความอิ่มสี) ได้หรือไม่?**  
A: แน่นอน หลังจากปรับความสว่างแล้ว คุณสามารถเรียก `adjustContrast`, `adjustSaturation` หรือเมธอดการแก้สีอื่น ๆ บนอินสแตนซ์ `RasterImage` เดียวกันได้.

---

**อัปเดตล่าสุด:** 2026-09-28  
**ทดสอบกับ:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [ไลบรารีการประมวลผลภาพ Java: กลับด้านเลเยอร์ด้วย Aspose.PSD](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [แปลงภาพเป็นระดับสีเทาโดยใช้ Aspose.PSD for Java](/psd/java/advanced-techniques/grayscale-image/)
- [วิธีหมุนภาพด้วยมุมเฉพาะโดยใช้ Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}