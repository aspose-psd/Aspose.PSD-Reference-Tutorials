---
date: 2026-04-05
description: เรียนรู้วิธีส่งออกไฟล์ PSD เป็น PNG และเพิ่มความคมชัดของภาพได้อย่างง่ายดายด้วย
  Aspose.PSD สำหรับ Java. เชี่ยวชาญการปรับระดับของเลเยอร์ด้วยคู่มือแบบขั้นตอนต่อขั้นตอนนี้.
keywords:
- export psd to png
- how to adjust levels
- batch process psd files
linktitle: ส่งออก PSD เป็น PNG และเรนเดอร์เลเยอร์ปรับระดับใน Java
second_title: Aspose.PSD Java API
title: ส่งออก PSD เป็น PNG และเรนเดอร์เลเยอร์ปรับระดับใน Java
url: /th/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก PSD เป็น PNG และเรนเดอร์เลเยอร์ปรับระดับใน Java

## บทนำ

เคยเปิดไฟล์ PSD แล้วสังเกตว่ารูปสีดูแบนหรือคอนทราสต์ไม่ตรงหรือไม่? คุณสามารถ **export PSD to PNG** อย่างรวดเร็วพร้อมปรับภาพด้วยเลเยอร์ปรับระดับ (Levels Adjustment Layer) โดยใช้ Aspose.PSD for Java ในบทแนะนำนี้เราจะเดินผ่านกระบวนการทั้งหมด—จากการโหลด PSD, ปรับระดับ, จนบันทึกผลลัพธ์เป็น PNG—เพื่อให้คุณเพิ่มความสดใสและเตรียมทรัพยากรที่พร้อมสำหรับเว็บในไม่กี่นาที.

## คำตอบสั้น
- **What does “export PSD to PNG” mean?** มันแปลงเอกสาร Photoshop เป็นภาพ PNG แบบ lossless พร้อมคงความโปร่งใส  
- **Can I adjust levels before exporting?** ใช่, Aspose.PSD ให้คุณแก้ไขระดับอินพุตและเอาต์พุตโดยโปรแกรม  
- **Do I need a license?** รุ่นทดลองฟรีใช้ได้สำหรับการพัฒนา; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **Is batch processing possible?** แน่นอน—คุณสามารถใส่โค้ดในลูปเพื่อประมวลผลหลายไฟล์ PSD  
- **Which Java version is required?** แนะนำให้ใช้ Java 8 หรือใหม่กว่า  

## อะไรคือ “export PSD to PNG”?
การส่งออก PSD เป็น PNG หมายถึงการนำไฟล์ Photoshop ที่มีหลายเลเยอร์มารวมเป็นภาพ Portable Network Graphics การรองรับการบีบอัดแบบ lossless และช่องอัลฟา ทำให้เหมาะสำหรับกราฟิกเว็บและ UI assets

## ทำไมต้องปรับระดับก่อนส่งออก?
การปรับระดับช่วยให้คุณควบคุมเงา, โทนกลาง, และไฮไลท์, ปรับปรุงคอนทราสต์และสมดุลสีโดยรวม ขั้นตอนนี้ทำให้ PNG สุดท้ายดูเรียบหรูโดยไม่ต้องแก้ไขด้วย Photoshop

## ข้อกำหนดเบื้องต้น

- **Java Development Kit (JDK)** – ดาวน์โหลดเวอร์ชันล่าสุดจากเว็บไซต์ Oracle ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).  
- **Aspose.PSD for Java Library** – รับได้จากหน้าดาวน์โหลดอย่างเป็นทางการ ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). มีรุ่นทดลองฟรี ([https://releases.aspose.com/](https://releases.aspose.com/)).  

## นำเข้าแพ็กเกจ

ก่อนจะลงลึกในโค้ด, ให้ import คลาสที่ให้เราสามารถจัดการ PSD และส่งออก PNG:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

## คู่มือขั้นตอน

### ขั้นตอนที่ 1: กำหนดเส้นทางไฟล์ (วิธีอัตโนมัติการประมวลผล PSD)

กำหนดตัวแปรที่ชัดเจนและอธิบายได้สำหรับ PSD ต้นฉบับ, PSD ที่แก้ไข, และตำแหน่งส่งออก PNG สุดท้าย

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

### ขั้นตอนที่ 2: โหลดภาพ PSD

ใช้ `Image.load` เพื่ออ่านไฟล์ PSD เข้าเป็นอ็อบเจ็กต์ `PsdImage`. Aspose.PSD จะตรวจจับฟอร์แมตโดยอัตโนมัติ

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### ขั้นตอนที่ 3: วนลูปผ่านเลเยอร์ (วิธีปรับระดับ)

วนลูปทุกเลเยอร์เพื่อค้นหาเลเยอร์ Levels Adjustment Layer

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (code to check for Levels Layer will be added here)
}
```

### ขั้นตอนที่ 4: ระบุเลเยอร์ Levels

ตรวจสอบแต่ละเลเยอร์ด้วย `instanceof LevelsLayer`. เมื่อพบ, ทำการ cast เพื่อให้สามารถแก้ไขคุณสมบัติได้

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (code to adjust levels will be added here)
   }
}
```

### ขั้นตอนที่ 5: ปรับระดับอย่างละเอียด (วิธีปรับระดับ)

ปรับระดับอินพุตและเอาต์พุตสำหรับช่องแรก (โดยทั่วไปคือช่องคอมโพสิต). ค่าตัวอย่างเหล่านี้สามารถเปลี่ยนแปลงได้ตามต้องการ

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Adjust Input Levels (0‑255):
	   channel.setInputShadowLevel((short) 10); // Darken shadows slightly
	   channel.setInputMidtoneLevel(2.0f);     // Increase midtones
	   channel.setInputHighlightLevel((short) 230); // Reduce highlights

	   // Adjust Output Levels (0‑255):
	   channel.setOutputShadowLevel((short) 20); // Darken shadows further
	   channel.setOutputHighlightLevel((short) 200); // Brighten highlights
   }
}
```

### ขั้นตอนที่ 6: บันทึก PSD ที่แก้ไข (วิธีอัตโนมัติ PSD)

บันทึกการเปลี่ยนแปลงกลับไปเป็นไฟล์ PSD ใหม่

```java
im.save(psdPathAfterChange);
```

### ขั้นตอนที่ 7: ส่งออกเป็น PNG (Export PSD to PNG)

หากต้องการเวอร์ชัน PNG, ตั้งค่า `PngOptions` แล้วบันทึกภาพ

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

## กรณีการใช้งานทั่วไป

- **Web asset preparation:** แปลง mockup PSD ที่ออกแบบให้เป็น PNG พร้อมใช้ในเบราว์เซอร์  
- **Batch processing:** อัตโนมัติการแปลงหลายสิบไฟล์ PSD ใน pipeline CI  
- **Dynamic image generation:** ปรับระดับแบบเรียลไทม์ตามข้อมูลผู้ใช้ก่อนส่งออก  

## การแก้ไขปัญหาและเคล็ดลับ

- **Null pointer when accessing layers:** ตรวจสอบให้แน่ใจว่า PSD มีเลเยอร์ Levels Adjustment Layer; หากไม่มีให้เพิ่มการตรวจสอบ null  
- **Unexpected colors after export:** ยืนยันว่าชนิดสี PNG ตั้งเป็น `TruecolorWithAlpha` เพื่อคงความโปร่งใส  
- **Performance with many files:** ใช้ `PsdImage` ตัวเดียวกันซ้ำเมื่อประมวลผลหลายไฟล์เพื่อประหยัดหน่วยความจำ  

## คำถามที่พบบ่อย

**Q: Can I adjust individual color channels (RGB) separately?**  
A: ใช่. ใช้ `levelsLayer.getChannel(index)` โดยที่ `index` = 0 (Red), 1 (Green), 2 (Blue) เพื่อปรับแต่ละช่องอย่างอิสระ  

**Q: How do I handle multiple Levels Adjustment Layers in one PSD?**  
A: ลูปจะประมวลผลทุกเลเยอร์; ทุก `LevelsLayer` ที่พบจะถูกปรับตามโค้ดในบล็อก `if`  

**Q: Are there other ways to improve contrast besides Levels?**  
A: Aspose.PSD ยังมี Curves, Brightness/Contrast, และ Histogram Equalization ให้เลือกใช้  

**Q: Can I automate this for a folder of PSD files?**  
A: ห่อ workflow ทั้งหมดในลูป `File[] files = new File(dataDir).listFiles((d, name) -> name.endsWith(".psd"));` แล้วประมวลผลไฟล์แต่ละไฟล์ตามลำดับ  

**Q: Where can I find more documentation and support?**  
A: เยี่ยมชมเอกสารอ้างอิงอย่างเป็นทางการ ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) และฟอรั่มชุมชน ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34))  

## สรุป

โดยการเชี่ยวชาญ workflow **export PSD to PNG** และเรียนรู้ **how to adjust levels** ผ่านโปรแกรม, คุณจะได้ควบคุมคุณภาพภาพอย่างเต็มที่โดยไม่ต้องออกจากสภาพแวดล้อม Java ไม่ว่าจะเป็นการเตรียม assets สำหรับเว็บ, การอัตโนมัติ pipeline การออกแบบ, หรือการสร้างตัวประมวลผลแบบ batch, Aspose.PSD for Java ทำให้งานเป็นเรื่องง่ายและเชื่อถือได้

---

**อัปเดตล่าสุด:** 2026-04-05  
**ทดสอบด้วย:** Aspose.PSD 24.11 for Java  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}