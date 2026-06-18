---
date: 2026-06-18
description: เรียนรู้วิธีการเปลี่ยนสีเงาใน Java และปรับแต่งเอฟเฟกต์เงาโดยใช้ Aspose.PSD
  for Java. ทำตามบทแนะนำการสร้างเอฟเฟกต์เงาแบบ step‑by‑step.
keywords:
- change shadow color java
- Aspose.PSD shadow effect
- Java PSD manipulation
linktitle: สนับสนุนเอฟเฟกต์เงา
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how to change shadow color java and customize shadow effects
    using Asprose.PSD for Java. Follow this step‑by‑step shadow effect tutorial.
  headline: Change Shadow Color Java with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to change shadow color java and customize shadow effects
    using Asprose.PSD for Java. Follow this step‑by‑step shadow effect tutorial.
  name: Change Shadow Color Java with Aspose.PSD for Java
  steps:
  - name: Load the PSD Image
    text: 'First, load the source PSD while enabling the loading of effect resources:'
  - name: Retrieve the Existing Drop Shadow Effect
    text: 'Locate the shadow effect on the desired layer (in this example, the second
      layer):'
  - name: Verify the Default Settings (Optional)
    text: 'Running these assertions helps you understand the original values before
      you modify them:'
  - name: '**Change Shadow Color** and Customize Other Properties'
    text: Now we actually **change shadow color** to green, adjust opacity, distance,
      size, and other attributes. This demonstrates the **customize shadow effect**
      capabilities of Aspose.PSD. The `setOpacity(byte)` method sets the shadow's
      opacity level (0‑255).
  - name: Save the Modified Image
    text: 'Finally, write the updated PSD back to disk using the `save` method of
      `PsdImage`:'
  type: HowTo
- questions:
  - answer: Absolutely! Aspose.PSD for Java is a powerful library designed for professional
      graphic design tasks.
    question: Is Aspose.PSD for Java suitable for professional graphic design projects?
  - answer: Yes, Aspose.PSD for Java is a commercial product. You can purchase it
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial applications?
  - answer: Yes, you can explore a free trial version [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Refer to the comprehensive documentation [here](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Join the community forum [here](https://forum.aspose.com/c/psd/34) for
      any support queries.
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: เปลี่ยนสีเงาใน Java ด้วย Aspose.PSD for Java
url: /th/java/basic-image-operations/support-shadow-effect/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เปลี่ยนสีเงา Java ด้วย Aspose.PSD สำหรับ Java

## บทนำ

การเพิ่มความลึกให้กับกราฟิกของคุณมักหมายถึง **การเปลี่ยนสีเงา** ให้สอดคล้องกับอารมณ์ของการออกแบบ ด้วย Aspose.PSD สำหรับ Java คุณสามารถเพิ่มหรือแก้ไขเอฟเฟกต์เงาตก, ควบคุมความทึบ, และปรับแต่งพารามิเตอร์อื่น ๆ ได้อย่างง่ายดาย—ทั้งหมดจากโค้ด Java ใน **บทเรียนเอฟเฟกต์เงา** นี้ เราจะอธิบายขั้นตอนการโหลดไฟล์ PSD, อ่านเงาที่มีอยู่, ปรับสี, ความทึบ, ระยะทาง, และสุดท้ายบันทึกไฟล์ที่อัปเดต คำแนะนำนี้แสดงวิธี **เปลี่ยนสีเงา java** อย่างชัดเจนและทำซ้ำได้

## คำตอบอย่างรวดเร็ว
- **“การเปลี่ยนสีเงา” หมายถึงอะไร?** มันอัปเดตคุณสมบัติสีของ DropShadowEffect ที่ใช้กับเลเยอร์ PSD  
- **ไลบรารีใดรองรับ?** Aspose.PSD สำหรับ Java ให้การสนับสนุนเต็มรูปแบบสำหรับเอฟเฟกต์เงา  
- **ต้องมีลิขสิทธิ์หรือไม่?** รุ่นทดลองใช้ได้สำหรับการพัฒนา; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการผลิต  
- **สามารถตั้งค่าความทึบของเงาได้หรือไม่?** ใช่ – ใช้ `setOpacity(byte)` เพื่อกำหนดความโปร่งใส (0‑255)  
- **โค้ดเข้ากันได้กับ Java 8+ หรือไม่?** แน่นอน, API รองรับ Java 8 และรุ่นต่อ ๆ ไป

## “การเปลี่ยนสีเงา” ในไฟล์ PSD คืออะไร?

การเปลี่ยนสีเงาจะปรับโทนสีของเงาตกที่ปรากฏอยู่ด้านหลังเลเยอร์ การปรับนี้ช่วยให้ดีไซเนอร์จำลองสภาพแสงต่าง ๆ, ทำให้เงาตรงกับพาเลตสีของแบรนด์, และเพิ่มความเป็นศิลปะให้กับคอมโพสชัน โดยการเปลี่ยนโทนสีคุณสามารถทำให้เงาดูอุ่น, เย็น, หรือแม้กระทั่งตรงกับโทนสีเฉพาะได้ เพิ่มผลกระทบภาพโดยรวม

## ทำไมต้องใช้ Aspose.PSD สำหรับ Java เพื่อปรับแต่งเอฟเฟกต์เงา?

Aspose.PSD สำหรับ Java รองรับ **รูปแบบภาพกว่า 100** แบบและสามารถประมวลผลไฟล์ PSD ขนาด **ถึง 2 GB** โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ ให้ประสิทธิภาพระดับองค์กร ไลบรารีให้คุณควบคุมคุณสมบัติของเงาทุกอย่าง—สี, ความทึบ, ระยะ, มุม, การกระจาย, และนอยส์—โดยไม่ต้องติดตั้ง Photoshop ทำงานบน JVM ของ Windows, Linux, และ macOS ทำให้เป็นตัวเลือกที่เชื่อถือได้ที่สุดสำหรับกระบวนการกราฟิกอัตโนมัติ

## ข้อกำหนดเบื้องต้น

- ความรู้พื้นฐานด้านการเขียนโปรแกรม Java  
- ติดตั้ง Aspose.PSD สำหรับ Java คุณสามารถดาวน์โหลดได้ [ที่นี่](https://releases.aspose.com/psd/java/)  

## นำเข้าแพ็กเกจ

ก่อนเริ่มทำงาน ให้นำเข้าคลาสที่จำเป็นเพื่อทำงานกับภาพและเอฟเฟกต์เงา:

คลาส `Color` แทนค่สีที่ใช้ทั่ว API  
คลาส `Image` เป็นประเภทพื้นฐานสำหรับอ็อบเจกต์ภาพทั้งหมด  
คลาส `PsdImage` ให้ฟังก์ชันเฉพาะสำหรับไฟล์ PSD  
คลาส `PsdLoadOptions` ให้คุณระบุการตั้งค่าสำหรับการโหลดไฟล์ PSD เช่นการเปิดใช้งานทรัพยากรเอฟเฟกต์  
คลาส `DropShadowEffect` แทนฟิลเตอร์เงาตกที่ใช้กับเลเยอร์ PSD และให้เข้าถึงคุณสมบัติที่ปรับได้ทั้งหมด  

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## คู่มือขั้นตอนโดยละเอียด

### ขั้นตอนที่ 1: โหลดภาพ PSD

โหลด PSD ต้นฉบับพร้อมเปิดใช้งานการโหลดทรัพยากรเอฟเฟกต์:

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

### ขั้นตอนที่ 3: ตรวจสอบการตั้งค่าเริ่มต้น (ไม่บังคับ)

การเรียกใช้การตรวจสอบเหล่านี้ช่วยให้คุณเข้าใจค่าต้นฉบับก่อนทำการแก้ไข:

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

ตอนนี้เราจะ **เปลี่ยนสีเงา** เป็นสีเขียว, ปรับความทึบ, ระยะ, ขนาด, และคุณลักษณะอื่น ๆ ซึ่งแสดงความสามารถ **ปรับแต่งเอฟเฟกต์เงา** ของ Aspose.PSD วิธี `setOpacity(byte)` ตั้งค่าระดับความทึบของเงา (0‑255)  

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

สุดท้ายให้บันทึก PSD ที่อัปเดตกลับไปยังดิสก์โดยใช้เมธอด `save` ของ `PsdImage`:

```java
im.save(psdPathAfterChange);
```

## ปัญหาทั่วไปและเคล็ดลับ

- **NullPointerException เมื่อดึงเอฟเฟกต์** – ตรวจสอบให้แน่ใจว่าได้เรียก `setLoadEffectsResource(true)`; มิฉะนั้นเอฟเฟกต์จะไม่ถูกโหลด  
- **สีไม่เปลี่ยน** – ตรวจสอบว่าคุณกำลังแก้ไขเลเยอร์ที่ถูกต้อง (`im.getLayers()[1]` ในตัวอย่างนี้)  
- **ความทึบดูเหมือนไม่เปลี่ยน** – จำไว้ว่าความทึบเป็น byte (0‑255) ต้องทำการแคสต์เป็น `(byte)`  

## สรุป

โดยทำตามขั้นตอนเหล่านี้คุณสามารถ **เปลี่ยนสีเงา**, **ตั้งค่าความทึบของเงา**, และปรับ **พารามิเตอร์เอฟเฟกต์เงา** ทั้งหมดในไฟล์ PSD ใด ๆ ด้วย Aspose.PSD สำหรับ Java ซึ่งช่วยให้คุณสร้างกราฟิกที่สมบูรณ์แบบโดยอัตโนมัติโดยไม่ต้องใช้ Photoshop ด้วยตนเอง เหมาะสำหรับสายงานออกแบบอัตโนมัติและการประมวลผลเป็นชุด

## คำถามที่พบบ่อย

**ถาม: Aspose.PSD สำหรับ Java เหมาะกับโครงการออกแบบกราฟิกระดับมืออาชีพหรือไม่?**  
ตอบ: แน่นอน! Aspose.PSD สำหรับ Java เป็นไลบรารีที่ทรงพลังออกแบบมาสำหรับงานออกแบบกราฟิกระดับมืออาชีพ

**ถาม: ฉันสามารถใช้ Aspose.PSD สำหรับ Java ในแอปพลิเคชันเชิงพาณิชย์ได้หรือไม่?**  
ตอบ: ใช่, Aspose.PSD สำหรับ Java เป็นผลิตภัณฑ์เชิงพาณิชย์ คุณสามารถซื้อได้ที่ [here](https://purchase.aspose.com/buy).

**ถาม: มีรุ่นทดลองใช้ฟรีหรือไม่?**  
ตอบ: มี, คุณสามารถสำรวจรุ่นทดลองใช้ฟรีได้ที่ [here](https://releases.aspose.com/).

**ถาม: ฉันสามารถหาเอกสารรายละเอียดได้ที่ไหน?**  
ตอบ: ดูเอกสารที่ครอบคลุมได้ที่ [here](https://reference.aspose.com/psd/java/).

**ถาม: ฉันจะรับการสนับสนุนสำหรับ Aspose.PSD สำหรับ Java ได้อย่างไร?**  
ตอบ: เข้าร่วมฟอรั่มชุมชนได้ที่ [here](https://forum.aspose.com/c/psd/34) สำหรับคำถามสนับสนุนใด ๆ.

---

**อัปเดตล่าสุด:** 2026-06-18  
**ทดสอบด้วย:** Aspose.PSD for Java 24.10  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทเรียนที่เกี่ยวข้อง

- [การจัดการภาพ Java - เพิ่มเอฟเฟกต์ขณะทำงานด้วย Aspose.PSD สำหรับ Java](/psd/java/advanced-techniques/add-effects-runtime/)
- [บันทึก PSD เป็น PNG และใช้การเรนเดอร์ Drop Shadow ใน Aspose.PSD สำหรับ Java](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [เบลอภาพ Java ด้วย Aspose.PSD – เพิ่มเอฟเฟกต์เบลอ](/psd/java/advanced-techniques/blur-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}