---
date: 2026-02-17
description: เรียนรู้วิธีสร้างไฟล์ PSD ที่มีการเติมลวดลายและเรนเดอร์เลเยอร์การเติมลวดลายใน
  PSD ด้วย Java และ Aspose.PSD ในบทแนะนำเชิงขั้นตอนที่ครบถ้วนนี้
linktitle: Render Pattern Fill Layer in PSD Files using Java
second_title: Aspose.PSD Java API
title: วิธีสร้างไฟล์ PSD เติมลวดลายโดยใช้ Java
url: /th/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีสร้างไฟล์ pattern fill psd ด้วย Java

## Introduction
หากคุณกำลังมองหา **สร้างไฟล์ pattern fill psd** อย่างอัตโนมัติ คุณมาถูกที่แล้ว ด้วย Aspose.PSD for Java คุณสามารถทำงานอัตโนมัติในการสร้าง, ปรับเปลี่ยน, และเรนเดอร์เลเยอร์ pattern fill ภายในเอกสาร Photoshop, ช่วยประหยัดเวลามนุษย์เป็นจำนวนมาก ในบทแนะนำนี้เราจะเดินผ่านการโหลด PSD, ค้นหาเลเยอร์ fill, ตั้งค่าลวดลาย, และสุดท้ายบันทึกไฟล์ที่อัปเดต เมื่อเสร็จคุณจะสามารถใช้ Java เพื่อ **สร้างไฟล์ pattern fill psd** ที่สามารถนำกลับมาใช้ใหม่ในโครงการหรือรวมเข้าไปใน pipeline อัตโนมัติได้อย่างมั่นใจ

## Quick Answers
- **ไลบรารีที่ต้องการคืออะไร?** Aspose.PSD for Java  
- **ฉันสามารถรันบนระบบปฏิบัติการใดก็ได้หรือไม่?** ใช่, แพลตฟอร์มใดก็ได้ที่รองรับ Java 8+  
- **ฉันต้องการไลเซนส์สำหรับการทดสอบหรือไม่?** การทดลองใช้งานฟรีเพียงพอสำหรับการพัฒนา  
- **ใช้เวลานานเท่าไหร่ในการทำงานนี้?** ประมาณ 10‑15 นาทีสำหรับตัวอย่างพื้นฐาน  
- **โค้ดนี้เข้ากันได้กับ Maven/Gradle หรือไม่?** แน่นอน – เพียงเพิ่ม dependency ของ Aspose.PSD  

## What is “create pattern fill psd”?
การสร้างไฟล์ PSD แบบ pattern fill หมายถึงการกำหนดลวดลายสีแบบต่อเนื่องโดยอัตโนมัติและนำไปใช้กับเลเยอร์ fill ภายในไฟล์ Photoshop เทคนิคนี้มีประโยชน์เมื่อคุณต้องการเทกซ์เจอร์ที่ทำซ้ำได้, องค์ประกอบแบรนด์, หรือกราฟิกไดนามิกที่สร้างขึ้นแบบเรียลไทม์

## Why use Aspose.PSD to create pattern fill psd?
- **Full automation** – ไม่ต้องทำขั้นตอนใน Photoshop ด้วยตนเอง  
- **Cross‑platform** – ทำงานบน Windows, macOS, และ Linux  
- **No Photoshop installation** – ไลบรารีจัดการโครงสร้าง PSD ภายในโดยอัตโนมัติ  
- **Rich API** – เข้าถึงคุณสมบัติของเลเยอร์, การตั้งค่า fill, และตัวเลือกการส่งออก  

## Prerequisites
ก่อนที่เราจะเริ่ม, มีสิ่งที่คุณต้องเตรียมเพื่อให้สามารถทำตามได้อย่างราบรื่น:
1. **Java Development Kit (JDK):** ตรวจสอบว่าคุณได้ติดตั้ง JDK บนเครื่องของคุณแล้ว คุณสามารถดาวน์โหลดได้จาก [Oracle’s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)  
2. **Aspose.PSD for Java:** เพื่อจัดการไฟล์ PSD คุณจะต้องใช้ไลบรารี Aspose.PSD คุณสามารถดาวน์โหลดได้จาก [Aspose releases page](https://releases.aspose.com/psd/java/)  
3. **Integrated Development Environment (IDE):** IDE อย่าง IntelliJ IDEA, Eclipse หรือ NetBeans จะทำให้การเขียนโค้ดง่ายขึ้น เลือกตามที่คุณชอบ!  
4. **Basic Java Knowledge:** ความคุ้นเคยกับไวยากรณ์ Java จะช่วยให้คุณทำตามบทแนะนำนี้ได้อย่างมีประสิทธิภาพ  
5. **Sample PSD File:** มีไฟล์ PSD พร้อมสำหรับการทดสอบ คุณสามารถสร้างไฟล์ด้วย Photoshop หรือดาวน์โหลดไฟล์ตัวอย่างจากเว็บ  

เมื่อคุณเตรียมสิ่งเหล่านี้ครบแล้ว, คุณก็พร้อมที่จะลงมือโค้ดกันแล้ว!

## Import Packages
เพื่อเริ่มต้นกับ Aspose.PSD for Java คุณต้องนำเข้าแพคเกจที่จำเป็น ด้านล่างเป็นวิธีตั้งค่าในโปรเจกต์ Java ของคุณ:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IPatternFillSettings;
import com.aspose.psd.imageoptions.PsdOptions;
import java.util.UUID;
```
การนำเข้าต่าง ๆ นี้ทำให้คุณสามารถทำงานกับภาพ PSD, เข้าถึงเลเยอร์, และจัดการคุณลักษณะต่าง ๆ ของเลเยอร์ fill ได้  
ต่อไปเราจะลงลึกในขั้นตอนแบบทีละขั้นเพื่อ **render pattern** fill layers ในไฟล์ PSD ของคุณ

## How to create pattern fill psd with Aspose.PSD
ต่อไปนี้เป็นคู่มือเชิงปฏิบัติที่พาคุณผ่านแต่ละขั้นตอนที่จำเป็น คุณสามารถคัดลอกโค้ดส่วนนั้นไปวางใน IDE ของคุณและรันกับไฟล์ PSD ตัวอย่างของคุณได้

### Step 1: Define Your Source and Output Directories
เพื่อเริ่มต้นคุณต้องกำหนดตำแหน่งที่ไฟล์ PSD ต้นฉบับของคุณอยู่และตำแหน่งที่ต้องการบันทึกไฟล์ผลลัพธ์  
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String sourceFile = sourceDir + "sample.psd";
String outputFile = outputDir + "sample_out.psd";
```
แทนที่ `"Your Source Directory"` และ `"Your Document Directory"` ด้วยพาธจริงบนเครื่องของคุณ

### Step 2: Load the PSD File
ต่อไปคุณจะโหลดไฟล์ PSD เข้าไปในอินสแตนซ์ของคลาส `PsdImage` ขั้นตอนนี้เปิดไฟล์ PSD ของคุณเพื่อการปรับเปลี่ยน  
```java
PsdImage image = (PsdImage) Image.load(sourceFile);
```
การแคสต์ภาพที่โหลดเป็น `PsdImage` จะทำให้คุณเข้าถึงคุณสมบัติและเมธอดเฉพาะของ PSD ได้

### Step 3: Loop Through Layers
เพื่อค้นหาและจัดการกับเลเยอร์ fill คุณต้องวนลูปผ่านทุกเลเยอร์ในภาพ PSD ที่โหลดมา  
```java
try {
    for (Layer layer : image.getLayers()) {
        if (layer instanceof FillLayer) {
            FillLayer fillLayer = (FillLayer)layer;
            // Additional code will go here.
        }
    }
}
```
การตรวจสอบ `instanceof` ทำให้เราทำงานเฉพาะกับออบเจ็กต์ `FillLayer` เท่านั้น

### Step 4: Configure Fill Layer Settings
เมื่อคุณระบุเลเยอร์ fill แล้ว ขั้นตอนต่อไปคือการปรับตั้งค่าต่าง ๆ ของมัน ที่นี่คุณสามารถปรับ offset, scale, และรายละเอียดของลวดลายได้  
```java
IPatternFillSettings settings = (IPatternFillSettings) fillLayer.getFillSettings();
settings.setHorizontalOffset(-5);
settings.setVerticalOffset(12);
settings.setScale(300);
settings.setLinked(true);
```
แต่ละคุณสมบัติมีผลต่อการเรนเดอร์ลวดลาย ตัวอย่างเช่น การปรับ offset จะทำให้ลวดลายเลื่อนตำแหน่งสัมพันธ์กับเลเยอร์

### Step 5: Define Pattern Data
ต่อไปเป็นการกำหนดลวดลายจริงโดยระบุสีที่ประกอบเป็น pattern fill ของคุณ  
```java
settings.setPatternData(new int[]{
    Color.getBlack().toArgb(), 
    Color.getRed().toArgb(),
    Color.getGreen().toArgb(), 
    Color.getBlue().toArgb(),
    Color.getWhite().toArgb(), 
    Color.getAliceBlue().toArgb(),
    Color.getViolet().toArgb(), 
    Color.getChocolate().toArgb(),
    Color.getIndianRed().toArgb(), 
    Color.getDarkOliveGreen().toArgb(),
    Color.getCadetBlue().toArgb(), 
    Color.getYellowGreen().toArgb(),
    Color.getBlack().toArgb(), 
    Color.getAzure().toArgb(),
    Color.getForestGreen().toArgb(), 
    Color.getSienna().toArgb(),
});
```
คุณสามารถเปลี่ยนสีใดก็ได้ตามต้องการเพื่อสร้างสไตล์ที่เป็นเอกลักษณ์ของคุณ

### Step 6: Set Pattern Dimensions and Name
การปรับแต่งเพิ่มเติมของเลเยอร์ fill เกี่ยวข้องกับการกำหนดความกว้างและความสูงของลวดลาย รวมถึงการตั้งชื่อและ ID ที่ไม่ซ้ำกัน  
```java
settings.setPatternHeight(4);
settings.setPatternWidth(4);
settings.setPatternName("$$$/Presets/Patterns/ColorfulSquare=Colorful Square New\0");
settings.setPatternId(UUID.randomUUID() + "\0");
```
ขนาดจะควบคุมขนาดของ tile ของลวดลาย ส่วนชื่อและ ID จะช่วยให้คุณระบุ pattern ได้ในภายหลัง

### Step 7: Update the Fill Layer
หลังจากตั้งค่าทุกอย่างแล้ว คุณต้องอัปเดตเลเยอร์ด้วยการเปลี่ยนแปลงที่ทำไว้  
```java
fillLayer.update();
```
การเรียก `update()` จะทำให้การแก้ไขทั้งหมดถูกนำไปใช้กับโครงสร้าง PSD ด้านล่าง

### Step 8: Save the Changes
สุดท้ายบันทึกไฟล์ PSD ที่อัปเดตโดยใช้เมธอด `save()` ขั้นตอนนี้จะเขียนการเปลี่ยนแปลงทั้งหมดกลับไปยังเอกสาร  
```java
image.save(outputFile, new PsdOptions(image));
```
ไฟล์ใหม่ของคุณตอนนี้มีเลเยอร์ pattern fill ที่กำหนดเองแล้ว

### Step 9: Dispose of the Image Object
เพื่อปลดปล่อยทรัพยากร ควรทำการ dispose ออบเจ็กต์ภาพเมื่อใช้งานเสร็จแล้ว  
```java
finally {
    image.dispose();
}
```
การ dispose จะทำให้หน่วยความจำถูกคืนค่าอย่างรวดเร็ว โดยเฉพาะเมื่อประมวลผลไฟล์ PSD ขนาดใหญ่

## Common Use Cases
- **Automated branding** – สร้าง pattern fill ที่สอดคล้องกับแบรนด์สำหรับสื่อการตลาด  
- **Dynamic textures** – สร้างเทกซ์เจอร์เชิงกระบวนการสำหรับเกมหรือการจำลองโดยไม่ต้องออกแบบด้วยมือ  
- **Batch processing** – ใช้ pattern fill มาตรฐานกับไฟล์ PSD จำนวนหลายร้อยไฟล์ในครั้งเดียว  

## Common Issues and Solutions
- **Pattern not visible after saving** – ตรวจสอบว่าเลเยอร์ที่แก้ไขไม่ได้ถูกซ่อน (`layer.setVisible(true)`) และขนาดของ pattern ตรงกับขนาด tile ที่คาดหวัง  
- **`ClassCastException`** – ตรวจสอบให้แน่ใจว่าคุณทำการแคสต์เป็น `FillLayer` หลังจากยืนยันว่าเป็น `instanceof FillLayer` แล้วเท่านั้น  
- **File path errors** – ใช้พาธแบบ absolute หรือ escape backslash สองครั้งบน Windows (`C:\\\\Images\\\\sample.psd`)  

## Frequently Asked Questions

**Q: Aspose.PSD for Java คืออะไร?**  
**A:** Aspose.PSD for Java เป็นไลบรารีที่ช่วยให้ผู้พัฒนาสามารถทำงานกับไฟล์ Photoshop PSD ได้โดยอัตโนมัติ

**Q: ฉันสามารถลอง Aspose.PSD ฟรีได้หรือไม่?**  
**A:** ใช่, คุณสามารถเข้าถึง [free trial](https://releases.aspose.com/) เพื่อสำรวจฟังก์ชันต่าง ๆ

**Q: ฉันสามารถซื้อ Aspose.PSD ได้จากที่ไหน?**  
**A:** คุณสามารถซื้อไลเซนส์ได้จาก [Aspose purchase page](https://purchase.aspose.com/buy)

**Q: มีการสนับสนุนสำหรับ Aspose.PSD หรือไม่?**  
**A:** แน่นอน! คุณสามารถขอความช่วยเหลือจาก [Aspose support forum](https://forum.aspose.com/c/psd/34)

**Q: ควรทำอย่างไรหากพบปัญหาเมื่อใช้ Aspose.PSD?**  
**A:** ตรวจสอบเอกสารสำหรับเคล็ดลับการแก้ไขปัญหา หรือขอความช่วยเหลือใน [support forum](https://forum.aspose.com/c/psd/34)

**Additional Q&A**

**Q: ฉันสามารถใช้โค้ดนี้เพื่อสร้างหลายเลเยอร์ pattern fill ใน PSD ไฟล์เดียวได้หรือไม่?**  
**A:** ได้. เพียงทำซ้ำลูปสำหรับแต่ละ `FillLayer` ที่ต้องการปรับแต่งและตั้งค่าตามต้องการ

**Q: ไลบรารีรองรับไฟล์ PSD ที่มี layer effects หรือไม่?**  
**A:** Aspose.PSD จะคง layer effects ส่วนใหญ่ไว้, แต่การเติม pattern จะใช้ได้เฉพาะกับออบเจ็กต์ `FillLayer` เท่านั้น

**Q: มีวิธีอ่าน pattern ที่มีอยู่ใน PSD แล้วนำกลับมาใช้ใหม่หรือไม่?**  
**A:** คุณสามารถดึง `IPatternFillSettings` ปัจจุบันจาก `FillLayer` แล้วทำการ clone คุณสมบัติก่อนนำไปแก้ไขต่อ

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.PSD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}