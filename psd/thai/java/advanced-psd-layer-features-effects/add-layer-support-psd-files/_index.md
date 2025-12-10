---
date: 2025-12-10
description: เรียนรู้วิธีดึงชั้น PSD และแปลงชั้น PSD เป็น PNG ด้วย Aspose.PSD สำหรับ
  Java เหมาะสำหรับนักพัฒนาที่ต้องการการจัดการกราฟิกที่แข็งแรง
linktitle: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
  Java
second_title: Aspose.PSD Java API
title: สกัดชั้น PSD และเพิ่มการสนับสนุนชั้นสำหรับไฟล์ PSD ด้วย Aspose.PSD Java
url: /th/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สกัดชั้น PSD และเพิ่มการสนับสนุนชั้นสำหรับไฟล์ PSD ด้วย Aspose.PSD Java

## Introduction
การทำงานกับไฟล์ Photoshop Document (PSD) เป็นความเป็นจริงในชีวิตประจำวันของนักออกแบบกราฟิกและนักพัฒนาซอฟต์แวร์เช่นกัน หนึ่งในงานที่พบบ่อยที่สุดคือ **การสกัดชั้น PSD** เพื่อให้สามารถแก้ไข ใช้ซ้ำ หรือแปลงเป็นรูปแบบอื่น ๆ เช่น PNG ในแอปพลิเคชัน Java Aspose.PSD ทำให้กระบวนการนี้ง่ายและเป็นมิตรต่อโค้ด ในบทแนะนำนี้เราจะพาคุณผ่านขั้นตอนที่จำเป็นทั้งหมดเพื่อสกัดชั้น PSD เปิดการสนับสนุนชั้น และ **แปลงชั้น PSD เป็น PNG** — ทั้งหมดพร้อมคำอธิบายที่ชัดเจนและเคล็ดลับที่ใช้งานได้จริง

## Quick Answers
- **“การสกัดชั้น PSD” หมายถึงอะไร?** หมายถึงการโหลดไฟล์ PSD แล้วเข้าถึงแต่ละชั้นแยกจากกันเพื่อทำการจัดการหรือส่งออก  
- **ไลบรารีใดจัดการเรื่องนี้ใน Java?** Aspose.PSD for Java ให้การประมวลผล PSD อย่างครบวงจรโดยไม่ต้องใช้ Photoshop  
- **ฉันสามารถแปลงชั้น PSD เป็น PNG ได้ในครั้งเดียวหรือไม่?** ได้ — โดยโหลดไฟล์ด้วยตัวเลือกที่เหมาะสมและบันทึกด้วยตัวเลือก PNG ที่รักษาความโปร่งใสไว้  
- **ต้องใช้ไลเซนส์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานในผลิตภัณฑ์; มีรุ่นทดลองฟรีสำหรับการประเมินผล  
- **ต้องใช้เวอร์ชัน Java ใด?** JDK 8 หรือสูงกว่า (บทแนะนำใช้ JDK 11 เป็นตัวอย่าง)

## What is “extract PSD layers”?
การสกัดชั้น PSD หมายถึงการอ่านโครงสร้างภายในของไฟล์ PSD และดึงแต่ละชั้นออกมาเป็นอ็อบเจ็กต์ภาพอิสระ ซึ่งทำให้คุณสามารถแก้ไข ซ่อน เปลี่ยนลำดับ หรือส่งออกชั้นแต่ละชั้นได้อย่างอิสระ — เหมือนกับที่นักออกแบบทำใน Photoshop แต่ทำแบบโปรแกรม

## Why extract PSD layers and convert them to PNG?
- **Reuse assets:** ดึงไอคอน ปุ่ม หรือองค์ประกอบ UI จาก PSD หลักโดยไม่ต้องส่งออกด้วยตนเอง  
- **Automation:** สร้างภาพย่อหรือภาพพร้อมใช้งานบนเว็บโดยอัตโนมัติ  
- **Preserve transparency:** PNG รักษาชาแนลอัลฟ่า ทำให้เหมาะกับกราฟิกบนเว็บ

## Prerequisites
ก่อนที่เราจะเริ่ม ให้ตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมแล้วหรือยัง:

1. **Java Development Environment** – ติดตั้ง JDK คุณสามารถดาวน์โหลดได้จาก [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)  
2. **Aspose.PSD for Java** – ดาวน์โหลดไลบรารีล่าสุดจากหน้าดาวน์โหลดอย่างเป็นทางการ [here](https://releases.aspose.com/psd/java/)  
3. **Basic Java knowledge** – มีความคุ้นเคยกับการคอมไพล์และรันโปรแกรม Java  
4. **IDE** – IntelliJ IDEA, Eclipse หรือโปรแกรมแก้ไขใด ๆ ที่คุณชอบ  
5. **A PSD file** – ใช้ไฟล์ PSD ใดก็ได้ที่คุณมี หรือดาวน์โหลดตัวอย่าง PSD สำหรับการทดสอบ  

เมื่อคุณเตรียมสิ่งเหล่านี้ครบแล้ว คุณพร้อมที่จะเริ่มสกัดชั้น PSD ได้แล้ว

## Import Packages
First, import the classes we’ll need from the Aspose.PSD library.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Step 1: Define Your Directories
Set up the paths for the source PSD and the output PNG. Adjust the `dataDir` to point to the folder where your files reside.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – Replace `"Your Document Directory"` with your actual folder path.  
- `sourceFileName` – Full path to the PSD you want to process.  
- `output` – Destination path for the PNG that will contain the extracted layers.

## Step 2: Set Up the Load Options
Configuring `PsdLoadOptions` ensures that all layer effects and resources are loaded correctly, which is essential when you **extract PSD layers**.

```java
PsdLoadOptions imageLoadOptions = new PsdLoadOptions();
imageLoadOptions.setLoadEffectsResource(true);
imageLoadOptions.setUseDiskForLoadEffectsResource(true);
```

- `setLoadEffectsResource(true)` – Loads additional **effects** (like drop shadows) attached to layers.  
- `setUseDiskForLoadEffectsResource(true)` – Offloads heavy resources to **disk**, reducing memory pressure.

## Step 3: Load the PSD File
Now we load the PSD into a `PsdImage` object using the options defined above.

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, imageLoadOptions);
```

At this point, `image` contains all layers, masks, and effects, ready for extraction.

## Step 4: Set Up the Save Options
Configure how the PNG will be saved. Using `TruecolorWithAlpha` preserves transparency from the original layers.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## Step 5: Save the Image (Convert PSD Layers to PNG)
Export the loaded PSD (with all its **layers**) to a single PNG file. This step effectively **convert psd layers png** in one operation.

```java
image.save(output, saveOptions);
```

If you **need** each **layer** as a separate PNG, you could iterate over `image.getLayers()`—but for many **use‑cases** a merged PNG is sufficient.

## Step 6: Wrap It Up
Add a friendly console message so you know the process succeeded.

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## Common Issues & Tips
- **Out‑of‑Memory Errors:** If you’re processing very large PSDs, keep `setUseDiskForLoadEffectsResource(true)` enabled to offload temporary data.  
- **Missing Effects:** Ensure `setLoadEffectsResource(true)` is set; otherwise some **layer effects** may be ignored.  
- **Path Problems:** Use `Paths.get(...)` from `java.nio.file` for platform‑independent path handling.

## Frequently Asked Questions

**Q: Aspose.PSD for Java คืออะไร?**  
A: Aspose.PSD for Java เป็นไลบรารีที่ช่วยให้คุณจัดการไฟล์ PSD ได้โดยไม่ต้องติดตั้ง Photoshop

**Q: ฉันสามารถใช้ Aspose.PSD กับรูปแบบไฟล์อื่นได้หรือไม่?**  
A: ได้! แม้ว่าไลบรารีนี้จะเน้นที่ไฟล์ PSD เป็นหลัก แต่ Aspose มีไลบรารีสำหรับรูปแบบไฟล์อื่น ๆ อีกหลายประเภท

**Q: มีรุ่นทดลองให้ดาวน์โหลดหรือไม่?**  
A: แน่นอน! คุณสามารถดาวน์โหลดรุ่นทดลองฟรีได้ [here](https://releases.aspose.com/)

**Q: จะหาการสนับสนุนได้จากที่ไหนหากต้องการความช่วยเหลือ?**  
A: คุณสามารถเข้าถึงการสนับสนุนในฟอรั่มของ Aspose [here](https://forum.aspose.com/c/psd/34)

**Q: สามารถแปลงจาก PNG กลับเป็น PSD ได้หรือไม่?**  
A: ไลบรารี Aspose.PSD มุ่งเน้นการอ่านและจัดการไฟล์ PSD มากกว่าการแปลงรูปแบบอื่นกลับเป็น PSD

**Q: จะสกัดแต่ละชั้นเป็น PNG แยกกันอย่างไร?**  
A: ทำการวนลูป `image.getLayers()` สร้าง `Bitmap` ใหม่สำหรับแต่ละชั้น แล้วบันทึกด้วย `PngOptions` ของตัวเอง ซึ่งจะได้ไฟล์ PNG แยกตามชั้น

## Conclusion
You’ve now learned how to **extract PSD layers**, enable full layer support, and **convert PSD layers to PNG** using Aspose.PSD for Java. Whether you’re building an automated asset pipeline or adding graphics capabilities to a desktop app, this approach gives you fine‑grained control over Photoshop files without the need for Photoshop itself. Feel free to explore further—such as applying filters, merging layers programmatically, or exporting each layer individually.

---

**Last Updated:** 2025-12-10  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}