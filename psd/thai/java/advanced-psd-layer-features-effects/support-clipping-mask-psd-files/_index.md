---
date: 2026-02-20
description: เรียนรู้วิธีส่งออกไฟล์ PSD เป็น PNG พร้อมคงความโปร่งใสและการสนับสนุนคลิปปิ้งมาสก์โดยใช้
  Aspose.PSD สำหรับ Java คู่มือขั้นตอนต่อขั้นตอนนี้แสดงวิธีบันทึก PSD เป็น PNG อย่างรวดเร็ว
linktitle: How to Export PSD as PNG with Clipping Mask – Aspose.PSD Java
second_title: Aspose.PSD Java API
title: วิธีส่งออก PSD เป็น PNG ด้วยคลิปปิ้งมาสก์ – Aspose.PSD Java
url: /th/java/advanced-psd-layer-features-effects/support-clipping-mask-psd-files/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สนับสนุน Clipping Mask ในไฟล์ PSD ด้วย Aspose.PSD Java

## การแนะนำ
อย่างเป็นทางการ **วิธีส่งออก PSD** เป็น PNG พร้อมคงข้อมูลคลิปปิ้งมาสก์ไว้ Aspose.PSD Java บางส่วนขั้นตอนนี้บางส่วนแนะนำในบทนี้พาคุณผ่านขั้นตอนการจัดการเพื่อให้จัดการไฟล์ PSD ด้วยโปรแกรม, ใช้คลิปมาสก์มาสก์, และ ** บันทึก PSD เป็น PNG** พร้อมด้วยความสามารถตรวจสอบได้อีกครั้งอีกครั้งก่อนที่โค้ดสั้นสำหรับที่นำกลับมาใช้ใหม่ได้ระบบใส่โปรเจกต์ Java ของคุณได้ทันที

## คำตอบด่วน
- **ไลบรารีทำอะไร?** อ่าน, ถ่ายทำ, และส่งออกไฟล์ Photoshop PSD ใน Java
- **สามารถคงคลิปปิ้งมาสก์ได้หรือเปล่า?** ได้ – มาสก์สามารถเก็บไว้เมื่อส่งออกเป็น PNG
- ** สำหรับแมตใด ๆ ที่แทบจะไม่มีการสูญเสีย?** PNG กับ TruecolorWithAlpha
- **ต้องมีลิขสิทธิ์ในโปรดักชันหรือไม่** ต้องมีลิขสิทธิ์ ©; มีรุ่นทดลองฟรีให้ใช้
- **ต้องการ Java ใด ๆ บ้าง?** JDK8 หรือที่อื่น

## วิธีส่งออก PSD เป็น PNG ด้วย Clipping Mask
ไฟล์ PSD เป็น PNG ที่เป็นเอกสาร Photoshop ที่มีหลายส่วนของการแปลงภาพเรสเตอร์แบบแบนพร้อมคงความสมบูรณ์ไว้ประโยชน์อัตโนมัติเมื่อจำเป็นต้องมีภาพพร้อมใช้, ต้องการ **คงความนุ่มนวล PNG**, หรือกำลังทำเป็นชุดของ PSD PNG

## เหตุใดจึงต้องใช้ Aspose.PSD สำหรับงานนี้
Aspose.PSD การปฏิบัติตามกฎระเบียบของ Photoshop — เช่นคลิปปิ้งมาสก์, ส่วนปรับค่า, และโหมดผสมสี — ในส่วนของการติดตั้ง Photoshop ในส่วนของโฟลว์อัตโนมัติ, สุขภาพเป็นชุด, หรือทรัพยากรการออกแบบเข้าสู่แอปพลิเคชันฝั่งเซิร์ฟเวอร์ใน **ส่งออก PSD เป็น PNG** ที่เชื่อถือได้

## ข้อกำหนดเบื้องต้น
เราจะลงลึกในการส่งเสริมให้คุณทราบอีกครั้ง:

1. **Java Development Kit (JDK)** – ขยี้ JDK8 ดาวน์โหลดได้จาก [เว็บไซต์ Oracle](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html)
2. **Aspose.PSD for Java Library** – รับไฟล์ JAR ล่าสุดจาก [หน้าดาวน์โหลด](https://releases.aspose.com/psd/java/) สืบค้นลิขสิทธิ์ [ทดลองใช้ฟรี](https://releases.aspose.com/)
3. **IDE** – IntelliJ IDEA, Eclipse หรือโปรแกรมแก้ไขใดๆ ที่คุณชอบ
4. **จาวาพื้นฐาน ความรู้** – การแสดงการทำ I/O ของไฟล์และแนวคิดเชิงวัตถุสมุนไพรได้มาก

## ส่งออก PSD เป็น PNG – คำแนะนำทีละขั้นตอน

### ขั้นตอนที่ 1: กำหนดไดเร็กทอรีเอกสารของคุณ
ก่อนอื่นบอกโปรแกรมว่าที่อยู่ของไฟล์ PSD ต้นทางและที่ที่ PNG ควรถูกเขียนออกไปอยู่ที่ไหน

```java
String dataDir = "Your Document Directory";
```

แทนที่ `"Your Document Directory"` ด้วยเส้นทางเต็มบนเครื่องของคุณที่มีไฟล์ PSD อยู่

### ขั้นตอนที่ 2: โหลดไฟล์ PSD
ต่อไปโหลดไฟล์ PSD เข้าไปในอ็อบเจกต์ `PsdImage` เพื่อให้คุณสามารถทำงานกับเลเยอร์และมาสก์ได้

```java
String sourceFileName = dataDir + "ClippingMaskComplex.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการส่งออก
กำหนดค่าการส่งออก PNG การใช้ `TruecolorWithAlpha` จะทำให้ส่วนที่โปร่งใสที่สร้างจากคลิปปิ้งมาสก์ถูกเก็บไว้ ดังนั้นคุณ **คงความโปร่งใส PNG** ได้

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

### ขั้นตอนที่ 4: ส่งออกรูปภาพ
บันทึก PSD (พร้อมคลิปปิ้งมาสก์) เป็นไฟล์ PNG

```java
String exportPath = dataDir + "ClippingMaskComplex.png";
im.save(exportPath, saveOptions);
```

ไฟล์ PNG ที่ได้สามารถใช้โดยตรงในหน้าเว็บ, แอปมือถือ, หรือที่ใดก็ได้ที่รับภาพเรสเตอร์

### ขั้นตอนที่ 5: ลบทรัพยากรที่ไม่จำเป็น
ควรทำการ `dispose` อ็อบเจกต์ `PsdImage` เสมอเมื่อทำงานเสร็จเพื่อคืนหน่วยความจำเนทีฟ

```java
im.dispose();
```

### วิธีบันทึก PSD เป็น PNG ในบรรทัดเดียว
หากคุณต้องการเวอร์ชันกระชับ กระบวนการทั้งหมดสามารถย่อให้เหลือบรรทัดเดียวได้ดังนี้

```java
Image.load(sourceFileName).save(exportPath, new PngOptions(){{
    setColorType(PngColorType.TruecolorWithAlpha);
}});
```

*(เวอร์ชันขยายด้านบนแสดงเพื่อความชัดเจนและง่ายต่อการดีบัก)*

## ปัญหาทั่วไปและแนวทางแก้ไข
- **Missing Transparency:** การถ่ายทำภาพยนตร์ได้จัดเตรียม `PngColorType.TruecolorWithAlpha` อย่างอื่น PNG จะแบบทึบ
- **File Not Found:** `dataDir` ลงท้ายด้วยตัวคั่นเส้นทางที่เหมาะสม (`/` หรือ `\\`)
- **OutOfMemoryError:** ทำ `dispose` `PsdImage` ทันทีโดยเฉพาะเมื่อต้องดาวน์โหลดไฟล์ขนาดใหญ่หรือเป็นชุด
- **Batch Convert PSD PNG:** ต้องแปลงไฟล์หลายไฟล์ให้ใส่ขั้นตอนในส่วนลึกและ `PngOptions` ซ้ำเพื่อเปิดเผย

## คำถามที่พบบ่อย

**Q: ดูคลิปปิ้งมาสในไฟล์ PSD หรือเปล่า?**
ตอบ: ดูคลิปปิ้งมาสใช้ความเหมือนของหนึ่งเพื่อจำกัดขอบเขตของส่วนอื่นๆ ของเราอีกครั้งหนึ่งและตรวจสอบอีกครั้งอย่างถาวร

**ถาม: ฉันสามารถใช้ Aspose.PSD เพื่อแก้ไขไฟล์ PSD ได้ใช่ไหม**
ตอบ: ได้อีกครั้งในการแก้ไข, สามารถใส่, และส่งออกเป็นฟอร์แมตเช่น PNG หรือ JPEG

**คำถาม: เอกสารสำหรับ Aspose.PSD จากที่ไหน?**
A: เอกสารประกอบอย่างครบถ้วนสำหรับ Aspose.PSD for Java ได้ที่ [ที่นี่](https://reference.aspose.com/psd/java/)

**Q: มีรุ่นทดลองของ Aspose.PSD บ้างไหม?**
ตอบ: มี! ลองเข้าถึงรุ่นทดลองฟรีของ Aspose.PSD ได้ที่ [ที่นี่](https://releases.aspose.com/)

**ถาม: จะขอรับสำหรับปัญหา Aspose.PSD ได้อย่างไร?**
ตอบ: สำหรับคำถามหรือปัญหาใด ๆ ที่ไม่เคยได้รับการร้องขอผ่านฟอรั่มของ Aspose ได้ที่ [ที่นี่](https://forum.aspose.com/c/psd/34)

## บทสรุป
คุณได้เรียนรู้ **วิธีส่งออก PSD เป็น PNG** พร้อมคงคลิปปิ้งมาสก์โดยใช้ Aspose.PSD for Java วิธีนี้ช่วยให้คุณอัตโนมัติกระบวนการออกแบบ, รวมทรัพยากร Photoshop เข้ากับบริการแบ็กเอนด์, และรักษาความคมชัดของภาพโดยไม่ต้องทำการส่งออกด้วยมือสำรวจฟีเจอร์อื่น ๆ ของ Aspose.PSD — เช่นการรวมเลเยอร์, การปรับสี, และการประมวลผลเป็นชุด — เพื่อทำให้เวิร์กโฟลว์ของคุณราบรื่นยิ่งขึ้น

---

**Last Updated:** 2026-02-20  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}