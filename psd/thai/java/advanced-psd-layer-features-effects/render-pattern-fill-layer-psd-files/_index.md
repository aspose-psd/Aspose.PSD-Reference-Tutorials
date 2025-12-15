---
date: 2025-12-14
description: เรียนรู้วิธีการเรนเดอร์เลเยอร์เติมลวดลายในไฟล์ PSD ด้วย Java และ Aspose.PSD
  ในบทเรียนเชิงขั้นตอนที่ครอบคลุมนี้
linktitle: Render Pattern Fill Layer in PSD Files using Java
second_title: Aspose.PSD Java API
title: วิธีเรนเดอร์เลเยอร์เติมลายแบบในไฟล์ PSD ด้วย Java
url: /th/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีการเรนเดอร์เลเยอร์เติมลวดลายในไฟล์ PSD ด้วย Java

## Introduction
หากคุณกำลังมองหา **วิธีการเรนเดอร์ลวดลาย** ของเลเยอร์เติมในเอกสาร Photoshop อย่างอัตโนมัติ คุณมาถูกที่แล้ว ด้วย Aspose.PSD for Java คุณสามารถทำงานอัตโนมัติในการสร้างและจัดการไฟล์ PSD ได้ ช่วยประหยัดเวลามนุษย์จำนวนมาก ในบทแนะนำนี้เราจะพาคุณผ่านขั้นตอนการโหลด PSD, ค้นหาเลเยอร์เติม, ตั้งค่าลวดลาย, และสุดท้ายบันทึกไฟล์ที่อัปเดตแล้ว เมื่อจบคุณจะสามารถใช้ Java เพื่อ **เรนเดอร์ลวดลาย** และแม้กระทั่ง **สร้างไฟล์ PSD เติมลวดลาย** ที่สามารถนำกลับมาใช้ใหม่ในโครงการต่าง ๆ ได้อย่างมั่นใจ

## Quick Answers
- **ไลบรารีที่ต้องการคืออะไร?** Aspose.PSD for Java  
- **ฉันสามารถรันนี้บนระบบปฏิบัติการใดก็ได้หรือไม่?** ได้, ทุกแพลตฟอร์มที่รองรับ Java 8+  
- **ฉันต้องการลิขสิทธิ์สำหรับการทดสอบหรือไม่?** การทดลองใช้ฟรีเพียงพอสำหรับการพัฒนา  
- **การทำงานนี้ใช้เวลานานเท่าไหร่?** ประมาณ 10‑15 นาทีสำหรับตัวอย่างพื้นฐาน  
- **โค้ดนี้เข้ากันได้กับ Maven/Gradle หรือไม่?** แน่นอน – เพียงเพิ่ม dependency ของ Aspose.PSD  

## Prerequisites
ก่อนที่เราจะเริ่ม, มีสิ่งที่คุณต้องเตรียมพร้อมเพื่อให้การทำตามขั้นตอนเป็นไปอย่างราบรื่น:
1. **Java Development Kit (JDK):** ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนเครื่องของคุณแล้ว คุณสามารถดาวน์โหลดได้จาก [Oracle’s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)  
2. **Aspose.PSD for Java:** เพื่อจัดการไฟล์ PSD คุณจะต้องใช้ไลบรารี Aspose.PSD คุณสามารถดาวน์โหลดได้จาก [Aspose releases page](https://releases.aspose.com/psd/java/)  
3. **Integrated Development Environment (IDE):** IDE เช่น IntelliJ IDEA, Eclipse หรือ NetBeans จะทำให้การเขียนโค้ดง่ายขึ้น เลือกใช้ตามที่คุณถนัด!  
4. **Basic Java Knowledge:** ความคุ้นเคยกับไวยากรณ์ของ Java จะช่วยให้คุณทำตามบทแนะนำนี้ได้อย่างมีประสิทธิภาพ  
5. **Sample PSD File:** เตรียมไฟล์ PSD ที่พร้อมสำหรับการทดสอบ คุณสามารถสร้างไฟล์ด้วย Photoshopตัวอย่างจากอินเทอร์เน็ต  

เมื่อคุณมีทุกอย่างพร้อมแล้ว, คุณก็พร้อมที่จะลงมือโค้ดกันแล้ว!

## Import Packages
เพื่อเริ่มต้นใช้งาน Aspose.PSD for Java คุณต้องนำเข้าแพ็กเกจที่จำเป็น ด้านล่างเป็นวิธีตั้งค่าในโปรเจกต์ Java ของคุณ:
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
การนำเข้าเหล่านี้จะทำให้คุณสามารถทำงานกับภาพ PSD, เข้าถึงเลเยอร์, และจัดการคุณลักษณะต่าง ๆ ของเลเยอร์เติมได้  
ต่อไปเราจะลงลึกในขั้นตอนการ **เรนเดอร์ลวดลาย** ของเลเยอร์เติมในไฟล์ PSD ของคุณ

## How to create pattern fill PSD with Aspose.PSD
ต่อไปนี้เป็นคำแนะนำเชิงปฏิบัติที่พาคุณผ่านแต่ละขั้นตอนที่จำเป็น คุณสามารถคัดลอกโค้ดส่วนนี้ไปวางใน IDE ของคุณและรันกับไฟล์ PSD ตัวอย่างของคุณได้เลย

### Step 1: Define Your Source and Output Directories
เพื่อเริ่มต้น คุณต้องกำหนดตำแหน่งที่เก็บไฟล์ PSD ต้นฉบับและที่ต้องการบันทึกไฟล์ผลลัพธ์  
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String sourceFile = sourceDir + "sample.psd";
String outputFile = outputDir + "sample_out.psd";
```
เปลี่ยน `"Your Source Directory"` และ `"Your Document Directory"` ให้เป็นพาธจริงบนเครื่องของคุณ

### Step 2: Load the PSD File
ต่อไปคุณจะโหลดไฟล์ PSD เข้าไปในอ็อบเจ็กต์ของคลาส `PsdImage` ขั้นตอนนี้คือการเปิดไฟล์ PSD เพื่อทำการแก้ไขต่อไป  
```java
PsdImage image = (PsdImage) Image.load(sourceFile);
```
การแคสต์ภาพที่โหลดเป็น `PsdImage` จะทำให้คุณเข้าถึงคุณสมบัติและเมธอดเฉพาะของ PSD ได้

### Step 3: Loop Through Layers
เพื่อค้นหาและจัดการกับเลเยอร์เติม คุณต้องวนลูปผ่านทุกเลเยอร์ในภาพ PSD ที่โหลดมา  
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
การตรวจสอบ `instanceof` จะทำให้เราทำงานเฉพาะกับอ็อบเจ็กต์ประเภท `FillLayer` เท่านั้น

### Step 4: Configure Fill Layer Settings
เมื่อคุณระบุได้ว่าเป็นเลเยอร์เติมแล้ว ขั้นตอนต่อไปคือการปรับตั้งค่าต่าง ๆ เช่น การเลื่อนตำแหน่ง, การสเกล, และรายละเอียดของลวดลาย  
```java
IPatternFillSettings settings = (IPatternFillSettings) fillLayer.getFillSettings();
settings.setHorizontalOffset(-5);
settings.setVerticalOffset(12);
settings.setScale(300);
settings.setLinked(true);
```
แต่ละคุณสมบัติจะส่งผลต่อวิธีการเรนเดอร์ลวดลาย ตัวอย่างเช่น การปรับค่า offset จะทำให้ลวดลายเลื่อนตำแหน่งสัมพันธ์กับเลเยอร์

### Step 5: Define Pattern Data
ต่อไปเป็นการกำหนดข้อมูลลวดลายจริง ๆ โดยการระบุสีที่ประกอบเป็นลวดลายเติมของคุณ  
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
คุณสามารถเปลี่ยนสีใด ๆ ตามต้องการเพื่อสร้างสไตล์ที่เป็นเอกลักษณ์ของคุณเอง

### Step 6: Set Pattern Dimensions and Name
การปรับแต่งเพิ่มเติมของเลเยอร์เติมรวมถึงการกำหนดความกว้างและความสูงของลวดลาย พร้อมตั้งชื่อและ ID ที่ไม่ซ้ำกันให้กับลวดลาย  
```java
settings.setPatternHeight(4);
settings.setPatternWidth(4);
settings.setPatternName("$$$/Presets/Patterns/ColorfulSquare=Colorful Square New\0");
settings.setPatternId(UUID.randomUUID() + "\0");
```
ขนาดจะควบคุมการทำเป็นไทล์ของลวดลาย ส่วนชื่อและ ID จะช่วยให้คุณระบุลวดลายได้ง่ายในภายหลัง

### Step 7: Update the Fill Layer
หลังจากตั้งค่าทุกอย่างแล้ว คุณต้องอัปเดตเลเยอร์ด้วยการเรียกเมธอดที่ทำการบันทึกการเปลี่ยนแปลงลงในโครงสร้าง PSD ด้านล่าง  
```java
fillLayer.update();
```
การเรียก `update()` จะนำการแก้ไขทั้งหมดไปใช้กับโครงสร้าง PSD ภายใน

### Step 8: Save the Changes
สุดท้ายบันทึกไฟล์ PSD ที่อัปเดตแล้วด้วยเมธอด `save()` ขั้นตอนนี้จะเขียนการเปลี่ยนแปลงทั้งหมดกลับไปยังเอกสาร  
```java
image.save(outputFile, new PsdOptions(image));
```
ไฟล์ใหม่ของคุณตอนนี้มีเลเยอร์เติมลวดลายที่กำหนดเองแล้ว

### Step 9: Dispose of the Image Object
เพื่อคืนทรัพยากร, ควรทำการปล่อยอ็อบเจ็กต์ภาพเมื่อใช้งานเสร็จแล้ว  
```java
finally {
    image.dispose();
}
```
การทำ `dispose()` จะช่วยให้หน่วยความจำถูกปล่อยออกอย่างรวดเร็ว โดยเฉพาะเมื่อประมวลผลไฟล์ PSD ขนาดใหญ่

## Common Issues and Solutions
- **Pattern not visible after saving** – ตรวจสอบว่าเลเยอร์ที่แก้ไขไม่ได้ถูกซ่อน (`layer.setVisible(true)`) และขนาดลวดลายตรงกับขนาดไทล์ที่คาดหวัง  
- **`ClassCastException`** – ตรวจสอบให้แน่ใจว่าคุณทำการแคสต์เป็น `FillLayer` หลังจากยืนยันว่าเป็น `instanceof FillLayer` แล้วเท่านั้น  
- **File path errors** – ใช้พาธแบบเต็มหรือทำการ escape ตัวอักษร backslash สองครั้งบน Windows (`C:\\\\Images\\\\sample.psd`)  

## FAQ's
### What is Aspose.PSD for JavaSD for Java คือไลบรารีที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Photoshop PSD ได้อย่างโปรแกรมเมติก

### Can I try Aspose.PSD for free?  
ได้, คุณสามารถเข้าถึง [free trial](https://releases.aspose.com/) เพื่อสำรวจฟีเจอร์ต่าง ๆ ได้

### Where can I buy Aspose.PSD?  
คุณสามารถซื้อไลเซนส์ได้จาก [Aspose purchase page](https://purchase.aspose.com/buy)

### Is there any support available for Aspose.PSD?  
แน่นอน! คุณสามารถรับความช่วยเหลือจาก [Aspose support forum](https://forum.aspose.com/c/psd/34)

### What should I do if I encounter issues when using Aspose.PSD?  
ตรวจสอบเอกสารสำหรับเคล็ดลับการแก้ปัญหา หรือขอความช่วยเหลือใน [support forum](https://forum.aspose.com/c/psd/34)

**Additional Q&A**

**Q: Can I use this code to create multiple pattern fill layers in one PSD?**  
A: ได้. เพียงทำซ้ำลูปสำหรับแต่ละ `FillLayer` ที่ต้องการปรับแต่งและตั้งค่าตามต้องการ

**Q: Does the library support PSD files with layer effects applied?**  
A: Aspose.PSD จะคงเอฟเฟกต์ของเลเยอร์ส่วนใหญ่ไว้, แต่การเติมลวดลายแบบกำหนดเองจะใช้ได้เฉพาะกับอ็อบเจ็กต์ `FillLayer` เท่านั้น

**Q: Is there a way to read an existing pattern from a PSD and reuse it?**  
A: คุณสามารถดึง `IPatternFillSettings` ปัจจุบันจาก `FillLayer` แล้วทำการคลอนคุณสมบัติก่อนนำไปปรับใช้ใหม่ได้

---

**Last Updated:** 2025-12-14  
**Tested With:** Aspose.PSD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}