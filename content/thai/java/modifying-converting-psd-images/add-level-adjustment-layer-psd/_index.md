---
title: เพิ่มเลเยอร์การปรับระดับใน PSD
linktitle: เพิ่มเลเยอร์การปรับระดับใน PSD
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีเพิ่ม Level Adjustment Layer ในไฟล์ PSD ของคุณอย่างมีประสิทธิภาพโดยใช้ Aspose.PSD สำหรับ Java ยกระดับทักษะการแก้ไขภาพของคุณ
type: docs
weight: 16
url: /th/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---
## การแนะนำ
เมื่อพูดถึงการแก้ไขภาพ การจัดการระดับสามารถสร้างโลกแห่งความแตกต่างในความมีชีวิตชีวาและความคมชัดของภาพถ่ายของคุณ เครื่องมือที่มีประโยชน์อย่างหนึ่งในคลังแสง Photoshop คือ "Level Adjustment Layer" ซึ่งช่วยให้คุณปรับแต่งช่วงโทนสีและความสมดุลของสีของภาพได้ ในคู่มือนี้ เราจะอธิบายวิธีใช้งาน Level Adjustment Layer ในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java ดังนั้นคว้า Java IDE ของคุณ
## ข้อกำหนดเบื้องต้น
ก่อนที่คุณจะกระโดดเข้าสู่โลกแห่งการปรับระดับ คุณจะต้องตั้งค่าบางสิ่งเพื่อให้แน่ใจว่าการขับขี่ราบรื่น:
1.  Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนเครื่องของคุณแล้ว หากไม่มีก็สามารถไปคว้าได้จาก[เว็บไซต์ออราเคิล](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) หรือใช้ OpenJDK
2.  Aspose.PSD สำหรับไลบรารี Java: หากต้องการจัดการไฟล์ PSD คุณจะต้องดาวน์โหลดไลบรารี Aspose.PSD คุณสามารถรับเวอร์ชันล่าสุดได้จากสิ่งนี้[ลิงค์ดาวน์โหลด](https://releases.aspose.com/psd/java/) และให้แน่ใจว่าคุณได้รวม JAR ไว้ในไลบรารีของโปรเจ็กต์ของคุณแล้ว
3. ความรู้พื้นฐานของ Java: การมีความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม Java จะช่วยได้ เนื่องจากเราจะเจาะลึกลงไปในตัวอย่างโค้ดตลอดบทช่วยสอนนี้
4. การตั้งค่า IDE: คุณสามารถใช้ Java IDE ใดก็ได้ที่คุณต้องการ เช่น IntelliJ IDEA, Eclipse หรือ NetBeans เพื่อเขียนและรันโค้ดของคุณ เพียงตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าโปรเจ็กต์ Java ของคุณและเพิ่มไลบรารี Aspose.PSD แล้ว

## แพ็คเกจนำเข้า
ก่อนที่เราจะเริ่มเขียนโค้ด เราจำเป็นต้องนำเข้าแพ็คเกจที่จำเป็นจากไลบรารี Aspose.PSD ต่อไปนี้คือวิธีที่คุณสามารถทำได้:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
ด้วยการนำเข้าแพ็คเกจเหล่านี้ เราจะสามารถเข้าถึงคลาสที่จำเป็นสำหรับการโหลด แก้ไข และบันทึกไฟล์ PSD ของเรา

ตอนนี้ เรามาแบ่งกระบวนการออกเป็นขั้นตอนย่อยๆ กัน ปฏิบัติตามในขณะที่เราดำเนินการโหลดไฟล์ PSD ปรับระดับ จากนั้นบันทึกการเปลี่ยนแปลงของคุณ 
## ขั้นตอนที่ 1: ตั้งค่าเส้นทางไฟล์ของคุณ
ขั้นตอนแรกคือการกำหนดตำแหน่งของไฟล์ PSD ของเรา และตำแหน่งที่เราต้องการบันทึกเอาต์พุตที่แก้ไข คุณสามารถปรับแต่งเส้นทางไดเร็กทอรีให้เหมาะกับความต้องการของคุณได้
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
 นี่ครับ แทนที่`"Your Document Directory"`ด้วยเส้นทางจริงในระบบของคุณที่เก็บไฟล์ PSD ของคุณ นี่เป็นการปูทางสำหรับทุกสิ่งที่เราจะทำต่อไป
## ขั้นตอนที่ 2: โหลดไฟล์ PSD
 ตอนนี้เรามาโหลดไฟล์ PSD โดยใช้นามสกุลไฟล์`PsdImage` ระดับ. ขั้นตอนนี้มีความสำคัญเนื่องจากช่วยให้เราสามารถเข้าถึงและจัดการเลเยอร์ได้
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 เมื่อคุณโทร`Image.load()` มันจะอ่านไฟล์ PSD และสร้างอินสแตนซ์ของ`PsdImage` ที่คุณสามารถทำงานได้
## ขั้นตอนที่ 3: วนซ้ำผ่านเลเยอร์
เนื่องจากเราต้องการปรับระดับ Layer Adjustment เราจึงต้องวนซ้ำแต่ละเลเยอร์ในไฟล์ PSD ของเรา สิ่งนี้ช่วยให้เราค้นหาเลเยอร์เฉพาะที่เราต้องการแก้ไข
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // การจัดการเพิ่มเติมจะไปที่นี่...
    }
}
```
 ในวงนี้`instanceof LevelsLayer` ตรวจสอบว่าเลเยอร์ปัจจุบันเป็นเลเยอร์การปรับระดับหรือไม่ หากเป็นเช่นนั้น เราก็สามารถปรับแต่งคุณสมบัติของมันต่อไปได้
## ขั้นตอนที่ 4: ปรับการตั้งค่าช่องระดับ
เมื่อเราระบุเลเยอร์ที่ถูกต้องแล้ว เราก็สามารถปรับเปลี่ยนระดับอินพุตและเอาท์พุตของมันได้ นี่คือจุดที่ความมหัศจรรย์เกิดขึ้น! ปรับพารามิเตอร์ต่างๆ เพื่อดูว่าส่งผลต่อภาพอย่างไร
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
ต่อไปนี้คือสิ่งที่แต่ละพารามิเตอร์ทำ:
- ระดับอินพุตเสียงกลาง: ปรับโทนเสียงกลาง
- ระดับเงาอินพุต: ปรับแต่งบริเวณที่มืดกว่าของภาพ
- ระดับไฮไลท์อินพุต: เปลี่ยนบริเวณที่สว่างของภาพ
- ระดับเงาเอาท์พุต: กำหนดว่าเงามืดจะปรากฏอย่างไร
- ระดับไฮไลท์เอาท์พุต: ตั้งค่าว่าแสงไฮไลท์จะปรากฏอย่างไร
รู้สึกอิสระที่จะทดลองกับค่าต่างๆ!
## ขั้นตอนที่ 5: บันทึกไฟล์ PSD ที่แก้ไข
ตอนนี้เราได้ทำการปรับเปลี่ยนแล้ว ก็ถึงเวลาบันทึกไฟล์ PSD ที่แก้ไขแล้ว ขั้นตอนนี้มีความสำคัญเพื่อให้แน่ใจว่าการเปลี่ยนแปลงของคุณจะถูกนำไปใช้และจัดเก็บ
```java
im.save(psdPathAfterChange);
```
 ตอนนี้คุณสามารถค้นหาไฟล์ PSD ที่ปรับแต่งแล้วได้ตามที่ระบุ`psdPathAfterChange`. 
## บทสรุป
คุณเพิ่งเรียนรู้วิธีเพิ่ม Level Adjustment Layer ให้กับไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java! ด้วยการทำตามคำแนะนำนี้ คุณสามารถปรับคุณภาพโทนสีของภาพของคุณได้อย่างง่ายดาย ปูทางไปสู่ผลลัพธ์ที่สดใสและน่าดึงดูดยิ่งขึ้น โปรดจำไว้ว่า การฝึกฝนทำให้สมบูรณ์แบบ ดังนั้นอย่าลังเลที่จะปรับแต่งการปรับแต่งและสำรวจไฟล์ PSD ต่างๆ เพื่อดูผลกระทบของการเปลี่ยนแปลงของคุณ
## คำถามที่พบบ่อย
### เลเยอร์การปรับระดับคืออะไร?
เลเยอร์การปรับระดับช่วยให้คุณสามารถแก้ไขช่วงโทนสีในภาพของคุณ ปรับสมดุลเงา มิดโทน และไฮไลต์ได้
### ฉันสามารถใช้ Aspose.PSD โดยไม่ต้องซื้อได้หรือไม่
ใช่! Aspose เสนอให้ทดลองใช้ฟรีเพื่อทดสอบห้องสมุดก่อนซื้อ
### ฉันจะหาเอกสารสำหรับ Aspose.PSD ได้ที่ไหน
 คุณสามารถค้นหาเอกสาร[ที่นี่](https://reference.aspose.com/psd/java/).
### มีการสนับสนุนจากชุมชนสำหรับผลิตภัณฑ์ Aspose หรือไม่?
 อย่างแน่นอน! คุณสามารถถามคำถามและรับการสนับสนุนได้ใน[ฟอรั่ม Aspose](https://forum.aspose.com/c/psd/34).
### ฉันจะรับใบอนุญาตชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร
 คุณสามารถยื่นขอใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).