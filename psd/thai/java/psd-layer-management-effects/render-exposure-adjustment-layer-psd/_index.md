---
title: เรนเดอร์เลเยอร์การปรับค่าแสงในไฟล์ PSD - Java
linktitle: เรนเดอร์เลเยอร์การปรับค่าแสงในไฟล์ PSD - Java
second_title: Aspose.PSD Java API
description: เรียนรู้วิธีเรนเดอร์และปรับเลเยอร์การรับแสงในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java คำแนะนำทีละขั้นตอนพร้อมตัวอย่างโค้ดสำหรับการแก้ไขและเพิ่มเลเยอร์การสัมผัส
type: docs
weight: 15
url: /th/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
---
## การแนะนำ

คุณทำงานกับไฟล์ Photoshop PSD และจำเป็นต้องปรับระดับแสงหรือเพิ่มเลเยอร์การปรับแสงโดยทางโปรแกรมหรือไม่ ไม่ว่าคุณจะปรับแต่งเลเยอร์ที่มีอยู่หรือเพิ่มเลเยอร์ใหม่ Aspose.PSD สำหรับ Java มอบวิธีที่มีประสิทธิภาพและใช้งานง่ายในการจัดการงานเหล่านี้ ในคู่มือนี้ เราจะอธิบายวิธีใช้ Aspose.PSD สำหรับ Java เพื่อเรนเดอร์และแก้ไขเลเยอร์การปรับแสงในไฟล์ PSD ในตอนท้ายของบทช่วยสอนนี้ คุณจะรู้วิธีปรับการตั้งค่าการรับแสงในเลเยอร์ที่มีอยู่ และเพิ่มเลเยอร์การปรับการรับแสงใหม่ให้กับไฟล์ PSD ของคุณ มาดำน้ำกันเถอะ!

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:

1. Java Development Kit (JDK): คุณต้องติดตั้ง JDK บนเครื่องของคุณ คู่มือนี้ถือว่าคุณมีอย่างน้อย JDK 8
2.  Aspose.PSD สำหรับ Java: คุณต้องมีไลบรารี Aspose.PSD เพื่อทำงานกับไฟล์ PSD คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/psd/java/).
3. ความรู้พื้นฐานของ Java: ความคุ้นเคยกับการเขียนโปรแกรม Java จะช่วยให้คุณปฏิบัติตามได้อย่างง่ายดาย
4. IDE หรือตัวแก้ไขข้อความ: ใช้ IDE ใดก็ได้ เช่น IntelliJ IDEA, Eclipse หรือตัวแก้ไขข้อความที่คุณเลือกเพื่อเขียนและรันโค้ด Java

## แพ็คเกจนำเข้า

ก่อนอื่น เรามานำเข้าแพ็คเกจที่จำเป็นจาก Aspose.PSD สำหรับ Java กันก่อน ขั้นตอนนี้ทำให้แน่ใจได้ว่าโค้ดของเราสามารถใช้คุณลักษณะของไลบรารีเพื่อจัดการไฟล์ PSD ได้

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## ขั้นตอนที่ 1: โหลดไฟล์ PSD

ในการเริ่มต้น คุณต้องโหลดไฟล์ PSD ของคุณลงในแอปพลิเคชัน ต่อไปนี้คือวิธีที่คุณสามารถทำได้:

```java
String dataDir = "Your Document Directory";  // กำหนดไดเร็กทอรีเอกสารของคุณ
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  // เส้นทางไฟล์ PSD ต้นฉบับ

PsdImage im = (PsdImage) Image.load(sourceFileName);  // โหลดไฟล์ PSD
```

 ในข้อมูลโค้ดนี้ ให้แทนที่`"Your Document Directory"` พร้อมเส้นทางที่ไฟล์ PSD ของคุณอยู่ ที่`Image.load()` วิธีการโหลดไฟล์ PSD ลงในอินสแตนซ์ของ`PsdImage`ซึ่งช่วยให้คุณจัดการเลเยอร์ของมันได้

## ขั้นตอนที่ 2: แก้ไขเลเยอร์การปรับค่าแสงที่มีอยู่

เมื่อโหลดไฟล์ PSD แล้ว คุณจะสามารถเข้าถึงและแก้ไขเลเยอร์ที่มีอยู่ได้ หากไฟล์มีเลเยอร์การปรับแสง คุณสามารถปรับคุณสมบัติของมันได้:

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  // ปรับระดับการรับแสง
        expLayer.setOffset(-0.25f);  // ตั้งค่าออฟเซ็ต
        expLayer.setGammaCorrection(0.5f);  // ปรับการแก้ไขแกมมา
    }
}
```

ในลูปนี้ เราจะวนซ้ำไฟล์ PSD ทุกเลเยอร์ ถ้าเราพบว่ามี`ExposureLayer` เราแก้ไขมัน`Exposure`, `Offset` , และ`GammaCorrection` คุณสมบัติ. สิ่งนี้ช่วยให้คุณปรับแต่งเอาท์พุตภาพของเลเยอร์การปรับแสงได้อย่างละเอียด

## ขั้นตอนที่ 3: บันทึกไฟล์ PSD ที่แก้ไข

หลังจากทำการเปลี่ยนแปลง คุณจะต้องบันทึกไฟล์ PSD ที่อัปเดต:

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  // เส้นทางในการบันทึกไฟล์ PSD ที่แก้ไข

im.save(psdPathAfterChange);  // บันทึกการเปลี่ยนแปลงในไฟล์ PSD
```

บรรทัดนี้จะบันทึกไฟล์ PSD ที่แก้ไขไปยังเส้นทางที่ระบุ โดยคงการปรับค่าแสงของคุณไว้

## ขั้นตอนที่ 4: ส่งออกเป็น PNG

หากต้องการส่งออกไฟล์ PSD ที่อัปเดตเป็น PNG ให้ทำตามขั้นตอนเหล่านี้:

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // เส้นทางในการบันทึกไฟล์ PNG

PngOptions saveOptions = new PngOptions();  // สร้างตัวเลือก PNG
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  // ตั้งค่าประเภทสีเป็น Truecolor ด้วย Alpha

im.save(pngExportPath, saveOptions);  // บันทึกเป็น PNG
```

 ที่นี่,`PngOptions` ใช้เพื่อกำหนดการตั้งค่าการส่งออก PNG`PngColorType.TruecolorWithAlpha` ช่วยให้มั่นใจได้ว่าไฟล์ PNG จะคงความลึกของสีและความโปร่งใสไว้

## ขั้นตอนที่ 5: เพิ่มเลเยอร์การปรับค่าแสงใหม่

หากคุณต้องการเพิ่มเลเยอร์การปรับแสงใหม่ให้กับไฟล์ PSD ที่มีอยู่ คุณสามารถทำได้โดยใช้โค้ดต่อไปนี้:

```java
String sourceFileName = dataDir + "PhotoExample.psd";  // เส้นทางไฟล์ PSD ต้นฉบับ

PsdImage img = (PsdImage) Image.load(sourceFileName);  // โหลดไฟล์ PSD

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  // เพิ่มเลเยอร์การปรับแสงใหม่

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  // เส้นทางในการบันทึกไฟล์ PSD ที่แก้ไข
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // เส้นทางในการบันทึกไฟล์ PNG

img.save(psdPathAfterChange);  // บันทึกการเปลี่ยนแปลงในไฟล์ PSD

PngOptions options = new PngOptions();  // สร้างตัวเลือก PNG
options.setColorType(PngColorType.TruecolorWithAlpha);  // ตั้งค่าประเภทสีเป็น Truecolor ด้วย Alpha

img.save(pngExportPath, options);  // บันทึกเป็น PNG
```

ในขั้นตอนนี้ เลเยอร์การปรับค่าแสงใหม่จะถูกเพิ่มลงในไฟล์ PSD พร้อมค่าการแก้ไขค่าแสง ออฟเซ็ต และแกมม่าที่ระบุ จากนั้นไฟล์ PSD และ PNG ที่อัปเดตจะถูกบันทึก

## บทสรุป

และคุณก็ได้แล้ว! คุณได้เรียนรู้วิธีเรนเดอร์และปรับเลเยอร์การรับแสงในไฟล์ PSD โดยใช้ Aspose.PSD สำหรับ Java แล้ว เราได้กล่าวถึงวิธีการแก้ไขเลเยอร์แสงที่มีอยู่ เพิ่มเลเยอร์ใหม่ และส่งออกงานของคุณเป็นไฟล์ PNG ไม่ว่าคุณจะปรับแต่งรูปภาพหรือเตรียมเนื้อหาการออกแบบ ทักษะเหล่านี้จะช่วยเพิ่มความสามารถในการจัดการไฟล์ PSD โดยทางโปรแกรม ขอให้มีความสุขในการเขียนโค้ด!

## คำถามที่พบบ่อย

### Aspose.PSD สำหรับ Java คืออะไร

Aspose.PSD สำหรับ Java เป็นไลบรารีที่ช่วยให้คุณสามารถสร้าง แก้ไข และแปลงไฟล์ PSD โดยทางโปรแกรมโดยใช้ Java มีฟังก์ชันการทำงานที่ครอบคลุมสำหรับการทำงานกับเอกสาร Photoshop

### ฉันสามารถใช้ Aspose.PSD สำหรับ Java เพื่อจัดการเลเยอร์ประเภทอื่นได้หรือไม่

ใช่ Aspose.PSD สำหรับ Java รองรับเลเยอร์หลายประเภท รวมถึงเลเยอร์ข้อความ เลเยอร์การปรับ และเลเยอร์รูปภาพ ทำให้สามารถจัดการไฟล์ PSD ได้อย่างกว้างขวาง

### ฉันจะเริ่มต้นใช้งาน Aspose.PSD สำหรับ Java ได้อย่างไร

 คุณสามารถเริ่มต้นด้วยการดาวน์โหลดไลบรารี่จาก[เว็บไซต์](https://releases.aspose.com/psd/java/) และอ้างถึง[เอกสารประกอบ](https://reference.aspose.com/psd/java/) สำหรับคำแนะนำและตัวอย่างโดยละเอียด

### มีการทดลองใช้ฟรีสำหรับ Aspose.PSD สำหรับ Java หรือไม่

 ใช่ มีให้ทดลองใช้ฟรี คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/).

### ฉันจะรับการสนับสนุน Aspose.PSD สำหรับ Java ได้อย่างไร

 สำหรับการสนับสนุนคุณสามารถเยี่ยมชมที่[กำหนดฟอรั่มการสนับสนุน](https://forum.aspose.com/c/psd/34) ที่ซึ่งคุณสามารถถามคำถามและรับความช่วยเหลือจากชุมชนได้