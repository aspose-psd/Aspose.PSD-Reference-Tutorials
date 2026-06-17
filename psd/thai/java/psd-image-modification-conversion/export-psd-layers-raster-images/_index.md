---
date: 2026-03-26
description: เรียนรู้วิธีส่งออกเลเยอร์ PSD เป็น PNG ด้วย Aspose.PSD สำหรับ Java. แปลงไฟล์
  PSD เป็นภาพเรสเตอร์และส่งออกเลเยอร์ PSD เป็นชุดอย่างมีประสิทธิภาพ.
linktitle: Export psd layers to png using Java
second_title: Aspose.PSD Java API
title: ส่งออกเลเยอร์ PSD เป็น PNG ด้วย Java
url: /th/java/psd-image-modification-conversion/export-psd-layers-raster-images/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออกชั้น PSD เป็น PNG ด้วย Java

## คำแนะนำ

ในโลกของการออกแบบดิจิทัล การทำงานกับภาพหลายชั้นอาจเป็นทั้งโอกาสและความท้าทาย ลองนึกภาพว่าคุณใช้เวลาหลายชั่วโมงสร้างภาพที่ยอดเยี่ยมใน Photoshop (รูปแบบ PSD) พร้อมกับหลายชั้นที่ทำให้การออกแบบของคุณมีชีวิตชีวา ตอนนี้คุณอาจต้องการ **export psd layers to png** แยกกันเพื่อใช้งานต่อไป นี่คือจุดที่ Aspose.PSD for Java ส่องแสงสว่างโดยอัตโนมัติงานที่น่าเบื่อในการแปลงแต่ละชั้นจากไฟล์ PSD ให้เป็นภาพราสเตอร์คุณภาพสูงเช่น PNG ในคู่มือฉบับเต็มนี้ เราจะพาคุณผ่านกระบวนการทั้งหมด ตั้งแต่การตั้งค่าสภาพแวดล้อมจนถึงการส่งออกชั้น PSD เป็นกลุ่มด้วยเพียงไม่กี่บรรทัดของโค้ด

## คำตอบอย่างรวดเร็ว
- **บทเรียนนี้ครอบคลุมอะไร?** การส่งออกแต่ละชั้น PSD เป็นไฟล์ PNG โดยใช้ Aspose.PSD for Java.  
- **ประโยชน์หลัก?** ประหยัดเวลาหลายชั่วโมงเมื่อเทียบกับการดึงข้อมูลด้วยตนเองใน Photoshop.  
- **ข้อกำหนดเบื้องต้น?** JDK 8+, ไลบรารี Aspose.PSD, และไฟล์ PSD ตัวอย่าง.  
- **สามารถส่งออกเป็นรูปแบบราสเตอร์อื่นได้หรือไม่?** ได้ – คุณสามารถแปลง PSD เป็นรูปแบบราสเตอร์เช่น BMP, TIFF หรือ JPEG.  
- **รองรับการประมวลผลแบบกลุ่มหรือไม่?** แน่นอน; ลูปในโค้ดช่วยให้คุณส่งออกชั้น PSD เป็นกลุ่มได้ในครั้งเดียว.

## psd layers to png คืออะไร?
การ **export psd layers to png** หมายถึงการนำแต่ละชั้นจากเอกสาร Photoshop มาเก็บเป็นไฟล์ PNG แยกต่างหาก PNG รักษาความโปร่งใส ทำให้เหมาะสำหรับกราฟิกเว็บ, สินทรัพย์ UI, และการประมวลผลภาพต่อไป

## ทำไมต้องใช้ Aspose.PSD for Java?
- **ไม่ต้องใช้ Photoshop** – ทำงานบนเซิร์ฟเวอร์หรือสภาพแวดล้อม CI ใดก็ได้.  
- **ความแม่นยำสูง** – รักษาเอฟเฟกต์ของชั้น, มาสก์, และแชนแนลอัลฟ่า.  
- **ขยายได้** – เหมาะสำหรับการส่งออกชั้น PSD เป็นกลุ่มใน pipeline อัตโนมัติ.  

## ข้อกำหนดเบื้องต้น

ก่อนจะลงมือเขียนโค้ด โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

1. **Java Development Kit (JDK)** – เวอร์ชัน 8 หรือสูงกว่า.  
2. **Aspose.PSD for Java** – ดาวน์โหลดไลบรารีล่าสุดจาก [Aspose Releases](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse หรือเครื่องมือแก้ไขใดที่คุณชอบ.  
4. **ไฟล์ PSD ตัวอย่าง** – เช่น `sample.psd`, วางไว้ในโฟลเดอร์โปรเจกต์ของคุณ.

ตอนนี้คุณพร้อมแล้ว เริ่มเขียนโค้ดกันเถอะ!

## นำเข้าแพ็กเกจ

ก่อนอื่นให้นำเข้าคลาสที่จำเป็นจากไลบรารี Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

การนำเข้าดังกล่าวทำให้คุณเข้าถึงการโหลดภาพ, ตัวเลือก PNG, และการจัดการชั้นได้

## ขั้นตอนที่ 1: กำหนดไดเรกทอรีเอกสารของคุณ

ระบุที่ตั้งของไฟล์ PSD ต้นฉบับและไฟล์ PNG ที่จะสร้างผลลัพธ์:

```java
String dataDir = "Your Document Directory";
```

แทนที่ `"Your Document Directory"` ด้วยพาธแบบ absolute หรือ relative ไปยัง `sample.psd`

## ขั้นตอนที่ 2: โหลดไฟล์ PSD

โหลด PSD เข้าไปในอ็อบเจ็กต์ `PsdImage` เพื่อให้คุณสามารถทำงานกับชั้นต่าง ๆ ได้:

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

การแคสต์เป็น `PsdImage` จะเปิดใช้งานฟังก์ชันเฉพาะชั้น

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือก PNG

ตั้งค่าพารามิเตอร์การส่งออก PNG การใช้ `TruecolorWithAlpha` จะคงความโปร่งใสไว้:

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## ขั้นตอนที่ 4: วนลูปผ่านชั้นและส่งออกแต่ละชั้น

วนลูปผ่านทุกชั้นและบันทึกเป็นไฟล์ PNG แยกแต่ละไฟล์ ลูปนี้ทำให้ **batch export psd layers** ทำงานอัตโนมัติ:

```java
for (int i = 0; i < psdImage.getLayers().length; i++) {
    // Convert and save the layer to PNG file format.
    psdImage.getLayers()[i].save(dataDir + String.format("layer_out%d.png", i + 1), pngOptions);
}
```

แต่ละรอบของลูปจะสร้าง `layer_out1.png`, `layer_out2.png`, เป็นต้น

## ปัญหาทั่วไปและวิธีแก้

- **FileNotFoundException** – ตรวจสอบว่า `dataDir` ชี้ไปยังโฟลเดอร์ที่ถูกต้องและ `sample.psd` มีอยู่.  
- **OutOfMemoryError** – สำหรับไฟล์ PSD ขนาดใหญ่มาก ให้พิจารณาประมวลผลชั้นเป็นชุดเล็ก ๆ หรือเพิ่มขนาด heap ของ JVM (`-Xmx`).  
- **Missing Transparency** – ตรวจสอบว่าได้ตั้งค่า `pngOptions.setColorType(PngColorType.TruecolorWithAlpha)`; หากไม่ตั้งค่า PNG จะถูกบันทึกโดยไม่มีแชนแนลอัลฟ่า.

## คำถามที่พบบ่อย

### Aspose.PSD for Java คืออะไร?
Aspose.PSD for Java เป็นไลบรารีที่ทรงพลังซึ่งช่วยให้นักพัฒนาสามารถสร้าง, แก้ไข, แปลง, และเรนเดอร์ไฟล์ Photoshop ได้โดยไม่ต้องใช้ Adobe Photoshop

### ฉันสามารถส่งออกชั้นเป็นรูปแบบอื่นนอกจาก PNG ได้หรือไม่?
ได้, Aspose.PSD รองรับ BMP, TIFF, JPEG, และรูปแบบราสเตอร์อื่น ๆ อีกหลายรูปแบบ เพียงสร้างอ็อบเจ็กต์ตัวเลือกที่สอดคล้อง (เช่น `JpegOptions`) แล้วส่งผ่านให้เมธอด `save`

### มีการทดลองใช้ฟรีสำหรับ Aspose.PSD หรือไม่?
แน่นอน! คุณสามารถทดลองใช้ Aspose.PSD ฟรีโดยดาวน์โหลดจาก [free trial page](https://releases.aspose.com/)

### จะทำอย่างไรหากพบปัญหาในการใช้ Aspose.PSD?
คุณสามารถขอความช่วยเหลือและสนับสนุนจากชุมชน Aspose ได้โดยเยี่ยมชมฟอรั่มสนับสนุนของพวกเขา [here](https://forum.aspose.com/c/psd/34)

### ฉันสามารถซื้อไลเซนส์สำหรับ Aspose.PSD ได้จากที่ไหน?
คุณสามารถซื้อไลเซนส์สำหรับ Aspose.PSD ได้ง่าย ๆ จากหน้า purchase ของพวกเขา [here](https://purchase.aspose.com/buy)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-26  
**Tested With:** Aspose.PSD for Java 24.12 (latest)  
**Author:** Aspose