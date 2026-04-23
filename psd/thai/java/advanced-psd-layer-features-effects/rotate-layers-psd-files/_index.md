---
date: 2026-02-17
description: เรียนรู้วิธีแปลง PSD เป็น PNG, รักษาความโปร่งใสของ PNG, และหมุนเลเยอร์
  PSD ใน Java ด้วย Aspose.PSD. คู่มือทีละขั้นตอนพร้อมตัวอย่างโค้ด.
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: แปลง PSD เป็น PNG และหมุนเลเยอร์ในไฟล์ PSD ด้วย Java
url: /th/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

 bold.

Also list of Quick Answers: bullet list.

Translate each question and answer but keep code parts like `PngColorType.TruecolorWithAlpha` unchanged.

Also "## What is “convert PSD to PNG”?" translate.

Continue.

Make sure to keep markdown formatting.

Let's produce final content.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง PSD เป็น PNG และหมุนเลเยอร์ในไฟล์ PSD ด้วย Java

## บทนำ
หากคุณต้องการ **แปลง PSD เป็น PNG** พร้อมกับการหมุนเลเยอร์ คู่มือนี้เหมาะกับคุณ ไม่ว่าคุณจะกำลังสร้างเครื่องมือประมวลผลแบบชุด, บริการเว็บที่ต้องการการจัดการภาพแบบเรียลไทม์, หรือเพียงแค่ต้องการทำอัตโนมัติในกระบวนการออกแบบ การทำแบบโปรแกรมจะช่วยประหยัดเวลาและลดการพึ่งพา Adobe Photoshop ในบทเรียนนี้เราจะอธิบาย **วิธีหมุนเลเยอร์ใน PSD** และส่งออกผลลัพธ์เป็น PNG ด้วยไลบรารี Aspose.PSD สำหรับ Java พร้อมกันเลย!

## คำตอบสั้น ๆ
- **ใช้ไลบรารีอะไรได้บ้าง?** Aspose.PSD for Java  
- **สามารถหมุนและแปลงได้ในขั้นตอนเดียวหรือไม่?** ได้ – หมุน PSD แล้วบันทึกเป็น PNG  
- **ต้องมีลิขสิทธิ์หรือไม่?** ทดลองใช้ฟรีได้สำหรับการทดสอบ; ต้องมีลิขสิทธิ์แบบชำระเงินสำหรับการใช้งานจริง  
- **รองรับเวอร์ชัน Java ใด?** Java 8 ขึ้นไป  
- **ผลลัพธ์ PNG มีความโปร่งใสหรือไม่?** มี, เมื่อคุณตั้งค่า `PngColorType.TruecolorWithAlpha`

## “แปลง PSD เป็น PNG” คืออะไร?
การแปลงไฟล์เอกสาร Photoshop (PSD) เป็นภาพ PNG หมายถึงการสกัดเนื้อหาภาพรวมถึงเลเยอร์, มาสก์, และความโปร่งใสออกเป็นรูปแบบเรสเตอร์ที่ได้รับการสนับสนุนอย่างกว้างขวาง PNG รองรับช่องอัลฟา ทำให้เหมาะสำหรับกราฟิกเว็บ, รูปย่อ, และการประมวลผลภาพต่อไป

## ทำไมต้องใช้ Aspose.PSD for Java เพื่อแปลง PSD เป็น PNG และหมุนเลเยอร์ PSD?
- **ไม่ต้องใช้ Photoshop** – ทำงานได้บนเซิร์ฟเวอร์หรือสภาพแวดล้อม CI ใดก็ได้  
- **รองรับเลเยอร์เต็มรูปแบบ** – รักษาความโปร่งใสและเอฟเฟกต์ของเลเยอร์ไว้ครบถ้วน  
- **API ง่าย** – หมุน, พลิก, และบันทึกด้วยเพียงไม่กี่คำสั่ง  
- **ข้ามแพลตฟอร์ม** – ทำงานบน Windows, Linux, และ macOS  
- **การแปลงภาพ Java** ทำได้อย่างง่ายดายด้วยไลบรารีเดียว  

## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะลงมือเขียนโค้ด, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมแล้ว:

- **Java Development Kit (JDK)** – ดาวน์โหลดจาก [เว็บไซต์ Oracle](https://www.oracle.com/java/technologies/javase-downloads.html)  
- **Integrated Development Environment (IDE)** – IntelliJ IDEA, Eclipse, หรือ NetBeans ล้วนใช้ได้  
- **Aspose.PSD for Java library** – รับไฟล์ JAR ล่าสุดจาก [หน้ารีลีส](https://releases.aspose.com/psd/java/)  
- **ความรู้พื้นฐาน Java** – ความคุ้นเคยกับคลาส, อ็อบเจ็กต์, และการจัดการข้อยกเว้น  

## คำแนะนำแบบขั้นตอน

### ขั้นตอนที่ 1: ตั้งค่าโปรเจกต์ Java ของคุณ
สร้างโปรเจกต์ Java ใหม่ใน IDE ของคุณและเพิ่มไฟล์ JAR ของ Aspose.PSD เข้าไปใน build path ของโปรเจกต์

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
ระบุตำแหน่งที่ไฟล์ PSD ต้นฉบับอยู่และที่ที่ไฟล์ผลลัพธ์จะถูกบันทึก

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **เคล็ดลับ:** ใช้เส้นทางแบบเต็มระหว่างการทดสอบเพื่อหลีกเลี่ยงข้อผิดพลาด “ไฟล์ไม่พบ”

### ขั้นตอนที่ 4: โหลดไฟล์ PSD
โหลด PSD เข้าเป็นอ็อบเจ็กต์ที่สามารถจัดการได้

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

ตอนนี้ `im` แทนเอกสาร Photoshop ทั้งหมด รวมถึงทุกเลเยอร์

### ขั้นตอนที่ 5: หมุนภาพ (วิธีหมุน PSD)
เลือกประเภทการหมุนจาก `RotateFlipType` ตัวอย่างนี้เราจะหมุน 270° และพลิกทั้งสองแกน

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

คุณสามารถทดลองค่าต่าง ๆ เช่น `Rotate90FlipNone` หรือ `Rotate180FlipX` ได้ตามต้องการ นี่คือส่วน **วิธีหมุน PSD** ของบทเรียน

### ขั้นตอนที่ 6: บันทึกภาพที่หมุนแล้วเป็น PNG (แปลง PSD เป็น PNG)
ตั้งค่าตัวเลือก PNG เพื่อรักษาความโปร่งใส แล้วบันทึก

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

PNG ที่ได้จะคงความโปร่งใสของเลเยอร์ไว้, ทำให้ **รักษาความโปร่งใสของ PNG** สำหรับการใช้งานต่อไป

### ขั้นตอนที่ 7: บันทึก PSD ที่แก้ไขแล้ว (ไม่บังคับ)
หากคุณต้องการไฟล์ PSD ใหม่ที่มีการหมุนแล้ว, สามารถบันทึกกลับได้

```java
im.save(psdPath);
```

ตอนนี้คุณมีทั้งไฟล์ PNG ตัวอย่างและไฟล์ PSD ที่อัปเดตแล้ว

## ปัญหาที่พบบ่อยและวิธีแก้
- **ไฟล์ไม่พบ:** ตรวจสอบว่า `dataDir` ลงท้ายด้วยตัวคั่นเส้นทาง (`/` หรือ `\`)  
- **OutOfMemoryError กับ PSD ขนาดใหญ่:** เพิ่มขนาด heap ของ JVM (`-Xmx2g`)  
- **โปร่งใสหาย:** ตรวจสอบให้แน่ใจว่าได้ตั้งค่า `PngColorType.TruecolorWithAlpha`; มิฉะนั้น PNG จะบันทึกโดยไม่มีอัลฟา  
- **การพลิกภาพ PSD ไม่ทำงานตามคาด:** ตรวจสอบค่าคงที่ `RotateFlipType` ที่เลือก; บางค่าผสมการหมุนและการพลิกในขั้นตอนเดียว  

## คำถามที่พบบ่อย

**ถาม: สามารถหมุนเลเยอร์เฉพาะในไฟล์ PSD ได้หรือไม่?**  
ตอบ: ได้, คุณสามารถใช้ `Layer.rotateFlip()` กับเลเยอร์แต่ละอันหลังจากวนลูป `im.getLayers()`  

**ถาม: มีข้อจำกัดด้านประสิทธิภาพกับ Aspose.PSD for Java หรือไม่?**  
ตอบ: ไลบรารีจัดการไฟล์ส่วนใหญ่ได้อย่างมีประสิทธิภาพ, แต่ PSD ขนาดใหญ่มาก (>500 MB) อาจต้องการหน่วยความจำเพิ่มเติม  

**ถาม: Aspose.PSD ใช้ได้ฟรีหรือไม่?**  
ตอบ: Aspose มีรุ่นทดลองฟรี, แต่ต้องมีลิขสิทธิ์แบบชำระเงินสำหรับการใช้งานจริง ตรวจสอบ [ลิขสิทธิ์ชั่วคราว](https://purchase.aspose.com/temporary-license/) สำหรับการทดสอบ  

**ถาม: จะหาเอกสารรายละเอียดได้จากที่ไหน?**  
ตอบ: คุณสามารถดูเอกสารครบถ้วนได้ที่ [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/)  

**ถาม: หากพบปัญหาในการใช้ Aspose.PSD ควรทำอย่างไร?**  
ตอบ: ติดต่อขอความช่วยเหลือผ่าน [Aspose Support Forum](https://forum.aspose.com/c/psd/34)  

**ถาม: การแปลง PSD เป็น PNG จะรักษาเอฟเฟกต์ของเลเยอร์หรือไม่?**  
ตอบ: ใช่, เมื่อบันทึกด้วย `PngColorType.TruecolorWithAlpha` เอฟเฟกต์ส่วนใหญ่จะถูกเรสเตอร์ไลซ์ลงใน PNG  

**ถาม: สามารถประมวลผลหลายไฟล์ PSD พร้อมกันได้หรือไม่?**  
ตอบ: แน่นอน. ให้ใส่โค้ดในลูปที่วนผ่านโฟลเดอร์ของไฟล์ PSD  

**ถาม: สามารถตั้งค่าระดับการบีบอัดของ PNG ได้หรือไม่?**  
ตอบ: คลาส `PngOptions` มีเมธอด `setCompressionLevel(int)` สำหรับปรับระดับบีบอัด  

**ถาม: จำเป็นต้องปิดอ็อบเจ็กต์ภาพหรือไม่?**  
ตอบ: `PsdImage` implements `Closeable`; ให้เรียก `im.close()` ในบล็อก `finally` หรือใช้ try‑with‑resources  

**ถาม: PNG ที่หมุนแล้วจะมีขนาดเท่ากับต้นฉบับหรือไม่?**  
ตอบ: การหมุน 90° หรือ 270° จะสลับความกว้างและความสูง PNG จะสะท้อนการหมุนใหม่  

## สรุป
ด้วยการใช้ Aspose.PSD for Java คุณสามารถ **แปลง PSD เป็น PNG**, **รักษาความโปร่งใสของ PNG**, และ **หมุนเลเยอร์ PSD** ได้ด้วยไม่กี่บรรทัดโค้ด วิธีนี้ช่วยลดการพึ่งพา Photoshop, เร่งกระบวนการทำงานอัตโนมัติ, และให้คุณควบคุมผลลัพธ์ภาพได้เต็มที่ ลองนำไปใช้ในโปรเจกต์ของคุณและสัมผัสความประหยัดเวลา!

---

**อัปเดตล่าสุด:** 2026-02-17  
**ทดสอบกับ:** Aspose.PSD for Java 24.11  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}