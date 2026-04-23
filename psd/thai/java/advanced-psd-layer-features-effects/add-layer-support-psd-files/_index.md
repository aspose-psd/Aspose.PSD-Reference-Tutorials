---
date: 2026-02-17
description: เรียนรู้วิธีดึงชั้น PSD และแปลงชั้น PSD เป็น PNG ด้วย Aspose.PSD สำหรับ
  Java เหมาะสำหรับนักพัฒนาที่ต้องการการจัดการกราฟิกที่แข็งแรง
linktitle: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
  Java
second_title: Aspose.PSD Java API
title: ดึงชั้น PSD และเพิ่มการสนับสนุนชั้นสำหรับไฟล์ PSD ด้วย Aspose.PSD Java
url: /th/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ดึงชั้น PSD และเพิ่มการสนับสนุนชั้นสำหรับไฟล์ PSD ด้วย Aspose.PSD Java

## บทนำ
การทำงานกับไฟล์ Photoshop Document (PSD) เป็นความเป็นจริงในชีวิตประจำวันของนักออกแบบกราฟิกและนักพัฒนาด้วยกัน หนึ่งในงานที่พบบ่อยที่สุดคือ **การดึงชั้น PSD** เพื่อให้สามารถแก้ไข ใช้ซ้ำ หรือแปลงเป็นรูปแบบอื่นเช่น PNG ในแอปพลิเคชัน Java, Aspose.PSD ทำให้กระบวนการนี้ตรงไปตรงมาและเป็นมิตรต่อโค้ด ในบทแนะนำนี้เราจะเดินผ่านขั้นตอนที่จำเป็นทั้งหมดเพื่อดึงชั้น PSD, เปิดใช้งานการสนับสนุนชั้น, และ **แปลงชั้น PSD เป็น PNG** — ทั้งหมดด้วยคำอธิบายที่ชัดเจนและเคล็ดลับที่ใช้งานได้จริง

## คำตอบสั้น
- **“การดึงชั้น PSD” หมายความว่าอะไร?** หมายถึงการโหลดไฟล์ PSD และเข้าถึงแต่ละชั้นเพื่อทำการปรับเปลี่ยนหรือส่งออก  
- **ไลบรารีใดจัดการเรื่องนี้ใน Java?** Aspose.PSD for Java ให้การประมวลผล PSD อย่างครบวงจรโดยไม่ต้องใช้ Photoshop  
- **ฉันสามารถแปลงชั้น PSD เป็น PNG ได้ในขั้นตอนเดียวหรือไม่?** ได้ — โดยโหลดไฟล์ด้วยตัวเลือกที่เหมาะสมและบันทึกด้วย PNG options ที่รักษาความโปร่งใส  
- **ต้องใช้ไลเซนส์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานในผลิตภัณฑ์; มีรุ่นทดลองฟรีสำหรับการประเมินผล  
- **ต้องใช้ Java เวอร์ชันใด?** JDK 8 หรือสูงกว่า (บทแนะนำใช้ JDK 11 เป็นตัวอย่าง)

## วิธีดึงชั้น PSD ด้วย Aspose.PSD for Java
ด้านล่างนี้เป็นคำแนะนำแบบขั้นตอนที่ครอบคลุมทุกอย่างตั้งแต่การตั้งค่าสภาพแวดล้อมจนถึงการบันทึก PNG สุดท้าย ทำตามขั้นตอนที่ระบุไว้ตามลำดับ คุณจะได้โซลูชันที่ทำงานได้ในไม่กี่นาที

## ทำไมต้องดึงชั้น PSD และแปลงเป็น PNG?
- **ใช้ซ้ำทรัพยากร:** ดึงไอคอน, ปุ่ม, หรือองค์ประกอบ UI จาก PSD หลักโดยไม่ต้องส่งออกด้วยตนเอง  
- **อัตโนมัติ:** สร้างภาพตัวอย่างหรือภาพพร้อมใช้งานบนเว็บแบบไดนามิก  
- **รักษาความโปร่งใส:** PNG เก็บช่องอัลฟา ทำให้เหมาะกับกราฟิกเว็บ  
- **ข้ามแพลตฟอร์ม:** ไม่ต้องมี Photoshop บนเซิร์ฟเวอร์; Aspose.PSD ทำงานได้ทุกที่ที่ Java ทำงาน

## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะลงลึก, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมแล้ว:

1. **สภาพแวดล้อมการพัฒนา Java** – ติดตั้ง JDK คุณสามารถดาวน์โหลดได้จาก [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)  
2. **Aspose.PSD for Java** – ดาวน์โหลดไลบรารีล่าสุดจากหน้าดาวน์โหลดอย่างเป็นทางการ [here](https://releases.aspose.com/psd/java/)  
3. **ความรู้พื้นฐาน Java** – คุ้นเคยกับการคอมไพล์และรันโปรแกรม Java  
4. **IDE** – IntelliJ IDEA, Eclipse หรือเครื่องมือแก้ไขใดก็ได้ที่คุณชอบ  
5. **ไฟล์ PSD** – ใช้ไฟล์ PSD ใดก็ได้ที่คุณมี, หรือดาวน์โหลด PSD ตัวอย่างสำหรับการทดสอบ  

เมื่อคุณเตรียมสิ่งเหล่านี้พร้อมแล้ว, คุณก็พร้อมเริ่มดึงชั้น PSD

## นำเข้าแพ็กเกจ
เริ่มต้นด้วยการนำเข้าคลาสที่จำเป็นจากไลบรารี Aspose.PSD

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## ขั้นตอนที่ 1: กำหนดไดเรกทอรีของคุณ
ตั้งค่าพาธสำหรับ PSD ต้นทางและ PNG ปลายทาง ปรับ `dataDir` ให้ชี้ไปยังโฟลเดอร์ที่ไฟล์ของคุณอยู่

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – แทนที่ `"Your Document Directory"` ด้วยพาธโฟลเดอร์จริงของคุณ  
- `sourceFileName` – พาธเต็มของไฟล์ PSD ที่ต้องการประมวลผล  
- `output` – พาธปลายทางสำหรับ PNG ที่จะบรรจุชั้นที่ดึงออกมา

## ขั้นตอนที่ 2: ตั้งค่า Load Options
การกำหนดค่า `PsdLoadOptions` ทำให้แน่ใจว่าทุกเอฟเฟกต์และทรัพยากรของชั้นถูกโหลดอย่างถูกต้อง, ซึ่งเป็นสิ่งสำคัญเมื่อ **ดึงชั้น PSD**

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

ในขั้นตอนนี้, `image` จะมีทุกชั้น, มาสก์, และเอฟเฟกต์ พร้อมสำหรับการดึงออก

## ขั้นตอนที่ 4: ตั้งค่า Save Options
กำหนดวิธีการบันทึก PNG การใช้ `TruecolorWithAlpha` จะรักษาความโปร่งใสจากชั้นต้นฉบับ

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## ขั้นตอนที่ 5: บันทึกภาพ (แปลงชั้น PSD เป็น PNG)
ส่งออก PSD ที่โหลด (พร้อมทุกชั้น) ไปเป็นไฟล์ PNG เดียว ขั้นตอนนี้ทำให้ **แปลงชั้น PSD เป็น PNG** ในการดำเนินการเดียว

```java
image.save(output, saveOptions);
```

หากคุณต้องการแต่ละชั้นเป็น PNG แยกไฟล์, สามารถวนลูป `image.getLayers()` — แต่สำหรับหลายกรณี PNG ที่รวมชั้นทั้งหมดก็เพียงพอ

## ขั้นตอนที่ 6: สรุป
เพิ่มข้อความคอนโซลเพื่อให้คุณทราบว่ากระบวนการสำเร็จ

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## ปัญหาและเคล็ดลับทั่วไป
- **Out‑of‑Memory Errors:** หากคุณประมวลผล PSD ขนาดใหญ่มาก, ควรเปิด `setUseDiskForLoadEffectsResource(true)` เพื่อย้ายข้อมูลชั่วคราวไปยังดิสก์  
- **Missing Effects:** ตรวจสอบให้แน่ใจว่าได้ตั้งค่า `setLoadEffectsResource(true)` มิฉะนั้นเอฟเฟกต์บางอย่างอาจถูกละเว้น  
- **Path Problems:** ใช้ `Paths.get(...)` จาก `java.nio.file` เพื่อจัดการพาธแบบข้ามแพลตฟอร์ม

## คำถามที่พบบ่อย

**Q: Aspose.PSD for Java คืออะไร?**  
A: Aspose.PSD for Java เป็นไลบรารีที่ช่วยให้คุณจัดการไฟล์ PSD ได้โดยไม่ต้องติดตั้ง Photoshop

**Q: สามารถใช้ Aspose.PSD กับรูปแบบไฟล์อื่นได้หรือไม่?**  
A: ใช่! แม้จะเน้นที่ไฟล์ PSD, Aspose มีไลบรารีสำหรับรูปแบบไฟล์อื่น ๆ อีกหลายประเภท

**Q: มีรุ่นทดลองให้ดาวน์โหลดหรือไม่?**  
A: แน่นอน! คุณสามารถดาวน์โหลดรุ่นทดลองฟรีได้ [here](https://releases.aspose.com/)

**Q: จะหาการสนับสนุนได้จากที่ไหนหากต้องการความช่วยเหลือ?**  
A: คุณสามารถเข้าถึงฟอรั่มสนับสนุนของ Aspose ได้ [here](https://forum.aspose.com/c/psd/34)

**Q: สามารถแปลงจาก PNG กลับเป็น PSD ได้หรือไม่?**  
A: ไลบรารี Aspose.PSD มุ่งเน้นการอ่านและจัดการไฟล์ PSD มากกว่าการแปลงรูปแบบอื่นกลับเป็น PSD

**Q: จะดึงแต่ละชั้นเป็น PNG แยกไฟล์ได้อย่างไร?**  
A: วนลูป `image.getLayers()`, สร้าง `Bitmap` ใหม่สำหรับแต่ละชั้น, แล้วบันทึกด้วย `PngOptions` ของแต่ละชั้น ซึ่งจะให้ไฟล์ PNG แยกตามชั้น

## สรุป
คุณได้เรียนรู้วิธี **ดึงชั้น PSD**, เปิดใช้งานการสนับสนุนชั้นเต็มรูปแบบ, และ **แปลงชั้น PSD เป็น PNG** ด้วย Aspose.PSD for Java ไม่ว่าคุณจะสร้างระบบอัตโนมัติสำหรับจัดการทรัพยากรหรือเพิ่มความสามารถด้านกราฟิกให้กับแอปเดสก์ท็อป, วิธีนี้ให้การควบคุมระดับละเอียดต่อไฟล์ Photoshop โดยไม่ต้องพึ่งพา Photoshop เอง อย่าลังเลที่จะสำรวจต่อ เช่น การใช้ฟิลเตอร์, การรวมชั้นโดยโปรแกรม, หรือการส่งออกแต่ละชั้นแยกเป็นไฟล์

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}