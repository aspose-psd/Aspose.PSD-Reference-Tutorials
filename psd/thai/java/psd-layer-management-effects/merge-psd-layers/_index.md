---
date: 2026-04-05
description: เรียนรู้วิธีส่งออกไฟล์ PSD เป็น PNG และรวมเลเยอร์ PSD ด้วย Aspose.PSD
  สำหรับ Java รวมถึงการแปลง PSD เป็น JPEG การตั้งค่าคุณภาพ JPEG และเคล็ดลับการแปลง
  PSD เป็น TIFF
keywords:
- export psd to png
- convert psd to jpeg
- how to merge psd
- set jpeg quality
- psd to tiff conversion
linktitle: ส่งออก PSD เป็น PNG และรวมเลเยอร์โดยใช้ Aspose.PSD สำหรับ Java
second_title: Aspose.PSD Java API
title: ส่งออก PSD เป็น PNG และรวมเลเยอร์โดยใช้ Aspose.PSD สำหรับ Java
url: /th/java/psd-layer-management-effects/merge-psd-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก PSD เป็น PNG และรวมเลเยอร์โดยใช้ Aspose.PSD สำหรับ Java

## บทนำ

เคยสงสัยไหมว่าผู้เชี่ยวชาญด้านกราฟิกทำอย่างไรถึงได้สร้างภาพที่ซับซ้อนและมีหลายเลเยอร์ใน Photoshop? ความลับมักอยู่ที่การ **exporting PSD to PNG** และการรวมเลเยอร์อย่างชาญฉลาด หากคุณทำงานกับไฟล์ PSD ใน Java การเชี่ยวชาญเทคนิคเหล่านี้จะช่วยให้คุณสร้างภาพคอมโพสิต ลดขนาดไฟล์ และเตรียมทรัพยากรสำหรับการใช้งานบนเว็บหรือมือถือ ในบทเรียนนี้เราจะอธิบาย **how to merge PSD** เลเยอร์โดยใช้ Aspose.PSD for Java และเราจะสาธิตวิธีส่งออกผลลัพธ์เป็น PNG (หรือ JPEG/TIFF เมื่อจำเป็น) เมื่อเสร็จคุณจะสามารถทำงานอัตโนมัติการจัดการเลเยอร์และกระบวนการส่งออกโดยตรงจากแอปพลิเคชัน Java ของคุณ

## คำตอบอย่างรวดเร็ว
- **ไลบรารีใดที่จัดการไฟล์ PSD ใน Java?** Aspose.PSD for Java.  
- **ฉันสามารถส่งออก PSD เป็น PNG ได้หรือไม่?** ใช่ – เพียงตั้งค่าตัวเลือกภาพที่เหมาะสม.  
- **ฉันจะรวมหลายเลเยอร์ได้อย่างไร?** โหลด PSD, จัดการคอลเลกชัน `Layer`, แล้วบันทึก.  
- **ถ้าฉันต้องการควบคุมคุณภาพ JPEG จะทำอย่างไร?** ใช้ `JpegOptions` และตั้งค่าคุณภาพ (0‑100).  
- **ต้องการ Photoshop หรือไม่?** ไม่จำเป็น, Aspose.PSD ทำงานโดยอิสระจากซอฟต์แวร์ Adobe.

## การส่งออก PSD เป็น PNG คืออะไร?
การส่งออก PSD เป็น PNG หมายถึงการแปลงเอกสาร Photoshop (PSD) ให้เป็นไฟล์ Portable Network Graphics (PNG) พร้อมกับการทำให้แบนหรือรวมเลเยอร์ตามต้องการ PNG รักษาความโปร่งใสและได้รับการสนับสนุนอย่างกว้างขวางบนเว็บ ทำให้เป็นรูปแบบที่นิยมสำหรับทรัพยากร UI.

## ทำไมต้องรวมเลเยอร์ PSD ด้วยโปรแกรม?
- **Automation:** ประมวลผลเป็นชุดหลายร้อยไฟล์โดยไม่ต้องคลิกมือ.  
- **Performance:** การรวมเลเยอร์ช่วยลดเวลาเรนเดอร์ในแอปพลิเคชันต่อไป.  
- **File size:** การทำให้แบนเลเยอร์ที่ไม่จำเป็นสามารถลดขนาดภาพสุดท้ายได้.  
- **Consistency:** รับประกันลำดับเลเยอร์และการผสมสีที่เหมือนกันในทุกการสร้าง.

## ข้อกำหนดเบื้องต้น

1. **Aspose.PSD for Java Library** – ดาวน์โหลดจาก [Aspose.PSD for Java download link](https://releases.aspose.com/psd/java/).  
2. **Java Development Environment** – IntelliJ IDEA, Eclipse หรือ IDE ใด ๆ ที่คุณชอบ.  
3. **Sample PSD File** – ไฟล์ที่มีหลายเลเยอร์ (เช่น `layers.psd`).  
4. **Basic Java Knowledge** – คุณควรคุ้นเคยกับคลาสและเมธอด.  
5. **Aspose Temporary License (Optional)** – สำหรับไฟล์ขนาดใหญ่หรือเพื่อยกเลิกข้อจำกัดของรุ่นทดลอง, รับ [temporary license](https://purchase.aspose.com/temporary-license/).

## นำเข้าแพ็กเกจ

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
```

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: โหลดไฟล์ PSD

```java
String dataDir = "Your Document Directory";
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```

> นี้โหลด `layers.psd` เข้าไปในอ็อบเจ็กต์ `PsdImage` ให้คุณเข้าถึงเลเยอร์ทั้งหมดได้อย่างเต็มที่.

### ขั้นตอนที่ 2: ตรวจสอบเลเยอร์ (how to merge psd)

```java
Layer[] layers = psdImage.getLayers();
System.out.println("Total layers: " + layers.length);

for (Layer layer : layers) {
    System.out.println("Layer name: " + layer.getName());
}
```

> การตรวจสอบชื่อเลเยอร์ช่วยให้คุณตัดสินใจว่าจะทำให้แบนหรือเก็บแยกกัน.

### ขั้นตอนที่ 3: ตั้งค่าตัวเลือกภาพ (set jpeg quality)

```java
JpegOptions jpgOptions = new JpegOptions();
jpgOptions.setQuality(80); // Set the quality of the JPEG image (0-100)
```

> หากคุณต้องการ PNG หรือ TIFF, คุณสามารถแทนที่ `JpegOptions` ด้วย `PngOptions` หรือ `TiffOptions` – ที่นี่คือจุดที่ **psd to tiff conversion** จะถูกกำหนดค่า.

### ขั้นตอนที่ 4: บันทึกภาพที่รวมแล้ว (export psd to png)

```java
psdImage.save(dataDir + "MergePSDlayers_output.png", jpgOptions);
```

> เมธอด `save` จะเขียนผลลัพธ์ที่รวมแล้วไปยัง `MergePSDlayers_output.png`.  
> *Tip:* เพื่อส่งออกเป็น PNG, แทนที่ `jpgOptions` ด้วยอินสแตนซ์ `PngOptions`; ส่วนอื่นของโค้ดยังคงเหมือนเดิม.

## ปัญหาทั่วไปและวิธีแก้

- **File‑not‑found exception:** ตรวจสอบว่า `dataDir` ลงท้ายด้วยตัวคั่นเส้นทาง (`/` หรือ `\\`) และว่า `layers.psd` มีอยู่.  
- **Unexpected colors after merge:** ตรวจสอบว่าโหมดการผสมของเลเยอร์เข้ากันได้; คุณสามารถปรับได้ผ่าน `layer.setBlendMode(...)`.  
- **Large output file:** ลดคุณภาพ JPEG หรือใช้ระดับการบีบอัด PNG เพื่อลดขนาด.

## คำถามที่พบบ่อย

**Q: สามารถบันทึกภาพที่รวมแล้วในรูปแบบอื่นนอกจาก JPEG ได้หรือไม่?**  
A: แน่นอน! Aspose.PSD รองรับ PNG, BMP, TIFF และอื่น ๆ เพียงใช้คลาสตัวเลือกที่สอดคล้อง (`PngOptions`, `BmpOptions`, `TiffOptions`).

**Q: ฉันจะปรับคุณภาพภาพสำหรับรูปแบบผลลัพธ์ต่าง ๆ ได้อย่างไร?**  
A: แต่ละคลาสตัวเลือกมีการตั้งค่าคุณภาพ/การบีบอัดของตนเอง สำหรับ JPEG ใช้ `setQuality(int)` สำหรับ PNG คุณสามารถควบคุม `CompressionLevel`.

**Q: จำเป็นต้องติดตั้ง Photoshop เพื่อใช้ Aspose.PSD for Java หรือไม่?**  
A: ไม่จำเป็น. Aspose.PSD ทำงานโดยอิสระจาก Adobe Photoshop, ดังนั้นคุณสามารถรันบนเซิร์ฟเวอร์หรือสภาพแวดล้อม CI ใดก็ได้.

**Q: จะเกิดอะไรขึ้นหากไม่ได้ตั้งค่าตัวเลือกภาพก่อนบันทึก?**  
A: ไลบรารีจะใช้การตั้งค่าเริ่มต้น (เช่น JPEG quality 75). การระบุตัวเลือกทำให้คุณควบคุมผลลัพธ์สุดท้ายได้.

**Q: ฉันสามารถแปลง PSD เป็น TIFF โดยตรงในขั้นตอนเดียวได้หรือไม่?**  
A: ได้ – สร้างอินสแตนซ์ `TiffOptions` แล้วเรียก `psdImage.save("output.tiff", tiffOptions);`.

---

**อัปเดตล่าสุด:** 2026-04-05  
**ทดสอบด้วย:** Aspose.PSD for Java 24.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}