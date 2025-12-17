---
date: 2025-12-17
description: เรียนรู้วิธีส่งออกไฟล์ PSD เป็น PNG พร้อมการสนับสนุนคลิปปิ้งมาสก์โดยใช้
  Aspose.PSD สำหรับ Java. ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนของเราเพื่อบันทึก PSD เป็น
  PNG อย่างรวดเร็ว.
linktitle: Export PSD as PNG with Clipping Mask – Aspose.PSD Java
second_title: Aspose.PSD Java API
title: ส่งออก PSD เป็น PNG พร้อมคลิปปิ้งมาสก์ – Aspose.PSD Java
url: /th/java/advanced-psd-layer-features-effects/support-clipping-mask-psd-files/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# รองรับ Clipping Mask ในไฟล์ PSD ด้วย Aspose.PSD Java

## คำแนะนำ
หากคุณต้องการ **export PSD as PNG** พร้อมคงข้อมูล clipping mask ไว้, Aspose.PSD for Java ทำให้ขั้นตอนนี้ง่ายดาย ในบทแนะนำนี้เราจะอธิบายขั้นตอนอย่างละเอียดเพื่อจัดการไฟล์ PSD ด้วยโปรแกรม, ใช้ clipping mask, และ **save PSD to PNG** พร้อมการสนับสนุนความโปร่งใสเต็มรูปแบบ เมื่อเสร็จสิ้นคุณจะได้โค้ดสั้นที่นำไปใช้ในโปรเจกต์ Java ของคุณได้ทันที

## คำตอบอย่างรวดเร็ว
- **ไลบรารีทำอะไร?** มันอ่าน, แก้ไข และส่งออกไฟล์ Photoshop PSD ใน Java.  
- **สามารถเก็บ clipping masks ได้หรือไม่?** ได้ – มาสก์จะถูกเก็บไว้เมื่อส่งออกเป็น PNG.  
- **ฟอร์แมตใดที่ใช้สำหรับการส่งออกแบบไม่มีการสูญเสีย?** PNG with TruecolorWithAlpha.  
- **ต้องการไลเซนส์สำหรับการใช้งานจริงหรือไม่?** จำเป็นต้องมีไลเซนส์เชิงพาณิชย์; มีรุ่นทดลองฟรี.  
- **ต้องการเวอร์ชัน Java ใด?** JDK 8 หรือสูงกว่า.

## “export psd as png” คืออะไร?
การส่งออกไฟล์ PSD เป็น PNG จะเปลี่ยนเอกสาร Photoshop ที่มีหลายเลเยอร์ให้เป็นภาพเรสเตอร์แบนเดียวพร้อมคงความโปร่งใสไว้ ซึ่งเป็นประโยชน์อย่างยิ่งเมื่อคุณต้องการภาพพร้อมใช้งานบนเว็บหรือแชร์การออกแบบโดยไม่ต้องใช้ Photoshop

## ทำไมต้องใช้ Aspose.PSD สำหรับงานนี้?
Aspose.PSD จัดการคุณลักษณะซับซ้อนของ Photoshop เช่น clipping masks, adjustment layers, และ blending modes ได้โดยไม่ต้องติดตั้ง Photoshop เหมาะสำหรับการทำงานอัตโนมัติ, การประมวลผลเป็นชุด, หรือการรวมทรัพยากรการออกแบบเข้าสู่แอปพลิเคชันฝั่งเซิร์ฟเวอร์

## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะลงลึกในโค้ด, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

1. **Java Development Kit (JDK)** – อย่างน้อย JDK 8. ดาวน์โหลดจาก [Oracle website](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html).  
2. **Aspose.PSD for Java Library** – รับ JAR เวอร์ชันล่าสุดจาก [download page](https://releases.aspose.com/psd/java/). คุณยังสามารถลองใช้ [free trial](https://releases.aspose.com/).  
3. **IDE** – IntelliJ IDEA, Eclipse, หรือโปรแกรมแก้ไขใด ๆ ที่คุณชอบ.  
4. **Basic Java Knowledge** – ความคุ้นเคยกับการทำงานไฟล์ I/O และแนวคิดเชิงวัตถุจะช่วยได้มาก.

## การส่งออก PSD เป็น PNG – คู่มือขั้นตอน

### ขั้นตอนที่ 1: กำหนดไดเรกทอรีเอกสารของคุณ
ก่อนอื่นบอกโปรแกรมว่าที่ใดที่ไฟล์ PSD ต้นฉบับของคุณอยู่และ PNG ควรบันทึกที่ใด

```java
String dataDir = "Your Document Directory";
```

เปลี่ยน `"Your Document Directory"` ให้เป็นเส้นทางเต็มบนเครื่องของคุณที่มีไฟล์ PSD อยู่

### ขั้นตอนที่ 2: โหลดไฟล์ PSD
ต่อไปให้โหลด PSD เข้าไปในอ็อบเจ็กต์ `PsdImage` เพื่อให้คุณสามารถทำงานกับเลเยอร์และมาสก์ได้

```java
String sourceFileName = dataDir + "ClippingMaskComplex.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการส่งออก
กำหนดค่าการส่งออก PNG การใช้ `TruecolorWithAlpha` จะทำให้ส่วนที่โปร่งใสจาก clipping mask ถูกเก็บไว้

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

### ขั้นตอนที่ 4: ส่งออกภาพ
บันทึก PSD (พร้อม clipping mask) เป็นไฟล์ PNG

```java
String exportPath = dataDir + "ClippingMaskComplex.png";
im.save(exportPath, saveOptions);
```

ไฟล์ PNG ที่ได้สามารถใช้โดยตรงในหน้าเว็บ, แอปมือถือ, หรือที่ใดก็ได้ที่รับภาพเรสเตอร์

### ขั้นตอนที่ 5: ทำความสะอาดทรัพยากร
ควรทำการ `dispose` ของ `PsdImage` เสมอเมื่อใช้งานเสร็จเพื่อคืนหน่วยความจำเนทีฟ

```java
im.dispose();
```

### วิธีบันทึก PSD เป็น PNG ในบรรทัดเดียว
หากคุณต้องการเวอร์ชันกระชับ กระบวนการทั้งหมดสามารถย่อเป็นบรรทัดเดียวได้:

```java
Image.load(sourceFileName).save(exportPath, new PngOptions(){{
    setColorType(PngColorType.TruecolorWithAlpha);
}});
```

*(เวอร์ชันขยายด้านบนแสดงเพื่อความชัดเจนและง่ายต่อการดีบัก)*

## ปัญหาทั่วไปและวิธีแก้
- **Missing Transparency:** ตรวจสอบให้แน่ใจว่าได้ตั้งค่า `PngColorType.TruecolorWithAlpha`; มิฉะนั้น PNG จะเป็นแบบทึบ.  
- **File Not Found:** ตรวจสอบว่า `dataDir` ลงท้ายด้วยตัวคั่นเส้นทางที่เหมาะสม (`/` หรือ `\\`).  
- **OutOfMemoryError:** ทำการ `dispose` ของ `PsdImage` ทันที, โดยเฉพาะเมื่อประมวลผลไฟล์ขนาดใหญ่หรือเป็นชุด.

## คำถามที่พบบ่อย

**Q: Clipping mask ในไฟล์ PSD คืออะไร?**  
A: Clipping mask ใช้ความทึบของเลเยอร์หนึ่งเพื่อจำกัดการมองเห็นของอีกเลเยอร์หนึ่ง, ทำให้สามารถสร้างคอมโพสิตซับซ้อนได้โดยไม่ต้องแก้ไขเลเยอร์อย่างถาวร.

**Q: ฉันสามารถใช้ Aspose.PSD เพื่อแก้ไขไฟล์ PSD ได้หรือไม่?**  
A: ได้, คุณสามารถแก้ไขเลเยอร์, ใส่เอฟเฟกต์, และส่งออกเป็นฟอร์แมตเช่น PNG หรือ JPEG.

**Q: จะหาเอกสารประกอบของ Aspose.PSD ได้จากที่ไหน?**  
A: คุณสามารถค้นหาเอกสารประกอบอย่างครบถ้วนสำหรับ Aspose.PSD for Java ได้ที่ [here](https://reference.aspose.com/psd/java/).

**Q: มีรุ่นทดลองของ Aspose.PSD หรือไม่?**  
A: มี! คุณสามารถเข้าถึงรุ่นทดลองฟรีของ Aspose.PSD ได้ที่ [here](https://releases.aspose.com/).

**Q: จะขอรับการสนับสนุนสำหรับปัญหา Aspose.PSD ได้อย่างไร?**  
A: สำหรับคำถามหรือปัญหาใด ๆ คุณสามารถรับการสนับสนุนผ่านฟอรัมของ Aspose ได้ที่ [here](https://forum.aspose.com/c/psd/34).

## สรุป
คุณได้เรียนรู้วิธี **export PSD as PNG** พร้อมคง clipping mask ไว้โดยใช้ Aspose.PSD for Java วิธีนี้ช่วยให้คุณอัตโนมัติการไหลของการออกแบบ, รวมทรัพยากร Photoshop เข้ากับบริการแบ็กเอนด์, และรักษาคุณภาพภาพโดยไม่ต้องทำการส่งออกด้วยตนเอง ลองสำรวจคุณลักษณะอื่นของ Aspose.PSD เช่น การรวมเลเยอร์, การปรับสี, และการประมวลผลเป็นชุด เพื่อเพิ่มประสิทธิภาพการทำงานของคุณต่อไป

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}