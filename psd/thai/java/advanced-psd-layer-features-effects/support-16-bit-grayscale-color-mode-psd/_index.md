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

## การแนะนำ
อย่าลืมเริ่มต้นสำรวจโลกของการออกแบบกราฟิกและการจัดการภาพการรู้ **วิธีแปลง PSD เป็น PNG** เปรียบเสมือนการควบคุมระบบ โหมดสีเทา 16 บิต ให้เห็นและอุดมของโทนสีนี้รูปภาพของคุณโดดเด่นขึ้นในบทเรียนนี้เราจะอธิบายวิธี **ตั้งค่าโหมดสี PSD** ระดับสีเทา 16 บิตแล้ว **ส่งออก PSD เป็น PNG** ด้วย Aspose.PSD สำหรับ Java พร้อมหรือยังที่จะยกระดับระบบให้กับภาพของคุณ? เริ่มกันเลย

## คำตอบด่วน
- **“แปลง PSD เป็น PNG” เกี่ยวข้องกับอะไรบ้าง** โปรดดูไฟล์ PSD, โหมดสีตามต้องการ, จากนั้นบันทึกเป็นไฟล์ PNG
- **คลาส Aspose ใดที่จัดการการแปลง** `PsdImage` สำหรับการศึกษาและ `PngOptions` สำหรับการวิจัย
- **ฉันจำเป็นต้องมีใบอนุญาตพิเศษหรือไม่** ตัวอย่างการทดลองเพื่อทดสอบ; ต้องมีเซนส์การชำระเงินแบบสมจริง
- **ฉันสามารถเก็บความลึก 16 บิตเป็น PNG ได้หรือไม่** สามารถทำได้ `PpngColorType.GrayscaleWithAlpha`
- **รองรับ IDE ใดบ้าง?** IDE ของ Java ลอนดอน – IntelliJ IDEA, Eclipse, VSCode เป็นต้น

## เหตุใดจึงแปลง PSD เป็น PNG ด้วยระดับสีเทา 16 บิต
* **รักษารายละเอียดโทนสี:** ระดับสีเทา 16 บิต เก็บเฉดสีเทาได้ 65536 ระดับ, ความละเอียดสูงภาพ 8 บิตได้ 256 ระดับ
* **ความเข้ากันได้แบบกว้าง:** PNG สามารถดูได้จากข้อมูลมือถือ, และเครื่องมือวิเคราะห์, ดูคงแหล่งที่มา
* **ขั้นตอนการทำงานแบบ Lossless:** การตัดสินใจด้วย Aspose.PSD ไม่ต้องทำอะไรที่ศิลปะการประกอบ, มื้ออาหารหรือฮาร์ดแวร์ต่อไป

## ข้อกำหนดเบื้องต้น
การเริ่มต้น, ทำให้คุณสามารถควบคุมและใช้งานได้เพื่อให้ได้ผลลัพธ์ที่ดีที่สุดจากบทเรียนนี้:

1. **Java Development Kit (JDK)** – ตรวจสอบการติดตั้งล่าสุดแล้ว ดาวน์โหลดได้จาก [เว็บไซต์ของ Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
2. **Aspose.PSD สำหรับ Java Library** – สิ่งสำคัญที่ทำให้ไฟล์ PSD ได้ ดาวน์โหลดจาก [หน้าดาวน์โหลด Aspose](https://releases.aspose.com/psd/java/)
3. **An IDE** – IntelliJ IDEA, Eclipse, หรือ Visual Studio Code จะนุ่มนวล
4. **ความรู้ Java พื้นฐาน** – คุณสมบัติของ Java ช่วยในการขั้นตอนการตรวจสอบ
5. **ไฟล์ PSD ตัวอย่าง** – สร้างไฟล์ใน Adobe Photoshop หรือดาวน์โหลดตัวอย่างฟรีออนไลน์

หรือยัง? ดีมาก! มาเริ่มนำเข้าโปรแกรมและเขียนโค้ดกันเถอะ

## แพคเกจนำเข้า
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

## ขั้นตอนที่ 1: กำหนดไดเร็กทอรีของคุณ
ตั้งค่าโฟลเดอร์ต้นทางและโฟลเดอร์ผลลัพธ์. นี้บอกโปรแกรมว่าจะอ่าน PSD ต้นฉบับจากที่ไหนและเขียนไฟล์ที่แปลงแล้วไปที่ไหน.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

แทนที่สตริงตัวอย่างด้วยพาธจริงบนเครื่องของคุณ.

## ขั้นตอนที่ 2: สร้างเมธอดสำหรับประมวลผลภาพ
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

## ขั้นตอนที่ 3: กำหนดเส้นทางไฟล์และโหลดไฟล์ PSD
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

## ขั้นตอนที่ 4: ประมวลผลเลเยอร์หรือภาพทั้งหมด
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

## ขั้นตอนที่ 5: บันทึกไฟล์ PSD ที่แก้ไขแล้ว
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

## ขั้นตอนที่ 6: แปลงไฟล์ PSD เป็น PNG
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

## ปัญหาทั่วไปและแนวทางแก้ไข
| ปัญหา | ทำไมมันถึงเกิดขึ้น | แก้ไข |
|----------------------|----------------|-----|
| **ข้อยกเว้น “ประเภทสีที่ไม่รองรับ”** | บันทึกเรื่องราว PSD ของช่องสีที่ไม่รองรับ | การตัดภาพให้ `channelBitsCount` ไม่จำเป็นต้องเก็บข้อมูลจริง (16) และ `channelsCount` ถูกต้องสำหรับ Grayscale (1) |
| **ไม่พบไฟล์** | ปธธต้นทางกับ. | หากต้องการตัด `sourceDir` อีกครั้งและยังมีไฟล์ PSD ที่มีอยู่ |
| **เอาต์พุต PNG ปรากฏเป็นสีดำ** | PNG บันทึกโดยไม่ได้จัดการช่อง Alpha. | ใช้ `PngColorType.GrayscaleWithAlpha` แสดงให้เห็นด้านบน |

## คำถามที่พบบ่อย

**ถาม: โหมดสีโทนสีเทา 16 บิตคืออะไร**
A: มันให้ 65536 เฉดสีเทา, ให้รายละเอียดโทนสีมากกว่ามาตรฐาน 8-บิต (256 เฉด) เฉดสี.

**ถาม: ฉันสามารถใช้ Aspose.PSD สำหรับรูปภาพที่ไม่ใช่ระดับสีเทาได้หรือไม่**
ตอบ: แน่นอน! Aspose.PSD รองรับ RGB, CMYK, Lab, และโหมดสีอื่นๆ ในรูปแบบอื่นๆ

**ถาม: Aspose.PSD มีเวอร์ชันทดลองใช้งานหรือไม่**
ตอบ: มี ลองทดลองรุ่นทดลองฟรีของ Aspose.PSD ไปที่ [หน้าดาวน์โหลด Aspose](https://releases.aspose.com/)

**ถาม: ฉันจะหาตัวอย่างเพิ่มเติมของการใช้ Aspose.PSD ได้ที่ไหน**
ตอบ: โปรดดูที่ [documentation](https://reference.aspose.com/psd/java/) เพื่อรับตัวอย่างและบทเรียนเชิงลึกเพิ่มเติม

**ถาม: ฉันจะซื้อใบอนุญาตสำหรับ Aspose.PSD ได้อย่างไร**
ตอบ: บางครั้งมันก็เหมือนกับที่นี่เลย [Aspose buy page](https://purchase.aspose.com/buy)

---

**อัปเดตล่าสุด:** 2026-02-20
**ทดสอบด้วย:** Aspose.PSD สำหรับ Java 24.12 (เวอร์ชันล่าสุด ณ เวลาที่เขียน)
**ผู้เขียน:** Aspose 

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}