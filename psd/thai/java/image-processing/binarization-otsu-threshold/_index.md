---
date: 2026-01-09
description: เรียนรู้วิธีทำการแยกส่วนภาพด้วย Otsu โดยใช้ Aspose.PSD สำหรับ Java บทเรียนนี้ครอบคลุมการประมวลผลภาพด้วย
  Java วิธีทำให้เป็นภาพขาว‑ดำ และการใช้ค่าเกณฑ์ Otsu.
linktitle: Binarization with Otsu Threshold
second_title: Aspose.PSD Java API
title: การแบ่งส่วนภาพ Otsu – การทำไบนารีด้วยเกณฑ์ Otsu ใน Aspose.PSD สำหรับ Java
url: /th/java/image-processing/binarization-otsu-threshold/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การทำไบนารีด้วยค่าเกณฑ์ Otsu ใน Aspose.PSD สำหรับ Java

## บทนำ

ยินดีต้อนรับ! ในคู่มือแบบขั้นตอนนี้คุณจะได้เรียนรู้ **image segmentation otsu** โดยใช้ไลบรารี Aspose.PSD สำหรับ Java ไม่ว่าคุณจะกำลังสร้างเครื่องมือแก้ไขภาพ, ระบบอัตโนมัติสำหรับการวิเคราะห์เอกสาร, หรือโครงการ **java image processing** ใด ๆ การเชี่ยวชาญวิธีการทำไบนารีภาพด้วยค่าเกณฑ์ Otsu จะทำให้คุณมีวิธีที่เชื่อถือได้ในการสร้าง **binary image conversion** ที่สะอาด มาร่วมเดินผ่านกระบวนการทั้งหมด—ตั้งแต่การตั้งค่าสภาพแวดล้อมจนถึงการบันทึก JPEG สุดท้าย—เพื่อให้คุณสามารถใช้ Otsu ในแอปพลิเคชันของคุณได้

## คำตอบอย่างรวดเร็ว
- **Otsu threshold ทำอะไร?** มันจะค้นหาจุดตัดระดับสีเทาที่เหมาะสมที่สุดโดยอัตโนมัติเพื่อแยกพิกเซลพื้นหน้าและพื้นหลังออกจากกัน.  
- **ไลบรารีใดสนับสนุนใน Java?** Aspose.PSD สำหรับ Java มีเมธอดในตัว `binarizeOtsu()`.  
- **ฉันต้องมีใบอนุญาตเพื่อทดลองใช้งานหรือไม่?** มีการทดลองใช้ฟรี; จำเป็นต้องมีใบอนุญาตสำหรับการใช้งานในสภาพแวดล้อมการผลิต.  
- **รูปแบบผลลัพธ์ที่ฉันสามารถใช้ได้คืออะไร?** ตัวอย่างบันทึกเป็น JPEG, แต่รูปแบบใดก็ได้ที่ `RasterCachedImage.save()` รองรับก็ทำงานได้.  
- **การทำงานนี้ใช้เวลานานเท่าไหร่?** ด้วย API ที่พร้อมใช้ คุณสามารถมีโซลูชันทำงานได้ภายในไม่เกิน 10 นาที.

## อะไรคือ Image Segmentation Otsu?

**Image segmentation otsu** เป็นเทคนิคทางสถิติที่กำหนดค่าค่าเกณฑ์ที่เหมาะสมที่สุดสำหรับการแปลงภาพระดับสีเทาเป็นภาพไบนารี วิธีนี้ประเมินความแปรปรวนภายในคลาสของพื้นหน้าและพื้นหลังและเลือกค่าเกณฑ์ที่ทำให้ความแปรปรวนนี้น้อยที่สุด ส่งผลให้แยกวัตถุจากพื้นหลังได้อย่างชัดเจน

## ทำไมต้องใช้ Aspose.PSD สำหรับ Java?

- **High‑performance caching** – ทำงานอย่างมีประสิทธิภาพกับไฟล์ PSD ขนาดใหญ่.  
- **One‑line binarization** – `binarizeOtsu()` จัดการงานหนักให้.  
- **Cross‑format support** – โหลด PSD, ประมวลผล, และบันทึกเป็น JPEG, PNG ฯลฯ.  
- **Enterprise‑ready licensing** – เหมาะสำหรับการใช้งานเชิงพาณิชย์.

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะลงลึกในโค้ด โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

- **Java Development Environment** – ติดตั้ง JDK 8 หรือสูงกว่า.  
- **Aspose.PSD for Java Library** – ดาวน์โหลดจากเว็บไซต์อย่างเป็นทางการ [here](https://releases.aspose.com/psd/java/).  
- **Sample PSD File** – PSD ที่คุณต้องการทำไบนารี (เช่น `sample.psd`).  

## นำเข้าแพ็กเกจ

Begin by importing the necessary classes:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterCachedImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสารของคุณ

Define the folder that contains your source PSD and where the output will be written:

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: โหลดไฟล์ PSD

Load the PSD into an `Image` object so you can work with it:

```java
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## ขั้นตอนที่ 3: แคชภาพ

If the image isn’t already cached, cache it to improve processing speed:

```java
RasterCachedImage rasterCachedImage = (RasterCachedImage)image;

if (!rasterCachedImage.isCached()) {
    rasterCachedImage.cacheData();
}
```

## ขั้นตอนที่ 4: ทำไบนารีภาพด้วยค่าเกณฑ์ Otsu

Apply the Otsu algorithm—this is the core of **how to apply otsu** for a **binary image conversion**:

```java
rasterCachedImage.binarizeOtsu();
```

## ขั้นตอนที่ 5: บันทึกภาพที่ได้

Finally, write the binarized image to disk using `JpegOptions` (you could also use PNG or BMP):

```java
String destName = dataDir + "BinarizationWithOtsuThreshold_out.jpg";
rasterCachedImage.save(destName, new JpegOptions());
```

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|-----|
| **`ClassCastException`** | พยายามแคสต์ภาพที่ไม่ใช่ raster | ตรวจสอบให้แน่ใจว่า PSD มีเลเยอร์ raster หรือใช้ `image.convertToRasterImage()` ก่อนทำการแคสต์. |
| **Out‑of‑Memory** | ไฟล์ PSD ขนาดใหญ่ใช้ RAM มาก | เรียก `rasterCachedImage.cacheData()` ตั้งแต่ต้นและพิจารณาเพิ่มขนาด heap ของ JVM (`-Xmx`). |
| **Incorrect output colors** | ภาพไม่ได้แคชอย่างถูกต้อง | ตรวจสอบว่า `isCached()` คืนค่า `true` ก่อนเรียก `binarizeOtsu()`. |

## คำถามที่พบบ่อย

### Q1: การทำไบนารีด้วยค่าเกณฑ์ Otsu คืออะไร?
A1: การทำไบนารีด้วยค่าเกณฑ์ Otsu เป็นวิธีที่ใช้สำหรับการแบ่งส่วนภาพ แยกภาพเป็นพื้นหน้าและพื้นหลังโดยอิงจากการกำหนดค่าเกณฑ์ที่เหมาะสมที่สุด.

### Q2: ฉันสามารถใช้ Aspose.PSD สำหรับ Java ได้ฟรีหรือไม่?
A2: Aspose.PSD สำหรับ Java เป็นไลบรารีเชิงพาณิชย์ แต่คุณสามารถสำรวจคุณสมบัติต่าง ๆ ได้ด้วยการทดลองใช้ฟรี รับได้จาก [here](https://releases.aspose.com/).

### Q3: ฉันสามารถหาเอกสารของ Aspose.PSD สำหรับ Java ได้ที่ไหน?
A3: เอกสารพร้อมให้บริการที่ [here](https://reference.aspose.com/psd/java/).

### Q4: ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD สำหรับ Java อย่างไร?
A4: เยี่ยมชมฟอรั่ม Aspose.PSD ที่ [here](https://forum.aspose.com/c/psd/34) เพื่อรับการสนับสนุนจากชุมชน.

### Q5: มีใบอนุญาตชั่วคราวสำหรับ Aspose.PSD สำหรับ Java หรือไม่?
A5: มี, คุณสามารถรับใบอนุญาตชั่วคราวได้จาก [here](https://purchase.aspose.com/temporary-license/).

**Q: วิธีนี้เข้ากับกระบวนการทำงานของ java image processing ที่ใหญ่กว่ามีอย่างไร?**  
A: หลังจากทำไบนารีแล้ว คุณสามารถส่งภาพไบนารีไปยังโมดูลการตรวจจับคอนทัวร์, การเตรียมข้อมูล OCR, หรือการวิเคราะห์รูปทรงได้

**Q: ฉันสามารถปรับพารามิเตอร์ของอัลกอริธึม Otsu ได้หรือไม่?**  
A: เมธอด `binarizeOtsu()` ใช้การทำงานมาตรฐานของ Otsu; หากต้องการค่าเกณฑ์ที่กำหนดเอง ให้ใช้ `binarize(int threshold)` แทน

## สรุป

ตอนนี้คุณได้เห็นวิธีการทำ **image segmentation otsu, ใช้ `binarizeOtsu()`, และบันทึกผลลัพธ์—คุณสามารถรวมการแปลงภาพไบนารีที่แข็งแกร่งเข้าไปในโครงการ **java image processing** ใด ๆ ทดลองกับไฟล์ต้นแบบต่าง ๆ, ผสานผลลัพธ์กับ OCR, หรือสร้างตัวประมวลผลแบบแบตช์เพื่อจัดการหลาย PSD โดยอัตโนมัติ

---

**อัปเดตล่าสุด:** 2026-01-09  
**ทดสอบด้วย:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}