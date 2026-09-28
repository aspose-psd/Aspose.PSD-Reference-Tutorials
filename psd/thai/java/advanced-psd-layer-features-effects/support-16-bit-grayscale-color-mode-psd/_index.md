---
date: 2026-09-28
description: เรียนรู้วิธีส่งออก PSD เป็น PNG พร้อมตั้งค่าโหมดสีของ PSD เป็น 16‑bit
  grayscale ด้วย Aspose.PSD for Java คู่มือแบบขั้นตอนพร้อมตัวอย่างโค้ด
keywords:
- export psd as png
- how to convert psd to png
- 16-bit grayscale java
lastmod: 2026-09-28
linktitle: ส่งออก PSD เป็น PNG – 16‑bit Grayscale – Java
og_description: ส่งออก PSD เป็น PNG ด้วย 16‑bit grayscale โดยใช้ Aspose.PSD for Java
  ปฏิบัติตามบทแนะนำขั้นตอนเพื่อรักษาเฉดสีเทา 65,536 เฉด
og_image_alt: Guide showing how to export PSD as PNG with 16-bit grayscale using Aspose.PSD
  Java
og_title: ส่งออก PSD เป็น PNG พร้อม 16‑bit grayscale ใน Java – คู่มือ Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  headline: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  type: TechArticle
- description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  name: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
    text: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
  - name: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
    text: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
  - name: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
    text: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
  type: HowTo
- questions:
  - answer: It provides 65 536 shades of gray, delivering far more tonal detail than
      the standard 8‑bit (256 shades).
    question: What is 16‑bit grayscale color mode?
  - answer: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other
      color modes.
    question: Can I use Aspose.PSD for non‑grayscale images?
  - answer: Yes, you can try a free trial version of Aspose.PSD. Just head to the
      [Aspose download page](https://releases.aspose.com/).
    question: Is there a trial version of Aspose.PSD?
  - answer: Check the official [documentation](https://reference.aspose.com/psd/java/)
      for in‑depth tutorials, API references, and sample projects.
    question: Where can I find more Aspose.PSD examples?
  - answer: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
title: วิธีส่งออก PSD เป็น PNG พร้อมโหมดสีเทา 16‑bit ใน Java
url: /th/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก PSD เป็น PNG ด้วยโหมดสีเทา 16‑บิตใน Java

## บทนำ
การส่งออก PSD เป็น PNG พร้อมคงโหมดสีเทา 16‑บิตให้ความลึกของภาพถ่ายระดับมืออาชีพและความเข้ากันได้ทั่วโลกของ PNG ในคู่มือนี้คุณจะได้เรียนรู้วิธี **ตั้งค่าโหมดสีของ PSD เป็นสีเทา 16‑บิต** และจากนั้น **ส่งออก PSD เป็น PNG** ด้วย Aspose.PSD สำหรับ Java การสอนครอบคลุมตั้งแต่ข้อกำหนดเบื้องต้นจนถึงการแก้ไขปัญหา เพื่อให้คุณสามารถผสานกระบวนการทำงานนี้เข้าไปในไพป์ไลน์ภาพที่ใช้ Java ได้ทุกประเภท

## คำตอบอย่างรวดเร็ว
- **อะไรคือการ “ส่งออก PSD เป็น PNG”?** โหลด PSD, ปรับเปลี่ยนโหมดสีตามต้องการ, แล้วบันทึกเป็นไฟล์ PNG.  
- **คลาส Aspose ใดที่จัดการการแปลง?** `PsdImage` โหลด PSD และ `PngOptions` กำหนดการตั้งค่าเอาต์พุตของ PNG.  
- **ต้องการไลเซนส์สำหรับการใช้งานจริงหรือไม่?** ใช่ – เวอร์ชันทดลองใช้ได้สำหรับการทดสอบ แต่ต้องมีไลเซนส์แบบชำระเงินสำหรับการใช้งานเชิงพาณิชย์.  
- **สามารถคงความลึก 16‑บิตใน PNG ได้หรือไม่?** แน่นอน โดยใช้ `PngColorType.GrayscaleWithAlpha`.  
- **IDE ที่รองรับมีอะไรบ้าง?** IDE ของ Java ใดก็ได้ – IntelliJ IDEA, Eclipse, VS Code หรือ NetBeans.

## การส่งออก PSD เป็น PNG คืออะไร?
การส่งออก PSD เป็น PNG คือกระบวนการแปลงเอกสาร Adobe Photoshop (PSD) ให้เป็นไฟล์ Portable Network Graphics (PNG) พร้อมคงข้อมูลพิกเซลและความลึกของสีของภาพ การแปลงนี้มักใช้เพื่อแชร์ทรัพยากรสีเทาคุณภาพสูงบนเว็บโดยไม่สูญเสียรายละเอียดโทนสี

## ทำไมต้องส่งออก PSD เป็น PNG ด้วยสีเทา 16‑บิต?
การส่งออกเป็น PNG พร้อมคงสีเทา 16‑บิตจะรักษาเฉดสีเทา 65 536 เฉด ซึ่งให้ความอุดมสมบูรณ์ของโทนสีมากกว่าภาพ 8‑บิต PNG ที่รองรับทั่วโลกทำให้ไฟล์สามารถแสดงผลในเบราว์เซอร์, แอปมือถือ, และโปรแกรมแก้ไขบนเดสก์ท็อปโดยไม่มีการสูญเสีย ในขณะเดียวกันการบีบอัดแบบไม่มีการสูญเสียของ Aspose.PSD รับประกันว่าจะไม่มีอาร์ติแฟคท์เกิดขึ้น

## ข้อกำหนดเบื้องต้น
1. **Java Development Kit (JDK)** – ติดตั้ง JDK รุ่นล่าสุดจาก [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – ดาวน์โหลดไฟล์ JAR จาก [Aspose download page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse หรือ Visual Studio Code ทำงานได้อย่างสมบูรณ์.  
4. **ความรู้พื้นฐาน Java** – คุณควรคุ้นเคยกับการสร้างคลาส, การจัดการข้อยกเว้น, และการทำงานกับเส้นทางไฟล์.  
5. **ไฟล์ PSD ตัวอย่าง** – สร้างไฟล์ใน Adobe Photoshop หรือดาวน์โหลดตัวอย่างฟรีจากออนไลน์.

## วิธีการส่งออก PSD เป็น PNG ทีละขั้นตอน

## วิธีตั้งค่าโหมดสีของ PSD เป็นสีเทา 16‑บิต?
`PsdImage` เป็นคลาสของ Aspose.PSD ที่โหลดและแสดงไฟล์ PSD ในหน่วยความจำ.  
`ColorMode` เป็น enumeration ที่กำหนดโหมดสีของภาพ PSD.  

โหลด PSD ด้วย `PsdImage`, เปลี่ยนโหมดสีโดยใช้คุณสมบัติ `ColorMode`, แล้วบันทึกไฟล์ที่แก้ไข การดำเนินการนี้ทำทั้งหมดในหน่วยความจำ ลดความจำเป็นของไฟล์กลางและทำให้การแปลงเร็วและมีประสิทธิภาพ.

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

การนำเข้าต่อไปนี้ให้คุณเข้าถึงฟังก์ชันที่ใช้ในการจัดการไฟล์ PSD, ตั้งค่าโหมดสี, และส่งออกผลลัพธ์เป็น PNG.

## วิธีกำหนดไดเรกทอรีต้นทางและปลายทาง?
`File` เป็นคลาสใน java.io ที่แสดงเส้นทางไฟล์หรือไดเรกทอรีบนระบบไฟล์.  

คุณต้องบอกโปรแกรมว่าจะอ่าน PSD ต้นฉบับจากที่ไหนและจะเขียน PNG ที่แปลงแล้วไปที่ไหน การใช้เส้นทางแบบ absolute หรือ relative ทำงานได้ แต่ควรคงความสอดคล้องกันในทุกสภาพแวดล้อมเพื่อหลีกเลี่ยงข้อผิดพลาดการแก้ไขเส้นทาง.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

แทนที่สตริงตัวแทนด้วยเส้นทางจริงบนเครื่องของคุณ.

## วิธีบรรจุตรรกะการแปลงในเมธอดที่ใช้ซ้ำได้?
`convertPsdToPng` เป็นเมธอดที่กำหนดเองซึ่งบรรจุขั้นตอนทั้งหมดที่จำเป็นในการแปลงไฟล์ PSD เป็น PNG พร้อมการตั้งค่าแบบเลือก.  

การสร้างเมธอดเฉพาะทำให้คุณสามารถใช้ขั้นตอนการแปลงเดียวกันซ้ำสำหรับหลายไฟล์หรือการตั้งค่าต่าง ๆ ส่งพารามิเตอร์เช่นเส้นทางต้นทาง, โฟลเดอร์ปลายทาง, และระดับการบีบอัดแบบเลือก ทำให้กระบวนการทำงานยืดหยุ่นและบำรุงรักษาได้ง่าย.

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

เมธอดนี้ทำให้คุณ **ตั้งค่าโหมดสีของ PSD** แล้ว **ส่งออก PSD เป็น PNG** ในขั้นตอนเดียว.

## วิธีโหลด PSD และใช้โหมดสีเทา 16‑บิต?
`PsdImage` เป็นคลาสของ Aspose.PSD ที่โหลดไฟล์ PSD เข้าหน่วยความจำ.  
`ColorMode.GRAYSCALE_16` เป็นค่าของ enumeration ที่ตั้งค่าภาพเป็นสีเทา 16‑บิต.  
`channelBitsCount` เป็นคุณสมบัติที่ระบุจำนวนบิตต่อช่อง.  

ภายในเมธอดแปลง, สร้างเส้นทางไฟล์เต็ม, สร้างอินสแตนซ์ `PsdImage`, และเปลี่ยน `ColorMode` เป็น `ColorMode.GRAYSCALE_16`. คุณสมบัติ `channelBitsCount` ต้องตั้งค่าเป็น 16 เพื่อคงความลึกบิตสูง, ทำให้ภาพรักษาข้อมูลโทนทั้งหมด.

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix` ช่วยให้คุณติดตามการตั้งค่าที่ใช้สำหรับแต่ละไฟล์ที่ส่งออก.

## วิธีวาดขอบบางบนภาพ (ขั้นตอนเลือก)?
`Graphics` เป็นคลาสที่ให้ความสามารถในการวาดบนแคนวาส `PsdImage`.  

คุณสามารถวาดสี่เหลี่ยมสีเทารอบภาพได้ตามต้องการเพื่อทำให้ผลลัพธ์มองเห็นได้ชัดขึ้นในระหว่างการทดสอบ ขั้นตอนนี้แสดงวิธีทำงานกับเลเยอร์และอ็อบเจ็กต์กราฟิก, และสี่เหลี่ยมจะคำนวณแบบไดนามิกเพื่อให้อยู่กึ่งกลางโดยไม่คำนึงถึงขนาดภาพ.

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

สี่เหลี่ยมจะคำนวณแบบไดนามิกเพื่อให้อยู่กึ่งกลางโดยไม่คำนึงถึงขนาดภาพ.

## วิธีบันทึก PSD ที่แก้ไขแล้วพร้อมโหมดสีใหม่?
`PsdOptions` เป็นคลาสที่ควบคุมวิธีการบันทึกไฟล์ PSD, รวมถึงการตั้งค่าโหมดสีและความลึกบิต.  

หลังจากวาด (หรือข้ามขั้นตอนนั้น) ให้เรียก `save` บนอินสแตนซ์ `PsdImage`, ส่งอ็อบเจ็กต์ `PsdOptions` ที่คงการกำหนดค่าสีเทา 16‑บิตไว้ การทำเช่นนี้ทำให้ PSD ที่บันทึกคงโหมดสีที่ต้องการโดยไม่มีการสูญเสียข้อมูล.

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

## วิธีแปลง PSD เป็น PNG พร้อมคงความลึก 16‑บิต?
`PngOptions` เป็นคลาสที่กำหนดการตั้งค่าเอาต์พุตของ PNG เช่น ประเภทสีและระดับการบีบอัด.  
`PngColorType.GrayscaleWithAlpha` เป็นค่าของ enumeration ที่เก็บข้อมูลสีเทา 16‑บิตพร้อมแชนแนลอัลฟา.  

โหลด PSD ที่บันทึกใหม่, ตั้งค่า `PngOptions` ด้วย `PngColorType.GrayscaleWithAlpha`, แล้วเรียก `save`. วิธีนี้ทำให้ข้อมูลสีเทา 16‑บิตคงอยู่ในไฟล์ PNG, ให้ภาพที่ไม่มีการสูญเสียคุณภาพสูง, เหมาะสำหรับการประมวลผลหรือแจกจ่ายต่อไป.

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

ตอนนี้คุณได้ **ส่งออก PSD เป็น PNG** อย่างสำเร็จพร้อมคงข้อมูลสีเทา 16‑บิตคุณภาพสูง.

## ปัญหาทั่วไปและวิธีแก้
| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|----------|
| **“Unsupported color type” exception** | พยายามบันทึก PSD ที่มีการกำหนดค่าช่องที่ไม่รองรับ. | ตรวจสอบให้ `channelBitsCount` ตรงกับความลึกบิตจริง (16) และ `channelsCount` ถูกต้องสำหรับสีเทา (1). |
| **File not found** | เส้นทางไดเรกทอรีต้นทางไม่ถูกต้อง. | ตรวจสอบสตริง `sourceDir` อีกครั้งและยืนยันว่าไฟล์ PSD มีอยู่ในตำแหน่งนั้น. |
| **Output PNG appears black** | PNG ถูกบันทึกโดยไม่มีการจัดการอัลฟาที่เหมาะสม. | ใช้ `PngColorType.GrayscaleWithAlpha` ตามที่แสดงข้างต้น. |
| **Memory overflow on large PSDs** | โหลดไฟล์ทั้งหมดเข้าในหน่วยความจำ. | เปิดโหมดสตรีมมิงโดยใช้ `PsdImage.load(inputStream, new LoadOptions())` เพื่อประมวลผลไฟล์ขนาดใหญ่อย่างมีประสิทธิภาพ. |

## คำถามที่พบบ่อย

**Q: โหมดสีเทา 16‑บิตคืออะไร?**  
A: มันให้ 65 536 เฉดสีเทา, ให้รายละเอียดโทนสีมากกว่ามาตรฐาน 8‑บิต (256 เฉด).

**Q: ฉันสามารถใช้ Aspose.PSD กับภาพที่ไม่ใช่สีเทาได้หรือไม่?**  
A: แน่นอน! Aspose.PSD รองรับ RGB, CMYK, Lab, Indexed และโหมดสีอื่น ๆ มากมาย.

**Q: มีเวอร์ชันทดลองของ Aspose.PSD หรือไม่?**  
A: ใช่, คุณสามารถทดลองใช้เวอร์ชันฟรีของ Aspose.PSD ได้ เพียงไปที่ [Aspose download page](https://releases.aspose.com/).

**Q: ฉันจะหา ตัวอย่าง Aspose.PSD เพิ่มเติมได้จากที่ไหน?**  
A: คุณสามารถดูตัวอย่างเพิ่มเติมของ Aspose.PSD ได้ที่ [documentation](https://reference.aspose.com/psd/java/) อย่างเป็นทางการเพื่อเรียนรู้เชิงลึก, อ้างอิง API, และโครงการตัวอย่าง.

**Q: ฉันจะซื้อไลเซนส์สำหรับ Aspose.PSD อย่างไร?**  
A: คุณสามารถซื้อไลเซนส์ได้โดยไปที่ [Aspose purchase page](https://purchase.aspose.com/buy).

**อัปเดตล่าสุด:** 2026-09-28  
**ทดสอบด้วย:** Aspose.PSD for Java 24.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [แปลง PSD เป็น PNG ด้วยความลึกบิตที่กำหนดโดยใช้ Aspose.PSD for Java](/psd/java/optimizing-png-files/specify-png-bit-depth/)
- [ส่งออก PSD เป็น PNG พร้อมเอฟเฟกต์เลเยอร์โดยใช้ Aspose.PSD for Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [บันทึก PSD เป็น JPEG และสนับสนุนสี RGB ด้วย Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}