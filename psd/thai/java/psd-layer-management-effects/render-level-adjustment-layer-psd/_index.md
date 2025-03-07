---
title: เลเยอร์การปรับระดับการเรนเดอร์ในไฟล์ PSD - Java
linktitle: เลเยอร์การปรับระดับการเรนเดอร์ในไฟล์ PSD - Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีปรับปรุงคอนทราสต์และความมีชีวิตชีวาของภาพได้อย่างง่ายดายโดยใช้ Aspose.PSD สำหรับ Java เลเยอร์การปรับระดับมาสเตอร์พร้อมคำแนะนำทีละขั้นตอนนี้
weight: 17
url: /th/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เลเยอร์การปรับระดับการเรนเดอร์ในไฟล์ PSD - Java

## การแนะนำ

คุณเคยเปิดไฟล์ PSD เพียงเพื่อพบว่าภาพขาดคอนทราสต์หรือความมีชีวิตชีวาหรือไม่? อย่ากลัวเลย นักรบแห่งการแก้ไขภาพ! Aspose.PSD สำหรับ Java เข้ามาช่วยเหลือด้วยความสามารถในการจัดการ Levels Adjustment Layer อันทรงพลัง คู่มือนี้จะช่วยให้คุณมีความรู้ในการปรับแต่งภาพของคุณโดยใช้ Levels ได้อย่างง่ายดาย 

## ข้อกำหนดเบื้องต้น

- Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK เวอร์ชันล่าสุดไว้ในระบบของคุณ คุณสามารถดาวน์โหลดได้จากเว็บไซต์ Oracle ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)-
- Aspose.PSD สำหรับไลบรารี Java: ดาวน์โหลด Aspose.PSD สำหรับไลบรารี Java จากหน้าดาวน์โหลด ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)- คุณจะต้องมีใบอนุญาตที่ถูกต้องเพื่อใช้คุณสมบัติทั้งหมด แต่สามารถทดลองใช้ฟรีเพื่อเริ่มต้นใช้งาน ([https://releases.aspose.com/](https://releases.aspose.com/)-

## แพ็คเกจนำเข้า

ก่อนที่จะเจาะลึกโค้ด เราจำเป็นต้องนำเข้าคลาส Aspose.PSD ที่จำเป็นเพื่อโต้ตอบกับไฟล์ PSD นี่คือสิ่งที่คุณต้องการ:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

 ที่`com.aspose.psd` แพ็คเกจให้การเข้าถึงฟังก์ชันการจัดการ PSD ในขณะที่`com.aspose.psd.imaging.PngOptions` ช่วยให้เราสามารถกำหนดตัวเลือกเมื่อบันทึกภาพเป็น PNG

ตอนนี้ เรามาเริ่มต้นการผจญภัยในการปรับระดับกันเถอะ:

## ขั้นตอนที่ 1: การตั้งค่าเส้นทางไฟล์:

- กำหนดตัวแปรสำหรับไดเร็กทอรีเอกสารของคุณ (`dataDir`) ชื่อไฟล์ PSD ต้นฉบับ (`sourceFileName`) กำหนดเป้าหมายชื่อไฟล์ PSD หลังจากแก้ไข (`psdPathAfterChange`) และเส้นทางการส่งออก PNG สุดท้าย (`pngExportPath`- พิจารณาใช้ชื่อที่สื่อความหมายเพื่อปรับปรุงความสามารถในการอ่านโค้ด

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## ขั้นตอนที่ 2: กำลังโหลดรูปภาพ PSD:

-  ใช้`Image.load` วิธีการเปิดไฟล์ PSD ต้นฉบับและจัดเก็บไว้ในไฟล์`PsdImage`วัตถุ (`im`- Aspose.PSD จะตรวจจับรูปแบบไฟล์โดยอัตโนมัติ

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## ขั้นตอนที่ 3: วนซ้ำผ่านเลเยอร์:

- เราจำเป็นต้องค้นหาเลเยอร์การปรับระดับภายใน PSD ของคุณ Aspose มอบวิธีที่สะดวกในการวนซ้ำทุกเลเยอร์โดยใช้ลูป

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (โค้ดสำหรับตรวจสอบ Levels Layer จะถูกเพิ่มไว้ที่นี่)
}
```

## ขั้นตอนที่ 4: การระบุเลเยอร์ระดับ:

- ภายในลูปตรวจสอบว่าเลเยอร์ปัจจุบัน (`im.getLayers()[i]` ) เป็นตัวอย่างหนึ่งของ`LevelsLayer` ชั้นเรียนโดยใช้`instanceof` ตัวดำเนินการ 
-  หากเป็นเช่นนั้น ให้ส่งเลเยอร์ไปที่ a`LevelsLayer` วัตถุเพื่อการจัดการต่อไป

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (โค้ดปรับระดับจะถูกเพิ่มไว้ที่นี่)
   }
}
```
## ขั้นตอนที่ 5: ปรับระดับแบบละเอียด (ต่อ):

-  ปรับระดับเอาต์พุตโดยใช้`setOutputShadowLevel` และ`setOutputHighlightLevel` เพื่อควบคุมความมืดและความสว่างของภาพที่ได้ ค่าเหล่านี้จะกำหนดช่วงของระดับอินพุตที่จะถูกแมปกับช่วงเอาต์พุต

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // ปรับระดับอินพุต (0-255):
	   channel.setInputShadowLevel((short) 10); // ทำให้เงามืดลงเล็กน้อย
	   channel.setInputMidtoneLevel(2.0f);     // เพิ่มเสียงกลาง
	   channel.setInputHighlightLevel((short) 230); // ลดไฮไลท์

	   // ปรับระดับเอาต์พุต (0-255):
	   channel.setOutputShadowLevel((short) 20); // ทำให้เงามืดลงอีก
	   channel.setOutputHighlightLevel((short) 200); //ไฮไลท์ให้สดใส
   }
}
```

## ขั้นตอนที่ 6: บันทึก PSD ที่แก้ไขแล้ว:

-  ใช้`save` วิธีการของ`PsdImage` วัตถุเพื่อบันทึกภาพที่แก้ไขไปยังเส้นทางที่ระบุ (`psdPathAfterChange`-

```java
im.save(psdPathAfterChange);
```

## ขั้นตอนที่ 7: ส่งออกเป็น PNG (ไม่บังคับ):

-  หากคุณต้องการรูปภาพที่ปรับแล้วในเวอร์ชัน PNG ให้สร้างไฟล์`PngOptions` object และตั้งค่าประเภทสีเป็น`TruecolorWithAlpha` - จากนั้นใช้`save` วิธีการอีกครั้งด้วยเส้นทางและตัวเลือกการส่งออก PNG

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

และคุณก็ได้แล้ว! คุณได้ปรับระดับเลเยอร์การปรับระดับในไฟล์ PSD ของคุณโดยใช้ Aspose.PSD สำหรับ Java เรียบร้อยแล้ว ด้วยการทำความเข้าใจขั้นตอนเหล่านี้และทดลองใช้ค่าต่างๆ คุณจะสามารถเพิ่มคอนทราสต์และลักษณะโดยรวมของภาพได้

## บทสรุป

Aspose.PSD สำหรับ Java ช่วยให้คุณสามารถควบคุมกระบวนการแก้ไขภาพของคุณได้ ด้วยการเรียนรู้เลเยอร์การปรับระดับ คุณจะสามารถสร้างชีวิตใหม่ให้กับภาพถ่ายและการออกแบบของคุณได้ โปรดจำไว้ว่า การฝึกฝนทำให้สมบูรณ์แบบ ดังนั้นอย่าลังเลที่จะทดลองและสำรวจศักยภาพสูงสุดของเครื่องมืออันทรงพลังนี้
 
## คำถามที่พบบ่อย

### ฉันสามารถปรับช่องสีแต่ละช่อง (RGB) แยกกันได้หรือไม่ 
ใช่ คุณสามารถเข้าถึงแต่ละช่องสีได้โดยใช้`getChannel` วิธีการของ`LevelsLayer` คัดค้านและปรับเปลี่ยนระดับของมันอย่างอิสระ

### ฉันจะจัดการกับเลเยอร์การปรับระดับหลายชั้นใน PSD ได้อย่างไร
โค้ดจะวนซ้ำทุกเลเยอร์ ดังนั้นมันจะประมวลผลเลเยอร์ระดับเพิ่มเติมใดๆ ที่พบในรูปภาพโดยอัตโนมัติ

### มีวิธีอื่นในการปรับคอนทราสต์ของภาพนอกเหนือจากระดับหรือไม่
อย่างแน่นอน! Aspose.PSD มีเครื่องมือปรับแต่งภาพมากมาย เช่น Curves, Brightness/Contrast และอื่นๆ อีกมากมาย

### ฉันสามารถทำให้กระบวนการนี้เป็นอัตโนมัติสำหรับภาพหลายภาพได้หรือไม่? 
ได้ คุณสามารถรวมโค้ดนี้เข้ากับสคริปต์ประมวลผลแบบวนซ้ำหรือเป็นชุดเพื่อประมวลผลไฟล์ PSD หลายไฟล์ได้อย่างมีประสิทธิภาพ

### ฉันจะหาข้อมูลเพิ่มเติมและการสนับสนุนได้ที่ไหน?
Aspose มีเอกสารประกอบมากมาย ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) และฟอรัมสนับสนุน ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) สำหรับคำถามหรือปัญหาใด ๆ ที่คุณอาจพบ
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
