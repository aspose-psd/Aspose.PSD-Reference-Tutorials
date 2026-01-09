---
date: 2026-01-09
description: เรียนรู้วิธีแปลงไฟล์ PSD เป็น PNG ด้วยเทคนิค Bradley Thresholding ใน
  Aspose.PSD สำหรับ Java คู่มือนี้จะแสดงวิธีเลือกค่าธรัชที่เหมาะสมและทำให้ภาพ PSD
  เป็นแบบไบนารีอย่างมีประสิทธิภาพ
linktitle: Bradley Thresholding
second_title: Aspose.PSD Java API
title: แปลง PSD เป็น PNG ด้วย Bradley Thresholding (Aspose.PSD Java)
url: /th/java/image-processing/bradley-thresholding/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง PSD เป็น PNG ด้วย Bradley Thresholding (Aspose.PSD Java)

ยินดีต้อนรับสู่คู่มือฉบับสมบูรณ์นี้เกี่ยวกับ **convert PSD to PNG** ด้วย Bradley Thresholding ใน Aspose.PSD สำหรับ Java ในไม่กี่นาทีต่อไป คุณจะได้เห็นว่าทำไมเทคนิคนี้จึงเหมาะอย่างยิ่งสำหรับการสร้างไฟล์ PNG ที่มีคอนทราสต์สูงและแปลงเป็นสีทึบจากเอกสาร Photoshop และคุณจะได้รับการสาธิตแบบทำตามขั้นตอนอย่างละเอียด

## คำตอบอย่างรวดเร็ว
- **ฉันสามารถแปลง PSD เป็น PNG ด้วย Aspose.PSD ได้หรือไม่?** ได้ – โหลดไฟล์ PSD, ใช้ `binarizeBradley`, แล้วบันทึกเป็น PNG.  
- **“choose optimal threshold” หมายถึงอะไร?** เป็นค่าความไว (0‑1) ที่กำหนดว่าพิกเซลที่มืดหรือสว่างจะถูกจัดประเภทอย่างไร.  
- **ฉันต้องการใบอนุญาตสำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์; เวอร์ชันทดลองฟรีใช้ได้สำหรับการประเมินผล.  
- **รูปแบบภาพใดบ้างที่รองรับการบันทึก?** PNG, JPEG, BMP และรูปแบบอื่น ๆ อีกหลายรูปแบบผ่านคลาส `ImageOptions`.  
- **โค้ดนี้เข้ากันได้กับ Java 8 และรุ่นต่อไปหรือไม่?** แน่นอน – API ของ Aspose.PSD Java รองรับ Java 8+.

## Bradley Thresholding คืออะไร?
Bradley Thresholding เป็นอัลกอริทึมการแปลงเป็นสีทึบแบบปรับตัวที่คำนวณค่าเฉลี่ยท้องถิ่นสำหรับแต่ละพิกเซลและเปรียบเทียบความเข้มของพิกเซลกับค่าเฉลี่ยนั้นที่คูณด้วยค่าธรัชที่ผู้ใช้กำหนด ผลลัพธ์คือภาพสีขาว-ดำที่คมชัดและคงรายละเอียดสำคัญไว้

## ทำไมต้องแปลง PSD เป็น PNG ด้วย Bradley Thresholding?
- **Preserve sharp edges** – เหมาะสำหรับ OCR, การตรวจจับบาร์โค้ด, หรือกระบวนการทำงานใด ๆ ที่ต้องการการแยกชัดเจนระหว่างพื้นหน้าและพื้นหลัง.  
- **Reduce file size** – PNG เป็นรูปแบบไม่มีการสูญเสียคุณภาพ แต่มักมีขนาดไฟล์เล็กลงหลังการแปลงเป็นสีทึบ.  
- **Cross‑platform compatibility** – PNG ใช้งานได้ทุกที่, ในขณะที่ PSD เฉพาะสำหรับ Photoshop.

## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่ม ให้แน่ใจว่าคุณมี:

1. **Java Development Environment** – ติดตั้ง JDK 8 หรือใหม่กว่า.  
2. **Aspose.PSD Library** – ดาวน์โหลด JAR เวอร์ชันล่าสุดจาก [here](https://releases.aspose.com/psd/java/).  
3. **Sample PSD Image** – ไฟล์ PSD ใดก็ได้ที่คุณต้องการแปลง; คุณสามารถใช้ตัวอย่างที่ให้มาจากตัวอย่างของ Aspose ได้เช่นกัน.

## นำเข้าแพ็กเกจ
เริ่มต้นด้วยการนำเข้าคลาสที่จำเป็นเข้าสู่โครงการ Java ของคุณ:

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## วิธีแปลง PSD เป็น PNG ด้วย Bradley Thresholding
ด้านล่างเป็นขั้นตอนการทำงานทั้งหมดที่แบ่งเป็นขั้นตอนที่ชัดเจนและเป็นลำดับ ตัวอย่างแต่ละขั้นตอนมีคำอธิบายสั้น ๆ ตามด้วยโค้ดที่คุณต้องคัดลอก‑วาง

### ขั้นตอนที่ 1: โหลดภาพ PSD
แรกเริ่ม ให้ระบุไฟล์ต้นฉบับของคุณและโหลดด้วย Aspose.PSD.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "binarized_out.png";

// Load an image
PsdImage image = (PsdImage)Image.load(sourceFile);
```

### ขั้นตอนที่ 2: เลือกค่าธรัชที่เหมาะสม
ค่าธรัช (ช่วง 0 – 1) ควบคุมความรุนแรงของการแปลงเป็นสีทึบ จุดเริ่มต้นที่ทั่วไปคือ **0.15** แต่คุณสามารถปรับให้เหมาะกับภาพของคุณได้

```java
// Define threshold value
double threshold = 0.15;
```

### ขั้นตอนที่ 3: แปลงภาพ PSD เป็นสีทึบ
ตอนนี้ให้ใช้ Bradley algorithm ขั้นตอนนี้ **binarize PSD image** ตามค่าธรัชที่คุณเลือก

```java
// Call BinarizeBradley method and pass the threshold value as a parameter
image.binarizeBradley(threshold);
```

### ขั้นตอนที่ 4: บันทึกผลลัพธ์เป็น PNG
สุดท้าย ให้เขียนภาพที่ประมวลผลแล้วลงดิสก์ในรูปแบบ PNG

```java
// Save the output image
image.save(destName, new PngOptions());
```

ทำซ้ำขั้นตอนเหล่านี้สำหรับไฟล์ PSD จำนวนใดก็ได้ที่คุณต้องการประมวลผล โดยปรับค่าธรัชตามต้องการเพื่อให้ได้ผลลัพธ์ภาพที่ดีที่สุด

## ปัญหาทั่วไปและเคล็ดลับ
- **Threshold too low/high:** หากผลลัพธ์ดูมีสัญญาณรบกวนมากเกินไปหรือสีจางเกินไป ให้ปรับค่า `threshold` ทีละน้อย (เช่น 0.10 – 0.20).  
- **Memory consumption:** ไฟล์ PSD ขนาดใหญ่อาจใช้หน่วยความจำมาก พิจารณาประมวลผลทีละไฟล์หรือเพิ่มขนาด heap ของ JVM (`-Xmx`).  
- **Preview before saving:** ใช้ `image.save("preview.bmp", new BmpOptions());` เพื่อตรวจสอบผลลัพธ์ที่แปลงเป็นสีทึบก่อนส่งออกเป็น PNG ขั้นสุดท้าย.

## คำถามที่พบบ่อย

**Q: What is the difference between `binarizeBradley` and other thresholding methods?**  
A: `binarizeBradley` computes a local mean for each pixel, making it more robust for images with uneven lighting compared to global thresholding.

**Q: Can I apply Bradley Thresholding to JPEG or BMP files?**  
A: Yes. Load any supported format with `Image.load(...)`, then call `binarizeBradley` before saving.

**Q: Is there a way to preview the binarized image before saving?**  
A: Absolutely. Use any of Aspose.PSD’s image‑saving options (e.g., BMP) to write a temporary preview file.

**Q: Where can I find more support and resources?**  
A: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community help and explore the full [documentation](https://reference.aspose.com/psd/java/) for advanced scenarios.

## สรุป
คุณได้เรียนรู้วิธี **แปลง PSD เป็น PNG** อย่างมีประสิทธิภาพโดย **เลือกค่าธรัชที่เหมาะสม** และ **แปลงภาพ PSD เป็นสีทึบ** ด้วย Bradley Thresholding วิธีนี้เหมาะอย่างยิ่งสำหรับกระบวนการทำงานที่ต้องการ PNG ที่คมชัดและคอนทราสต์สูงจากไฟล์ Photoshop ที่ซับซ้อน

---

**อัปเดตล่าสุด:** 2026-01-09  
**ทดสอบด้วย:** Aspose.PSD Java 23.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}