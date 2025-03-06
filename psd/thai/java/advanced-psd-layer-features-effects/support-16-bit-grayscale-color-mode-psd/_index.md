---
title: รองรับโหมดสีโทนสีเทา 16 บิตใน PSD - Java
linktitle: รองรับโหมดสีโทนสีเทา 16 บิตใน PSD - Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีใช้งานโหมดสีระดับสีเทา 16 บิตในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java พร้อมบทช่วยสอนแบบละเอียดทีละขั้นตอนนี้
weight: 11
url: /th/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# รองรับโหมดสีโทนสีเทา 16 บิตใน PSD - Java

## การแนะนำ
เมื่อคุณดำดิ่งสู่โลกแห่งการออกแบบกราฟิกและการปรับแต่งภาพ การทำความเข้าใจวิธีการทำงานในโหมดสีต่างๆ ก็เหมือนกับการมีอาวุธลับ โดยเฉพาะอย่างยิ่ง ระดับสีเทา 16 บิตสามารถเป็นตัวเปลี่ยนเกมได้ ทำให้ภาพของคุณมีความลึกและรายละเอียดที่น่าทึ่งจนทำให้ภาพดูโดดเด่นอย่างแท้จริง คุณพร้อมที่จะสำรวจคุณสมบัติอันทรงพลังนี้โดยใช้ Aspose.PSD สำหรับ Java แล้วหรือยัง? หากคุณมีอุปกรณ์การเขียนโค้ดพร้อมแล้ว มาเริ่มกันเลย
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณได้จัดเตรียมทุกอย่างไว้แล้วเพื่อให้ได้ประโยชน์สูงสุดจากบทช่วยสอนนี้ นี่คือสิ่งที่คุณต้องการ:
1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK เวอร์ชันล่าสุดแล้ว คุณสามารถดาวน์โหลดได้จาก[เว็บไซต์ของออราเคิล](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD สำหรับ Java Library: นี่คือสิ่งที่เราจะใช้เพื่อจัดการไฟล์ PSD คุณสามารถสัมผัสมันได้จาก[กำหนดหน้าดาวน์โหลด](https://releases.aspose.com/psd/java/).
3. สภาพแวดล้อมการพัฒนาแบบรวม (IDE): IDE ใด ๆ ที่รองรับ Java จะทำ ตัวเลือกยอดนิยม ได้แก่ IntelliJ IDEA, Eclipse หรือแม้แต่ Visual Studio Code
4. ความรู้พื้นฐานของ Java: ความคุ้นเคยกับการเขียนโปรแกรม Java จะช่วยให้คุณปฏิบัติตามได้อย่างราบรื่นอย่างแน่นอน
5. ไฟล์ PSD ตัวอย่าง: ตรวจสอบให้แน่ใจว่าคุณมีไฟล์ PSD ที่คุณต้องการใช้งาน หากคุณยังไม่มี คุณสามารถสร้าง PSD ง่ายๆ โดยใช้ซอฟต์แวร์ เช่น Adobe Photoshop หรือค้นหาไฟล์ตัวอย่างทางออนไลน์
พร้อม? ยอดเยี่ยม! มานำเข้าแพ็คเกจที่จำเป็นและเริ่มเขียนโค้ดกันดีกว่า
## แพ็คเกจนำเข้า
ในการเริ่มต้น เรามานำเข้าแพ็คเกจที่เกี่ยวข้องซึ่งเราจะต้องทำงานร่วมกับ Aspose.PSD สำหรับ Java กัน เพิ่มบรรทัดต่อไปนี้ลงในไฟล์ Java ของคุณ:
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
การนำเข้าเหล่านี้ทำให้คุณสามารถเข้าถึงฟังก์ชันที่คุณจะใช้เพื่อจัดการไฟล์ PSD สร้างกราฟิก และบันทึกรูปภาพในรูปแบบต่างๆ
## ขั้นตอนที่ 1: กำหนดไดเรกทอรีของคุณ
สิ่งแรกสุดที่คุณต้องทำคือตั้งค่าไดเร็กทอรีต้นทางและเอาต์พุตของคุณ นี่คือที่ที่ไฟล์ PSD ของคุณจะถูกโหลดและบันทึกไว้ ต่อไปนี้คือวิธีที่คุณสามารถทำได้:
```java
String sourceDir = "Your Source Directory"; // เปลี่ยนเป็นไดเร็กทอรีต้นทางของคุณ
String outputDir = "Your Document Directory"; // เปลี่ยนเป็นไดเร็กทอรีเอาต์พุตของคุณ
```
ตรวจสอบให้แน่ใจว่าได้แทนที่ “Your Source Directory” และ “Your Document Directory” ด้วยเส้นทางจริงบนคอมพิวเตอร์ของคุณซึ่งมีไฟล์ PSD ของคุณอยู่ และตำแหน่งที่คุณต้องการบันทึกไฟล์ที่ประมวลผล
## ขั้นตอนที่ 2: สร้างวิธีการจัดการกับการประมวลผลภาพ
ตอนนี้เราจะสร้างวิธีจัดการการประมวลผลไฟล์ PSD วิธีการนี้จะใช้ชุดพารามิเตอร์เพื่อระบุลักษณะของไฟล์ PSD และกระบวนการระดับสีเทา
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
วิธีนี้ทำให้คุณสามารถระบุชื่อไฟล์ โหมดสี จำนวนบิต จำนวนช่อง วิธีการบีบอัด และหมายเลขเลเยอร์ เราจะแจกแจงการทำงานของวิธีนี้ทีละขั้นตอน!
## ขั้นตอนที่ 3: กำหนดเส้นทางของไฟล์และโหลด PSD
ภายในวิธีการของคุณ เรามากำหนดวิธีสร้างเส้นทางของไฟล์และโหลดอิมเมจ PSD กัน:
```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// โหลด PSD ระดับสีเทา 16 บิตที่กำหนดไว้ล่วงหน้า
PsdImage image = (PsdImage)Image.load(filePath);
```
ที่นี่ เราสร้างเส้นทางที่จำเป็นสำหรับไฟล์ PSD ที่เราจะใช้งาน ตลอดจนเตรียมการบันทึกไฟล์ PSD และ PNG ที่แก้ไขแล้ว
## ขั้นตอนที่ 4: ประมวลผลเลเยอร์หรือรูปภาพเต็ม
ถัดไป คุณจะต้องวาดบนเลเยอร์ที่เลือกหรือทั้งรูปภาพ โดยเพิ่มเส้นขอบสีเทารอบๆ นี่เป็นวิธีที่ยอดเยี่ยมในการเพิ่มการมองเห็นและเพิ่มความเก๋ไก๋ให้กับภาพ
```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // วาดขอบด้านในสีเทารอบปริมณฑลของเลเยอร์
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
ในส่วนนี้ คุณกำลังใช้คลาส Graphics จาก Aspose เพื่อสร้างบริบทการวาด ขนาดของสี่เหลี่ยมจะคำนวณตามขนาดภาพของคุณ เพื่อให้แน่ใจว่าจะวาดตรงกลางได้พอดี
## ขั้นตอนที่ 5: บันทึกไฟล์ PSD ที่แก้ไข
เมื่อคุณวาดเสร็จแล้ว ก็ถึงเวลาบันทึกการแก้ไขของคุณเป็นไฟล์ PSD ใหม่ นี่คือที่ที่คุณตั้งค่าตัวเลือกที่คุณระบุไว้ก่อนหน้านี้
```java
    // บันทึกสำเนา PSD ที่มีลักษณะเฉพาะ
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```
ด้วยการตั้งค่าตัวเลือกสำหรับ PSD คุณสามารถควบคุมการทำงานของรูปภาพของคุณเมื่อบันทึกได้ ช่วยให้มั่นใจได้ว่ารายละเอียดที่พิถีพิถันทั้งหมดจะถูกเก็บรักษาไว้
## ขั้นตอนที่ 6: แปลง PSD เป็น PNG
ไอซิ่งบนเค้กจะเกิดขึ้นเมื่อคุณแปลง PSD ที่บันทึกไว้ใหม่เป็นรูปแบบ PNG ซึ่งออกแบบมาเป็นพิเศษสำหรับระดับสีเทาด้วยอัลฟ่า
```java
finally {
    image.dispose();
}
// โหลด PSD ที่บันทึกไว้
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // แปลง PSD ที่บันทึกไว้เป็นภาพ PNG ระดับสีเทา
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // ที่นี่ไม่ควรมีข้อยกเว้น
}
finally {
    image1.dispose();
}
```
กระบวนการแปลงนั้นตรงไปตรงมาและทำให้แน่ใจว่ารูปภาพของคุณพร้อมที่จะใช้ในแอปพลิเคชันต่างๆ หรือแชร์ทางออนไลน์
## บทสรุป
และคุณก็เข้าใจแล้ว—คำแนะนำโดยละเอียดเกี่ยวกับวิธีรองรับโหมดสีระดับสีเทา 16 บิตในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java! คุณได้เรียนรู้วิธีตั้งค่าสภาพแวดล้อม ประมวลผลรูปภาพ และแม้แต่ส่งออกเป็นรูปแบบต่างๆ ไม่น่าแปลกใจเลยที่โค้ดเพียงไม่กี่บรรทัดสามารถนำไปสู่ผลลัพธ์ที่สวยงามเช่นนี้ได้
ด้วยความสามารถในการปรับแต่งภาพเช่นนี้ ใครจะรู้เกี่ยวกับการผจญภัยที่คุณสามารถเริ่มต้นได้? ไม่ว่าจะเป็นการปรับปรุงการออกแบบที่มีอยู่หรือการสร้างผลงานชิ้นเอกใหม่ทั้งหมด จินตนาการของคุณมีขีดจำกัด!

## คำถามที่พบบ่อย
### โหมดสีโทนสีเทา 16 บิตคืออะไร
ระดับสีเทา 16 บิตช่วยให้มีช่วงเฉดสีที่ครอบคลุมมากขึ้นเมื่อเทียบกับมาตรฐาน 8 บิต ส่งผลให้ได้ภาพที่มีรายละเอียดมากขึ้น
### ฉันสามารถใช้ Aspose.PSD สำหรับรูปภาพที่ไม่ใช่ระดับสีเทาได้หรือไม่
อย่างแน่นอน! Aspose.PSD รองรับโหมดสีต่างๆ ดังนั้นคุณจึงสามารถทำงานกับ RGB, CMYK และอื่นๆ ได้เช่นกัน
### มี Aspose.PSD เวอร์ชันทดลองใช้หรือไม่
 ได้ คุณสามารถทดลองใช้ Aspose.PSD เวอร์ชันทดลองใช้ฟรีได้ เพียงมุ่งหน้าไปที่[กำหนดหน้าดาวน์โหลด](https://releases.aspose.com/).
### ฉันจะหาตัวอย่างเพิ่มเติมของการใช้ Aspose.PSD ได้ที่ไหน
 คุณสามารถตรวจสอบได้ที่[เอกสารประกอบ](https://reference.aspose.com/psd/java/) สำหรับตัวอย่างและบทช่วยสอนเชิงลึกเพิ่มเติม
### ฉันจะซื้อใบอนุญาตสำหรับ Aspose.PSD ได้อย่างไร
 คุณสามารถซื้อใบอนุญาตได้โดยไปที่[กำหนดหน้าการซื้อ](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
