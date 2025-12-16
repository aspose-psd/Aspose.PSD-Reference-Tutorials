---
date: 2025-12-15
description: เรียนรู้วิธีแปลงไฟล์ PSD เป็น PNG และหมุนเลเยอร์ PSD ใน Java ด้วย Aspose.PSD
  คู่มือแบบขั้นตอนพร้อมตัวอย่างโค้ด
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: แปลง PSD เป็น PNG และหมุนเลเยอร์ในไฟล์ PSD ด้วย Java
url: /th/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง PSD เป็น PNG และหมุนเลเยอร์ในไฟล์ PSD ด้วย Java

## บทนำ
หากคุณต้องการ **แปลง PSD เป็น PNG** พร้อมกับการหมุนเลเยอร์ คู่มือนี้เหมาะสำหรับคุณ ไม่ว่าคุณจะกำลังสร้างเครื่องมือประมวลผลแบบชุดหรือผสานการจัดการภาพเข้าไปในบริการเว็บ การทำแบบโปรแกรมช่วยประหยัดเวลาและลบการพึ่งพา Adobe Photoshop ออกไป ในบทเรียนนี้เราจะแสดงให้คุณเห็น **วิธีหมุนเลเยอร์ PSD** และส่งออกผลลัพธ์เป็น PNG โดยใช้ไลบรารี Aspose.PSD สำหรับ Java มาลุยกันเลยเพื่อให้กระบวนการออกแบบของคุณทำงานได้อย่างราบรื่น!

## คำตอบอย่างรวดเร็ว
- **ไลบรารีที่ฉันสามารถใช้ได้คืออะไร?** Aspose.PSD for Java  
- **ฉันสามารถหมุนและแปลงได้ในขั้นตอนเดียวหรือไม่?** ใช่ – หมุน PSD แล้วบันทึกเป็น PNG  
- **ฉันต้องการไลเซนส์หรือไม่?** การทดลองใช้ฟรีทำงานสำหรับการทดสอบ; จำเป็นต้องมีไลเซนส์แบบชำระเงินสำหรับการใช้งานจริง  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Java 8 และรุ่นต่อไป  
- **ผลลัพธ์ PNG มีความโปร่งใสหรือไม่?** ใช่ เมื่อคุณตั้งค่า `PngColorType.TruecolorWithAlpha`

## “การแปลง PSD เป็น PNG” คืออะไร?
การแปลงเอกสาร Photoshop (PSD) เป็นภาพ PNG หมายถึงการสกัดเนื้อหาภาพรวมถึงทุกเลเยอร์, มาสก์, และความโปร่งใส ไปเป็นรูปแบบแรสเตอร์ที่ได้รับการสนับสนุนอย่างกว้างขวาง PNG จะรักษาชาแนลอัลฟ่าไว้ ทำให้เหมาะสำหรับกราฟิกเว็บ, รูปย่อ, และการประมวลผลภาพต่อไป

## ทำไมต้องใช้ Aspose.PSD for Java เพื่อแปลง PSD เป็น PNG และหมุนเลเยอร์ PSD?
- **ไม่ต้องใช้ Photoshop** – ทำงานบนเซิร์ฟเวอร์หรือสภาพแวดล้อม CI ใดก็ได้  
- **รองรับเลเยอร์เต็มรูปแบบ** – รักษาความโปร่งใสและเอฟเฟกต์ของเลเยอร์ไว้ครบ  
- **API ที่ง่าย** – หมุน, พลิก, และบันทึกด้วยการเรียกเมธอดเพียงไม่กี่ครั้ง  
- **ข้ามแพลตฟอร์ม** – ทำงานบน Windows, Linux, และ macOS  

## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะลงลึกในโค้ด, ตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

- **Java Development Kit (JDK)** – ดาวน์โหลดจาก [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Integrated Development Environment (IDE)** – IntelliJ IDEA, Eclipse หรือ NetBeans ล้วนใช้ได้  
- **Aspose.PSD for Java library** – รับไฟล์ JAR ล่าสุดจาก [release page](https://releases.aspose.com/psd/java/).  
- **ความรู้พื้นฐานของ Java** – คุ้นเคยกับคลาส, อ็อบเจกต์, และการจัดการข้อยกเว้น  

## คู่มือแบบขั้นตอน

### ขั้นตอนที่ 1: ตั้งค่าโครงการ Java ของคุณ
สร้างโครงการ Java ใหม่ใน IDE ของคุณและเพิ่มไฟล์ Aspose.PSD JAR ไปยังเส้นทางการสร้างของโครงการ

### ขั้นตอนที่ 2: นำเข้าคลาสที่จำเป็น
เพิ่มการนำเข้าต่อไปนี้ที่ส่วนหัวของไฟล์ซอร์ส Java ของคุณ:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

คลาสเหล่านี้ให้คุณเข้าถึงการโหลดภาพ, การหมุน, และตัวเลือกเฉพาะของ PNG

### ขั้นตอนที่ 3: กำหนดเส้นทางไฟล์
ระบุที่ตั้งของไฟล์ PSD ต้นฉบับและที่ที่ไฟล์ผลลัพธ์ควรจะถูกเขียนออกไป

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **เคล็ดลับ:** ใช้เส้นทางแบบเต็มระหว่างการทดสอบเพื่อหลีกเลี่ยงข้อผิดพลาด “ไฟล์ไม่พบ”

### ขั้นตอนที่ 4: โหลดไฟล์ PSD
โหลด PSD เข้าไปเป็นอ็อบเจกต์ที่สามารถจัดการได้

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

ตอนนี้ `im` แสดงถึงเอกสาร Photoshop ทั้งหมด, รวมถึงทุกเลเยอร์

### ขั้นตอนที่ 5: หมุนภาพ (วิธีหมุน PSD)
เลือกประเภทการหมุนจาก `RotateFlipType` ในตัวอย่างนี้เราจะหมุน 270° และพลิกทั้งสองแกน

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

ลองใช้ค่าต่าง ๆ เช่น `Rotate90FlipNone` หรือ `Rotate180FlipX` ได้ตามต้องการ

### ขั้นตอนที่ 6: บันทึกภาพที่หมุนแล้วเป็น PNG (แปลง PSD เป็น PNG)
กำหนดตัวเลือก PNG เพื่อรักษาความโปร่งใส, แล้วบันทึก

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

PNG ที่ได้จะคงความโปร่งใสของเลเยอร์ไว้ ทำให้พร้อมใช้งานบนเว็บ

### ขั้นตอนที่ 7: บันทึก PSD ที่แก้ไขแล้ว (ทางเลือก)
หากคุณต้องการไฟล์ PSD ใหม่ที่มีการหมุนแล้ว, ให้บันทึกกลับไป

```java
im.save(psdPath);
```

คุณจะได้ทั้งไฟล์ PNG ตัวอย่างและไฟล์ PSD ที่อัปเดตแล้ว

## ปัญหาที่พบบ่อยและวิธีแก้
- **ไฟล์ไม่พบ:** ตรวจสอบว่า `dataDir` ลงท้ายด้วยตัวคั่นเส้นทาง (`/` หรือ `\`).  
- **OutOfMemoryError กับ PSD ขนาดใหญ่:** เพิ่มขนาด heap ของ JVM (`-Xmx2g`).  
- **ความโปร่งใสหายไป:** ตรวจสอบว่าตั้งค่า `PngColorType.TruecolorWithAlpha`; มิฉะนั้น PNG จะถูกบันทึกโดยไม่มีอัลฟ่า  

## คำถามที่พบบ่อย

### ฉันสามารถหมุนเลเยอร์เฉพาะในไฟล์ PSD ได้หรือไม่?
ใช่, คุณสามารถใช้ `Layer.rotateFlip()` กับเลเยอร์แต่ละอันหลังจากวนลูปผ่าน `im.getLayers()`  

### มีข้อจำกัดด้านประสิทธิภาพกับ Aspose.PSD for Java หรือไม่?
ไลบรารีจัดการไฟล์ส่วนใหญ่ได้อย่างมีประสิทธิภาพ, แต่ PSD ขนาดใหญ่มาก (>500 MB) อาจต้องการหน่วยความจำเพิ่มเติม  

### Aspose.PSD ใช้ได้ฟรีหรือไม่?
Aspose มีรุ่นทดลองใช้ฟรี, แต่ต้องมีไลเซนส์แบบชำระเงินสำหรับการใช้งานจริง ตรวจสอบ [temporary license](https://purchase.aspose.com/temporary-license/) สำหรับการทดสอบ  

### ฉันจะหาเอกสารรายละเอียดได้จากที่ไหน?
คุณสามารถดูเอกสารเต็มได้ที่ [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/)  

### จะทำอย่างไรหากพบปัญหาในการใช้ Aspose.PSD?
ขอความช่วยเหลือได้ผ่าน [Aspose Support Forum](https://forum.aspose.com/c/psd/34)  

## คำถามที่พบบ่อยเพิ่มเติม

**Q: การแปลง PSD เป็น PNG จะคงเอฟเฟกต์ของเลเยอร์ไว้หรือไม่?**  
A: ใช่, เมื่อบันทึกด้วย `PngColorType.TruecolorWithAlpha` เอฟเฟกต์ส่วนใหญ่จะถูกเรสเตอร์ไลซ์ลงใน PNG  

**Q: ฉันสามารถประมวลผลหลายไฟล์ PSD พร้อมกันได้หรือไม่?**  
A: แน่นอน. ห่อโค้ดในลูปที่วนผ่านไดเรกทอรีของไฟล์ PSD  

**Q: สามารถตั้งค่าระดับการบีบอัดของ PNG ได้หรือไม่?**  
A: คลาส `PngOptions` มีเมธอด `setCompressionLevel(int)` สำหรับปรับระดับการบีบอัดอย่างละเอียด  

**Q: จำเป็นต้องปิดอ็อบเจกต์ภาพหรือไม่?**  
A: `PsdImage` implements `Closeable`; ให้เรียก `im.close()` ในบล็อก `finally` หรือใช้ try‑with‑resources  

**Q: PNG ที่หมุนแล้วจะมีขนาดเท่ากับต้นฉบับหรือไม่?**  
A: การหมุน 90° หรือ 270° จะสลับความกว้างและความสูง PNG จะสะท้อนการเปลี่ยนแปลงทิศทางใหม่  

## สรุป
โดยการใช้ Aspose.PSD for Java คุณสามารถ **แปลง PSD เป็น PNG** และ **หมุนเลเยอร์ PSD** ได้ด้วยเพียงไม่กี่บรรทัดของโค้ด วิธีนี้ช่วยลดการพึ่งพา Photoshop, เร่งกระบวนการทำงานอัตโนมัติ, และให้คุณควบคุมผลลัพธ์ของภาพได้อย่างเต็มที่ ลองใช้ในโปรเจกต์ของคุณและสัมผัสความประหยัดเวลา!

---

**Last Updated:** 2025-12-15  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}