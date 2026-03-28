---
date: 2026-03-28
description: เรียนรู้วิธีสร้างเลเยอร์ฟิลเตอร์ภาพและเพิ่มเลเยอร์ปรับแต่งไฟล์ PSD ด้วย
  Aspose.PSD สำหรับ Java. ปฏิบัติตามคำแนะนำนี้เพื่อแก้ไขและเพิ่มฟิลเตอร์ได้อย่างง่ายดาย.
linktitle: How to Create Photo Filter Layer in PSD Using Java
second_title: Aspose.PSD Java API
title: วิธีสร้างเลเยอร์ฟิลเตอร์รูปภาพใน PSD ด้วย Java
url: /th/java/psd-image-modification-conversion/manage-photo-filter-adjustment-layer-psd/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# จัดการเลเยอร์การปรับแต่ง Photo Filter ใน PSD - Java

## บทนำ
หากคุณเป็นนักพัฒนา Java ที่ต้องการ **สร้างเลเยอร์ฟิลเตอร์รูปภาพ** ภายในไฟล์ PSD คุณมาถูกที่แล้ว ในบทแนะนำนี้เราจะอธิบายการใช้ Aspose.PSD for Java เพื่อแก้ไข Photo Filter Adjustment Layers ที่มีอยู่และเพิ่มเลเยอร์ใหม่ ๆ เมื่อจบคุณจะรู้วิธี **สร้างเลเยอร์ฟิลเตอร์รูปภาพ** ปรับคุณสมบัติต่าง ๆ ของมัน และแม้กระทั่ง **เพิ่มเลเยอร์การปรับแต่ง PSD** อย่างอัตโนมัติ—ช่วยเร่งกระบวนการออกแบบกราฟิกของคุณ

## คำตอบสั้น
- **ไลบรารีใดจัดการเลเยอร์ PSD ใน Java?** Aspose.PSD for Java  
- **ฉันสามารถแก้ไขเลเยอร์ Photo Filter ที่มีอยู่ได้หรือไม่?** ใช่ – โหลดไฟล์ PSD, ค้นหา `PhotoFilterLayer`, แล้วแก้ไขคุณสมบัติของมัน  
- **ฉันจะเพิ่มเลเยอร์ฟิลเตอร์ใหม่อย่างไร?** ใช้ `addPhotoFilterLayer(Color)` บนอินสแตนซ์ `PsdImage`  
- **ต้องใช้ลิขสิทธิ์สำหรับการใช้งานจริงหรือไม่?** จำเป็นต้องมีลิขสิทธิ์เชิงพาณิชย์; มีรุ่นทดลองฟรีให้ใช้  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** JDK 8 หรือสูงกว่า (แนะนำ JDK 11)

## Photo Filter Adjustment Layer คืออะไร?
Photo Filter Adjustment Layer คือเอฟเฟกต์แบบไม่ทำลายข้อมูลที่ทำให้ภาพทั้งหมดเปลี่ยนสีด้วยสีที่เลือกไว้ คล้ายกับการใช้ฟิลเตอร์ถ่ายภาพ มันอยู่บนเลเยอร์ของตนเอง ทำให้คุณปรับสี ความหนาแน่น และความสว่างได้โดยไม่กระทบพิกเซลต้นฉบับ

## ทำไมต้องใช้ Aspose.PSD เพื่อสร้างเลเยอร์ฟิลเตอร์รูปภาพ?
- **การควบคุมเต็มรูปแบบ** ของโครงสร้าง PSD โดยไม่ต้องใช้ Adobe Photoshop  
- **ข้ามแพลตฟอร์ม** Java API ทำงานบน Windows, Linux, และ macOS  
- **ไม่มี COM interop** – เป็น Java แท้ ๆ เหมาะสำหรับการประมวลผลฝั่งเซิร์ฟเวอร์  
- **รองรับ PSD เวอร์ชัน 1‑8** รักษาเอฟเฟกต์และมาสก์ของเลเยอร์ไว้

## ข้อกำหนดเบื้องต้น
### ซอฟต์แวร์ที่จำเป็น
1. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณมี JDK รุ่นที่เข้ากันได้ติดตั้งบนเครื่องของคุณ คุณสามารถดาวน์โหลดได้จาก [เว็บไซต์ของ Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java: เพื่อจัดการไฟล์ PSD คุณจะต้องใช้ไลบรารี Aspose.PSD คุณสามารถดาวน์โหลดได้จาก [หน้า releases ของ Aspose](https://releases.aspose.com/psd/java/). อย่าลืมตรวจสอบ [เอกสารของ Aspose](https://reference.aspose.com/psd/java/) สำหรับรายละเอียดเพิ่มเติม.
3. IDE (Integrated Development Environment): IDE ที่ดีเช่น IntelliJ IDEA หรือ Eclipse จะทำให้ประสบการณ์การเขียนโค้ดของคุณราบรื่นยิ่งขึ้น.

### ทำความเข้าใจพื้นฐาน
การคุ้นเคยกับการเขียนโปรแกรม Java และความเข้าใจพื้นฐานเกี่ยวกับการทำงานของไฟล์ PSD จะเป็นประโยชน์ หากคุณใหม่กับการใช้ไลบรารีใน Java ควรทำความคุ้นเคยกับการนำเข้าและใช้งานเฟรมเวิร์กต่าง ๆ

## นำเข้าแพ็กเกจ
เพื่อเริ่มต้น เราต้องนำเข้าคลาสที่จำเป็นจากไลบรารี Aspose.PSD นี่คือตัวอย่างคำสั่ง import ที่คุณต้องใส่ที่ส่วนต้นของไฟล์ Java ของคุณ:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PhotoFilterLayer;
```
คัดลอกโค้ดนี้ไปวางที่ส่วนบนของไฟล์ Java ของคุณ แล้วคุณก็พร้อมเริ่มทำงานกับภาพ PSD แล้ว!

## การแก้ไขเลเยอร์ Photo Filter ที่มีอยู่
### ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีข้อมูล
ก่อนอื่นคุณต้องกำหนดไดเรกทอรีที่เก็บไฟล์ PSD ของคุณ แทนที่ `"Your Document Directory"` ด้วยพาธจริง นี่คือวิธีจัดระเบียบไฟล์ทั้งหมด:
```java
String dataDir = "Your Document Directory";
```

### ขั้นตอนที่ 2: โหลดไฟล์ PSD ของคุณ
ต่อไปให้โหลดไฟล์ PSD ที่คุณต้องการแก้ไข ตรวจสอบให้แน่ใจว่า `PhotoFilterAdjustmentLayer.psd` มีอยู่ในไดเรกทอรีที่กำหนด
```java
String sourceFileName = dataDir + "PhotoFilterAdjustmentLayer.psd";
```

### ขั้นตอนที่ 3: เริ่มต้นอ็อบเจ็กต์ภาพ
โดยใช้ฟังก์ชันในตัวของ Aspose เราจะโหลดภาพเข้าสู่โปรเจกต์ของเรา:
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### ขั้นตอนที่ 4: วนลูปผ่านเลเยอร์
ต่อไปเราจะตรวจสอบเลเยอร์ภายในไฟล์ PSD เป้าหมายของเราคือค้นหา `PhotoFilterLayer`:
```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof PhotoFilterLayer) {
        PhotoFilterLayer photoLayer = (PhotoFilterLayer) im.getLayers()[i];
        // Make changes to the layer
    }
}
```

### ขั้นตอนที่ 5: ปรับแต่งเลเยอร์ Photo Filter
นี่คือจุดที่ความมหัศจรรย์เกิดขึ้น! คุณสามารถแก้ไข `Color` และ `Density` ตัวอย่างเช่น เราสามารถตั้งค่าสีเป็นสีแดงสดและปรับความหนาแน่นได้:
```java
photoLayer.setColor(Color.fromArgb(255, 60, 60));
photoLayer.setDensity(78);
photoLayer.setPreserveLuminosity(false);
```

### ขั้นตอนที่ 6: บันทึกไฟล์ PSD ที่แก้ไขแล้ว
สุดท้ายบันทึกการเปลี่ยนแปลงเพื่อสร้างไฟล์ PSD ใหม่ที่มีการปรับแต่งของคุณ:
```java
String psdPathAfterChange = dataDir + "PhotoFilterAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
คุณเพิ่งแก้ไข Photo Filter Adjustment Layer ในไฟล์ PSD แล้ว

## การเพิ่มเลเยอร์ Photo Filter ใหม่
### ขั้นตอนที่ 1: ตั้งค่าเส้นทางไดเรกทอรี
เช่นเดียวกับก่อนหน้า เราเริ่มด้วยการกำหนดไดเรกทอรีข้อมูลของเรา:
```java
String dataDir = "Your Document Directory";
```

### ขั้นตอนที่ 2: โหลดไฟล์ต้นฉบับ
ในตัวอย่างนี้ ให้โหลดไฟล์ PSD อื่นที่เราต้องการ **เพิ่มเลเยอร์การปรับแต่ง PSD**:
```java
String sourceFileName = dataDir + "PhotoExample.psd";
```

### ขั้นตอนที่ 3: เริ่มต้นอ็อบเจ็กต์ภาพอีกครั้ง
เราต้องสร้างอินสแตนซ์ `PsdImage` ใหม่ ดังนั้นจึงโหลดไฟล์:
```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### ขั้นตอนที่ 4: เพิ่มเลเยอร์ Photo Filter
ตอนนี้เราสามารถเพิ่มเลเยอร์ Photo Filter ใหม่ด้วยสีที่กำหนดเองได้ นี่คือวิธีทำ:
```java
PhotoFilterLayer layer = img.addPhotoFilterLayer(Color.fromArgb(25, 255, 35));
```

### ขั้นตอนที่ 5: บันทึกไฟล์ PSD ใหม่
อีกครั้งหนึ่ง ถึงเวลาบันทึกการเปลี่ยนแปลงของเรา นี่คือบรรทัดที่ทำเช่นนั้น:
```java
String psdPathAfterChange = dataDir + "PhotoExampleAddedPhotoFilter.psd";
img.save(psdPathAfterChange);
```
คุณได้เพิ่มเลเยอร์ฟิลเตอร์รูปภาพใหม่ลงในไฟล์ PSD ของคุณสำเร็จแล้ว

## ปัญหาที่พบบ่อยและวิธีแก้
- **`ClassCastException` เมื่อโหลดภาพ** – ตรวจสอบให้แน่ใจว่าไฟล์ที่โหลดเป็น PSD; รูปแบบอื่นต้องใช้คลาสที่แตกต่างกัน  
- **ค่าของสีแสดงผลไม่ถูกต้อง** – ใช้ `Color.fromArgb(alpha, red, green, blue)` โดยแต่ละคอมโพเนนต์ต้องอยู่ในช่วง 0‑255  
- **ไม่พบเลเยอร์** – ยืนยันว่า PSD ต้นทางมี `PhotoFilterLayer` อยู่จริง ใช้ `im.getLayers().length` เพื่อตรวจสอบ

## คำถามที่พบบ่อย
### Aspose.PSD คืออะไร?
Aspose.PSD คือไลบรารีสำหรับ .NET และ Java ที่ใช้สร้าง แก้ไข และแปลงไฟล์ PSD

### ฉันสามารถทดลองใช้ Aspose.PSD ได้ฟรีหรือไม่?
ใช่, Aspose มีรุ่นทดลองฟรี ตรวจสอบได้ [ที่นี่](https://releases.aspose.com/).

### ฉันจะหาเอกสารได้จากที่ไหน?
คุณสามารถค้นหาเอกสารเต็มรูปแบบได้ที่ [หน้าอ้างอิงของ Aspose](https://reference.aspose.com/psd/java/).

### ฉันจะซื้อ Aspose.PSD ได้อย่างไร?
คุณสามารถซื้อซอฟต์แวร์ได้จาก [ลิงก์นี้](https://purchase.aspose.com/buy).

### มีการสนับสนุนสำหรับ Aspose.PSD หรือไม่?
แน่นอน! คุณสามารถรับการสนับสนุนผ่านฟอรั่มของ Aspose [ที่นี่](https://forum.aspose.com/c/psd/34).

---

**อัปเดตล่าสุด:** 2026-03-28  
**ทดสอบด้วย:** Aspose.PSD for Java 24.11 (latest as of 2026)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}