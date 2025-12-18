---
date: 2025-12-17
description: เรียนรู้วิธีแปลงไฟล์ PSD เป็น PNG พร้อมตั้งค่าโหมดสีของ PSD เป็นระดับสีเทา
  16‑บิตโดยใช้ Aspose.PSD สำหรับ Java คู่มือขั้นตอนโดยละเอียดพร้อมตัวอย่างโค้ด
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: วิธีแปลง PSD เป็น PNG ด้วยโหมดสีเทา 16‑บิตใน Java
url: /th/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง PSD เป็น PNG ด้วยโหมดสี Grayscale 16-bit ใน Java

## Introduction
เมื่อคุณเริ่มต้นสำรวจโลกของการออกแบบกราฟิกและการจัดการภาพ การเข้าใจวิธี **แปลง PSD เป็น PNG** จะเหมือนกับการมีอาวุธลับโดยเฉพาะ การใช้โหมดสี Grayscale 16‑bit จะทำให้ภาพของคุณมีความลึกและรายละเอียดที่น่าทึ่งอย่างแท้จริง ในบทเรียนนี้เราจะอธิบายวิธี **ตั้งค่าโหมดสีของ PSD** เป็น Grayscale 16‑bit แล้ว **ส่งออก PSD เป็น PNG** ด้วย Aspose.PSD for Java พร้อมหรือยังที่จะยกระดับกระบวนการทำงานกับภาพของคุณ? เริ่มกันเลย

## Quick Answers
- **“แปลง PSD เป็น PNG” มีขั้นตอนอะไรบ้าง?** การโหลดไฟล์ PSD, ปรับเปลี่ยนโหมดสีตามต้องการ, แล้วบันทึกเป็นไฟล์ PNG  
- **คลาสของ Aspose ที่รับผิดชอบการแปลงคืออะไร?** `PsdImage` สำหรับการโหลดและ `PngOptions` สำหรับการบันทึก  
- **ต้องใช้ไลเซนส์พิเศษหรือไม่?** เวอร์ชันทดลองใช้ได้สำหรับการทดสอบ; จำเป็นต้องมีไลเซนส์แบบชำระเงินสำหรับการใช้งานจริง  
- **สามารถเก็บความลึก 16‑bit ไว้ใน PNG ได้หรือไม่?** ได้โดยใช้ `PngColorType.GrayscaleWithAlpha`  
- **IDE ที่รองรับมีอะไรบ้าง?** IDE ใดก็ได้ที่รองรับ Java – IntelliJ IDEA, Eclipse, VS Code ฯลฯ  

## Prerequisites
ก่อนเริ่ม เรามาตรวจสอบให้แน่ใจว่าคุณมีทุกอย่างพร้อมสำหรับบทเรียนนี้:

1. **Java Development Kit (JDK)** – ตรวจสอบว่าคุณได้ติดตั้งเวอร์ชันล่าสุดแล้ว คุณสามารถดาวน์โหลดได้จาก [เว็บไซต์ของ Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)  
2. **Aspose.PSD for Java Library** – นี่คือเอนจินที่จะช่วยให้เราจัดการไฟล์ PSD ได้ ดาวน์โหลดจาก [หน้าดาวน์โหลดของ Aspose](https://releases.aspose.com/psd/java/)  
3. **IDE** – IntelliJ IDEA, Eclipse หรือ Visual Studio Code จะทำงานได้ดี  
4. **ความรู้พื้นฐานของ Java** – ความคุ้นเคยกับไวยากรณ์ของ Java จะทำให้ขั้นตอนต่าง ๆ ราบรื่นขึ้น  
5. **ไฟล์ PSD ตัวอย่าง** – สร้างไฟล์ใน Adobe Photoshop หรือดาวน์โหลดตัวอย่างฟรีจากอินเทอร์เน็ต  

พร้อมหรือยัง? ดีมาก! มาเริ่มนำเข้าแพ็กเกจที่จำเป็นและเขียนโค้ดกัน

## Import Packages
เพื่อเริ่มต้น ให้เพิ่มการนำเข้า Aspose.PSD ที่จำเป็นลงในไฟล์ Java ของคุณ:

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

การนำเข้าเหล่านี้จะให้คุณเข้าถึงฟังก์ชันที่ใช้จัดการไฟล์ PSD, ตั้งค่าโหมดสี, และส่งออกผลลัพธ์เป็น PNG

## Step 1: Define Your Directories
ตั้งค่าโฟลเดอร์ต้นทางและโฟลเดอร์ผลลัพธ์ ซึ่งบอกโปรแกรมว่าจะอ่านไฟล์ PSD ต้นฉบับจากที่ไหนและเขียนไฟล์ที่แปลงแล้วไปที่ไหน

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

แทนที่สตริงตัวอย่างด้วยพาธที่แท้จริงบนเครื่องของคุณ

## Step 2: Create a Method to Handle Image Processing
เราจะห่อหุ้มตรรกะการแปลงไว้ในเมธอดที่สามารถนำกลับมาใช้ใหม่ได้ เมธอดนี้รับพารามิเตอร์ต่าง ๆ ที่คุณอาจต้องการปรับ เช่น โหมดสี, ความลึกบิต, และการบีบอัด

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

เมธอดนี้ทำให้คุณ **ตั้งค่าโหมดสีของ PSD** แล้ว **ส่งออก PSD เป็น PNG** ได้ในขั้นตอนเดียว

## Step 3: Define File Paths and Load the PSD
ภายในเมธอด ให้สร้างพาธไฟล์เต็มรูปแบบและโหลดไฟล์ PSD Grayscale 16‑bit ดั้งเดิม:

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix` ช่วยให้คุณติดตามการตั้งค่าที่ใช้สำหรับแต่ละไฟล์ที่ส่งออกได้ง่ายขึ้น

## Step 4: Process the Layer or Full Image
ต่อไปเราจะวาดบนเลเยอร์เฉพาะหรือบนภาพทั้งหมด ในตัวอย่างนี้เราจะเพิ่มกรอบสีเทาอ่อนเพื่อทำให้ผลลัพธ์มองเห็นได้ชัดเจนขึ้น

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

สี่เหลี่ยมจะคำนวณแบบไดนามิกเพื่อให้อยู่กึ่งกลางไม่ว่าขนาดภาพจะเป็นเท่าใด

## Step 5: Save the Modified PSD File
หลังจากวาดเสร็จ เราจะบันทึกไฟล์ PSD ด้วยโหมดสีและความลึกบิตที่คุณระบุ นี่คือขั้นตอนสำคัญของ **การตั้งค่าโหมดสีของ PSD** ก่อนการแปลง

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## Step 6: Convert the PSD to PNG
สุดท้าย เราจะโหลด PSD ที่บันทึกใหม่และส่งออกเป็น PNG โดยใช้ `PngColorType.GrayscaleWithAlpha` เพื่อรักษาความลึก 16‑bit ไว้ในไฟล์ PNG

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

ตอนนี้คุณได้ **แปลง PSD เป็น PNG** พร้อมคงข้อมูล Grayscale 16‑bit คุณภาพสูงเรียบร้อยแล้ว

## Common Issues and Solutions
| Issue | Why It Happens | Fix |
|-------|----------------|-----|
| **ข้อยกเว้น “Unsupported color type”** | พยายามบันทึก PSD ที่มีการกำหนดช่องสีที่ไม่รองรับ | ตรวจสอบให้ `channelBitsCount` ตรงกับความลึกบิตจริง (16) และ `channelsCount` ถูกต้องสำหรับ Grayscale (1) |
| **ไฟล์ไม่พบ** | พาธโฟลเดอร์ต้นทางไม่ถูกต้อง | ตรวจสอบสตริง `sourceDir` อีกครั้งและยืนยันว่าไฟล์ PSD มีอยู่จริง |
| **PNG ที่ส่งออกเป็นสีดำ** | PNG ถูกบันทึกโดยไม่ได้จัดการช่อง Alpha | ใช้ `PngColorType.GrayscaleWithAlpha` ตามที่แสดงข้างต้น |

## Frequently Asked Questions

**Q: โหมดสี Grayscale 16-bit คืออะไร?**  
A: ให้สีเทา 65 536 ระดับ ซึ่งให้รายละเอียดโทนที่มากกว่ามาตรฐาน 8‑bit (256 ระดับ) อย่างมาก

**Q: สามารถใช้ Aspose.PSD กับภาพที่ไม่ใช่ Grayscale ได้หรือไม่?**  
A: แน่นอน! Aspose.PSD รองรับ RGB, CMYK, Lab และโหมดสีอื่น ๆ อีกหลายแบบ

**Q: มีเวอร์ชันทดลองของ Aspose.PSD หรือไม่?**  
A: มี คุณสามารถลองใช้เวอร์ชันทดลองฟรีของ Aspose.PSD ได้ เพียงไปที่ [หน้าดาวน์โหลดของ Aspose](https://releases.aspose.com/)  

**Q: จะหา ตัวอย่างเพิ่มเติมของการใช้ Aspose.PSD ได้จากที่ไหน?**  
A: คุณสามารถตรวจสอบ [เอกสารประกอบ](https://reference.aspose.com/psd/java/) เพื่อดูตัวอย่างและบทเรียนเชิงลึกเพิ่มเติม

**Q: จะซื้อไลเซนส์สำหรับ Aspose.PSD อย่างไร?**  
A: คุณสามารถซื้อไลเซนส์ได้โดยไปที่ [หน้าแผนการซื้อของ Aspose](https://purchase.aspose.com/buy)

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}