---
date: 2025-12-30
description: เรียนรู้วิธีเปลี่ยนสีเงาและปรับแต่งเอฟเฟกต์เงาโดยใช้ Aspose.PSD สำหรับ
  Java. ทำตามบทแนะนำการสร้างเอฟเฟกต์เงาแบบขั้นตอนต่อขั้นตอนนี้.
linktitle: Support Shadow Effect
second_title: Aspose.PSD Java API
title: วิธีเปลี่ยนสีเงาด้วย Aspose.PSD สำหรับ Java
url: /th/java/basic-image-operations/support-shadow-effect/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เปลี่ยนสีเงาด้วย Aspose.PSD for Java

## บทนำ

การเพิ่มความลึกให้กับกราฟิกมักหมายถึง **การเปลี่ยนสีเงา** ให้สอดคล้องกับอารมณ์ของการออกแบบ ด้วย Aspose.PSD for Java คุณสามารถเพิ่มหรือแก้ไขเอฟเฟกต์เงาตก, ควบคุมความทึบแสง, และปรับแต่งพารามิเตอร์อื่น ๆ ได้อย่างง่ายดายโดยใช้โค้ด Java ใน **บทเรียนการทำเงา** นี้ เราจะอธิบายขั้นตอนการโหลดไฟล์ PSD, อ่านเงาที่มีอยู่, ปรับสี, ความทึบ, ระยะห่าง, และสุดท้ายบันทึกไฟล์ที่อัปเดต

## คำตอบสั้น
- **“เปลี่ยนสีเงา” หมายถึงอะไร?** จะอัปเดตคุณสมบัติสีของ DropShadowEffect ที่ใช้กับเลเยอร์ PSD  
- **ไลบรารีใดสนับสนุน?** Aspose.PSD for Java ให้การสนับสนุนเต็มรูปแบบสำหรับเอฟเฟกต์เงา  
- **ต้องใช้ไลเซนส์หรือไม่?** เวอร์ชันทดลองใช้ได้สำหรับการพัฒนา; ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **สามารถตั้งค่าความทึบของเงาได้หรือไม่?** ได้ – ใช้ `setOpacity(byte)` เพื่อกำหนดความโปร่งแสง (0‑255)  
- **โค้ดนี้เข้ากันได้กับ Java 8+ หรือไม่?** แน่นอน, API รองรับ Java 8 และรุ่นถัดไป

## “เปลี่ยนสีเงา” ในไฟล์ PSD คืออะไร?

การเปลี่ยนสีเงาจะปรับโทนสีของเงาตกที่ปรากฏอยู่ด้านหลังเลเยอร์ ซึ่งเป็นประโยชน์สำหรับการสร้างแสงที่สมจริง, ทำให้สีตรงกับแบรนด์, หรือเพิ่มความเป็นศิลปะ

## ทำไมต้องใช้ Aspose.PSD for Java เพื่อปรับแต่งเอฟเฟกต์เงา?

- **รักษาความสมบูรณ์ของ PSD** – ทุกเอฟเฟกต์เลเยอร์รวมถึงเงาจะถูกเก็บไว้ครบถ้วน  
- **ไม่ต้องใช้ Photoshop** – จัดการไฟล์โดยอัตโนมัติบนเซิร์ฟเวอร์ใดก็ได้  
- **ควบคุมระดับละเอียด** – ปรับสี, ความทึบ, ระยะห่าง, มุม, การกระจาย, และนอยส์  
- **ข้ามแพลตฟอร์ม** – ทำงานบน JVM ของ Windows, Linux, และ macOS

## ข้อกำหนดเบื้องต้น

- ความรู้พื้นฐานด้านการเขียนโปรแกรม Java  
- ติดตั้ง Aspose.PSD for Java คุณสามารถดาวน์โหลดได้จาก [ที่นี่](https://releases.aspose.com/psd/java/)  

## นำเข้าแพ็กเกจ

ก่อนเริ่มทำงาน ให้นำเข้าคลาสที่จำเป็นเพื่อจัดการภาพและเอฟเฟกต์เงา:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## คู่มือแบบขั้นตอน

### ขั้นตอนที่ 1: โหลดภาพ PSD

โหลดไฟล์ PSD ต้นฉบับพร้อมเปิดใช้งานการโหลดทรัพยากรเอฟเฟกต์:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### ขั้นตอนที่ 2: ดึงเอฟเฟกต์ Drop Shadow ที่มีอยู่

ค้นหาเอฟเฟกต์เงาบนเลเยอร์ที่ต้องการ (ในตัวอย่างนี้คือเลเยอร์ที่สอง):

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### ขั้นตอนที่ 3: ตรวจสอบค่าตั้งต้น (ไม่บังคับ)

การรันการตรวจสอบเหล่านี้ช่วยให้คุณเข้าใจค่าต้นฉบับก่อนทำการแก้ไข:

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

### ขั้นตอนที่ 4: **เปลี่ยนสีเงา** และปรับคุณสมบัติอื่น ๆ

ตอนนี้เราจะ **เปลี่ยนสีเงา** เป็นสีเขียว, ปรับความทึบ, ระยะห่าง, ขนาด, และคุณลักษณะอื่น ๆ ซึ่งแสดงถึงความสามารถ **ปรับแต่งเอฟเฟกต์เงา** ของ Aspose.PSD:

```java
shadowEffect.setColor(Color.getGreen());          // change shadow color
shadowEffect.setOpacity((byte)128);               // set shadow opacity (50% transparent)
shadowEffect.setDistance(11);                     // move shadow farther from the object
shadowEffect.setUseGlobalLight(false);            // use local lighting
shadowEffect.setSize(9);                          // adjust blur radius
shadowEffect.setAngle(45);                        // rotate light source
shadowEffect.setSpread(3);                        // increase spread
shadowEffect.setNoise(50);                        // add texture noise
```

### ขั้นตอนที่ 5: บันทึกภาพที่แก้ไขแล้ว

สุดท้ายให้เขียนไฟล์ PSD ที่อัปเดตกลับไปยังดิสก์:

```java
im.save(psdPathAfterChange);
```

## ปัญหาที่พบบ่อย & เคล็ดลับ

- **NullPointerException เมื่อดึงเอฟเฟกต์** – ตรวจสอบให้แน่ใจว่าได้เรียก `setLoadEffectsResource(true)`; มิฉะนั้นเอฟเฟกต์จะไม่ถูกโหลด  
- **สีไม่เปลี่ยน** – ตรวจสอบว่าคุณแก้ไขเลเยอร์ที่ถูกต้อง (`im.getLayers()[1]` ในตัวอย่างนี้)  
- **ความทึบดูเหมือนไม่เปลี่ยน** – จำไว้ว่าความทึบเป็นประเภท byte (0‑255) ต้องแคสท์เป็น `(byte)`  

## สรุป

โดยทำตามขั้นตอนเหล่านี้คุณสามารถ **เปลี่ยนสีเงา**, **ตั้งค่าความทึบของเงา**, และปรับ **พารามิเตอร์เอฟเฟกต์เงา** ทั้งหมดในไฟล์ PSD ใด ๆ ด้วย Aspose.PSD for Java ซึ่งช่วยให้คุณสร้างกราฟิกที่สมบูรณ์แบบโดยอัตโนมัติโดยไม่ต้องใช้ Photoshop ด้วยตนเอง

## คำถามที่พบบ่อย

**ถาม: Aspose.PSD for Java เหมาะกับโครงการออกแบบกราฟิกระดับมืออาชีพหรือไม่?**  
ตอบ: แน่นอน! Aspose.PSD for Java เป็นไลบรารีที่ทรงพลังออกแบบมาสำหรับงานออกแบบกราฟิกระดับมืออาชีพ

**ถาม: สามารถใช้ Aspose.PSD for Java ในแอปพลิเคชันเชิงพาณิชย์ได้หรือไม่?**  
ตอบ: ได้, Aspose.PSD for Java เป็นผลิตภัณฑ์เชิงพาณิชย์ คุณสามารถซื้อได้ [ที่นี่](https://purchase.aspose.com/buy)

**ถาม: มีเวอร์ชันทดลองฟรีหรือไม่?**  
ตอบ: มี, คุณสามารถสำรวจเวอร์ชันทดลองฟรีได้ [ที่นี่](https://releases.aspose.com/)

**ถาม: จะหาเอกสารรายละเอียดได้จากที่ไหน?**  
ตอบ: ดูเอกสารฉบับสมบูรณ์ได้ [ที่นี่](https://reference.aspose.com/psd/java/)

**ถาม: จะรับการสนับสนุนสำหรับ Aspose.PSD for Java อย่างไร?**  
ตอบ: เข้าร่วมฟอรั่มชุมชน [ที่นี่](https://forum.aspose.com/c/psd/34) สำหรับคำถามสนับสนุนใด ๆ  

---

**อัปเดตล่าสุด:** 2025-12-30  
**ทดสอบด้วย:** Aspose.PSD for Java 24.10  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}