---
date: 2026-06-28
description: เรียนรู้วิธีตั้งค่า overlay opacity ใน Java, ใช้ color overlay, และปรับแต่ง
  overlay color ด้วย Aspose.PSD for Java. คู่มือขั้นตอนโดยพร้อมตัวอย่างที่พร้อมรัน.
keywords:
- set overlay opacity java
- Aspose.PSD overlay effect
- Java PSD color overlay
linktitle: ใช้ Color Overlay Effect
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to set overlay opacity java, apply a color overlay, and customize
    overlay color using Aspose.PSD for Java. Step‑by‑run guide with ready‑to‑run examples.
  headline: How to Set Overlay Opacity Java with Aspose.PSD
  type: TechArticle
- description: Learn how to set overlay opacity java, apply a color overlay, and customize
    overlay color using Aspose.PSD for Java. Step‑by‑run guide with ready‑to‑run examples.
  name: How to Set Overlay Opacity Java with Aspose.PSD
  steps:
  - name: Set Your Document Directory
    text: The `File` class represents a file system path. Replace **Your Document
      Directory** with the absolute path where your PSD files reside.
  - name: Load PSD File with Effects
    text: '`LoadOptions` tells Aspose.PSD how to read the file. Setting `setLoadEffectsResource(true)`
      ensures existing layer effects, including any colour overlay, are loaded and
      become accessible.'
  - name: Access Color Overlay Effect
    text: '`Layer` is Aspose.PSD’s representation of a PSD layer. `ColorOverlayEffect`
      is the specific effect object that controls colour overlay properties. Here
      we retrieve the first effect of the second layer (index 1). Adjust the indices
      if your PSD structure differs.'
  - name: Customize Overlay Color and Set Overlay Opacity
    text: The `ColorOverlayEffect` class represents a color overlay effect applied
      to a PSD layer. - **Colour** – Use any static colour from `java.awt.Color` or
      create a custom one with `new Color(r, g, b)`. - **Opacity** – The opacity byte
      ranges from 0 (fully transparent) to 255 (fully opaque). In this exam
  - name: Save the Modified PSD File
    text: '`save` writes the updated document back to disk. The edited file, *ColorOverlayChanged.psd*,
      now contains the new overlay colour and opacity.'
  type: HowTo
- questions:
  - answer: No, a layer can have only one `ColorOverlayEffect`. To simulate multiple
      colours, duplicate the layer and apply separate overlays.
    question: Can I apply multiple overlays to a single layer?
  - answer: Yes, it works with Eclipse, IntelliJ IDEA, NetBeans, and any IDE that
      supports Maven or Gradle.
    question: Is Aspose.PSD compatible with different Java IDEs?
  - answer: Yes, you can use it in both personal and commercial applications. Visit
      [here](https://purchase.aspose.com/buy) for licensing details.
    question: Can I use Aspose.PSD for commercial projects?
  - answer: Visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) for community
      help or purchase a [temporary license](https://purchase.aspose.com/temporary-license/)
      for priority support.
    question: How can I get support for Aspose.PSD?
  - answer: Yes, explore the [free trial](https://releases.aspose.com/) version before
      deciding.
    question: Are there free trial options available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: วิธีตั้งค่า overlay opacity ใน Java ด้วย Aspose.PSD
url: /th/java/image-editing/color-overlay-effect/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีตั้งค่าความทึบของ Overlay ใน Java ด้วย Aspose.PSD

## คำนำ

ยินดีต้อนรับสู่โลกของการออกแบบกราฟิกและการจัดการภาพด้วย Aspose.PSD สำหรับ Java! ในบทเรียนนี้คุณจะได้เรียนรู้ **วิธีตั้งค่าความทึบของ overlay java**, การใส่สี overlay ให้กับเลเยอร์ PSD, และการปรับแต่งสี overlay ไม่ว่าคุณจะสร้างเครื่องมือประมวลผลแบบชุดหรือเพิ่มสีแบรนด์ให้กับการออกแบบ ขั้นตอนต่อไปนี้จะนำคุณผ่านทุกอย่างที่ต้องการ ตั้งแต่ข้อกำหนดเบื้องต้นจนถึงการบันทึกไฟล์ขั้นสุดท้าย

## คำตอบสั้น
- **ไลบรารีที่ใช้คืออะไร?** Aspose.PSD for Java  
- **เป้าหมายหลักคืออะไร?** ตั้งค่าความทึบของ overlay java, ใส่สี overlay, และบันทึกไฟล์ PSD ที่แก้ไขแล้ว  
- **ข้อกำหนดเบื้องต้นคืออะไร?** Java 8+, Aspose.PSD for Java, ไฟล์ PSD ที่มีอย่างน้อยหนึ่งเลเยอร์  
- **ระยะเวลาในการทำงานโดยประมาณคือ?** 10‑15 นาทีสำหรับ overlay พื้นฐาน  
- **ฉันสามารถเปลี่ยนสี overlay ได้ภายหลังหรือไม่?** ได้ – แก้ไขคุณสมบัติของ `ColorOverlayEffect` แล้วบันทึกใหม่  

## อะไรคือ set overlay opacity java?
เมธอด `setOpacity(byte)` กำหนดระดับความโปร่งใสของ overlay คำว่า “set overlay opacity java” หมายถึงการปรับค่าความทึบ (0‑255) ของเอฟเฟกต์สี‑overlay บนเลเยอร์ PSD ด้วยโค้ด Java ใน Aspose.PSD คุณควบคุมความทึบผ่านเมธอด `ColorOverlayEffect.setOpacity(byte)` ซึ่งส่งผลโดยตรงต่อความโปร่งใสหรือความทึบของ overlay

## ทำไมต้องใช้ Aspose.PSD สำหรับการทำงานกับ overlay?
Aspose.PSD รักษาความสมบูรณ์ของ PSD **100 %** และรองรับ **กว่า 50 ฟอร์แมต** (รวมถึง PSD, PNG, JPEG, TIFF, และ BMP) สามารถประมวลผลไฟล์ขนาด **ถึง 500 MB** โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ ทำให้เหมาะกับการทำงานอัตโนมัติบนเซิร์ฟเวอร์ ไม่ต้องติดตั้ง Adobe Photoshop และโค้ด Java เดียวกันทำงานได้บน Windows, Linux, และ macOS

## ข้อกำหนดเบื้องต้น

- **สภาพแวดล้อมการพัฒนา Java** – ติดตั้ง JDK 8 หรือสูงกว่า  
- **ไลบรารี Aspose.PSD** – ดาวน์โหลดและติดตั้งไลบรารี Aspose.PSD สำหรับ Java จาก [here](https://releases.aspose.com/psd/java/)  
- **เอกสาร PSD** – ไฟล์ PSD (เช่น *ColorOverlay.psd*) ที่มีอย่างน้อยหนึ่งเลเยอร์ที่คุณต้องการใส่ overlay  

## นำเข้าแพ็กเกจ

ในโปรเจกต์ Java ของคุณ ให้นำเข้าแพ็กเกจที่จำเป็น เพื่อให้คอมไพเลอร์สามารถหาคลาสที่คุณจะใช้ได้

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## คู่มือขั้นตอนโดยละเอียด

### ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสารของคุณ

คลาส `File` แทนที่เส้นทางของระบบไฟล์  
แทนที่ **Your Document Directory** ด้วยเส้นทางเต็มที่ไฟล์ PSD ของคุณอยู่

```java
String dataDir = "Your Document Directory";
```

### ขั้นตอนที่ 2: โหลดไฟล์ PSD พร้อมเอฟเฟกต์

`LoadOptions` บอก Aspose.PSD ว่าจะอ่านไฟล์อย่างไร การตั้งค่า `setLoadEffectsResource(true)` ทำให้เอฟเฟกต์เลเยอร์ที่มีอยู่ รวมถึง colour overlay ถูกโหลดและสามารถเข้าถึงได้

```java
String sourceFileName = dataDir + "ColorOverlay.psd";
String psdPathAfterChange = dataDir + "ColorOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### ขั้นตอนที่ 3: เข้าถึงเอฟเฟกต์ Color Overlay

`Layer` คือการแทนเลเยอร์ PSD ของ Aspose.PSD `ColorOverlayEffect` คืออ็อบเจกต์เอฟเฟกต์ที่ควบคุมคุณสมบัติของ colour overlay  
ที่นี่เราจะดึงเอฟเฟกต์แรกของเลเยอร์ที่สอง (ดัชนี 1) ปรับดัชนีหากโครงสร้าง PSD ของคุณแตกต่าง

```java
com.aspose.psd.fileformats.psd.layers.layereffects.ColorOverlayEffect colorOverlay = (com.aspose.psd.fileformats.psd.layers.layereffects.ColorOverlayEffect)
        (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### ขั้นตอนที่ 4: ปรับแต่งสี Overlay และตั้งค่าความทึบของ Overlay

คลาส `ColorOverlayEffect` แทนเอฟเฟกต์สี overlay ที่ใช้กับเลเยอร์ PSD  
- **Colour** – ใช้สีใดก็ได้จาก `java.awt.Color` หรือสร้างสีกำหนดเองด้วย `new Color(r, g, b)`  
- **Opacity** – ค่าบายต์ความทึบอยู่ระหว่าง 0 (โปร่งใสเต็ม) ถึง 255 (ทึบเต็ม) ในตัวอย่างนี้ตั้งค่าเป็น 50 % (`128`)  

> **เคล็ดลับพิเศษ:** เพื่อ **เปลี่ยนสี overlay ของ PSD** อย่างไดนามิก ให้อ่านค่าฮีกซ์ที่ต้องการจากไฟล์คอนฟิกและแปลงด้วย `Color.fromArgb()`

```java
colorOverlay.setColor(Color.getGreen());
colorOverlay.setOpacity((byte) 128);
```

### ขั้นตอนที่ 5: บันทึกไฟล์ PSD ที่แก้ไขแล้ว

เมธอด `save` จะเขียนเอกสารที่อัปเดตกลับไปยังดิสก์ ไฟล์ที่แก้ไขแล้ว *ColorOverlayChanged.psd* จะมีสี overlay และความทึบใหม่แล้ว

```java
im.save(psdPathAfterChange);
```

## วิธีตั้งค่า overlay opacity java

คลาส `ColorOverlayEffect` แทนเอฟเฟกต์สี overlay ที่ใช้กับเลเยอร์ PSD โหลด PSD เป้าหมาย, ดึง `ColorOverlayEffect` จากเลเยอร์ที่ต้องการ, เรียก `setOpacity((byte)128)` (หรือค่าใดก็ได้ 0‑255) แล้วบันทึกเอกสาร การเปลี่ยนแปลงบรรทัดเดียวนี้จะปรับความโปร่งใสของ overlay ทันทีโดยไม่กระทบคุณสมบัติอื่นของเลเยอร์

## กรณีการใช้งานทั่วไป

- **การสร้างแบรนด์** – ใส่สี overlay ของบริษัทลงในสื่อการตลาดเป็นชุด  
- **การออกแบบธีม** – สลับ mockup UI ระหว่างธีมสว่างและมืดแบบไดนามิก  
- **การตรวจสอบ** – ทดสอบว่าความทึบของ overlay ต่าง ๆ มีผลต่อการอ่านข้อความบนพื้นหลังซับซ้อนอย่างไร  

## ปัญหาทั่วไปและวิธีแก้ไข

| ปัญหา | วิธีแก้ไข |
|-------|----------|
| **Overlay ไม่แสดง** | ตรวจสอบให้แน่ใจว่าได้ตั้งค่า `loadOptions.setLoadEffectsResource(true)` แล้วและเลเยอร์เป้าหมายมี `ColorOverlayEffect` จริง |
| **ดัชนีเลเยอร์ไม่ถูกต้อง** | ใช้ `psdImage.getLayers()` เพื่อตรวจสอบชื่อเลเยอร์และเลือกดัชนีที่ถูกต้อง |
| **ความทึบดูแสง/มืดเกินไป** | ปรับค่าบายต์ (0‑255) จำไว้ว่า 255 คือทึบเต็ม |
| **สีไม่ถูกนำไปใช้** | ยืนยันว่าคุณใช้ `colorOverlay.setColor()` กับอินสแตนซ์ `java.awt.Color` ที่ถูกต้อง |

## คำถามที่พบบ่อย

**Q: ฉันสามารถใส่ overlay หลายชั้นบนเลเยอร์เดียวได้หรือไม่?**  
A: ไม่ได้, เลเยอร์หนึ่งสามารถมี `ColorOverlayEffect` ได้เพียงหนึ่งอ็อบเจกต์เท่านั้น หากต้องการจำลองหลายสีให้ทำการคัดลอกเลเยอร์และใส่ overlay แยกกัน

**Q: Aspose.PSD รองรับ IDE ของ Java ต่าง ๆ หรือไม่?**  
A: รองรับ, ทำงานได้กับ Eclipse, IntelliJ IDEA, NetBeans และ IDE ใด ๆ ที่สนับสนุน Maven หรือ Gradle

**Q: ฉันสามารถใช้ Aspose.PSD ในโครงการเชิงพาณิชย์ได้หรือไม่?**  
A: ได้, คุณสามารถใช้ได้ทั้งในแอปพลิเคชันส่วนบุคคลและเชิงพาณิชย์ เยี่ยมชม [here](https://purchase.aspose.com/buy) เพื่อดูรายละเอียดการให้สิทธิ์ใช้งาน

**Q: ฉันจะขอรับการสนับสนุนสำหรับ Aspose.PSD ได้อย่างไร?**  
A: เยี่ยมชม [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) เพื่อขอความช่วยเหลือจากชุมชน หรือซื้อ [temporary license](https://purchase.aspose.com/temporary-license/) เพื่อรับการสนับสนุนแบบเร่งด่วน

**Q: มีตัวเลือกทดลองใช้ฟรีหรือไม่?**  
A: มี, สำรวจเวอร์ชัน [free trial](https://releases.aspose.com/) ก่อนตัดสินใจ

**อัปเดตล่าสุด:** 2026-06-28  
**ทดสอบด้วย:** Aspose.PSD 24.11 for Java  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [ตั้งค่าความทึบของเลเยอร์และสนับสนุน Blend Modes ใน Aspose.PSD สำหรับ Java](/psd/java/basic-image-operations/support-blend-modes/)
- [ตั้งค่าความทึบของ Fill สำหรับเลเยอร์ PSD ด้วย Aspose.PSD Java](/psd/java/psd-image-modification-conversion/set-fill-opacity-psd-layers/)
- [เพิ่มเอฟเฟกต์ Pattern Overlay ใน Aspose.PSD สำหรับ Java](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}