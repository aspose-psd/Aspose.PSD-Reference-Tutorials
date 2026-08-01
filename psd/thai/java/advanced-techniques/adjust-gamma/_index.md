---
date: 2026-08-01
description: เรียนรู้วิธีปรับค่าแกมม่าในการประมวลผลภาพด้วย Java และ Aspose.PSD, แปลง
  PSD เป็น TIFF, และแก้ไขภาพที่ซีดจางในบทเรียนสั้นๆ
keywords:
- how to adjust gamma
- fix washed out image
- java image processing
- convert psd to tiff
- server side image processing
lastmod: 2026-08-01
linktitle: ปรับค่าแกมม่าให้กับภาพ
og_description: เรียนรู้วิธีปรับค่าแกมม่าในการประมวลผลภาพด้วย Java โดยใช้ Aspose.PSD
  – ไลบรารีที่เร็วและทำงานบนเซิร์ฟเวอร์ที่ช่วยแก้ไขภาพซีดจางและแปลง PSD เป็น TIFF
  เพียงไม่กี่บรรทัดของโค้ด
og_image_alt: 'Guide: Adjust gamma in Java images with Aspose.PSD, convert PSD to
  TIFF'
og_title: วิธีปรับค่าแกมม่า – การประมวลผลด้วย Java และ Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  headline: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  type: TechArticle
- description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  name: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  steps:
  - name: '**Java Development Environment** – Java 8 or later installed.'
    text: '**Java Development Environment** – Java 8 or later installed.'
  - name: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
    text: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
  type: HowTo
- questions:
  - answer: Yes – the `adjustGamma` method accepts separate float values for red,
      green, and blue channels.
    question: Can I apply different gamma values to each colour channel?
  - answer: Absolutely. You can perform resizing, cropping, or colour corrections
      sequentially on the same `RasterImage` instance.
    question: Is it possible to chain multiple image adjustments before saving?
  - answer: Yes, each layer can be accessed and processed individually.
    question: Does Aspose.PSD support multi‑page PSD files?
  - answer: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective
      options classes.
    question: What format can I export to besides TIFF?
  - answer: Start with a moderate gamma (around 2.0) and preview the result; adjust
      downwards if the image looks too bright.
    question: How do I avoid a washed‑out image after gamma correction?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- adjust gamma
- Aspose.PSD
- Java image processing
- PSD to TIFF
- server side processing
title: วิธีปรับค่าแกมม่าในการประมวลผลภาพด้วย Java และ Aspose.PSD
url: /th/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีปรับแกมม่าในการประมวลผลภาพ Java ด้วย Aspose.PSD

## บทนำ

หากคุณกำลังทำงานกับ **java image processing** การเรียนรู้ **วิธีปรับแกมม่า** เป็นเทคนิคพื้นฐานเพื่อปรับปรุงความสว่างและคอนทราสต์โดยไม่สูญเสียรายละเอียด ในบทเรียนนี้เราจะอธิบายวิธีใช้ **Aspose.PSD for Java** เพื่อทำการแก้ไข gamma ให้กับไฟล์ PSD, **convert PSD to TIFF**, และหลีกเลี่ยง **washed‑out image** คุณจะเห็นว่าทำไมวิธีนี้จึงเร็ว เชื่อถือได้ และเหมาะสำหรับ **server‑side image processing** pipelines

## คำตอบด่วน
- **What does gamma correction do?** มันทำการแมปค่าความสว่างใหม่เพื่อทำให้พื้นที่มืดสว่างขึ้นหรือพื้นที่สว่างมืดลงในขณะที่ยังคงรักษารายละเอียดโดยรวมไว้  
- **Which library handles the processing?** Aspose.PSD for Java มีเมธอด `adjustGamma` เฉพาะสำหรับภาพแรสเตอร์  
- **Can I convert PSD to TIFF in the same flow?** ใช่ – หลังจากปรับแกมม่าแล้วคุณสามารถบันทึกภาพโดยตรงเป็น TIFF ด้วย `TiffOptions`  
- **Do I need a license for development?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการทดสอบ; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานในสภาพแวดล้อมจริง  
- **What Java version is supported?** Aspose.PSD รองรับ Java 8 ขึ้นไป  

## Java Gamma Correction คืออะไร

การแก้ไข gamma เปลี่ยนความสัมพันธ์เชิงไม่เชิงเส้นระหว่างค่าพิกเซลที่เข้ารหัสกับความสว่างที่แสดงผล โดยการปรับแต่งเส้นโค้ง gamma คุณสามารถ **fix washed out image** ปัญหา หรือเพิ่มรายละเอียดในเงาโดยไม่ทำให้ไฮไลท์สว่างเกินไป มันทำงานโดยการใช้ฟังก์ชันพาวเวอร์‑ลอว์กับแต่ละพิกเซล ซึ่งทำให้โทนสีมืดสว่างขึ้นและบีบอัดไฮไลท์ ส่งผลให้ภาพดูเป็นธรรมชาติมากขึ้น  

## ทำไมต้องใช้ Aspose.PSD สำหรับ Gamma Correction

Aspose.PSD เป็น **java image processing library** ที่ทำให้ซับซ้อนของรูปแบบ PSD ถูกซ่อนอยู่ มันรองรับการประมวลผลไฟล์ขนาดสูงสุดถึง 2 GB, รองรับรูปแบบภาพกว่า 50 แบบต่าง ๆ, และให้เมธอด `adjustGamma` ที่ง่ายต่อการใช้งาน ทำให้เหมาะสำหรับ **java gamma correction** และ **convert PSD to TIFF** workflow  

## ข้อกำหนดเบื้องต้น

1. **Java Development Environment** – ติดตั้ง Java 8 หรือรุ่นใหม่กว่า  
2. **Aspose.PSD Library** – ดาวน์โหลดและเพิ่มไฟล์ JAR ไปยังโปรเจกต์ของคุณ ดูที่ [documentation](https://reference.aspose.com/psd/java/) อย่างเป็นทางการ  
3. **Sample Image** – ไฟล์ PSD ที่คุณต้องการประมวลผล (เช่น `sample.psd`)  

## นำเข้าแพ็กเกจ

ก่อนเริ่มต้น ให้นำเข้าเนมสเปซที่จำเป็นซึ่งให้คุณเข้าถึงการจัดการแรสเตอร์และตัวเลือกรูปแบบไฟล์  

## ขั้นตอนที่ 1: โหลดภาพ

คลาส `RasterImage` แสดงข้อมูลพิกเซลที่แรสเตอร์ของเลเยอร์ PSD ในหน่วยความจำ การโหลดภาพเพียงครั้งเดียวและแคชไว้ช่วยลดการใช้หน่วยความจำสำหรับการปรับแต่งต่อไป  

## ขั้นตอนที่ 2: ปรับ Gamma

โหลด PSD ของคุณด้วย `new RasterImage("sample.psd")` แล้วเรียก `rasterImage.adjustGamma(2.0f)` — บรรทัดเดียวนี้จะใช้ค่า gamma 2.0 กับทุกช่องสี ทำให้เงาสว่างขึ้นในขณะที่ไฮไลท์ยังคงอยู่ คุณสามารถส่งค่าที่แตกต่างกันสำหรับสีแดง เขียว และน้ำเงินได้หากต้องการปรับแต่งแยกช่อง  

## ขั้นตอนที่ 3: สร้าง TiffOptions

`TiffOptions` ให้คุณควบคุมการบีบอัด, บิตต่อตัวอย่าง, และการตั้งค่าเฉพาะของ TIFF การตั้งค่าเป็นตัวอย่าง 8‑bit (`{8,8,8}`) ทำให้ขนาดไฟล์ TIFF อยู่ในระดับที่เหมาะสมพร้อมคงความแม่นยำของสี  

## ขั้นตอนที่ 4: บันทึกภาพที่ได้

เรียก `rasterImage.save("output.tif", tiffOptions)` เพื่อบันทึกภาพที่ประมวลผลลงดิสก์ หลังจากบันทึกแล้วคุณสามารถส่งไฟล์ TIFF ไปยังระบบต่อเนื่อง เช่น บริการพิมพ์หรือเว็บ API  

## กรณีการใช้งานทั่วไป

- **Automated graphics pipelines** – ปรับ gamma แบบเรียลไทม์ก่อนสร้างภาพย่อ  
- **Batch conversion tools** – แปลงคลัง PSD ขนาดใหญ่เป็น TIFF พร้อมทำให้ความสว่างเป็นมาตรฐาน  
- **Web services** – เปิดเผย endpoint ที่รับ PSD, ทำการแก้ไข gamma, และส่งคืนเป็น TIFF ให้ลูกค้าใช้งาน  

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|----------|
| **Image appears washed out** | ค่า gamma สูงเกินไป (เช่น > 2.5) | ลดค่า gamma ลงให้อยู่ระหว่าง 1.8 ถึง 2.2 |
| **`rasterImage.isCached()` returns false** | ภาพยังไม่ได้โหลดเข้าสู่หน่วยความจำ | เรียก `rasterImage.cacheData()` ก่อนปรับ gamma |
| **TIFF file size is large** | ตั้งค่าบิตต่อตัวอย่างเป็น 16‑bit | ใช้ตัวอย่าง 8‑bit (`{8,8,8}`) ตามตัวอย่าง |

## คำถามที่พบบ่อย

**Q: สามารถใช้ค่า gamma ที่แตกต่างกันสำหรับแต่ละช่องสีได้หรือไม่?**  
A: ใช่ – เมธอด `adjustGamma` ยอมรับค่าจำนวนจริง (float) แยกสำหรับช่องสีแดง, เขียว, และน้ำเงิน  

**Q: สามารถเชื่อมต่อการปรับภาพหลายขั้นตอนก่อนบันทึกได้หรือไม่?**  
A: แน่นอน คุณสามารถทำการปรับขนาด, ครอป, หรือแก้ไขสีตามลำดับบนอินสแตนซ์ `RasterImage` เดียวกัน  

**Q: Aspose.PSD รองรับไฟล์ PSD แบบหลายหน้าไหม?**  
A: ใช่, แต่ละเลเยอร์สามารถเข้าถึงและประมวลผลได้แยกกัน  

**Q: สามารถส่งออกเป็นรูปแบบอื่นนอกจาก TIFF ได้หรือไม่?**  
A: Aspose.PSD รองรับ PNG, JPEG, BMP, และรูปแบบอื่น ๆ อีกหลายรูปแบบผ่านคลาสตัวเลือกที่เกี่ยวข้อง  

**Q: จะหลีกเลี่ยงภาพที่ดู washed‑out หลังการแก้ไข gamma ได้อย่างไร?**  
A: เริ่มต้นด้วยค่า gamma ปานกลาง (ประมาณ 2.0) แล้วดูตัวอย่างผลลัพธ์; ปรับค่าลงหากภาพดูสว่างเกินไป  

## สรุป

ขอแสดงความยินดี! คุณได้เรียนรู้ **how to adjust gamma** ใน workflow **java image processing** อย่างสำเร็จ, แปลง PSD เป็น TIFF, และหลีกเลี่ยงข้อผิดพลาดทั่วไปเช่น **washed‑out image** รูปแบบนี้ให้การควบคุมความสว่างและคอนทราสต์อย่างละเอียด ทำให้เหมาะสำหรับ pipelines กราฟิกอัตโนมัติ, เว็บเซอร์วิส, หรือยูทิลิตี้บนเดสก์ท็อป  

---

**Last Updated:** 2026-08-01  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทเรียนที่เกี่ยวข้อง

- [บทแนะนำการประมวลผลภาพ Java - ปรับความสว่างของภาพด้วย Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-brightness/)
- [วิธีแปลง PSD เป็น TIFF และปรับคอนทราสต์ด้วย Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-contrast/)
- [แปลง PSD เป็นภาพใน Java – ใช้ Adjustment Layers ด้วย Aspose.PSD](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```