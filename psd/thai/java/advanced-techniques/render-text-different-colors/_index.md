---
date: 2025-12-22
description: เรียนรู้วิธีบันทึกไฟล์ PSD เป็น PNG ด้วยสีข้อความที่แตกต่างโดยใช้ Aspose.PSD
  สำหรับ Java. ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนของเราเพื่อส่งออก PSD เป็น PNG และเรนเดอร์ข้อความ.
linktitle: Render Text with Different Colors in Text Layer
second_title: Aspose.PSD Java API
title: บันทึกไฟล์ PSD เป็น PNG พร้อมข้อความสีโดยใช้ Aspose.PSD สำหรับ Java
url: /th/java/advanced-techniques/render-text-different-colors/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึกไฟล์ PSD เป็น PNG พร้อมข้อความสีโดยใช้ Aspose.PSD for Java

## บทนำ

ยินดีต้อนรับสู่คู่มือขั้นตอนโดยละเอียด **วิธีบันทึกไฟล์ PSD เป็น PNG** พร้อมการกำหนดสีต่าง ๆ ให้กับข้อความในเลเยอร์ข้อความโดยใช้ Aspose.PSD for Java  Aspose.PSD เป็นไลบรารี Java ที่ทรงพลัง ช่วยให้คุณจัดการไฟล์ Photoshop ผ่านโปรแกรมได้อย่างอัตโนมัติ พร้อมการควบคุมเต็มรูปแบบของรูปแบบ PSD และ PSB

## คำตอบสั้น
- **บทเรียนนี้ครอบคลุมอะไร?** การเรนเดอร์ข้อความสีและการบันทึก PSD เป็นภาพ PNG  
- **ต้องใช้ไลบรารีใด?** Aspose.PSD for Java  
- **ต้องมีลิขสิทธิ์หรือไม่?** สามารถใช้รุ่นทดลองฟรีสำหรับการพัฒนา; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **สามารถเปลี่ยนรูปแบบผลลัพธ์ได้หรือไม่?** ได้, คุณสามารถส่งออก PSD ไปเป็น PNG หรือรูปแบบที่รองรับอื่น ๆ  
- **โค้ดนี้เข้ากันได้กับ Java 8+ หรือไม่?** แน่นอน, ตัวอย่างทำงานบน Java 8 และรุ่นใหม่กว่า

## **save PSD as PNG** คืออะไร?
การบันทึก PSD เป็น PNG หมายถึงการแปลงไฟล์ Photoshop ที่มีเลเยอร์หลายชั้นให้เป็นภาพเรสเตอร์แบบแบนที่คงความโปร่งใสและความแม่นยำของสีไว้ ซึ่งเหมาะสำหรับการใช้งานบนเว็บหรือเมื่อต้องการแชร์ผลลัพธ์ภาพโดยไม่เปิดเผยเลเยอร์ต้นฉบับ

## ทำไมต้องใช้ Aspose.PSD เพื่อ **export PSD to PNG**?
- **ไม่ต้องติดตั้ง Photoshop** – ไลบรารีจัดการการแยกวิเคราะห์ PSD ภายในเอง  
- **คงสไตล์ข้อความ** – สามารถแก้ไขฟอนต์, สีและเอฟเฟกต์ก่อนการส่งออกได้  
- **ประสิทธิภาพสูง** – ปรับให้ทำงานได้ดีกับไฟล์ขนาดใหญ่และการประมวลผลเป็นชุด  

## ข้อกำหนดเบื้องต้น

- ความรู้พื้นฐานด้านการเขียนโปรแกรม Java  
- ติดตั้งไลบรารี Aspose.PSD for Java คุณสามารถดาวน์โหลดได้จาก [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)

## นำเข้าแพ็กเกจ

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## วิธี **Save PSD as PNG** พร้อมข้อความสี

### ขั้นตอนที่ 1: ตั้งค่าโปรเจกต์ของคุณ
สร้างโปรเจกต์ Java ใหม่และเพิ่มไฟล์ JAR ของ Aspose.PSD ลงใน classpath ตรวจสอบให้แน่ใจว่าแอปพลิเคชันมีสิทธิ์อ่าน/เขียนในโฟลเดอร์ที่คุณจะใช้

### ขั้นตอนที่ 2: กำหนดโฟลเดอร์ต้นทางและโฟลเดอร์ผลลัพธ์
ปรับเปลี่ยนพาธให้ชี้ไปยังไฟล์ PSD ของคุณและโฟลเดอร์ที่ต้องการบันทึกไฟล์ PNG

```java
String sourceDir = "Your Document Directory";
String outputDir = "Your Document Directory";
```

### ขั้นตอนที่ 3: โหลดไฟล์ PSD และเข้าถึงเลเยอร์ข้อความ
เราจะโหลดไฟล์ PSD ที่ต้องการ, ค้นหาเลเยอร์ข้อความ, และรีเฟรชข้อมูลของเลเยอร์เพื่อให้การเปลี่ยนสีมีผล

```java
String targetFilePath = sourceDir + "text_ethalon_different_colors.psd";
String resultFilePath = outputDir + "RenderTextWithDifferentColorsInTextLayer_out.png";

PsdImage psdImage = null;
try
{
    psdImage = (PsdImage) Image.load(targetFilePath);
    TextLayer txtLayer = (TextLayer)psdImage.getLayers()[1];
    txtLayer.getTextData().updateLayerData();
```

### ขั้นตอนที่ 4: ตั้งค่า PNG Options และ **Export PSD to PNG**
กำหนดค่า PNG ให้คงความลึกสีเต็มและช่องอัลฟา, จากนั้นบันทึกภาพ

```java
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
    psdImage.save(resultFilePath, pngOptions);
}
finally
{
    if (psdImage != null) psdImage.dispose();
}
```

## ข้อผิดพลาดทั่วไป & เคล็ดลับ
- **ดัชนีเลเยอร์:** ตรวจสอบให้แน่ใจว่าคุณอ้างอิงดัชนีเลเยอร์ที่ถูกต้อง (`[1]` ในตัวอย่าง) การจัดลำดับเลเยอร์อาจแตกต่างกันระหว่างไฟล์  
- **การอัปเดตสี:** ต้องเรียก `updateLayerData()` หลังจากแก้ไขคุณสมบัติของข้อความ; หากไม่ทำการเปลี่ยนแปลงจะไม่แสดงใน PNG ที่ส่งออก  
- **การจัดการหน่วยความจำ:** ปิดวัตถุ `PsdImage` ในบล็อก `finally` เพื่อปล่อยทรัพยากรเนทีฟ

## สรุป

ขอแสดงความยินดี! ตอนนี้คุณรู้ **วิธีบันทึกไฟล์ PSD เป็น PNG** พร้อมการเรนเดอร์ข้อความหลายสีโดยใช้ Aspose.PSD for Java เทคนิคนี้เปิดประตูสู่การสร้างภาพอัตโนมัติ, การประมวลผลเป็นชุด, และการสร้างกราฟิกไดนามิกโดยไม่ต้องเปิด Photoshop

## คำถามที่พบบ่อย

### Q1: สามารถใช้ Aspose.PSD for Java กับภาษาโปรแกรมอื่นได้หรือไม่?
A1: Aspose.PSD ถูกออกแบบมาสำหรับ Java เป็นหลัก, แต่ Aspose มีไลบรารีที่คล้ายกันสำหรับหลายภาษาโปรแกรม

### Q2: มีรุ่นทดลองสำหรับ Aspose.PSD for Java หรือไม่?
A2: มี, คุณสามารถดาวน์โหลดรุ่นทดลองฟรีได้จาก [Aspose.PSD](https://releases.aspose.com/)

### Q3: จะหาแหล่งสนับสนุนหรือความช่วยเหลือเพิ่มเติมได้จากที่ไหน?
A3: เยี่ยมชม [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) เพื่อรับการสนับสนุนจากชุมชนและการสนทนา

### Q4: จะขอรับลิขสิทธิ์ชั่วคราวสำหรับ Aspose.PSD for Java ได้อย่างไร?
A4: คุณสามารถขอรับลิขสิทธิ์ชั่วคราวได้จาก [Aspose.PSD](https://purchase.aspose.com/temporary-license/)

### Q5: มีบทเรียนอื่น ๆ สำหรับ Aspose.PSD หรือไม่?
A5: มี, สำรวจ [Aspose.PSD documentation](https://reference.aspose.com/psd/java/) เพื่อดูบทเรียนและตัวอย่างเพิ่มเติม

---

**Last Updated:** 2025-12-22  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}