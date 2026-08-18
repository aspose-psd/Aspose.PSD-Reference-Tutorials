---
date: 2026-03-18
description: เรียนรู้วิธีแปลงไฟล์ PSD เป็น PNG พร้อมปรับความลึกบิตของ PNG ด้วย Aspose.PSD
  for Java – คู่มือขั้นตอนโดยละเอียดพร้อมตัวอย่างโค้ด.
linktitle: Specify PNG Bit Depth in Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: วิธีแปลง PSD เป็น PNG ด้วยความลึกบิตที่กำหนดโดยใช้ Aspose.PSD สำหรับ Java
url: /th/java/optimizing-png-files/specify-png-bit-depth/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง PSD เป็น PNG พร้อมความลึกบิตที่กำหนดโดยใช้ Aspose.PSD สำหรับ Java

## คำแนะนำ
หากคุณต้องการ **convert psd to png** และควบคุมความลึกบิตของ PNG อย่างแม่นยำ คุณมาถูกที่แล้ว ในบทแนะนำนี้เราจะอธิบายวิธีการเปลี่ยนความลึกบิตของ PNG ขณะบันทึกไฟล์ PSD เป็นภาพ PNG ด้วย Aspose.PSD สำหรับ Java ไม่ว่าคุณจะกำลังสร้างเครื่องมือประมวลผลเป็นชุด, บริการเว็บ, หรือยูทิลิตี้บนเดสก์ท็อป การที่คุณสามารถ **save png with options** เช่นประเภทสีระดับสีเทาและความลึกบิตที่กำหนดเอง จะทำให้คุณควบคุมคุณภาพภาพและขนาดไฟล์ได้อย่างละเอียด

## คำตอบสั้น
- **Can I change the PNG bit depth?** Yes – use `PngOptions.setBitDepth()` to specify 1, 2, 4, 8, or 16 bits.  
- **Which color types are supported?** Grayscale, TrueColor, Indexed, and others via `PngColorType`.  
- **Do I need a license for Aspose.PSD?** A free trial works for development; a commercial license is required for production.  
- **What Java version is required?** Java 8+ (the library is compatible with newer JDKs).  
- **Is the code runnable as‑is?** Yes – just replace the placeholder path with your own folder.

## “convert psd to png” กับความลึกบิตที่กำหนดเองคืออะไร?
การแปลงไฟล์ Photoshop PSD เป็นภาพ PNG เป็นงานทั่วไปเมื่อคุณต้องการรูปแบบที่เป็นมิตรกับเว็บ การเพิ่มความสามารถในการ **adjust png quality** โดยการตั้งค่าความลึกบิตทำให้คุณสามารถปรับสมดุลระหว่างความคมชัดของภาพกับขนาดไฟล์ได้ ซึ่งมีประโยชน์อย่างยิ่งสำหรับภาพย่อ, ไอคอน, หรือเมื่อแบนด์วิธจำกัด

## ทำไมต้องใช้ Aspose.PSD สำหรับ Java?
Aspose.PSD สำหรับ Java ให้ API ระดับสูงที่ทำให้การทำงานกับรูปแบบ PSD ง่ายขึ้น มันช่วยให้คุณ **create grayscale png**, **save png with options**, และจัดการโปรไฟล์สีโดยไม่ต้องยุ่งกับการจัดการไบต์ระดับต่ำ ไลบรารีนี้เป็นแบบจัดการเต็มรูปแบบ, รองรับหลายแพลตฟอร์ม, และได้รับการอัปเดตเป็นประจำ

## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะลงลึกในโค้ด โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

1. **Java Development Kit (JDK)** – ดาวน์โหลดจาก [Oracle’s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – รับ JAR ล่าสุดจาก [this link](https://releases.aspose.com/psd/java/).  
3. **Basic Java knowledge** – คุณควรคุ้นเคยกับคลาส, เมธอด, และการจัดการข้อยกเว้น  
4. **An IDE** เช่น IntelliJ IDEA หรือ Eclipse (ไม่บังคับแต่แนะนำ)  
5. **A sample PSD file** – วางไฟล์ในโฟลเดอร์ที่คุณจะอ้างอิงในโค้ด  

พร้อมหรือยัง? ดีมาก – เรามานำเข้าแพ็กเกจที่จำเป็นกัน

## นำเข้าแพ็กเกจ
ตอนนี้เรามีข้อกำหนดครบแล้ว ถึงเวลาตั้งค่าสภาพแวดล้อมโดยการนำเข้าแพ็กเกจที่เกี่ยวข้องในแอปพลิเคชัน Java ของเรา เปิดสภาพแวดล้อมการเขียนโค้ดและเพิ่มคำสั่ง import ด้านล่างนี้ที่ส่วนหัวของไฟล์ Java ของคุณ:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

คำสั่งเหล่านี้จะนำเข้าคลาสที่เราจะใช้ตลอดบทแนะนำ ทำให้เราสามารถโหลดไฟล์ PSD และบันทึกเป็น PNG ด้วยความลึกบิตที่กำหนดได้

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสารของคุณ
ก่อนจะเริ่มประมวลผลภาพ เรามากำหนดโฟลเดอร์ที่ภาพของเราจะถูกจัดเก็บ เหมือนกับการสร้างที่เก็บอุปกรณ์ศิลปะก่อนเริ่มโครงการฝีมือ

```java
String dataDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: โหลดภาพ PSD
ต่อไปเราต้องโหลดไฟล์ภาพ PSD ที่ต้องการแปลง เหมือนกับการเปิดผ้าใบที่คุณจะทำงานทั้งหมด

```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
```

ที่นี่เราจะใช้เมธอด `Image.load()` เพื่ออ่านไฟล์ PSD ตัวอย่างของเราและแคสท์เป็น `PsdImage` เพื่อเข้าถึงคุณสมบัติเฉพาะของ PSD

## ขั้นตอนที่ 3: สร้าง PNG Options
เมื่อเราเปิดผ้าใบแล้ว เราต้องกำหนดชุดตัวเลือกสำหรับการบันทึกภาพ นี่คือการเลือกสีและสไตล์แปรงก่อนเริ่มวาด

```java
PngOptions options = new PngOptions();
```

ในขั้นตอนนี้เราจะสร้างอินสแตนซ์ของ `PngOptions` ซึ่งให้เรากำหนดพารามิเตอร์สำหรับผลลัพธ์ PNG

## ขั้นตอนที่ 4: ตั้งค่าประเภทสีที่ต้องการ
ต่อไปเราตัดสินใจว่าจะใช้สีแบบไหนใน PNG สุดท้ายของเรา คุณต้องการพาเลตสีสันสดใสหรือสไตล์โมโนโครม? มาตัดสินใจกัน!

```java
options.setColorType(PngColorType.Grayscale);
```

ในตัวอย่างนี้เราตั้งค่า `color type` เป็นระดับสีเทา (grayscale) คุณก็สามารถเลือก `PngColorType.TrueColor` หากต้องการภาพสีเต็มรูปแบบ นี่คือส่วนที่เราจะ **create grayscale png** 

## ขั้นตอนที่ 5: ระบุความลึกบิต
ต่อไปเราจะระบุความลึกบิต ซึ่งคล้ายกับการบอกเครื่องพิมพ์ว่าควรพิมพ์ภาพของคุณละเอียดแค่ไหน – บิตมากเท่าไหร่ รายละเอียดก็ยิ่งมาก!

```java
options.setBitDepth((byte)1);
```

ที่นี่เราตั้งค่าความลึกบิตเป็น **1 bit** ซึ่งเหมาะกับภาพระดับสีเทาแบบง่าย คุณสามารถเปลี่ยนค่าเป็น 2, 4, 8 หรือ 16 ตามความต้องการคุณภาพของคุณ – ตัวอย่างคลาสสิกของการ **change png bit depth**

## ขั้นตอนที่ 6: บันทึกภาพ PNG
สุดท้ายถึงเวลาบันทึกผลงานของคุณ! ขั้นตอนนี้สรุปโครงการของเราโดยการย้ายงานศิลปะจากผ้าใบแก้ไขไปยังผนังแกลเลอรี

```java
psdImage.save(dataDir + "SpecifyBitDepth_out.png", options);
```

โดยใช้เมธอด `save()` ของ `PsdImage` เราบันทึกไฟล์ที่แปลงแล้วพร้อมตัวเลือกที่กำหนดไว้ เสร็จแล้ว! ภาพของเราถูกบันทึกด้วยความลึกบิตที่กำหนดเอง

## ปัญหาที่พบบ่อยและวิธีแก้
- **`NullPointerException` เมื่อโหลด PSD** – ตรวจสอบให้แน่ใจว่า `dataDir` ชี้ไปยังโฟลเดอร์ที่ถูกต้องและไฟล์ `sample.psd` มีอยู่จริง  
- **Unsupported bit depth** – Aspose.PSD รองรับ 1, 2, 4, 8, และ 16 บิตสำหรับ PNG การใช้ค่าที่ไม่อยู่ในรายการจะทำให้เกิด `IllegalArgumentException`  
- **Color type mismatch** – หากคุณตั้งค่าความลึกบิตที่ไม่สอดคล้องกับ `PngColorType` ที่เลือก ไลบรารีจะปรับอัตโนมัติไปยังการตั้งค่าที่รองรับใกล้เคียงที่สุด

## คำถามที่พบบ่อย

**Q: Aspose.PSD สำหรับ Java คืออะไร?**  
A: Aspose.PSD สำหรับ Java เป็นไลบรารีสำหรับทำงานกับไฟล์ PSD ในแอปพลิเคชัน Java ที่ช่วยให้คุณจัดการและแปลงภาพได้

**Q: ฉันจะกำหนดความลึกบิตต่าง ๆ ได้อย่างไร?**  
A: คุณสามารถตั้งค่าความลึกบิตโดยใช้เมธอด `options.setBitDepth((byte)n)` โดยแทนที่ `n` ด้วยค่าที่ต้องการ

**Q: ฉันสามารถใช้ Aspose.PSD ได้ฟรีหรือไม่?**  
A: ใช่ คุณสามารถทดลองใช้ไลบรารีด้วยเวอร์ชันทดลองฟรีที่คุณสามารถหาได้ [here](https://releases.aspose.com/)

**Q: ฉันจะขอรับใบอนุญาตสนับสนุนสำหรับ Aspose ได้จากที่ไหน?**  
A: สำหรับใบอนุญาตชั่วคราว คุณสามารถสมัครได้ [here](https://purchase.aspose.com/temporary-license/)

**Q: ฉันสามารถแปลงภาพประเภทใดได้บ้าง?**  
A: Aspose.PSD เน้นการทำงานกับไฟล์ PSD แต่รองรับการแปลงเป็นหลายรูปแบบเช่น PNG, JPEG, และ TIFF

## สรุป
คุณได้เรียนรู้วิธี **convert psd to png** พร้อมควบคุมความลึกบิตของ PNG ด้วย Aspose.PSD สำหรับ Java แล้ว โดยการปรับ `PngOptions` คุณสามารถ **adjust png quality**, สร้าง **grayscale png**, และปรับขนาดไฟล์ให้เหมาะกับสถานการณ์ใด ๆ ทดลองใช้ประเภทสีและความลึกบิตต่าง ๆ เพื่อหาสมดุลที่ดีที่สุดสำหรับแอปพลิเคชันของคุณ

---

**Last Updated:** 2026-03-18  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}