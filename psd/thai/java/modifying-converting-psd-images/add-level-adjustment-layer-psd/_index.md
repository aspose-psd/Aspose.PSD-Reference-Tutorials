---
date: 2026-03-07
description: เรียนรู้วิธีปรับระดับโดยการเพิ่มเลเยอร์ปรับระดับในไฟล์ PSD ด้วย Aspose.PSD
  สำหรับ Java. เชี่ยวชาญการปรับโทนอย่างรวดเร็ว.
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
title: วิธีปรับระดับ – เพิ่มเลเยอร์การปรับระดับใน PSD
url: /th/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เพิ่มเลเยอร์ปรับระดับ (Level Adjustment Layer) ใน PSD

## คำนำ
หากคุณกำลังมองหา **วิธีปรับระดับ** ในเอกสาร Photoshop ของคุณ เลเยอร์ปรับระดับ (Level Adjustment Layer) คือเครื่องมือที่สมบูรณ์แบบ มันช่วยให้คุณปรับเงา, โทนกลาง, และไฮไลท์ได้อย่างละเอียดโดยไม่ทำให้พิกเซลต้นฉบับเปลี่ยนแปลงอย่างถาวร ในบทแนะนำนี้เราจะสาธิตการเพิ่มเลเยอร์ปรับระดับลงในไฟล์ PSD ด้วย Aspose.PSD for Java เพื่อให้คุณสามารถควบคุมโทนสีระดับมืออาชีพได้ในไม่กี่ขั้นตอน

## คำตอบสั้น
- **เลเยอร์ปรับระดับทำหน้าที่อะไร?** ปรับช่วงโทนของภาพแบบไม่ทำลายข้อมูลเดิม  
- **ใช้ไลบรารีอะไร?** Aspose.PSD for Java  
- **ต้องมีลิขสิทธิ์หรือไม่?** ทดลองใช้ฟรีสำหรับการพัฒนา; ต้องมีลิขสิทธิ์สำหรับการใช้งานจริง  
- **ใช้เวลานานเท่าไหร่ในการทำ?** ประมาณ 10‑15 นาทีสำหรับการปรับพื้นฐาน  
- **สามารถปรับหลายช่องสีได้หรือไม่?** ได้, คุณสามารถตั้งค่าระดับอินพุต/เอาต์พุตสำหรับแต่ละช่องสีแยกกัน

## เลเยอร์ปรับระดับคืออะไร?
เลเยอร์ปรับระดับช่วยให้คุณแก้ไขสมดุลโทนของภาพโดยปรับเงา, โทนกลาง, และไฮไลท์ รวมถึงระดับเอาต์พุต เนื่องจากเป็นเลเยอร์แยก คุณสามารถเปิด/ปิดการมองเห็นหรือทำการลบได้โดยไม่กระทบต่องานศิลปะที่อยู่ด้านล่าง

## ทำไมต้องเพิ่มเลเยอร์ปรับระดับด้วย Aspose.PSD?
- **อัตโนมัติ:** ผสานการปรับระดับเข้าในกระบวนการประมวลผลแบบชุด  
- **ข้ามแพลตฟอร์ม:** ทำงานบน OS ใดก็ได้ที่รองรับ Java  
- **ความแม่นยำ:** เข้าถึงการตั้งค่าของแต่ละช่องสีผ่านโค้ดเพื่อผลลัพธ์ที่แม่นยำ  

## ข้อกำหนดเบื้องต้น
1. Java Development Kit (JDK) หากยังไม่มีให้ดาวน์โหลดจาก [เว็บไซต์ Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) หรือใช้ OpenJDK  
2. ไลบรารี Aspose.PSD for Java – ดาวน์โหลด JAR ล่าสุดจาก [ลิงก์ดาวน์โหลดนี้](https://releases.aspose.com/psd/java/)  
3. ความรู้พื้นฐานด้านการเขียนโปรแกรม Java  
4. IDE เช่น IntelliJ IDEA, Eclipse หรือ NetBeans พร้อมเพิ่ม Aspose.PSD JAR เข้าไปใน classpath ของโปรเจกต์

## นำเข้าแพ็กเกจ
ก่อนเริ่มเขียนโค้ด เราต้องนำเข้าแพ็กเกจที่จำเป็นจากไลบรารี Aspose.PSD ดังนี้:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
การนำเข้าเหล่านี้ทำให้เราสามารถเข้าถึงคลาสสำหรับโหลดไฟล์ PSD, ทำงานกับเลเยอร์ปรับระดับ, และจัดการการตั้งค่าช่องสีแต่ละช่องได้

## วิธีปรับระดับในไฟล์ PSD
ต่อไปนี้เป็นขั้นตอนแบบละเอียดที่แสดง **วิธีปรับระดับ** ผ่านโค้ด

### ขั้นตอนที่ 1: ตั้งค่าเส้นทางไฟล์
กำหนดตำแหน่งที่เก็บไฟล์ PSD ต้นฉบับและที่ต้องการบันทึกไฟล์ที่แก้ไขแล้ว
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
เปลี่ยน `"Your Document Directory"` ให้เป็นโฟลเดอร์จริงบนเครื่องของคุณ

### ขั้นตอนที่ 2: โหลดไฟล์ PSD
สร้างอินสแตนซ์ `PsdImage` จากไฟล์ต้นฉบับ
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
ตอนนี้คุณสามารถเข้าถึงเลเยอร์ทั้งหมดภายใน PSD ได้เต็มที่

### ขั้นตอนที่ 3: วนลูปผ่านเลเยอร์
ค้นหาเลเยอร์ปรับระดับที่ต้องการแก้ไข
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
การตรวจสอบ `instanceof LevelsLayer` ทำให้เราทำงานเฉพาะกับเลเยอร์ปรับระดับเท่านั้น

### ขั้นตอนที่ 4: ปรับค่าการตั้งค่าช่องระดับ
ปรับค่าตัวอินพุตและเอาต์พุตสำหรับช่องที่เลือก
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
- **ระดับกลาง (Input Midtone Level):** ปรับช่วงโทนกลาง  
- **ระดับเงา (Input Shadow Level):** ทำให้เงามืดหรือสว่างขึ้น  
- **ระดับไฮไลท์ (Input Highlight Level):** ควบคุมส่วนที่สว่างที่สุด  
- **ระดับเงา/ไฮไลท์เอาต์พุต (Output Shadow/Highlight Levels):** กำหนดช่วงเอาต์พุตสุดท้าย  

ลองปรับค่าต่าง ๆ เพื่อดูผลกระทบต่อภาพของคุณ

### ขั้นตอนที่ 5: บันทึกไฟล์ PSD ที่แก้ไขแล้ว
บันทึกการเปลี่ยนแปลงลงไฟล์ใหม่
```java
im.save(psdPathAfterChange);
```
ไฟล์ PSD ที่อัปเดตจะอยู่ในตำแหน่งที่คุณระบุใน `psdPathAfterChange`

## ปัญหาที่พบบ่อยและวิธีแก้
- **ไฟล์ไม่พบ:** ตรวจสอบว่า `dataDir` ชี้ไปยังโฟลเดอร์ที่ถูกต้องและไฟล์ PSD ต้นฉบับมีอยู่จริง  
- **ClassCastException:** ยืนยันว่าไฟล์ที่โหลดเป็น PSD; รูปแบบอื่นต้องใช้คลาสที่ต่างกัน  
- **ข้อผิดพลาดลิขสิทธิ์:** ใช้ลิขสิทธิ์ Aspose.PSD ที่ถูกต้องสำหรับการสร้างเวอร์ชันผลิต; รุ่นทดลองใช้ได้สำหรับการพัฒนา

## สรุป
คุณได้เรียนรู้ **วิธีปรับระดับ** โดยการเพิ่มและกำหนดค่าเลเยอร์ปรับระดับในไฟล์ PSD ด้วย Aspose.PSD for Java เทคนิคนี้ให้การควบคุมโทนสีอย่างแม่นยำพร้อมรักษาการทำงานแบบอัตโนมัติเต็มรูปแบบ อย่าลืมทดลองค่าช่องต่าง ๆ และสำรวจการประมวลผลแบบชุดเพื่อปรับหลายภาพพร้อมกัน

## คำถามที่พบบ่อย

**ถาม: เลเยอร์ปรับระดับคืออะไร?**  
ตอบ: เป็นเลเยอร์ที่ไม่ทำลายข้อมูลซึ่งช่วยให้คุณแก้ไขช่วงโทน (เงา, โทนกลาง, ไฮไลท์) ของภาพได้

**ถาม: สามารถใช้ Aspose.PSD ได้โดยไม่ซื้อไลเซนส์หรือไม่?**  
ตอบ: ใช่, คุณสามารถประเมินไลบรารีด้วยรุ่นทดลองฟรี, แต่ต้องมีไลเซนส์สำหรับการใช้งานเชิงพาณิชย์

**ถาม: จะหาเอกสารของ Aspose.PSD ได้จากที่ไหน?**  
ตอบ: เอกสารสามารถดูได้ [ที่นี่](https://reference.aspose.com/psd/java/)

**ถาม: มีชุมชนสนับสนุนผลิตภัณฑ์ Aspose หรือไม่?**  
ตอบ: มีแน่นอน! คุณสามารถถามคำถามและรับความช่วยเหลือใน [ฟอรั่ม Aspose](https://forum.aspose.com/c/psd/34)

**ถาม: จะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.PSD ได้อย่างไร?**  
ตอบ: คุณสามารถสมัครขอไลเซนส์ชั่วคราว [ที่นี่](https://purchase.aspose.com/temporary-license/)

---

**อัปเดตล่าสุด:** 2026-03-07  
**ทดสอบด้วย:** เวอร์ชันล่าสุดของ Aspose.PSD (Java)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}