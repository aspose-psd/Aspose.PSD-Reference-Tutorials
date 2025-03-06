---
title: เรนเดอร์รูปแบบการเติมเลเยอร์ในไฟล์ PSD โดยใช้ Java
linktitle: เรนเดอร์รูปแบบการเติมเลเยอร์ในไฟล์ PSD โดยใช้ Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีใช้ Aspose.PSD สำหรับ Java เพื่อแสดงเลเยอร์การเติมรูปแบบในไฟล์ PSD ด้วยบทช่วยสอนทีละขั้นตอนที่ครอบคลุมนี้
weight: 24
url: /th/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เรนเดอร์รูปแบบการเติมเลเยอร์ในไฟล์ PSD โดยใช้ Java

## การแนะนำ
ในขอบเขตของการออกแบบกราฟิก การทำงานกับเอกสาร Photoshop (PSD) ไม่เคยราบรื่นเท่านี้มาก่อนด้วยเครื่องมืออย่าง Aspose.PSD สำหรับ Java หากคุณกำลังผจญภัยเข้าสู่โลกแห่งการปรับแต่ง PSD การทำความเข้าใจวิธีเรนเดอร์เลเยอร์การเติมรูปแบบอย่างมีประสิทธิภาพสามารถช่วยคุณประหยัดเวลาได้มาก ลองนึกภาพความสามารถในการทำให้กระบวนการออกแบบของคุณเป็นแบบอัตโนมัติหรือปรับแต่งเลเยอร์โดยทางโปรแกรม ค่อนข้างเท่ห์ใช่มั้ย? ในคู่มือนี้ เราจะอธิบายขั้นตอนที่จำเป็นในการโหลดไฟล์ PSD จัดการเลเยอร์ของไฟล์ และจัดการการเติมรูปแบบโดยใช้ Java มาดำน้ำกันเถอะ!
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่มต้น มีสิ่งที่ต้องมีบางประการเพื่อให้แน่ใจว่าคุณสามารถปฏิบัติตามได้โดยไม่มีปัญหา:
1.  Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนเครื่องของคุณแล้ว คุณสามารถดาวน์โหลดได้จาก[เว็บไซต์ของออราเคิล](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  Aspose.PSD สำหรับ Java: หากต้องการจัดการไฟล์ PSD คุณจะต้องมีไลบรารี Aspose.PSD คุณสามารถดาวน์โหลดได้จาก[กำหนดหน้าการเผยแพร่](https://releases.aspose.com/psd/java/).
3. สภาพแวดล้อมการพัฒนาแบบรวม (IDE): IDE เช่น IntelliJ IDEA, Eclipse หรือ NetBeans จะทำให้การเขียนโค้ดง่ายขึ้น เลือกที่คุณชื่นชอบ!
4. ความรู้พื้นฐานของ Java: ความคุ้นเคยกับไวยากรณ์ Java จะช่วยให้คุณนำทางผ่านบทช่วยสอนนี้ได้อย่างมีประสิทธิภาพ
5. ไฟล์ PSD ตัวอย่าง: เตรียมไฟล์ PSD ให้พร้อมสำหรับการทดสอบ คุณสามารถสร้างได้โดยใช้ Photoshop หรือดาวน์โหลดไฟล์ตัวอย่างจากเว็บ
เมื่อคุณมีสิ่งเหล่านี้ครบแล้ว คุณก็พร้อมที่จะเริ่มต้นการเขียนโค้ด!
## แพ็คเกจนำเข้า
หากต้องการเริ่มต้นใช้งาน Aspose.PSD สำหรับ Java คุณต้องนำเข้าแพ็คเกจที่จำเป็น ต่อไปนี้เป็นวิธีการตั้งค่าในโปรเจ็กต์ Java ของคุณ:
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
การนำเข้าเหล่านี้มีฟังก์ชันการทำงานที่ช่วยให้คุณสามารถทำงานกับรูปภาพ PSD เข้าถึงเลเยอร์ และจัดการคุณลักษณะต่างๆ ของเลเยอร์การเติมได้ 
ตอนนี้ เรามาเจาะลึกกระบวนการทีละขั้นตอนเพื่อแสดงเลเยอร์การเติมรูปแบบในไฟล์ PSD ของคุณ
## ขั้นตอนที่ 1: กำหนดไดเรกทอรีต้นทางและเอาต์พุตของคุณ
ในการเริ่มต้น คุณต้องกำหนดตำแหน่งของไฟล์ PSD ต้นฉบับของคุณ และตำแหน่งที่คุณต้องการบันทึกไฟล์เอาต์พุต 
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String sourceFile = sourceDir + "sample.psd";
String outputFile = outputDir + "sample_out.psd";
```
 ข้อมูลโค้ดนี้กำหนดเส้นทางไฟล์ที่จำเป็น แทนที่`"Your Source Directory"` และ`"Your Document Directory"` พร้อมเส้นทางจริงบนเครื่องของคุณ 
## ขั้นตอนที่ 2: โหลดไฟล์ PSD
 จากนั้น คุณจะโหลดไฟล์ PSD ลงในอินสแตนซ์ของไฟล์`PsdImage` ระดับ. ขั้นตอนนี้จะเปิดไฟล์ PSD ของคุณเพื่อจัดการ
```java
PsdImage image = (PsdImage) Image.load(sourceFile);
```
 ที่นี่ คุณกำลังส่งภาพที่โหลดไปที่`PsdImage`ซึ่งช่วยให้คุณเข้าถึงคุณสมบัติและวิธีการเฉพาะของ PSD ได้
## ขั้นตอนที่ 3: วนซ้ำผ่านเลเยอร์
ในการค้นหาและจัดการเลเยอร์การเติม คุณต้องวนซ้ำเลเยอร์ทั้งหมดในอิมเมจ PSD ที่โหลด
```java
try {
    for (Layer layer : image.getLayers()) {
        if (layer instanceof FillLayer) {
            FillLayer fillLayer = (FillLayer)layer;
            // รหัสเพิ่มเติมจะอยู่ที่นี่
        }
    }
}
```
 ข้อมูลโค้ดนี้จะตรวจสอบว่าเลเยอร์ปัจจุบันเป็นตัวอย่างของหรือไม่`FillLayer`- หากเป็นเช่นนั้น คุณจะสามารถแก้ไขคุณสมบัติของมันได้ในขั้นตอนต่อๆ ไป
## ขั้นตอนที่ 4: กำหนดการตั้งค่าการเติมเลเยอร์
เมื่อคุณระบุเลเยอร์การเติมแล้ว ขั้นตอนต่อไปคือการแก้ไขการตั้งค่า ที่นี่คุณสามารถปรับแต่งรายละเอียดออฟเซ็ต สเกล และรูปแบบได้
```java
IPatternFillSettings settings = (IPatternFillSettings) fillLayer.getFillSettings();
settings.setHorizontalOffset(-5);
settings.setVerticalOffset(12);
settings.setScale(300);
settings.setLinked(true);
```
 ที่นี่คุณกำลังตั้งค่าคุณสมบัติต่างๆ ของเลเยอร์การเติม การตั้งค่าแต่ละอย่างเหล่านี้มีส่วนช่วยให้การเติมรูปแบบแสดงผลเป็นภาพได้อย่างไร เช่น การปรับ`setHorizontalOffset` และ`setVerticalOffset` สามารถเปลี่ยนรูปแบบให้สัมพันธ์กับเลเยอร์ได้ 
## ขั้นตอนที่ 5: กำหนดข้อมูลรูปแบบ
ตอนนี้ได้เวลากำหนดค่ารูปแบบจริงแล้ว สิ่งนี้เกี่ยวข้องกับการกำหนดสีที่จะประกอบขึ้นเป็นรูปแบบการเติมของคุณ
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
ที่นี่ คุณกำลังตั้งค่าอาร์เรย์ข้อมูลสีของรูปแบบการเติม คุณสามารถปรับแต่งรายการนี้ด้วยสีที่คุณต้องการเพื่อสร้างสไตล์ภาพที่เป็นเอกลักษณ์
## ขั้นตอนที่ 6: กำหนดขนาดและชื่อรูปแบบ
การปรับแต่งเลเยอร์การเติมเพิ่มเติมนั้นเกี่ยวข้องกับการกำหนดความกว้างและความสูงของเลเยอร์การเติม รวมถึงการกำหนดชื่อและ ID ที่ไม่ซ้ำกัน
```java
settings.setPatternHeight(4);
settings.setPatternWidth(4);
settings.setPatternName("$$$/Presets/Patterns/ColorfulSquare=Colorful Square New\0");
settings.setPatternId(UUID.randomUUID() + "\0");
```
 โดยการปรับ`setPatternHeight` และ`setPatternWidth`คุณสามารถควบคุมขนาดของรูปแบบการเติมของคุณได้ ชื่อและรหัสสามารถช่วยระบุรูปแบบได้ในภายหลัง
## ขั้นตอนที่ 7: อัปเดตเลเยอร์การเติม
หลังจากกำหนดค่าคุณสมบัติที่ต้องการทั้งหมดแล้ว คุณจะต้องอัปเดตเลเยอร์เมื่อมีการเปลี่ยนแปลงใดๆ เกิดขึ้น
```java
fillLayer.update();
```
ขั้นตอนนี้มีความสำคัญเนื่องจากจะใช้การแก้ไขทั้งหมดที่คุณทำกับออบเจ็กต์เลเยอร์การเติม
## ขั้นตอนที่ 8: บันทึกการเปลี่ยนแปลง
 สุดท้าย ให้บันทึกไฟล์ PSD ที่อัปเดตโดยใช้นามสกุลไฟล์`save()` วิธี. ขั้นตอนนี้เขียนการเปลี่ยนแปลงทั้งหมดของคุณกลับไปยังเอกสาร
```java
image.save(outputFile, new PsdOptions(image));
```
เมื่อบันทึกรูปภาพ การแก้ไขของคุณจะถูกนำไปใช้กับไฟล์เอาต์พุตที่ระบุ 
## ขั้นตอนที่ 9: กำจัดวัตถุรูปภาพ
หากต้องการเพิ่มพื้นที่ว่าง แนวทางปฏิบัติที่ดีคือการกำจัดรูปภาพเมื่อคุณดำเนินการเสร็จแล้ว
```java
finally {
    image.dispose();
}
```
สิ่งนี้จะช่วยให้มั่นใจได้ว่าออบเจ็กต์ทั้งหมดได้รับการล้างข้อมูลอย่างเหมาะสมและจะไม่ใช้หน่วยความจำโดยไม่จำเป็น
## บทสรุป
และคุณก็ได้แล้ว! คุณสร้างเลเยอร์การเติมลวดลายในไฟล์ PSD ได้สำเร็จโดยใช้ Java และ Aspose.PSD เทคนิคที่เรียบง่ายแต่ทรงพลังนี้เปิดประตูสู่การทำงานออกแบบกราฟิกแบบอัตโนมัติและบูรณาการเข้ากับแอปพลิเคชันได้อย่างราบรื่น จำไว้ว่าการฝึกฝนทำให้สมบูรณ์แบบ! ยิ่งคุณทดลองใช้การปรับแต่ง PSD มากเท่าไร คุณก็จะยิ่งเก่งขึ้นเท่านั้น 
## คำถามที่พบบ่อย
### Aspose.PSD สำหรับ Java คืออะไร  
Aspose.PSD สำหรับ Java เป็นไลบรารีที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Photoshop PSD โดยทางโปรแกรม
### ฉันสามารถทดลองใช้ Aspose.PSD ได้ฟรีหรือไม่  
 ใช่ คุณสามารถเข้าถึง[ทดลองใช้ฟรี](https://releases.aspose.com/) เพื่อสำรวจฟังก์ชันการทำงาน
### ฉันจะซื้อ Aspose.PSD ได้ที่ไหน  
 คุณสามารถซื้อใบอนุญาตได้จาก[กำหนดหน้าการซื้อ](https://purchase.aspose.com/buy).
### มีการสนับสนุนสำหรับ Aspose.PSD หรือไม่  
 อย่างแน่นอน! คุณสามารถขอความช่วยเหลือได้จาก[กำหนดฟอรั่มการสนับสนุน](https://forum.aspose.com/c/psd/34).
### ฉันควรทำอย่างไรหากพบปัญหาเมื่อใช้ Aspose.PSD  
 ตรวจสอบเอกสารสำหรับคำแนะนำในการแก้ไขปัญหาหรือขอความช่วยเหลือใน[ฟอรั่มการสนับสนุน](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
