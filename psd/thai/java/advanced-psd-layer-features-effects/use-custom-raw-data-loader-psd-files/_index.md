---
date: 2026-02-22
description: เรียนรู้วิธีการใช้งานอินเทอร์เฟซ IPartialRawDataLoader เพื่อโหลดข้อมูลดิบแบบกำหนดเองในไฟล์ PSD
  ด้วย Aspose.PSD for Java คู่มือแบบขั้นตอนต่อขั้นตอนพร้อมการตั้งค่าและการทำความสะอาด.
linktitle: Use Custom Raw Data Loader in PSD Files - Java
second_title: Aspose.PSD Java API
title: ดำเนินการ IPartialRawDataLoader สำหรับไฟล์ PSD - Java
url: /th/java/advanced-psd-layer-features-effects/use-custom-raw-data-loader-psd-files/
weight: 29
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ใช้ตัวโหลดข้อมูลดิบแบบกำหนดเองในไฟล์ PSD - Java

## Introduction
การทำงานกับไฟล์ PSD ใน Java อาจดูซับซ้อน โดยเฉพาะเมื่อต้องจัดการกับข้อมูลดิบ แต่ไม่ต้องกังวล! ด้วย Aspose.PSD for Java คุณสามารถจัดการและดึงข้อมูลพิกเซลดิบจากไฟล์ PSD ได้อย่างง่ายดายโดยใช้ **custom raw data loader** ในบทแนะนำนี้ คุณจะได้เรียนรู้วิธี **implement IPartialRawDataLoader interface** เพื่อควบคุมสตรีมพิกเซลตามที่ต้องการ คู่มือนี้จะพาคุณผ่านขั้นตอนทั้งหมด ตั้งแต่การตั้งค่าโครงการจนถึงการทำความสะอาดทรัพยากร เพื่อให้คุณเริ่มประมวลผลเลเยอร์ของ PSD ได้อย่างมั่นใจ

## Quick Answers
- **What does a custom raw data loader do?** It lets you intercept and process raw pixel bytes while a PSD file is being read.  
- **Which library provides this feature?** Aspose.PSD for Java includes the `IPartialRawDataLoader` interface.  
- **Do I need a license?** A free trial works for testing; a commercial license is required for production.  
- **What Java version is required?** Java 8 or higher (JDK 11 is recommended).  
- **Can I reuse the loader for multiple files?** Yes—instantiate your loader once and reuse it across images.

## How to implement IPartialRawDataLoader interface
การทำงานกับ `IPartialRawDataLoader` interface จะให้จุดเชื่อมต่อเข้าสู่กระบวนการโหลดข้อมูลดิบ ด้านล่างนี้เราจะสร้างคลาสเล็ก ๆ ที่สอดคล้องกับสัญญาและแสดงตำแหน่งที่คุณสามารถแทรกตรรกะของคุณเอง (เช่น การบันทึก, การแปลง, การสตรีม)

## What is a custom raw data loader?
**custom raw data loader** คือคลาสที่ผู้ใช้สร้างขึ้นซึ่งสอดคล้องกับ `IPartialRawDataLoader` interface มันรับบัฟเฟอร์พิกเซลดิบ, พิกัดสี่เหลี่ยม, และตัวเลือกการโหลดเพิ่มเติม ทำให้คุณมีการควบคุมเต็มที่ว่าข้อมูลพิกเซลจะถูกอ่าน, แปลง, หรือจัดเก็บอย่างไร สิ่งนี้มีประโยชน์อย่างยิ่งสำหรับการวิเคราะห์ภาพแบบกำหนดเอง, การแปลงสีแบบเรียลไทม์, หรือการสตรีม PSD ขนาดใหญ่โดยไม่ต้องโหลดภาพทั้งหมดเข้าสู่หน่วยความจำ

## Why use a custom raw data loader with Aspose.PSD?
- **Performance tuning:** Process only the regions you need, reducing memory footprint.  
- **Specialized workflows:** Apply proprietary compression, encryption, or analytics directly on the pixel stream.  
- **Integration flexibility:** Hook into existing image pipelines or third‑party processing libraries.

## Prerequisites
ก่อนจะลงลึกในส่วนสนุก ๆ เรามาตรวจสอบให้แน่ใจว่าคุณมีทุกอย่างที่จำเป็นสำหรับการเริ่มต้นกับ Aspose.PSD ใน Java ดังต่อไปนี้:

1. **Basic Knowledge of Java** – Familiarity with Java programming is essential.  
2. **Development Environment** – IntelliJ IDEA, Eclipse, or any editor with a command‑line build tool.  
3. **Aspose.PSD Library** – Download the Aspose.PSD for Java library from the [เว็บไซต์](https://releases.aspose.com/psd/java/). You can choose between a free trial or a purchased license.  
4. **Java Development Kit (JDK)** – Make sure a recent JDK is installed. You can download it from the [เว็บไซต์ของ Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) or use OpenJDK.  
5. **Knowledge of PSD Files** – Understanding layers and pixel data will help you make the most of the loader.

เมื่อคุณเตรียมสิ่งเหล่านี้ครบแล้ว คุณก็พร้อมเริ่มเขียนโค้ดได้แล้ว!

## Import Packages
เพื่อใช้ Aspose.PSD อย่างมีประสิทธิภาพในโปรเจกต์ของคุณ คุณต้องนำเข้าชุดแพ็กเกจที่เกี่ยวข้อง ด้านล่างเป็นการนำเข้าขั้นต่ำที่จำเป็นสำหรับตัวอย่างตัวโหลดแบบกำหนดเอง:

```java
import com.aspose.psd.*;
```

## Step 1: Create the RawDataTester Class
ขั้นตอนแรกคือการกำหนดคลาสที่ implements `IPartialRawDataLoader` interface คลาสนี้จะมีเมธอดสำหรับประมวลผลข้อมูลพิกเซลดิบ

```java
class RawDataTester implements IPartialRawDataLoader {
    public void process(Rectangle rectangle, byte[] pixels, Point start, Point end) {
        // Process raw pixel data here
    }
    public void process(Rectangle rectangle, byte[] pixels, Point start, Point end, LoadOptions loadOptions) {
        // Process raw pixel data with load options here
    }
}
```

คลาส `RawDataTester` มีเมธอด `process` สองแบบ คุณสามารถปรับแต่งเมธอดเหล่านี้เพื่อบันทึกข้อมูลพิกเซล, ทำการแปลงแบบกำหนดเอง, หรือสตรีมข้อมูลไปยังบริการอื่นได้

## Step 2: Set Up Paths for PSD File
ต่อไปให้ระบุไดเรกทอรีต้นทางที่เก็บไฟล์ PSD ของคุณ

```java
String sourceDir = "Your Source Directory";
String inFilePath = sourceDir + "CmykWithAlpha.psd";
```

แทนที่ `"Your Source Directory"` ด้วยพาธจริงที่นำไปสู่ไฟล์ PSD ของคุณ และตรวจสอบให้แน่ใจว่าชื่อไฟล์ตรงกับ PSD ที่ต้องการโหลด

## Step 3: Load the PSD File
ตอนนี้เราจะโหลดไฟล์ PSD ด้วยเมธอด `Image.load` ซึ่งจะให้เรามีตัวแทนภาพในหน่วยความจำ

```java
RasterImage image = (RasterImage)Image.load(inFilePath);
```

การแคสต์เป็น `RasterImage` เป็นสิ่งจำเป็นเพราะเมธอด `loadRawData` ที่เราจะใช้ต่อไปอยู่ในคลาสนี้

## Step 4: Initialize RawDataSettings
เมื่อภาพถูกโหลดแล้ว คุณสามารถเริ่มต้น `RawDataSettings` ได้ การตั้งค่านี้กำหนดวิธีการจัดการข้อมูลพิกเซลดิบ

```java
try {
    RawDataSettings rawDataSettings = image.getRawDataSettings();
```

ขั้นตอนนี้ดึงการตั้งค่าที่เกี่ยวข้องกับข้อมูลดิบในไฟล์ PSD เพื่อให้คุณสามารถปรับพฤติกรรมการโหลดได้ตามต้องการ

## Step 5: Load Raw Data with the Custom Loader
สร้างอินสแตนซ์ของตัวโหลดแบบกำหนดเอง (`RawDataTester`) แล้วใช้มันโหลดข้อมูลดิบจากภาพ

```java
    RawDataTester loader = new RawDataTester();
    image.loadRawData(image.getBounds(), rawDataSettings, loader);
```

การเรียก `loadRawData` จะสตรีมข้อมูลพิกเซลผ่านการทำงานของ `RawDataTester` ทำให้คุณควบคุมแต่ละบล็อกไบต์ได้อย่างเต็มที่

## Step 6: Clean Up Resources
หลังจากโหลดข้อมูลดิบสำเร็จแล้ว ควรปล่อยทรัพยากรที่ใช้เพื่อป้องกันการรั่วไหลของหน่วยความจำ

```java
} finally {
    image.dispose();
}
```

บล็อก `finally` จะรับประกันว่าไม่ว่าการทำงานจะสำเร็จหรือไม่ ภาพจะถูกทำลายอย่างถูกต้อง

## Common Pitfalls & Troubleshooting
- **Incorrect path:** Double‑check the file path; a missing slash or typo will cause a `FileNotFoundException`.  
- **Casting errors:** Ensure the loaded image is indeed a `RasterImage`; otherwise, a `ClassCastException` will be thrown.  
- **Loader not invoked:** Verify that your `RawDataTester` methods are correctly overridden; otherwise, the default loader will be used.  
- **Memory usage:** When processing very large PSDs, consider loading only specific rectangles instead of the full bounds to keep memory consumption low.

## Frequently Asked Questions
### What is Aspose.PSD for Java?  
Aspose.PSD for Java is a library that allows developers to manipulate PSD files programmatically, including reading, writing, and editing PSD layers.

### How do I download Aspose.PSD?  
You can download Aspose.PSD for Java from the [หน้ารีลีส](https://releases.aspose.com/psd/java/).

### Can I use Aspose.PSD for free?  
Yes, Aspose.PSD offers a free trial version that you can access [ที่นี่](https://releases.aspose.com/).

### What if I face issues or need support?  
For support and community assistance, you can visit the [ฟอรั่มของ Aspose](https://forum.aspose.com/c/psd/34).

### How can I obtain a temporary license for Aspose.PSD?  
You can acquire a temporary license to evaluate all features by visiting the [หน้าใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/).

---

**อัปเดตล่าสุด:** 2026-02-22  
**ทดสอบด้วย:** Aspose.PSD for Java (เวอร์ชันล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}