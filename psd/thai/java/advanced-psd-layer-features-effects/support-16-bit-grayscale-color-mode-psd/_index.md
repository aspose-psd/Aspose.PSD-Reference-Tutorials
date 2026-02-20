---
date: 2026-02-20
description: เรียนรู้วิธีแปลงไฟล์ PSD เป็น PNG พร้อมตั้งค่าโหมดสีของ PSD เป็นระดับสีเทา
  16‑บิตโดยใช้ Aspose.PSD for Java คู่มือขั้นตอนโดยละเอียดพร้อมตัวอย่างโค้ด
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: วิธีแปลง PSD เป็น PNG ด้วยโหมดสีเทา 16‑บิตใน Java
url: /th/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง PSD เป็น PNG ด้วยโหมดสี Grayscale 16‑bit ใน Java

## Introduction
เมื่อคุณเริ่มต้นสำรวจโลกของการออกแบบกราฟิกและการจัดการภาพ การรู้ **how to convert PSD to PNG** เปรียบเสมือนอาวุธลับ การใช้โหมด Grayscale 16‑bit จะเพิ่มความลึกและความอุดมของโทนสี ทำให้ภาพของคุณโดดเด่นขึ้น ในบทเรียนนี้เราจะอธิบายวิธี **set PSD color mode** เป็น Grayscale 16‑bit แล้ว **export PSD as PNG** ด้วย Aspose.PSD for Java พร้อมหรือยังที่จะยกระดับกระบวนการทำงานกับภาพของคุณ? เริ่มกันเลย

## Quick Answers
- **What does “convert PSD to PNG” involve?** การโหลดไฟล์ PSD, ปรับโหมดสีตามต้องการ, แล้วบันทึกเป็นไฟล์ PNG.  
- **Which Aspose class handles the conversion?** `PsdImage` สำหรับการโหลดและ `PngOptions` สำหรับการบันทึก.  
- **Do I need a special license?** สามารถใช้รุ่นทดลองเพื่อทดสอบ; ต้องมีไลเซนส์แบบชำระเงินสำหรับการใช้งานจริง.  
- **Can I keep the 16‑bit depth in PNG?** ได้, โดยใช้ `PpngColorType.GrayscaleWithAlpha`.  
- **What IDEs are supported?** IDE ของ Java ใดก็ได้ – IntelliJ IDEA, Eclipse, VS Code เป็นต้น.

## Why Convert PSD to PNG with 16‑bit Grayscale?
* **Preserve tonal detail:** Grayscale 16‑bit เก็บเฉดสีเทาได้ 65 536 ระดับ, มากกว่าภาพ 8‑bit ที่มี 256 ระดับ.  
* **Broad compatibility:** PNG รองรับอย่างกว้างขวางบนเว็บ, แอปมือถือ, และเครื่องมือเดสก์ท็อป, พร้อมคงคุณภาพสูง.  
* **Lossless workflow:** การแปลงด้วย Aspose.PSD จะไม่มีการบีบอัดที่ทำให้เกิดศิลปะบิดเบือน, เหมาะสำหรับการเก็บรักษาหรือการประมวลผลต่อไป.

## Prerequisites
ก่อนเริ่ม, ให้ตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมใช้งานเพื่อให้ได้ผลลัพธ์ที่ดีที่สุดจากบทเรียนนี้:

1. **Java Development Kit (JDK)** – ตรวจสอบว่าคุณติดตั้งเวอร์ชันล่าสุดแล้ว. คุณสามารถดาวน์โหลดได้จาก [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java Library** – เป็นเครื่องมือที่ทำให้เราสามารถจัดการไฟล์ PSD ได้. ดาวน์โหลดจาก [Aspose download page](https://releases.aspose.com/psd/java/).  
3. **An IDE** – IntelliJ IDEA, Eclipse, หรือ Visual Studio Code จะทำงานได้ดี.  
4. **Basic Java knowledge** – ความคุ้นเคยกับไวยากรณ์ Java จะช่วยให้ขั้นตอนเป็นไปอย่างราบรื่น.  
5. **A sample PSD file** – สร้างไฟล์ใน Adobe Photoshop หรือดาวน์โหลดตัวอย่างฟรีออนไลน์.

พร้อมหรือยัง? ดีมาก! มาเริ่มนำเข้าแพ็กเกจที่จำเป็นและเขียนโค้ดกันเถอะ.

## Import Packages
เพื่อเริ่มต้น, เพิ่มการนำเข้า Aspose.PSD ที่จำเป็นลงในไฟล์ Java ของคุณ:

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

การนำเข้าเหล่านี้จะทำให้คุณเข้าถึงฟังก์ชันที่ใช้จัดการไฟล์ PSD, ตั้งค่าโหมดสี, และส่งออกผลลัพธ์เป็น PNG.

## Step 1: Define Your Directories
ตั้งค่าโฟลเดอร์ต้นทางและโฟลเดอร์ผลลัพธ์. นี้บอกโปรแกรมว่าจะอ่าน PSD ต้นฉบับจากที่ไหนและเขียนไฟล์ที่แปลงแล้วไปที่ไหน.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

แทนที่สตริงตัวอย่างด้วยพาธจริงบนเครื่องของคุณ.

## Step 2: Create a Method to Handle Image Processing
เราจะห่อหุ้มตรรกะการแปลงไว้ในเมธอดที่สามารถนำกลับมาใช้ใหม่ได้. เมธอดนี้รับพารามิเตอร์ต่าง ๆ ที่คุณอาจต้องปรับ, เช่น โหมดสี, ความลึกบิต, และการบีบอัด.

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

เมธอดนี้ทำให้คุณ **set PSD color mode** แล้ว **export PSD as PNG** ในขั้นตอนเดียว.

## Step 3: Define File Paths and Load the PSD
ภายในเมธอด, สร้างพาธไฟล์เต็มและโหลด PSD Grayscale 16‑bit ต้นฉบับ:

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix` ช่วยให้คุณติดตามการตั้งค่าที่ใช้สำหรับแต่ละไฟล์ที่ส่งออกได้ง่ายขึ้น.

## Step 4: Process the Layer or Full Image
ต่อไปเราจะวาดบนเลเยอร์เฉพาะหรือบนภาพทั้งหมด. ในตัวอย่างนี้เราจะเพิ่มกรอบสีเทาอ่อนเพื่อทำให้ผลลัพธ์มองเห็นได้ชัดเจนขึ้น.

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

สี่เหลี่ยมจะคำนวณแบบไดนามิกเพื่อให้คงอยู่กึ่งกลางไม่ว่าขนาดภาพจะเป็นเท่าใด.

## Step 5: Save the Modified PSD File
หลังจากวาดเสร็จ, เราบันทึก PSD ด้วยโหมดสีและความลึกบิตที่คุณกำหนดไว้. นี้เป็นหัวใจของ **setting PSD color mode** ก่อนการแปลง.

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
สุดท้าย, เราโหลด PSD ที่บันทึกใหม่และส่งออกเป็น PNG. ด้วยการใช้ `PngColorType.GrayscaleWithAlpha` เราจะคงความลึก 16‑bit ไว้ในไฟล์ PNG.

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

ตอนนี้คุณได้ **converted PSD to PNG** อย่างสำเร็จพร้อมข้อมูล Grayscale 16‑bit คุณภาพสูงแล้ว.

## Common Issues and Solutions
| Issue | Why It Happens | Fix |
|-------|----------------|-----|
| **“Unsupported color type” exception** | พยายามบันทึก PSD ที่มีการกำหนดช่องสีที่ไม่รองรับ. | ตรวจสอบให้ `channelBitsCount` ตรงกับความลึกบิตจริง (16) และ `channelsCount` ถูกต้องสำหรับ Grayscale (1). |
| **File not found** | พาธโฟลเดอร์ต้นทางไม่ถูกต้อง. | ตรวจสอบสตริง `sourceDir` อีกครั้งและยืนยันว่าไฟล์ PSD มีอยู่. |
| **Output PNG appears black** | PNG ถูกบันทึกโดยไม่ได้จัดการช่อง Alpha. | ใช้ `PngColorType.GrayscaleWithAlpha` ตามที่แสดงด้านบน. |

## Frequently Asked Questions

**Q: What is 16-bit grayscale color mode?**  
A: มันให้ 65 536 เฉดสีเทา, ให้รายละเอียดโทนสีมากกว่ามาตรฐาน 8‑bit (256 เฉด) อย่างมาก.

**Q: Can I use Aspose.PSD for non‑grayscale images?**  
A: แน่นอน! Aspose.PSD รองรับ RGB, CMYK, Lab, และโหมดสีอื่น ๆ อีกหลายแบบ.

**Q: Is there a trial version of Aspose.PSD?**  
A: มี, คุณสามารถลองใช้รุ่นทดลองฟรีของ Aspose.PSD ได้โดยไปที่ [Aspose download page](https://releases.aspose.com/).

**Q: Where can I find more examples of using Aspose.PSD?**  
A: คุณสามารถดูที่ [documentation](https://reference.aspose.com/psd/java/) เพื่อรับตัวอย่างและบทเรียนเชิงลึกเพิ่มเติม.

**Q: How do I purchase a license for Aspose.PSD?**  
A: คุณสามารถซื้อไลเซนส์ได้โดยเยี่ยมชม [Aspose purchase page](https://purchase.aspose.com/buy).

---

**Last Updated:** 2026-02-20  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}