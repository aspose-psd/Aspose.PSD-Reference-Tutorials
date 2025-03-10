---
title: ใช้เลเยอร์การปรับในไฟล์ PSD โดยใช้ Java
linktitle: ใช้เลเยอร์การปรับในไฟล์ PSD โดยใช้ Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีใช้เลเยอร์การปรับในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java ในคำแนะนำทีละขั้นตอนสำหรับนักพัฒนา
weight: 15
url: /th/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ใช้เลเยอร์การปรับในไฟล์ PSD โดยใช้ Java

## การแนะนำ
คุณเป็นนักพัฒนา Java ที่ต้องการปรับปรุงภาพที่จัดเก็บไว้ในไฟล์ PSD หรือไม่? ถ้าเป็นเช่นนั้น คุณมาถูกที่แล้ว! ในบทความนี้ เราจะสำรวจวิธีการใช้เลเยอร์การปรับในไฟล์ PSD โดยใช้ไลบรารี Aspose.PSD สำหรับ Java ไม่ว่าคุณจะทำงานในโครงการส่วนตัวหรือแอปพลิเคชันระดับมืออาชีพ การทำความเข้าใจวิธีจัดการไฟล์ PSD สามารถยกระดับความสามารถของซอฟต์แวร์ของคุณได้อย่างมาก 

## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะพูดถึงโค้ดและเริ่มใช้เลเยอร์การปรับเปลี่ยนเหล่านั้น มีข้อกำหนดเบื้องต้นบางประการที่คุณต้องมี:
1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK บนเครื่องของคุณแล้ว คุณสามารถดาวน์โหลดได้จาก[เว็บไซต์ของออราเคิล](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2.  ไลบรารี Aspose.PSD: หากคุณยังไม่ได้ดาวน์โหลด คุณจะต้องดาวน์โหลดไลบรารี Aspose.PSD สำหรับ Java คุณสามารถหามันได้[ที่นี่](https://releases.aspose.com/psd/java/).
3. สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนาแบบรวม Java (IDE) เช่น IntelliJ IDEA หรือ Eclipse ซึ่งคุณจะเขียนและรันโค้ดของคุณ
4. ความคุ้นเคยขั้นพื้นฐานกับ Java: ความเข้าใจทั่วไปเกี่ยวกับการเขียนโปรแกรม Java จะช่วยให้คุณปฏิบัติตามได้อย่างราบรื่น
5. ไฟล์ PSD: มีไฟล์ PSD สองสามไฟล์อยู่ในมือเพื่อการทดสอบ คุณสามารถสร้างบางส่วนได้โดยใช้ Adobe Photoshop หรือดาวน์โหลดไฟล์ตัวอย่างจากอินเทอร์เน็ต
## แพ็คเกจนำเข้า
ก่อนที่เราจะเริ่มเขียนโค้ด เรามาทำความเข้าใจก่อนว่าแพ็คเกจใดบ้างที่เราต้องนำเข้า Aspose.PSD ช่วยให้เราสามารถทำงานกับไฟล์ Photoshop ได้หลายวิธี ดังนั้นเรามาเรียนคลาสที่จำเป็นเพื่อจัดการรูปภาพ PSD และเลเยอร์การปรับกันดีกว่า
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.AdjustmentLayer;
```
ตอนนี้เรามีแพ็คเกจพร้อมแล้ว เรามาแจกแจงตัวอย่างทีละขั้นตอนกันดีกว่า!
## ขั้นตอนที่ 1: โหลดไฟล์ PSD
ขั้นตอนแรกในการเดินทางของเราคือการโหลดไฟล์ PSD นี่คือไฟล์ที่เราจะใช้งานเพื่อใช้เลเยอร์การปรับเปลี่ยนของเรา
```java
String dataDir = "Your Document Directory";
String sourceFileName1 = dataDir + "ChannelMixerAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName1);
```
 ในตัวอย่างนี้ เรากำหนดไดเร็กทอรีที่มีไฟล์ PSD ของเราอยู่ และโหลดไฟล์เฉพาะที่เราต้องการจัดการ ตรวจสอบให้แน่ใจว่าได้เปลี่ยน`"Your Document Directory"` ด้วยเส้นทางจริงไปยังไฟล์ PSD ของคุณบนเครื่องของคุณ
## ขั้นตอนที่ 2: วนซ้ำเลเยอร์
ตอนนี้เราได้โหลดไฟล์ PSD แล้ว เราจะต้องวนซ้ำผ่านเลเยอร์ต่างๆ เพื่อค้นหาเลเยอร์การปรับแต่งของเรา
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) im.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(im.getLayers()[0]);
        }
    }
}
```
 ในขั้นตอนนี้ เราจะวนซ้ำแต่ละเลเยอร์ในไฟล์ PSD เพื่อระบุสิ่งที่เป็นของ`AdjustmentLayer` พิมพ์. หากเราพบเราจะรวมมันเข้ากับชั้นฐานซึ่งโดยปกติจะเป็นชั้นแรก (`im.getLayers()[0]`- กระบวนการผสานนี้ใช้การปรับภาพของเราอย่างมีประสิทธิภาพ 
## ขั้นตอนที่ 3: บันทึกไฟล์ PSD ที่แก้ไข
หลังจากแก้ไขเลเยอร์แล้ว สิ่งสำคัญคือต้องบันทึกการเปลี่ยนแปลงที่เราได้ทำไว้ เรามาทำสิ่งนี้กันในขั้นตอนถัดไป
```java
String exportPath1 = dataDir + "ChannelMixerAdjustmentLayerChanged.psd";
im.save(exportPath1);
```
 ที่นี่ เราระบุเส้นทางการส่งออกสำหรับไฟล์ PSD ที่แก้ไขแล้วของเรา และเรียกไฟล์`save()` วิธีการเขียนการเปลี่ยนแปลงของเราลงดิสก์
## ขั้นตอนที่ 4: เลเยอร์การปรับระดับ
ทำซ้ำขั้นตอนสำหรับเลเยอร์การปรับเปลี่ยนประเภทอื่น: เลเยอร์การปรับระดับ 
### โหลดเลเยอร์การปรับระดับ PSD
```java
String sourceFileName2 = dataDir + "LevelsAdjustmentLayerRgb.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName2);
```
เช่นเคย เราโหลดไฟล์ PSD ที่มีเลเยอร์การปรับระดับของเรา 
### วนซ้ำผ่านเลเยอร์ระดับ
ต่อไป เราจะวนซ้ำเลเยอร์ต่างๆ อีกครั้ง เช่นเดียวกับที่เราทำก่อนหน้านี้ แต่ตอนนี้เรากำลังทำงานกับไฟล์ PSD อื่น
```java
for (int i = 0; i < img.getLayers().length; i++) {
    if (img.getLayers()[i] instanceof AdjustmentLayer) {
        AdjustmentLayer adjustmentLayer = (AdjustmentLayer) img.getLayers()[i];
        
        if (adjustmentLayer != null) {
            adjustmentLayer.mergeLayerTo(img.getLayers()[0]);
        }
    }
}
```
รหัสนี้ทำหน้าที่คล้ายกับการวนซ้ำครั้งก่อน โดยจะค้นหาเลเยอร์การปรับภายในไฟล์ PSD ปัจจุบัน เพื่อให้เราสามารถปรับใช้การปรับใดๆ ที่มีอยู่ได้
## บันทึกเลเยอร์การปรับระดับ PSD
สุดท้าย เราจะบันทึกไฟล์ใหม่นี้หลังจากใช้การปรับเปลี่ยน
```java
String exportPath2 = dataDir + "LevelsAdjustmentLayerRgbChanged.psd";
img.save(exportPath2);
```
ตอนนี้เราได้ประมวลผลเลเยอร์การปรับระดับสำเร็จแล้ว!
## บทสรุป
ยินดีด้วย! คุณเพิ่งเรียนรู้วิธีใช้เลเยอร์การปรับในไฟล์ PSD โดยใช้ Java และไลบรารี Aspose.PSD ไม่ว่าคุณจะปรับแต่งสีหรือปรับระดับ ตอนนี้คุณมีทักษะพื้นฐานในการจัดการไฟล์ PSD โดยทางโปรแกรมแล้ว
การใช้ Aspose.PSD สามารถปรับปรุงขั้นตอนการทำงานในการแก้ไขภาพได้อย่างมาก ทำให้สามารถทำงานอัตโนมัติและปรับแต่งได้ในแบบที่เครื่องมือแบบเดิมอาจไม่สามารถทำได้ อย่าลังเลที่จะสำรวจห้องสมุดเพิ่มเติมและทดลองใช้เลเยอร์ประเภทต่างๆ เพื่อดูว่ามีความเป็นไปได้ที่สร้างสรรค์อะไรบ้าง
## คำถามที่พบบ่อย
### ไลบรารี Aspose.PSD คืออะไร
Aspose.PSD เป็นไลบรารีที่ช่วยให้นักพัฒนาโหลด จัดการ และบันทึกไฟล์ Photoshop PSD ในแอปพลิเคชัน Java
### ฉันสามารถใช้ Aspose.PSD ได้ฟรีหรือไม่
 ใช่! Aspose เสนอการทดลองใช้ฟรีให้คุณสำรวจห้องสมุดของพวกเขา คุณสามารถลงทะเบียนได้[ที่นี่](https://releases.aspose.com/).
### ฉันจำเป็นต้องติดตั้ง Photoshop เพื่อใช้ Aspose.PSD หรือไม่
ไม่ คุณไม่จำเป็นต้องมี Photoshop Aspose.PSD ทำงานอย่างอิสระเพื่อจัดการไฟล์ PSD โดยทางโปรแกรม
### ฉันจะหาเอกสารสำหรับ Aspose.PSD ได้ที่ไหน
คุณสามารถเยี่ยมชมหน้าเอกสารประกอบ[ที่นี่](https://reference.aspose.com/psd/java/) เพื่อสำรวจคุณสมบัติ คลาส และวิธีการ
### ฉันจะรับการสนับสนุนสำหรับผลิตภัณฑ์ Aspose ได้อย่างไร
 คุณสามารถเข้าถึงการสนับสนุนผ่านทาง[ฟอรั่ม Aspose](https://forum.aspose.com/c/psd/34) ที่คุณสามารถถามคำถามและค้นหาแนวทางแก้ไขได้
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
