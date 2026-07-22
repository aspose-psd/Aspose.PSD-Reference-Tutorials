---
date: 2026-07-22
description: เรียนรู้วิธีสกัดชั้น PSD และแปลงชั้น PSD เป็น PNG ด้วย Aspose.PSD for
  Java เหมาะสำหรับนักพัฒนาที่ต้องการการจัดการกราฟิกที่มีประสิทธิภาพ
keywords:
- extract psd layers
- how to extract psd
- convert psd to png
lastmod: 2026-07-22
linktitle: สกัดชั้น PSD และเพิ่มการสนับสนุนชั้นสำหรับไฟล์ PSD ด้วย Aspose.PSD Java
og_description: สกัดชั้น PSD และแปลงเป็น PNG ด้วย Aspose.PSD for Java ทำตามคู่มือ
  step‑by‑step นี้เพื่ออัตโนมัติการสกัดชั้นและการแปลงภาพ
og_image_alt: Developer guide showing Java code to extract PSD layers and save as
  PNG using Aspose.PSD
og_title: สกัดชั้น PSD – เพิ่มการสนับสนุนชั้นสำหรับไฟล์ PSD ด้วย Aspose.PSD Java
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to extract PSD layers and convert PSD layers to PNG using
    Aspose.PSD for Java. Ideal for developers needing robust graphics manipulation.
  headline: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
    Java
  type: TechArticle
- description: Learn how to extract PSD layers and convert PSD layers to PNG using
    Aspose.PSD for Java. Ideal for developers needing robust graphics manipulation.
  name: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD Java
  steps:
  - name: '**Java Development Environment** – JDK installed. You can download it from
      the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Environment** – JDK installed. You can download it from
      the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java** – Grab the latest library from the official download
      page [here](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – Grab the latest library from the official download
      page [here](https://releases.aspose.com/psd/java/).'
  - name: '**Basic Java knowledge** – Familiarity with compiling and running Java
      programs.'
    text: '**Basic Java knowledge** – Familiarity with compiling and running Java
      programs.'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**A PSD file** – Use any PSD you have, or download a sample PSD for testing.'
    text: '**A PSD file** – Use any PSD you have, or download a sample PSD for testing.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that allows you to manipulate PSD files
      without having Photoshop installed.
    question: What is Aspose.PSD for Java?
  - answer: Yes! While primarily for PSD files, Aspose offers libraries for a wide
      range of formats, including AI, PDF, and SVG.
    question: Can I use Aspose.PSD for other file formats?
  - answer: Absolutely! You can download a free trial version [here](https://releases.aspose.com/).
    question: Is a trial version available?
  - answer: Access the Aspose forum for PSD‑related questions [here](https://forum.aspose.com/c/psd/34).
    question: Where can I get support if I run into problems?
  - answer: Iterate over `image.getLayers()`, create a new `Bitmap` for each layer,
      and save it with its own `PngOptions`. This yields individual PNG files per
      layer.
    question: Can I convert each layer to a separate PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- extract psd
- Aspose.PSD
- Java image processing
title: สกัดชั้น PSD และเพิ่มการสนับสนุนชั้นสำหรับไฟล์ PSD ด้วย Aspose.PSD Java
url: /th/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ดึงชั้น PSD และเพิ่มการสนับสนุนชั้นสำหรับไฟล์ PSD ด้วย Aspose.PSD Java

## บทนำ
การทำงานกับไฟล์ Photoshop Document (PSD) เป็นความเป็นจริงในชีวิตประจำวันของนักออกแบบกราฟิกและนักพัฒนาซอฟต์แวร์เช่นกัน และ **extract psd layers** มักเป็นขั้นตอนแรกในการนำทรัพยากรกลับมาใช้ใหม่หรือทำให้กระบวนการภาพอัตโนมัติ ในบทแนะนำนี้คุณจะได้เรียนรู้วิธีดึงชั้นแต่ละชั้นจากไฟล์ PSD, เปิดใช้งานการสนับสนุนชั้นเต็มรูปแบบ, และ **convert PSD layers to PNG** ด้วย Aspose.PSD for Java เราจะครอบคลุมทุกอย่างตั้งแต่การตั้งค่าสภาพแวดล้อมจนถึงเคล็ดลับการปฏิบัติที่ดีที่สุด เพื่อให้คุณสามารถรวมเวิร์กโฟลว์นี้เข้าในแอปพลิเคชัน Java ใดก็ได้ในไม่กี่นาที

## คำตอบสั้น
- **What does “extract PSD layers” mean?** หมายถึงการโหลดไฟล์ PSD และเข้าถึงแต่ละชั้นเพื่อการปรับแต่งหรือส่งออก  
- **Which library handles this in Java?** Aspose.PSD for Java ให้การประมวลผล PSD ที่ครบถ้วนโดยไม่ต้องใช้ Photoshop  
- **Can I convert PSD layers to PNG in one go?** ใช่—โดยการโหลดไฟล์ด้วยตัวเลือกที่เหมาะสมและบันทึกด้วยตัวเลือก PNG ที่รักษาความโปร่งใส  
- **Do I need a license for production use?** จำเป็นต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานในผลิตภัณฑ์; มีรุ่นทดลองฟรีสำหรับการประเมิน  
- **What Java version is required?** JDK 8 หรือสูงกว่า (บทแนะนำนี้ใช้ JDK 11 เป็นตัวอย่าง)

## วิธีดึงชั้น PSD ด้วย Aspose.PSD for Java?
โหลดไฟล์ PSD, เปิดใช้งานเอฟเฟกต์ของชั้น, และบันทึกผลลัพธ์เป็น PNG เพียงไม่กี่บรรทัดของโค้ด Java วิธีตรงนี้ช่วยขจัดความจำเป็นในการใช้ Photoshop บนเซิร์ฟเวอร์และทำงานบนแพลตฟอร์มใดก็ได้ที่รองรับ Java 8+  
คุณเริ่มต้นด้วยการสร้างอ็อบเจกต์ `PsdLoadOptions` ด้วย `setLoadEffectsResource(true)` และ `setUseDiskForLoadEffectsResource(true)`, จากนั้นโหลดไฟล์ด้วย `PsdImage.load(path, options)` หลังจากโหลดแล้วคุณสามารถรวมชั้นโดยใช้ `image.save(outputPath, new PngOptions())` หรือวนลูปผ่าน `image.getLayers()` เพื่อส่งออกแต่ละชั้นแยกกัน, ทำให้มั่นใจว่าเอฟเฟกต์ทั้งหมดถูกเก็บไว้ในขณะที่ใช้หน่วยความจำน้อย

## ทำไมต้องดึงชั้น PSD และแปลงเป็น PNG?
การดึงชั้นทำให้คุณ **reuse assets**, **automate thumbnail generation**, และ **preserve transparency** สำหรับกราฟิกที่พร้อมใช้งานบนเว็บ Aspose.PSD รองรับ **50+ input and output formats** และสามารถประมวลผลไฟล์ PSD หลายร้อยหน้าโดยไม่ต้องโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ, ขอบคุณการจัดการทรัพยากรแบบดิสก์

## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่ม, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

1. **Java Development Environment** – ติดตั้ง JDK แล้ว คุณสามารถดาวน์โหลดได้จาก [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java** – รับไลบรารีล่าสุดจากหน้าดาวน์โหลดอย่างเป็นทางการ [here](https://releases.aspose.com/psd/java/).  
3. **Basic Java knowledge** – ความคุ้นเคยกับการคอมไพล์และรันโปรแกรม Java.  
4. **IDE** – IntelliJ IDEA, Eclipse หรือเครื่องมือแก้ไขใดที่คุณชอบ.  
5. **A PSD file** – ใช้ไฟล์ PSD ใดก็ได้ที่คุณมี, หรือดาวน์โหลด PSD ตัวอย่างสำหรับการทดสอบ.

เมื่อคุณเตรียมพร้อมแล้ว, คุณพร้อมที่จะเริ่มดึงชั้น PSD

## นำเข้าแพ็กเกจ
`PsdImage`, `PsdLoadOptions`, และ `PngOptions` เป็นคลาสหลักของเวิร์กโฟลว์  
`PsdImage` คืออ็อบเจกต์ระดับบนของ Aspose.PSD ที่แสดงไฟล์ PSD เดียวในหน่วยความจำ  
`PsdLoadOptions` ให้คุณควบคุมวิธีการโหลดทรัพยากรเช่นเอฟเฟกต์ของชั้น  
`PngOptions` กำหนดรูปแบบเอาต์พุตและการจัดการความโปร่งใสสำหรับไฟล์ PNG

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## ขั้นตอนที่ 1: กำหนดไดเรกทอรีของคุณ
ตั้งค่าพาธสำหรับ PSD ต้นฉบับและ PNG ผลลัพธ์ ปรับ `dataDir` ให้ชี้ไปยังโฟลเดอร์ที่ไฟล์ของคุณอยู่

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – แทนที่ `"Your Document Directory"` ด้วยพาธโฟลเดอร์จริงของคุณ  
- `sourceFileName` – พาธเต็มของไฟล์ PSD ที่คุณต้องการประมวลผล  
- `output` – พาธปลายทางสำหรับ PNG ที่จะบรรจุชั้นที่ดึงออกมา

## ขั้นตอนที่ 2: ตั้งค่าตัวเลือกการโหลด
การกำหนดค่า `PsdLoadOptions` ทำให้แน่ใจว่าทุกเอฟเฟกต์และทรัพยากรของชั้นถูกโหลดอย่างถูกต้อง, ซึ่งเป็นสิ่งสำคัญเมื่อคุณ **extract PSD layers**.

```java
PsdLoadOptions imageLoadOptions = new PsdLoadOptions();
imageLoadOptions.setLoadEffectsResource(true);
imageLoadOptions.setUseDiskForLoadEffectsResource(true);
```

- `setLoadEffectsResource(true)` – โหลดเอฟเฟกต์เพิ่มเติม (เช่นเงาตก) ที่แนบกับชั้น  
- `setUseDiskForLoadEffectsResource(true)` – ย้ายทรัพยากรหนักไปยังดิสก์ เพื่อลดความกดดันของหน่วยความจำ

## ขั้นตอนที่ 3: โหลดไฟล์ PSD
ตอนนี้เราจะโหลด PSD เข้าไปในอ็อบเจกต์ `PsdImage` โดยใช้ตัวเลือกที่กำหนดไว้ข้างต้น

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, imageLoadOptions);
```

ในขั้นตอนนี้, `image` มีชั้นทั้งหมด, มาสก์, และเอฟเฟกต์, พร้อมสำหรับการดึงข้อมูล

## ขั้นตอนที่ 4: ตั้งค่าตัวเลือกการบันทึก
กำหนดวิธีการบันทึก PNG โดยใช้ `TruecolorWithAlpha` จะรักษาความโปร่งใสจากชั้นต้นฉบับ

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## ขั้นตอนที่ 5: บันทึกภาพ (แปลงชั้น PSD เป็น PNG)
ส่งออก PSD ที่โหลดแล้ว (พร้อมทุกชั้น) ไปเป็นไฟล์ PNG เดียว ขั้นตอนนี้ทำให้ **convert psd layers png** อย่างมีประสิทธิภาพในหนึ่งการดำเนินการ

```java
image.save(output, saveOptions);
```

หากคุณต้องการแต่ละชั้นเป็น PNG แยกต่างหาก, คุณสามารถวนลูปผ่าน `image.getLayers()`—แต่สำหรับหลายกรณีการใช้ PNG ที่รวมกันก็เพียงพอ

## ขั้นตอนที่ 6: สรุป
เพิ่มข้อความคอนโซลที่เป็นมิตรเพื่อให้คุณทราบว่ากระบวนการสำเร็จ

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## ปัญหาทั่วไป & เคล็ดลับ
- **Out‑of‑Memory Errors:** หากคุณกำลังประมวลผล PSD ขนาดใหญ่มาก, ให้เปิดใช้งาน `setUseDiskForLoadEffectsResource(true)` เพื่อย้ายข้อมูลชั่วคราวไปยังดิสก์  
- **Missing Effects:** ตรวจสอบให้แน่ใจว่าได้ตั้งค่า `setLoadEffectsResource(true)`; หากไม่ตั้งค่าเอฟเฟกต์ของบางชั้นอาจถูกละเว้น  
- **Path Problems:** ใช้ `Paths.get(...)` จาก `java.nio.file` เพื่อจัดการพาธที่ไม่ขึ้นกับแพลตฟอร์ม

## คำถามที่พบบ่อย

**Q: What is Aspose.PSD for Java?**  
A: Aspose.PSD for Java เป็นไลบรารีที่ช่วยให้คุณจัดการไฟล์ PSD ได้โดยไม่ต้องติดตั้ง Photoshop  

**Q: Can I use Aspose.PSD for other file formats?**  
A: ใช่! แม้ว่าจะเน้นที่ไฟล์ PSD, Aspose มีไลบรารีสำหรับรูปแบบไฟล์หลากหลายรวมถึง AI, PDF, และ SVG  

**Q: Is a trial version available?**  
A: แน่นอน! คุณสามารถดาวน์โหลดรุ่นทดลองฟรีได้ [here](https://releases.aspose.com/).  

**Q: Where can I get support if I run into problems?**  
A: เข้าถึงฟอรั่มของ Aspose สำหรับคำถามเกี่ยวกับ PSD [here](https://forum.aspose.com/c/psd/34).  

**Q: Can I convert each layer to a separate PNG?**  
A: วนลูปผ่าน `image.getLayers()`, สร้าง `Bitmap` ใหม่สำหรับแต่ละชั้น, และบันทึกด้วย `PngOptions` ของมันเอง ซึ่งจะได้ไฟล์ PNG แยกตามชั้น  

## สรุป
คุณได้เรียนรู้วิธี **extract PSD layers**, เปิดใช้งานการสนับสนุนชั้นเต็มรูปแบบ, และ **convert PSD layers to PNG** ด้วย Aspose.PSD for Java แล้ว ไม่ว่าคุณจะสร้างสายงานอัตโนมัติสำหรับทรัพยากรหรือเพิ่มความสามารถกราฟิกให้กับแอปเดสก์ท็อป, วิธีนี้ให้การควบคุมระดับละเอียดต่อไฟล์ Photoshop โดยไม่ต้องใช้ Photoshop เอง สำรวจต่อไปโดยการใช้ฟิลเตอร์, รวมชั้นด้วยโปรแกรม, หรือส่งออกแต่ละชั้นแยกตามความต้องการของคุณ

---

**อัปเดตล่าสุด:** 2026-07-22  
**ทดสอบด้วย:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [ส่งออก PSD เป็น PNG และเพิ่มเลเยอร์ปกติใหม่โดยใช้ Aspose.PSD for Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [ส่งออก PSD เป็น PNG พร้อมการสนับสนุน Layer Mask ใน Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [แปลง PSD เป็น Image ใน Java – ใช้ Adjustment Layers กับ Aspose.PSD](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}