---
title: เพิ่มเลเยอร์การปรับความอิ่มตัวของสีให้กับ PSD
linktitle: เพิ่มเลเยอร์การปรับความอิ่มตัวของสีให้กับ PSD
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีเพิ่มเลเยอร์การปรับความอิ่มตัวของสีให้กับ PSD โดยใช้ Aspose.PSD สำหรับ Java ในบทช่วยสอนที่ครอบคลุมทีละขั้นตอนนี้ ปรับปรุงขั้นตอนการออกแบบกราฟิกของคุณ
type: docs
weight: 14
url: /th/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---
## การแนะนำ
เมื่อพูดถึงการออกแบบกราฟิก การปรับแต่งสีมีบทบาทสำคัญ โดยเฉพาะอย่างยิ่ง การปรับแต่งเฉดสี ความอิ่มตัวของสี และความสว่าง สามารถเปลี่ยนอารมณ์และคุณภาพของภาพได้อย่างมาก วิธีหนึ่งที่มีประสิทธิภาพในการบรรลุเป้าหมายนี้คือการใช้เลเยอร์การปรับแต่งใน Photoshop (ไฟล์ PSD) หากคุณต้องการปรับปรุงไฟล์ PSD ของคุณโดยทางโปรแกรมโดยใช้ Java ไลบรารี Aspose.PSD พร้อมให้ความช่วยเหลือ! บทช่วยสอนนี้จะนำคุณผ่านขั้นตอนต่างๆ ในการเพิ่มเลเยอร์การปรับความอิ่มตัวของสีให้กับไฟล์ PSD ของคุณ ซึ่งจะทำให้ขั้นตอนการทำงานของคุณมีประสิทธิผลและประสิทธิผลมากขึ้น
ในคู่มือนี้ เราจะครอบคลุมทุกอย่างตั้งแต่การนำเข้าแพ็คเกจที่จำเป็นไปจนถึงรายละเอียดสำคัญของตัวอย่างโค้ด
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะพูดถึงโค้ด ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:
1.  Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK 8 ขึ้นไปบนเครื่องของคุณ คุณสามารถดาวน์โหลดได้จาก[ดาวน์โหลดชุดพัฒนา Java SE](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD สำหรับไลบรารี Java: คุณจะต้องมีไลบรารี Aspose.PSD ซึ่งคุณสามารถทำได้[ดาวน์โหลดได้ที่นี่](https://releases.aspose.com/psd/java/). 
3. IDE: สภาพแวดล้อมการพัฒนาแบบรวม (IDE) ที่เหมาะสม เช่น IntelliJ IDEA หรือ Eclipse สำหรับการพัฒนา Java
4. ความรู้พื้นฐานของ Java: ความคุ้นเคยกับการเขียนโปรแกรม Java นั้นเป็นข้อดี แต่ไม่ต้องกังวล เราจะแนะนำคุณเกี่ยวกับรหัสทีละขั้นตอน
ตอนนี้เราได้จัดการข้อกำหนดเบื้องต้นแล้ว มาดูส่วนที่สนุกกันดีกว่า—การเขียนโค้ด!
## แพ็คเกจนำเข้า
ในการเริ่มทำงานกับไลบรารี Aspose.PSD ขั้นตอนแรกคือการนำเข้าคลาสที่จำเป็น ต่อไปนี้คือวิธีที่คุณสามารถทำได้ในไฟล์ Java ของคุณ:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
ตรวจสอบให้แน่ใจว่าคุณได้เพิ่มไลบรารีที่เหมาะสมลงในโปรเจ็กต์ของคุณ เพื่อให้การนำเข้าเหล่านี้ทำงานได้อย่างราบรื่น
## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสารของคุณ
ทุกโครงการจำเป็นต้องมีจุดเริ่มต้น และโครงการของเราก็ไม่มีข้อยกเว้น คุณต้องระบุไดเร็กทอรีที่เก็บไฟล์ PSD ของคุณ นี่เป็นสิ่งสำคัญสำหรับการโหลดและบันทึกภาพอย่างถูกต้อง
```java
String dataDir = "Your Document Directory"; // อัปเดตเส้นทางนี้ไปยังไดเร็กทอรีจริงของคุณ
```
## ขั้นตอนที่ 2: โหลดไฟล์ PSD ที่มีอยู่
ในการจัดการไฟล์ PSD ที่มีอยู่ เราต้องโหลดมันลงในโปรแกรมของเราก่อน ต่อไปนี้คือวิธีที่คุณสามารถทำได้:
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 ในรหัสนี้ให้อัปเดต`"HueSaturationAdjustmentLayer.psd"` เป็นชื่อไฟล์ PSD ที่มีอยู่ที่คุณต้องการแก้ไข
## ขั้นตอนที่ 3: แก้ไขเลเยอร์ Hue/Saturation
ต่อไป เราจะวนซ้ำเลเยอร์ต่างๆ ของรูปภาพ PSD ที่โหลดไว้ เพื่อค้นหาและแก้ไขเลเยอร์ Hue/Saturation ที่มีอยู่ ขั้นตอนนี้เกี่ยวข้องกับการปรับเปลี่ยนค่าเฉดสี ความอิ่มตัว และความสว่าง
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```
ในตัวอย่างนี้:
- เรากำลังปรับเฉดสีเป็น -25 ความอิ่มตัวของสีเป็น -12 และความสว่างเป็น +67
-  ที่`getRange(2)` วิธีการช่วยให้เราปรับแต่งช่วงสีที่ต้องการได้
## ขั้นตอนที่ 4: บันทึกไฟล์ PSD ที่แก้ไข
หลังจากปรับแต่งแล้ว ขั้นตอนต่อไปคือการบันทึกไฟล์ นี่เป็นส่วนสำคัญของกระบวนการของเรา เพื่อให้มั่นใจว่าการเปลี่ยนแปลงที่เราทำไว้จะไม่สูญหาย
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## ขั้นตอนที่ 5: เพิ่มเลเยอร์ Hue/Saturation ใหม่
ถัดไป คุณอาจต้องการเพิ่มเลเยอร์การปรับ Hue/Saturation ใหม่ให้กับไฟล์ PSD อื่น เพียงทำตามวิธีการเดียวกับที่คุณใช้ก่อนหน้านี้ แต่ใช้ไฟล์ PSD ที่แตกต่างกัน
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## ขั้นตอนที่ 6: ตั้งค่า Hue/Saturation ใหม่สำหรับเลเยอร์ใหม่
เมื่อคุณสร้างเลเยอร์ใหม่แล้ว ให้ตั้งค่าเฉดสี ความอิ่มตัว และความสว่างที่ต้องการเหมือนเมื่อก่อน
```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```
## ขั้นตอนที่ 7: บันทึกไฟล์ PSD ที่อัปเดต
สุดท้าย ให้บันทึกไฟล์ PSD ด้วยเลเยอร์ Hue/Saturation ที่เพิ่มเข้ามาเพื่อให้คุณเห็นการเปลี่ยนแปลงของคุณ
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
ยินดีด้วย! คุณจัดการไฟล์ PSD สำเร็จโดยใช้ Aspose.PSD สำหรับ Java ตอนนี้คุณสามารถทดลองกับรูปภาพต่างๆ และการปรับแต่งที่ลึกซึ้งยิ่งขึ้น เพื่อทำให้โปรเจ็กต์การออกแบบกราฟิกของคุณมีชีวิตขึ้นมา
## บทสรุป
การทำงานกับกราฟิกโดยทางโปรแกรมจะเปิดโลกแห่งความเป็นไปได้ การใช้ Aspose.PSD สำหรับ Java เพื่อเพิ่มและแก้ไข Hue Saturation Adjustment Layers มอบความยืดหยุ่นและประสิทธิภาพที่สามารถทำให้ขั้นตอนการออกแบบของคุณคล่องตัวขึ้น ไม่ว่าคุณจะปรับปรุงภาพถ่ายสำหรับโปรเจ็กต์หรือสร้างเนื้อหาภาพที่น่าทึ่ง การใช้เครื่องมือเหล่านี้อย่างเชี่ยวชาญสามารถปรับปรุงผลลัพธ์ของคุณได้อย่างมาก
 สำรวจฟังก์ชันเพิ่มเติมของ Aspose.PSD ได้อย่างอิสระโดยเข้าไปดู[เอกสารประกอบ](https://reference.aspose.com/psd/java/) หรือพิจารณาขัดขวาง[ใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/) เพื่อทดสอบศักยภาพของห้องสมุดอย่างเต็มที่
## คำถามที่พบบ่อย
### เลเยอร์การปรับความอิ่มตัวของสีคืออะไร
เลเยอร์การปรับความอิ่มตัวของสีช่วยให้คุณสามารถแก้ไขคุณสมบัติสีของภาพโดยไม่ต้องเปลี่ยนพิกเซลดั้งเดิมอย่างถาวร
### ฉันจำเป็นต้องติดตั้ง Photoshop เพื่อใช้ Aspose.PSD หรือไม่
ไม่ Aspose.PSD เป็นไลบรารีแบบสแตนด์อโลนที่ทำงานโดยไม่ขึ้นอยู่กับ Photoshop
### ฉันสามารถใช้ Aspose.PSD สำหรับการประมวลผลเป็นชุดได้หรือไม่
ใช่ คุณสามารถดำเนินการและประมวลผลไฟล์ PSD หลายไฟล์เป็นชุดโดยอัตโนมัติด้วย Aspose.PSD
### Aspose.PSD ฟรีหรือไม่
Aspose.PSD ให้ทดลองใช้ฟรี แต่ต้องมีใบอนุญาตสำหรับการใช้งานระยะยาว คุณสามารถดูราคาได้[ที่นี่](https://purchase.aspose.com/buy).